---
title: Permitir reordenações
description: Saiba como fornecer recursos de reposição para seus clientes.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Permitir reordenações

Quando ativadas, as reordens podem ser feitas diretamente da conta do cliente ou do pedido original no _Admin_. As reordenações são ativadas por padrão.

![Link de reordenação do cliente no Administrador](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Critérios para a reordenação ser ativada para um pedido

- A variável _Permitir reordenação_ a opção de configuração deve estar habilitada.

- Se a ordem estiver em `Hold` ou em `Payment Review` , a opção de reordenação estará desativada.

- Se qualquer um dos itens no pedido estiver indisponível, esgotado ou desativado, a opção de reordenação está desativada na loja.

- Um _Admin_ O pode reordenar mesmo se algum dos itens estiver indisponível ou desativado.

## Configurar para permitir reordenações do cliente

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Reorder]** seção.

   ![Opções de reordenação](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Allow Reorder]** para `Yes`.

   Essa configuração habilita a funcionalidade de reordenação da conta do cliente na vitrine ou na lista de pedidos do Administrador.

1. Clique em **[!UICONTROL Save Config]**.

## Reordenar da loja

Um cliente pode iniciar a funcionalidade de reordenação para um pedido específico a partir de duas páginas:

- _Meus Pedidos_ página

- _Visualização do pedido_ página

### Meus Pedidos

A variável _Reordenar_ é sempre exibido na lista com Pedidos (mesmo se todos os produtos do pedido não estiverem disponíveis para reordenação).

![Exemplo de vitrine - página Meus pedidos](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Caso 1.** Todos os produtos do pedido são **disponível** para reordenação

O usuário é redirecionado para o carrinho e todos os produtos são adicionados a ele

![Carrinho de compras](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Caso 2.** Alguns/todos os produtos do pedido são **não disponível** para reordenação

>[!NOTE]
>
>É possível reordenar `Not Visible Individually` produtos.

A variável _Reordenar_ O botão não aparece na guia _Meus Pedidos_ e _Visualizar pedido_ páginas.

![Meus pedidos página 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Página de exibição de pedidos

**Caso 1.** Todos os produtos do pedido estão disponíveis para reordenação

O usuário é redirecionado para o carrinho e todos os produtos são adicionados a ele

**Caso 2.** Alguns/todos os produtos do pedido são **não disponível** para reordenação

>[!NOTE]
>
>É possível reordenar `Not Visible Individually` produtos.

A variável _Reordenar_ O botão não aparece na guia _Meus Pedidos_ e _Visualizar pedido_ páginas.

![Página de detalhes do pedido](./assets/order-view-page.png){width="700" zoomable="yes"}

### O carrinho não está vazio

Se o carrinho não estiver vazio e o usuário clicar em **[!UICONTROL Reorder]** (do _Meus Pedidos_  ou _Visualização do pedido_ ), os produtos existentes permanecerão no carrinho com os produtos de reordenação adicionados.

![Reordenar itens](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Reordenar do administrador

1. No _Admin_ barra lateral, vá para **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Localizar o pedido e abrir em **[!UICONTROL View]** modo.

1. Clique em **[!UICONTROL Reorder]** que é exibido na barra de botões superior.

   ![Detalhes do pedido no Administrador](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Depois de clicar em **[!UICONTROL Reorder]**, o _Criar novo pedido_ será aberta com produtos de reposição.

   ![Criar reordenação](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Preencha todos os campos obrigatórios conforme necessário.

1. Para enviar o pedido, clique em **[!UICONTROL Submit Order]**.
