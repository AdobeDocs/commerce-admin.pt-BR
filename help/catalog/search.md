---
title: Visão geral da pesquisa no catálogo
description: Saiba mais sobre as ferramentas de Pesquisa rápida e Pesquisa avançada que os clientes podem usar para localizar produtos na loja.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
TQID: https://experienceleague.adobe.com/PV3ZrkqHaUZw-2LFHCNKUeDcvJmkvFcuoR3ZxxURP54
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 541
ht-degree: 0%

---

# Visão geral da pesquisa no catálogo

>[!TIP]
>
>O [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=pt-BR) fornece uma experiência de pesquisa rápida, relevante e intuitiva e está disponível para o Adobe Commerce sem custo adicional. Esta seção descreve a funcionalidade de pesquisa padrão que pode ser diferente de [!DNL Live Search].

Pesquisas mostram que as pessoas que usam a pesquisa têm mais probabilidade de fazer uma compra do que os clientes que dependem apenas da navegação. Na verdade, de acordo com alguns estudos, as pessoas que usam a pesquisa têm quase duas vezes mais chances de fazer uma compra.

As seções a seguir descrevem os recursos básicos de pesquisa do catálogo. Para obter informações sobre como configurar e personalizar os recursos nativos de pesquisa no catálogo, consulte:

- [Configurar pesquisa no catálogo](search-configuration.md)
- [Resultados da pesquisa](search-results.md)
- [Gerenciar termos de pesquisa](search-terms.md)

>[!NOTE]
>
>A funcionalidade de pesquisa nativa no Commerce fornece resultados de pesquisa com correspondência exata. Enquanto o [!DNL Live Search], um módulo opcional disponível para instalação e habilitação no Adobe Commerce, é implementado de forma diferente e o resultado não é limitado à sequência de pesquisa exata. Por exemplo, onde você tem dez produtos rotulados numericamente para o _Omega_: a pesquisa por `Omega 1` resulta em uma única correspondência para o _Omega 1_ com o recurso de pesquisa nativo. Mas a mesma sequência de pesquisa fornecida pelo Live Search resulta em uma correspondência para vários itens, _Ômega 1_ e _Ômega 10_.

## Pesquisa rápida

>[!NOTE]
>
>Quando o [[!DNL Live Search]](https://experienceleague.adobe.com/pt-br/docs/commerce/live-search/overview) está instalado e o widget [[!DNL Storefront Popover]](https://experienceleague.adobe.com/pt-br/docs/commerce/live-search/live-search-storefront/storefront-popover) está habilitado, a caixa de pesquisa retorna o resultado &quot;pesquisar ao digitar&quot; em um pop-over.

A caixa de pesquisa no cabeçalho da loja ajuda os visitantes a encontrar produtos no catálogo. O texto da pesquisa pode ser o nome completo ou parcial do produto ou qualquer outra palavra ou frase que descreva o produto. Os termos de pesquisa que as pessoas usam para encontrar produtos podem ser gerenciados no Administrador.

1. Para **[!UICONTROL Search]**, o cliente insere as primeiras letras do que deseja encontrar.

   Todas as correspondências no catálogo são exibidas abaixo, com o número de resultados encontrados.

1. O cliente pressiona a tecla Enter ou clica em um resultado na lista de produtos correspondentes.

   ![Pesquisar](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Pesquisa avançada

>[!NOTE]
>
>A funcionalidade de pesquisa avançada de formulário descrita aqui não se aplica a [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=pt-BR).

A Pesquisa avançada permite que os compradores pesquisem no catálogo com base nos valores inseridos em um formulário. Como o formulário contém vários campos, uma única pesquisa pode incluir vários parâmetros. O resultado é uma lista de todos os produtos no catálogo que correspondem aos critérios. Um link para Pesquisa avançada está no rodapé da loja.

![Pesquisa avançada](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Cada campo no formulário corresponde a um atributo do catálogo de produtos. Para adicionar um campo, defina as propriedades de front-end do atributo como `Include in Advanced Search`. Como prática recomendada, inclua apenas os campos que os clientes têm maior probabilidade de usar para localizar um produto, pois ter muitos atrasa a pesquisa.

1. No rodapé da loja, o cliente clica em **[!UICONTROL Advanced Search]**.

1. No formulário _Pesquisa Avançada_, o adiciona valores totais ou parciais em quantos campos forem necessários.

1. Clica em **[!UICONTROL Search]** para exibir os resultados.

   ![Resultados da Pesquisa](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. Se não vir o que está procurando nos resultados da pesquisa, o cliente clica em **[!UICONTROL Modify your search]** e tenta outra combinação de critérios.
