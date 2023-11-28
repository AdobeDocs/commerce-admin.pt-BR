---
title: Criar e atualizar eventos
description: Saiba como criar um evento associado a uma categoria do catálogo.
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---

# Criar e atualizar eventos

{{ee-feature}}

Cada evento é associado a uma categoria do catálogo e somente um evento pode ser associado a qualquer categoria por vez. Para exibir uma lista de eventos futuros na sua loja, você também deve configurar um [Carrossel de eventos do catálogo](../content-design/widget-event-carousel.md) widget.

![Lista de eventos](./assets/category-events.png){width="700" zoomable="yes"}

## Criar um evento

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. No canto superior direito, clique em **[!UICONTROL Add Catalog Event]**.

1. Na árvore de categorias, escolha a categoria que deseja associar ao evento.

   Como cada categoria pode ter apenas um evento por vez, as categorias que já têm um evento são desativadas.

   ![Novo evento - árvore de categorias](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. Defina o **[!UICONTROL Catalog Event Information]**:

   ![Informações do evento de catálogo](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - Para o **[!UICONTROL Start Date]** do evento, use o calendário (![Ícone de calendário](../assets/icon-calendar.png)) para escolher a data. Use o **[!UICONTROL Hour]** e **[!UICONTROL Minute]** controles deslizantes para definir a hora em que o evento começa.

   - Para o **[!UICONTROL End Date]** do evento, use o calendário (![Ícone de calendário](../assets/icon-calendar.png)) para escolher a data. Use o **[!UICONTROL Hour]** e **[!UICONTROL Minute]** controles deslizantes para definir a hora em que o evento termina.

   - Para carregar um **[!UICONTROL Image]** para o widget de evento, clique em **[!UICONTROL Choose File]** e selecione o arquivo de imagem no seu diretório.

   - No **[!UICONTROL Sort Order]** insira um número para indicar a sequência em que esse evento aparece quando listado com outros eventos.

   - Marque a caixa de seleção de cada tipo de página no qual deseja exibir o marcador de contagem regressiva.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Atualizar eventos

Os eventos podem ser editados na página Eventos ou na categoria associada ao evento. Quando uma categoria tem um evento associado, um botão Editar evento é exibido no canto superior direito.

### Método 1: editar um evento na página Eventos

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Localize o evento na lista e abra-o no modo de edição.

1. Faça as alterações necessárias no evento.

1. Quando terminar, clique em **[!UICONTROL Save]**.

### Método 2: editar um evento de uma categoria

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Na árvore de categorias à esquerda, selecione a categoria associada ao evento.

1. No canto superior direito, clique em **[!UICONTROL Edit Even]t**.

1. Faça as alterações necessárias no evento.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Excluir um evento

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Encontre o evento na lista e abra-o no modo de edição.

1. No canto superior direito, clique em **[!UICONTROL Delete]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

## Descrições dos campos

| Campo | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Category] | Global | Ao criar um evento, esse campo é vinculado de volta à árvore de categorias. Ao editar um evento, ele vincula à página de categoria relacionada ao evento. |
| [!UICONTROL Start Date] | Global | A data e a hora de início do evento em `MMDDYYYY HH;MM` formato. Clique no ícone de calendário para selecionar a data. |
| [!DNL End Date] | Global | A data e a hora de término do evento em `MMDDYYYY HH;MM` formato. Clique no ícone de calendário para selecionar a data. |
| [!UICONTROL Image] | Exibição da loja | Carrega uma imagem que aparece no [Widget do Carrossel de eventos do catálogo](../content-design/widget-event-carousel.md). |
| [!UICONTROL Sort Order] | Global | Determina a sequência em que esse evento aparece quando listado com outros eventos. |
| [!UICONTROL Display Countdown Ticker On] | Global | Exibe o ticker de contagem regressiva no cabeçalho de cada página especificada. Opções: `Category Page` / `Product Page` |
| [!UICONTROL Status] | Global | Indica o status do evento com base na Data inicial e no intervalo de Datas final. O status é um valor somente leitura. Valores: `Open` / `Closed` / `Upcoming` |

{style="table-layout:auto"}

## Barra de botões

| Botão | Descrição |
|--- |--- |
| **[!UICONTROL Back]** | Retorna à página Eventos sem salvar o novo evento ou as alterações em um evento existente. |
| **[!UICONTROL Delete]** | Exclui o evento. |
| **[!UICONTROL Reset]** | Limpa a forma de quaisquer alterações não salvas e restaura as informações originais do evento. |
| **[!UICONTROL Save and Continue Edit]** | Salva todas as alterações e mantém o formulário aberto no modo de edição. |
| **[!UICONTROL Save]** | Salva alterações, fecha o formulário e retorna à página Eventos. |

{style="table-layout:auto"}
