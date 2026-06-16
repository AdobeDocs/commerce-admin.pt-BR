---
title: Gerenciar assinantes do informativo
description: Saiba como gerenciar os assinantes do boletim informativo usando uma lista simples de assinaturas ativas.
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
TQID: https://experienceleague.adobe.com/l4Kmwm62UeLYZva-SCsVHPmf4IbKQhgoyN9N7zo4O0g
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffa
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 509
ht-degree: 0%

---

# Gerenciar assinantes do informativo

Como prática recomendada, você deve gerenciar a lista de assinaturas regularmente e processar todas as solicitações para cancelar a inscrição. Em algumas jurisdições, é exigido por lei que os pedidos de cancelamento de subscrição sejam processados em um período específico.

É possível gerenciar facilmente os assinantes usando uma lista simples de assinaturas ativas. Quando um cliente envia uma solicitação de cancelamento de assinatura, você pode simplesmente aplicar uma ação _Cancelar assinatura_ a uma ou mais assinaturas selecionadas.

Em configurações de site único com várias exibições de loja, uma assinatura de conta de cliente pode ser associada a uma exibição de loja específica.

Em configurações de vários sites e vários sites com um [escopo de conta de cliente](../customers/customer-account-scope.md) global, uma conta de cliente pode assinar boletins informativos para vários sites/lojas. Nesse caso, talvez você queira editar a conta do cliente para gerenciar um grupo de assinaturas ou cancelar uma assinatura para um site/loja específico para atender a uma solicitação.

Se quiser usar um serviço de terceiros para enviar informativos, é possível exportar a lista de assinaturas como um arquivo CSV ou XML.

## Gerenciar assinaturas de um cliente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Encontre o cliente na grade e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Clique em **[!UICONTROL Newsletter]** no painel esquerdo.

1. Modifique as assinaturas do cliente de acordo com a configuração do site/loja.

   Para uma única configuração de site/loja, basta marcar ou desmarcar a caixa de seleção **[!UICONTROL Subscribed to Newsletter]**.

   ![Caixa de seleção de assinatura do boletim informativo do cliente de loja única](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   Para uma configuração de um único site/várias lojas, você pode marcar ou desmarcar a caixa de seleção **[!UICONTROL Subscribed to Newsletter]** e definir **[!UICONTROL Subscribed on Store View]** para a exibição de loja correta para a assinatura.

   ![Caixa de seleção de assinatura do boletim informativo do cliente de várias lojas e seletor de exibição de loja](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   Para uma configuração de vários sites/várias lojas com um escopo de conta de cliente global, a página exibe o status de assinatura de todos os sites. Você pode marcar ou desmarcar a caixa de seleção **[!UICONTROL Subscribed]** e/ou alterar a **[!UICONTROL Store View]** da assinatura.

   ![Caixas de seleção de assinatura de boletim informativo de vários sites e seletores de exibição de repositório](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. Clique em **[!UICONTROL Save Customer]**.

## Cancelar uma assinatura na lista de assinantes

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   Para uma configuração de vários sites, em que alguns clientes têm assinaturas para mais de um site, cada assinatura é exibida como um item de linha na grade.

1. Localize o assinante na grade e marque a caixa de seleção na primeira coluna.

   >[!NOTE]
   >
   >Para um cancelamento de subscrição em massa, marque a caixa de seleção de cada assinante que deseja cancelar.

1. Defina o controle _[!UICONTROL Action]_como **[!UICONTROL Unsubscribe]**e clique em **[!UICONTROL Submit]**.

   ![Cancelar assinatura do informativo](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   O status do registro muda para `Unsubscribed`.

## Exportar a lista de assinantes

1. Na lista _[!UICONTROL Newsletter Subscribers]_, use os controles de filtro para incluir apenas registros com um_ Status _de `Subscribed` e para o modo de exibição de site, loja ou loja apropriado.

1. Defina o controle **[!UICONTROL Export to]** como um dos seguintes:

   - `CSV`
   - `XML`

1. Clique em **[!UICONTROL Export]**, procure o prompt na parte inferior da tela e salve o arquivo.

   ![Exportar assinantes do informativo](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## Deletar um assinante da lista de assinantes

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. Localize o assinante na grade e marque a caixa de seleção na primeira coluna.

1. Defina o controle _[!UICONTROL Action]_como **[!UICONTROL Delete]**e clique em **[!UICONTROL Submit]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.
