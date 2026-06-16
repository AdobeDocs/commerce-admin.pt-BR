---
title: Adicionar um estoque de estoque
description: Saiba como adicionar um estoque e mapear fontes para canais de vendas (sites), fornecendo um link direto para quantidades comercializáveis e inventários de produtos.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
TQID: https://experienceleague.adobe.com/oP-H4hvUmNunTl-hThx4ytzC6qOXa1PhK4P1omwFBUg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 409
ht-degree: 0%

---

# Adicionar um estoque

Os estoques mapeiam suas fontes para canais de vendas (ou sites), fornecendo um link direto para quantidades comercializáveis e inventários de produtos.

Ao criar um estoque personalizado, você atribui sites e fontes. As origens podem incluir origens ativadas e desativadas. Por exemplo, você pode adicionar um depósito ao estoque, preparando-se para abrir o local para gerenciar estoque e concluir remessas.

Depois de adicionar origens, você deve priorizar a ordem das origens de cima (primeiro) para baixo (último). Esse pedido afeta as recomendações durante o envio do pedido.

![Novo Estoque](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Adicionar o estoque de estoque

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Clique em **[!UICONTROL Add New Stock]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL General]** e insira um **[!UICONTROL Name]** exclusivo para identificar o novo estoque.

   ![Opções gerais de ações](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Sales Channels]** e selecione o **[!UICONTROL Websites]** onde esse estoque está disponível.

   Para uma instalação multissite, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada site.

   >[!NOTE]
   >
   >Se você selecionar um site ou canal de vendas atribuído a outro estoque, ele será desatribuído desse estoque. Todos os Canais de vendas não atribuídos a um estoque personalizado são atribuídos ao Estoque padrão.

   ![Opções de canais de vendas para estoques](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Sources]** e faça o seguinte para qualquer estoque diferente do padrão:

   - Clique em **[!UICONTROL Assign Sources]**.

   ![Fontes atribuídas](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Marque as caixas de seleção para todas as origens que você deseja atribuir ao estoque.

   >[!IMPORTANT]
   >
   >Se você atribuir a mesma origem a vários estoques, poderá resultar em venda excessiva dos produtos atribuídos a essa origem.

   - Clique em **[!UICONTROL Done]**.

     As fontes adicionadas são exibidas em Fontes atribuídas.

     ![Atribuir fontes ao estoque](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Use o ![ícone Classificar](assets/icon-sort.png) para arrastar e soltar as fontes em uma prioridade de cima (primeiro) para baixo (último).

   A ordem de origem é importante ao enviar ordens.

   ![Exemplo de fontes atribuídas](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. No menu _[!UICONTROL Save]_(![Seta do menu](../assets/icon-menu-down-arrow-red.png)), escolha **[!UICONTROL Save & Close]**.

## Descrições dos campos

| Campo | Descrição |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Nome do estoque. Por exemplo: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Define o [escopo](../getting-started/websites-stores-views.md#scope-settings) do estoque atribuindo o estoque a sites específicos como _canais de vendas_. Selecione um ou mais sites por estoque. Cada site só pode ser atribuído a um estoque. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Atribui origens de estoque a esse estoque. As fontes personalizadas não podem ser atribuídas ao Estoque padrão. |
| [!UICONTROL Assigned Sources] | Lista de fontes atribuídas. Arraste e solte as fontes usando o ![Ícone Classificar](assets/icon-sort.png) em uma ordem priorizada para atendimento e remessa de pedidos.<br/><br/>**[!UICONTROL Code]**- Identificação de código exclusivo para a origem.<br/>**[!UICONTROL Name]** - Descrição de nome da origem.<br/>**[!UICONTROL Unassign]**- Remova a origem atribuída do estoque usando o ![ícone Lixeira](../assets/icon-delete-trashcan-solid.png). |
