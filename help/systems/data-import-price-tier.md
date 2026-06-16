---
title: Importar preços de camada
description: Saiba como exportar dados de preços de camada e importar dados atualizados.
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/8eyWhVu-RtuzEYG81xOyqsEFdbz0s7evB-UGepUGCNw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 0%

---

# Importar preços de camada

Em vez de inserir [preços de camada](../catalog/product-price-tier.md) manualmente para cada produto, pode ser mais eficiente [importar](data-import.md) os dados de preços. Antes de começar, crie um arquivo de amostra de dados de preço da camada exportados que você possa usar como modelo.

![Exemplo de vitrine - preços em camadas](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## Etapa 1: Exportar os dados de preço da camada

O exemplo a seguir exporta dados de preços de camada para um único produto. Em seguida, você pode usar os dados exportados como um modelo para importações em massa de dados de preço da camada. Para saber mais sobre como exportar dados de preços avançados, consulte [Dados de preços avançados](data-attributes-product.md#advanced-pricing-attributes).

![Preços em camadas do produto](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Em _[!UICONTROL Export Settings]_, defina **[!UICONTROL Entity Type]**como `Advanced Pricing`.

1. Na grade **[!UICONTROL Entity Attributes]**, role para baixo até os atributos SKU e faça o seguinte:

   - Para preços de nível baseados em uma porcentagem de desconto, insira o SKU de cada produto a ser exportado, separado por vírgula.

     ![Exportação de dados - SKUs de produto](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - Para preços de nível baseados em uma quantidade fixa, insira o SKU de cada produto.

   - Role para baixo e clique em **[!UICONTROL Continue]**.

1. Localize o arquivo de exportação no local de downloads do seu navegador da Web e abra o arquivo.

   ![Exemplo - dados de preço da camada de desconto do grupo de clientes exportados](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_Dados de preço de camada exportados_**

As seguintes colunas estão incluídas nos dados exportados:

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

Use os dados exportados como um modelo para importar dados de preço de camada.

## Etapa 2: Atualizar os dados

1. Atualize os dados de preço da camada para cada produto, conforme necessário.

   Todos os produtos sem atualizações de preço por nível podem ser excluídos do arquivo CSV. Não há necessidade de reimportar os produtos que não foram alterados.

1. **[!UICONTROL Save]** o arquivo CSV atualizado.

>[!NOTE]
>
>O tamanho de um arquivo de importação não pode ser maior que 2 MB.

## Etapa 3: Importar os dados atualizados

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Em _Importar Configurações_, defina **[!UICONTROL Entity Type]** como `Advanced Pricing`.

1. Defina **[!UICONTROL Import Behavior]** como `Add/Update`.

1. Em **[!UICONTROL File to Import]**, clique em **[!UICONTROL Choose File]** e selecione o arquivo que você preparou para importar do seu diretório.

1. No canto superior direito, clique em **[!UICONTROL Check Data]**.

1. Se o arquivo for válido, clique em **[!UICONTROL Import]**.

   Caso contrário, corrija cada problema com os dados listados na mensagem e tente importar o arquivo novamente.
