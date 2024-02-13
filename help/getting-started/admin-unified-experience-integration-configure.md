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

# Configurar a integração do Experience Cloud com o administrador de comércio

Comece a integração do Experience Cloud com o Administrador do Commerce configurando o aplicativo do Commerce para usar as extensões da Experiência unificada do administrador do Commerce e Eventos do Commerce.


## Pré-requisitos

- O Adobe Commerce deve ser configurado para usar [Autenticação do Adobe IMS](../getting-started/adobe-ims-config.md)
- Provisionamento e permissões de conta — os administradores devem ter uma [perfil empresarial do Adobe](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) com acesso aos seguintes recursos para configurar a integração de Experience Cloud:
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html)—Adição e gerenciamento de contas de usuários e desenvolvedores do Adobe para a organização
   - [Console do Adobe Developer](https://developer.adobe.com/developer-console/docs/guides/getting-started/)—Acesso de desenvolvedor ou administrador do sistema para criar projetos do App Builder e gerar as credenciais de conexão e a configuração do projeto para usar o serviço de Eventos do Adobe I/O
   - [Projeto de infraestrutura do Commerce na nuvem](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface)—Instale os módulos necessários e configure o servidor de aplicativos do Commerce usando a CLI do Adobe Commerce
   - [Administrador de comércio](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—Atualizar a configuração da loja e gerenciar contas de usuário do Commerce

## Visão geral da configuração

Habilite a integração concluindo as seguintes tarefas:

1. [Verificar o ambiente de comércio e a configuração do aplicativo](#check-the-commerce-environment-and-application-configuration).

1. [Habilitar a extensão Commerce Admin Unified Experience](#enable-the-commerce-admin-unified-experience-extension).

1. [Configurar eventos do Adobe I/O para o Commerce](#set-up-adobe-io-events).

1. [Testar a integração](#test-the-integration).

## Verificar o ambiente de comércio e a configuração do aplicativo

Antes de configurar a integração de Experience Cloud, verifique se o projeto e o aplicativo do Commerce atendem aos requisitos.

1. Na estação de trabalho local, altere para o diretório do projeto do Commerce.

1. Verifique a ramificação do ambiente para a instância a ser integrada ao Experience Cloud.

1. Verifique se o Adobe IMS está ativado.

   - Use o [URL de acesso SSH](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) para que o ambiente se conecte ao servidor de aplicativos do Commerce.

   - Na linha de comando, use a Adobe Commerce CLI para verificar o status do módulo IMS.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Se o módulo não estiver ativado, [ative-o usando a Organização e as credenciais para o projeto de integração do IMS](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module).

1. Verifique se o usuário Administrador pode fazer logon no Administrador do Commerce usando sua Adobe ID.

   - Vá para o URL de administração do Commerce.

   - Se você estiver conectado, faça logout.

   - Certifique-se de que o usuário Administrador seja redirecionado para fazer logon usando sua Adobe ID.

     ![Fazer logon no Adobe Commerce usando o Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

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

## Habilitar a experiência unificada de administrador do Commerce

Habilite a extensão Commerce Admin Unified Experience e faça logon por meio do Experience Cloud.

>[!NOTE]
>
>Essas instruções mostram como um administrador de projeto do Commerce Cloud pode habilitar a extensão usando a CLI do Adobe Commerce. Os usuários de Administração de comércio também podem habilitar a extensão, atualizando o [Definições de configuração da loja de comércio](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. No diretório raiz do ambiente do projeto na nuvem na estação de trabalho local, use o [ferramenta magento-cloud CLI](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) para fazer logon no servidor de aplicativos do Commerce.

   ```bash
   magento-cloud ssh
   ```

1. Ativar o `magento/module-unified-experience` usando a Adobe Commerce CLI:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Limpe o cache.

   ```bash
   bin/magento cache:clean
   ```

## Configurar eventos do Adobe I/O para o Commerce

Quando a integração Experience Cloud está habilitada, o serviço de Eventos Adobe I/O envia dados do evento Commerce para o Experience Cloud para gerenciar o acesso de administrador a projetos Commerce. A configuração do serviço exige a habilitação da extensão Adobe I/O Events para Commerce (`magento/commerce-eventing`) e configuração do serviço Adobe I/O Events no Admin.

### Ativar eventos comerciais

Habilitar a extensão Eventos de comércio (`magento/commerce-eventing`) para enviar dados do evento personalizado do aplicativo Commerce para o serviço Adobe I/O Events.

>[!NOTE]
>
>Para o Commerce 2.4.6 e versões posteriores, a extensão Commerce Events é instalada por padrão. Para projetos do Commerce com o Commerce 2.4.5, use o Composer pela primeira vez para [instalar a extensão](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce), em seguida, ative-a.

1. No ambiente de desenvolvimento de projeto local do Commerce, adicione a seguinte configuração à `.magento.env.yaml` arquivo.

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

1. Adicionar, confirmar e implantar o atualizado `.magento.env.yaml file` para o ambiente de nuvem.

>[!TIP]
>
>Para obter detalhes sobre a configuração e o gerenciamento das variáveis de ambiente usando o `.magento.env.yaml` arquivo, consulte [Configurar variáveis de ambiente para implantação](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### Configurar a integração de eventos de comércio

Configure a integração de Eventos de comércio concluindo as tarefas a seguir. Para obter instruções detalhadas, consulte [Eventos Adobe I/O para Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/) documentação do desenvolvedor.

1. [Criar um projeto do App Builder](https://developer.adobe.com/commerce/extensibility/events/project-setup/) para receber dados do evento da instância do Commerce.

   Você precisa de credenciais e dados de configuração do projeto do App Builder para configurar a integração no Administrador do Commerce.

1. Configure o Adobe Commerce para usar o Adobe I/O Events.

   - [Atualizar as definições de Configuração de Armazenamento para o serviço de Eventos Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Configurar um provedor de eventos para enviar eventos de comércio](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Atualize o projeto do App Builder para receber dados do evento da instância do Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Não registre ou assine eventos da instância do Commerce. O registro de evento é enviado para o projeto do App Builder quando você configura o provedor de eventos para o aplicativo do Commerce.

   Depois de conectar o provedor de eventos ao projeto do App Builder, assine a `observer.uex_commerce_instance_update` e salve as alterações.

1. Para estabelecer a conexão, envie um evento por meio do provedor de eventos para o consumidor.

   - Na linha de comando no diretório do projeto na nuvem local, [usar SSH para se conectar ao servidor de aplicativos do Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Envie dados do evento verificando o status da extensão Admin Unified Experience usando a CLI do Adobe Commerce.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Testar a integração

Verifique se um administrador de comércio pode fazer logon no Experience Cloud para visualizar os projetos do Commerce disponíveis e acessar o administrador e a loja de cada projeto.

1. [Fazer logon no Experience Cloud](https://experiencecloud.adobe.com/library) usando a Adobe ID e a organização associadas à instância do Commerce.

   ![Acessar projetos de comércio na página inicial do Experience Cloud](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Exibir projetos do Commerce disponíveis selecionando **[!UICONTROL Commerce]**.

   ![Espaço de trabalho de Projetos do Commerce para Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Abra o Administrador de uma instância selecionando **[!UICONTROL Open]**.

   ![Exibição de administrador do Commerce com integração Experience Cloud habilitada](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Verifique se você pode executar tarefas de Administrador conforme esperado.

   Os workflows no Administrador do Commerce devem seguir o mesmo processo. Se ocorrer alterações ou erros no fluxo de trabalho após habilitar a integração de Experience Cloud, entre em contato com o administrador de sistema do Commerce ou [enviar um tíquete de suporte Adobe](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Após configurar a integração de Experience Cloud, verifique se as contas de administrador estão provisionadas corretamente para acessar projetos do Commerce por meio do Experience Cloud. Consulte [Gerenciar usuários administradores](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
