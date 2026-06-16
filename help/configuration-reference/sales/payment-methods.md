---
title: '[!UICONTROL Sales] > [!UICONTROL Payment Methods]'
description: Revise as configurações na página [!UICONTROL Sales] > [!UICONTROL Payment Methods] do Administrador do Commerce.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
TQID: https://experienceleague.adobe.com/Z6f-lyypn4xUeVxiR0SQ81PswzU69X3sVCqEa8bTDnc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1746
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Os Payment Services for Adobe Commerce and Magento Open Source fornecem uma solução de autoatendimento pronta para uso, incluindo teste de sandbox e uma configuração simples, para fornecer um processamento de pagamento robusto e seguro. Para saber mais sobre este poderoso conjunto de ferramentas e como ele pode fornecer a você o controle e a insight necessários para criar a melhor experiência para seus compradores, consulte o [_Guia do Usuário dos Serviços de Pagamento_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=pt-BR).

{{config}}

## [!UICONTROL Merchant Location]

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

![Localização do Comerciante](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/en/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Site | Identifica o país onde o comerciante está registrado para realizar negócios. |

{style="table-layout:auto"}

## Soluções recomendadas

As seguintes soluções de pagamento são recomendadas como uma maneira fácil para os comerciantes que estão apenas começando a aceitar o pagamento online por conta PayPal ou cartão de crédito. À medida que sua empresa cresce, você pode combiná-los com soluções de pagamento PayPal adicionais.

- [Payment Services](payment-services.md)
- [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} [Check-out do PayPal Express](paypal-express-checkout.md)
- [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} [Braintree](braintree.md)

>[!NOTE]
>
>Algumas integrações de pagamento e extensões agrupadas foram removidas nas versões 2.4.x e movidas para o Commerce Marketplace. Você pode encontrar as últimas extensões oficiais de integração de pagamento no [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.
><br/>>**Amazon Pay** e **Klarna**: as versões 2.4.0 a 2.4.3 da Adobe Commerce e do Magento Open Source incluíam essas extensões desenvolvidas pelo fornecedor. A partir da versão 2.4.4, essas extensões não serão mais agrupadas com a versão principal e deverão ser instaladas e atualizadas do Commerce Marketplace. O Marketplace também fornece acesso à documentação atual fornecida pelo desenvolvedor da extensão.
><br/>>Se uma dessas extensões agrupadas estiver habilitada e configurada, você deverá atualizar seu arquivo `composer.json` como parte do processo de atualização 2.4.4 e gerenciar as atualizações de extensão a partir de agora. Consulte [Atualizar módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) no _Guia de Atualização_ para obter mais informações.<br/>
><br/>>**Worldpay**, **Eway**, **CyberSource** e **Authorize.Net**: para obter detalhes sobre como fazer uma transição segura dessas integrações de pagamento, consulte o [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Outros métodos do PayPal

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

PayPal oferece várias soluções de pagamento que atendem às necessidades de empresas de todos os portes, e que estão envolvidas em negócios em todo o mundo. PayPal oferece a capacidade de aceitar pagamentos de todos os principais cartões de débito e crédito. O PayPal oferece conveniência adicional sem esforço extra, porque até mesmo os clientes que não têm uma conta do PayPal podem pagar suas compras com o PayPal.

### Métodos multifuncionais PayPal

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

- [Pagamento avançado do PayPal](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

### Gateways de pagamento do PayPal

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

- [PayPal Payflow Pro](paypal-payflow-pro.md) (Inclui Check-out Expresso)
- [Link do Fluxo de Pagamento do PayPal](paypal-payflow-link.md) (Inclui Check-out Expresso)

## Métodos de pagamento de base

Os métodos de pagamento a seguir são criados no Commerce e não usam um provedor de serviço de pagamento de terceiros para processar a transação. Muitos dos métodos de pagamento básicos são gerenciados off-line, em vez de on-line.

### [!UICONTROL Check / Money Order]

![Cheque/Ordem de Pagamento](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site | Determina se os clientes podem pagar com cheque ou ordem de pagamento. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O nome deste método de pagamento que aparece para os clientes durante a finalização da compra. |
| [!UICONTROL New Order Status] | Site | Determina o [status do pedido](../../stores-purchase/order-status.md) inicial atribuído a pedidos pagos por cheque ou ordem de pagamento. Valor padrão: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site | Determina os países dos quais você aceita pagamento por cheque ou ordem de pagamento. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site | Identifica os países específicos a partir dos quais você aceita pagamento por cheque ou ordem de pagamento. |
| [!UICONTROL Make Check Payable to] | Exibição da loja | O nome da entidade a quem os cheques e as ordens de pagamento devem ser pagos. |
| [!UICONTROL Send Check to] | Exibição da loja | O endereço ou caixa postal para o qual os cheques e as ordens de pagamento devem ser enviados. |
| [!UICONTROL Minimum Order Total] | Site | O menor valor do pedido que pode ser pago por cheque ou ordem de pagamento. |
| [!UICONTROL Maximum Order Total] | Site | O maior valor de ordem que pode ser pago por cheque ou ordem de pagamento. <br/><br/>**_Nota:_** Um pedido é qualificado se o total estiver entre, ou corresponder, ao total mínimo ou máximo do pedido. |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o pagamento por cheque ou ordem de pagamento é exibido quando listado com outros métodos de pagamento durante a finalização da compra. Digite `0` para colocá-lo no topo da lista. |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![Pagamento por Transferência Bancária](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site | Determina se os clientes podem pagar transferindo o pagamento diretamente do banco para a conta do comerciante. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O nome deste método de pagamento que aparece para os clientes durante a finalização da compra. |
| [!UICONTROL New Order Status] | Site | Determina o status inicial do pedido atribuído a pedidos pagos por transferência bancária. Valor padrão: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site | Determina os países dos quais você aceita pagamento por transferência bancária. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site | Identifica os países específicos dos quais você aceita pagamento por transferência bancária. |
| [!UICONTROL Minimum Order Total] | Site | O menor valor de ordem que pode ser pago por transferência bancária. |
| [!UICONTROL Maximum Order Total] | Site | O maior valor de ordem que pode ser pago por transferência bancária. <br/><br/>**_Nota:_** Um pedido é qualificado se o total estiver entre, ou corresponder, ao total mínimo ou máximo do pedido. |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o pagamento por transferência bancária é exibido quando listado com outros métodos de pagamento durante a finalização da compra. Digite `0` para colocá-lo no topo da lista. |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![Pagamento na conta](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site | Determina se as empresas podem usar o crédito da empresa para fazer compras. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O nome deste método de pagamento que aparece para os clientes durante a finalização da compra. |
| [!UICONTROL New Order Status] | Site | Determina o status de novos pedidos cobrados em uma conta da empresa. Opções: `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Site | Determina os países nos quais você permite que as empresas debitem as compras de suas contas. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site | Identifica os países específicos em que as empresas podem cobrar compras em suas contas. |
| [!UICONTROL Minimum Order Total] | Site | Especifica o menor valor de pedido que pode ser cobrado em uma conta de empresa. |
| [!UICONTROL Maximum Order Total] | Site | O maior valor de pedido que pode ser cobrado em uma conta de empresa. <br/><br/>**_Nota:_** Um pedido é qualificado se o total estiver entre, ou corresponder, ao total mínimo ou máximo do pedido. |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o pagamento por conta é exibido quando listado com outros métodos de pagamento durante a finalização da compra. Digite `0` para colocá-lo no topo da lista. |

{style="table-layout:auto"}

>[!NOTE]
>
>O pagamento por conta não é suportado para pedidos com [vários endereços de envio](../../stores-purchase/shipping-settings.md#multiple-addresses) e não aparece entre as opções de pagamento.

### [!UICONTROL Cash On Delivery Payment]

![Pagamento à vista na entrega](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site | Determina se os clientes podem pagar transferindo o pagamento diretamente do banco para a conta do comerciante. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O nome deste método de pagamento que aparece para os clientes durante a finalização da compra. |
| [!UICONTROL New Order Status] | Site | Determina o status inicial do pedido atribuído a pedidos pagos por transferência bancária. Valor padrão: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site | Determina os países dos quais você aceita pagamento por transferência bancária. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site | Identifica os países específicos dos quais você aceita pagamento por transferência bancária. |
| [!UICONTROL Minimum Order Total] | Site | Especifica o menor valor de ordem que pode ser pago por transferência bancária. |
| [!UICONTROL Maximum Order Total] | Site | O maior valor de ordem que pode ser pago por transferência bancária. <br/><br/>**_Nota:_** Um pedido é qualificado se o total estiver entre, ou corresponder, ao total mínimo ou máximo do pedido. |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o pagamento por transferência bancária é exibido quando listado com outros métodos de pagamento durante a finalização da compra. Digite `0` para colocá-lo no topo da lista. |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![Check-out de Subtotal Zero](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Title] | Exibição da loja | O nome usado para este método de pagamento durante o check-out. Valor padrão: Nenhuma Informação de Pagamento Necessária |
| [!UICONTROL Enabled] | Site | Determina se o Check-out de Subtotal Zero está disponível para que o administrador da loja gerencie pedidos que têm um subtotal igual a zero, como um que foi tributado, mas um desconto reduziu o valor para zero. Opções: `Yes` / `No` |
| [!UICONTROL New Order Status] | Site | Determina o status inicial do pedido atribuído aos pedidos processados como Checkout de subtotal zero. Valor padrão: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site | Determina os países a partir dos quais o Check-out de Subtotal Zero pode ser aplicado. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site | Identifica os países específicos para os quais o Check-out de Subtotal Zero pode ser aplicado. |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o título, como &quot;Nenhuma Informação de Pagamento é Necessária&quot;, é exibido quando listado com outros métodos de pagamento durante a finalização da compra. Digite `0` para colocá-lo no topo da lista. |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

As ações de pagamento estão configuradas _por método de pagamento_. A ação de pagamento determina quando os fundos são capturados e quando as NFFs são criadas para suas ordens de venda.

Consulte a seção Configurações básicas de cada tópico de método de pagamento individual para obter uma lista abrangente de opções de configuração individuais.

| Ação de pagamento | Descrição |
|--- |---|
| [!UICONTROL Authorization] | Aprova a compra, mas retém os fundos. O valor não é sacado até que seja capturado pelo comerciante. |
| [!UICONTROL Authorize] | Autoriza a conta do comprador para o total do pedido, mas não captura o pagamento. Capturar pagamento criando uma NFF. As ordens autorizadas podem ser anuladas ou canceladas. |
| [!UICONTROL Authorize and Capture] | Autoriza a conta do comprador para o total do pedido e captura o pagamento. Uma NFF é criada automaticamente. Você pode reembolsar fundos capturados por meio de um aviso de crédito. Não é possível cancelar um pedido depois que o pagamento é capturado. |
| [!UICONTROL Charge on shipment] | A Amazon recebe uma solicitação de captura e cobra do cliente quando uma fatura é criada no Commerce. |
| [!UICONTROL Charge on order] | A Amazon cria a fatura e cobra o cliente quando o pedido é feito. |
| [!UICONTROL Not Capture] | Quando a fatura é enviada, o sistema não captura o pagamento. Pressupõe-se que você capture o pagamento por meio do Commerce posteriormente. Há um botão Capturar na fatura concluída. Antes de capturar, você pode cancelar a NFF. Depois de capturar, você pode criar um aviso de crédito e anular a NFF. |
| [!UICONTROL Order] | Representa um acordo com o PayPal que permite que o comerciante capture um ou mais valores até o total do pedido da conta do comprador do cliente, dentro de um período de tempo definido (até 29 dias). |
| [!UICONTROL Sale] | O valor da compra é autorizado e imediatamente retirado da conta do cliente. |

{style="table-layout:auto"}

>[!NOTE]
>
>Não selecione a opção _[!UICONTROL Not Capture]_, a menos que tenha certeza de que capturará o pagamento por meio do Commerce posteriormente. Você não pode criar um aviso de crédito até que o pagamento tenha sido capturado usando o botão Capturar.

## [!UICONTROL Purchase Order]

![Ordem de Compra](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site | Determina se os clientes podem pagar por ordem de compra (OC). Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O nome deste método de pagamento que aparece para os clientes durante a finalização da compra. |
| [!UICONTROL New Order Status] | Site | Determina o [status do pedido](../../stores-purchase/order-status.md) inicial atribuído a pedidos pagos por OC. Valor padrão: Pendente |
| [!UICONTROL Payment from Applicable Countries] | Site | Determina os países a partir dos quais você aceita pagamento por OC. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site | Identifica os países específicos a partir dos quais você aceita pagamento por OC. |
| [!UICONTROL Minimum Order Total] | Site | O menor valor de ordem que pode ser pago por OC. |
| [!UICONTROL Maximum Order Total] | Site | O maior valor de ordem que pode ser pago por OC. <br/><br/>**_Nota:_** Um pedido é qualificado se o total estiver entre, ou corresponder, ao total mínimo ou máximo do pedido. |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o pagamento por OC é exibido quando listado com outros métodos de pagamento durante a finalização da compra. Digite `0` para colocá-lo no topo da lista. |

{style="table-layout:auto"}
