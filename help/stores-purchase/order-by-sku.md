---
title: Solicitar por SKU
description: Saiba como configurar sua loja para aceitar pedidos feitos pelo SKU como conveniência para seus clientes.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Solicitar por SKU

{{ee-feature}}

Um &quot;SKU&quot; é uma &quot;Unidade de manutenção de estoque&quot;. As SKUs geralmente ajudam os vendedores online a identificar as características mais importantes do produto, como tamanho, cor, preço e material. As IDs de produto são diferentes das SKUs:

- A variável `Product ID` é uma série sequencial de números usados internamente para identificar produtos e que não estão disponíveis para os clientes.
- A variável `SKU` é gerado pelo vendedor, normalmente com base no nome do produto e nos atributos para marketing ou rastreamento interno. Por exemplo: Uma camiseta azul de algodão, tamanho médio: T-COT-MED-BL. O SKU pode ser alterado pelo vendedor, se necessário.

Normalmente, um SKU inclui um conjunto de abreviações que indicam as características distintivas do produto. O comprimento máximo do SKU é de 64 caracteres. As SKUs são importantes para rastrear e gerenciar com eficiência o inventário, portanto, configurá-las corretamente é essencial para o comércio eletrônico.

_Solicitar por SKU_ é um [widget](../content-design/widgets.md) que pode ser exibido na loja como uma conveniência para todos os compradores, ou disponibilizado apenas aos compradores em grupos de clientes específicos. Os compradores podem inserir as informações de SKU e quantidade diretamente no bloco Pedido por SKU ou carregar um arquivo csv da conta do cliente. Independentemente da configuração, pedir por SKU está sempre disponível para administradores de armazenamento.

![Pedir por SKU na vitrine](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## Configurar pedido por SKU

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda a **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Order by SKU Settings]** seção.

1. Definir **[!UICONTROL Enable Order by SKU on my Account in Storefront]** a um dos seguintes:

   - `Yes, for Everyone` - O bloco Ordenar por SKU está disponível na loja para cada comprador.
   - `Yes, for Specified Customer Groups` - Pedido por SKU está disponível somente para membros de um grupo de clientes específico, como `Wholesale`.
   - `No` - O bloco Ordenar por SKU não é exibido na vitrine e a página Ordenar por SKU não está disponível na conta do cliente.

   ![Ordenar por configurações de SKU](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.

![Adobe Commerce B2B](../assets/b2b.svg) (somente Adobe Commerce B2B) _**Para ativar a função Ordenar por SKU, desative a função Ordem Rápida:**_

1. Ir para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL B2B Features]**

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL B2B Features]** seção.

1. Definir **[!UICONTROL Enable Quick Order]** para `No`.

   A variável [Recurso de pedido rápido](../b2b/quick-order.md) O permite que clientes e convidados façam pedidos rapidamente com base no SKU ou no nome do produto.

## Experiência da vitrine

Quando a funcionalidade é configurada para a loja, os clientes podem fazer pedidos por SKU de qualquer página que inclua a _Solicitar por SKU_ ou no painel da conta.

### Ordenar por SKU do bloco de páginas

1. No _Solicitar por SKU_ bloco, o cliente informa o **[!UICONTROL SKU]** e **[!UICONTROL Qty]** do item a ser solicitado.

1. Para adicionar outro item, clique em **[!UICONTROL Add Row]** e repita o processo.

1. Cliques **[!UICONTROL Add to Cart]**.

### Solicitar por SKU de uma conta de cliente

1. Na loja, o cliente faz logon em sua conta.

1. No painel à esquerda, escolhe **[!UICONTROL Order by SKU]**.

1. Adiciona itens individuais de acordo com a preferência:

   _**Adiciona cada item por SKU:**_

   - Insere o **[!UICONTROL SKU]** e **[!UICONTROL Qty]** do item a ser solicitado.

   - Para adicionar outros itens, conforme necessário, clique em _Adicionar linha_ ![Botão de sinal de mais](../assets/button-add-item.png) O e o repetem para quantos itens forem necessários.

   - Cliques **[!UICONTROL Add to Cart]**.

   _**Carrega um arquivo CSV de vários itens:**_

   - Prepara um [importar CSV de dados](../systems/data-csv.md) (Valor separado por vírgula) arquivo que inclui colunas para `SKU` e `Qty`.

   ![SKUs a importar](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - Para fazer upload do arquivo CSV, clique em **[!UICONTROL Choose File]** e selecione o arquivo a ser carregado.

   - Cliques **[!UICONTROL Add to Cart]**.

   Se qualquer um dos produtos tiver opções adicionais, o cliente será avisado no carrinho de compras que o produto requer atenção.

   ![O produto requer atenção](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se houver SKUs duplicadas, as quantidades serão combinadas em um item de linha no carrinho de compras. O cliente pode alterar a quantidade de qualquer item e clicar em **[!UICONTROL Update Shopping Cart]** para recalcular os totais.

