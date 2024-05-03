---
title: Atualizações programadas de produto
description: Saiba como agendar alterações nas listas de produtos para dar suporte a campanhas e programas promocionais.
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Agendar atualizações do produto

{{ee-feature}}

As atualizações de produtos podem ser aplicadas de acordo com o agendamento e agrupadas com outras alterações de conteúdo. Você pode usar [preparo de conteúdo](../content-design/content-staging.md) para criar uma campanha com base em alterações programadas no produto ou aplicar as alterações a uma campanha existente.

>[!NOTE]
>
>A variável [!UICONTROL Set Product as New From] e [!UICONTROL To] campos e [!UICONTROL Schedule Design Update] As guias do foram removidas em ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce e não podem ser modificados diretamente no produto. Você deve criar uma atualização agendada para essas ativações.

>[!NOTE]
>
>Todas as atualizações programadas são aplicadas consecutivamente, o que significa que qualquer entidade pode ter apenas uma atualização programada de cada vez. Qualquer atualização agendada é aplicada a todas as exibições de loja dentro de seu período de tempo. Como resultado, uma entidade não pode ter atualizações agendadas diferentes para exibições de loja diferentes ao mesmo tempo. Todos os valores de atributo de entidade em todas as exibições de armazenamento, que não são afetados pela atualização agendada atual, são obtidos dos valores padrão, e não da atualização agendada anterior.

>[!NOTE]
>
>Uma visualização de preparo para uma atualização agendada sempre começa no **padrão** visualização de loja, que emula a experiência do cliente de navegar pela campanha de atualização de preparo.

## Criar uma atualização agendada

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecione um produto existente e clique em **[!UICONTROL Edit]**.

1. Clique em **[!UICONTROL Schedule New Update]**.

1. Selecionar **[!UICONTROL Save as a New Update]**.

1. Para **[!UICONTROL Update Name]**, digite um nome para a nova campanha de preparo de conteúdo.

1. Insira um resumo **[!UICONTROL Description]** da atualização e como ela será usada.

1. Usar o calendário (![ícone de calendário](../assets/icon-calendar.png)) para escolher a **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** para a campanha.

   >[!NOTE]
   >
   >Campaign **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** deve ser definido usando o **_padrão_** Fuso horário do administrador, que é convertido do fuso horário local para cada site. Por exemplo, com vários sites em fusos horários diferentes nos quais você deseja iniciar uma campanha com base em um fuso horário dos EUA, é necessário agendar uma atualização separada para cada fuso horário local. Definir **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** para cada, e é convertido do fuso horário do site local para o fuso horário padrão do Administrador.

   ![Agendar como uma nova atualização](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. Role para baixo até _[!UICONTROL Price]_e clique em **[!UICONTROL Advanced Pricing]**.

1. Insira um **[!UICONTROL Special Price]** do produto durante a campanha agendada e clique em **[!UICONTROL Done]**.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Atribuir a atualização existente

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selecione um produto existente e clique em **[!UICONTROL Edit]**.

1. Clique em **[!UICONTROL Schedule New Update]**.

1. Selecionar **[!UICONTROL Assign to Existing Campaign]**.

1. Na lista, selecione a campanha que deve ser modificada.

   ![Atribuir a uma campanha existente](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Exibir a alteração agendada

A alteração programada é exibida na parte superior da página do produto, com as datas de início e término da campanha.

![Alteração programada](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## Editar a alteração agendada

1. No _[!UICONTROL Scheduled Changes]_na parte superior da página, clique em **[!UICONTROL View/Edit]**.

1. Faça as alterações necessárias na atualização agendada.

1. Clique em **[!UICONTROL Save]**.

## Remover a alteração agendada

1. No _[!UICONTROL Scheduled Changes]_na parte superior da página, clique em **[!UICONTROL View/Edit]**.

1. Na barra superior, clique em **[!UICONTROL Remove from Update]**.

   ![Remover Alteração Agendada](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. Na caixa de diálogo, selecione **[!UICONTROL Delete the Update]** e clique em **[!UICONTROL Done]**.

   >[!NOTE]
   >
   >O produto é removido da atualização e todas as alterações agendadas são perdidas.

## Programar uma atualização de design

{{ce-feature}}

A variável _[!UICONTROL Schedule Design Update]_oferece a capacidade de fazer alterações temporárias na aparência da página do produto. Você pode agendar alterações de design para uma temporada, promoção ou apenas para atualizar as coisas. As alterações de design podem ser programadas com antecedência para entrarem em vigor ou_ gotejar _, de acordo com a programação definida.

![Atualização programada do design](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| Campo | Descrição |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Determina o intervalo de datas em que um layout personalizado é aplicado ao produto. |
| [!UICONTROL New Theme] | Aplica um tema personalizado ao produto. |
| [!UICONTROL New Layout] | Aplica um layout diferente à página do produto. Opções: <br/>**[!UICONTROL No layout updates]**- Por padrão, as atualizações de layout não estão disponíveis para a página do produto.<br/>**[!UICONTROL Empty]** - Permite definir seu próprio layout, como uma página de 4 colunas. (Requer compreensão de XML.) <br/>**[!UICONTROL 1 column]**- Aplica um layout de uma coluna à página do produto.<br/>**[!UICONTROL 2 columns with left bar]** - Aplica um layout de duas colunas com uma barra lateral esquerda à página do produto. <br/>**[!UICONTROL 2 columns with right bar]**- Aplica um layout de duas colunas com uma barra lateral direita à página do produto.<br/>**[!UICONTROL 3 columns]** - Aplica um layout de três colunas à página do produto. |

{style="table-layout:auto"}
