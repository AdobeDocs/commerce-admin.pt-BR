---
title: Instalar e configurar a integração do Experience Manager Assets
description: Saiba como instalar e configurar o [!DNL AEM Assets Integration for Adobe Commerce] em uma instância do Adobe Commerce.
feature: CMS, Media
exl-id: 2f8b3165-354d-4b7b-a46e-1ff46af553aa
source-git-commit: 521dd5c333e5753211127567532508156fbda5b4
workflow-type: tm+mt
source-wordcount: '1387'
ht-degree: 0%

---

# Instalar e configurar a Integração do AEM Assets para o Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Prepare seu ambiente do Commerce para usar a Integração do AEM Assets para o Commerce instalando a extensão PHP `aem-assets-integration`. Em seguida, atualize a configuração de Administrador para habilitar a comunicação e os fluxos de trabalho entre o Adobe Commerce e o AEM Assets.

## Requisitos do sistema

A integração do AEM Assets para Commerce tem os seguintes requisitos de sistema e configuração.

**Requisitos de software**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Compositor: 2.x

**Requisitos de configuração**

- Provisionamento e permissões de conta
   - [Administrador do projeto na nuvem do Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access)—Instale as extensões necessárias e configure o servidor de aplicativos do Commerce a partir do Administrador ou da linha de comando
   - [Administrador do Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview)—Atualize a configuração de armazenamento e gerencie as contas de usuário do Commerce

>[!TIP]
>
> O Adobe Commerce pode ser configurado para usar a [autenticação do Adobe IMS](/help/getting-started/adobe-ims-config.md).

## Visão geral da configuração

Habilite a integração concluindo as seguintes tarefas:

1. [Instalar a extensão de Integração do AEM Assets (`aem-assets-integration`)](#install-the-aem-assets-integration-extension).
1. [Configure o Commerce Services Connector](#configure-the-commerce-services-connector) para conectar sua instância do Adobe Commerce e com os serviços que permitem a transmissão de dados entre o Adobe Commerce e o AEM Assets.
1. [Configurar eventos de Adobe I/O para o Commerce](#configure-adobe-io-events-for-commerce)
1. [Obter credenciais de autenticação para acesso à API](#get-authentication-credentials-for-api-access)

## Instalar a extensão de Integração do AEM Assets

>[!BEGINSHADEBOX]

**Pré-requisito**

- Acesse [repo.magento.com](https://repo.magento.com/admin/dashboard) para instalar a extensão.

  Para geração de chaves e obtenção dos direitos necessários, consulte [Obter suas chaves de autenticação](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Para instalações na nuvem, consulte o [Guia de Infraestrutura do Commerce na Nuvem](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Acesso à linha de comando do servidor de aplicativos do Adobe Commerce.

>[!ENDSHADEBOX]

Instale a versão mais recente da extensão de Integração do AEM Assets (`aem-assets-integration`) em uma instância do Adobe Commerce com a versão Adobe Commerce 2.4.5+. A Integração de Ativos AEM é fornecida como um metapackage de compositor no [repositório.magento.com](https://repo.magento.com/admin/dashboard).

>[!BEGINTABS]

>[!TAB Infraestrutura em nuvem]

Use este método para instalar a extensão [!DNL AEM Assets Integration] para uma instância de Commerce Cloud.

1. Na estação de trabalho local, altere para o diretório do projeto do Adobe Commerce na infraestrutura em nuvem.

   >[!NOTE]
   >
   >Para obter informações sobre o gerenciamento local de ambientes de projeto do Commerce, consulte [Gerenciamento de ramificações com a CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) no _Guia do Usuário do Adobe Commerce na Infraestrutura da Nuvem_.

1. Confira a ramificação do ambiente para atualizar usando a CLI do Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Adicione a extensão Integração do AEM Assets para Commerce.

   ```shell
   composer require "magento/aem-assets-integration" "<version-tbd>" --no-update
   ```

1. Atualizar dependências de pacote.

   ```shell
   composer update "magento/aem-assets-integration"
   ```

1. Confirmar e enviar alterações de código para os arquivos `composer.json` e `composer.lock`.

1. Adicione, confirme e envie por push as alterações de código dos arquivos `composer.json` e `composer.lock` para o ambiente de nuvem.

   ```shell
   git add -A
   git commit -m "Install AEM Assets Integration extension for Adobe Commerce"
   git push origin <branch-name>
   ```

   O envio das atualizações inicia o [processo de implantação da nuvem do Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) para aplicar as alterações. Verifique o status da implantação no [log de implantação](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

>[!TAB No local]

Use este método para instalar a extensão [!DNL AEM Assets Integration] para uma instância local.

1. Use o Composer para adicionar a extensão do AEM Assets Integration for Commerce ao seu projeto:

   ```shell
   composer require "magento/aem-assets-integration" --no-update
   ```

1. Atualize as dependências e instale a extensão:

   ```shell
   composer update  "magento/aem-assets-integration"
   ```

1. Atualizar o Adobe Commerce:

   ```shell
   bin/magento setup:upgrade
   ```

1. Limpe o cache:

   ```shell
   bin/magento cache:clean
   ```

>[!TIP]
>
>Ao implantar na produção, considere não limpar o código compilado para economizar tempo. Sempre faça backup do sistema antes de fazer alterações.

>[!ENDTABS]

## Configurar o Commerce Services Connector

O Commerce Services Connector permite a sincronização e a comunicação de dados entre a instância do Commerce, o Serviço do mecanismo de regras do ativo e outros serviços de suporte.

>[!NOTE]
>
>A instalação do Commerce Services Connector é um processo único necessário para usar os [serviços SaaS do Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices). Se você já tiver configurado o conector para outro serviço, poderá ver a configuração existente no Administrador do Commerce selecionando **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]**.

Para transmitir dados entre sua instância do Adobe Commerce e os serviços que habilitam a Integração do AEM Assets, configure o Commerce Services Connector com o seguinte:

- Chaves de API de produção e sandbox para autenticação.
- Configure um espaço de dados (identificador SaaS) para armazenamento em nuvem seguro.
- Forneça a IMS organization ID na qual seus ambientes do Commerce e do AEM Assets são provisionados.

Para obter instruções detalhadas, consulte [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid).

Depois de configurar o Commerce Services Connector, o sistema gera o projeto SaaS e as IDs do banco de dados que identificam o ambiente de armazenamento em nuvem seguro para os Serviços da Commerce e exibe as IDs na configuração do administrador. Esses valores são necessários para concluir o processo de integração da sincronização de ativos.

![IDs de projeto e espaço de dados SaaS para integração com o AEM Assets](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Configurar eventos de Adobe I/O para o Commerce

A Integração do AEM Assets usa o serviço Adobe I/O Events para enviar dados de eventos personalizados entre a instância do Commerce e o Experience Cloud. Os dados do evento são usados para coordenar workflows para a integração do AEM Assets.

>[!BEGINSHADEBOX]

**Pré-requisito**

- Certifique-se de que o RabbitMQ esteja ativado e aguardando eventos.
   - [Instalação do RabbitMQ para Adobe Commerce no local](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - [Instalação do RabbitMQ para Adobe Commerce na infraestrutura em nuvem](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - Verifique se os [trabalhos cron estão habilitados](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration). Os trabalhos do Cron são necessários para comunicação e fluxos de trabalho para a integração do AEM Assets.

>[!NOTE]
>
> Para projetos na versão 2.4.5 do Commerce, você deve [instalar os módulos Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce). Na versão 2.4.6+ do Commerce, esses módulos são carregados automaticamente. Para a integração do AEM Assets com o Commerce, é necessário instalar apenas os módulos. A configuração do App Builder não é necessária.

>[!ENDSHADEBOX]

### Ativar a estrutura de eventos do Commerce

Ative a estrutura de eventos no Administrador do Commerce.

1. No Admin, vá para **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Adobe I/O Events**.

1. Expandir **[!UICONTROL Commerce events]**.

1. Defina **[!UICONTROL Enabled]** como `Yes`.

   ![Configuração do administrador do Adobe I/O Events Commerce - habilitar eventos do Commerce](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

1. Insira o nome da empresa de comerciante em **[!UICONTROL Merchant ID]** e o nome do ambiente em **[!UICONTROL Environment ID]** campos. Use somente caracteres alfanuméricos e sublinhados ao definir esses valores.

>[!BEGINSHADEBOX]

**Configurar VCL Personalizado para solicitações de bloqueio**

Se você usar um trecho de VCL personalizado para bloquear solicitações de entrada desconhecidas, talvez precise incluir o cabeçalho HTTP `X-Ims-Org-Idheader` para permitir conexões de entrada do serviço AEM Assets Integration for Commerce.

>[!TIP]
>
> Você pode usar o módulo Fastly CDN para criar uma ACL do Edge com uma lista de endereços IP que você deseja bloquear.

O seguinte código de trecho de VCL personalizado (formato JSON) mostra um exemplo com um cabeçalho de solicitação `X-Ims-Org-Id`.

```json
{
  "name": "blockbyuseragent",
  "dynamic": "0",
  "type": "recv",
  "priority": "5",
  "content": "if ( req.http.X-ims-org ~ \"<YOUR-IMS-ORG>\" ) {error 405 \"Not allowed\";}"
}
```

Antes de criar um trecho com base neste exemplo, revise os valores para determinar se você precisa fazer alterações:

- `name`: Nome do trecho VCL. Neste exemplo, usamos o nome `blockbyuseragent`.

- `dynamic`: Define a versão do trecho. Neste exemplo, usamos `0`. Consulte os [trechos de VCL do Fastly](https://www.fastly.com/documentation/reference/api/vcl-services/snippet/) para obter informações detalhadas sobre o modelo de dados.

- `type`: Especifica o tipo de trecho VCL, que determina o local do trecho no código VCL gerado. Neste exemplo, usamos `recv`, consulte a [referência de trecho Fastly VCL](https://docs.fastly.com/api/config#api-section-snippet) para obter a lista de tipos de trecho.

- `priority`: Determina quando o trecho VCL é executado. Este exemplo usa a prioridade `5` para executar imediatamente e verificar se uma solicitação de administrador vem de um endereço IP permitido.

- `content`: o trecho de código VCL a ser executado, que verifica o endereço IP do cliente. Se o IP estiver na ACL do Edge, o acesso será bloqueado com um erro `405 Not allowed` para todo o site. Todos os outros endereços IP de clientes têm acesso permitido.

Para obter informações detalhadas sobre o uso de trechos de VCL para bloquear solicitações de entrada, consulte [VCL personalizado para solicitações de bloqueio](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/cdn/custom-vcl-snippets/fastly-vcl-blocking) no _Guia de Infraestrutura do Commerce na Nuvem_.

>[!ENDSHADEBOX]

## Obter credenciais de autenticação para acesso à API

A integração do AEM Assets para o Commerce exige credenciais de autenticação do OAuth para permitir o acesso da API à instância do Commerce. Essas credenciais são necessárias para autenticar solicitações de API ao gerenciar ativos usando a integração do AEM Assets.

Gere as credenciais adicionando a integração à instância do Commerce e ativando-a.

### Adicionar a integração ao ambiente do Commerce

1. No Admin, vá para **Sistema** > Extensões > **Integrações** e clique em **Adicionar nova integração**.

1. Insira informações sobre a integração.

   Na seção **Geral**, especifique apenas o **Nome** e o **Email** da integração. Use o email para uma conta do Adobe IMS com acesso à organização em que o Commerce e o Experience Manager Assets são implantados.

   ![Integração do AEM Assets para a configuração do administrador do Commerce](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. Confirme sua identidade clicando em **Confirmar Identidade**.

   O sistema verifica sua identidade ao autenticar no Experience Cloud com sua ID de Adobe.

1. Configure os recursos da API.

   1. No painel esquerdo, clique em **[!UICONTROL API]**.

   1. Selecione o recurso de mídia externa **[!UICONTROL Catalog > Inventory > Products > External Media]**.

      ![Configuração de integração do administrador para recursos de API](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save]**.

### Gerar credenciais

Na página Integrações, gere as credenciais de autenticação do OAuth clicando em **Ativar** para a integração com o Assets. Você precisa dessas credenciais para registrar o projeto do Commerce com o serviço do Mecanismo de regras da Assets e para enviar solicitações de API para gerenciar ativos entre o Adobe Commerce e o AEM Assets.

1. Na página Integrações, gere as credenciais clicando em **[!UICONTROL Activate]**.

   ![Ativar a configuração do Commerce para integração com o Assets](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. Se você planeja usar a API, salve as credenciais da chave do consumidor e do token de acesso para configurar a autenticação no cliente da API.

   ![Credenciais OAuth para autenticar solicitações de API](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Done]**.

>[!NOTE]
>
>Você também pode gerar credenciais de autenticação usando as APIs do Adobe Commerce. Para obter detalhes sobre esse processo e mais informações sobre a autenticação baseada em OAuth para o Adobe Commerce, consulte [Autenticação baseada em OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) na documentação do Adobe Developer.
