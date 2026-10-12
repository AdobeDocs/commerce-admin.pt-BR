---
title: Tipos de produto
description: Saiba como o [!DNL Inventory Management] oferece suporte ao gerenciamento de estoque e pedidos para todos os tipos de produtos Adobe Commerce e Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%
---
# Tipos de produto

O [!DNL Inventory Management] oferece suporte ao gerenciamento de estoque e pedido para todos os tipos de produtos na Adobe Commerce e Magento Open Source: simples, configurável, virtual, baixável, agrupada e agrupada. As opções e os requisitos podem diferir de acordo com o tipo de produto para origens, estoques e remessa.

- [Comerciantes de origem única](merchant-sourcing.md#single-source-merchants) criam e atualizam configurações e quantidades de produtos sem exigir atualizações adicionais. Todos os produtos criados e recém-importados são automaticamente atribuídos ao Source padrão e ao Estoque padrão, imediatamente disponíveis aos clientes se ativados e no Estoque.

- [Comerciantes de várias origens](merchant-sourcing.md#multi-source-merchants) atribuem origens, quantidades por origem e configurações durante ou após a criação do produto. O [!DNL Commerce] atribui todos os produtos recém-importados à Source Padrão, exigindo edições adicionais para atribuir origens e quantidades.

| Tipo de produto | Algoritmo de seleção de envio e Source |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Oferece suporte a recomendações e substituições de SSA no envio. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Oferece suporte a recomendações e substituições de SSA no envio. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Sempre usa a recomendação do SSA. O sistema executa o algoritmo implicitamente ao criar NFFs e sempre usa os resultados sugeridos.<br/>Não é possível ajustar esses resultados. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Sempre usa a recomendação do SSA. O sistema executa o algoritmo implicitamente ao criar NFFs e sempre usa os resultados sugeridos. <br/>Não é possível ajustar esses resultados. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Oferece suporte a recomendações e substituições de SSA no envio. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Oferece suporte a recomendações e substituições de SSA no envio. |
