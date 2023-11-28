---
title: Escopo de preço
description: Saiba mais sobre o escopo usado para preços de produtos, que pode ser configurado para ser aplicado no nível global ou do site.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Escopo de preço

O âmbito de aplicação do [moeda de base](../stores-purchase/currency-configuration.md) que é usado para os preços do produto podem ser configurados para serem aplicados no nível global ou no nível do site. Se aplicado ao nível global, o mesmo preço é usado em toda a hierarquia da loja. Se aplicado ao nível do site, o mesmo produto pode estar disponível a preços diferentes de lojas associadas a sites diferentes. Por padrão, o escopo dos preços do produto é global.

Fatores diferentes podem afetar o preço do mesmo produto em um local e não em outro. Por exemplo, pode haver custos adicionais de distribuição para o produto e outras considerações que afetam o preço dos produtos vendidos em uma loja específica. O diagrama a seguir mostra uma instalação multissite com a moeda base definida no nível do site. As lojas e visualizações de loja associadas a cada site refletem os preços do produto definidos no nível do site.

![B2B para Adobe Commerce](../assets/b2b.svg) Se estiver usando catálogos compartilhados, consulte também [Definir preço e estrutura do catálogo compartilhado](../b2b/catalog-shared-pricing-structure.md) no _Guia B2B do Adobe Commerce_.

![Diagrama de escopo de preço](./assets/catalog-price-scope.svg){width="550"}

## Configurar escopo de preço

1. No _Admin_ , acesse **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** por baixo.

1. Role para baixo até **[!UICONTROL Price]** seção e definir **[!UICONTROL Catalog Price Scope]** a um dos seguintes:

   - `Global`
   - `Website`

   A configuração de escopo escolhida aparece abaixo dos campos de preço no catálogo.

   ![Escopo do preço de catálogo](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Usar escopo para configurar preços de produtos

O Commerce não permite a definição de um preço de produto para cada loja. Mas você pode alterar o preço por site:

1. No _Admin_ , acesse **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** por baixo.

1. No **[!UICONTROL Price]** , defina o escopo do preço como `Website` em vez de global.

1. Defina o preço abrindo a página de edição do produto, selecionando o escopo no canto superior esquerdo e inserindo um novo preço por site.
