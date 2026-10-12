---
title: Categorias - Configurações de design
description: Saiba mais sobre como usar as configurações do [!UICONTROL Design] para definir a aparência de uma categoria, todas as páginas de produto associadas e o layout da página.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
TQID: 'https://experienceleague.adobe.com/cRTRPl-UTfAKXY8rmtVKlnAZooVWpTCjSkVSdNHXp28'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%
---
# Categorias - Configurações de design

A seção _[!UICONTROL Design]_oferece controle sobre a aparência de uma categoria, todas as páginas de produto associadas e o layout da página. É possível personalizar uma página de categoria e seus produtos associados para uma promoção ou para diferenciar a categoria. Por exemplo, você pode desenvolver um design especial para uma marca ou linha especial de produtos ou aplicar uma atualização por um período específico.

![Configurações de design para uma categoria](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Quando o mesmo produto é atribuído a várias categorias com configurações de design diferentes para cada categoria, é recomendável definir **Usar Caminho de Categorias para URLs de Produtos** = `Yes` nas [opções de configuração da Otimização do Mecanismo de Pesquisa](../configuration-reference/catalog/catalog.md#search-engine-optimization). Para acessar esta configuração, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, expanda **[!UICONTROL Catalog]**e escolha **Catálogo**no painel esquerdo e, em seguida, expanda a seção **Otimização do Mecanismo de Pesquisa**na página.

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Permite que a categoria atual herde as configurações de design da categoria principal. Se usados, todos os outros campos na seção Design ficarão indisponíveis. Opções: `Yes` / ` No` |
| [!UICONTROL Theme] | Aplica um tema personalizado à categoria. |
| [!UICONTROL Layout] | Aplica um layout diferente à página de categoria. Opções: <br/>**[!UICONTROL No layout updates]**- Por padrão, as atualizações de layout não estão disponíveis para páginas de categoria.<br/>**[!UICONTROL Empty]** - Use para definir seu próprio layout de página. (Requer compreensão de XML.) <br/>**[!UICONTROL 1 column]**- Aplica um layout de uma coluna à página de categoria.<br/>**[!UICONTROL 2 columns with left bar]** - Aplica um layout de duas colunas com uma barra lateral esquerda à página de categoria. <br/>**[!UICONTROL 2 columns with right bar]**- Aplica um layout de duas colunas com uma barra lateral direita à página de categoria.<br/>**[!UICONTROL 3 columns]** - Aplica um layout de três colunas à página de categoria.<br/>**[!UICONTROL Page -- Full Width]**- (Requer o [Page Builder](../page-builder/introduction.md)) Aplica o layout de largura total das páginas do CMS à página de categoria.<br/>**[!UICONTROL Category -- Full Width]** - (Exige o Page Builder) Aplica o layout de largura total das páginas de categoria à página de categoria. <br/>**[!UICONTROL Product -- Full Width]**- (Exige o Page Builder) Aplica o layout de largura total das páginas de produto à página de categoria. |
| [!UICONTROL Custom Layout Update] | Lista os arquivos de atualização de layout personalizado disponíveis no servidor. Escolha a atualização de layout personalizado que deseja aplicar à categoria. |
| [!UICONTROL Apply Design to Products] | Quando selecionada, aplica as configurações personalizadas a todos os produtos na categoria. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

A seção _[!UICONTROL Scheduled Design Update]_determina o intervalo de datas quando um design personalizado é aplicado a páginas de categoria.

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Determina o intervalo de datas quando um layout personalizado é aplicado à categoria. |

![Atualização de Design Agendada](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
