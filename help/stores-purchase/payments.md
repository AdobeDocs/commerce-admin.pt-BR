---
title: Visão geral de pagamentos
description: Saiba mais sobre os métodos e serviços de pagamento compatíveis nativamente com o Adobe Commerce e o Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Visão geral de pagamentos

O Adobe Commerce e o Magento Open Source são compatíveis com uma grande variedade de métodos e serviços de pagamento. Isso inclui vários métodos de pagamento offline, incluindo pagamento por cheque ou ordem de pagamento e pagamento na entrega (COD). Também há integrações nativas para várias soluções de pagamento online e gateways, incluindo o Braintree como uma extensão agrupada desenvolvida pelo fornecedor.

>[!TIP]
>
>Os Payment Services for Adobe Commerce and Magento Open Source fornecem uma solução de autoatendimento pronta para uso, incluindo teste de sandbox e uma configuração simples, para fornecer um processamento de pagamento robusto e seguro. Para saber mais sobre este poderoso conjunto de ferramentas e como ele pode fornecer a você o controle e a insight necessários para criar a melhor experiência para seus compradores, consulte o [Guia do Usuário dos Serviços de Pagamento](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=pt-BR). Esta é a solução de pagamentos padrão no [Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/commerce/cloud-service/overview).

>[!NOTE]
>
>Revise as [diretrizes de conformidade PCI](../getting-started/compliance-pci.md), que descrevem os requisitos definidos pelo PCI (Payment Card Industry, setor de cartões de pagamento) para empresas que aceitam pagamentos por cartão de crédito pela Internet.

## Alterações no ponto 2.4

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

Algumas integrações de pagamento e extensões agrupadas foram removidas nas versões 2.4.x e movidas para a Commerce Marketplace. Você pode encontrar as últimas extensões oficiais de integração de pagamento no [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.

- **Pagamento do Amazon** e **Klarna**: as versões 2.4.0 a 2.4.3 da Adobe Commerce e do Magento Open Source incluíam essas extensões desenvolvidas pelo fornecedor. A partir da versão 2.4.4, essas extensões não serão mais agrupadas com a versão principal e deverão ser instaladas e atualizadas do Commerce Marketplace. O Marketplace também fornece acesso à documentação atual fornecida pelo desenvolvedor da extensão.

  Se você tiver uma dessas extensões agrupadas ativadas e configuradas, deverá atualizar o arquivo composer.json como parte do processo de atualização 2.4.4 e gerenciar as atualizações de extensão a partir de agora. Consulte [Atualizar módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=pt-BR) no _Guia de Atualização_ para obter mais informações.

- **Worldpay**, **Eway**, **CyberSource** e **Authorize.Net**: para obter detalhes sobre como fazer uma transição segura dessas integrações de pagamento, consulte o [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Métodos de pagamento offline

O Adobe Commerce e o Magento Open Source incluem vários métodos de pagamento offline incorporados, que não exigem os serviços de uma empresa de processamento de pagamentos terceirizada:

- [Checkout de Subtotal Zero](zero-subtotal-checkout.md)
- [Pagamento à vista na entrega](cash-on-delivery.md)
- [Pagamento de Transferência Bancária](bank-transfer.md)
- [Cheque/Ordem de pagamento](check-money-order.md)
- [Ordem de Compra](purchase-order.md)
- [Pagamento na Conta](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (Disponível com Adobe Commerce B2B)

## Métodos de pagamento online

A Adobe Commerce e a Magento Open Source oferecem suporte a várias soluções de pagamento que oferecem serviços aos comerciantes em todas as partes do mundo. Ao contrário das soluções de pagamento que transferem o controle para outro site para concluir a transação, um gateway de pagamento possibilita que você aceite pagamentos com cartão de crédito diretamente da sua loja sem que o cliente saia do site.

### Soluções recomendadas

- [Serviços de pagamento](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=pt-BR)
- [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} [Check-out do PayPal Express](paypal-express-checkout.md)
- [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} [Braintree](braintree.md)

### Outras soluções de pagamento PayPal

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

Consulte [Soluções de pagamento do PayPal](paypal.md) para obter mais informações sobre as opções de método de pagamento do PayPal.

#### Soluções PayPal completas

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

- [Pagamentos do PayPal Avançados](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

#### Gateways de pagamento do PayPal

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Link do fluxo de pagamento do PayPal](paypal-payflow-link.md)

## Proteção contra fraude

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

Os serviços e filtros de proteção contra fraude examinam os pedidos enviados antes que a transação seja processada para detectar pedidos fraudulentos e protegê-lo contra as despesas de cobranças retroativas. A Adobe Commerce e a Magento Open Source oferecem suporte às seguintes soluções de proteção contra fraudes:

- [Filtro de Gerenciamento de Fraude do PayPal](paypal.md#paypal-fraud-management-filters)

- [Soluções de Proteção contra Fraude no Marketplace](https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection)

>[!NOTE]
>
>Para oferecer suporte a atualizações de conformidade com a segurança, a proteção contra fraudes do Signifyd é removida do Commerce a partir da versão 2.4.0. Se você usa a integração Signifyd em uma versão 2.3.x ou anterior, é recomendável fazer a transição para a [extensão de Proteção contra fraude e chargeback Signifyd](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"}. Mantenha as atualizações da extensão de acordo com as diretrizes do fornecedor.

## Solução de problemas de recursos

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

Para obter ajuda com a solução de problemas de pagamento, consulte a [Base de Dados de Conhecimento de Suporte](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=pt-BR).
