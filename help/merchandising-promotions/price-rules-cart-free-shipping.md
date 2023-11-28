---
title: Exemplo de regra de preço do carrinho - promoção de frete grátis
description: Analise um exemplo de uso de uma regra de preço de carrinho para oferecer frete gratuito.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Exemplo de regra de preço do carrinho - promoção de frete grátis

O frete gratuito pode ser oferecido como uma promoção, com ou sem um [cupom](price-rules-cart-coupon.md). Um cupom de entrega gratuita, ou voucher, também pode ser aplicado a ordens de retirada do cliente, para que a ordem possa ser faturada e entregue para concluir a [fluxo de trabalho](../stores-purchase/order-processing.md#order-workflow-and-processing).

Algumas configurações de transportadoras oferecem a capacidade de oferecer frete grátis com base em um pedido mínimo. Para expandir esse recurso básico, você pode usar as regras de preço do carrinho de compras para criar condições complexas com base em vários atributos de produto, conteúdo do carrinho e grupos de clientes.

## Etapa 1. Ativar frete grátis

1. Ativar [frete grátis](../stores-purchase/shipping-free.md) na configuração da loja.

1. Conclua as configurações de envio gratuito para qualquer [serviço de operadora](../stores-purchase/carriers.md) que você deseja usar para frete grátis.

## Etapa 2. Criar uma regra de preço de carrinho

No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Siga as etapas abaixo para configurar o tipo de promoção de frete gratuito que deseja oferecer.

### Exemplo 1: envio gratuito para qualquer pedido

1. Conclua o **[!UICONTROL Rule Information]** do seguinte modo:

   - Insira um **[!UICONTROL Rule Name]** para referência interna.
   - Insira um resumo **[!UICONTROL Description]** para descrever a regra.
   - Definir **[!UICONTROL Active]** para `Yes`.
   - No **[!UICONTROL Websites]** selecione cada site onde o cupom de frete grátis deve estar disponível.
   - Selecione o **[!UICONTROL Customer Groups]** à qual a regra se aplica.
   - Definir **[!UICONTROL Coupon]** a um dos seguintes:
      - Para oferecer uma promoção de frete gratuito sem um cupom, aceite o padrão (`No Coupon`).
      - Para usar um cupom com a regra de preço, selecione `Specific Coupon`. Se necessário, complete as instruções para configurar um [cupom](price-rules-cart-coupon.md).

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Actions]** e faça o seguinte:

   - Definir **[!UICONTROL Apply]** para `Percent of product price discount`.
   - Definir **[!UICONTROL Apply to Shipping Amount]** para `Yes`.
   - Definir **[!UICONTROL Free Shipping]** para `For matching items only`.

   ![Regra de preço do carrinho - ações de remessa gratuita](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Exemplo 2: envio gratuito para pedidos acima do valor de $

1. Conclua o **[!UICONTROL General Information]** conforme descrito no exemplo anterior.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Conditions]** seção.

1. Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) para inserir uma condição e faça o seguinte:

   - Na lista abaixo **[!UICONTROL Cart Attribute]**, escolha `Subtotal`.
   - Clique em **[!UICONTROL is]** e escolha `equals or greater than`.
   - Clique em **..** e insira um valor de limite para o Subtotal, como `100`, para completar a condição.

   ![Regra de preço do carrinho - condição](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Se necessário, expanda ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Actions]** e faça o seguinte:

   - Definir **[!UICONTROL Apply]** para `Percent of product price discount`.
   - Definir **[!UICONTROL Apply to Shipping Amount]** para `Yes`.
   - Definir **[!UICONTROL Free Shipping]** para `For matching items only`.

## Etapa 3. Preencha os rótulos

Concluído [Etapa 4](price-rules-cart.md) das instruções de regra de preço do carrinho para inserir quaisquer rótulos que apareçam durante a finalização da compra.

## Etapa 4. Salvar e testar a regra

{{new-price-rule}}

1. Quando a regra for concluída, clique em **[!UICONTROL Save Rule]**.

1. Teste a regra para verificar se ela funciona corretamente.
