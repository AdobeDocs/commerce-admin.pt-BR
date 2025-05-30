---
title: Gerenciar autenticação de dois fatores
description: Saiba como gerenciar a autenticação de dois fatores e redefinir os autenticadores para usuários administradores.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Gerenciar autenticação de dois fatores

Os usuários que não conseguem entrar no _Admin_ com autenticação de dois fatores (2FA) podem tentar sincronizar ou solucionar o problema. Também é possível redefinir os autenticadores associados à conta. Quando redefinido, o usuário deve fazer logon novamente e reconfigurar os autenticadores necessários.

Se você tiver problemas para fazer logon com 2FA, considere o seguinte:

- Alguns aplicativos móveis incluem opções de sincronização. Essa opção reconecta o aplicativo e o servidor e sincroniza as configurações de tempo no dispositivo e no servidor.
- Revogar um dispositivo ou redefinir um autenticador pode ajudar os usuários a se conectarem.
- Limpar o cache da Web e os cookies para a instalação do Adobe Commerce ou do Magento Open Source também pode ajudar. Os autenticadores, como o Google, usam cookies gerados para salvar o acesso e a duração. Limpe os cookies do navegador específico e armazene o domínio.
- O bloqueio de cookies impede que alguns autenticadores, como o [!DNL Google Authenticator], concluam o processo de verificação. Adicione uma regra ao navegador que permita cookies para a instalação do Adobe Commerce.

Para redefinir autenticadores da linha de comando e obter informações mais avançadas sobre solução de problemas, consulte [Autenticação de Dois Fatores](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) na documentação do desenvolvedor.

**_Para redefinir autenticadores para uma conta de usuário:_**

>[!NOTE]
>
>Para redefinir provedores 2FA para outros usuários, você deve ser um _administrador_ com `All` permissões ou ter `Custom` permissões para sua função com [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] e [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] selecionada. Para saber mais, consulte [Funções de usuário](permissions-user-roles.md).

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Selecione o usuário e abra a conta no modo de edição.

1. Role para baixo até a seção _[!UICONTROL Current User Identity Verification]_&#x200B;e digite sua senha.

1. No painel esquerdo, clique em **[!UICONTROL 2FA]**.

1. Na seção _[!UICONTROL Configuration reset]_, clique em **[!UICONTROL Reset]**&#x200B;e **[!UICONTROL OK]**&#x200B;para confirmar.

   ![Conta de usuário - habilitar 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Se o usuário quiser restaurar os métodos 2FA necessários para sua conta, será necessário reconfigurar cada um na página _Logon_.

1. Quando terminar, clique em **[!UICONTROL Save User]**.
