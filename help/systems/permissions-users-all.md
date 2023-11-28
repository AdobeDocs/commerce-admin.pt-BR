---
title: Gerenciar contas de usuário Admin
description: Saiba como criar contas de usuário administrador e atribuir funções para conceder permissões a funções administrativas.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Gerenciar contas de usuário Admin

Quando seu armazenamento é instalado pela primeira vez, uma conta padrão de administrador é criada com credenciais de logon que fornecem acesso administrativo total. Como prática recomendada, você deve criar outra conta de usuário com acesso total de Administrador. Dessa forma, você pode usar uma conta para suas atividades administrativas diárias e reservar a outra como uma conta de &quot;Super Admin&quot;. Isso pode ser útil se você esquecer suas credenciais normais ou elas se tornarem inutilizáveis de alguma forma.

Se houver outros em sua equipe ou provedores de serviços que precisem de acesso, você poderá criar uma conta de usuário separada para cada e atribuir acesso restrito com base na necessidade comercial deles de saber. Para limitar os sites ou lojas que os usuários podem acessar no Administrador, primeiro você deve [criar uma função](permissions-user-roles.md) com escopo limitado e apenas os recursos necessários selecionados. Em seguida, é possível atribuir a função a uma conta de usuário específica. Os usuários administradores atribuídos a uma função restrita podem ver e alterar dados somente de sites ou lojas associados à função, mas não podem alterar configurações ou dados globais.

>[!NOTE]
>
>Os comerciantes do Adobe Commerce que têm um Adobe ID e desejam um logon simplificado para produtos Adobe Commerce e Adobe Business podem integrar a autenticação do Commerce ao fluxo de trabalho de autenticação do Adobe IMS. Depois que essa integração for habilitada para a sua loja de Commerce, cada usuário administrador deverá usar suas credenciais de Adobe, não suas credenciais de Commerce, para fazer logon. Consulte [Visão geral da integração do Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Para usuários ou funções temporários, também é possível definir uma data de expiração para a conta de usuário.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Criar um usuário

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. No canto superior direito, clique em **[!UICONTROL Add New User]**.

   Para editar um usuário existente, clique em um nome de usuário na grade. Você pode modificar a variável _[!UICONTROL User Info]_e_[!UICONTROL User Role]_ seções conforme necessário.

1. No _[!UICONTROL Account Information]_faça o seguinte:

   ![Informações da conta do usuário](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Insira o **[!UICONTROL User Name]** para a conta.

     O nome de usuário deve ser fácil de lembrar. Não diferencia maiúsculas de minúsculas. Por exemplo, se o nome de usuário for `John`, eles também podem fazer logon como `john`.

   - Preencha as seguintes informações:

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Cada conta de usuário deve ter um endereço de email exclusivo.

   - Insira um **[!UICONTROL Password]** para a conta.

     >[!NOTE]
     >
     >A senha do administrador deve ter sete ou mais caracteres e incluir letras e números. Para obter opções adicionais de senha, consulte [Configuração da segurança do administrador](security-admin.md).

   - Para **[!UICONTROL Password Confirmation]**, digite novamente a senha para verificar se ela foi inserida corretamente.

   - Se sua loja tiver vários idiomas, defina **[!UICONTROL Interface Locale]** ao idioma a ser usado para a interface do Administrador.

1. Definir **[!UICONTROL This Account is]** para `Active`.

1. Clique no ícone do calendário para definir a **[!UICONTROL Expiration Date]** para a conta de usuário.

   Definir uma data de expiração é útil quando um usuário ou função é temporária. Após a data de expiração, o status da conta do usuário muda para `Inactive` e podem ser atualizadas, se necessário.

1. Em _[!UICONTROL Current User Identity Verification]_, digite a senha da sua conta de usuário.

>[!IMPORTANT]
>
>Com o _[!UICONTROL Account Information]_for concluída, você poderá salvar o usuário. O novo usuário é exibido no campo_[!UICONTROL Users]_ grade, mas o nome de usuário não pode fazer logon até que uma função seja atribuída.

## Atribuir uma função de usuário

1. No painel esquerdo, clique em **[!UICONTROL User Role]**.

   A grade lista todas as funções de usuário existentes. Para uma nova loja, _[!UICONTROL Administrators]_O é a única função disponível.

   ![Administrador - adicionar nova função de usuário](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. No _[!UICONTROL Assigned]_selecione uma função de usuário.

   Você pode [visualizar funções de usuário existentes ou definir funções adicionais](permissions-user-roles.md). Depois que uma função é definida, você deve editar a conta de usuário para atribuir a nova função.

## Verificar ou redefinir provedores 2FA

1. Abra a conta de usuário Admin.

1. No painel esquerdo, clique em **[!UICONTROL 2FA]**.

   ![Administrador - adicionar nova função de usuário](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Verifique as soluções 2FA disponíveis para _Admin_ e aconselha cada usuário a instalar as soluções que deseja usar antes de entrar.

   A autenticação por apenas uma solução 2FA é necessária para fazer logon na _Admin_.

1. Se o usuário precisar reinstalar a solução 2FA, é possível redefinir a configuração atual do 2FA.

   Isso requer que o usuário repita o processo de configuração antes de fazer logon novamente. Por exemplo, o usuário pode ter um novo smartphone e precisa reinstalar o Google Authenticator. Para limpar a configuração atual do 2FA do usuário, clique em **[!UICONTROL Reset (Provider)]** para cada solução que você deseja limpar. Quando solicitado, clique em **[!UICONTROL OK]** para confirmar.

   O usuário recebe um email com um link para [configurar 2FA](security-two-factor-authentication.md). O link pode ser usado apenas uma vez. Se o usuário tentar fazer logon várias vezes, um novo link será enviado após cada tentativa.

1. Clique em **[!UICONTROL Save User]**.

1. Quando solicitado, digite sua senha para confirmar a identidade e clique novamente em **[!UICONTROL Save User]**.

   A variável _[!UICONTROL Users]_A grade é aberta e lista todos os usuários.

## Excluir um usuário administrador

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Localize a conta de usuário usando filtros acima da grade e clique no nome do usuário.

1. Quando solicitado, digite sua senha para confirmar sua identidade.

1. No canto superior direito, clique em **[!UICONTROL Delete User]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

## Senha esquecida e emails redefinidos

A configuração do modelo de email de administrador determina os emails enviados quando os usuários esquecem e redefinem suas senhas. Essa configuração especifica o contato de armazenamento que aparece como remetente da mensagem e por quanto tempo o link de recuperação de senha permanece válido.

**_Para configurar os templates de email de Admin:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. No painel lateral esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL Admin]**.

1. Expandir ![alternador de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Admin User Emails]** seção.

   ![Configuração avançada - Configurações do modelo de email do administrador](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Forgot Password Email Template]** ao modelo que é enviado quando um usuário administrador esquece suas senhas.

1. Definir **[!UICONTROL Forgot and Reset Email Sender]** ao contato da loja que aparece como remetente da mensagem.

1. Definir **[!UICONTROL User Notification Template]** ao template de email usado como padrão para notificações do administrador.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Usuários bloqueados

Para a segurança da sua empresa, as contas de usuário são bloqueadas por padrão após seis tentativas falhas de [fazer logon](../getting-started/admin-signin.md) para o Administrador. Qualquer conta de usuário que esteja bloqueada no momento será exibida na grade Usuários bloqueados. Uma conta pode ser desbloqueada por qualquer outro usuário com permissões totais de Administrador.

Medidas adicionais de segurança de senha podem ser implementadas no [Administrador avançado](../configuration-reference/advanced/admin.md#security) configuração. Consulte [Segurança do administrador](security-admin.md).

![Alerta da tela de login - A conta está temporariamente desativada](./assets/admin-login-locked-out-message.png){width="300"}

**_Para desbloquear uma conta de administrador:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. Na grade, marque a caixa de seleção da conta bloqueada.

   ![Permissões - contas de usuário bloqueadas](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. No canto superior esquerdo, defina **[!UICONTROL Actions]** para `Unlock`.

1. Clique em **[!UICONTROL Submit]** para desbloquear a conta.
