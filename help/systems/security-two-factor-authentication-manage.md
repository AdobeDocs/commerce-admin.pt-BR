---
title: Gerenciar autenticação de dois fatores
description: Saiba como gerenciar a autenticação de dois fatores e redefinir os autenticadores para usuários administradores.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/aE-36667-f0E4GSXDjZZmFUkS3wa-xTLUMbVtjwS6qk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 336
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

1. Role para baixo até a seção _[!UICONTROL Current User Identity Verification]_e digite sua senha.

1. No painel esquerdo, clique em **[!UICONTROL 2FA]**.

1. Na seção _[!UICONTROL Configuration reset]_, clique em **[!UICONTROL Reset]**e **[!UICONTROL OK]**para confirmar.

   ![Conta de usuário - habilitar 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Se o usuário quiser restaurar os métodos 2FA necessários para sua conta, será necessário reconfigurar cada um na página _Logon_.

1. Quando terminar, clique em **[!UICONTROL Save User]**.
