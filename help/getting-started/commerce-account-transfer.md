---
title: Transferir uma conta do Commerce
description: Saiba como transferir sua conta do Commerce para outro proprietário ou endereço de email.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 9daf227e52c8f225e957ee5009d0d0a02815d835
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 0%

---

# Transferir uma conta do Commerce

À medida que as responsabilidades comerciais mudam, talvez seja necessário transferir a propriedade da conta existente do Commerce para um novo proprietário ou para outro endereço de email. Essa transferência requer uma alteração no email do usuário principal associado à conta.

As informações a seguir descrevem o processo de transferência de uma conta do Commerce (MAGEID). Não inclui alterações na propriedade da conta da nuvem (projeto na nuvem ou New Relic). Para obter mais informações sobre o acesso aos projetos na nuvem, consulte [Gerenciar acesso do usuário](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) no _Guia do Commerce na Infraestrutura da Nuvem_.

>[!IMPORTANT]
>
>Se o novo Proprietário da conta tiver adquirido extensões originalmente usando o Acesso compartilhado, o acesso a essas extensões será perdido assim que o processo de Transferência de conta for iniciado. Antes de solicitar a transferência de conta, verifique se o novo proprietário recupera as IDs de pedido para as compras de [sua conta do Marketplace](https://commercemarketplace.adobe.com/sales/order/history/) e solicita um reembolso para essas extensões da [equipe do Marketplace](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). Não é possível transferir compras de extensão para uma conta diferente.

## Identificar o tipo de transferência

A forma como você conclui essa transferência depende de qual dos seguintes cenários descreve a sua situação como o proprietário atual da conta e o novo proprietário (endereço de email) para quem você deseja transferir a conta:

| Tipo de transferência | Proprietário atual | Novo proprietário |
| ------------- | ------------- | --------- |
| [Nova Adobe ID e alteração de email](#new-adobe-id-and-email-change) | Possui uma MAGEID que **_não está conectada_** a uma conta de logon do Adobe. | Não tem uma MAGEID e não está conectado a uma conta de logon do Adobe. |
| [Alteração de email](#email-change) | Tem uma MAGEID que está **_conectada_** a uma conta de logon do Adobe. | Não tem uma MAGEID e não está conectado a uma conta de logon do Adobe. |
| [Opção do Adobe ID](#adobe-id-account-switch) | Tem uma MAGEID que está **_conectada_** a uma conta de logon do Adobe. | Tem uma MAGEID e está conectado a uma conta de logon da Adobe sem nenhum outro produto/serviço da Adobe associado. |

{style="table-layout:auto"}

>[!NOTE]
>
>Como a Adobe Commerce continua a se integrar a outras soluções da Adobe, uma conta da Commerce (MAGEID) agora requer uma associação com um logon da Adobe. Essa Adobe ID usa o mesmo endereço de email conectado à sua conta da Commerce.

## Nova Adobe ID e alteração de email

>[!IMPORTANT]
>
>Revise os [tipos de transferência](#identify-your-transfer-type) e verifique se você atende às pré-condições para esta sequência de etapas.

Esse tipo de transferência requer que você primeiro crie uma Adobe ID associada e, em seguida, altere essa conta para o endereço de email do novo proprietário.

1. Vá para sua [conta do Commerce](https://account.magento.com/customer/account/login/).

1. Clique em **[!UICONTROL Sign in with Adobe ID]**.

1. Clique em **[!UICONTROL Create an account]**.

1. Digite o endereço de email do proprietário atual e uma senha.

1. Clique em **[!UICONTROL Continue]**.

   Isso cria uma Adobe ID e a vincula à conta atual da Commerce (MAGEID). Com este link de conta, o campo _[!UICONTROL Email]_está bloqueado contra quaisquer alterações. O endereço de email associado é gerenciado pela conta do Adobe ID.

1. Navegue até [account.adobe.com](https://account.adobe.com/).

1. Clique em **[!UICONTROL Change Email]**.

1. Digite o endereço de email do novo proprietário.

1. Clique em **[!UICONTROL Change]**.

   Isso gera um email de verificação enviado para o novo endereço de email. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Insira o código de confirmação enviado para o novo endereço de email.

1. Clique em **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Alteração de email

>[!IMPORTANT]
>
>Revise os [tipos de transferência](#identify-your-transfer-type) e verifique se você atende às pré-condições para esta sequência de etapas.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe.

1. Em seu nome de conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, digite o endereço de email do novo proprietário.

1. Clique em **[!UICONTROL Change]**.

   Isso gera um email de verificação enviado para o novo endereço de email. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Insira o código de confirmação enviado para o novo endereço de email.

1. Clique em **[!UICONTROL Verify]**.

## Alternância de conta do Adobe ID

>[!IMPORTANT]
>
>Revise os [tipos de transferência](#identify-your-transfer-type) e verifique se você atende às pré-condições para esta sequência de etapas.

Caso o proprietário atual e o novo proprietário tenham IDs do Adobe existentes, ambas as contas devem permanecer, mas os endereços de email precisam ser alternados entre elas. Isso requer o uso de um endereço de email _temporário_ que seja válido, mas não esteja associado ao e ao Adobe ID.

### Alterar para uma conta temporária

O proprietário atual conclui essas etapas para associar sua Adobe ID a outro endereço de email temporário.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe.

1. Em seu nome de conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, insira um endereço de email temporário válido que não seja usado por uma Adobe ID.

   Você deve ter acesso ao endereço de email para poder recuperar o email com o código de confirmação.

1. Clique em **[!UICONTROL Change]**.

   Isso gera um email de verificação enviado ao endereço de email temporário. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Insira o código de confirmação enviado para o endereço de email temporário.

1. Clique em **[!UICONTROL Verify]**.

1. Faça logout da conta do Adobe.

### Novas etapas de proprietário

Depois que o proprietário atual concluir a transferência para um endereço de email temporário, conclua essas etapas para alterar sua conta para o proprietário atual.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe.

1. Em seu nome de conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, digite o endereço de email original do proprietário atual.

1. Clique em **[!UICONTROL Change]**.

   Isso gera um email de verificação enviado para esse endereço de email. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Insira o código de confirmação enviado ao proprietário atual.

1. Clique em **[!UICONTROL Verify]**.

1. Faça logout da conta do Adobe.

### Etapas de acompanhamento

Depois que o novo proprietário transferir com êxito sua conta do Adobe para o proprietário atual (agora anterior), conclua essas etapas para transferir a propriedade.

1. Navegue até [account.adobe.com](https://account.adobe.com/) (primeira conta usada na série de etapas) e conclua o logon do Adobe.

   Este logon requer o uso do endereço de email temporário.

1. Em nome da conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, digite o endereço de email do novo proprietário.

1. Clique em **[!UICONTROL Change]**.

   Isso gera um email de verificação enviado para esse endereço de email. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Insira o código de confirmação enviado ao novo proprietário.

1. Clique em **[!UICONTROL Verify]**.

>[!IMPORTANT]
>
>Envie uma solicitação de suporte para informar à equipe de suporte que você atualizou o endereço de email do proprietário da conta. A equipe deve executar etapas adicionais para concluir a atualização, como atualizar o endereço de email no seu perfil do [Commerce Marketplace](https://commercemarketplace.adobe.com/). Inclua em sua solicitação o endereço de email do proprietário da conta anterior.
