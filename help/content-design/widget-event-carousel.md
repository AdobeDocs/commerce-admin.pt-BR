---
title: Widget do carrossel de eventos do catálogo
description: Saiba como usar um widget carrossel de eventos do catálogo para exibir um controle deslizante de eventos futuros em uma página.
exl-id: 4e88b253-f320-4c94-9996-94d7005effc6
feature: Page Content, Promotions/Events
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Widget do carrossel de eventos do catálogo

{{ee-feature}}

Um widget carrossel de eventos do catálogo exibe um controle deslizante de eventos futuros com um marcador de contagem regressiva para cada evento. Você pode escolher as páginas e a área do layout da página onde deseja que o carrossel apareça e controlar a largura e o número de eventos que aparecem de uma vez. O resultado obtido depende do tema, onde ele está posicionado para aparecer na página e das opções escolhidas.

![Carrossel de eventos na barra lateral esquerda](./assets/storefront-event-carousel-sidebar-gear.png){width="700" zoomable="yes"}

## Etapa 1: Ativar o widget carrossel do catálogo

Antes de começar, siga as [instruções](../merchandising-promotions/event-configure.md) para configurar o widget _Evento de catálogo_ para que ele seja habilitado para a loja.

![Configuração de evento de catálogo](./assets/config-catalog-catalog-events-1.png){width="500" zoomable="yes"}

## Etapa 2: criar o widget

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]**.

1. Na seção _[!UICONTROL Settings]_, faça o seguinte:

   - Defina **[!UICONTROL Type]** como `Catalog Events Carousel`.

   - Escolha o **[!UICONTROL Design Theme]** que é usado pelo armazenamento.

1. Clique em **[!UICONTROL Continue]**.

   ![Configurações de widget para um carrossel de eventos](./assets/widget-event-carousel-settings.png){width="500" zoomable="yes"}

1. Na seção _[!UICONTROL Storefront Properties]_, faça o seguinte:

   - Para **[!UICONTROL Widget Title]**, insira um título descritivo para o widget.

     Este título é visível somente do _Administrador_.

   - Para **[!UICONTROL Assign to Store Views]**, selecione as exibições de loja nas quais você deseja que o widget fique visível.

     Você pode selecionar um modo de exibição de loja específico ou `All Store Views`. Para selecionar várias exibições, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

   - (Opcional) Para **[!UICONTROL Sort Order]**, insira um número para determinar a ordem de exibição deste item com outros na mesma parte da página. (`0` = primeiro, `1` = segundo, `3` = terceiro e assim por diante.)

     ![Propriedades da vitrine do widget](./assets/widget-event-carousel-storefront-properties.png){width="600" zoomable="yes"}

## Etapa 3: Escolher o local

1. Na seção _Atualizações de Layout_, clique em **[!UICONTROL Add Layout Update]**.

1. Defina **[!UICONTROL Display On]** como `Specified Page`.

1. Defina **[!UICONTROL Page]** como `CMS Home Page`.

1. Defina **[!UICONTROL Container]** um dos seguintes:

   - `Main Content Area`
   - `Sidebar Additional`
   - `Sidebar Main`

   >[!NOTE]
   >
   >Os resultados variam de acordo com o tema e o layout da página. Você também deve especificar o _[!UICONTROL Catalog Events Carousel Default Template]_na configuração da categoria.

1. Se quiser que o carrossel de eventos apareça em outro local na loja, clique em **[!UICONTROL Add Layout Update]** e repita essas etapas para esse local.

   ![Atualizações de layout](./assets/widget-event-carousel-layout-updates-catalog-category-sidebar.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save and Continue Edit]**.

   Por enquanto, você pode ignorar a mensagem para atualizar o cache.

## Etapa 4: configurar as opções

1. No painel esquerdo, escolha **[!UICONTROL Widget Options]**.

1. Para **[!UICONTROL Frame Size]**, insira o número de eventos que você deseja listar no controle deslizante ao mesmo tempo.

   Para exibir apenas um evento por vez, digite `1`.

1. Para **[!UICONTROL Scroll]**, insira o número de listagens de eventos que deseja rolar por clique.

   Para rolar até o próximo evento, digite `1`.

1. Para uma largura personalizada, insira o número de pixels para **[!UICONTROL Block Custom Width]**.

   Na página de exemplo a seguir, a largura personalizada é definida como 250 pixels.

   ![Opções de widget de largura personalizada](./assets/widget-options-custom-width.png){width="400" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado a atualizar o cache, clique no link na mensagem na parte superior da página e siga as instruções.
