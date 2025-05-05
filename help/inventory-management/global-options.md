---
title: Configurar  [!DNL Inventory Management] opções globais
description: Saiba como definir as  [!DNL Inventory Management] opções de configuração padrão para o produto e o estoque de seus sites.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# Configurar opções globais do [!DNL Inventory Management]

Configure as opções de configuração padrão de produto e estoque para seus sites. Algumas dessas configurações podem ser substituídas por produto por meio de [Configurando Opções de Produto](product-options.md). Para configurar a Prioridade de Distância, consulte [Configurando o Algoritmo de Prioridade de Distância](distance-priority-algorithm.md).

## Configurar opções de produto e estoque globalmente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Inventory]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Stock Options]** e defina as opções:

   ![Opções do Stock](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Para ajustar a quantidade disponível quando um pedido for feito, defina **[!UICONTROL Decrease Stock When Order is Placed]** como `Yes`.

   - Para devolver itens para estoque se um pedido for cancelado, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** para `Yes`.

   - Para continuar a exibir produtos no catálogo que não estão mais em estoque, defina **[!UICONTROL Display Out of Stock Products]** como `Yes`.

   - Se os [alertas de preço](alert-setup.md) estiverem habilitados, os clientes poderão se inscrever para receber uma notificação quando o produto estiver novamente em estoque.

   - Para definir o início da exibição do último valor de estoque restante na página do produto, insira um valor para **[!UICONTROL Only X left Threshold]**.

     A mensagem começa a aparecer quando a quantidade em estoque atinge o limite. Por exemplo, se definida como `3`, a mensagem `Only 3 left` aparecerá quando a quantidade em estoque atingir três. A mensagem é ajustada para refletir a quantidade em estoque, até que a quantidade atinja zero.

   - Para exibir uma mensagem de &quot;Em Estoque&quot; ou &quot;Sem Estoque&quot; na página do produto, defina **[!UICONTROL Display Products Availability In Stock on Storefront]** como `Yes`.

   - Para verificar o estoque ao carregar um produto no carrinho, defina **[!UICONTROL Enable Inventory Check On Cart Load]** como `Yes`. Com esta opção desativada, a verificação do inventário é ignorada. Desativar essa opção acelera o check-out, especialmente se houver muitos itens no carrinho de compras. No entanto, se você ignorar a pré-validação, os clientes poderão ver erros de &quot;Produto esgotado&quot; posteriormente no processo de finalização.

   - Para manter a consistência entre inventário e catálogo, defina **[!UICONTROL Synchronize with Catalog]** como `Yes`. Com essa opção ativada, os dados do inventário são ajustados de acordo com as alterações do catálogo (como produto removido, SKU do produto alterado e tipo de produto alterado).

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Product Stock Options]** e defina as opções:

   - Para ativar o [controle de inventário](enable.md) para o catálogo, defina **[!UICONTROL Manage Stock]** como `Yes`.

     ![Opções de Estoque de Produtos](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Defina **[!UICONTROL Backorders]** como um dos seguintes:

     | Opção | Descrição |
     | ----- | ----- |
     | `No Backorders` | [Pedidos pendentes](backorders.md) não são aceitos quando o produto está esgotado. |
     | `Allow Qty Below 0` | Backorders são aceitos quando a quantidade cai abaixo de zero. |
     | `Allow Qty Below 0 and Notify Customer` | Backorders são aceitos quando a quantidade cair abaixo de zero e o sistema notifica o cliente que o pedido ainda pode ser feito. |

   - Insira o **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Digite um valor para **[!UICONTROL Out-of-Stock Threshold]**:

     | Valor | Descrição |
     | ----- |-----|
     | Valor positivo | Com Ordens pendentes desativadas, informe um valor positivo. |
     | Zero | Com Backorders habilitado, inserir `0` permite backorders infinitos. |
     | Valor negativo | Com Backorders ativados, é recomendável inserir um valor negativo. O valor é adicionado à Quantidade Venável. Por exemplo, insira `-50` para permitir pedidos até esse valor. |

   - Insira o **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** para o grupo e os valores selecionados.

   - Para **[!UICONTROL Notify for Quantity Below]**, insira o nível de estoque que aciona a notificação de que o item está esgotado.

   - Para ativar incrementos de quantidade para o produto, defina **[!UICONTROL Enable Qty Increments]** como `Yes`. Em seguida, para **[!UICONTROL Qty Increments]**, insira o número dos itens que devem ser comprados para atender ao requisito.

     Por exemplo, um item vendido em incrementos de seis pode ser comprado em quantidades de `6`, `12`, `18` e assim por diante.

   - Para [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** está definido como `No`. Ao submeter um aviso de crédito, você informa e seleciona para retornar o estoque às origens.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Admin bulk operations]** e defina as opções:

   ![Operações em massa do administrador](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Definir **[!UICONTROL Run asynchronously]** para executar operações em massa de forma assíncrona para ações de produtos em massa

     Essas operações incluem [atribuição e desatribuição de fontes](bulk-assignment.md) em massa e [transferência de estoque para a origem](inventory-transfer.md). Ele coleta ações em massa até o tamanho do lote Assíncrono e, em seguida, executa essas ações. Essa opção está desativada por padrão. É recomendável analisar o desempenho com ações em massa antes de habilitar.

     >[!NOTE]
     >
     >Para configurar e suportar _gerenciadores de fila assíncronos_, você deve emitir um comando usando a linha de comando. Esta etapa pode exigir ajuda do desenvolvedor. Consulte [Iniciar consumidores da fila de mensagens](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html?lang=pt-BR) no _Guia de Configuração_.

   - Se habilitado, defina o **[!UICONTROL Asynchronous batch size]**. O tamanho padrão do lote é 100. Quando os processos em massa atingem essa quantidade, o sistema a aciona.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
