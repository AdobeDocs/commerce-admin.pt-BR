---
title: Guia de referência de configuração
description: Revise as informações descritivas para todas as configurações de armazenamento do administrador do Commerce organizadas pelas guias de configuração, páginas e seções.
exl-id: b0359ba4-3643-4355-9154-adfedb369ec3
source-git-commit: 323ea635286fcb9a2bcc7f4f56b32c1518a7beef
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Guia de referência de configuração

Este guia destina-se aos comerciantes e administradores de sistema que trabalham com Adobe Commerce ou Magento Open Source. Ela fornece informações de referência para todas as definições de configuração de armazenamento acessadas do _Admin_ barra lateral em **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

Ela não aborda detalhes sobre os recursos do Adobe Commerce e do Magento Open Source ou procedimentos para configuração de armazenamento.

Este guia é organizado de acordo com a navegação à esquerda da configuração:

| Guia Configuração | Guias secundárias |
| ----------------- | ---------- |
| **[!UICONTROL General]** <br/><br/>A variável _[!UICONTROL General]_as seções de configuração determinam os parâmetros da loja, URLs, tema, moeda, endereços de email, contatos da loja, editor e relatório do painel. | - [[!UICONTROL General]](./general/general.md)<br>- [[!UICONTROL B2B Features]](./general/b2b-features.md)<br>- [[!UICONTROL Web]](./general/web.md)<br>- [[!UICONTROL Currency Setup]](./general/currency-setup.md)<br>- [[!UICONTROL Store Email Addresses]](./general/store-email-addresses.md)<br>- [[!UICONTROL Contacts]](./general/contacts.md)<br>- [[!UICONTROL Reports]](./general/reports.md)<br>- [[!UICONTROL Content Management]](./general/content-management.md)<br>- [[!UICONTROL New Relic Reporting]](./general/new-relic-reporting.md)<br>- [[!UICONTROL Advanced Reporting]](./general/advanced-reporting.md) |
| **[!UICONTROL Catalog]** <br/><br/>A variável _[!UICONTROL Catalog]_as configurações determinam as configurações do produto e do inventário, controlam a geração do mapa de site e do feed RSS e especificam o modelo de email usado para compartilhar produtos com amigos. | - [[!UICONTROL Catalog]](./catalog/catalog.md)<br>- [[!UICONTROL Visual Merchandiser]](./catalog/visual-merchandiser.md)<br>- [[!UICONTROL Inventory]](./catalog/inventory.md)<br>- [[!UICONTROL XML Sitemap]](./catalog/xml-sitemap.md)<br>- [[!UICONTROL RSS Feeds]](./catalog/rss-feeds.md)<br>- [[!UICONTROL Email to a Friend]](./catalog/email-to-a-friend.md) |
| **[!UICONTROL Security]** <br/><br/>A variável _[!UICONTROL Security]_as configurações controlam a segurança do armazenamento, a autenticação de dois fatores e o recurso reCAPTCHA do Google. | - [[!UICONTROL 2FA]](./security/2fa.md)<br>- [[!UICONTROL Google reCAPTCHA Admin Panel]](./security/google-recaptcha-admin.md)<br>- [[!UICONTROL Google reCAPTCHA Storefront]](./security/google-recaptcha-storefront.md)<br>- [[!UICONTROL Security.txt]](./security/security-txt.md) |
| **[!UICONTROL Customers]** <br/><br/>A variável _[!UICONTROL Customers]_as configurações estabelecem opções básicas de logon e conta do cliente, configurações do boletim informativo, lista de desejos e o formato de códigos de cupom gerados automaticamente. | - [[!UICONTROL Login as Customer]](./customers/login-as-customer.md)<br>- [[!UICONTROL Newsletter]](./customers/newsletter.md)<br>- [[!UICONTROL Company Configuration]](./customers/company-configuration.md)<br>- [[!UICONTROL Customer Configuration]](./customers/customer-configuration.md)<br>- [[!UICONTROL Requisition Lists]](./customers/requisition-lists.md)<br>- [[!UICONTROL Wish List]](./customers/wishlist.md)<br>- [[!UICONTROL Invitations]](./customers/invitations.md)<br>- [[!UICONTROL Reward Points]](./customers/reward-points.md)<br>- [[!UICONTROL Promotions]](./customers/promotions.md)<br>- [[!UICONTROL Gift Registry]](./customers/gift-registry.md)<br>- [[!UICONTROL Persistent Shopping Cart]](./customers/persistent-shopping-cart.md) |
| **[!UICONTROL Sales]** <br/><br/>A variável _[!UICONTROL Sales]_as configurações determinam as configurações de pagamento e imposto, opções de pagamento e envio, email de vendas e impressões de PDF e configurações da API do Google. | - [[!UICONTROL Sales]](./sales/sales.md)<br>- [[!UICONTROL Sales Emails]](./sales/sales-emails.md)<br>- [[!UICONTROL Quotes]](./sales/quotes.md)<br>- [[!UICONTROL PDF Print-outs]](./sales/pdf-print-outs.md)<br>- [[!UICONTROL Tax]](./sales/tax.md)<br>- [[!UICONTROL Checkout]](./sales/checkout.md)<br>- [[!UICONTROL Shipping Settings]](./sales/shipping-settings.md)<br>- [[!UICONTROL Multishipping Settings]](./sales/multishipping-settings.md)<br>- [[!UICONTROL Delivery Methods]](./sales/delivery-methods.md)<br>- [[!UICONTROL Google API]](./sales/google-api.md)<br>- [[!UICONTROL 3D Secure]](./sales/3d-secure.md)<br>- [[!UICONTROL Gift Cards]](./sales/gift-cards.md)<br>- [[!UICONTROL Payment Methods]](./sales/payment-methods.md) |
| **[!UICONTROL Sales Channels]** <br/><br/>Quando a variável [!DNL Amazon Sales Channel] estiver instalada, a variável _[!UICONTROL Sales Channels]_as configurações controlam as operações de integração automatizada com a loja da Amazon. | - [[!UICONTROL Global Settings]](sales-channels.md) |
| **[!UICONTROL Services]** <br/><br/>A variável _[!UICONTROL Services]_As configurações do determinam as configurações de integração da API do Commerce, incluindo SOAP e OAuth. | - [[!UICONTROL Web API]](./services/magento-web-api.md)<br>- [[!UICONTROL Commerce Services]](./services/saas.md)<br>- [[!UICONTROL OAuth]](./services/oauth.md) |
| **[!UICONTROL Advanced]** <br/><br/>A variável _[!UICONTROL Advanced]_As configurações do determinam as configurações padrão do Administrador, várias configurações do sistema, controles avançados de módulo e ferramentas de desenvolvedor. | - [[!UICONTROL Admin]](./advanced/admin.md)<br>- [[!UICONTROL System]](./advanced/system.md)<br>- [[!UICONTROL Developer]](./advanced/developer.md) |

{style="table-layout:auto"}

Ela não aborda detalhes sobre os recursos do Adobe Commerce e do Magento Open Source ou procedimentos para configuração de armazenamento.

## Documentação disponível

{{docs-links}}
