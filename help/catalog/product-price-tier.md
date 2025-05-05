---
title: Nível de preços
description: Saiba como usar o preço de camada para oferecer um desconto por quantidade de uma lista de produtos ou página de produtos.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Nível de preços

Os preços de nível permitem oferecer um desconto por quantidade de uma lista de produtos ou página de produtos na loja. O desconto pode ser aplicado a uma exibição de loja específica, grupo de clientes ou catálogo compartilhado.

Se você tem muitos produtos para atualizar, é mais eficiente importar as alterações de preço de nível, em vez de inseri-las individualmente. Para obter mais informações, consulte [Importar preços de camada](../systems/data-import-price-tier.md).

![Preço de camada em uma página de produto da loja](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

A página do produto calcula o desconto por quantidade e exibe uma mensagem como:

`Buy 6 for $5.95 each and save 15%`

Os preços na loja têm prioridade da quantidade mais alta para a mais baixa. Se você tiver um preço de camada para a quantidade `5` e um para `10` e um cliente adicionar cinco, seis, sete, oito ou nove itens ao carrinho de compras, o cliente receberá o preço com desconto para a camada de quantidade `5`. Quando o cliente adiciona o décimo item, o preço com desconto especificado para a camada de quantidade `10` substitui a camada para uma quantidade de `5` e o preço com desconto para `10` se aplica.

## Adicionar uma camada de preços para um produto

1. Abra o produto no modo de edição.

1. Abaixo do campo _[!UICONTROL Price]_, clique em **[!UICONTROL Advanced Pricing]**.

1. Na seção _[!UICONTROL Tier Price]_, clique em **[!UICONTROL Add]**.

   Se você estiver criando um nível de vários preços, clique em **[!UICONTROL Add]** para cada nível adicional, para que você possa trabalhar todos os níveis ao mesmo tempo. Cada camada no grupo tem o mesmo site e grupo de clientes ou atribuição de catálogo compartilhado, mas uma quantidade e preço diferentes.

## Configurar a camada de preços

1. Se sua loja tiver vários sites, escolha o **[!UICONTROL Website]** ao qual se aplica o preço de camada.

1. Se necessário, limite a disponibilidade da camada de preços selecionando o **[!UICONTROL Customer Group]** ou **[!UICONTROL Shared Catalog]** (![Adobe Commerce B2B](../assets/b2b.svg) Disponível somente com [Adobe Commerce B2B](./b2b/../introduction.md)).

1. Para **[!UICONTROL Qty]**, insira a quantidade que deve ser solicitada para receber o desconto.

   - **Método 1:** Inserir preço como valor fixo

     Defina **[!UICONTROL Price]** como `Fixed` e insira o preço ajustado para uma unidade nessa camada.

     ![Classificar preço como valor fixo](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Método 2:** Inserir preço como uma porcentagem

     Defina **[!UICONTROL Price]** como `Discount` e insira o preço com desconto como uma porcentagem do preço base do produto.

     Por exemplo, para um desconto de 15%, insira o número `15`. (O preço é salvo com duas casas decimais, como `15.00`.)

     >[!NOTE]
     >
     >Para obter o preço com desconto, a porcentagem definida é calculada em relação ao valor definido no campo _[!UICONTROL Price]_, não no campo&#x200B;_[!UICONTROL Special Price]_.

     ![Preço da camada como uma porcentagem](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Concluir a configuração de preço

1. Para adicionar outro conjunto de preços de camada para um site ou grupo de clientes diferente, repita as etapas anteriores.

1. Quando terminar, clique em **[!UICONTROL Done]** e depois em **[!UICONTROL Save]**.

>[!NOTE]
>
>O preço do produto **_final_** é calculado como o preço relevante de **_mínimo_**, usando a seguinte fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Preço Fixo_** O produto de Opções Personalizáveis _não_ é afetado pelas regras de Preço de Grupo, Preço de Camada, Preço Especial ou Preço de Catálogo.
