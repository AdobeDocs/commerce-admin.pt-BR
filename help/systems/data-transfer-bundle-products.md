---
title: Importar produtos do pacote
description: Analise um exemplo de importação de dados de produto para um produto de pacote.
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# Importar produtos do pacote

Um pacote de produtos apresenta uma seleção de itens e permite que os clientes escolham aqueles que desejam comprar. Todos os itens que compõem um pacote existem no catálogo como [Produtos simples](../catalog/product-create-simple.md) ou [Produtos virtuais](../catalog/product-create-virtual.md). Normalmente, os produtos do pacote são criados e atualizados pelo administrador. No entanto, você também pode importar dados para criar um produto de pacote ou exportar produtos de pacote existentes, editar os dados e importá-los de volta para o catálogo. O Sprite Yoga Companion Kit é um produto empacotado nos dados de amostra que são usados nos exemplos a seguir.

![Pacote de produtos](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## Alterar a ordem dos itens do pacote

Há duas maneiras de alterar a ordem dos itens em um produto de pacote.

### Método 1: arrastar e soltar

Ao trabalhar com um produto [Pacote](../catalog/product-create-bundle.md) do Administrador, você pode arrastar e soltar itens e seções na posição.

![Agrupar itens](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### Método 2: editar os dados do produto

A melhor maneira de entender a estrutura de um produto combinado é exportar o produto e examinar os dados em uma planilha. Você pode alterar a ordem dos itens de pacote exportando o produto e adicionando um parâmetro de posição aos dados de cada item. Os dados do item estão na coluna `bundle_values` do produto exportado. Quando abertos em uma planilha, todos os itens associados ao produto estão em uma única célula como uma longa sequência de texto. A coluna `bundle_values` contém os seguintes elementos para cada item:

- Nome da seção do item
- Controle de entrada
- Indicador de item obrigatório
- SKU
- Cor
- Preço
- Indicador de opção padrão
- Quantidade padrão
- Tipo de preço
- Indicador de quantidade editável

#### Etapa 1: exportar o produto do pacote

Nesta etapa, o Sprite Yoga Companion Kit é exportado como um arquivo ([CSV](data-csv.md). Você pode usar qualquer outro produto incluído no catálogo.

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Em _Configurações de Exportação_, defina **[!UICONTROL Entity Type]** como `Products`.

1. Na lista de atributos do produto, role para baixo até **[!UICONTROL SKU]** e insira o SKU do produto do pacote que você deseja exportar.

   A SKU é `24-WG080` para o produto neste exemplo.

1. Role para baixo até a parte inferior da seção e clique em **[!UICONTROL Continue]**.

1. Na coluna _[!UICONTROL Action]_&#x200B;da grade&#x200B;_[!UICONTROL File name]_, clique em **[!UICONTROL Select]** e escolha `Download`.

   O arquivo aparece no local de download usado pelo navegador.

#### Etapa 2: Editar os dados

1. Abra o arquivo CSV baixado em uma planilha.

1. Role até a extremidade direita até ver a coluna `bundle_values`.

   Nos dados `bundle_values`, cada elemento é separado por vírgula, e cada item do pacote é separado do próximo com uma barra vertical. (O último item não termina com uma barra vertical.) Os dados do pacote exportados devem ser semelhantes ao seguinte exemplo:

   ![Valores do Pacote](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. Para facilitar a edição, copie os dados do `bundle_values` e cole-os em um editor de texto. Em seguida, adicione uma quebra de linha após cada item, para que cada item fique em uma linha separada.

1. Após editar os dados, remova cuidadosamente as quebras de linha e cole os dados editados de volta na coluna `bundle_values`.

   Na ilustração a seguir, um parâmetro `position=[number]` é adicionado a cada tira de ioga para alterar a ordem dos itens na listagem da loja.

   ![Parâmetro de Posição](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. Após editar os dados, **[!UICONTROL Save]** o arquivo CSV.

#### Etapa 3: importar o produto atualizado

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Em _[!UICONTROL Import Settings]_, defina **[!UICONTROL Entity Type]**&#x200B;como `Products`.

1. Defina **[!UICONTROL Import Behavior]** como `Replace`.

   Essa opção substitui os dados anteriores do produto do pacote, em vez de adicionar as alterações como itens adicionais.

1. Role para baixo até a seção _Arquivo a ser importado_ e clique em **[!UICONTROL Choose File]**.

1. Selecione o arquivo CSV editado.

1. Clique em **[!UICONTROL Check Data]** e aguarde alguns minutos para que os dados sejam verificados.

1. Se o arquivo for válido, clique em **[!UICONTROL Import]**.

1. Quando o processo estiver concluído, vá para **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;e clique em **[!UICONTROL Flush Cache Storage]**.

   Isso garante que o produto atualizado fique imediatamente disponível na loja.
