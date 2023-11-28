---
title: Importar e exportar estoque
description: Use os recursos nativos de importação e exportação com [!DNL Inventory Management] opções para atualizar origens e quantidades por SKU.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Importar e exportar estoque

Para catálogos com muitos produtos, use os recursos nativos de importação e exportação com [!DNL Inventory Management] opções para atualizar origens e quantidades por SKU. Com essas opções, você pode adicionar novas origens e atualizar quantidades de inventário para todas ou uma origem específica. Por exemplo, você pode exportar produtos para uma origem na Alemanha sem afetar as informações de produtos para origens na França, Inglaterra ou EUA.

- [!DNL Commerce] O atribui automaticamente a Origem padrão aos seus produtos ao atualizar [!DNL Commerce] ou importação de novos produtos. Se você importar produtos com uma origem personalizada atribuída, a Origem padrão ainda será adicionada com uma quantidade de 0. Para atualizar origens e quantidades, use essas instruções de importação.

- Os comerciantes de origem única usam a importação para atualizar apenas as quantidades do produto. Todos os produtos existentes e adicionados são atribuídos à Origem padrão.

- Comerciantes de várias origens usam a importação para adicionar várias origens e quantidades por linha por SKU.

Para importar atualizações, primeiro exporte um arquivo CSV de uma origem específica ou de todas as origens. Edite o arquivo CSV e adicione uma linha por SKU para cada origem e quantidade. Você precisa do código-fonte ao adicionar uma fonte e quantidades de estoque. Não é possível adicionar ou atualizar estoques usando recursos de importação/exportação.

## Conteúdo do arquivo CSV

O arquivo de importação de exportação inclui as seguintes informações de acordo com a origem:

- `source_code` - O código para fontes em [!DNL Commerce]. Há uma linha para cada origem e SKU.
- `sku` - O SKU do produto em [!DNL Commerce]. O SKU deve corresponder a um produto em sua loja para atualizar corretamente [!DNL Inventory Management] dados.
- `status` - 0 para Sem Estoque. 1 para Em estoque. Esse valor deve ser 1 para comprar estoque dessa fonte.
- `quantity` - A quantidade total de estoque disponível para este SKU e esta origem.

Use um arquivo CSV para atualizar rapidamente vários produtos e fontes atribuídas para atualizar e corrigir imprecisões nos registros de inventário, em vez de uma de cada vez, por meio da interface do aplicativo. Para um arquivo básico, exporte primeiro e atualize conforme necessário.

![Exemplo de arquivo CSV para importação - exportar dados de inventário](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Exportar dados do produto de todas as fontes

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Para **[!UICONTROL Entity Type]**, escolha `Stock Sources`.

   A exportação só extrai dados de produtos com um SKU.

1. Clique em **[!UICONTROL Continue]**.

   O arquivo gera e baixa para abrir e editar.

Depois de atualizar os valores de estoque e os dados do produto, importe o arquivo de volta para o [!DNL Commerce].

![Exportar fontes de estoque para fontes e dados de produtos](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Exportar dados do produto para uma origem específica

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Para **[!UICONTROL Entity Type]**, escolha `Stock Sources`.

   A exportação só extrai dados de produtos com um SKU.

1. Use o **[!UICONTROL Entity Attributes]** para filtrar os produtos exportados de uma origem específica.

   Para `source_code`, insira o código da origem no campo de filtro.

1. Clique em **[!UICONTROL Continue]**.

   O arquivo gera e baixa para abrir e editar.

Depois de atualizar os valores de estoque e os dados do produto, importe o arquivo de volta para o [!DNL Commerce].

## Importar dados do produto

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Para **[!UICONTROL Entity Type]**, escolha `Stock Sources`.

   A exportação só extrai dados de produtos com um SKU.

1. Selecione as configurações para o **[!UICONTROL Import Behavior]**.

1. Selecione o arquivo .csv a ser importado.

1. Clique em **[!UICONTROL Check Data]** e conclua a importação.

![Importar dados e fontes de produtos](assets/inventory-import-sources.png){width="600" zoomable="yes"}
