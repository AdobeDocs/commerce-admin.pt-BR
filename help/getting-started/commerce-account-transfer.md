---
title: Transferir uma conta do Commerce
description: Saiba como transferir sua conta do Commerce para outro proprietário ou endereço de email.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: a7b23834b00b2ae0f5fd98de47fdc6f4aa00c010
workflow-type: tm+mt
source-wordcount: '1196'
ht-degree: 0%

---

# Transferir uma conta do Commerce

À medida que as responsabilidades comerciais mudam, talvez seja necessário transferir sua conta da Commerce para um novo proprietário ou para outro endereço de email. Essa transferência requer uma alteração no email do usuário principal associado à conta.

As informações a seguir descrevem o processo de transferência de uma conta do Commerce (MAGEID). Não inclui alterações na propriedade da conta da nuvem (projeto na nuvem ou New Relic). Para obter mais informações sobre o acesso aos projetos na nuvem, consulte [Gerenciar acesso do usuário](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) no _Guia do Commerce na Infraestrutura da Nuvem_.

>[!IMPORTANT]
>
>Se o novo proprietário da conta tiver adquirido extensões usando o Acesso compartilhado, o acesso a essas extensões será perdido assim que o processo de Transferência de conta for iniciado. Antes de solicitar a transferência de conta, verifique se o novo proprietário recupera as IDs de pedido para as compras de [sua conta do Marketplace](https://commercemarketplace.adobe.com/sales/order/history/) e solicita um reembolso para essas extensões da [equipe do Marketplace](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). Não é possível transferir compras de extensão para uma conta diferente.

## Identificar o tipo de transferência

O tipo de transferência de conta do Commerce depende das credenciais de conta do Commerce disponíveis para o proprietário atual e para o novo proprietário. Os cenários a seguir descrevem os diferentes tipos de transferência com base nessas credenciais.

| Tipo de transferência | Proprietário atual | Novo proprietário |
| ------------- | ------------- | --------- |
| [Nova Adobe ID e alteração de email](#new-adobe-id-and-email-change) | Tem uma MAGEID que **_não foi conectada_** a uma conta de logon do Adobe | Não tem uma MAGEID e não está conectado a uma conta de logon do Adobe. |
| [Alteração de email](#email-change) | Tem uma MAGEID que está **_conectada_** a uma conta de logon do Adobe. | Tem uma conta de logon do Adobe, mas **_não tem uma MAGEID_** conectada a uma conta de logon do Adobe. |
| [Opção de conta da Adobe ID](#adobe-id-account-switch) | Tem uma MAGEID que está **_conectada_** a uma conta de logon do Adobe. | Tem uma MAGEID e está conectado a uma conta de logon do Adobe. |

{style="table-layout:auto"}

>[!NOTE]
>
>Como a Adobe Commerce continua a se integrar a outras soluções da Adobe, uma conta da Commerce (MAGEID) agora requer uma associação com um logon da Adobe. Essa Adobe ID usa o mesmo endereço de email conectado à sua conta da Commerce.

## Nova Adobe ID e alteração de email

>[!IMPORTANT]
>
>Revise os [tipos de transferência](#identify-your-transfer-type) e verifique se você atende às pré-condições para esta sequência de etapas.

Esse tipo de transferência requer uma Adobe ID vinculada à conta existente do Commerce e, em seguida, a alteração dessa conta para o endereço de email do novo proprietário.

1. Vá para a página [logon da conta do Commerce](https://account.magento.com/customer/account/login/).

1. Clique em **[!UICONTROL Sign in with Adobe ID]**.

1. Clique em **[!UICONTROL Create an account]**.

1. Digite o endereço de email do proprietário atual e uma senha.

1. Clique em **[!UICONTROL Continue]**.

   Essa etapa cria uma Adobe ID e a vincula à conta atual da Commerce (MAGEID). Com este link de conta, o campo _[!UICONTROL Email]_está bloqueado contra quaisquer alterações. A configuração do endereço de email associado é gerenciada na conta do Adobe ID.

1. Navegue até [account.adobe.com](https://account.adobe.com/).

1. Clique em **[!UICONTROL Change Email]**.

1. Digite o endereço de email do novo proprietário.

   Se o novo endereço de email já estiver vinculado a outra conta no sistema, ele não poderá ser usado diretamente para a transferência. Em vez disso, o processo requer o uso de um [endereço de email temporário](#change-to-a-temporary-account) para facilitar a alteração.

1. Clique em **[!UICONTROL Change]**.

   Essa etapa gera um email de verificação enviado para o novo endereço de email. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Insira o código de confirmação enviado para o novo endereço de email.

1. Clique em **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Alteração de email

>[!IMPORTANT]
>
>Revise os [tipos de transferência](#identify-your-transfer-type) e verifique se você atende às pré-condições para esta sequência de etapas.

Esse tipo de transferência faz com que o proprietário da conta atual perca o acesso a outros produtos da Adobe.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe.

1. Em seu nome de conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, digite o endereço de email do novo proprietário.

   Se o novo endereço de email já estiver vinculado a outra conta no sistema, ele não poderá ser usado diretamente para a transferência. Em vez disso, o processo requer o uso de um [endereço de email temporário](#change-to-a-temporary-account) para facilitar a alteração.

1. Clique em **[!UICONTROL Change]**.

   Essa etapa gera um email de verificação enviado para o novo endereço de email. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Insira o código de confirmação enviado para o novo endereço de email.

1. Clique em **[!UICONTROL Verify]**.

## Alternância de conta do Adobe ID

>[!IMPORTANT]
>
>Revise os [tipos de transferência](#identify-your-transfer-type) e verifique se você atende às pré-condições para esta sequência de etapas.

Esse tipo de transferência usa um endereço de email temporário para alternar a propriedade da conta quando o proprietário atual e o novo proprietário têm Adobe IDs existentes e você deseja manter ambas as contas. Para concluir a transferência de propriedade, é necessário usar um endereço de email temporário que não esteja associado a uma Adobe ID.

### Alterar para uma conta temporária

O proprietário atual conclui essas etapas para associar sua Adobe ID a outro endereço de email temporário.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe.

1. Em seu nome de conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, insira um endereço de email temporário válido que não seja usado por uma Adobe ID.

>[!NOTE]
>
>Você deve ter acesso ao endereço de email para poder recuperar o email com o código de confirmação.
>
>Se não conseguir acessar o email da conta, peça à sua equipe de TI para configurar o encaminhamento de email para o endereço de email da conta no sistema de email da sua empresa. Se não for possível configurar o encaminhamento de email, verifique se o novo Proprietário da Conta tem uma Adobe ID e [envie uma solicitação de Suporte](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) com todos os detalhes necessários para iniciar a transferência da conta.

1. Clique em **[!UICONTROL Change]**.

   Essa etapa gera um email de verificação enviado ao endereço de email temporário. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Insira o código de confirmação enviado para o endereço de email temporário.

1. Clique em **[!UICONTROL Verify]**.

1. Faça logout da conta do Adobe.

### Novas etapas de proprietário

Depois que o proprietário atual concluir a transferência para um endereço de email temporário, o novo proprietário deverá concluir essas etapas para alterar a configuração da conta para apontar para o endereço de email original do proprietário atual.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe.

1. Em seu nome de conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, digite o endereço de email original do proprietário atual.

1. Clique em **[!UICONTROL Change]**.

   Esta etapa gera um email de verificação enviado ao endereço de email original do proprietário atual. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Digite o código de confirmação enviado ao endereço de email original do proprietário atual.

1. Clique em **[!UICONTROL Verify]**.

1. Faça logout da conta do Adobe.

### Etapas de acompanhamento

Depois que o novo proprietário configurar com êxito sua conta do Adobe com o endereço de email original do proprietário atual, conclua essas etapas para transferir a propriedade.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe usando o endereço de email da [conta temporária](#change-to-a-temporary-account).

1. Em nome da conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, digite o endereço de email do novo proprietário.

1. Clique em **[!UICONTROL Change]**.

   Esta etapa gera um email de verificação enviado ao endereço de email do novo proprietário. O email contém um código de confirmação necessário para concluir a alteração do endereço de email.

1. Insira o código de confirmação enviado para o endereço de email do novo proprietário.

1. Clique em **[!UICONTROL Verify]**.

## Etapas finais

Depois que o novo proprietário concluir as etapas no primeiro ou no terceiro caso de uso, o novo proprietário deverá [enviar uma solicitação de suporte](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case) para informar à equipe de suporte sobre a atualização do endereço de email. A equipe de suporte concluirá tarefas adicionais, como atualizar o endereço de email no perfil do [Commerce Marketplace](https://commercemarketplace.adobe.com/). Inclua na solicitação o endereço de email do proprietário da conta anterior.