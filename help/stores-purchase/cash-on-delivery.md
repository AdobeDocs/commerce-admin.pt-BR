---
title: Dinheiro na entrega (COD)
description: Saiba como configurar o pagamento na entrega como um método de pagamento offline em sua loja.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
TQID: https://experienceleague.adobe.com/xKFjuGpjrF-XfVnNqWR2St8v3D4Lnr74WozkrynBbdo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 0%

---

# Dinheiro na entrega (COD)

O Adobe Commerce e o Magento Open Source permitem que você aceite _pagamentos à vista na entrega_ (COD) para compras. Você pode aceitar o pagamento COD somente de países específicos e pode ajustar a configuração com limites totais mínimos e máximos de pedidos.

A transportadora recebe o pagamento do cliente no momento da entrega, que é então transferido a você. Você pode fazer um ajuste para qualquer taxa cobrada pelo serviço da transportadora em seus encargos de remessa e manuseio.

**_Para configurar pagamentos de entrega à vista:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Em _Outros Métodos de Pagamento_, expanda ![Seletor de Expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Cash On Delivery Payment]**.

   ![Pagamento em Dinheiro na Entrega](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas definições de configuração, consulte [Pagamento com Pagamento na Entrega](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) no _Guia de Referência de Configuração_.

   >[!NOTE]
   >
   >Se necessário, primeiro desmarque a caixa de seleção **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para ativar o pagamento à vista na entrega, defina **[!UICONTROL Enabled]** como `Yes`.

1. Para **[!UICONTROL Title]**, insira um título que identifique o método de pagamento COD durante o check-out.

1. Defina **[!UICONTROL New Order Status]** como `Pending` até que o recebimento do pagamento seja confirmado.

   Se preferir, você pode usar o status `Processing` ou `Suspected Fraud` para novos pedidos com esta forma de pagamento.

1. Defina **[!UICONTROL Payment from Applicable Countries]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` - Depois que você escolher essa opção, a lista _[!UICONTROL Payment from Specific Countries]_&#x200B;será exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Insira o **[!UICONTROL Instructions]** para aceitar a entrega de um pedido COD.

1. Defina **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** para os valores do pedido que são necessários para se qualificar para o pagamento do COD.

   >[!NOTE]
   >
   >Um pedido é qualificado se o total estiver entre, ou corresponder, ao total mínimo ou máximo do pedido.

1. Para **[!UICONTROL Sort Order]**, insira um número que determine a posição deste item na lista de métodos de pagamento exibidos durante o check-out.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
