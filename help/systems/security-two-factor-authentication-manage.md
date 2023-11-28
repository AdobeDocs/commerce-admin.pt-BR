---
title: Gerenciar autenticação de dois fatores
description: Saiba como gerenciar a autenticação de dois fatores e redefinir os autenticadores para usuários administradores.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Gerenciar autenticação de dois fatores

Usuários que não conseguem fazer logon na _Admin_ com a autenticação de dois fatores (2FA) pode tentar sincronizar ou solucionar o problema. Também é possível redefinir os autenticadores associados à conta. Quando redefinido, o usuário deve fazer logon novamente e reconfigurar os autenticadores necessários.

Se você tiver problemas para fazer logon com 2FA, considere o seguinte:

- Alguns aplicativos móveis incluem opções de sincronização. Essa opção reconecta o aplicativo e o servidor e sincroniza as configurações de tempo no dispositivo e no servidor.
- Revogar um dispositivo ou redefinir um autenticador pode ajudar os usuários a se conectarem.
- Limpar o cache da Web e os cookies para a instalação do Adobe Commerce ou do Magento Open Source também pode ajudar. Os autenticadores, como o Google, usam cookies gerados para salvar o acesso e a duração. Limpe os cookies do navegador específico e armazene o domínio.
- O bloqueio de cookies impede que alguns autenticadores, como o [!DNL Google Authenticator]da conclusão do processo de verificação. Adicione uma regra ao navegador que permita cookies para a instalação do Adobe Commerce.

Para redefinir autenticadores a partir da linha de comando e de informações mais avançadas sobre solução de problemas, consulte [Autenticação de dois fatores](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) na documentação do desenvolvedor.

**_Para redefinir autenticadores para uma conta de usuário:_**

>[!NOTE]
>
>Para redefinir provedores 2FA para outros usuários, você deve ser um _administrador_ com `All` ou ter `Custom` permissões para sua função com [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] e [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] selecionado. Para saber mais, consulte [Funções do usuário](permissions-user-roles.md).

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Selecione o usuário e abra a conta no modo de edição.

1. Role para baixo até _[!UICONTROL Current User Identity Verification]_e digite sua senha.

1. No painel esquerdo, clique em **[!UICONTROL 2FA]**.

1. No _[!UICONTROL Configuration reset]_clique em **[!UICONTROL Reset]**e **[!UICONTROL OK]**para confirmar.

   ![Conta de usuário - ativar 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Se quiser restaurar os métodos 2FA necessários para sua conta, o usuário deverá reconfigurar cada um dos _Fazer logon_ página.

1. Quando terminar, clique em **[!UICONTROL Save User]**.
