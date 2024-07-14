---
title: Configurar a integração de Experience Cloud para o administrador do Commerce
description: Saiba como configurar um projeto do Commerce para habilitar o acesso de administrador por meio do Experience Cloud.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: 8278d725a7377b865c118b86a57702cd2be43238
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 0%

---

# Configurar a integração do Experience Cloud com o administrador do Commerce

Comece a integração do Experience Cloud com o Commerce Admin configurando o aplicativo do Commerce para usar as extensões do Commerce Admin Unified Experience e do Commerce Events.


## Pré-requisitos

- O Adobe Commerce deve ser configurado para usar a [autenticação do Adobe IMS](../getting-started/adobe-ims-config.md)
- Provisionamento e permissões de conta — Os administradores devem ter um [perfil de negócios Adobe](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) com acesso aos seguintes recursos para configurar a integração Experience Cloud:
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html)—Adicione e gerencie contas de usuário e de desenvolvedor do Adobe para a organização
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/) — Acesso de desenvolvedor ou administrador do sistema para criar projetos do App Builder e gerar as credenciais de conexão e a configuração do projeto para usar o serviço de Eventos do Adobe I/O
   - [Projeto de infraestrutura do Commerce na nuvem](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface)—Instale os módulos necessários e configure o servidor de aplicativos do Commerce usando a CLI do Adobe Commerce
   - [Administrador do Commerce](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—Atualize a configuração de armazenamento e gerencie as contas de usuário do Commerce

## Visão geral da configuração

Habilite a integração concluindo as seguintes tarefas:

1. [Verifique o ambiente do Commerce e a configuração do aplicativo](#check-the-commerce-environment-and-application-configuration).

1. [Habilitar a extensão da Experiência Unificada do Administrador do Commerce](#enable-the-commerce-admin-unified-experience-extension).

1. [Configurar Adobe I/O Events para Commerce](#set-up-adobe-io-events).

1. [Testar a integração](#test-the-integration).

## Verifique o ambiente do Commerce e a configuração do aplicativo

Antes de configurar a integração de Experience Cloud, verifique se o projeto e o aplicativo Commerce atendem aos requisitos.

1. Na estação de trabalho local, altere para o diretório do projeto do Commerce.

1. Verifique a ramificação do ambiente para a instância a ser integrada ao Experience Cloud.

1. Verifique se o Adobe IMS está ativado.

   - Use a [URL de Acesso SSH](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) do ambiente para se conectar ao servidor de aplicativos do Commerce.

   - Na linha de comando, use a Adobe Commerce CLI para verificar o status do módulo IMS.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Se o módulo não estiver habilitado, [habilite-o usando a Organização e as credenciais para o projeto de integração IMS](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module).

1. Verifique se o usuário Admin pode fazer logon no Commerce Admin usando a Adobe ID.

   - Vá para o URL do administrador do Commerce.

   - Se você estiver conectado, faça logout.

   - Certifique-se de que o usuário Administrador seja redirecionado para fazer logon usando sua Adobe ID.

     ![Entrar no Adobe Commerce usando o Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. No diretório do projeto na nuvem na estação de trabalho local, verifique se a extensão Commerce Admin Unified Experience está instalada.

   ```bash
   composer show *unified-experience*
   ```

   Se a extensão estiver instalada, o Composer retornará o nome e a descrição da extensão.

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   Se a extensão não estiver instalada, use o Composer para instalá-la. Em seguida, confirme as alterações e reimplante o ambiente de nuvem.

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## Habilitar a experiência unificada do administrador do Commerce

Habilite a extensão Commerce Admin Unified Experience e faça logon por meio do Experience Cloud.

>[!NOTE]
>
>Essas instruções mostram como um administrador de projeto do Commerce Cloud pode habilitar a extensão usando a CLI do Adobe Commerce. Os usuários de Administração do Commerce também podem habilitar a extensão atualizando as [configurações de armazenamento do Commerce](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. No diretório raiz do ambiente do projeto na nuvem na estação de trabalho local, use a [ferramenta Magento-Cloud CLI](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) para fazer logon no servidor de aplicativos do Commerce.

   ```bash
   magento-cloud ssh
   ```

1. Habilite a extensão `magento/module-unified-experience` usando a Adobe Commerce CLI:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Limpe o cache.

   ```bash
   bin/magento cache:clean
   ```

## Configurar eventos do Adobe I/O para o Commerce

Quando a integração Experience Cloud está habilitada, o serviço de Eventos Adobe I/O envia dados de eventos Commerce para o Experience Cloud para gerenciar o acesso do administrador a projetos Commerce. A configuração do serviço exige a habilitação dos Eventos de Adobe I/O para a extensão do Commerce (`magento/commerce-eventing`) e a configuração do serviço de Eventos de Adobe I/O no Administrador.

### Ativar eventos do Commerce

Habilite a extensão de Eventos da Commerce (`magento/commerce-eventing`) para enviar dados de eventos personalizados do aplicativo Commerce para o serviço de Eventos Adobe I/O.

>[!NOTE]
>
>Para o Commerce 2.4.6 e posterior, a extensão Commerce Events é instalada por padrão. Para projetos do Commerce com o Commerce 2.4.5, primeiro use o Composer para [instalar a extensão](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce) e, em seguida, habilite-a.

1. No ambiente de desenvolvimento de projetos local do Commerce, adicione a seguinte configuração ao arquivo `.magento.env.yaml`.

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. Adicione, confirme e implante o `.magento.env.yaml file` atualizado no ambiente de nuvem.

>[!TIP]
>
>Para obter detalhes sobre como configurar e gerenciar variáveis de ambiente usando o arquivo `.magento.env.yaml`, consulte [Configurar variáveis de ambiente para implantação](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### Configurar a integração de eventos do Commerce

Configure a integração dos Eventos da Commerce concluindo as tarefas a seguir. Para obter instruções detalhadas, consulte a documentação do desenvolvedor [Adobe I/O Events for Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/).

1. [Crie um projeto do App Builder](https://developer.adobe.com/commerce/extensibility/events/project-setup/) para receber dados do evento da instância do Commerce.

   Você precisa de credenciais e dados de configuração do projeto do App Builder para configurar a integração no Administrador do Commerce.

1. Configure o Adobe Commerce para usar o Adobe I/O Events.

   - [Atualize as definições de Configuração de Armazenamento para o serviço de Eventos Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Configure um provedor de eventos para enviar eventos Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Atualize o projeto do App Builder para receber dados do evento da instância do Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Não registre ou assine eventos da instância do Commerce. O registro de eventos é enviado para o projeto do App Builder quando você configura o provedor de eventos para o aplicativo do Commerce.

   Depois de conectar o provedor de eventos ao projeto do App Builder, assine o evento `observer.uex_commerce_instance_update` e salve as alterações.

1. Para estabelecer a conexão, envie um evento por meio do provedor de eventos para o consumidor.

   - Na linha de comando no diretório de projeto da nuvem local, [use SSH para se conectar ao servidor de aplicativos do Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Envie dados do evento verificando o status da extensão Admin Unified Experience usando a CLI do Adobe Commerce.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Testar a integração

Verifique se um administrador do Commerce pode fazer logon no Experience Cloud para ver os projetos Commerce disponíveis e acessar o administrador e a loja de cada projeto.

1. [Entre no Experience Cloud](https://experiencecloud.adobe.com/library) usando a Adobe ID e a organização associada à instância do Commerce.

   ![Acessar projetos do Commerce na home page do Experience Cloud](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Exibir Projetos Commerce disponíveis selecionando **[!UICONTROL Commerce]**.

   ![Espaço de trabalho do Commerce Projects para Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Abra o Administrador de uma instância selecionando **[!UICONTROL Open]**.

   ![Modo de exibição de Administrador do Commerce com integração de Experience Cloud habilitada](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Verifique se você pode executar tarefas de Administrador conforme esperado.

   Os workflows no Administrador do Commerce devem seguir o mesmo processo. Se ocorrer alterações ou erros no fluxo de trabalho após habilitar a integração de Experience Cloud, contate o administrador de sistema da Commerce ou [envie um tíquete de Suporte de Adobe](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Após configurar a integração de Experience Cloud, verifique se as contas de administrador estão provisionadas corretamente para acessar os projetos Commerce por meio do Experience Cloud. Consulte [Gerenciar usuários administradores](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
