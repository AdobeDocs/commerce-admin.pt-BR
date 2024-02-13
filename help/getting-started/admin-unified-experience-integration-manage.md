---
title: Gerenciar a integração de Experience Cloud
description: Saiba como gerenciar a integração de Experience Cloud e solucionar problemas
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: 15569794c1e66ba5a93e46206244e2951522923e
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Gerenciar a integração de Experience Cloud

Após a ativação inicial, gerencie o status da integração do Experience Cloud habilitando ou desabilitando a extensão Commerce Admin Unified Experience.

- Se a extensão Commerce Admin Unified Experience estiver habilitada e as contas de administrador estiverem [provisionado corretamente](#manage-admin-user-accounts)No entanto, os administradores de Commerce podem visualizar e acessar projetos do Commerce disponíveis no Adobe Experience Cloud. Os administradores ainda podem acessar projetos individuais usando o URL do administrador para o ambiente de projeto do Commerce.

- Se a extensão Commerce Admin Unified Experience estiver desativada, o acesso pelo Experience Cloud será desativado. Os administradores devem fazer logon em projetos individuais usando o URL do administrador para o ambiente de projeto do Commerce.

>[!WARNING]
>
>Se a integração do IMS (Adobe Identity Management Service) estiver desativada, a integração do Experience Cloud será desativada automaticamente.

## Gerenciar a integração do Administrador

1. No Administrador do Commerce, abra o menu Configuração da loja selecionando **[!UICONTROL Stores]** no menu de navegação esquerdo, selecione **[!UICONTROL Configuration]**.

1. No menu Configuração, selecione **[!UICONTROL Advanced > Admin]** e, em seguida, expanda a **[!UICONTROL Unified Experience option]**.

   ![Configuração da Admin Store para integração com o Experience Cloud](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Ative ou desative a integração selecionando o **[!UICONTROL Enable]** valor.

1. Altere o nome do projeto exibido no espaço de trabalho Projetos do Commerce adicionando ou atualizando o **[!UICONTROL Project Name]** valor.

1. Salve a configuração.

1. Limpe o cache.

## Gerenciar a integração usando a CLI do Adobe Commerce

Os administradores de sistemas de comércio com acesso de administrador ao projeto da Commerce Cloud podem usar comandos da CLI do Adobe Commerce para gerenciar a integração com o Experience Cloud.

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

   - **Ativar**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Desativar**—`bin/magento config:set admin/unified_experience/enabled 0`

## Gerenciar contas de usuário Admin

Todos os usuários administradores do Commerce devem ter uma conta de administrador na instância do Commerce e uma conta de usuário Adobe (Adobe ID) para acessar produtos e serviços Adobe. Ambas as contas devem ser associadas ao mesmo endereço de email.

- **Conta de administrador do Commerce**—[Gerenciar usuários administradores do Commerce](../systems/permissions-users-all.md) do Administrador para a instância do Commerce. As contas de usuário para administradores do Commerce devem receber a função de Administrador.

  Os administradores de sistema no projeto do Commerce podem usar [SSH para conectar ao ambiente remoto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment)e usar a CLI do Commerce `admin:user:create` e `admin:user:unlock` comandos para adicionar ou desbloquear contas de usuário Admin.

- **conta de usuário do Adobe**— Um administrador da organização de Adobe associada à instância do Commerce deve fazer logon na Adobe Admin Console e adicionar o Adobe ID para cada administrador de Commerce à organização. Em seguida, eles devem atribuir direitos e permissões de produto para acessar o aplicativo Commerce. Consulte [Configurar usuários do Adobe Commerce na Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Os administradores que gerenciam a configuração da integração de Experience Cloud no Adobe Developer Console devem ter uma conta de usuário Adobe com acesso de Administrador do sistema ou Desenvolvedor.

>[!NOTE]
>
>Uma Adobe ID é uma conta criada por meio do Adobe, necessária para acessar produtos e serviços por meio do Experience Cloud. Os administradores de comércio que não têm um Adobe ID podem [criar uma conta gratuita](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) usando o mesmo endereço de email que usam para fazer logon no Administrador do Commerce.
