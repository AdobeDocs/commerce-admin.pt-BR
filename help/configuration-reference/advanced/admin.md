---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Admin]'
description: Revise as configurações na página [!UICONTROL Advanced] &gt; [!UICONTROL Admin] do Administrador do Commerce.
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# Avançado > Administrador

{{config}}

## [!UICONTROL Admin User Emails]

![Emails de usuário administrador](./assets/admin-admin-user-emails.png)<!-- zoom -->

Para obter mais informações sobre como alterar essas configurações, consulte [Senha esquecida e redefinir email](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails).

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | Global | Identifica o modelo de email usado para a mensagem enviada quando um usuário administrador esquece a senha. Modelo padrão: `Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | Global | Identifica o contato de armazenamento que aparece como remetente do email _Esqueceu a senha_. Remetente padrão: `General Contact`<br/>Outras opções de remetente: `Sales Representative`, `Customer Support`, `Custom Email` |
| [!UICONTROL User Notification Template] | Global | Determina o modelo de email usado como o padrão para notificações de administrador. Modelo padrão: `User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![Página de inicialização](./assets/admin-startup-page.png)<!-- zoom -->

Para obter mais informações sobre como alterar essas configurações, consulte [Alterar a página de inicialização](../../getting-started/admin-dashboard.md#change-the-startup-page) no _Guia de Introdução_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | Global | Determina a página de aterrissagem do administrador que aparece depois que você faz logon. |

{style="table-layout:auto"}

### [!UICONTROL Startup Page] opções

| Área |                                                                                                                                                                                                                                                                                                                                                                           | Opção |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`Dashboard`](../../getting-started/admin-dashboard.md) |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Sales` | `Operations` | [`Quotes`](../../b2b/quotes.md) ![Adobe Commerce B2B](../../assets/b2b.svg) <br/>[`Orders`](../../stores-purchase/orders.md)<br/>[`Invoices`](../../stores-purchase/invoices.md)<br/>[`Shipments`](../../stores-purchase/shipments.md)<br/>[`Credit Memos`](../../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../../stores-purchase/returns.md) ![Adobe Commerce](../../assets/adobe-logo.svg) </span><br/>[`Transactions`](../../stores-purchase/transactions.md)<br/>`Braintree Virtual Terminal` |
| `Catalog` | [`Inventory`](../../inventory-management/introduction.md) | [`Products`](../../catalog/products-list.md)<br/>[`Categories`](../../catalog/categories.md)<br/>[`Shared Catalog`](../../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../../assets/b2b.svg) |
| `Customers` | [`All Customers`](../../customers/customers-all.md)<br/>[`Now Online`](../../customers/now-online.md)<br/>[`Customer Groups`](../../customers/customer-groups.md)<br/>[`Segments`](../../customers/customer-segments.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Companies`](../../b2b/account-companies.md)![Adobe Commerce B2B](../../assets/b2b.svg) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Marketing` | `Promotions` | [`Catalog Price Rule`](../../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../../merchandising-promotions/price-rules-cart.md)) <br/>[`Related Products Rules`](../../merchandising-promotions/product-related-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Gift Card Accounts`](../../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Private Sales`](../../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Events`](../../merchandising-promotions/event-configure.md) <br/>[`Invitations`](../../merchandising-promotions/invitations.md) |
|                                                         | `Communications` | [`Email Templates`](../../systems/email-templates.md) <br/>[`Newsletter Template`](../../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../../merchandising-promotions/email-reminder-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | `SEO & Search` | [`Search Terms`](../../catalog/search-terms.md) <br/>[`Search Synonyms`](../../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../../merchandising-promotions/url-rewrite.md) <br/>[`Site Map`](../../merchandising-promotions/sitemap-xml.md) |
|                                                         | [`User Content`](../../catalog/settings-advanced-product-reviews.md) | [`All Reviews`](../../catalog/settings-advanced-product-reviews.md) <br/>[`Pending Reviews`](../../merchandising-promotions/product-reviews-moderate.md) <br/> |
| `Content` | `Elements` | [`Pages`](../../content-design/pages.md)<br/>[`Hierarchy`](../../content-design/page-hierarchy.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Blocks`](../../content-design/blocks.md)<br/>[`Dynamic Blocks`](../../content-design/dynamic-blocks.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Widgets`](../../content-design/widgets.md)<br/>[`Media Gallery`](../../content-design/media-storage.md) |
|                                                         | `Design` | [`Configuration`](../../content-design/configuration.md)<br/>[`Themes`](../../content-design/themes.md)<br/>[`Schedule`](../../content-design/schedule.md) |
|                                                         | `Content Staging` ![Adobe Commerce](../../assets/adobe-logo.svg)<br /> | [Painel](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Customers`](../../getting-started/customer-reports.md) | `Order Total`<br/>`Order Count`<br/>`New`<br/>`Wish Lists`<br/>`Segments`<br/> |
|                                                         | [`Products`](../../getting-started/product-reports.md) | `Views`<br/>`Bestsellers`<br/>`Low Stock`<br/>`Ordered`<br/>`Downloads` |
|                                                         | [`Private Sales`](../../getting-started/private-sales-reports.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | `Invitations`<br/>`Invited Customers`<br/>`Conversions` |
|                                                         | `Statistics` | [`Refresh Statistics`](../../getting-started/sales-reports.md#refresh-statistics) |
|                                                         | [`Business Intelligence`](../../getting-started/business-intelligence.md) | `Advanced Reporting`<br/>`BI Essentials`<br/> |
|                                                         | `Customer Engagement` | `Dashboard`<br/>`Importer Status`<br/>`Automation Enrollment`<br/>`Campaign Sends`<br/>`SMS Sends`<br/>`Cron Tasks`<br/>`Log Viewer`<br/>`Abandoned Carts` |
| `Stores` | `Settings` | [`All Stores`](../../stores-purchase/stores.md)<br/>[`Configuration`](../../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../../stores-purchase/order-status.md) |
|                                                         | [`Inventory`](../../inventory-management/introduction.md) | [`Sources`](../../inventory-management/sources-stocks.md#sources)<br/>[`Stocks`](../../inventory-management/sources-stocks.md#stocks) |
|                                                         | [`Taxes`](../../stores-purchase/taxes.md) | [`Tax Rules`](../../stores-purchase/tax-rules.md)<br/>[`Tax Zones and Rates`](../../stores-purchase/tax-zones-rates.md) |
|                                                         | [`Currency`](../../stores-purchase/currency.md) | [`Currency Rates`](../../stores-purchase/currency-configuration.md)<br/>[`Currency Symbols`](../../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |
|                                                         | `Attributes` | [`Customer`](../../systems/data-attributes-customer.md)<br/>[`Customer Address`](../../systems/data-attributes-customer.md#customer-addresses)<br/>[`Product`](../../systems/data-attributes-product.md)<br/>[`Attribute Set`](../../catalog/attribute-sets.md)<br/>[`Returns`](../../stores-purchase/attributes-returns.md)<br/>[`Ratings`](../../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|                                                         | `Other Settings` | [`Reward Exchange Rates`](../../merchandising-promotions/reward-exchange-rates.md)<br/>[`Gift Wrapping`](../../stores-purchase/cart-configuration.md#gift-wrap)<br/>[`Gift Registry`](../../merchandising-promotions/gift-registry-create.md) |
| `System` | [`Data Transfer`](../../systems/data-transfer.md) | [`Import`](../../systems/data-import.md)<br/>[`Export`](../../systems/data-export.md)<br/>[`Import/Export Tax Rates`](../../systems/data-transfer-tax-rates.md)<br/>[`Import History`](../../systems/data-import.md#import-history)<br/>[`Scheduled Import/Export`](../../systems/data-scheduled-import-export.md) |
|                                                         | `Extensions` | [`Integrations`](../../systems/integrations.md) |
|                                                         | `Tools` | [`Cache Management`](../../systems/cache-management.md)<br/>[`Index Management`](../../systems/index-management.md) |
|                                                         | `Support` | [`Data Collector`](../../systems/support.md#data-collector)<br/>[`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=en#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![URL Base do Administrador](./assets/admin-admin-base-url.png)<!-- zoom -->

Para obter mais informações sobre a configuração dessas opções, consulte [Configurar a URL de base](../../stores-purchase/store-urls.md#configure-the-base-url) no _Guia de Experiência de Compras e Lojas_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | Global | Determina se um URL personalizado é usado para acessar o Administrador. Opções: `Yes` / `No` |
| [!UICONTROL Custom Admin URL] | Global | Especifica uma URL personalizada para acessar o Administrador. Por padrão, o URL de administração é igual ao URL de base.<br/>**Importante:** a URL do Administrador deve estar na mesma instalação do Commerce e ter a mesma raiz do documento que a loja. |
| [!UICONTROL Use Custom Admin Path] | Global | Determina se um caminho personalizado é usado para acessar o Administrador. O caminho padrão é `admin`. Opções: `Yes` / `No` |
| [!UICONTROL Custom Admin Path] | Global | Altera o nome do caminho padrão do Administrador para algo difícil de adivinhar. Insira o nome do caminho personalizado em caracteres minúsculos. Por exemplo: `aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![Segurança](./assets/admin-security.png)<!-- zoom -->

Para obter mais informações sobre a configuração dessas opções, consulte [Configurar a segurança do administrador](../../systems/security-admin.md) no _Guia de Sistemas do Administrador_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | Exibição da loja | Determina se um usuário administrador pode fazer logon na mesma conta simultaneamente a partir de diferentes dispositivos. Opções: <br/>**`Yes`**- Permite várias sessões ativas da mesma conta de Administrador.<br/>**`No`** - Permite somente uma sessão ativa por conta de Administrador. |
| [!UICONTROL Password Reset Protection Type] | Exibição da loja | Determina o método usado para gerenciar solicitações de redefinição de senha. Opções: <br/>**`By IP and Email`**- A senha pode ser redefinida online depois que uma resposta é recebida da notificação enviada para o endereço de email associado à conta de Administrador.<br/>**`By IP`** - A senha pode ser redefinida online sem confirmação adicional. <br/>**`By Email`**- A senha só pode ser redefinida respondendo por email à notificação enviada para o endereço de email associado à conta de Administrador.<br/>**`None`** - A senha pode ser redefinida somente pelo administrador de armazenamento. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Global | Determina o número de horas que um link de recuperação de senha permanece válido. |
| [!UICONTROL Max Number of Password Reset Requests] | Exibição da loja | Determina o número máximo de solicitações de senha que podem ser enviadas por hora. |
| [!UICONTROL Min Time Between Password Reset Requests] | Exibição da loja | Determina o número mínimo de minutos entre as solicitações de redefinição de senha. |
| [!UICONTROL Add Secret Key to URLs] | Global | Quando ativado, o anexa uma chave secreta ao URL do administrador como precaução contra explorações. Opções: `Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | Global | Determina se as credenciais de logon inseridas por um usuário devem corresponder às maiúsculas e minúsculas dos armazenados. Opções: `Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | Global | Determina a duração de uma sessão do Administrador em segundos. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Global | Determina o número de vezes que os usuários administradores podem tentar fazer logon antes que suas contas sejam bloqueadas. Se o campo estiver vazio, nenhum mínimo será definido. Valor padrão: `6` |
| [!UICONTROL Lockout Time (minutes)] | Global | Determina por quantos minutos uma conta de Administrador é bloqueada antes que o usuário possa tentar fazer logon novamente. Valor padrão: `30` |
| [!UICONTROL Password Lifetime (days)] | Global | Determina o número de dias antes de uma senha de administrador expirar. Se o campo estiver vazio, nenhuma duração será definida. Valor padrão: `90` |
| [!UICONTROL Password Change] | Global | Determina se usuários administradores precisam alterar suas senhas. Opções: <br/>**`Forced`**- Exige que os usuários Administradores alterem suas senhas após a configuração da conta.<br/>**`Recommended`** - Recomenda que os usuários administradores alterem suas senhas após a configuração da conta. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Painel](./assets/admin-dashboard.png)<!-- zoom -->

Para obter mais informações sobre como configurar essas opções, consulte o [Painel de administração](../../getting-started/admin-dashboard.md) no _Guia de Introdução_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | Global | Determina se o painel inclui um gráfico gerado dos dados de vendas atuais. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![Grades do Administrador](./assets/admin-admin-grids.png)<!-- zoom -->

Para obter mais informações sobre como configurar essas opções, consulte [Limitar exibição do produto](../../catalog/products-list.md#limit-product-display) no _Guia de Gerenciamento de Catálogo_.

>[!NOTE]
>
>Para melhorar o desempenho de catálogos grandes, é recomendável limitar o número de produtos exibidos na grade.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | Global | Determina se o número de produtos exibidos na grade é limitado ao valor _[!UICONTROL Records Limit]_. Opções: `Yes` / `No` |
| [!UICONTROL Records Limit] | Global | Define o limite de número de produtos na grade de produtos. O valor mínimo padrão é `20000`. |

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/admin-captcha.png)<!-- zoom -->

Para obter mais informações sobre a configuração dessas opções, consulte [CAPTCHA](../../systems/security-captcha.md) no _Guia de Sistemas de Administração_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | Global | Habilita CAPTCHA para o logon de Administrador. Opções: `Yes` / `No` |
| [!UICONTROL Font] | Global | Determina a fonte usada para exibir o CAPTCHA. Para adicionar sua própria fonte, coloque o arquivo de fonte no mesmo diretório da instância do Commerce e adicione a declaração ao arquivo config.xml em `app/code/Magento/Captcha/etc` Fonte padrão:` LinLibertine` |
| [!UICONTROL Forms] | Global | Determina os formulários em que CAPTCHA é usado. Opções: `Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | Global | Determina quando o CAPTCHA é exibido. Opções: <br/>**`Always`**- CAPTCHA é sempre necessário para fazer logon.<br/>**`After number of attempts to login`** - Exibe o campo [!UICONTROL Number of Unsuccessful Attempts to Login]. Insira o número de tentativas de logon permitidas. Um valor de 0 (zero) é semelhante à definição de Modo de exibição como Sempre. Essa opção não abrange os formulários Esqueceu a senha e Criar usuário. Se CAPTCHA estiver ativado e definido para ser exibido, ele sempre será incluído no formulário.<br />**Observação**: para rastrear o número de tentativas de logon malsucedidas, cada tentativa de logon em um endereço de email e a partir de um endereço IP é contada. O número máximo de tentativas de logon permitidas no mesmo endereço IP é 1.000. Essa limitação se aplica somente quando CAPTCHA está ativado. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Global | Determina o número de vezes que uma pessoa pode tentar fazer logon antes que a conta seja bloqueada. Para rastrear o número de tentativas de logon malsucedidas, o sistema rastreia as tentativas de um endereço de email a partir de um único endereço IP. O número máximo de tentativas permitidas no mesmo endereço IP é 1.000. Essa limitação se aplica somente se CAPTCHA estiver ativado. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Global | Determina a duração do CAPTCHA atual. Quando o CAPTCHA expira, o usuário deve recarregar a página. |
| [!UICONTROL Number of Symbols] | Global | Determina o número de símbolos usados no CAPTCHA. O valor máximo permitido é `8`. Você também pode especificar um intervalo, por exemplo, `5-8`. |
| [!UICONTROL Symbols Used in CAPTCHA] | Global | Determina quais símbolos são usados no CAPTCHA. Somente letras (a-z e A-Z) e números (0-9) são permitidos. O conjunto padrão de símbolos sugeridos no campo exclui símbolos de aparência semelhante como i, l ou 1. A exibição desses símbolos no CAPTCHA diminui a probabilidade de um usuário reconhecer CAPTCHA corretamente. |
| [!UICONTROL Case Sensitive] | Global | Determina se os caracteres usados em CAPTCHA diferenciam maiúsculas de minúsculas. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![Log de Ações do Administrador](./assets/admin-actions-logging.png)<!-- zoom -->

Para obter mais informações sobre a configuração dessas opções, consulte [Arquivo de log de ações](../../systems/action-log-archive.md) no _Guia de Sistemas de Administração_.

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | Global | Habilita o log de ações para cada uma das ações selecionadas: <br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` &lbrace;22 <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites` <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/><br/>`Customer Invitations`<br/>`Gift Registry Entity`<br/>`Newsletter Subscribers` `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![Uso do Administrador](./assets/admin-usage.png)<!-- zoom -->

Para obter mais informações sobre a configuração dessas opções, consulte [Coleção de dados de uso](../../getting-started/admin.md#usage-data-collection) no _Guia de Introdução_.

| Campo | Escopo | Descrição |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | Global | Concede permissão para que o Adobe colete dados de uso de Administrador para melhorar a experiência de uso do _Administrador_ e de produtos e serviços relacionados. Permitir a coleta de dados também habilita o _Guia no Produto_, que foi projetado para fornecer conteúdo interativo, como ajuda, dicas de ferramentas, guias passo a passo, informações de integração, anúncios de recursos e muito mais, ao _Administrador_. Os administradores individuais não são identificados nos dados de uso. Opções:<br />**`Yes`**- Permite a coleta de dados e habilita a _Orientação no Produto_.<br />**`No`** - Não permite coleta de dados nem habilita _Orientação no Produto_. |

{style="table-layout:auto"}
