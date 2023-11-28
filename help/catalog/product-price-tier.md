---
title: Nível de preços
description: Saiba como usar o preço de camada para oferecer um desconto por quantidade de uma lista de produtos ou página de produtos.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Nível de preços

Os preços de nível permitem oferecer um desconto por quantidade de uma lista de produtos ou página de produtos na loja. O desconto pode ser aplicado a uma exibição de loja específica, grupo de clientes ou catálogo compartilhado.

Se você tem muitos produtos para atualizar, é mais eficiente importar as alterações de preço de nível, em vez de inseri-las individualmente. Para obter mais informações, consulte [Importar preços de camada](../systems/data-import-price-tier.md).

![Nivelar preço em uma página de produto da loja](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

A página do produto calcula o desconto por quantidade e exibe uma mensagem como:

`Buy 6 for $5.95 each and save 15%`

Os preços na loja têm prioridade da quantidade mais alta para a mais baixa. Se você tiver um preço de camada para a quantidade `5` e um para `10`, e um cliente adicionar cinco, seis, sete, oito ou nove itens ao carrinho de compras, ele receberá o preço com desconto pela quantidade `5` nível. Quando o cliente adiciona o décimo item, o preço com desconto especificado para a quantidade `10` camada substitui a camada para uma quantidade de `5`e preço com desconto para `10` aplicável.

## Adicionar uma camada de preços para um produto

1. Abra o produto no modo de edição.

1. Abaixo do _[!UICONTROL Price]_clique em **[!UICONTROL Advanced Pricing]**.

1. No _[!UICONTROL Tier Price]_clique em **[!UICONTROL Add]**.

   Se estiver criando uma camada de vários preços, clique em **[!UICONTROL Add]** para cada nível adicional, para que você possa trabalhar todos os níveis ao mesmo tempo. Cada camada no grupo tem o mesmo site e grupo de clientes ou atribuição de catálogo compartilhado, mas uma quantidade e preço diferentes.

## Configurar a camada de preços

1. Se sua loja tiver vários sites, escolha a variável **[!UICONTROL Website]** aos quais se aplica a tarifação por níveis.

1. Se necessário, limite a disponibilidade do tipo de preço selecionando o **[!UICONTROL Customer Group]** ou **[!UICONTROL Shared Catalog]** (![B2B para Adobe Commerce](../assets/b2b.svg) Disponível com [B2B para Adobe Commerce](./b2b/../introduction.md) somente).

1. Para **[!UICONTROL Qty]**, insira a quantidade que deve ser solicitada para receber o desconto.

   - **Método 1:** Inserir preço como um valor fixo

     Definir **[!UICONTROL Price]** para `Fixed` e informe o preço ajustado para uma unidade nesse nível.

     ![Classificar Preço como um Valor Fixo](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Método 2:** Inserir preço como uma porcentagem

     Definir **[!UICONTROL Price]** para `Discount` e insira o preço com desconto como uma porcentagem do preço base do produto.

     Por exemplo, para um desconto de 15%, insira o número `15`. (O preço é salvo com duas casas decimais, como `15.00`.)

     >[!NOTE]
     >
     >Para obter o preço com desconto, a porcentagem definida é calculada em relação ao valor definido na variável _[!UICONTROL Price]_ campo, não o _[!UICONTROL Special Price]_ campo.

     ![Preço da camada como uma porcentagem](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Concluir a configuração de preço

1. Para adicionar outro conjunto de preços de camada para um site ou grupo de clientes diferente, repita as etapas anteriores.

1. Quando terminar, clique em **[!UICONTROL Done]** e depois **[!UICONTROL Save]**.

>[!NOTE]
>
>A variável **_final_** o preço do produto é calculado como a **_mínimo_** preço relevante, utilizando a seguinte fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Preço Fixo_** produto As opções personalizáveis são _não_ afetados pelas regras de Preço do Grupo, Preço da Camada, Preço Especial ou Preço do Catálogo.
