---
title: Soluções de pagamento PayPal
description: Saiba mais sobre as integrações da solução de pagamento PayPal disponíveis para sua loja.
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# Soluções de pagamento PayPal

PayPal é um líder global em pagamentos online e uma maneira rápida e segura para seus clientes pagarem online. A seleção de soluções PayPal disponíveis varia de acordo com a localização do comerciante. PayPal Express Checkout e PayPal Payments Standard podem ser usados em todas as partes do mundo. Para saber mais, consulte [Soluções PayPal por país](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**Requisitos de PSD2:** <br/>
>A partir de 14 de setembro de 2019, os bancos europeus poderão recusar pagamentos que não satisfaçam [PSD 2](../getting-started/compliance-payment-services-directive.md) requisitos. Para a maioria das soluções do PayPal, nenhuma ação é necessária para estar em conformidade com o PSD2, pois esses requisitos são tratados pelo PayPal.

## Conta comercial do PayPal

Para oferecer o PayPal como um método de pagamento em sua loja, você deve ter um PayPal [conta comercial][1] e/ou um [Conta de Fluxo de Pagamento do PayPal][2]. Os requisitos da conta são especificados na descrição de cada solução do PayPal. Sua conta de comerciante do PayPal também é usada para gerenciar qualquer [filtros de fraude](#paypal-fraud-management-filters) que são aplicados às compras feitas em sua loja.

Os clientes que usam o Check-out expresso do PayPal ou o Check-out expresso para o Payflow Pro devem ter uma conta de comprador do PayPal. PayPal Payments Standard (Padrão de Pagamentos de Sites em alguns países) pode ser usado diretamente ou por meio de uma conta do comprador quando o comerciante permite _Conta do PayPal opcional_. Por padrão, esse parâmetro é ativado para que os clientes possam optar por inserir suas informações de cartão de crédito ou criar uma conta do comprador com o PayPal. Quando desativado, os clientes devem primeiro criar uma conta de comprador do PayPal antes de fazer uma compra.

Website Payments Pro, Website Payments Pro Payflow Edition, Payflow Pro Gateway e Payflow Link exigem que os clientes insiram informações de cartão de crédito durante o checkout.

## PayPal Credit e PayLater

PayPal PayLater oferece aos seus clientes acesso rápido ao financiamento, para que possam comprar agora e pagar ao longo do tempo, sem custo adicional para você. Você não é cobrado quando os clientes escolhem as opções de crédito do PayPal e você paga apenas sua taxa de transação normal do PayPal. Para saber mais, consulte a [Site do PayPal][3].

Dê um impulso às suas vendas ao anunciar financiamento. O PayPal ajuda a transformar navegadores em compradores com financiamento do PayPal PayLater. Seus clientes podem pagar ao longo do tempo, enquanto você é pago antecipadamente — sem custo adicional para você. Use anúncios de banner gratuitos do PayPal para anunciar o financiamento do PayPal como uma opção de pagamento quando seus clientes fizerem check-out com o PayPal. Demonstrou-se que o PayPal Advertising Program gera compras adicionais e aumenta os tamanhos médios das compras em 15% ou mais.

Você pode adicionar facilmente anúncios de banner gratuitos e prontos para as páginas do seu site e da _Crédito do PayPal_ botão ao carrinho de compras durante o checkout para lembrar aos clientes que o financiamento está prontamente disponível.

>[!NOTE]
>
>A partir da versão 2.4.3, o PayPal PayLater é compatível com implantações que incluem o PayPal. Esse recurso permite que os compradores paguem um pedido em prestações quinzenais em vez de pagar o valor total no momento da compra. A experiência do PayPal Credit está obsoleta.

Para comerciantes dos EUA, o Crédito do PayPal é ativado por padrão para o [Check-out do PayPal Express](paypal-express-checkout.md) opção de pagamento. Para desativá-lo para este método de pagamento, consulte _Recursos_ seção de [Configuração de finalização de compra do PayPal Express](paypal-express-checkout.md#features).

O Crédito do PayPal está desabilitado por padrão para as outras soluções de pagamento do PayPal, mas pode ser habilitado na configuração do método de pagamento para soluções de suporte:

- [Pagamentos Avançados](paypal-payments-advanced.md)
- [Pagamentos Pro](paypal-payments-pro.md)
- [Pagamentos Padrão](paypal-payments-standard.md)
- [Fluxo de pagamento Pro](paypal-payflow-pro.md)
- [Vínculo de Fluxo de Pagamento](paypal-payflow-link.md)

>[!IMPORTANT]
>
>Antes de configurar o PayPal Credit ou o PayPal PayLater para sua loja, verifique se ele está ativado em sua conta de comerciante do PayPal.

## Soluções PayPal integradas

Com PayPal e Adobe Commerce, você pode aceitar pagamentos de todos os principais cartões de débito e crédito. PayPal oferece conveniência adicional sem esforço extra, porque até mesmo seus clientes que não têm uma conta PayPal podem pagar por suas compras com PayPal.

>[!NOTE]
>
>Você não pode ter mais de um método do PayPal habilitado em sua loja por vez, exceto pelo Check-out expresso do PayPal. O Check-out do PayPal Express pode ser usado com outros métodos de pagamento do PayPal, exceto para o PayPal Payments Standard. Se você alterar as soluções de pagamento, o método anterior será desabilitado.

### Check-out do PayPal Express

[Check-out do PayPal Express](paypal-express-checkout.md)

### Soluções de pagamento PayPal All-in-one

Nos Estados Unidos, o PayPal oferece as seguintes soluções compatíveis com PCI para atender às necessidades de sua empresa em crescimento.

- [Pagamentos do PayPal Avançados](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

![Soluções de pagamento PayPal all-in-one](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### Gateways de pagamento do PayPal

Um gateway de pagamento é um serviço de comerciantes fornecido por um provedor de serviços de aplicativos de comércio eletrônico que autoriza o processamento de pagamentos diretos ou por cartão de crédito. Eles trabalham como intermediários entre clientes e bancos.

Os gateways de pagamento estão disponíveis em ambientes online e offline. Os pagamentos podem ser aceitos por telefone, online ou por meio de um aplicativo móvel. A transação é enviada ao sistema de processamento do provedor de serviços e, em seguida, enviada ao banco do cliente para verificação e confirmação. Se verificado, o comerciante recebe o pagamento sem ter contato direto com a conta bancária do cliente.

Há dois tipos de gateways de pagamento — direto e hospedado.

- Os gateways de pagamento direto permitem que os usuários insiram os detalhes de seus cartões no site da loja.
- Os gateways de pagamento hospedados redirecionam os usuários para uma página de pagamento hospedada, fora do site da loja.

O gateway de pagamento fornece segurança e proteção para todas as partes envolvidas em uma transação.

PayPal oferece uma opção de duas soluções de gateway de pagamento para sua empresa. Você pode permitir que o PayPal hospede seu checkout em seu site de pagamento seguro ou pode assumir o controle de toda a experiência de pagamento com uma solução personalizável.

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Link do fluxo de pagamento do PayPal](paypal-payflow-link.md)

![Configurar gateways de pagamento do PayPal](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## Filtros de gerenciamento de fraude do PayPal

Os filtros de gerenciamento de fraudes do PayPal facilitam a detecção e a resposta a transações fraudulentas, e podem ser configurados para sinalizar, reter para análise ou negar pagamentos com maior risco. Ações relacionadas ao Commerce [status do pedido](order-status.md) valores alterados de acordo com as configurações do filtro de fraude:

| Ação | Resultado |
| --- | --- |
| [!UICONTROL Review] | O pedido suspeito recebe o status _Revisão de pagamento_ quando o pedido é feito. Você pode revisar o pedido e aprovar, ou cancelar o pagamento no Admin, ou no lado do PayPal. Ao clicar em **[!UICONTROL Accept Payment]** ou **[!UICONTROL Deny Payment]**, nenhuma nova transação para o pedido será criada. <br/><br/>Se você alterar o status da transação no site do PayPal, deverá clicar em **[!UICONTROL Get Payment Update]** na página Pedido do Administrador para aplicar as alterações. Se você clicar em **[!UICONTROL Accept Payment]** ou **[!UICONTROL Deny Payment]**, as alterações feitas no site do PayPal são aplicadas. |
| [!UICONTROL Deny] | O pedido suspeito não pode ser feito pelo cliente, porque a transação correspondente é rejeitada pelo PayPal. <br/><br/>Para negar o pagamento ao Administrador, clique em **[!UICONTROL Deny Payment]** no canto superior direito da página. O status do pedido muda para `Canceled`, a transação é revertida e os fundos são liberados na conta do cliente. As informações correspondentes são adicionadas na _[!UICONTROL Comments History]_seção da visualização de pedido. |
| [!UICONTROL Flag] | O pedido suspeito recebe o status `Processing` quando é colocado. A transação correspondente é marcada com um sinalizador na lista de transações de conta de comerciante. |

{style="table-layout:auto"}

## Soluções PayPal por país

| País | Solução de pagamento do PayPal |
|--- |--- |
| Austrália | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Canadá | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (inclui Check-out expresso)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| França | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Alemanha | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| RAE de Hong Kong | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Itália | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Japão | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Nova Zelândia | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Espanha | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Reino Unido | [!DNL PayPal Payments Pro Hosted Solution] (inclui Check-out expresso)<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Estados Unidos | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) (inclui Check-out expresso)<br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) (inclui Check-out expresso)<br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) (inclui Check-out expresso)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (inclui Check-out expresso)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

{style="table-layout:auto"}

### Outros países

PayPal Express Checkout e PayPal Website Payments Standard estão disponíveis nos seguintes países:

- Argentina
- Áustria
- Bélgica
- Brasil
- Bulgária
- Chile
- Costa Rica
- Chipre
- República Checa
- Dinamarca
- República Dominicana
- Equador
- Estônia
- Finlândia
- Guiana Francesa
- Gibraltar
- Grécia
- Guadalupe
- Hungria
- Islândia
- Índia
- Indonésia
- Irlanda
- Israel
- Jamaica
- Letônia
- Liechtenstein
- Lituânia
- Luxemburgo
- Malásia
- Malta
- Martinica
- México
- Holanda
- Noruega
- Filipinas
- Polônia
- Portugal
- Reunião
- Romênia
- San Marino
- Singapura
- Eslováquia
- Eslovênia
- África do Sul
- Coreia do Sul
- Suécia
- Suíça
- Taiwan
- Tailândia
- Turquia
- Emirados Árabes Unidos
- Uruguai
- Venezuela
- Vietnã


[1]: https://manager.paypal.com/
[2]: https://developer.paypal.com/docs/payflow/payflow-gateway/
[3]: https://www.paypal.com/us/business/buy-now-pay-later
