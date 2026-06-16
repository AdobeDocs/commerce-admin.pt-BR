---
title: Classes de imposto
description: Saiba como configurar as classes de imposto usadas para regras de imposto.
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
TQID: https://experienceleague.adobe.com/wzq0p5sH7Ulpl6hiY5IaWPe9AvsrwJjrAZsX4PFZ2-Y
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 501
ht-degree: 0%

---

# Classes de imposto

Classes de imposto podem ser atribuídas a clientes, produtos e entregas. A Commerce analisa o carrinho de compras de cada cliente e calcula o imposto apropriado de acordo com a classe do cliente, a classe dos produtos no carrinho e a região. A região é determinada pelo endereço de entrega, endereço de faturamento ou origem da remessa do cliente. Novas classes de imposto podem ser criadas quando uma [regra de imposto](tax-rules.md) é definida.

- **Cliente** — Você pode criar quantas classes de imposto do cliente forem necessárias e atribuí-las a [grupos de clientes](../customers/customer-groups.md). Por exemplo, em algumas jurisdições, as transações grossistas não são tributadas, mas as transações retalhistas são tributadas. Você pode associar membros do grupo Cliente Atacado à classe de imposto Atacado.

- **Produto** — As classes de produto são usadas nos cálculos para determinar se a alíquota de imposto correta é aplicada ao carrinho de compras. Quando você cria o produto, ele é atribuído a uma classe de imposto específica. Por exemplo, os alimentos podem não ser tributados ou ser tributados a uma taxa diferente.

- **Envio** — Se a loja cobrar um imposto extra sobre o envio, você deverá designar uma classe de imposto do produto específica para envio. Em seguida, na configuração, especifique-a como a classe de imposto usada para entrega.

## Configurar classes de imposto

A classe de imposto usada para remessa e as classes de imposto padrão para [produtos e clientes](#add-a-product-tax-class) estão definidas na configuração _[!UICONTROL Sales]_.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Tax]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Tax Classes]**.

   ![Configuração - classes de imposto](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Escolha a classe de imposto para cada uma das seguintes opções:

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Adicionar classes de imposto

Classes de imposto para clientes e produtos podem ser facilmente adicionadas, atribuídas a clientes e produtos individuais e usadas em regras de imposto.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Clique em **[!UICONTROL Add New Tax Rule]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Additional Settings]**.

   ![Adicionar Nova Classe de Imposto](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Em _Classe de Imposto do Cliente_, clique em **[!UICONTROL Add New Tax Class]**.

1. Insira o **[!UICONTROL Name]** da nova classe de imposto na caixa de texto.

   ![Adicionar Nova Classe de Imposto](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. Para adicionar a nova classe à lista de classes de imposto do cliente disponíveis, clique na marca de seleção.

   ![Novas classes de imposto](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## Adicionar uma classe de imposto do produto

1. Em _Classe de Imposto do Produto_, clique em **[!UICONTROL Add New Tax Class]**.

1. Insira o **[!UICONTROL Name]** da nova classe de imposto na caixa de texto.

1. Para adicionar a nova classe à lista de classes de imposto do produto disponíveis, clique na marca de seleção.

1. Quando terminar, clique em **[!UICONTROL Back]** na barra de botões para retornar à grade _Regras de Imposto_.

## Destino de imposto padrão

As configurações padrão de destino do imposto determinam o país, o estado e o CEP usados como base para os cálculos do imposto.

**_Para configurar o destino de imposto padrão para cálculos:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Tax]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Default Tax Destination Calculation]**.

   ![Cálculo de Destino de Imposto Padrão](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Default Country]** como o país no qual se baseiam os cálculos de imposto.

1. Defina **[!UICONTROL Default State]** para o estado ou província que é usado como base de cálculos de imposto.

1. Defina **[!UICONTROL Default Post Code]** como CEP ou código postal usado como base de cálculos de impostos locais.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
