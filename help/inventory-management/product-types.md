---
title: Tipos de produto
description: Saiba como [!DNL Inventory Management] O oferece suporte ao gerenciamento de inventário e pedido para todos os tipos de produtos Adobe Commerce e Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Tipos de produto

[!DNL Inventory Management] O oferece suporte ao gerenciamento de inventário e pedido para todos os tipos de produtos no Adobe Commerce e no Magento Open Source: simples, configurável, virtual, baixável, pacote e agrupado. As opções e os requisitos podem diferir de acordo com o tipo de produto para origens, estoques e remessa.

- [Comerciantes de origem única](merchant-sourcing.md#single-source-merchants) criar e atualizar configurações e quantidades de produto sem exigir atualizações adicionais. Todos os produtos criados e recém-importados são automaticamente atribuídos à Origem padrão e ao Estoque padrão, imediatamente disponíveis aos clientes se ativados e no Estoque.

- [Comerciantes de várias origens](merchant-sourcing.md#multi-source-merchants) atribuir origens, quantidades por origem e configurações durante ou após a criação do produto. [!DNL Commerce] atribui todos os produtos importados recentemente à Origem Padrão, exigindo edições adicionais para atribuir origens e quantidades.

| Tipo de produto | Algoritmo de Seleção de Origem e Entrega |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Oferece suporte a recomendações e substituições de SSA no envio. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Oferece suporte a recomendações e substituições de SSA no envio. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Sempre usa a recomendação do SSA. O sistema executa o algoritmo implicitamente ao criar NFFs e sempre usa os resultados sugeridos.<br/>Você não pode ajustar esses resultados. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Sempre usa a recomendação do SSA. O sistema executa o algoritmo implicitamente ao criar NFFs e sempre usa os resultados sugeridos. <br/>Você não pode ajustar esses resultados. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Oferece suporte a recomendações e substituições de SSA no envio. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Oferece suporte a recomendações e substituições de SSA no envio. |
