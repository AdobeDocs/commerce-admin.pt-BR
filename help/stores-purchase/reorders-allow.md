---
title: Permitir reordenações
description: Saiba como fornecer recursos de reposição para seus clientes.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
TQID: https://experienceleague.adobe.com/comSKludWZnDkDjdZyhi4-9WNAE9scH3dgSce08IyJo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 432
ht-degree: 0%

---

# Permitir reordenações

Quando habilitados, os reordenamentos podem ser feitos diretamente da conta do cliente ou do pedido original no _Administrador_. As reordenações são ativadas por padrão.

![Link de reordenação do cliente no Administrador](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Critérios para a reordenação ser ativada para um pedido

- A opção de configuração _Permitir Reordenação_ deve estar habilitada.

- Se a ordem estiver no status `Hold` ou `Payment Review`, a opção de reordenação estará desabilitada.

- Se qualquer um dos itens no pedido estiver indisponível, esgotado ou desativado, a opção de reordenação está desativada na loja.

- Um _Administrador_ pode reordenar mesmo se algum dos itens estiver indisponível ou desabilitado.

## Configurar para permitir reordenações do cliente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales]** abaixo de.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Reorder]**.

   ![Opções de reordenação](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Allow Reorder]** como `Yes`.

   Essa configuração habilita a funcionalidade de reordenação da conta do cliente na vitrine ou na lista de pedidos do Administrador.

1. Clique em **[!UICONTROL Save Config]**.

## Reordenar da loja

Um cliente pode iniciar a funcionalidade de reordenação para um pedido específico a partir de duas páginas:

- Página _Meus Pedidos_

- Página _Exibição do pedido_

### Meus Pedidos

O botão _Reordenar_ é sempre exibido na lista com Pedidos (mesmo se todos os produtos do pedido não estiverem disponíveis para reordenação).

![Exemplo de vitrine - Página Meus Pedidos](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Caso 1.** Todos os produtos do pedido estão **disponíveis** para reordenação

O usuário é redirecionado para o carrinho e todos os produtos são adicionados a ele

![Carrinho de compras](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Caso 2.** Alguns/todos os produtos do pedido **não estão disponíveis** para reordenação

>[!NOTE]
>
>É possível reordenar `Not Visible Individually` produtos.

O botão _Reordenar_ não aparece nas páginas _Meus Pedidos_ e _Exibir Pedido_.

![Página Meus Pedidos 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Página de exibição de pedidos

**Caso 1.** Todos os produtos do pedido estão disponíveis para reordenação

O usuário é redirecionado para o carrinho e todos os produtos são adicionados a ele

**Caso 2.** Alguns/todos os produtos do pedido **não estão disponíveis** para reordenação

>[!NOTE]
>
>É possível reordenar `Not Visible Individually` produtos.

O botão _Reordenar_ não aparece nas páginas _Meus Pedidos_ e _Exibir Pedido_.

![Página de detalhes do pedido](./assets/order-view-page.png){width="700" zoomable="yes"}

### O carrinho não está vazio

Se o carrinho não estiver vazio e o usuário clicar em **[!UICONTROL Reorder]** (na página _Meus pedidos_ ou _Visualização do pedido_), os produtos existentes permanecerão no carrinho com os produtos de reordenação adicionados.

![Reordenar itens](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Reordenar do administrador

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Localize a ordem e abra no modo **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Reorder]**, que é exibido na barra de botões superior.

   ![Detalhes do pedido no Administrador](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Depois de clicar em **[!UICONTROL Reorder]**, a página _Criar novo pedido_ será aberta com a reorganização de produtos.

   ![Criar reordenação](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Preencha todos os campos obrigatórios conforme necessário.

1. Para enviar o pedido, clique em **[!UICONTROL Submit Order]**.
