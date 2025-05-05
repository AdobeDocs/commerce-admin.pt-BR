---
title: Instalar, atualizar e remover [!DNL Inventory Management]
description: Saiba como gerenciar o  [!DNL Inventory Management] metapackage.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Instalar, atualizar e remover [!DNL Inventory Management]

Os módulos do [!DNL Inventory Management] fornecem todos os recursos e opções de estoque para comerciantes de origem única e múltipla para gerenciar quantidades de produtos e estoque para canais de vendas. Esses recursos estão disponíveis nas versões 2.4.x do Adobe Commerce e do Magento Open Source.

Esses recursos e extensões foram desenvolvidos como parte do [Projeto de inventário](https://github.com/magento/inventory) por meio do programa de engenharia da comunidade da Magento Open Source.

O [!DNL Inventory Management] é instalado nas versões 2.3.x e 2.4.x do Adobe Commerce e do Magento Open Source, com todos os recursos habilitados por padrão. Não são necessárias etapas adicionais para habilitar esses recursos de inventário. As atualizações da versão 2.1.x ou 2.2.x podem exigir etapas adicionais. Consulte [Atualizar Inventory management](#upgrade-inventory-management).

É recomendável a instalação de acordo com a [Instalação rápida local](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=pt-BR){target="_blank"}. Instale com um metapackage para receber todos os [!DNL Inventory Management] módulos.

A seguinte linha no metapackage `composer.json` instala [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Para obter uma lista de [!DNL Inventory Management] versões do metapackage, consulte as [notas de versão](release-notes.md).

O processo de instalação do [!DNL Inventory Management] adiciona todos os módulos ao arquivo `<Magento_installation_directory>/app/etc/config.php`. Um valor `1` indica que o módulo correspondente está habilitado. É adicionada a seguinte lista de módulos:

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## Habilitar recursos do [!DNL Inventory Management]

Quando instalada, atualizada ou atualizada, a opção _[!UICONTROL Manage Stock]_&#x200B;no Administrador é habilitada por padrão. Esta opção habilita o controle e o gerenciamento de inventário, mas não afeta o status do módulo. Para desativar módulos, consulte a próxima seção.

Para obter mais informações sobre configurações, consulte [Configurar Inventory management](configuration.md).

## Desativar Inventory management

>[!IMPORTANT]
>
>É altamente recomendado usar os módulos [!DNL Inventory Management] padrão. O módulo [!DNL CatalogInventory] alternativo, que é usado para sistemas com [!DNL Inventory Management] módulos desabilitados, agora está obsoleto. Desabilitar os módulos [!DNL Inventory Management] pode causar instabilidade no sistema e resultar em vários problemas.

Talvez você queira desabilitar [!DNL Inventory Management] módulos para:

* Acelere o processo de upgrade para comerciantes que migram do 2.0.x, 2.1.x, 2.2.x ou 2.3.x para o 2.4.x.
* Use módulos de sistema de gerenciamento de pedidos e inventário personalizados ou de terceiros.

Consulte a página [Habilitar ou desabilitar módulos](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=pt-BR) no _Guia de Instalação_ para obter informações sobre como desabilitar os módulos aplicáveis.

Quando concluído, o sistema fornece uma lista de módulos e valores em `<Magento_installation_directory>/app/etc/config.php`, começando com:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Se você tiver os módulos do Conector OMS instalados, certifique-se de não desabilitar o módulo `Magento_InventoryMessageBus`, que é um módulo de Conector. É necessário usar o Conector com OMS.

## Remover Inventory management

>[!IMPORTANT]
>
>É altamente recomendado usar os módulos [!DNL Inventory Management] padrão. O módulo [!DNL CatalogInventory] alternativo, que é usado para sistemas com [!DNL Inventory Management] módulos removidos, agora está obsoleto. A remoção dos módulos [!DNL Inventory Management] pode causar instabilidade no sistema e resultar em vários problemas.

Se você optar por não usar a funcionalidade [!DNL Inventory Management], poderá remover (desinstalar) esses módulos. Para remover todos os módulos por meio do arquivo compositor, adicione o seguinte a `composer.json`:

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

Quando essa alteração for concluída, execute a instalação do composer e ele removerá automaticamente esses módulos do Inventory management.

## Atualizar o Inventory management

### Versões [!DNL Commerce] anteriores

Ao atualizar ou atualizar uma instalação existente do 2.1.x, 2.2.x ou 2.3.x para o Adobe Commerce ou Magento Open Source 2.4.x, os módulos do [!DNL Inventory Management] são desabilitados por padrão. Essa configuração padrão é uma precaução para evitar atualizações incompatíveis com versões anteriores e oferecer melhor suporte ao Order Management (OMS).

>[!NOTE]
>
>O Order Management não oferece suporte a [!DNL Inventory Management]. Durante a atualização, os módulos do [!DNL Inventory Management] são desabilitados para permitir que o OMS e o [!DNL Commerce] 2.3.x funcionem perfeitamente.


Para habilitar [!DNL Inventory Management] módulos:

1. Edite o arquivo `<Commerce_installation_directory>/app/etc/config.php`.
1. Modifique todos os módulos de inventário de `0` para `1` para habilitar.
1. Atualize o banco de dados:

   ```bash
   bin/magento setup:upgrade
   ```

1. Limpe o cache:

   ```bash
   bin/magento cache:clean
   ```

É recomendável usar os [comandos de inconsistência de reserva](cli.md) após a atualização. Ao atualizar, todos os seus produtos são adicionados ao Estoque padrão. Se você tiver ordens pendentes, os comandos atualizarão corretamente a quantidade e as reservas para vendas e atendimento de ordens.

### Versões [!DNL Inventory Management] anteriores

Ao atualizar de versões anteriores do [!DNL Inventory Management] para a versão mais recente, siga as etapas normais de atualização de extensão.

Para obter a versão mais recente, atualize a versão do metapackage:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Consulte os guias a seguir para obter mais informações sobre atualizações do Commerce:

* [Guia de Atualização do Commerce](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html?lang=pt-BR){target="_blank"}
* [Habilitar ou desabilitar módulos](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=pt-BR){target="_blank"}
