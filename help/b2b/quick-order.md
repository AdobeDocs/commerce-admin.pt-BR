---
title: Pedidos rápidos
description: Saiba mais sobre a funcionalidade de pedidos rápidos e como habilitá-la para seus clientes.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Pedidos rápidos

O recurso _Pedido rápido_ reduz o processo de pedido a vários cliques para clientes que sabem o nome do produto ou a SKU dos produtos que desejam solicitar. Pedidos com vários SKUs podem ser informados manualmente ou importados para o formulário Pedido rápido. O Pedido rápido pode ser usado por clientes que estão conectados a suas contas e por convidados. Quando habilitado, o link _Pedido Rápido_ aparece na parte superior da página, ao lado do nome do cliente.

![Link de Pedido Rápido](./assets/quick-order-link.png){width="700" zoomable="yes"}

## Habilitar pedidos rápidos para sua loja

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Na seção _[!UICONTROL General]_&#x200B;do painel esquerdo, escolha **[!UICONTROL B2B Features]**.

1. Defina **[!UICONTROL Enable Quick Order]** como `Yes`.

   ![Habilitar Pedido Rápido](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, clique em [Gerenciamento de cache](../systems/cache-management.md) e atualize todos os caches inválidos.

## Fluxos de trabalho de pedido rápido

Os clientes podem especificar produtos para pedidos rápidos usando um dos métodos a seguir.

### Método 1: informar produtos individuais

1. O cliente clica no link **[!UICONTROL Quick Order]**.

1. Seleciona o produto por SKU ou nome do produto:

   Para fazer um pedido rápido do **por SKU**, o cliente faz o seguinte:

   - Entra no **[!UICONTROL SKU]**.

   - Cliques **[!UICONTROL Add to List]**.

     O SKU aparece na linha de entrada, com os detalhes do produto abaixo.

     ![Detalhes do Pedido Rápido](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   Para fazer um pedido rápido do **pelo nome do produto**, o cliente faz o seguinte:

   - Insira os primeiros caracteres de **[!UICONTROL Product Name]**.

     >[!NOTE]
     >
     >Não use a tecla _Enter_ para escolher o nome do produto.

   - Quando a lista de correspondências possíveis for exibida, o cliente clicará no produto que deseja solicitar.

     ![Clique para Escolher o Nome do Produto](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. Entra no **[!UICONTROL Qty]**.

1. Usando a próxima linha de entrada, repete esse processo quantas vezes forem necessárias.

1. Cliques **[!UICONTROL Add to Cart]**.

### Método 2: informar vários produtos

1. Na caixa **[!UICONTROL Enter Multiple SKUs]**, o cliente realiza uma das ações a seguir:

   - Insere um SKU por linha

   - Insere todos os SKUs na mesma linha, separados por vírgulas e sem espaços.

     ![Inserir várias SKUs](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. Para adicionar os produtos à lista, clique em **[!UICONTROL Add to List]**.

1. Insira o **[!UICONTROL Qty]** a ser ordenado para cada item na lista.

   ![Lista de Pedidos Rápidos](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se o produto tiver opções necessárias, o cliente será solicitado a escolher as opções. Eles podem aguardar até chegarem ao carrinho de compras para adicionar opções de produto.

   ![Escolher Opções](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### Método 3: carregar uma lista de produtos

1. Na seção _[!UICONTROL Add from File]_, clique em **[!UICONTROL Download Sample]**&#x200B;para baixar um modelo de pedido.

   ![Adicionar do Arquivo](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. Abre o arquivo baixado.

1. Usa o modelo para adicionar os SKUs do produto a serem carregados para a lista de Pedidos rápidos.

1. Quando terminar, clica em **[!UICONTROL Save]**.

   ![SKUs para Carregar](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. Para carregar o arquivo, clique em **[!UICONTROL Choose]** e selecione o arquivo no sistema.

   Os itens são adicionados à lista de Pedidos rápidos.

1. Quando estiver pronto, clica em **[!UICONTROL Add to Cart]**.

Depois que o cliente cria o pedido rápido, ele pode prosseguir com a finalização da compra como de costume.

![Pedido Rápido](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
