---
title: Funções do usuário
description: Saiba como criar funções de usuário e as permissões associadas para gerenciar o acesso às funções de Administrador.
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: dff29b7c3a95d4a0ae5ce16819c41a4560b477c4
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Funções do usuário

Para conceder a alguém acesso restrito ao Administrador, a primeira etapa é criar uma função com o nível apropriado de permissões. Depois que a função for salva, você pode adicionar novos usuários e atribuir a função restrita para conceder a eles acesso limitado ao Administrador.

![Administrador - funções de usuário](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## Definir uma função

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Role]**.

1. Conclua as etapas para definir a função:

### Etapa 1: adicionar o nome da função

1. Em _[!UICONTROL Role Information]_, insira um **[!UICONTROL Role Name]**&#x200B;descritivo.

1. Em _[!UICONTROL Current User Identity Verification]_, digite sua senha.

   ![Permissões do sistema - informações da função](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### Etapa 2: Atribuir recursos

>[!IMPORTANT]
>
>Ao atribuir recursos, desative o acesso à ferramenta Permissões se estiver limitando o acesso de uma determinada função. Caso contrário, os usuários poderão modificar suas próprias permissões.

1. Defina **[!UICONTROL Role Scopes]** como um dos seguintes:

   - `All`
   - `Custom`

   Se definido como `Custom` para uma instalação multissite, marque a caixa de seleção do site e armazene onde a função será usada.

   ![Recursos de função de usuário - escopo personalizado](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Os usuários com escopo de função `Custom` não podem criar sites e categorias, atribuir produtos a categorias ou editar produtos no escopo _[!UICONTROL All Store Views]_&#x200B;quando são atribuídos a lojas restritas. Esses usuários também não podem executar outras ações_ globais _que afetam escopos aos quais não têm acesso.

1. Em _[!UICONTROL Roles Resources]_, defina **[!UICONTROL Resource Access]**&#x200B;como `Custom`.

   >[!NOTE]
   >
   >Se a Autenticação de Dois Fatores (2FA) for necessária para fazer logon no Administrador, habilite o Recurso `Permissions` > `Two Factor Auth` para esta função. Caso contrário, os usuários recém-criados com este escopo de função `Custom` não poderão configurar 2FA quando acessarem o Administrador pela primeira vez.

1. Na estrutura de árvore **[!UICONTROL Resource]**, marque a caixa de seleção de cada recurso de Administrador que a função pode acessar.

   Para criar uma função de Administrador com acesso às configurações de imposto, escolha os recursos Vendas/Imposto e Sistema/Imposto. Se estiver configurando um site para uma região que difere do seu [ponto de origem de remessa](../stores-purchase/shipping-settings.md#point-of-origin) padrão, você deve permitir acesso aos recursos Sistema/Remessa para a função. As configurações de entrega determinam a alíquota de imposto da loja usada para preços de catálogo.

   ![Recursos de função de usuário atribuídos](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   A lista de permissões disponíveis pode incluir opções adicionais para extensões agrupadas e instaladas. Ao selecionar a permissão mais alta para cada recurso, você atribui todas as permissões disponíveis para o usuário.

   >[!NOTE]
   >
   >Um usuário administrador deve ter **[!UICONTROL Sales / Archive]** permissões para que seu escopo de função veja as _[!UICONTROL Invoices]_,_[!UICONTROL Credit Memos]_ e _[!UICONTROL Shipments]_[guias](../stores-purchase/order-processing.md).

1. Quando terminar, clique em **[!UICONTROL Save Role]**.

   A função agora aparece na grade e pode ser atribuída a contas de usuário.

## Atribuir uma função aos usuários

1. Na grade _[!UICONTROL Roles]_, abra o registro no modo de edição.

1. Em _[!UICONTROL Current User Identity Verification]_, digite a senha da sua conta de usuário.

1. No painel esquerdo, escolha **[!UICONTROL Role Users]**.

   A opção _[!UICONTROL Role Users]_&#x200B;aparece somente depois que uma nova função é salva.

   ![Contas de usuário atribuídas à função](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. Para pesquisar um registro de usuário específico, faça o seguinte:

   - Insira o valor no filtro de pesquisa na parte superior de uma coluna e pressione **Enter**.

   - Quando estiver pronto para retornar à lista completa, clique em **[!UICONTROL Reset Filter]**.

1. Marque a caixa de seleção de qualquer usuário a ser atribuído à função.

1. Clique em **[!UICONTROL Save Role]**.

## Editar uma função

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Localize a função usando filtros acima da grade e clique no nome da função.

1. Faça as alterações necessárias.

   Revise as etapas para criar uma função de usuário para obter informações sobre as configurações da função.

1. Quando solicitado, digite sua senha para confirmar sua identidade.

1. Clique no **[!UICONTROL Save Role]**.

## Excluir uma função

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Localize a função usando filtros acima da grade e abra no modo de edição.

1. No canto superior direito, clique em **[!UICONTROL Delete Role]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

## Demonstração das funções do usuário

Assista a este vídeo para saber mais sobre o gerenciamento de funções de usuário:

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12&learn=on)

## Recursos de função

O acesso aos recursos a seguir pode ser atribuído a uma função personalizada. Consulte a página vinculada para saber mais sobre os recursos associados a cada recurso.

![Adobe Commerce](../assets/adobe-logo.svg) - somente Adobe Commerce

![Adobe Commerce B2B](../assets/b2b.svg) - Disponível somente com Adobe Commerce B2B

| Recurso |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![Adobe Commerce B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html?lang=pt-BR) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [Preparo de conteúdo](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html?lang=pt-BR) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}
