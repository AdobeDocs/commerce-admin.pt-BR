---
title: Gerenciar a integração do Experience Cloud
description: Saiba como gerenciar a integração do Experience Cloud e solucionar problemas
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Gerenciar a integração do Experience Cloud

Após a ativação inicial, gerencie o status da integração do Experience Cloud ativando ou desativando a extensão do Commerce Admin Unified Experience.

- Se a extensão Commerce Admin Unified Experience estiver habilitada e as contas de administrador forem [provisionadas corretamente](#manage-admin-user-accounts), os administradores do Commerce poderão exibir e acessar os projetos Commerce disponíveis no Adobe Experience Cloud. Os administradores ainda podem acessar projetos individuais usando o URL do administrador para o ambiente de projetos do Commerce.

- Se a extensão Commerce Admin Unified Experience estiver desativada, o acesso pelo Experience Cloud será desativado. Os administradores devem fazer logon em projetos individuais usando o URL do administrador para o ambiente de projeto do Commerce.

>[!WARNING]
>
>Se a integração do Adobe Identity Management Service (IMS) estiver desativada, a integração do Experience Cloud será desativada automaticamente.

## Gerenciar a integração do Administrador

1. No Administrador do Commerce, abra o menu Configuração de armazenamento selecionando **[!UICONTROL Stores]** no menu de navegação esquerdo e selecione **[!UICONTROL Configuration]**.

1. No menu Configuração, selecione **[!UICONTROL Advanced > Admin]** e expanda a **[!UICONTROL Unified Experience option]**.

   ![Configuração do Admin Store para integração com o Experience Cloud](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Ative ou desative a integração selecionando o valor **[!UICONTROL Enable]**.

1. Altere o nome do projeto que é exibido no espaço de trabalho do Commerce Projects adicionando ou atualizando o valor **[!UICONTROL Project Name]**.

1. Salve a configuração.

1. Limpe o cache.

## Gerenciar a integração usando a CLI do Adobe Commerce

Os administradores de sistema do Commerce com acesso de administrador ao projeto de nuvem do Commerce podem usar comandos da CLI do Adobe Commerce para gerenciar a integração do Experience Cloud.

1. Faça logon no projeto de nuvem a partir do ambiente de desenvolvimento local.

   ```bash
   magento-cloud login
   ```

1. No diretório raiz do ambiente do projeto na nuvem, conecte-se ao servidor de aplicativos do Commerce.

   ```bash
   ssh magento-cloud
   ```

1. Verifique o status da extensão Admin Unified Experience:

   ```bash
   bin/magento admin:uex:status
   ```

1. Altere o status da extensão para desativar a integração

   - **Habilitar**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Desabilitar**—`bin/magento config:set admin/unified_experience/enabled 0`

## Gerenciar contas de usuário Admin

Todos os usuários administradores do Commerce devem ter uma conta de administrador na instância do Commerce e uma conta de usuário do Adobe (Adobe ID) para acessar os produtos e serviços da Adobe. Ambas as contas devem ser associadas ao mesmo endereço de email.

- **Conta de administrador do Commerce**—[Gerenciar usuários administradores do Commerce](../systems/permissions-users-all.md) por meio do Administrador da instância do Commerce. As contas de usuário para administradores do Commerce devem receber a função de Administrador.

  Os administradores de sistema no projeto do Commerce podem usar o [SSH para se conectar ao ambiente remoto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment) e usar os comandos `admin:user:create` e `admin:user:unlock` da CLI do Commerce para adicionar ou desbloquear contas de usuário administrador.

- **Conta de usuário do Adobe** — Um administrador da organização da Adobe associada à instância do Commerce deve fazer logon na Adobe Admin Console e adicionar o Adobe ID para cada administrador do Commerce à organização. Em seguida, eles devem atribuir direitos e permissões de produto para acessar o aplicativo do Commerce. Consulte [Configurar usuários do Adobe Commerce na Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Os administradores que gerenciam a configuração da integração do Experience Cloud no Adobe Developer Console devem ter uma conta de usuário do Adobe com acesso de Administrador do sistema ou Desenvolvedor.

>[!NOTE]
>
>Uma Adobe ID é uma conta criada pela Adobe, necessária para acessar produtos e serviços por meio da Experience Cloud. Os administradores do Commerce que não têm uma Adobe ID podem [criar uma conta gratuita](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) usando o mesmo endereço de email que usam para entrar no Administrador do Commerce.
