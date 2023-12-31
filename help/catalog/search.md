---
title: Visão geral da pesquisa no catálogo
description: Saiba mais sobre as ferramentas de Pesquisa rápida e Pesquisa avançada que os clientes podem usar para localizar produtos na loja.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Visão geral da pesquisa no catálogo

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) O oferece uma experiência de pesquisa rápida, relevante e intuitiva e está disponível para o Adobe Commerce sem custo adicional. Esta seção descreve a funcionalidade de pesquisa padrão que pode ser diferente do [!DNL Live Search].

Pesquisas mostram que as pessoas que usam a pesquisa têm mais probabilidade de fazer uma compra do que os clientes que dependem apenas da navegação. Na verdade, de acordo com alguns estudos, as pessoas que usam a pesquisa têm quase duas vezes mais chances de fazer uma compra.

As seções a seguir descrevem os recursos básicos de pesquisa do catálogo. Para obter informações sobre como configurar e personalizar os recursos nativos de pesquisa no catálogo, consulte:

- [Configurar pesquisa no catálogo](search-configuration.md)
- [Resultados da pesquisa](search-results.md)
- [Gerenciar termos de pesquisa](search-terms.md)

>[!NOTE]
>
>A funcionalidade de pesquisa nativa no Commerce fornece resultados de pesquisa de correspondência exata. Enquanto [!DNL Live Search], um módulo opcional disponível para instalação e ativação no Adobe Commerce, é implementado de forma diferente e o resultado não se limita à sequência de pesquisa exata. Por exemplo, onde você tem dez produtos rotulados numericamente para _Ômega_: Uma pesquisa para `Omega 1` resulta em uma única correspondência para _Ômega 1_ com o recurso de pesquisa nativa. Mas a mesma sequência de pesquisa fornecida pelo Live Search resulta em uma correspondência para vários itens, _Ômega 1_ e _Ômega 10_.

## Pesquisa rápida

>[!NOTE]
>
>Quando [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) estiver instalado, a caixa de pesquisa retornará os resultados &quot;pesquisar ao digitar&quot; em um pop-up.

A caixa de pesquisa no cabeçalho da loja ajuda os visitantes a encontrar produtos no catálogo. O texto da pesquisa pode ser o nome completo ou parcial do produto ou qualquer outra palavra ou frase que descreva o produto. Os termos de pesquisa que as pessoas usam para encontrar produtos podem ser gerenciados no Administrador.

1. Para **[!UICONTROL Search]**, o cliente digita as primeiras letras do que deseja encontrar.

   Todas as correspondências no catálogo são exibidas abaixo, com o número de resultados encontrados.

1. O cliente pressiona a tecla Enter ou clica em um resultado na lista de produtos correspondentes.

   ![Pesquisar](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Pesquisa avançada

>[!NOTE]
>
>A funcionalidade de pesquisa avançada de formulário descrita aqui não se aplica a [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

A Pesquisa avançada permite que os compradores pesquisem no catálogo com base nos valores inseridos em um formulário. Como o formulário contém vários campos, uma única pesquisa pode incluir vários parâmetros. O resultado é uma lista de todos os produtos no catálogo que correspondem aos critérios. Um link para Pesquisa avançada está no rodapé da loja.

![Pesquisa avançada](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Cada campo no formulário corresponde a um atributo do catálogo de produtos. Para adicionar um campo, defina as propriedades de front-end do atributo como `Include in Advanced Search`. Como prática recomendada, inclua apenas os campos que os clientes têm maior probabilidade de usar para localizar um produto, pois ter muitos atrasa a pesquisa.

1. No rodapé da loja, o cliente clica em **[!UICONTROL Advanced Search]**.

1. No _Pesquisa avançada_ , adiciona valores inteiros ou parciais no número de campos necessário.

1. Cliques **[!UICONTROL Search]** para exibir os resultados.

   ![Resultados da pesquisa](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. Se não vir o que está procurando nos resultados da pesquisa, o cliente clica em **[!UICONTROL Modify your search]** e tenta outra combinação de critérios.
