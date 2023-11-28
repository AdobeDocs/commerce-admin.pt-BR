---
title: Braintree
description: Saiba como configurar o Braintree como uma solução de pagamento online em sua loja.
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: dba610f53893a8698d2c52fe92fd0266f1cfa0cb
workflow-type: tm+mt
source-wordcount: '2380'
ht-degree: 0%

---

# Braintree

O Braintree oferece uma experiência de finalização de compra totalmente personalizável com detecção de fraudes e integração com o PayPal. Ele suporta [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo e métodos de pagamento locais. O Braintree reduz a carga de conformidade PCI para os comerciantes, pois a transação ocorre no sistema Braintree. A integração do Braintree Payments é desenvolvida pela [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>Se estiver atualizando para 2.4.x a partir de uma versão anterior do Adobe Commerce ou Magento Open Source com a extensão Braintree da Commerce Marketplace instalada, consulte a [Notas de atualização do 2.4](#24-upgrade-notes) no final desta página.

{{beta2-updates}}

## Etapa 1: Obtenha suas credenciais de Braintree

Ir para [Pagamentos Braintree][1] e cadastre-se em uma conta.

## Etapa 2: concluir as configurações básicas

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

   - Se a sua instalação do Commerce tiver vários sites, lojas ou visualizações, no canto superior esquerdo, escolha a **[!UICONTROL Store View]** onde a configuração se aplica.

   - No _[!UICONTROL Merchant Location]_, verifique se **[!UICONTROL Merchant Country]**O está definido como o local da sua empresa.

1. Em _[!UICONTROL Recommended Solutions]_, no_[!UICONTROL Braintree Payments (by GENE Commerce v4.5.0)]_ clique em **[!UICONTROL Configure]**.

   ![Configurar Braintree](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, insira um título que identifique o Braintree como uma opção de pagamento durante o check-out.

1. Definir o sistema operacional atual **[!UICONTROL Environment]** para transações Braintree a `Sandbox` ou `Production`

   Ao testar a configuração em uma sandbox, use apenas [números de cartão de crédito][2] que são recomendados pelo Braintree. Quando estiver pronto para entrar na produção com o Braintree, defina **[!UICONTROL Environment]** para `Production`.

   ![Configurações de credenciais básicas](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Payment Action]** a um dos seguintes:

   - `Authorize Only` - Aprova a compra e suspende os fundos. O valor não é sacado da conta bancária do cliente até que a venda seja _capturado_ pelo comerciante.|
   - `Intent Sale`  - O valor da compra é autorizado e imediatamente retirado da conta do cliente. **_Nota:_** Esse valor foi  _Autorizar e capturar_ nas versões 2.3.x e anteriores.|

1. Insira o **[!UICONTROL Sandbox Merchant ID / Merchant ID]** da sua conta Braintree.

1. Digite as seguintes credenciais da sua conta Braintree:

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >Há campos separados para ambos **(Sandbox e produção)** e os outros campos são renderizados com base no ambiente selecionado.

1. Antes de salvar a configuração, clique em **[!UICONTROL Validate Credentials]** para validar suas credenciais.

1. Definir **[!UICONTROL Enable Card Payments]** para `Yes`.

   ![Configurações básicas](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   Se você quiser ter a capacidade de armazenar informações do cliente com segurança, para que os clientes não precisem digitá-las novamente sempre que fizerem uma compra, defina **[!UICONTROL Enable Vault for Card Payments]** para `Yes`.

## Etapa 3: concluir as configurações avançadas

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Advanced Braintree Settings]** seção.

   ![Configurações avançadas](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. Para **[!UICONTROL Vault Title]**, insira um título descritivo para sua referência que identifique o cofre no qual as informações de cartão do cliente estão armazenadas.

1. Insira o **[!UICONTROL Merchant Account ID]** da sua conta Braintree.

   Se você não especificar a conta de comerciante a ser usada, o Braintree processará a transação usando sua conta de comerciante padrão.

1. Se você quiser impedir que a transação seja enviada para avaliação como parte das verificações das Ferramentas Avançadas de Fraude, em pedidos feitos por meio do Administrador, defina **[!UICONTROL Skip Fraud Checks on Admin Orders]** para `Yes`.

1. Defina o **[!UICONTROL Bypass Fraud Protection Threshold]** para que o `Advanced Fraud Protection` as verificações são ignoradas quando o limite é atingido ou excedido.

   Deixar esse campo em branco desativa essa opção.

1. Se quiser que o sistema salve um arquivo de log de interações entre a loja e o Braintree, defina **[!UICONTROL Debug]** para `Yes`.

1. Para exigir que os clientes forneçam o código de segurança de três dígitos da parte traseira de um cartão de crédito, defina **[!UICONTROL CVV Verification]** para `Yes`.

   Se estiver usando a verificação CVV, habilite o AVS e/ou CVV no _Configurações/Processamento_ seção da sua conta Braintree.

1. Para enviar os itens de linha do carrinho para todos os métodos de pagamento, defina **[!UICONTROL Send Card Line Items]** para `Yes`.

1. Para **[!UICONTROL Credit Card Types]**, selecione cada cartão de crédito aceito pela loja como pagamento por meio do Braintree.

   Para selecionar vários tipos de placa, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Para **[!UICONTROL Sort Order]**, informe um número para determinar a sequência em que o Braintree aparece quando listado com outros métodos de pagamento durante a finalização da compra.

## Etapa 4: completar as configurações do webhook do Braintree

![Configurações de webhooks do Braintree](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Enable Webhook]** para `Yes` para ativar a funcionalidade webhook para proteção contra fraude, pagamentos ACH e métodos de pagamento locais.

1. Copie o URL no **[!UICONTROL Fraud Protection URL]** e adicione-o à sua conta Braintree como o _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >Este URL deve ser seguro e estar acessível publicamente.

1. Defina o **[!UICONTROL Fraud Protection Approve Order Status]** para determinar quando a proteção contra fraude é aprovada pelo Braintree.

   O status do pedido selecionado é atribuído ao pedido de Comércio.

1. Defina o **[!UICONTROL Fraud Protection Reject Order Status]** para determinar quando a proteção contra fraude é rejeitada pelo Braintree.

   O status do pedido selecionado é atribuído ao pedido de Comércio.

## Etapa 5: concluir as configurações específicas do país

1. Definir **[!UICONTROL Payment from Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de pagamento.
   - `Specific Countries` - Após escolher esta opção, o _[!UICONTROL Payment from Specific Countries]_é exibida. Mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada país na lista onde os clientes podem fazer compras na sua loja.

   ![Configurações específicas do país](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. Para configurar **[!UICONTROL Country Specific Credit Card Types]**:

   - Clique em **[!UICONTROL Add]**.

   - Defina o **[!UICONTROL Country]** e escolha cada **[!UICONTROL Allowed Credit Card Type]**.

   - Repita para identificar os cartões de crédito aceitos de cada país.

## Etapa 6: completar as configurações de ACH por Braintree

![ACH por Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. Para incluir ACH como uma opção de pagamento com Braintree, defina **[!UICONTROL Enable ACH Direct Debit]** para `Yes`.

1. Para **[!UICONTROL Sort Order]**, informe um número para determinar a sequência na qual a opção de pagamento Braintree ACH aparecerá quando listada com outras opções de pagamento durante o checkout.

## Etapa 7: conclua o [!UICONTROL Apple Pay] através das configurações de Braintree

![ApplePay por meio das configurações de Braintree](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. Para incluir [!DNL Apple Pay] como uma opção de pagamento com Braintree, defina **[!UICONTROL Enable ApplePay through Braintree]** para `Yes`.

   Verifique se [verifique o nome do domínio](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) em sua conta Braintree primeiro.

1. Definir **[!UICONTROL Payment Action]** a um dos seguintes:

   - `Authorize Only` - Aprova a compra e suspende os fundos. O valor não é sacado da conta bancária do cliente até que a venda seja _capturado_ pelo comerciante.
   - `Intent Sale` - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

1. Para **[!UICONTROL Merchant Name]**, insira o texto que especifica o rótulo exibido para os clientes na caixa de diálogo Pagamento do Apple.

1. Para **[!UICONTROL Sort Order]**, insira um número para determinar a sequência na qual [!DNL Apple Pay] opção de pagamento aparece quando listada com outras opções de pagamento durante a finalização da compra.

## Etapa 8: concluir as configurações para métodos de pagamento locais

1. Para incluir métodos de pagamento local como uma opção de pagamento com Braintree, defina **[!UICONTROL Enable Local Payment Methods]** para `Yes`.

1. Para **[!UICONTROL Title]**, insira o texto a ser usado para o rótulo que aparece na seção método de pagamento de finalização de compra (valor padrão: `Local Payments`).

1. Para **[!UICONTROL Allowed Payment Methods]**, selecione o método de pagamento local a ser ativado.

   Opções: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (ainda não suportado)

   ![Configurações de Métodos de pagamento locais](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >A extensão de Braintree agrupada não oferece suporte a todos os métodos de pagamento locais listados na [Documentação do desenvolvedor do Braintree](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Outros métodos de pagamento locais estão em desenvolvimento para serem compatíveis em versões futuras.

1. Para **[!UICONTROL Sort Order]**, informe um número para determinar a sequência em que o método de pagamento local será exibido quando listado com outras opções de pagamento durante a finalização da compra.

## Etapa 9: conclua o [!DNL Google Pay] através das configurações de Braintree

![Google Pay through Braintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. Para incluir [!DNL Google Pay] como uma opção de pagamento com Braintree, defina **[!UICONTROL Enable GooglePay Through Braintree]** para `Yes`.

1. Definir **[!UICONTROL Payment Action]** a um dos seguintes:

   - `Authorize Only` - Aprova a compra e suspende os fundos. O valor não é sacado da conta bancária do cliente até que a venda seja _capturado_ pelo comerciante.
   - `Intent Sale`  - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

1. Definir **[!UICONTROL Button Color]** para determinar a cor do [!DNL Google Pay] botão: `White` ou `Black`

1. Para **[!UICONTROL Merchant ID]**, digite sua ID do comerciante (fornecida pela Google).

1. Para **[!UICONTROL Accepted Cards]**, selecione os tipos de cartões que um cliente pode usar para fazer um pedido usando [!DNL Google Pay].

   Opções: `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. Para **[!UICONTROL Sort Order]**, insira um número para determinar a sequência na qual [!DNL Google Pay] é exibido quando listado com outras opções de pagamento durante a finalização da compra.

## Etapa 10: completar as configurações de Venmo até Braintree

1. Para incluir Venmo como uma opção de pagamento com Braintree, defina **[!UICONTROL Enable Venmo through Braintree]** para `Yes`.

   ![Venmo por Braintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Payment Action]** a um dos seguintes:

   - `Authorize Only` - Aprova a compra e suspende os fundos. O valor não é sacado da conta bancária do cliente até que a venda seja _capturado_ pelo comerciante.
   - `Intent Sale`  - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

1. Para **[!UICONTROL Sort Order]**, insira um número para determinar a sequência em que Venmo aparece quando listado com outras opções de pagamento durante o check-out.

## Etapa 11: Concluir o PayPal por meio das configurações de Braintree

![PayPal por meio de Configurações de Braintree](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. Para incluir o PayPal como uma opção de pagamento com Braintree, defina **[!UICONTROL Enable PayPal through Braintree]** para `Yes`.

1. Especifique seu PayPal através do método de pagamento Braintree:

   >[!NOTE]
   >
   >Ou **[!DNL PayPal Credit]** ou **[!DNL PayPal PayLater]** pode ser ativado. Ambos os métodos não podem ser ativados ao mesmo tempo.

   - Para incluir [!DNL PayPal Credit] como uma opção de pagamento com Braintree, defina **[!UICONTROL Enable PayPal Credit through Braintree]** para `Yes`.

     Quando **Habilitar PayPal por meio do Braintree** está definida como `Yes`, somente esse campo aparecerá.

     >[!NOTE]
     >
     >O PayPal Credit só está disponível nos Estados Unidos e no Reino Unido. O Crédito do PayPal estará desativado se o valor selecionado para o _[!UICONTROL Merchant Country]_o campo não está `US` ou `UK`.

   - Para incluir [!DNL PayPal PayLater] como uma opção de pagamento com Braintree, defina **[!UICONTROL Enable PayPal PayLater through Braintree]** para `Yes`.

     Quando **[!UICONTROL Enable PayPal PayLater through Braintree]** está definida como `Yes`, somente esse campo aparecerá.

     Você pode exibir mensagens do PayLater no seu site para ofertas, como _Pagamento em 3_, que permite que os clientes paguem com três pagamentos mensais sem juros. A integração Braintree pode exibir mensagens no site para promover esse recurso. Não é possível promover ofertas do PayLater com qualquer outro conteúdo, marketing ou material.

1. Para **[!UICONTROL Title]**, insira um título que identifique a opção Braintree payment by PayPal durante o check-out.

1. Definir **[!UICONTROL Vault Title]** para `Yes` para habilitar o uso de um cofre seguro para armazenar as informações de cartão de crédito dos clientes.

1. Para **[!UICONTROL Sort Order]**, digite um número para determinar a sequência na qual a opção de pagamento Braintree do PayPal aparece quando listada com outras opções de pagamento durante o check-out.

1. Para exibir seu nome de comerciante de forma diferente do que está definido em seu [configuração da loja](../getting-started/store-details.md#store-information), digite o nome no campo **[!UICONTROL Override Merchant Name]** como você deseja que ele apareça.

1. Definir **[!UICONTROL Payment Action]** a um dos seguintes:

   - `Authorize Only` - Aprova a compra e suspende os fundos. O valor não é sacado da conta bancária do cliente até que a venda seja _capturado_ pelo comerciante.
   - `Authorize and Capture` - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

1. Definir **[!UICONTROL Payment from Applicable Countries]** a um dos seguintes para transações Braintree processadas pelo PayPal:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de pagamento.
   - `Specific Countries` - Após escolher esta opção, o _[!UICONTROL Payment from Specific Countries]_é exibida. Mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada país na lista onde os clientes podem fazer compras na sua loja.

1. Para exigir que os clientes forneçam um endereço de faturamento, defina **[!UICONTROL Require Customer's Billing Address]** para `Yes`.

   >[!NOTE]
   >
   >Este recurso deve ser habilitado para sua conta pelo Suporte Técnico do PayPal.

1. Para salvar um arquivo de log das interações entre sua loja e o PayPal por meio do Braintree, defina **[!UICONTROL Debug]** para `Yes`.

1. Para exibir o botão PayPal no carrinho e na página do carrinho de compras, defina **[!UICONTROL Display on Shopping Cart]** para `Yes`.

## Etapa 12: definir as configurações de estilo

1. Para **[!UICONTROL Location]**, escolha onde as mensagens e os botões do PayPal são renderizados: `Mini-Cart and Cart Page`, `Checkout Page`ou `Product Page`

   ![Configurações de Estilo do PayPal](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

As opções e configurações desta seção variam de acordo com a configuração no _[!UICONTROL Location]_campo.

1. Definir **[!UICONTROL PayPal Button Type]** para um dos três tipos de botões: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

As opções e configurações desta seção variam de acordo com o tipo de botão selecionado no _[!UICONTROL PayPal Button Type]_campo.

1. Para mostrar o botão PayPal na vitrine do local selecionado, defina **[!UICONTROL Show PayPal Button]** para `Yes`.

1. Para **[!UICONTROL Button Label]**, selecione o rótulo do botão PayPal: `Paypal`, `Checkout`, `Buynow`ou `Pay`

1. Para **[!UICONTROL Color]**, selecione a cor do botão PayPal: `Blue`, `Black`, `Gold`ou `Silver`

1. Para **[!UICONTROL Shape]**, selecione a forma do botão PayPal: `Pill` ou `Rectangle`

1. Para **[!UICONTROL Size]**, selecione o tamanho do botão PayPal: `Medium`, `Large`ou `Responsive`

**[!UICONTROL PayLater Messaging]**

1. Para mostrar [!DNL PayLater] mensagens na loja no local selecionado, defina **[!UICONTROL Show PayLater Messaging]** para `Yes`.

   Essa mensagem inclui a exibição de [!DNL PayLater] mensagens para ofertas disponíveis ([restrições se aplicam](https://developer.paypal.com/docs/checkout/pay-later/us/)).

1. Para **[!UICONTROL Message Layout]**, selecione o [!DNL PayLater] layout de mensagem: `Text` ou `Flex`

1. Para **[!UICONTROL Logo]**, selecione o tipo de logotipo PayPal: `Inline`, `Primary`, `Alternative`ou `None`

1. Para **[!UICONTROL Logo Position]**, selecione a posição do logotipo do PayPal: `Left`, `Right`ou `Top`

1. Para **[!UICONTROL Text Color]**, selecione o [!DNL PayLater] cor do texto da mensagem: `Black`, `White`, `Monochrome`ou `Grayscale`

Quando essas opções são definidas, você pode visualizar os botões do PayPal e as mensagens do PayLater. Há controles que você pode usar para aplicar as configurações ou redefinir os valores:

- Para armazenar as configurações de estilo selecionadas para mensagens de botões e PayLater e aplicá-las ao local atual e ao tipo de botão atual, clique em **[!UICONTROL Apply]**.

- para armazenar as configurações de estilo selecionadas para botões e valores de mensagens do PayLater e aplicá-las a todos os tipos e locais de botões, clique em **[!UICONTROL Apply to All Buttons]**.

- Para retornar as configurações de estilo aos valores padrão recomendados para mensagens de botões e PayLater e aplicá-las a todos os tipos e locais de botões, clique em **[!UICONTROL Reset to Recommended Defaults]**.

## Etapa 13: Concluir as configurações de verificação 3D

1. Se você quiser adicionar uma etapa de verificação para clientes que usam cartões de crédito inscritos em um programa de verificação (como _Verificado pela VISA_), definir **[!UICONTROL 3D Secure Verification]** para `Yes`.

   Durante o processo, o valor da transação enviado para verificação é verificado em relação ao valor enviado para autorização.

2. Para sempre desafiar a solicitação do 3D Secure para todas as transações, defina **[!UICONTROL Always request 3DS]** para `Yes`.

3. Para **[!UICONTROL Threshold Amount]**, insira o valor mínimo do pedido necessário para acionar a verificação 3D.

4. Definir **[!UICONTROL Verify for Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de pagamento.
   - `Specific Countries` - Após escolher esta opção, o _[!UICONTROL Verify for Specific Countries]_é exibida. Mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada país na lista onde os clientes podem fazer compras na sua loja.

   ![Configurações de verificação 3D](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## Etapa 14: configurar os descritores dinâmicos de Braintree

Os descritores a seguir são usados para identificar compras em demonstrativos de cartão de crédito do cliente. Você pode reduzir o número de cobranças retroativas identificando claramente a empresa associada a cada compra. Se os descritores dinâmicos não estiverem ativados para sua conta, entre em contato com o suporte ao Braintree.

![Descritores dinâmicos](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. Insira o descritor dinâmico para o **[!UICONTROL Name]**, **[!UICONTROL Phone]**, e **[!UICONTROL URL]** de acordo com essas diretrizes:

   - **[!UICONTROL Name]** - Há duas partes no descritor de nome, separadas por um asterisco (*). Por exemplo:

     `company*myproduct`

     A primeira parte do descritor identifica a empresa ou o DBA e a segunda identifica o produto. O comprimento do `company` e `product` partes do descritor podem ser alocadas das seguintes maneiras, para um comprimento combinado de até 22 caracteres.

     **_Caracteres no descritor de nome_**

     _Opção 1:_ `Company` deve ter três caracteres, `Product` pode conter até 18 caracteres

     _Opção 2:_ `Company` deve ter sete caracteres, `Product` pode ter até 14 caracteres

     _Opção 3_: `Company` deve ter 12 caracteres, `Product` pode conter até nove caracteres

   - **[!UICONTROL Phone]** - O descritor de telefone deve ter entre 10 e 14 caracteres e pode incluir apenas números, traços, parênteses e pontos. Por exemplo:

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - O descritor de URL representa seu nome de domínio e pode ter até 13 caracteres. Por exemplo:

     `company.com`

1. Quando a configuração do Braintree estiver concluída, clique em **[!UICONTROL Save Config]**.

## Notas de atualização do 2.4

Antes de atualizar para o Commerce 2.4 a partir da versão 2.3, é recomendável que os comerciantes substituam a integração principal do Commerce Braintree pela extensão oficial do Braintree. [Commerce Marketplace](https://commercemarketplace.adobe.com/catalogsearch/result/?q=braintree). A partir do Adobe Commerce e Magento Open Source 2.4.0, a extensão Braintree está incluída na versão.

Se você estiver migrando para o Commerce 2.4.x de uma versão anterior à 2.4.0 que tenha a extensão Braintree do Marketplace instalada, será necessário desinstalar essa extensão (`paypal/module-braintree` ou `gene/module-braintree`) e atualizar qualquer personalização de código para usar o `PayPal_Braintree` namespace em vez de `Magento_Braintree`. As configurações da extensão principal do Commerce Braintree Payments agrupada e da extensão distribuída no Commerce Marketplace persistem e os pagamentos feitos com essas versões anteriores ainda podem ser capturados, anulados ou reembolsados normalmente.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
