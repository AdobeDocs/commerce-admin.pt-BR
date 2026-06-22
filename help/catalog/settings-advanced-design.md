---
title: Configurações do produto - [!UICONTROL Design]
description: Para um produto, as configurações de [!UICONTROL Design] permitem aplicar um tema diferente a uma página de produto e alterar o layout.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
TQID: https://experienceleague.adobe.com/u6VzZ9TiovuSopBcBjmpQTKl3pzh3DoXXzpr8akWp-8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 0%

---

# Configurações do produto - [!UICONTROL Design]

As configurações de _[!UICONTROL Design]_&#x200B;permitem que um tema diferente seja aplicado à página do produto, alteram o layout da coluna, determinam onde as opções do produto são exibidas e inserem o código XML personalizado.

![Design](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Quando o mesmo produto é atribuído a várias categorias com configurações de design diferentes para cada categoria, é recomendável definir **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` nas [opções de configuração de Otimização do Mecanismo de Pesquisa](../configuration-reference/catalog/catalog.md#search-engine-optimization). Para acessar esta configuração, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, expanda **[!UICONTROL Catalog]**&#x200B;e escolha **[!UICONTROL Catalog]**&#x200B;abaixo no painel esquerdo e, em seguida, expanda a seção **[!UICONTROL Search Engine Optimization]**&#x200B;na página.

| Campo | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|---|---|----|
| [!UICONTROL Theme] | Exibição da loja | ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Oferece a capacidade de aplicar um tema diferente ao produto. Opções: (todos os temas disponíveis) |
| [!UICONTROL Layout] | Exibição da loja | Oferece a capacidade de aplicar um [layout](../content-design/page-layout.md) diferente à página do produto. Opções: <br/>**[!UICONTROL No layout updates]**- Por padrão, as atualizações de layout não estão disponíveis para a página do produto.<br/>**[!UICONTROL Empty]** - Permite definir seu próprio layout, como uma página de 4 colunas. (Requer compreensão de XML.) <br/>**[!UICONTROL 1 column]**- Aplica um layout de uma coluna à página do produto.<br/>**[!UICONTROL 2 columns with left bar]** - Aplica um layout de duas colunas com uma barra lateral esquerda à página do produto. <br/>**[!UICONTROL 2 columns with right bar]**- Aplica um layout de duas colunas com uma barra lateral direita à página do produto.<br/>**[!UICONTROL 3 columns]** - Aplica um layout de três colunas à página do produto. <br/>**[!UICONTROL Page -- Full Width]**- (Requer [[!DNL Page Builder]](../page-builder/introduction.md)) Aplica o layout de largura total das páginas do CMS à página do produto.<br/>**[!UICONTROL Category -- Full Width]** - (Requer [!DNL Page Builder]) Aplica o layout de largura total das páginas de categoria à página do produto. <br/>**[!UICONTROL Product -- Full Width]**- (Requer [!UICONTROL Page Builder]) Aplica o layout de largura total das páginas do produto à página do produto. |
| [!UICONTROL Display Product Options In] | Exibição da loja | Determina onde as opções do produto são exibidas na página do produto. Opções: `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Exibição da loja | Usado para acessar opções para atualizar um layout personalizado na página do produto. |

{style="table-layout:auto"}

