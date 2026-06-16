---
title: Gerenciar estoque de estoque
description: Saiba como o estoque é usado para representar um inventário agregado virtual de produtos para fontes de seus canais de vendas.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
TQID: https://experienceleague.adobe.com/IeG1bA1etAjxiDjSWY83GLNugllHT1mUrZBde45Ha8g
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 524
ht-degree: 0%

---

# Gerenciar estoque

O Stock representa um inventário agregado virtual de produtos para fontes de seus canais de vendas (sites). Dependendo da configuração do site, o estoque pode ser atribuído a um ou mais canais de vendas. Cada canal de vendas só pode ter um único estoque atribuído a ele, e um único estoque pode ser atribuído a vários canais de vendas. Por meio do estoque, você pode modificar a priorização das fontes usadas à medida que os pedidos chegam por meio de um canal de vendas.

Você começa com um Estoque padrão que não pode ser removido ou desativado. Você pode adicionar outros canais de vendas somente ao estoque. A única origem atribuída é o Source padrão. Esse estoque é usado por comerciantes de origem única, integrações de terceiros e produtos importados.

Os Canais de vendas representam entidades que vendem seu inventário. Por padrão, o [!DNL Commerce] fornece os sites da loja como canais de vendas. Os canais de vendas podem ser estendidos para oferecer suporte a canais adicionais, como grupos de clientes B2B e visualizações de loja. Cada canal de vendas pode ser associado a apenas um Stock.

- **Suporte da Sales Channel** - Os canais de vendas atualmente incluem sites prontos para uso. Você pode estender canais de vendas para incluir opções personalizadas, como grupos de clientes B2B e exibições de loja. Cada canal de vendas só pode ter um único estoque atribuído a ele. Um único estoque pode ser atribuído a vários canais de vendas.
- **Mapear para Fontes** - Cada estoque pode ter uma ou mais fontes habilitadas ou desabilitadas atribuídas, calculando o estoque agregado virtual por produto.
- **Atendimento de pedidos por prioridade** - O algoritmo de prioridade pronto para uso do algoritmo de seleção Source usa a lista de origem do estoque de cima para baixo ao atender pedidos.

O diagrama a seguir ajuda a definir como um Stock funciona em relação a Origens e Canais de Vendas para um comerciante de uma Loja de Bicicletas.

![Diagrama para exemplo de ações para um armazenamento](assets/diagram-stock.png){width="600" zoomable="yes"}

## Exemplo de ações para uma mountain bike e loja

Todos os armazenamentos começam com um Estoque padrão. Ele deve permanecer `Enabled` pelos seguintes motivos:

- Ele é usado ao importar novos produtos, atribuindo automaticamente produtos à fonte padrão e ao estoque para acesso imediato a [!DNL Inventory Management].
- Não é possível adicionar outras fontes além do Source padrão a esse estoque.
- Ela é necessária e usada por comerciantes de origem única, produtos de pacote e produtos agrupados.

Para comerciantes de várias origens, crie e configure estoques para melhor se adequar às suas lojas e ao atendimento de pedidos. Quando você atribui um novo estoque a um canal de vendas, qualquer estoque pré-existente nesse canal de vendas se torna não atribuído.

Para uma instalação com várias lojas, o Estoque Padrão é atribuído inicialmente ao [Site Principal](../stores-purchase/stores.md#add-websites){target="_blank"} e à loja padrão. O estoque e as quantidades corretos são exibidos para produtos habilitados e desabilitados na exibição de grade **[!UICONTROL Products]**.

![Gerenciar Estoque](assets/inventory-stock.png){width="600" zoomable="yes"}

## Barra de botões

| Botão | Descrição |
|--|--|
| [!UICONTROL Add New Stock] | Abre o formulário _[!UICONTROL New Stock]_usado para inserir um novo estoque de estoque para mapear o estoque para o canal de vendas. |

## Descrições da coluna Gerenciar estoque

| Coluna | Descrição |
|--|--|
| [!UICONTROL ID] | ID numérica exclusiva gerada para a entrada de estoque. |
| [!UICONTROL Name] | Nome exclusivo que identifica o estoque de estoque. |
| [!UICONTROL Sales Channels] | Define o escopo do estoque atribuindo o estoque a sites específicos como _canais de vendas_. |
| [!UICONTROL Assigned sources] | Fontes atribuídas ao estoque que fornecem todas as quantidades de produtos. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Abre o registro de estoque de estoque no modo de edição. |
