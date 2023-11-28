---
title: "Instalar, atualizar e remover [!DNL Inventory Management]"
description: Saiba como gerenciar o [!DNL Inventory Management] metapackage.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
source-git-commit: d6c81da4b4e0674d6699e9781921ccb2160b9983
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Instalar, atualizar e remover [!DNL Inventory Management]

[!DNL Inventory Management] Os módulos do fornecem todos os recursos e opções de inventário para comerciantes de origem única e múltipla para gerenciar quantidades de produtos e estoque para canais de vendas. Esses recursos estão disponíveis nas versões 2.4.x do Adobe Commerce e Magento Open Source.

Esses recursos e extensões foram desenvolvidos como parte da [Projeto de estoque](https://github.com/magento/inventory) através do programa de engenharia da comunidade Magento Open Source.

[!DNL Inventory Management] O é instalado nas versões 2.3.x e 2.4.x do Adobe Commerce e Magento Open Source, com todos os recursos ativados por padrão. Não são necessárias etapas adicionais para habilitar esses recursos de inventário. As atualizações da versão 2.1.x ou 2.2.x podem exigir etapas adicionais. Consulte [Atualizar o Inventory management](#upgrade-inventory-management).

Instalação de acordo [Instalação de início rápido local](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} é recomendada. Instale o com um metapackage para receber tudo [!DNL Inventory Management] módulos.

A seguinte linha no campo `composer.json` instalações do metapackage [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Para obter uma lista de [!DNL Inventory Management] versões de metapackage, consulte a seção [notas de versão](release-notes.md).

A variável [!DNL Inventory Management] processo de instalação adiciona todos os módulos à `<Magento_installation_directory>/app/etc/config.php` arquivo. A `1` indica que o módulo correspondente está ativado. É adicionada a seguinte lista de módulos:

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

## Ativar [!DNL Inventory Management] recursos

Quando instalado, atualizado ou atualizado, o _[!UICONTROL Manage Stock]_A opção é ativada por padrão no Admin. Esta opção habilita o controle e o gerenciamento de inventário, mas não afeta o status do módulo. Para desativar módulos, consulte a próxima seção.

Para obter mais informações sobre configurações, consulte [Configurar Inventory management](configuration.md).

## Desativar Inventory management

>[!IMPORTANT]
>
>Uso do padrão [!DNL Inventory Management] é altamente recomendado. A alternativa [!DNL CatalogInventory] o módulo, que é usado para sistemas com [!DNL Inventory Management] módulos, agora está obsoleto. Desativar o [!DNL Inventory Management] módulos podem causar instabilidade no sistema e resultar em vários problemas.

Talvez você queira desativar [!DNL Inventory Management] módulos para:

* Acelere o processo de upgrade para comerciantes que migram do 2.0.x, 2.1.x, 2.2.x ou 2.3.x para o 2.4.x.
* Use módulos de sistema de gerenciamento de pedidos e inventário personalizados ou de terceiros.

Consulte a [Ativar ou desativar módulos](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) página no _Guia de instalação_ para obter informações sobre como desativar os módulos aplicáveis.

Quando concluído, o sistema fornece uma lista de módulos e valores em `<Magento_installation_directory>/app/etc/config.php`, começando com:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Se você tiver os módulos do Conector OMS instalados, certifique-se de não desativar o `Magento_InventoryMessageBus` que é um módulo de Conector. É necessário usar o Conector com OMS.

## Remover Inventory management

>[!IMPORTANT]
>
>Uso do padrão [!DNL Inventory Management] é altamente recomendado. A alternativa [!DNL CatalogInventory] que é usado para sistemas com [!DNL Inventory Management] módulos, agora está obsoleto. Remover o [!DNL Inventory Management] módulos podem causar instabilidade no sistema e resultar em vários problemas.

Se você optar por não usar o [!DNL Inventory Management] você pode remover (desinstalar) esses módulos. Para remover todos os módulos através do arquivo compositor, adicione o seguinte a `composer.json`:

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

### Anterior [!DNL Commerce] versões

Ao atualizar ou atualizar uma instalação existente do 2.1.x, 2.2.x ou 2.3.x para o Adobe Commerce ou o Magento Open Source 2.4.x, [!DNL Inventory Management] Os módulos do são desativados por padrão. Essa configuração padrão é uma precaução para evitar atualizações incompatíveis com versões anteriores e oferecer melhor suporte ao Order Management (OMS).

>[!NOTE]
>
>O Order Management não suporta [!DNL Inventory Management]. Ao atualizar, [!DNL Inventory Management] Os módulos do estão desativados para permitir OMS e [!DNL Commerce] 2.3.x para funcionar perfeitamente.


Para habilitar [!DNL Inventory Management] módulos:

1. Edite o `<Commerce_installation_directory>/app/etc/config.php` arquivo.
1. Modificar todos os módulos de inventário de `0` para `1` para ativar.
1. Atualize o banco de dados:

   ```bash
   bin/magento setup:upgrade
   ```

1. Limpe o cache:

   ```bash
   bin/magento cache:clean
   ```

É recomendável que você use o [comandos de inconsistências de reserva](cli.md) após a atualização. Ao atualizar, todos os seus produtos são adicionados ao Estoque padrão. Se você tiver ordens pendentes, os comandos atualizarão corretamente a quantidade e as reservas para vendas e atendimento de ordens.

### Anterior [!DNL Inventory Management] versões

Ao atualizar de versões anteriores do [!DNL Inventory Management] para obter a versão mais recente, siga as etapas normais de atualização de extensão.

Para obter a versão mais recente, atualize a versão do metapackage:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Consulte os guias a seguir para obter mais informações sobre atualizações do Commerce:

* [Guia de atualização do Commerce](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [Ativar ou desativar módulos](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
