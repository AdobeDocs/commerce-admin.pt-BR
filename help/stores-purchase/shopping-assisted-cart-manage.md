---
title: Gerenciar um carrinho de compras
description: Saiba como ajudar um cliente com seu carrinho de compras diretamente do administrador.
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 1%

---

# Gerenciar um carrinho de compras

{{ee-feature}}

Para iniciar uma sessão de compras assistidas, o cliente deve estar conectado à sua conta na loja para disponibilizar as informações. Se o cliente não tiver uma conta, você poderá [criar um](../customers/account-create.md).

![Carrinho de compras na conta do cliente](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## Controle de ações

| Opção | Descrição |
|--- |--- |
| [!UICONTROL Remove] | Remove itens do carrinho de compras atual |
| [!UICONTROL Move to Wish List] | Move itens para a lista de desejos do cliente selecionada |

{style="table-layout:auto"}

## Botões de controle

| Botão | Descrição |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | Limpa o carrinho de compras atual de todos os produtos. |
| [!UICONTROL Update Items and Quantities|]Insira a quantidade necessária na **[!UICONTROL Qty]** e atualize o número de itens no carrinho. |
| [!UICONTROL Add selections to my cart] | Adiciona produtos de todas as seções ao carrinho. |

{style="table-layout:auto"}

## Verifique se o cliente está conectado

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   Todos os visitantes da loja e os clientes conectados aparecem na lista.

   ![Clientes Agora Online](./assets/customers-now-online.png){width="700" zoomable="yes"}

## Oferecer compras assistidas

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Na lista, abra o registro do cliente no modo de edição.

   >[!TIP]
   >
   >Para encontrar o registro do cliente com pressa, use o [Filtros](../getting-started/admin-grid-controls.md) controle.

   No perfil do cliente, em _[!UICONTROL Personal Information]_, o_[!UICONTROL Last Logged In]_ data e hora mostra que o cliente está online.

   ![Perfil do cliente de um cliente online](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. Para entrar no modo de compra assistida, clique em **[!UICONTROL Manage Shopping Cart]** na barra de botões superior.

   ![Modo de compra assistida](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## Adicionar produtos ao carrinho por atributo

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Products]** seção.

1. Localize um produto usando qualquer um dos filtros na parte superior de cada coluna.

1. Clique em **[!UICONTROL Search]**.

1. Use uma das seguintes séries de etapas, de acordo com o tipo de produto:

### Adicionar um produto simples

1. Clique no produto que deseja solicitar.

   Esta ação seleciona o registro e define **[!UICONTROL Quantity]** ao valor padrão de `1`.

1. Se necessário, atualize a quantidade solicitada.

1. À esquerda acima da grade, clique em **[!UICONTROL Add selections to my cart]**.

   ![Adicionar produto ao carrinho](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   O item de linha é adicionado ao carrinho de compras na parte superior da página.

   ![Carrinho atualizado](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### Adicionar um produto com configuração

Há três tipos de produtos que devem ser configurados antes de adicionar ao carrinho: `Bundle Product`, `Configurable Product`, e `Grouped Product`.

1. Na grade, clique em **[!UICONTROL Configure]** ao lado do nome do produto.

   ![Configurar o produto](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. No _Produtos associados_ escolha cada opção de produto para descrever o item a ser solicitado, insira o **[!UICONTROL Quantity]** e clique em **[!UICONTROL OK]**.

   O produto é selecionado com uma marca de seleção e a quantidade solicitada aparece na grade.

1. Para adicionar o produto ao carrinho, clique em **[!UICONTROL Add selections to my cart]**.

   ![Produto configurável no carrinho](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. Atualize as opções do produto no carrinho, se necessário:

   - Clique em **[!UICONTROL Configure]**.

   - Atualize as opções e clique em **[!UICONTROL OK]**.

## Adicionar produto por SKU

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Add to Shopping Cart by SKU]** seção.

1. Adicionar produtos individualmente por **[!UICONTROL SKU]** ou adicione produtos fazendo upload de um arquivo CSV.

### Adicionar itens individualmente por SKU

1. Insira o **[!UICONTROL SKU]** e **[!UICONTROL Qty]** do item a ser solicitado.

1. Para solicitar outro produto, clique em **[!UICONTROL Add another]**.

   ![Adicionar produtos por SKU](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Add selections to my cart]**.

1. Se o item for um produto configurável, escolha as opções do produto quando solicitado e clique em **[!UICONTROL Add to Shopping Cart]**.

### Adicionar produtos fazendo upload de um arquivo CSV

1. Preparar um [arquivo csv](../systems/data-csv.md) com os itens a serem adicionados ao carrinho.

   O arquivo deve conter apenas duas colunas, com `sku` e `qty` no cabeçalho.

1. Fazer upload do arquivo preparado:

   - Clique em **[!UICONTROL Choose File]**.

   - Selecione o arquivo a ser carregado a partir do diretório.

## Transferir um item

Você pode transferir itens da lista de desejos de um cliente para o carrinho e também visualizar, comparar ou solicitar itens recentemente. O número de itens em cada seção aparece entre parênteses após o cabeçalho da seção.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) uma das seguintes seções:

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. Na grade, selecione cada produto a ser solicitado e insira o **[!UICONTROL Quantity]**.

1. Para inserir as opções de um produto configurável, clique em **[!UICONTROL Configure]** e defina as opções do produto conforme necessário.

1. Clique em **[!UICONTROL Add selections to my cart]**.

1. Aplique um código de cupom, se disponível:

   - Para **[!UICONTROL Apply Coupon Code]**, insira um código de cupom válido.

   - Clique em _Aplicar_ ( ![Ícone de seta](../assets/icon-apply-arrow.png) ).

1. Ajuste a quantidade solicitada conforme necessário:

   - No **[!UICONTROL Qty]** do produto a ser ajustado, insira o valor correto.

   - Clique em **[!UICONTROL Update Items and Quantities]**.

## Criar o pedido

1. Clique em **[!UICONTROL Create Order]**.

   A variável _[!UICONTROL Create New Order]_mostra os itens no carrinho, seguidos pelas informações de envio e pagamento.

1. Preencha as informações sobre entrega e pagamento.

1. Clique em **[!UICONTROL Submit Order]**.

Para saber mais, consulte [Criar um pedido](customer-account-create-order.md).
