---
title: Escopo de preço
description: Saiba mais sobre o escopo usado para preços de produtos, que pode ser configurado para ser aplicado no nível global ou do site.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/4tNRviXPzBubIpyAn9vgUs8BaILjJ6BEdV4yj5ngz6Y
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 0%

---

# Escopo de preço

O escopo da [moeda base](../stores-purchase/currency-configuration.md) usada para os preços dos produtos pode ser configurado para ser aplicado no nível global ou do site. Se aplicado ao nível global, o mesmo preço é usado em toda a hierarquia da loja. Se aplicado ao nível do site, o mesmo produto pode estar disponível a preços diferentes de lojas associadas a sites diferentes. Por padrão, o escopo dos preços do produto é global.

Fatores diferentes podem afetar o preço do mesmo produto em um local e não em outro. Por exemplo, pode haver custos adicionais de distribuição para o produto e outras considerações que afetam o preço dos produtos vendidos em uma loja específica. O diagrama a seguir mostra uma instalação multissite com a moeda base definida no nível do site. As lojas e visualizações de loja associadas a cada site refletem os preços do produto definidos no nível do site.

![Adobe Commerce B2B](../assets/b2b.svg) Se você estiver usando catálogos compartilhados, consulte também [Definir estrutura e preço do catálogo compartilhado](../b2b/catalog-shared-pricing-structure.md) no _Guia B2B do Adobe Commerce_.

![Diagrama de escopo de preço](./assets/catalog-price-scope.svg){width="550"}

## Configurar escopo de preço

1. No menu _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Role para baixo até a seção **[!UICONTROL Price]** e defina **[!UICONTROL Catalog Price Scope]** como um dos seguintes:

   - `Global`
   - `Website`

   A configuração de escopo escolhida aparece abaixo dos campos de preço no catálogo.

   ![Escopo do preço de catálogo](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Usar escopo para configurar preços de produtos

A Commerce não permite a definição de um preço de produto para cada loja. Mas você pode alterar o preço por site:

1. No menu _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Na guia **[!UICONTROL Price]**, defina o escopo de preço como `Website` em vez de `Global`.

1. Defina o preço abrindo a página de edição do produto, selecionando o escopo no canto superior esquerdo e inserindo um novo preço por site.

Em casos raros, quando o escopo de preço está definido como `Global`, o banco de dados do Commerce ainda pode ter preços diferentes no nível do site. Isso pode acontecer como resultado de problemas de sincronização fora do Commerce. Nesses casos, o Comerciante deve realizar uma limpeza de preço no nível da loja e executar uma Sincronização de catálogo com os Serviços da Commerce.