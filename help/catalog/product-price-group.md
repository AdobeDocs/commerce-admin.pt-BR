---
title: Preços em grupo
description: Saiba como usar preços de grupo para definir preços para itens com desconto com base nos grupos de clientes em sua loja.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Preços em grupo

Você pode usar as definições de configuração do produto no Administrador para definir preços para itens com desconto com base nos grupos de clientes em sua loja. Esse modelo de preço estratégico é chamado de _preços de grupo_.

O preço com desconto de qualquer produto pode ser oferecido aos membros de um grupo de clientes específico quando o comprador estiver conectado à sua conta. O preço do grupo de clientes é exibido na página do produto junto com o preço normal para que o comprador possa facilmente comparar os preços e agir de acordo. Depois de adicionar o produto ao carrinho, o preço normal é substituído pelo preço em grupo com base no grupo de clientes.

Os preços para grupos de clientes são um componente de [preços em camadas](product-price-tier.md) e é definido de maneira semelhante. A única diferença é que os preços de grupo de clientes têm uma quantidade de 1.

![Desconto do Grupo de Clientes](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Benefícios do uso de preços em grupo

- Adequado para compradores por atacado

- Incentivo para clientes atualizarem seu grupo de clientes para aproveitarem os descontos

- Campanhas de marketing direcionadas

- Desenvolva confiança e credibilidade recompensando clientes fiéis

## Configurar um preço de grupo

1. Abra o produto no modo de edição.

1. Abaixo do _[!UICONTROL Price]_clique em **[!UICONTROL Advanced Pricing]**.

1. No _[!UICONTROL Customer Group Price]_clique em **[!UICONTROL Add]**.

   Se sua loja incluir [Adobe Commerce B2B](../b2b/introduction.md) e tem [catálogos compartilhados](../b2b/catalog-shared.md) ativada, esta seção é rotulada como _[!UICONTROL Catalog and Tier Price]_.

   ![Advanced Pricing](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Configure o preço do grupo:

   - Para uma instalação de vários sites, escolha o **[!UICONTROL Website]** se aplica o preço de grupo.

   - Escolha o **[!UICONTROL Customer Group]** que é receber o desconto.

   - Insira um **[!UICONTROL Quantity]** de `1`.

   - Para **[!UICONTROL Price]**, defina o tipo de preço e o valor:

      - `Fixed` - Insira o preço do produto com desconto.

      - `Discount` - Insira o preço com desconto como uma porcentagem do preço do produto.

     ![Precificação de Grupo de Clientes](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Para adicionar outro preço de grupo, clique em **[!UICONTROL Add]** e repita a etapa anterior.

1. Quando terminar, clique em **[!UICONTROL Done]** e depois **[!UICONTROL Save]**.

>[!NOTE]
>
>A variável **_final_** o preço do produto é calculado como a **_mínimo_** preço relevante, utilizando a seguinte fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Preço Fixo_** produto As opções personalizáveis são _não_ afetados pelas regras de Preço do Grupo, Preço da Camada, Preço Especial ou Preço do Catálogo.
