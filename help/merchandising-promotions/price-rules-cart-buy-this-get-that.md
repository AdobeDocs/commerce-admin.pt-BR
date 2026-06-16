---
title: Exemplo de regra de preço do carrinho - compre este e obtenha
description: Analise um exemplo de uso de uma regra de preço do carrinho para oferecer uma promoção comprar-este-obter-aquilo.
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/hhsxk4QXpulYqJrCBdXNQ9RZireHGb85lCwq8ns38l4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 613
ht-degree: 0%

---

# Exemplo de regra de preço do carrinho - compre este e obtenha

Este exemplo mostra como configurar uma [regra de preço do carrinho](price-rules-cart.md) para uma _Comprar isto, obter a promoção_ gratuita. O formato do desconto é o seguinte:

_Comprar X quantidade de produto, obter Y quantidade gratuitamente_

## Etapa 1. Criar uma regra de preço de carrinho

Conclua a [Etapa 1](price-rules-cart.md) das instruções de regra de preço do carrinho para concluir as informações da regra.

## Etapa 2. Definir as condições

Conclua a [Etapa 2](price-rules-cart.md) das instruções do carrinho para definir as condições da regra de preço. Essa é a primeira das duas condições que podem ser adicionadas à regra e determina quando a regra é acionada. Ela pode ser baseada em uma combinação dos seguintes:

- Atributos do produto
- Produtos
- Atributos do carrinho
- ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Segmentos de clientes

Se deixado em branco, a regra será acionada para cada carrinho.

![Regra de preço do carrinho - condição](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Etapa 3. Definir as ações

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Actions]** e faça o seguinte:

   - Defina **[!UICONTROL Apply]** como `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - Defina **[!UICONTROL Discount Amount]** como `1`. Essa é a quantidade que o cliente recebe gratuitamente.

   - Para limitar o número de descontos que podem ser aplicados quando a condição é atendida, insira o número no campo **[!UICONTROL Maximum Qty Discount is Applied To]**. Isso é calculado usando esta [fórmula](#maximum-quantity-discount).

   - Para **[!UICONTROL Discount Qty Step (Buy X)]**, insira a quantidade que o cliente deve comprar para se qualificar para o desconto. Neste exemplo, o cliente deve comprar três.

   - Se quiser impedir que outros descontos sejam aplicados à compra, defina **[!UICONTROL Discard subsequent rules]** como `Yes`.

   ![Regra de preço do carrinho - compre 3 e ganhe 1 grátis](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Para aplicar a regra somente a itens específicos no carrinho, preencha a condição para descrever os itens do carrinho e/ou os atributos do produto necessários para a promoção.

   O exemplo a seguir usa o SKU para aplicar a regra a todas as variações associadas de um produto configurável.

   ![Regra de preço do carrinho - condição para itens de carrinho](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. Para incluir **[!UICONTROL Free Shipping]**, escolha `For matching items only`.

1. Clique em **[!UICONTROL Save and Continue Edit]** e conclua o restante da regra conforme necessário.

## Etapa 4. Preencha o rótulo

Conclua a [Etapa 4](price-rules-cart.md) das instruções de regra de preço do carrinho para inserir o rótulo que aparece durante o check-out.

## Etapa 5: salvar e testar a regra

{{new-price-rule}}

1. Quando a regra estiver concluída, clique em **[!UICONTROL Save Rule]**.

1. Teste a regra para verificar se ela funciona corretamente.

## Variações

Comprar X Obter Y Gratuito é processado como uma única ação, com uma dependência de _total de linhas_. Todos os itens devem ser do mesmo SKU para se qualificarem para a promoção. Por exemplo:

Compre X quantidade de produto da categoria A, obtenha Y quantidade do mesmo produto gratuitamente.

Para limitar o produto livre às categorias A, B e C, defina a ação da seguinte maneira:

Se TODAS essas condições forem VERDADEIRAS:
A categoria é uma de A, B, C

Para limitar os itens livres de qualquer categoria (A, B ou C) e receber Y dos SKUs (D123, E123 ou F123), defina a ação da seguinte maneira:

Se TODAS essas condições forem VERDADEIRAS:
SKU é um dos modelos D123, E123, F123

## Desconto de quantidade máxima

Use a fórmula a seguir para determinar o valor correto para o Desconto da Qtde Máxima:

Fórmula = `(X+Y) * (M/Y)`
Onde
`X` = número de itens comprados
`Y` = número de itens livres
`M` = Número máximo de itens livres permitido

Por exemplo:

Compre cinco e ganhe dois gratuitos com um máximo de quatro itens gratuitos permitidos.

    Onde
    X = 5
    Y = 2
    M = 4
    Desconto de Quantidade Máxima = (5+2)*(4/2)=(7)*(2)=14

Compre cinco e ganhe três gratuitamente com um máximo de nove itens gratuitos permitidos.

    Onde
    X = 5
    Y = 3
    M = 9
    Desconto de Quantidade Máxima = (5+3)*(9/3)=24

Compre 20 e ganhe dois grátis com um máximo de 20 itens gratuitos permitidos.

    Onde
    X = 20
    Y = 2
    M = 20
    Desconto de Quantidade Máxima = (20+2)*(20/2)=(22)*(10)=220
