---
title: Visão geral dos atributos do produto
description: Saiba mais sobre os atributos do produto e como eles são usados para descrever características específicas de um produto.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: e0468763b2314e69e8ee4922da9bb9cf65578904
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Visão geral dos atributos do produto

Os atributos são os blocos fundamentais do catálogo de produtos e descrevem características específicas de um produto. Os atributos do produto podem ser organizados em [conjuntos de atributos](attribute-sets.md), que são usados como modelos para a criação de produtos.

Os atributos determinam o tipo de controle de entrada usado para opções de produtos e fornecem informações adicionais para páginas de produtos. Eles também são usados como parâmetros de pesquisa e critérios para navegação em camadas, relatórios de comparação de produtos e promoções. É possível criar quantos atributos e conjuntos de atributos forem necessários para descrever os produtos no catálogo. Além dos atributos que você pode criar, os atributos do sistema, como preço, são incorporados à plataforma principal do Commerce e não podem ser alterados.

![Criando um novo atributo ao editar um produto](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Use as práticas recomendadas descritas nas seções a seguir ao planejar e criar atributos de produto.

## Nomes de atributo

Estabeleça convenções consistentes de nomenclatura de atributos, incluindo letras maiúsculas e minúsculas e pontuação. Por exemplo, `Color:Green` e `Color:green` podem ser considerados dois valores de atributo diferentes por sistemas diferentes. Esse ruído nos dados pode afetar as regras de negócios, os resultados da pesquisa e os filtros de dados dos aplicativos que correspondem produtos às regras.

## Uso do atributo

Considere como os atributos devem ser usados ao designar propriedades e valores. Identifique os atributos que são usados como rótulos para a apresentação, como nome do produto, imagem, preço e descrição, e quais atributos são usados para a entrada de dados. Considere como os atributos são representados em páginas diferentes em todo o site e como eles são exibidos em páginas de categoria, páginas de detalhes do produto, grades de categoria e controles deslizantes de miniatura.

## Cor

Descrições de cores específicas podem representar um desafio do ponto de vista das operações de banco de dados. Nomes de cores como &quot;Azure Skies&quot; ou &quot;Robin Egg Blue&quot; têm grande apelo, mas podem não retornar os melhores resultados quando usados como critérios de pesquisa, ou se o merchandising exigir que você especifique `Color_Family:Blue`. Considere como as cores são representadas nos resultados da pesquisa e na navegação em camadas e estabeleça algumas diretrizes para suas necessidades comerciais. Em seguida, seja consistente ao atribuir valores de atributos de cor em todo o catálogo.

## Gerenciamento de variações

Use as [opções de configurações](product-configurations.md) e os [produtos configuráveis](product-create-configurable.md) do produto para gerenciar variações nas ofertas de produtos. Esses recursos facilitam a categorização de produtos, a criação de regras de preço do carrinho e de regras de categorias dinâmicas, além de oferecer uma seleção de opções com vários tipos de entrada de texto, seleção e data.

## Pesquisa ponderada

Os atributos de produto habilitados para a [pesquisa de catálogo](search.md) podem receber um peso para atribuir a eles um valor maior nos resultados da pesquisa. Os atributos com um peso maior são retornados antes daqueles com um peso menor. Por exemplo, considere dois atributos no sistema, _cor_ com um peso de pesquisa de 3 e _descrição_ com um peso de pesquisa de 1. Uma pesquisa pela palavra _vermelho_ retorna uma lista de produtos com um valor de atributo de cor de `red`, mas não retorna produtos com descrições que contenham a palavra _vermelho_. Neste exemplo, o atributo `color` tem um peso definido maior que o atributo `description`.

## Propriedades não usadas

Remova propriedades de produtos não utilizadas para melhorar a estruturação e a indexação mais rápida.


>[OBSERVAÇÃO!]
>
>Para obter informações sobre como otimizar a configuração do atributo de produto para desempenho, consulte [Práticas recomendadas de gerenciamento de catálogo](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/planning/catalog-management#product-attributes) no _Manual de implementação_.
