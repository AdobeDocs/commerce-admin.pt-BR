---
title: Configurar atributos inteligentes para o Visual Merchandiser
description: Saiba como configurar os atributos inteligentes usados pelo Visual Merchandiser.
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: 'https://experienceleague.adobe.com/-6tbdpZ7L6nS1sIOXdk5Faxpkkt9qzqWhIjqp9MwgiM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 76cfaac4-e563-56dd-8938-708bf8b84956
    internal-label: Attributes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%
---
# Configurar atributos inteligentes para o Visual Merchandiser

{{ee-feature}}

A configuração do Visual Merchandiser determina os atributos que podem ser usados na janela de merchandising e o limite mínimo de estoque. A configuração também identifica o atributo usado para cor e a ordem dos valores de cor.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Visual Merchandiser]** abaixo de.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL General Options]**.

   ![Configuração do catálogo - visual merchandiser](../configuration-reference/catalog/assets/catalog-visual-merchandiser-general-options.png){width="600" zoomable="yes"}

1. Na lista **[!UICONTROL Attributes for Category Rules]**, selecione cada atributo que você deseja disponibilizar para merchandising visual.

   Para selecionar vários atributos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada item.

1. Digite o **[!UICONTROL Minimum Stock Threshold]** para que um produto seja exibido na janela Visual Merchandiser.

1. Insira o **[!UICONTROL Color Attribute Code]**.

   O valor padrão é `color`. Se o catálogo usar um atributo diferente, insira o nome do atributo em minúsculas.

1. Para **[!UICONTROL Color Order]**, insira cada valor de cor em uma linha separada e em sequência para determinar a prioridade de cada cor.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
