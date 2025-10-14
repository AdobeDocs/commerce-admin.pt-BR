---
title: Arquivar ordens
description: Saiba como configurar o arquivo de pedidos para melhorar o desempenho e simplificar o Commerce para sua organização.
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Arquivar ordens

{{ee-feature}}

O arquivamento de pedidos melhora regularmente o desempenho e mantém seu espaço de trabalho livre de informações desnecessárias, para que você possa se concentrar nos negócios atuais. NFFs, entregas e avisos de crédito podem ser arquivados automática ou manualmente e podem ser exibidos a qualquer momento.

>[!NOTE]
>
>A opção _[!UICONTROL Archive]_&#x200B;aparece no menu [[!UICONTROL Sales]](sales-menu.md) somente quando o arquivamento está [habilitado](../configuration-reference/sales/sales.md).

## Configurar o arquivo de pedidos

Sua loja pode ser configurada para arquivar ordens, NFFs, entregas e avisos de crédito após um número definido de dias. Você pode mover pedidos e seus documentos associados para o arquivo morto ou restaurá-los ao estado anterior. Os pedidos arquivados não são excluídos e permanecem disponíveis no Administrador. Os dados arquivados podem ser exportados para um arquivo CSV e abertos em uma planilha. Quando habilitada, a ação _Arquivar_ aparece na parte superior do espaço de trabalho.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda a seção **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales]** abaixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]**.

   ![Configurações de Pedidos, Faturas, Remessas, Arquivamento de Avisos de Crédito](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Enable Archiving]** como `Yes`.

   >[!NOTE]
   >
   >Se você decidir desativar o arquivamento posteriormente, todas as ordens arquivadas serão restauradas ao estado anterior.

1. Defina **[!UICONTROL Archive Orders Purchased]** como o número de dias de espera antes que os pedidos concluídos sejam arquivados.

   Por padrão, os pedidos são arquivados 30 dias após a compra.

1. Na lista **[!UICONTROL Order Statuses to be Archived]**, selecione cada status de pedido a ser usado para identificar pedidos a serem arquivados.

   Para selecionar vários itens, mantenha pressionada a tecla Ctrl (Windows) ou Command (Mac) enquanto clica em cada item.

1. Clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, atualize qualquer cache inválido.

## Visualizar documentos arquivados

1. No menu _[!UICONTROL Sales]_, em&#x200B;_[!UICONTROL Archive]_, escolha uma das opções a seguir:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Para exibir detalhes, clique em qualquer documento arquivado na lista.

## Aplicar uma ação a um documento arquivado

Selecione cada documento para ser o destino da ação e escolha um dos seguintes **[!UICONTROL Actions]**:

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## Arquivar documentos manualmente

1. Selecione o tipo do documento a ser arquivado a partir do seguinte:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Marque a caixa de seleção de cada item que você deseja arquivar.

1. No canto superior direito, defina **[!UICONTROL Actions]** como `Move to Archive`.

1. Clique em **[!UICONTROL Submit]** para arquivar os documentos selecionados.

## Restaurar documentos arquivados

1. Escolha o tipo de documento que deseja restaurar.

1. Selecione documentos usando uma das seguintes opções:

   - Para selecionar todos os documentos visíveis, no canto superior esquerdo, clique em **[!UICONTROL Select Visible]**.

   - Marque manualmente a caixa de seleção de cada documento que você deseja restaurar.

1. No canto superior direito, defina **[!UICONTROL Action]** como `Move to Orders Management`.

1. Clique em **[!UICONTROL Submit]** para restaurar os documentos.

## Exportar documentos arquivados

1. Escolha o tipo de documento que deseja exportar.

1. No menu superior direito, defina **[!UICONTROL Export to:]** como um dos seguintes valores:

   - `CSV`
   - `Excel`

1. Clique em **[!UICONTROL Export]**.

Sua loja pode ser configurada para arquivar ordens, NFFs, entregas e avisos de crédito após um número definido de dias. Você pode mover pedidos e seus documentos associados para o arquivo morto ou restaurá-los ao estado anterior. Os pedidos arquivados não são excluídos e permanecem disponíveis no Administrador. Os dados arquivados podem ser exportados para um arquivo CSV e abertos em uma planilha. Quando habilitado, o comando _[!UICONTROL Archive]_&#x200B;aparece na parte superior do espaço de trabalho.

## Arquivar ordens manualmente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Para selecionar a ordem na grade, marque a caixa de seleção na primeira coluna.

1. Defina o controle **[!UICONTROL Actions]** como `Move to Archive` e procure a mensagem de que a ordem foi arquivada.

   ![Movendo ordens selecionadas para o arquivo morto &#x200B;](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>Para especificar uma lista de status de pedidos que podem ser arquivados, consulte [Configurar o arquivo de pedidos](#configure-the-order-archive).

## Exibir um pedido arquivado

1. Abra a exibição de arquivamento usando um dos seguintes métodos:

   - Na barra de botões acima da grade _[!UICONTROL Orders]_, clique em **[!UICONTROL Go to Archive]**.

   - Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >Assim como a página Pedidos, o título da página de pedidos arquivados é _[!UICONTROL Orders]_. A única diferença visível é a opção na barra de botões para&#x200B;_[!UICONTROL Return to Orders Management]_. O URL da página também indica que você está na ordem de arquivamento.

1. Na coluna _Ação_, clique em **[!UICONTROL View]**.

   ![Exibir uma ordem arquivada](./assets/order-archived-view.png){width="600" zoomable="yes"}

## Restaurar uma ordem arquivada

>[!NOTE]
>
>Uma ordem restaurada a partir de uma ordem arquivada é arquivada novamente de acordo com o número de dias configurado na configuração [!UICONTROL Archive Orders Purchased] (consulte [Configurar o arquivo de ordem](#configure-the-order-archive)). O número de dias é calculado em relação à data [!UICONTROL Updated At] do pedido, que é alterada quando o pedido é movido do arquivo.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Na barra de botões, clique em **[!UICONTROL Go to Archive]**.

1. Localize o registro a ser restaurado e clique na caixa de seleção para selecioná-lo.

   ![Selecionar ordem para ser restaurada](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. Defina o valor de controle **[!UICONTROL Actions]** como `Move to Order Management`.

Procure a mensagem informando que a ordem arquivada foi removida do arquivamento.

## Exportar ordem arquivada

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. No menu de ações, clique em **[!UICONTROL Export]** e selecione o formato desejado.
