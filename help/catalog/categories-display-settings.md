---
title: Categorias - Configurações de exibição
description: Saiba mais sobre como usar as configurações do [!UICONTROL Display] para definir quais elementos de conteúdo aparecem em uma página de categoria e a ordem em que os produtos aparecem.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/t5UfvWvJ7R-kZb5kyMwpzwI2gfs3x3g1amlfWzQcAsw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# Categorias - Configurações de exibição

As configurações de exibição determinam quais elementos de conteúdo aparecem em uma página de categoria e a ordem em que os produtos aparecem. Você pode habilitar blocos do CMS, definir o status de âncora da categoria e gerenciar opções de classificação na guia _[!UICONTROL Display Settings]_. Para obter exemplos de como as categorias são refletidas na loja, consulte [Navegação no catálogo](navigation.md).

![Configurações de Exibição para categorias](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Display Mode] | Determina os elementos de conteúdo exibidos na página de categoria. Opções: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Quando definido como `Yes`, exibe produtos das subcategorias na categoria, mesmo que eles não tenham sido explicitamente adicionados à categoria, e habilita a exibição da seção _[!UICONTROL filter by attribute]_&#x200B;na navegação em camadas. Opções: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obrigatório) Os valores padrão são `Position`, `Name` e `Price`. Para personalizar a opção de classificação, desmarque a caixa de seleção **[!UICONTROL Use All Available Attributes]** e selecione os atributos que deseja usar. Você pode definir e adicionar atributos conforme necessário. Esta configuração não se aplica ao [!DNL Live Search] [Widget de página de listagem de produtos](https://experienceleague.adobe.com/pt-br/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obrigatório) Para definir a opção _[!UICONTROL Sort By]_&#x200B;padrão, desmarque a caixa de seleção **[!UICONTROL Use Config Settings]**&#x200B;e selecione um atributo. Esta configuração não se aplica ao [!DNL Live Search] [Widget de página de listagem de produtos](https://experienceleague.adobe.com/pt-br/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Por padrão, o Commerce exibe a faixa de preços em incrementos de 10, 100 e 1000, dependendo dos produtos na lista. Para alterar o intervalo de Etapas de Preço, desmarque a caixa de seleção **[!UICONTROL Use Config Settings]**. |

{style="table-layout:auto"}
