---
title: Transferir uma conta do Adobe Commerce
description: Saiba como transferir uma conta do Adobe Commerce para um novo proprietário ou endereço de email, escolher o tipo de transferência correto, verificar as alterações de email e entrar em contato com o Suporte.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e01cba363eb149286479718e660f8cdf6526e826
workflow-type: tm+mt
source-wordcount: 1553
ht-degree: 0%

---

# Transferir uma conta do Adobe Commerce

À medida que as responsabilidades comerciais mudam, talvez seja necessário transferir sua conta da Adobe Commerce para um novo proprietário ou para outro endereço de email. Essa transferência requer uma alteração no email do usuário principal associado à conta.

As informações a seguir descrevem o processo de transferência de uma conta do Adobe Commerce (MAGEID). Ela não inclui alterações na Adobe Commerce na propriedade do projeto de infraestrutura em nuvem ou na propriedade de [!DNL New Relic]. Para obter mais informações sobre o acesso aos projetos na nuvem, consulte [Gerenciar acesso do usuário](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) no _Guia do Commerce na Infraestrutura da Nuvem_.

>[!IMPORTANT]
>
>Se o novo proprietário da conta adquiriu extensões usando o Shared Access, o acesso a essas extensões é perdido assim que a transferência de conta começa.
>
>Antes de solicitar a transferência de conta, verifique se o novo proprietário recupera as IDs de Pedido para as compras da [sua [!DNL Commerce Marketplace] conta](https://commercemarketplace.adobe.com/sales/order/history/) e solicita um reembolso da [[!DNL Commerce Marketplace] equipe](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). As compras de extensão não podem ser transferidas para uma conta diferente.

## Identificar o tipo de transferência

O processo de transferência de conta apropriado do Adobe Commerce depende do status da conta do proprietário atual e do novo proprietário, e se o endereço de email do proprietário atual ainda está acessível. Por exemplo, se o proprietário atual tiver deixado a empresa, talvez ainda seja necessário acessar os emails enviados para esse endereço.

Os cenários a seguir descrevem as opções de transferência disponíveis com base nessas condições.

| Tipo de transferência | Proprietário atual | Novo proprietário |
| ------------- | ------------- | --------- |
| [Nova Adobe ID e alteração de email](#new-adobe-id-and-email-change) | Tem uma MAGEID que não foi conectada a uma Adobe ID | Não tem um MAGEID e não tem um Adobe ID. |
| [Somente alteração de email](#email-change) | Tem uma MAGEID conectada a uma Adobe ID. | Tem uma Adobe ID, mas não tem uma MAGEID conectada à conta. |
| [Opção de conta da Adobe ID](#adobe-id-account-switch) | Tem uma MAGEID conectada a uma Adobe ID. | Tem uma MAGEID e está conectado a uma Adobe ID. |

{style="table-layout:auto"}

>[!NOTE]
>
>Como a Adobe Commerce continua a se integrar a outras soluções da Adobe, uma conta da Adobe Commerce (MAGEID) agora requer uma associação com uma Adobe ID. O Adobe ID usa o mesmo endereço de email conectado à sua [conta do Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

## Verificar uma alteração de email do Adobe ID

Vários caminhos de transferência usam o mesmo fluxo de trabalho de verificação em [account.adobe.com](https://account.adobe.com/). Após inserir o endereço de email de destino e clicar em **[!UICONTROL Change]**, conclua estas etapas:

1. Abra o email de verificação enviado para o endereço inserido e localize o código de confirmação.

1. Insira o código de confirmação.

1. Clique em **[!UICONTROL Verify]**.

## Nova Adobe ID e alteração de email

>[!IMPORTANT]
>
>Revise os [tipos de transferência](#identify-your-transfer-type) e confirme se esse caminho corresponde à sua situação:
>
>- O proprietário atual ainda está na empresa.
>- O proprietário atual não tem uma Adobe ID ou tem uma Adobe ID que não está conectada à sua [conta da Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- O novo proprietário não tem uma Adobe ID e uma conta da Adobe Commerce.

Use esse caminho quando o proprietário atual tiver uma MAGEID que ainda não esteja vinculada a uma Adobe ID. O proprietário atual primeiro cria e vincula uma Adobe ID e, em seguida, altera esse endereço de email da Adobe ID para o novo endereço de email do proprietário.

1. Vá para a página [logon da conta do Adobe Commerce](https://account.magento.com/customer/account/login/).

1. Clique em **[!UICONTROL Sign in with Adobe ID]**.

1. Clique em **[!UICONTROL Create an account]**.

1. Digite o endereço de email e a senha do proprietário atual.

1. Clique em **[!UICONTROL Continue]**.

   Essa etapa cria uma Adobe ID e a vincula à conta atual da Adobe Commerce (MAGEID). Com este link de conta, o campo _[!UICONTROL Email]_&#x200B;está bloqueado contra quaisquer alterações. A configuração do endereço de email associado é gerenciada na conta do Adobe ID.

1. Navegue até [account.adobe.com](https://account.adobe.com/).

1. Clique em **[!UICONTROL Change Email]**.

1. Digite o endereço de email do novo proprietário.

   Se o novo endereço de email já estiver vinculado a outra conta no sistema, ele não poderá ser usado diretamente para a transferência. Em vez disso, siga o caminho [opção de conta da Adobe ID](#adobe-id-account-switch) e use um [endereço de email temporário](#change-to-a-temporary-account).

1. Conclua as [etapas de verificação de email](#verify-an-adobe-id-email-change).

Depois que o novo proprietário verificar o endereço de email, continue para [Etapas finais](#final-steps) para que o Suporte da Adobe Commerce possa atualizar registros de conta como o perfil [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on){transcript=true}

## Somente alteração de email {#email-change}

>[!IMPORTANT]
>
>Revise os [tipos de transferência](#identify-your-transfer-type) e confirme se esse caminho corresponde à sua situação:
>
>- O proprietário atual ainda está na empresa.
>- O proprietário atual tem uma Adobe ID conectada à sua [conta da Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- O novo proprietário tem uma Adobe ID que não está conectada a uma conta da Adobe Commerce.

Antes de começar, observe que esse tipo de transferência faz com que o proprietário da conta atual perca o acesso a outros produtos da Adobe vinculados a essa Adobe ID.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe.

1. Em seu nome de conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, digite o endereço de email do novo proprietário.

   Se o novo endereço de email já estiver vinculado a outra conta no sistema, ele não poderá ser usado diretamente para a transferência. Em vez disso, siga o caminho [opção de conta da Adobe ID](#adobe-id-account-switch) e use um [endereço de email temporário](#change-to-a-temporary-account).

1. Conclua as [etapas de verificação de email](#verify-an-adobe-id-email-change).

Depois que o novo proprietário verificar o endereço de email, continue para [Etapas finais](#final-steps) para que o Suporte da Adobe Commerce possa atualizar registros de conta como o perfil [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

## Alternância de conta do Adobe ID

>[!IMPORTANT]
>
>Revise os [tipos de transferência](#identify-your-transfer-type) e confirme se esse caminho corresponde à sua situação:
>
>- O proprietário atual não está mais na empresa, mas os emails enviados para o endereço de email da empresa do proprietário atual ainda estão acessíveis, ou sua equipe de TI pode encaminhar esses emails para um contato autorizado.
>- O proprietário atual tem uma Adobe ID conectada à sua [conta da Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- O novo proprietário tem uma Adobe ID conectada à conta da Adobe Commerce.

Esse tipo de transferência usa um endereço de email temporário para alternar a propriedade da conta quando o proprietário atual e o novo proprietário têm Adobe IDs existentes e você deseja manter ambas as Adobe IDs. Para concluir a transferência de propriedade, é necessário usar um endereço de email temporário que não esteja associado a uma Adobe ID.

### Alterar para uma conta temporária

Conclua essas etapas para associar a Adobe ID do proprietário atual a um endereço de email temporário. Você deve ter acesso a esse endereço de email para poder recuperar o código de confirmação.

>[!NOTE]
>
>Se não conseguir acessar o email do proprietário atual, peça à sua equipe de TI para configurar o encaminhamento de email para o endereço de email da conta no sistema de email da sua empresa. Se não for possível configurar o encaminhamento de email, verifique se o novo proprietário da conta tem uma Adobe ID e [envie uma solicitação de suporte](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) com todos os detalhes necessários para iniciar a transferência da conta.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe.

1. Em seu nome de conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, insira um endereço de email temporário válido que não seja usado por uma Adobe ID.

1. Conclua as [etapas de verificação de email](#verify-an-adobe-id-email-change).

1. Faça logout da conta do Adobe.

### Novas etapas de proprietário

Depois que o proprietário atual concluir a transferência para um endereço de email temporário, o novo proprietário deverá concluir essas etapas para alterar seu endereço de email do Adobe ID para o endereço de email original do proprietário atual.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe.

1. Em seu nome de conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, digite o endereço de email original do proprietário atual.

1. Conclua as [etapas de verificação de email](#verify-an-adobe-id-email-change).

1. Faça logout da conta do Adobe.

### Etapas de acompanhamento

Depois que o novo proprietário configurar com êxito sua Adobe ID com o endereço de email original do proprietário atual, conclua essas etapas para atribuir esse endereço de email ao novo proprietário.

1. Navegue até [account.adobe.com](https://account.adobe.com/) e conclua o logon da Adobe usando o endereço de email da [conta temporária](#change-to-a-temporary-account).

1. Em nome da conta e avatar, clique em **[!UICONTROL Change Email]**.

1. Na caixa de diálogo, digite o endereço de email do novo proprietário.

1. Conclua as [etapas de verificação de email](#verify-an-adobe-id-email-change).

Depois que o novo proprietário verificar o endereço de email, continue para [Etapas finais](#final-steps) para que o Suporte da Adobe Commerce possa atualizar registros de conta como o perfil [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

## Etapas finais

Conclua estas etapas após concluir o processo [Nova Adobe ID e alteração de email](#new-adobe-id-and-email-change), [Somente alteração de email](#email-change) ou [alternância de conta da Adobe ID](#adobe-id-account-switch).

1. Como novo proprietário, [envie uma solicitação de suporte](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case).

   Inclua os seguintes detalhes:

   - O endereço de email do proprietário da conta anterior
   - O endereço de email do novo proprietário
   - Uma observação informando que você concluiu uma transferência de conta do Adobe Commerce e atualizou o endereço de email do Adobe ID

1. Aguarde o Suporte da Adobe Commerce confirmar a atualização.

   O suporte também atualiza registros relacionados, como o endereço de email do seu perfil do [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

Depois que o suporte concluir a solicitação, o novo proprietário poderá fazer logon na conta da Adobe Commerce com a Adobe ID. A MAGEID permanece como o identificador de direito da conta.
