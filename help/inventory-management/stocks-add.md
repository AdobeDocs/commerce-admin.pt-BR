---
title: Adicionar um estoque de estoque
description: Saiba como adicionar um estoque e mapear fontes para canais de vendas (sites), fornecendo um link direto para quantidades comercializáveis e inventários de produtos.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# Adicionar um estoque

Os estoques mapeiam suas fontes para canais de vendas (ou sites), fornecendo um link direto para quantidades comercializáveis e inventários de produtos.

Ao criar um estoque personalizado, você atribui sites e fontes. As origens podem incluir origens ativadas e desativadas. Por exemplo, você pode adicionar um depósito ao estoque, preparando-se para abrir o local para gerenciar estoque e concluir remessas.

Depois de adicionar origens, você deve priorizar a ordem das origens de cima (primeiro) para baixo (último). Esse pedido afeta as recomendações durante o envio do pedido.

![Novo Estoque](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Adicionar o estoque de estoque

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Clique em **[!UICONTROL Add New Stock]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL General]** e insira um nome exclusivo **[!UICONTROL Name]** para identificar o novo estoque.

   ![Opções gerais de ações](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Sales Channels]** e selecione o **[!UICONTROL Websites]** onde esta unidade populacional está disponível.

   Para uma instalação multissite, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada site.

   >[!NOTE]
   >
   >Se você selecionar um site ou canal de vendas atribuído a outro estoque, ele será desatribuído desse estoque. Qualquer Sales Channel não atribuído a um estoque personalizado é atribuído ao Estoque padrão.

   ![opções de Sales Channel para estoques](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Sources]** e faça o seguinte para qualquer estoque que não seja o padrão:

   - Clique em **[!UICONTROL Assign Sources]**.

   ![Fontes atribuídas](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Marque as caixas de seleção para todas as origens que você deseja atribuir ao estoque.

   >[!IMPORTANT]
   >
   >Se você atribuir a mesma origem a vários estoques, poderá resultar em venda excessiva dos produtos atribuídos a essa origem.

   - Clique em **[!UICONTROL Done]**.

     As fontes adicionadas são exibidas em Fontes atribuídas.

     ![Atribuir origens ao estoque](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Uso ![Ícone Classificar](assets/icon-sort.png) para arrastar e soltar as fontes em uma prioridade de cima (primeiro) para baixo (último).

   A ordem de origem é importante ao enviar ordens.

   ![Exemplo de fontes atribuídas](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. No _[!UICONTROL Save]_(![Seta de menu](../assets/icon-menu-down-arrow-red.png)), escolha **[!UICONTROL Save & Close]**.

## Descrições dos campos

| Campo | Descrição |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Nome do estoque. Por exemplo: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Define o [escopo](../getting-started/websites-stores-views.md#scope-settings) do estoque, atribuindo o estoque a sites específicos como _canais de vendas_. Selecione um ou mais sites por estoque. Cada site só pode ser atribuído a um estoque. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Atribui origens de estoque a esse estoque. As fontes personalizadas não podem ser atribuídas ao Estoque padrão. |
| [!UICONTROL Assigned Sources] | Lista de fontes atribuídas. Arraste e solte as fontes usando ![Ícone Classificar](assets/icon-sort.png) em um pedido priorizado para atendimento e envio de pedidos.<br/><br/>**[!UICONTROL Code]**- ID de código exclusiva da origem.<br/>**[!UICONTROL Name]** - Descrição de nome da origem.<br/>**[!UICONTROL Unassign]**- Remova a origem atribuída do estoque usando ![Ícone de lixeira](../assets/icon-delete-trashcan-solid.png). |
