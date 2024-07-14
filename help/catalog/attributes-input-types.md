---
title: Tipos de entrada de atributo
description: Saiba mais sobre os tipos de entrada disponíveis para atributos de produto, que determinam o tipo de dados que podem ser inseridos e o formato do campo ou do controle de entrada.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Tipos de entrada de atributo

Quando visualizados pelo Admin, os atributos são os campos que você preenche ao criar um produto. O tipo de entrada atribuído a um atributo determina o tipo de dados que podem ser inseridos e o formato do campo ou do controle de entrada. Do ponto de vista do cliente, os atributos fornecem informações sobre o produto e são as opções e os campos de entrada de dados que devem ser preenchidos para comprar um produto.

## Tipos de entrada

| Propriedade | Descrição |
|--- |--- |
| [!UICONTROL Text Field] | Um campo de entrada de linha única para texto. |
| [!UICONTROL Text Area] | Um campo de entrada de várias linhas para inserir parágrafos de texto, como uma descrição do produto. Você pode usar o Editor WYSIWYG para formatar o texto com tags HTML ou inserir as tags diretamente no texto. |
| [!UICONTROL Text Editor] | Um editor de texto totalmente funcional no local do atributo. |
| [!UICONTROL Date] | Exibe um valor de data no [formato preferido](#date-and-time-options) e [fuso horário](../getting-started/store-details.md#locale-options). Os valores de data podem ser selecionados de uma lista ou de um calendário ( ![Ícone de calendário](../assets/icon-calendar.png) ). <br/><br/>**_Observação:_**Dependendo da configuração do seu sistema, os usuários do_Administrador _podem inserir datas diretamente em um campo ou selecionar uma data no calendário ou na lista. Para obter informações sobre como especificar valores de data e hora, consulte [Opções de data e hora](#date-and-time-options). |
| [!UICONTROL Date and Time] | Exibe um valor de data e hora no [formato preferido](#date-and-time-options) e [fuso horário](../getting-started/store-details.md#locale-options). A data e a hora podem ser inseridas manualmente ou selecionadas em um calendário. Exemplo de formato: MM/DD/AAAA HH:MM |
| [!UICONTROL Yes/No] | Exibe uma lista suspensa com opções predefinidas de `Yes` e `No`. |
| Lista suspensa | Exibe uma lista suspensa de valores que aceitam apenas uma única seleção. O tipo de entrada suspensa é um componente chave de [produtos configuráveis](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | Exibe uma lista suspensa de valores que aceitam várias seleções. |
| [!UICONTROL Price] | Este tipo de entrada é usado para criar campos de preço que estão além dos atributos predefinidos: `Price`, `Special Price`, `Tier Price` e `Cost`. A moeda usada é determinada pela configuração do sistema. |
| [!UICONTROL Media Image] | Associa uma imagem extra a um produto, como um logotipo do produto, instruções de cuidados ou ingredientes de um rótulo de alimentos. Quando você adiciona um atributo de imagem de mídia ao conjunto de atributos de um produto, ele se torna um tipo de imagem extra, juntamente com Base, Pequeno e Miniatura. O atributo de imagem de mídia pode ser excluído do [navegador de mídia de vitrine](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | Permite definir [taxas FPT](../stores-purchase/fixed-product-tax.md) com base nos requisitos da sua localidade. |
| [!UICONTROL Visual Swatch] | Exibe uma amostra que representa a cor, a textura ou o padrão de um produto configurável. Uma [amostra visual](swatches.md) pode ser preenchida com um valor de cor hexadecimal ou exibir uma imagem carregada que represente a cor, o material, a textura ou o padrão da opção. |
| [!UICONTROL Text Swatch] | Uma representação baseada em texto de uma opção de produto configurável que é frequentemente usada para o tamanho. [Amostras de texto](swatches.md) também podem incluir valores de cor hexadecimais. |
| [!UICONTROL Page Builder] | Um espaço de trabalho [[!DNL Page Builder]](../page-builder/workspace.md) no local do atributo que facilita a adição de conteúdo envolvente à página do produto. |

{style="table-layout:auto"}

## Opções de data e hora

É possível personalizar o formato dos campos de data e hora e selecionar o controle de entrada usado para a entrada de dados. Os valores de datas podem ser selecionados em uma lista suspensa ou em um calendário pop-up.

![Exemplo - calendário pop-up de vitrine](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_Para formatar campos de data/hora:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel à esquerda, expanda **[!UICONTROL Catalog]** e clique no subitem **[!UICONTROL Catalog]**.

1. Expanda a seção **[!UICONTROL Date & Time Custom Options]**.

   ![Configuração do catálogo - opções de data e hora](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte as [_Opções Personalizadas de Data e Hora_](../configuration-reference/catalog/catalog.md) na _Referência de Configuração_.

1. Para usar um calendário pop-up como controle de entrada para campos de data, defina **[!UICONTROL Use JavaScript Calendar]** como `Yes`.

1. Para estabelecer o **[!UICONTROL Date Fields Order]**, defina a ordem de cada parte do campo de data conforme necessário:

   - Month
   - Dia
   - Ano

1. Para definir o formato de hora de sua preferência, defina **Formato de Hora** como um dos seguintes:

   - `12h AM/PM`
   - `24h`

1. Para estabelecer o **[!UICONTROL Year Range]** para os valores suspensos, insira o ano (AAAA) para definir as datas **[!UICONTROL from]** e **[!UICONTROL to]**.

   Se estiver em branco, o campo assumirá como padrão o ano atual.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
