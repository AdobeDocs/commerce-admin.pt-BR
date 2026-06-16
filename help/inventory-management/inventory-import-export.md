---
title: Importar e exportar estoque
description: Use os recursos nativos de importação e exportação com opções  [!DNL Inventory Management]  expandidas para atualizar fontes e quantidades por SKU.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
TQID: https://experienceleague.adobe.com/TrH9Ncak4gPMh-4kejFF0NdCIzjT-xT5-M4eETSQ9FM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 510
ht-degree: 0%

---

# Importar e exportar estoque

Para catálogos com muitos produtos, use os recursos de importação e exportação nativos com opções [!DNL Inventory Management] expandidas para atualizar fontes e quantidades por SKU. Com essas opções, você pode adicionar novas origens e atualizar quantidades de inventário para todas ou uma origem específica. Por exemplo, você pode exportar produtos para uma origem na Alemanha sem afetar as informações de produtos para origens na França, Inglaterra ou EUA.

- O [!DNL Commerce] atribui automaticamente o Source Padrão aos seus produtos ao atualizar o [!DNL Commerce] ou importar novos produtos. Se você importar produtos com uma origem personalizada atribuída, o Source padrão ainda será adicionado com uma quantidade de 0. Para atualizar origens e quantidades, use essas instruções de importação.

- Os comerciantes de origem única usam a importação para atualizar apenas as quantidades do produto. Todos os produtos existentes e adicionados são atribuídos ao Source padrão.

- Comerciantes de várias origens usam a importação para adicionar várias origens e quantidades por linha por SKU.

Para importar atualizações, primeiro exporte um arquivo CSV de uma origem específica ou de todas as origens. Edite o arquivo CSV e adicione uma linha por SKU para cada origem e quantidade. Você precisa do código-fonte ao adicionar uma fonte e quantidades de estoque. Não é possível adicionar ou atualizar estoques usando recursos de importação/exportação.

## Conteúdo do arquivo CSV

O arquivo de importação de exportação inclui as seguintes informações de acordo com a origem:

- `source_code` - O código das fontes em [!DNL Commerce]. Há uma linha para cada origem e SKU.
- `sku` - O SKU do produto em [!DNL Commerce]. O SKU deve corresponder a um produto em seu armazenamento para atualizar corretamente os dados do [!DNL Inventory Management].
- `status` - 0 para Sem Estoque. 1 para Em estoque. Esse valor deve ser 1 para comprar estoque dessa fonte.
- `quantity` - A quantidade total de estoque disponível para esta SKU e esta origem.

Use um arquivo CSV para atualizar rapidamente vários produtos e fontes atribuídas para atualizar e corrigir imprecisões nos registros de inventário, em vez de uma de cada vez, por meio da interface do aplicativo. Para um arquivo básico, exporte primeiro e atualize conforme necessário.

![Exemplo de arquivo CSV para importação - exportar dados de inventário](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Exportar dados do produto de todas as fontes

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Para **[!UICONTROL Entity Type]**, escolha `Stock Sources`.

   A exportação só extrai dados de produtos com um SKU.

1. Clique em **[!UICONTROL Continue]**.

   O arquivo gera e baixa para abrir e editar.

Depois de atualizar os valores de estoque e os dados do produto, importe o arquivo de volta para [!DNL Commerce].

![Exportar fontes de estoque para fontes e dados de produtos](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Exportar dados do produto para uma origem específica

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Para **[!UICONTROL Entity Type]**, escolha `Stock Sources`.

   A exportação só extrai dados de produtos com um SKU.

1. Use o **[!UICONTROL Entity Attributes]** para filtrar os produtos exportados de uma origem específica.

   Para `source_code`, insira o código da origem no campo de filtro.

1. Clique em **[!UICONTROL Continue]**.

   O arquivo gera e baixa para abrir e editar.

Depois de atualizar os valores de estoque e os dados do produto, importe o arquivo de volta para [!DNL Commerce].

## Importar dados do produto

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Para **[!UICONTROL Entity Type]**, escolha `Stock Sources`.

   A exportação só extrai dados de produtos com um SKU.

1. Selecione as configurações para o **[!UICONTROL Import Behavior]**.

1. Selecione o arquivo .csv a ser importado.

1. Clique em **[!UICONTROL Check Data]** e conclua a importação.

![Importar fontes e dados de produtos](assets/inventory-import-sources.png){width="600" zoomable="yes"}
