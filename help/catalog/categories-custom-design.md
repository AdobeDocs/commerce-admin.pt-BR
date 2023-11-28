---
title: Categorias - Configurações de design
description: Saiba mais sobre como usar o [!UICONTROL Design] configurações para definir a aparência de uma categoria, todas as páginas de produto associadas e o layout da página.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Categorias - Configurações de design

A variável _[!UICONTROL Design]_fornece controle sobre a aparência de uma categoria, todas as páginas de produto associadas e o layout da página. É possível personalizar uma página de categoria e seus produtos associados para uma promoção ou para diferenciar a categoria. Por exemplo, você pode desenvolver um design especial para uma marca ou linha especial de produtos ou aplicar uma atualização por um período específico.

![Configurações de design para uma categoria](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Quando um mesmo produto é atribuído a várias categorias com configurações de design diferentes para cada categoria, é recomendável definir **Usar caminho de categorias para URLs de produtos** = `Yes` no [Opções de configuração de Otimização do mecanismo de pesquisa](../configuration-reference/catalog/catalog.md#search-engine-optimization). Para acessar essa configuração, acesse  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, expandir **[!UICONTROL Catalog]**e escolha **Catálogo**abaixo no painel esquerdo e, em seguida, expanda a variável **Otimização do mecanismo de pesquisa**na página.

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Permite que a categoria atual herde as configurações de design da categoria principal. Se usados, todos os outros campos na seção Design ficarão indisponíveis. Opções: `Yes` / ` No` |
| [!UICONTROL Theme] | Aplica um tema personalizado à categoria. |
| [!UICONTROL Layout] | Aplica um layout diferente à página de categoria. Opções: <br/>**[!UICONTROL No layout updates]**- Por padrão, as atualizações de layout não estão disponíveis para páginas de categoria.<br/>**[!UICONTROL Empty]** - Use para definir seu próprio layout de página. (Requer compreensão de XML.) <br/>**[!UICONTROL 1 column]**- Aplica um layout de uma coluna à página de categoria.<br/>**[!UICONTROL 2 columns with left bar]** - Aplica um layout de duas colunas com uma barra lateral esquerda à página de categoria. <br/>**[!UICONTROL 2 columns with right bar]**- Aplica um layout de duas colunas com uma barra lateral direita à página de categoria.<br/>**[!UICONTROL 3 columns]** - Aplica um layout de três colunas à página de categoria.<br/>**[!UICONTROL Page -- Full Width]**- (Exige [Page Builder](../page-builder/introduction.md)) Aplica o layout de largura total das páginas CMS à página de categoria.<br/>**[!UICONTROL Category -- Full Width]** - (Exige o Page Builder) Aplica o layout de largura total das páginas de categoria à página de categoria. <br/>**[!UICONTROL Product -- Full Width]**- (Exige o Page Builder) Aplica o layout de largura total das páginas de produto à página de categoria. |
| [!UICONTROL Custom Layout Update] | Lista os arquivos de atualização de layout personalizado disponíveis no servidor. Escolha a atualização de layout personalizado que deseja aplicar à categoria. |
| [!UICONTROL Apply Design to Products] | Quando selecionada, aplica as configurações personalizadas a todos os produtos na categoria. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

A variável _[!UICONTROL Scheduled Design Update]_determina o intervalo de datas em que um design personalizado é aplicado às páginas de categoria.

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Determina o intervalo de datas quando um layout personalizado é aplicado à categoria. |

![Atualização programada do design](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
