---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods]'
description: Revise as configurações na página [!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods] do Administrador do Commerce.
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '3792'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![Taxa Uniforme](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-flat-rate) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site | Quando habilitada, a Taxa Uniforme aparece como uma opção na seção _Estimar Envio e Imposto_ do carrinho de compras e na seção _Envio_ durante o check-out. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O nome usado para este método de envio durante o check-out. |
| [!UICONTROL Method Name] | Exibição da loja | Um nome que descreve o método de cálculo usado para produzir uma estimativa de entrega. O nome do método aparece ao lado da taxa estimada calculada no carrinho de compras. O valor padrão é `Fixed`. |
| [!UICONTROL Type] | Site | Descreve o tipo de cálculo usado para determinar a taxa uniforme. Opções: <br/>**`None`**- Nenhum cálculo é usado. Define a Taxa Uniforme como zero, que é o equivalente ao frete grátis.<br/>**`Per Order`** - Cobra uma única taxa uniforme para o pedido inteiro. <br/>**`Per Item`**- Cobra uma taxa uniforme separada para cada item no carrinho. A taxa é multiplicada pelo número de itens no carrinho, mesmo que a quantidade total inclua uma combinação de itens diferentes. |
| [!UICONTROL Price] | Site | O preço que você cobra do cliente pela entrega com taxa uniforme. |
| [!UICONTROL Calculate Handling Fee] | Site | Determina como a taxa de manuseio é calculada, se incluída. Opções: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Site | Insira o valor a ser cobrado por uma taxa de manuseio, com base no método escolhido para calcular o valor. Por exemplo, se o encargo for baseado em uma taxa fixa, insira o valor como um valor decimal, como 4,90. No entanto, se a taxa de manuseio se basear em uma porcentagem do pedido, insira o valor como uma porcentagem. Por exemplo, se você estiver cobrando seis por cento do pedido, insira o valor como `.06`. |
| [!UICONTROL Displayed Error Message] | Exibição da loja | Uma mensagem que será exibida se um cliente escolher Taxa Uniforme, mas, por algum motivo, o método não estiver disponível. |
| [!UICONTROL Ship to Applicable Countries] | Site | Identifica os países nos quais você oferece remessa com Taxa Uniforme. Opções: <br/>**`All Allowed Countries`**- Clientes de qualquer país especificado na configuração da loja podem usar a remessa com Taxa Uniforme.<br/>**`Specific Countries`** - Clientes somente de países específicos podem usar o envio com Taxa Uniforme. |
| [!UICONTROL Ship to Specific Countries] | Site | Identifica cada país onde os clientes podem usar a entrega com Taxa Uniforme. |
| [!UICONTROL Show Method if Not Applicable] | Site | Determina se a Taxa única aparecerá como uma opção durante o check-out se o método não se aplicar à compra. Opções: `Yes` / `No` |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que a Taxa Uniforme é exibida quando listada com outros métodos de delivery durante a finalização da compra. |

{style="table-layout:auto"}

### [!UICONTROL Free Shipping]

![Envio gratuito](./assets/delivery-methods-free-shipping.png)<!-- zoom -->

<!-- [Free Shipping](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-free) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site | Quando ativado, o Frete gratuito é exibido como uma opção na seção Envio durante a finalização da compra. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O nome usado para este método de envio durante o check-out. |
| Nome do método | Exibição da loja | Um nome que descreve o método de cálculo usado para produzir uma estimativa de entrega. O nome do método aparece ao lado da taxa estimada calculada no carrinho de compras. O valor padrão é `Free`. |
| Valor Mínimo do Pedido | Site | A compra mínima necessária para aplicar o Frete Gratuito a um pedido. |
| Incluir Imposto no Valor | Site | Determina se o imposto está incluído no cálculo da Quantia Mínima da Ordem. Opções: <br/>**Sim** - O imposto é incluído ao calcular o valor Mínimo do Pedido (Subtotal + Imposto - Desconto).<br/>**Não** - O imposto não é incluído ao calcular o valor Mínimo da Ordem (Subtotal - Desconto). |
| Mensagem de erro exibida | Exibição da loja | Uma mensagem que é exibida se um cliente escolher Frete gratuito, mas por algum motivo o método não estiver disponível. |
| País de Destino Aplicável | Site | Identifica os países onde você oferece Frete Gratuito. Opções: <br/>**Todos os Países Permitidos** - Os clientes de qualquer país especificado na configuração da loja podem usar a Remessa Gratuita. <br/>**Países Específicos** - Os clientes somente de países específicos podem usar o Frete Gratuito. |
| Países específicos para envio | Site | Identifica cada país onde os clientes podem usar o Frete gratuito. |
| Mostrar método se não aplicável | Site | Determina se o Frete gratuito aparecerá como uma opção durante o check-out se o método não se aplicar à compra. Opções: `Yes` / `No` |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o Frete Gratuito é exibido quando listado com outros métodos de entrega durante a finalização da compra. |

{style="table-layout:auto"}

### [!UICONTROL Table Rates]

![Taxas de tabela](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-table-rate) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site | Quando ativado, a opção Taxas de tabela aparece na seção Estimar remessa e imposto do carrinho de compras e na seção Remessa durante a finalização da compra. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O nome usado para este método de envio durante o check-out. |
| Nome do método | Exibição da loja | Um nome que descreve o método de cálculo usado para produzir uma estimativa de entrega. O nome do método aparece ao lado da taxa estimada calculada no carrinho de compras. O valor padrão é `Table Rate`. |
| [!UICONTROL Condition] | Site | Determina a condição em que o cálculo é baseado. O formato do arquivo CSV que é carregado é específico para cada condição. Opções: `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | Site | Determina se os produtos virtuais que não precisam ser enviados estão incluídos nos cálculos de preço de Taxa de Tabela. |
| [!UICONTROL Calculate Handling Fee] | Site | Determina como a taxa de manuseio é calculada, se incluída. Opções: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Site | O valor de qualquer taxa adicionada ao encargo de remessa para cobrir as despesas de manuseio da remessa. Insira o valor como um decimal. Por exemplo, se a taxa for baseada em uma porcentagem, insira 0,06 em vez de 6%. Para um valor fixo, insira `6.00`. |
| [!UICONTROL Displayed Error Message] | Exibição da loja | Uma mensagem que será exibida se um cliente escolher Taxas de tabela, mas por algum motivo o método não estiver disponível. |
| [!UICONTROL Ship to Applicable Countries] | Site | Identifica os países nos quais você oferece entrega com Taxa de Tabela. Opções: <br/>**`All Allowed Countries`**- Clientes de qualquer país especificado na configuração da loja podem usar a remessa com Taxa de Tabela.<br/>**`Specific Countries`** - Clientes somente de países específicos podem usar o envio com Taxa de Tabela. |
| [!UICONTROL Ship to Specific Countries] | Site | Identifica cada país onde os clientes podem usar a entrega com Taxa de Tabela. |
| [!UICONTROL Show Method if Not Applicable] | Site | Determina se as Taxas de tabela aparecem como uma opção durante o check-out se o método não se aplicar à compra. Opções: `Yes` / `No` |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que as Taxas de tabela aparecem quando listadas com outros métodos de delivery durante a finalização da compra. |

{style="table-layout:auto"}

### [!UICONTROL In-Store Delivery]

![Entrega na loja](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-in-store-delivery) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site | Quando habilitada, a entrega na loja pode aparecer como uma opção na seção _Estimar Envio e Imposto_ do carrinho de compras e na seção _Envio_ durante o check-out. Opções: `Yes` / `No` |
| [!UICONTROL Method Name] | Exibição da loja | Um nome que identifica o recurso de retirada na loja como um método de remessa. Esse valor é exibido como o rótulo de uma guia na parte superior da página de finalização de remessa e na tabela de métodos de envio disponíveis na parte inferior da mesma página. O valor padrão é `In-store Delivery`. |
| [!UICONTROL Title] | Exibição da loja | O nome usado para este método de envio durante o check-out. |
| [!UICONTROL Price] | Site | O preço que você cobra do cliente por uma coleta na loja. |
| [!UICONTROL Search Radius] | Site | O raio, em km, a ser usado ao pesquisar locais de coleta. |
| [!UICONTROL Displayed Error Message] | Exibição da loja | Uma mensagem que é exibida quando um cliente seleciona a retirada na loja, mas o método de entrega não está disponível. |

{style="table-layout:auto"}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

![Configurações da conta REST UPS](./assets/delivery-methods-ups1.png)<!-- zoom -->

![Configurações de Conta XML UPS](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS REST Account Settings]https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | Site | Determina se o no-break está disponível para os clientes como um método de envio durante o checkout. Opções: `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | Site | Determina se a UPS está disponível aos clientes como um método de envio para uma RMA. Opções: `Yes` / `No` |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | Exibição da loja | Especifica que a conta do United Parcel Service está ativa. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O nome usado para este método de envio durante o check-out. |
| _[!UICONTROL UPS REST Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Site | Para o serviço UPS REST, exibe os seguintes URLs necessários para transmitir dados JSON: URL de gateway, URL de rastreamento, URL de envio. Use os endpoints de Sandbox ou Produção de acordo com a configuração da Conta dinâmica. |
| [!UICONTROL Mode] | Site | Determina o modo de transmissão usado para os dados enviados para o sistema UPS. Opções: <br/>**`Development`**- O UPS não verifica se os dados recebidos do servidor do Commerce são enviados por SSL.<br/>**`Live`** - O no-break verifica se os dados recebidos do servidor do Commerce são enviados por uma camada de soquete seguro (SSL). |
| ID de usuário | Site | ID do cliente da conta do despachante da UPS. |
| [!UICONTROL Origin of the Shipment] | Site | (Somente no-break REST) O país ou região de onde a entrega do produto é originada. |
| [!UICONTROL Password] | Exibição da loja | Segredo do cliente da conta do despachante da UPS. |

{style="table-layout:auto"}

![Informações do Pacote UPS](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information]https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | Site | (Somente UPS REST) Ativa/desativa taxas especiais, de acordo com seu contrato com a UPS. Opções: `Yes` / `No` |
| [!UICONTROL Packages Request Type] | Site | Determina como o peso é calculado para remessas com vários pacotes. Opções: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | Site | (Somente UPS REST) O Número do Remetente UPS de seis caracteres é necessário para referência para usar taxas negociadas. |
| [!UICONTROL Container] | Site | Define o tipo de contêiner usado para empacotar remessas. Opções: `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | Site | Define a unidade de medida padrão para o peso do produto na loja. Consulte [Peso dimensional](../../stores-purchase/carriers.md#dimensional-weight) para obter mais informações. |
| [!UICONTROL Tracking URL] | Site | (Somente no-break REST) O URL do no-break usado para rastrear pacotes. Use `https://onlinetools.ups.com/api/track` para produção OU `https://wwwcie.ups.com/api/track` para configuração de sandbox. |
| [!UICONTROL Destination Type] | Site | Define o tipo de destino da remessa padrão. Opções: `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | Site | Define o peso máximo que um pacote pode ter, conforme especificado pelo UPS. Se os produtos solicitados excederem o peso máximo do pacote, essa opção de envio não estará disponível. De acordo com o [UPS.com](https://www.ups.com/us/en/global.page), os pacotes não podem exceder 70 kg (150 lb). Consulte a sua transportadora para verificar o peso máximo. |
| [!UICONTROL Pickup Method] | Site | Define o método de coleta UPS. Opções: `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | Site | Define o peso mínimo que um pacote pode ter, conforme especificado pelo UPS. Se o peso dos produtos solicitados for menor que o peso mínimo da embalagem, essa opção de envio não estará disponível. Para verificar o peso mínimo, verifique com a transportadora. |
| [!UICONTROL Calculate Handling Fee] | Site | Define o método de cálculo da taxa de manuseio de material para remessa com taxa de tabela. Opções: <br>**`Fixed`**- A taxa de manuseio é fixa.<br>**`Percent`** - Taxa de manuseio aplicada como porcentagem do valor do pedido. |
| [!UICONTROL Handling Applied] | Site | Especifica se a taxa de manuseio é aplicada a cada pedido ou a cada pacote dentro de um pedido. |
| [!UICONTROL Handling Fee] | Site | Define o manuseio incluído com o preço da taxa de remessa. A taxa de manuseio pode ser definida como um valor fixo ou uma porcentagem. <br/><br/>**_Observação:_**&#x200B;se você digitar um valor percentual, use o formato decimal `0.25` para 25%. |

{style="table-layout:auto"}

![Métodos permitidos UPS](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods]https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Site | Especifica os métodos permitidos de envio UPS oferecidos aos clientes. As taxas de remessa são calculadas com base no método de remessa selecionado. |
| [!UICONTROL Free Method] | Site | Identifica o método usado para o método de envio gratuito por meio do UPS. Para desativar o frete grátis, escolha &quot;Nenhum&quot;. <br/><br/>**_Observação:_**&#x200B;este método é semelhante ao [Envio gratuito](../../stores-purchase/shipping-free.md) básico, no entanto, ele aparece como uma opção de envio UPS durante o check-out. |
| [!UICONTROL Free Shipping Amount Threshold] | Site | Determina se o frete gratuito é aplicado quando a quantidade do pedido atinge o limite de frete gratuito. Opções: `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | Site | Define o valor total mínimo que um pedido deve atingir para se qualificar para remessa gratuita. |
| [!UICONTROL Displayed Error Message] | Exibição da loja | A mensagem de erro que é exibida quando este método de envio não está disponível por algum motivo. |

{style="table-layout:auto"}

![Países e Outras Configurações Aplicáveis ao UPS](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings]https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site | Especifica quais clientes do país têm permissão para usar esse método de envio. Opções: <br/>**`All Allowed Countries`**- Clientes de todos os [países](../../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar este método de envio.<br/>**`Specific Countries`** - Depois de escolher esta opção, a lista [!UICONTROL Ship to Specific Countries] é exibida. Selecione cada país na lista onde este método de envio pode ser usado. |
| [!UICONTROL Show Method if Not Applicable] | Site | Determina se a UPS sempre aparece como uma opção de envio durante o check-out. Opções: <br/>**`Yes`**- UPS sempre aparece como uma opção de envio durante o check-out, mesmo se não for aplicável ao pedido.<br/>**`No`** - UPS aparece como uma opção de envio durante o check-out somente se aplicável ao pedido. (Por exemplo, se o peso do pedido exceder a quantidade máxima de peso.) |
| [!UICONTROL Debug] | Site | Especifica se as transmissões de dados entre seu armazenamento e o no-break estão registradas no sistema para depuração. A menos que haja um problema que deva ser rastreado e registrado, esta opção deve ser definida como `No`. |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o UPS aparece quando listado com outros métodos de delivery durante o checkout. Digite `0` no início da lista. |

{style="table-layout:auto"}

### [!UICONTROL USPS]

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| Ativado para check-out | Site | Determina se o USPS estará disponível aos clientes como um método de envio durante o checkout. Opções: `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Site | O URL usado para conectar ao sistema USPS para recuperar dinamicamente as taxas de envio. |
| [!UICONTROL Secure Gateway URL] | Site | O URL seguro usado para conectar ao sistema USPS em uma SSL (Secure Socket Layer) para recuperar dinamicamente as taxas de envio. |
| [!UICONTROL Title] | Exibição da loja | O título dessa opção de envio como exibido no checkout do carrinho de compras. |
| [!UICONTROL User ID] | Site | Sua ID de usuário da conta da transportadora USPS. |
| [!UICONTROL Password] | Site | Sua senha da conta do carregador USPS. |
| [!UICONTROL Mode] | Site | Determina o modo de transmissão usado para dados enviados ao sistema USPS. As opções incluem: <br/>**`Development`**- O USPS não verifica se os dados recebidos do servidor do Commerce são enviados por SSL.<br/>**`Live`** - O USPS verifica se os dados recebidos do servidor do Commerce são enviados por uma camada de soquete seguro (SSL). |

{style="table-layout:auto"}

![Configurações de empacotamento da USPS](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Site | Determina como o peso é calculado para remessas com vários pacotes. Opções: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | Site | Define o tipo de contêiner usado para empacotar remessas. Opções: `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` / Não retangular |
| [!UICONTROL Size] | Site | Define a opção Size para o tamanho típico do pacote de remessa. Essa opção afeta o cálculo da taxa de envio. Opções: `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | Site | Especifica se o pacote pode ser processado por computador. Essa opção afeta o cálculo da taxa de envio. |
| [!UICONTROL Maximum Package Weight] | Site | Define o peso máximo que um pacote pode ter, conforme especificado pela USPS. Se os produtos solicitados excederem o peso máximo do pacote, essa opção de envio não estará disponível. |

{style="table-layout:auto"}

![Configurações da Taxa de Manuseio de USPS](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Site | Define o método de cálculo da taxa de manuseio de material para remessa com taxa de tabela. Opções: <br/>**`Fixed`**- A taxa de manuseio é fixa.<br/>**`Percent`** - Taxa de manuseio aplicada como porcentagem do valor do pedido. |
| [!UICONTROL Handling Applied] | Site | Especifica se a taxa de manuseio é aplicada a cada pedido ou a cada pacote dentro de um pedido. |
| [!UICONTROL Handling Fee] | Site | Define o manuseio incluído com o preço da taxa de remessa. A taxa de manuseio pode ser definida como um valor fixo ou uma porcentagem. <br/><br/>**_Observação:_**&#x200B;ao digitar um valor percentual, use o formato decimal `0.25` para 25%. |

{style="table-layout:auto"}

![Métodos permitidos pela USPS](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Site | Especifica os métodos permitidos de envio de USPS oferecidos aos clientes. As taxas de remessa são calculadas com base no método de remessa selecionado. |
| [!UICONTROL Free Method] | Site | Define o método de envio gratuito por meio do USPS, ou pode ser desativado selecionando `None`. <br/><br/>**_Observação:_**&#x200B;este método de envio é semelhante ao método de envio gratuito de sua loja, no entanto, ele é listado como uma opção de envio USPS e identificado como envio USPS. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Site | Define o valor mínimo da ordem que deve ser atendido para se qualificar para remessa gratuita. |
| [!UICONTROL Displayed Error Message] | Exibição da loja | A mensagem de erro que aparece quando o USPS não está disponível por algum motivo. |

{style="table-layout:auto"}

![Países Aplicáveis ao USPS](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site | Especifica os países onde os pedidos podem ser enviados. Opções: <br/>**`All Allowed Countries`**- Clientes de todos os [países](../../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar este método de envio.<br/>**`Specific Countries`** - Depois de escolher esta opção, a lista [!UICONTROL Ship to Specific Countries] é exibida. Selecione cada país na lista onde este método de envio pode ser usado. |
| [!UICONTROL Show Method if Not Applicable] | Site | Controla a exibição do envio de USPS durante o check-out. Opções: <br/>**`Yes`**- USPS sempre aparece como uma opção de envio durante o check-out, mesmo se não for aplicável ao pedido.<br/>**`No`** - USPS aparece como uma opção de envio durante o check-out somente se aplicável ao pedido (ou seja, o peso do pedido excede o valor de peso máximo). |
| [!UICONTROL Debug] | Site | Determina se um log de transmissões de dados entre seu armazenamento e a USPS é mantido pelo sistema para depuração. A menos que haja um problema que deva ser rastreado e registrado, esta opção deve ser definida como `No`. |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o USPS aparece quando listado com outros métodos de delivery durante o checkout. Digite `0` no início da lista. |

{style="table-layout:auto"}

### [!UICONTROL FedEx]

<!-- [FedEx Account Settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/fedex) -->

#### Configurações de conta do FedEx

![Configurações de Conta do FedEx](./assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|-------|------ |-----------------------------------------------------------------------------|
| [!UICONTROL Enabled for Checkout] | Site | Determina se o FedEx está disponível para os clientes como um método de envio durante o check-out. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O título dessa opção de envio como exibido no checkout do carrinho de compras. |
| [!UICONTROL Account ID] | Site | A ID da sua conta FedEx. |
| [!UICONTROL Api Key] | Site | Sua chave de API da conta FedEx. |
| [!UICONTROL Secret Key] | Site | Sua chave secreta da API da conta FedEx. |
| [!UICONTROL Sandbox Mode] | Site | Para executar transações FedEx em um ambiente de teste, defina o Modo Sandbox como `Yes`. Opções: `Yes` / `No`. |
| [!UICONTROL Web-Services URL] | Site | O URL necessário depende da configuração do Modo de sandbox. Opções: <br/>**`Production`**- A URL para acessar os serviços Web FedEx quando o armazenamento estiver ativo.<br/>**`Sandbox`** - A URL para acessar o ambiente de teste dos serviços Web FedEx. |

{style="table-layout:auto"}

#### Configurações de empacotamento de FedEx

![Empacotamento de FedEx](./assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Pickup Type] | Site | Na lista, selecione o método de retirada: <br/>**`DropOff at Fedex Location`**- (Padrão) Indica que você entrega remessas em sua estação FedEx local.<br/>**`Contact Fedex to Schedule`** - Indica que você contatou o FedEx para solicitar uma retirada. <br/>**`Use Scheduled Pickup`**- Indica que a remessa foi retirada como parte de uma retirada regular agendada.<br/>**`On Call`** - Indica que a coleta está agendada ao chamar FedEx. <br/>**`Package Return Program`**- Indica que a remessa foi recebida pelo Programa de Devoluções de Pacotes Terrestres do FedEx.<br/>**`Regular Stop`** - Indica que a remessa foi retirada na programação de coleta regular. <br/>**`Tag`**- Indica que a retirada da remessa é específica para uma solicitação de retirada de etiqueta expressa ou de chamada em terra. Isso é aplicável somente para uma etiqueta de remessa de devolução. |
| [!UICONTROL Packages Request Type] | Site | Determina como o peso é calculado para remessas com vários pacotes. Opções: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | Site | Na lista, selecione o tipo de contêiner que normalmente é usado para empacotar produtos solicitados da loja. |
| [!UICONTROL Weight Unit] | Site | A unidade usada para peso do pacote. Opções: `Pounds` (padrão) / `Kilograms` |
| [!UICONTROL Maximum Package Weight] | Site | O padrão para o FedEx é 150 libras. Consulte sua transportadora para obter o peso máximo suportado. O uso do valor padrão é recomendado, a menos que você tenha acordos especiais com o FedEx. |

{style="table-layout:auto"}

#### Configurações de taxa de manuseio de FedEx

![Taxa de Manuseio de FedEx](./assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Calculate Handling Fee] | Site | Determina o método usado para calcular taxas de manuseio. Opções: `Fixed Fee` / `Percentage` <br/><br/>**_Observação:_**&#x200B;A taxa de tratamento é opcional e aparece como um encargo extra que é adicionado ao custo de envio da FedEx. |
| [!UICONTROL Handling Applied] | Site | Determina como as taxas de manuseio são aplicadas. Opções: `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | Site | Especifica o valor cobrado como uma taxa de manuseio, com base no método usado para calcular o valor. Se o encargo for baseado em uma taxa fixa, insira o valor em formato decimal, como `4.90`. Se a taxa de manuseio for baseada em uma porcentagem do pedido, insira o valor como uma porcentagem. Por exemplo, para cobrar seis por cento do pedido, insira o valor como `.06`. |

{style="table-layout:auto"}

#### Métodos de delivery FedEx

![Métodos de entrega FedEx](./assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Residential Delivery] | Site | Defina como um dos seguintes, dependendo se você vende B2C (Business-to-Consumer) ou B2B (Business-to-Business): <br/>**`Yes`**- Para entregas B2C<br/>**`No`** - Para entregas B2B |
| [!UICONTROL Allowed Methods] | Site | Na lista, selecione os métodos de entrega que você suporta. Os métodos dependem da sua conta FedEx, da frequência e do tamanho das suas remessas e se você permite remessas internacionais. Como comerciante, você pode decidir oferecer apenas frete terrestre. |
| [!UICONTROL Hub ID] | Site | Uma ID fornecida pelo FedEx usada com o método [!DNL Smart Post]. |
| [!UICONTROL Free Method] | Site | Na lista, selecione o método de envio que você prefere usar para ofertas de frete gratuito. <br/><br/>**_Observação:_**&#x200B;este método de envio é semelhante ao método de envio gratuito normal, no entanto, ele está listado nas opções de envio do FedEx e é identificado como envio do FedEx. |
| [!UICONTROL Free Shipping Amount Threshold] | Site | Determina se um valor de pedido mínimo é necessário para frete grátis. Opções: <br/>**`Enable`**- Habilita o envio gratuito do FedEx para pedidos que atendem ao valor mínimo.<br/>**`Disable`** - Desabilita o envio gratuito do FedEx com pedido mínimo. |
| [!UICONTROL Free Shipping Amount Threshold] | Site | Especifica o valor mínimo da ordem que é necessário para frete grátis. |
| [!UICONTROL Displayed Error Message] | Exibição da loja | A mensagem que aparece quando o FedEx não está disponível por algum motivo. Você pode usar a mensagem padrão ou inserir outra. |

{style="table-layout:auto"}

#### Configurações de país aplicáveis ao FedEx

![Países Aplicáveis ao FedEx](./assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Ship to Applicable Countries] | Site | Indica os países para os quais seus clientes podem enviar por FedEx. Opções: <br/>**`All Allowed Countries`**- Clientes de todos os [países](../../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar este método de envio.<br/>**`Specific Countries`** - Depois de escolher esta opção, a lista [!UICONTROL Ship to Specific Countries] é exibida. Selecione cada país na lista onde este método de envio pode ser usado. |
| [!UICONTROL Ship to Specific Countries] | Site | Indica os países específicos para os quais seus clientes podem enviar por FedEx. |
| [!UICONTROL Debug] | Site | Determina se um log de transmissões de dados entre seu armazenamento e o FedEx é mantido pelo sistema para depuração. A menos que haja um problema que deva ser rastreado e registrado, esta opção deve ser definida como `No`. |
| [!UICONTROL Show Method if Not Applicable] | Site | Determina quando o FedEx aparece como um método de envio durante o check-out. Opções: <br/>**`Yes`**- A opção de envio FedEx é exibida na lista de métodos de entrega, independentemente do pedido se qualificar para usá-lo.<br/>**`No`** - A opção de envio FedEx não será exibida na lista de métodos de entrega se não for aplicável ao pedido (por exemplo, se o peso do pedido exceder o valor máximo de peso). |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que o FedEx aparece quando listado com outros métodos de delivery durante o checkout. Digite `0` no início da lista. |

{style="table-layout:auto"}

### [!UICONTROL DHL]

![Configurações de conta da DHL](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Site | Determina se a DHL está disponível para os clientes como um método de envio durante o checkout. Opções: `Yes` / `No` |
| [!UICONTROL Title] | Exibição da loja | O título deste método de envio como exibido durante a finalização da compra. |
| [!UICONTROL Gateway URL] | Site | Normalmente, você pode aceitar o URL do Gateway padrão. No entanto, se a DHL tiver fornecido um URL alternativo, insira o valor nesse campo. |
| [!UICONTROL Access ID] | Site | ID de acesso da sua conta de despachante DHL. |
| [!UICONTROL Password] | Site | Sua senha da conta do carregador da DHL. |
| [!UICONTROL Account Number] | Site | Seu número de conta da DHL. |

{style="table-layout:auto"}

![Configurações do Pacote DHL](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Site | A taxa de manuseio é opcional e aparece como uma taxa extra adicionada ao custo de envio da DHL. Na lista, selecione o método que deseja usar para calcular as taxas de manuseio. Opções: Taxa Fixa / Porcentagem. |
| [!UICONTROL Handling Applied] | Site | Na lista, selecione como deseja que as taxas de tratamento sejam aplicadas. Opções: `Per Order` / `Per Package` |
| Taxa de manuseio | Site | Insira o valor a ser cobrado por uma taxa de manuseio, com base no método escolhido para calcular o valor. Por exemplo, se o encargo for baseado em uma taxa fixa, insira o valor como um valor decimal, como `4.90`. No entanto, se a taxa de manuseio se basear em uma porcentagem do pedido, insira o valor como uma porcentagem. Por exemplo, se você estiver cobrando seis por cento do pedido, insira o valor como `.06`. |
| [!UICONTROL Divide Order Weight] | Exibição da loja | Determina se o peso de um pedido acima de 70 kg pode ser dividido em unidades menores para garantir um encargo de envio preciso. Opções: `Yes` / `No` |
| [!UICONTROL Weight Unit] | Exibição da loja | Determina a unidade de medida do peso usada nos cálculos de remessa. Opções: `Pounds` / `Kilograms` |
| [!UICONTROL Size] | Exibição da loja | Determina o tamanho do pacote. Opções: <br/>**`Regular`**- Os pacotes enviados estão em conformidade com os métodos de embalagem padrão da DHL. Na lista [!UICONTROL Allowed Methods], selecione cada método de empacotamento usado para enviar produtos da sua loja.<br/>**`Specific`** - Se os pacotes enviados tiverem dimensões personalizadas, conclua o seguinte: [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{style="table-layout:auto"}

![Métodos permitidos pela DHL](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Site | Na lista, selecione cada método de entrega que você suporta. |
| [!UICONTROL Ready Time] | Site | Especifica quando o pacote estará pronto para retirada (em horas) após o envio de um pedido. |
| [!UICONTROL Displayed Error Message] | Exibição da loja | Essa mensagem aparece quando a DHL fica indisponível por qualquer motivo. Você pode usar a mensagem padrão ou inserir sua própria mensagem. |
| [!UICONTROL Free Method] |  | Este método de envio é semelhante ao método de envio gratuito regular, no entanto, ele está listado nas opções de envio da DHL e é identificado como envio da DHL. Na lista, selecione o método de envio que você prefere usar para ofertas de frete gratuito. |
| [!UICONTROL Free Shipping with Minimum Order Amount] | Site | Defina como um dos seguintes: <br/>**`Enable`**- Para permitir o envio gratuito da DHL para pedidos que atendam ao valor mínimo.<br/>**`Disable`** - Não oferecer frete DHL gratuito com pedido mínimo. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Site | Se você habilitar [!UICONTROL Free Shipping with Minimum Order], insira o valor mínimo do pedido no campo. |

{style="table-layout:auto"}

![Países aplicáveis da DHL](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site | Especifica quais clientes do país têm permissão para usar esse método de envio. Opções: <br/>**Todos os Países Permitidos** - Todos os países permitidos são aplicáveis para usar o método de envio gratuito. Os Países Permitidos estão especificados na página de configuração [!UICONTROL General]. <br/>**Países Específicos** - Limita esta opção de remessa aos países especificados na lista Remeter para Países Específicos. |
| [!UICONTROL Ship to Specific Countries] | Site | Especifica os países para onde as remessas da DHL podem ser enviadas. A lista de países selecionada será usada se `Specific Countries` for selecionada na opção [!UICONTROL Ship to Applicable Countries]. |
| [!UICONTROL Show Method if Not Applicable] | Site | Determina quando a DHL aparece como um método de envio durante o check-out. Opções: <br/>**`Yes`**- A DHL sempre aparece como uma opção de envio durante o check-out, mesmo se não for aplicável ao pedido.<br/>**`No`** - A DHL aparece como uma opção de envio durante o check-out somente se aplicável ao pedido (ou seja, o peso do pedido excede a quantidade máxima de peso). |
| [!UICONTROL Debug] | Site | Cria um arquivo de log com informações de erro. |
| [!UICONTROL Sort Order] | Site | Um número que determina a ordem em que a DHL aparece quando listada com outros métodos de delivery durante o checkout. Para colocá-lo no início da lista, digite `0`. |

{style="table-layout:auto"}
