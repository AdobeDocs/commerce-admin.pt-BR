---
title: Menu [!UICONTROL Stores]
description: O Administrador do Commerce inclui o menu [!UICONTROL Stores], que fornece acesso às ferramentas para configurar a hierarquia da loja, a configuração, o inventário, os impostos e os atributos.
exl-id: b9d8ea6b-5b4b-42af-b74d-7afa48ccf2ff
TQID: https://experienceleague.adobe.com/LEoQUYqvin2UfF55kCMUiEUh8YungghN-VuEwUOu7gY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%
---
# Menu [!UICONTROL Stores]

O menu _[!UICONTROL Stores]_&#x200B;fornece acesso a configurações usadas com menos frequência, mas referenciadas durante a instalação do Adobe Commerce ou do Magento Open Source. Essas funções incluem a definição da hierarquia da loja, a configuração, as configurações de vendas e pedidos, os impostos e a moeda, os atributos do produto, as classificações de revisão do produto e os grupos de clientes.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

![Administrador - Menu Lojas](./assets/stores-menu.png){width="500" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE Somente SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplicável somente a projetos do Adobe Commerce as a Cloud Service e do Adobe Commerce Optimizer (infraestrutura SaaS gerenciada pela Adobe)."}

![Administrador - Menu Lojas](./assets/stores-menu-accs.png){width="500" zoomable="yes"}

>[!ENDTABS]

## Exibir o menu [!UICONTROL Stores]

Na barra lateral _Admin_, clique em **[!UICONTROL Stores]**.

## Seções principais

### [!UICONTROL Settings]

Gerencie a hierarquia de [sites, lojas e exibições de loja](stores.md#store-and-site-structure) na sua instalação do Adobe Commerce ou do Magento Open Source e em todas as [configurações](../configuration-reference/guide-overview.md). Além disso, você pode configurar os [Termos e Condições](terms-and-conditions.md) de uma venda e gerenciar as [configurações de status do pedido](order-status.md#custom-order-status).

### [!UICONTROL Inventory]

[Gerencie e crie estoques](../inventory-management/introduction.md) para vincular seus canais ou sites de vendas a [fontes](../inventory-management/sources-manage.md). As existências representam uma quantidade de produtos comercializável agregada. Comerciantes individuais da Source usam o Estoque padrão, enquanto Comerciantes de vários Source usam estoques personalizados adicionais.

### [!UICONTROL Taxes]

Gerencie todos os tipos de [funções de imposto](taxes.md) em sua loja, configure as regras de imposto para sua loja, defina classes de imposto de cliente e produto e gerencie zonas de imposto e alíquotas. Você também pode importar dados de alíquota do imposto para sua loja.

### [!UICONTROL Currency]

Gerencie as taxas para as [moedas](currency.md) aceitas como pagamento em sua loja e personalize os símbolos de moeda que aparecem nos preços dos produtos e nos documentos de venda.

### [!UICONTROL Attributes]

Gerenciar atributos usados para [informações do cliente](../customers/attribute-properties.md) ou [informações do produto](../catalog/attribute-product-create.md), devoluções e classificações do produto. Você pode criar atributos, editar atributos existentes e gerenciar [conjuntos de atributos](../catalog/attribute-sets.md).

### [!UICONTROL Other Settings]

Gerencie configurações adicionais para [taxas de câmbio de premiação](../merchandising-promotions/reward-exchange-rates.md), [invólucro de presentes](cart-configuration.md#gift-wrap) e [registros de presentes](../merchandising-promotions/gift-registries.md).

## Integração do [!DNL Adobe Commerce Optimizer]

Quando o [!DNL Adobe Commerce Optimizer Connector] estiver instalado, você poderá sincronizar o site e armazenar dados de exibição para [!DNL Adobe Commerce Optimizer]. Controles de escopo de site [sincronização de preços](stores.md#step-1-create-a-website) (preços e catálogos de preços). Controles de escopo de exibição de armazenamento [sincronização de produto](store-views.md#add-a-store-view) (produtos e atributos de produto).

Para obter os indicadores de status de sincronização mostrados na grade [!UICONTROL All Stores], consulte [status de sincronização do Adobe Commerce Optimizer](store-views.md#optimizer-sync-status). Para conhecer os comportamentos de instalação e configuração do conector, consulte [Personalizar a configuração de exportação de escopos do Commerce](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/get-started#customize-the-commerce-scopes-export-configuration) no *Guia do Adobe Commerce Optimizer Connector*.

Se o [!DNL Adobe Commerce Optimizer Connector for B2B] estiver instalado, os dados também serão sincronizados para os catálogos compartilhados B2B disponíveis. Consulte [Gerenciar exibições do catálogo](../b2b/catalog-views-manage.md).
