---
title: "Configurar [!DNL Inventory Management] opções globais"
description: Saiba como configurar o padrão [!DNL Inventory Management] opções de configuração de produto e estoque para seus sites.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# Configurar [!DNL Inventory Management] opções globais

Configure as opções de configuração padrão de produto e estoque para seus sites. Algumas dessas configurações podem ser substituídas por produto por meio de [Configuração das opções de produto](product-options.md). Para definir as configurações de Prioridade de Distância, consulte [Configurando o algoritmo de prioridade de distância](distance-priority-algorithm.md).

## Configurar opções de produto e estoque globalmente

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Inventory]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Stock Options]** e defina as opções:

   ![Opções de estoque](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Para ajustar a quantidade em estoque quando um pedido é feito, defina **[!UICONTROL Decrease Stock When Order is Placed]** para `Yes`.

   - Para devolver itens para estoque se um pedido for cancelado, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** para `Yes`.

   - Para continuar a exibir produtos no catálogo que não estão mais no estoque, defina **[!UICONTROL Display Out of Stock Products]** para `Yes`.

   - Se [alertas de preço](alert-setup.md) estiverem ativados, os clientes poderão se inscrever para serem notificados quando o produto estiver de volta ao estoque.

   - Para definir o início da exibição do último valor de estoque restante na página do produto, insira um valor para **[!UICONTROL Only X left Threshold]**.

     A mensagem começa a aparecer quando a quantidade em estoque atinge o limite. Por exemplo, se definido como `3`, a mensagem `Only 3 left` aparece quando a quantidade em estoque atinge três. A mensagem é ajustada para refletir a quantidade em estoque, até que a quantidade atinja zero.

   - Para exibir uma mensagem &quot;Em estoque&quot; ou &quot;Sem estoque&quot; na página do produto, defina **[!UICONTROL Display Products Availability In Stock on Storefront]** para `Yes`.

   - Para verificar o estoque ao carregar um produto no carrinho, defina **[!UICONTROL Enable Inventory Check On Cart Load]** para `Yes`. Com esta opção desativada, a verificação do inventário é ignorada. Desativar essa opção acelera o check-out, especialmente se houver muitos itens no carrinho de compras. No entanto, se você ignorar a pré-validação, os clientes poderão ver erros de &quot;Produto esgotado&quot; posteriormente no processo de finalização.

   - Para manter a consistência entre o inventário e o catálogo, defina **[!UICONTROL Synchronize with Catalog]** para `Yes`. Com essa opção ativada, os dados do inventário são ajustados de acordo com as alterações do catálogo (como produto removido, SKU do produto alterado e tipo de produto alterado).

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Product Stock Options]** e defina as opções:

   - Para ativar [controle de inventário](enable.md) para o catálogo, defina **[!UICONTROL Manage Stock]** para `Yes`.

     ![Opções de estoque do produto](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Definir **[!UICONTROL Backorders]** a um dos seguintes:

     | Opção | Descrição |
     | ----- | ----- |
     | `No Backorders` | [Ordens pendentes](backorders.md) não são aceitos quando o produto está esgotado. |
     | `Allow Qty Below 0` | Backorders são aceitos quando a quantidade cai abaixo de zero. |
     | `Allow Qty Below 0 and Notify Customer` | Backorders são aceitos quando a quantidade cair abaixo de zero e o sistema notifica o cliente que o pedido ainda pode ser feito. |

   - Insira o **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Insira um valor para a variável **[!UICONTROL Out-of-Stock Threshold]**:

     | Valor | Descrição |
     | ----- |-----|
     | Valor positivo | Com Ordens pendentes desativadas, informe um valor positivo. |
     | Zero | Com Ordens pendentes ativadas, informando `0` permite ordens pendentes infinitas. |
     | Valor negativo | Com Backorders ativados, é recomendável inserir um valor negativo. O valor é adicionado à Quantidade Venável. Por exemplo, insira `-50` para permitir pedidos até esse valor. |

   - Insira o **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** para o grupo e os valores selecionados.

   - Para **[!UICONTROL Notify for Quantity Below]**, insira o nível de estoque que aciona a notificação de que o item está esgotado.

   - Para ativar incrementos de quantidade para o produto, defina **[!UICONTROL Enable Qty Increments]** para `Yes`. Em seguida, para **[!UICONTROL Qty Increments]**, insira o número dos itens que devem ser comprados para atender à exigência.

     Por exemplo, um item vendido em incrementos de seis pode ser comprado em quantidades de `6`, `12`, `18`e assim por diante.

   - Para [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** está definida como `No`. Ao submeter um aviso de crédito, você informa e seleciona para retornar o estoque às origens.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Admin bulk operations]** e defina as opções:

   ![Operações em massa do administrador](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Definir **[!UICONTROL Run asynchronously]** para executar operações em massa de forma assíncrona para ações de produtos em massa

     Essas operações incluem operações em massa [atribuindo e desatribuindo origens](bulk-assignment.md), e [transferindo inventário para origem](inventory-transfer.md). Ele coleta ações em massa até o tamanho do lote Assíncrono e, em seguida, executa essas ações. Essa opção está desabilitada por padrão. É recomendável analisar o desempenho com ações em massa antes de habilitar.

     >[!NOTE]
     >
     >Para configurar e suportar _gerenciadores de filas assíncronos_, você deve emitir um comando usando a linha de comando. Esta etapa pode exigir ajuda do desenvolvedor. Consulte [Iniciar consumidores da fila de mensagens](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) no _Guia de configuração_.

   - Se ativado, defina a variável **[!UICONTROL Asynchronous batch size]**. O tamanho padrão do lote é 100. Quando os processos em massa atingem essa quantidade, o sistema a aciona.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
