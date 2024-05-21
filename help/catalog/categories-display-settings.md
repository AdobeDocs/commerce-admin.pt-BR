---
title: Categorias - Configurações de exibição
description: Saiba mais sobre como usar o [!UICONTROL Display] configurações para definir quais elementos de conteúdo aparecem em uma página de categoria e a ordem na qual os produtos aparecem.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: a47e744cf4cc5163ca2ba0718ccb78eb65a7d404
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Categorias - Configurações de exibição

As configurações de exibição determinam quais elementos de conteúdo aparecem em uma página de categoria e a ordem em que os produtos aparecem. Você pode ativar blocos CMS, definir o status de âncora da categoria e gerenciar opções de classificação na _[!UICONTROL Display Settings]_guia. Para obter exemplos de como as categorias são refletidas na loja, consulte [Navegação no catálogo](navigation.md).

![Configurações de exibição para categorias](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Display Mode] | Determina os elementos de conteúdo exibidos na página de categoria. Opções: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Quando definido como `Yes`O exibe produtos das subcategorias na categoria, mesmo que não tenham sido explicitamente adicionados à categoria, e permite a exibição dos _[!UICONTROL filter by attribute]_na navegação em camadas. Opções: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obrigatório) Os valores padrão são `Position`, `Name`, e `Price`. Para personalizar a opção de classificação, desmarque a opção **[!UICONTROL Use All Available Attributes]** e selecione os atributos que deseja usar. Você pode definir e adicionar atributos conforme necessário. Essa configuração não se aplica à variável [!DNL Live Search] [Widget da página de listagem de produtos](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obrigatório) Para definir o padrão _[!UICONTROL Sort By]_, desmarque a opção **[!UICONTROL Use Config Settings]**e selecione um atributo. Essa configuração não se aplica à variável [!DNL Live Search] [Widget da página de listagem de produtos](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Por padrão, o Commerce exibe a faixa de preços em incrementos de 10, 100 e 1000, dependendo dos produtos na lista. Para alterar a faixa de Fases de Preço, desmarque a opção **[!UICONTROL Use Config Settings]** caixa de seleção |

{style="table-layout:auto"}
