---
title: Configurações do produto - [!UICONTROL Search Engine Optimization]
description: Para um produto, as configurações [!UICONTROL Search Engine Optimization] definem a Chave da URL e os metadados que são usados pelos mecanismos de pesquisa para indexar o produto.
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Configurações do produto - [!UICONTROL Search Engine Optimization]

A _Otimização do mecanismo de pesquisa_ (SEO) é a prática de ajustar o conteúdo e a apresentação de um site para melhorar a forma como as páginas são indexadas pelos mecanismos de pesquisa.

As configurações de _[!UICONTROL Search Engine Optimization]_&#x200B;para um produto especificam os campos [Chave de URL](catalog-urls.md) e [metadados](../merchandising-promotions/meta-data.md) usados pelos mecanismos de pesquisa para indexar o produto. Embora alguns mecanismos de pesquisa ignorem metapalavras-chave, outros mecanismos de pesquisa continuam a usá-las. A [prática recomendada da SEO](../merchandising-promotions/seo-overview.md) atual é incorporar palavras-chave de alto valor no metatítulo e na metadescrição.

O valor padrão para cada campo de metadados pode ser gerado automaticamente com base nos valores especificados na configuração. Cada campo contém um espaço reservado que é substituído por um valor real. Para obter mais informações, consulte [Geração automática de campos de produto](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation).

## Preencha os campos de SEO

1. Abra o produto no modo de edição.

1. Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) na seção _[!UICONTROL Search Engine Optimization]_.

![Otimização do Mecanismo de Pesquisa](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. Insira o **[!UICONTROL URL Key]** (opcional).

   A chave de URL padrão é baseada no nome do produto. Você pode usar o padrão ou alterá-lo conforme necessário. Para obter mais informações, consulte [Catálogo de URLs](catalog-urls.md).

1. Insira o **[!UICONTROL Meta Title]** (opcional).

   O metatítulo é o texto que aparece na parte superior da janela do navegador. Você pode usar o padrão, que se baseia no nome do produto, ou alterá-lo conforme necessário.

1. Adicione o **[!UICONTROL Meta Keywords]** (opcional).

   As meta palavras-chave são usadas por alguns mecanismos de pesquisa mais do que outros. É uma prática recomendada inserir algumas palavras-chave de alto valor para ajudar o produto a ganhar mais visibilidade.

1. Insira o **[!UICONTROL Meta Description]**.

   A meta descrição é o texto que aparece nas listagens de resultados de pesquisa. Para obter melhores resultados, insira uma descrição com comprimento entre 150 e 160 caracteres.

## Referência do campo

| Campo | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |------------------|
| [!UICONTROL URL Key] | Exibição da loja | Determina o endereço online do produto. A chave do URL é adicionada ao URL de base da loja e aparece na barra de endereços de um navegador. Inicialmente, o Commerce cria uma URL _compatível com mecanismo de pesquisa_ que se baseia no nome do produto. A chave do URL deve ter todos os caracteres em minúsculas, com hifens não à direita entre esses caracteres em vez de espaços. Não inclua um sufixo como `.html` na chave da URL, pois ele é gerenciado na configuração. |
| [!UICONTROL Meta Title] | Exibição da loja | O título aparece na barra de título e na guia do navegador e também é usado como o título em uma página de resultados de mecanismo de pesquisa (SERP). O metatítulo deve ser exclusivo da página e ter menos de 70 caracteres. Valor gerado automaticamente: `{{name}}` |
| [!UICONTROL Meta Keywords] | Exibição da loja | Palavras-chave relevantes para o produto. Considere usar palavras-chave que os clientes possam usar para encontrar o produto. Valor gerado automaticamente: `{{name}}` |
| [!UICONTROL Meta Description] | Exibição da loja | A meta descrição fornece uma breve visão geral da página para listagens de resultados de pesquisa. Um comprimento ideal é entre 150 e 160 caracteres, com um máximo de 255 caracteres. Embora não seja visível para o cliente, alguns mecanismos de pesquisa incluem a metadescrição na página de resultados da pesquisa. Valor gerado automaticamente: `{{name}} {{description}}` |

{style="table-layout:auto"}
