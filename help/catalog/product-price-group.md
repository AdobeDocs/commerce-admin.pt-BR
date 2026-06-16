---
title: Preços em grupo
description: Saiba como usar preços de grupo para definir preços para itens com desconto com base nos grupos de clientes em sua loja.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
TQID: https://experienceleague.adobe.com/OCeX5pLtUzWdwOW5W8qpI4DCeab2PTAVi5xF8HUr91A
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
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
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 0%

---

# Preços em grupo

Você pode usar as definições de configuração do produto no Administrador para definir preços para itens com desconto com base nos grupos de clientes em sua loja. Este modelo de preços estratégicos é chamado de _preço de grupo_.

O preço com desconto de qualquer produto pode ser oferecido aos membros de um grupo de clientes específico quando o comprador estiver conectado à sua conta. O preço do grupo de clientes é exibido na página do produto junto com o preço normal para que o comprador possa facilmente comparar os preços e agir de acordo. Depois de adicionar o produto ao carrinho, o preço normal é substituído pelo preço em grupo com base no grupo de clientes.

Os preços para grupos de clientes são um componente de [preços em camadas](product-price-tier.md) e são definidos de maneira semelhante. A única diferença é que os preços de grupo de clientes têm uma quantidade de 1.

![Desconto do Grupo de Clientes](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Benefícios do uso de preços em grupo

- Adequado para compradores por atacado

- Incentivo para clientes atualizarem seu grupo de clientes para aproveitarem os descontos

- Campanhas de marketing direcionadas

- Desenvolva confiança e credibilidade recompensando clientes fiéis

## Configurar um preço de grupo

1. Abra o produto no modo de edição.

1. Abaixo do campo _[!UICONTROL Price]_, clique em **[!UICONTROL Advanced Pricing]**.

1. Na seção _[!UICONTROL Customer Group Price]_, clique em **[!UICONTROL Add]**.

   Se o seu armazenamento incluir o [Adobe Commerce B2B](../b2b/introduction.md) e tiver [catálogos compartilhados](../b2b/catalog-shared.md) habilitados, esta seção será rotulada como _[!UICONTROL Catalog and Tier Price]_.

   ![Preços Avançados](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Configure o preço do grupo:

   - Para uma instalação de vários sites, escolha o **[!UICONTROL Website]** onde o preço de grupo se aplica.

   - Escolha a **[!UICONTROL Customer Group]** que receberá o desconto.

   - Insira um **[!UICONTROL Quantity]** de `1`.

   - Para **[!UICONTROL Price]**, defina o tipo de preço e o valor:

      - `Fixed` - Insira o preço com desconto do produto.

      - `Discount` - Insira o preço com desconto como uma porcentagem do preço do produto.

     ![Preços do grupo de clientes](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Para adicionar outro preço de grupo, clique em **[!UICONTROL Add]** e repita a etapa anterior.

1. Quando terminar, clique em **[!UICONTROL Done]** e depois em **[!UICONTROL Save]**.

>[!NOTE]
>
>O preço do produto **_final_** é calculado como o preço relevante de **_mínimo_**, usando a seguinte fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Preço Fixo_** O produto de Opções Personalizáveis _não_ é afetado pelas regras de Preço de Grupo, Preço de Camada, Preço Especial ou Preço de Catálogo.
