---
title: Ordem de classificação para totais de check-out
description: Saiba mais sobre o total de check-out exibido e como configurar a ordem de classificação dos totais de check-out no resumo do pedido.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Ordem de classificação para totais de check-out

Durante a revisão da ordem, o total aparece na parte inferior da ordem, com quaisquer ajustes para descontos, encargos de entrega, crédito de loja e impostos. A ordem de cada item determina a sequência dos cálculos e é definida na configuração por um número atribuído a cada item. Por exemplo, o Subtotal é o primeiro item na seção e recebe um valor de 10. O Total geral é exibido por último e recebe um valor de 100. Todos os outros itens na seção de totais recebem um valor entre esses valores.

![Resumo do pedido exibe o total de finalização](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_Para configurar a ordem de classificação dos totais de check-out:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda a **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Checkout Totals Sort Order]** seção.

   ![Opções de totais de check-out numeradas para determinar a ordem de classificação](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Ordem de classificação dos totais de check-out](../configuration-reference/sales/sales.md#checkout-totals-sort-order) no _Guia de referência de configuração_.

1. Se a configuração for para uma exibição de loja específica, [escolher a exibição de loja](../configuration-reference/scope-change.md#set-the-scope) onde a configuração se aplica.

   Quando solicitado, clique em **[!UICONTROL OK]** para continuar.

1. Para determinar a ordem no _Totais_ alterar o número atribuído a cada item.

   Quanto menor o valor, mais cedo será o seu posicionamento na lista. Na configuração padrão, o Subtotal (`10`) é o primeiro e o total geral (`100`) é o último.

   Se necessário, limpe a **[!UICONTROL Use system value]** para concluir essas alterações.

1. Clique em **[!UICONTROL Save Config]**.
