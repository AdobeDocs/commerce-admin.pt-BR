---
title: FedEx
description: Saiba como configurar o FedEx como uma transportadora de remessa para sua loja.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---

# FedEx

A FedEx é uma das maiores empresas de serviços de transporte marítimo do mundo, fornecendo serviços de transporte aéreo, de carga e terrestre com vários níveis de prioridade.

![Opções de envio do FedEx na finalização da compra](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>O FedEx pode usar [peso dimensional](carriers.md#dimensional-weight) para determinar algumas taxas de envio. No entanto, o Adobe Commerce e o Magento Open Source suportam apenas o cálculo de custos de envio baseado em peso.

## Etapa 1: Registrar-se para produção dos serviços Web FedEx

A [Conta de comerciante da FedEx][1] e o registro para o FedEx Web Services Production Access é obrigatório. Depois de criar uma conta FedEx, leia a página de informações da conta de produção e clique no link _Obter Chave De Produção_ link na parte inferior da página para se registrar e obter uma chave.

>[!NOTE]
>
>Certifique-se de copiar ou anotar a chave de autenticação. É necessário configurar o FedEx nas configurações de envio do Commerce.

## Etapa 2: Ativar o FedEx para sua loja

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Delivery Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL FedEx]** seção.

1. Definir **[!UICONTROL Enabled for Checkout]** para `Yes`.

1. Para **[!UICONTROL Title]**, insira um título que identifique o método de envio FedEx durante o check-out.

1. Insira as seguintes informações da sua conta FedEx:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. Se você configurou uma sandbox do FedEx e deseja trabalhar no ambiente de teste, defina **[!UICONTROL Sandbox Mode]** para `Yes`.

   >[!NOTE]
   >
   >Lembre-se de definir o Modo de sandbox como `No` quando você estiver pronto para oferecer FedEx como um método de envio para seus clientes.

   ![Configurações da conta FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Etapa 3: Descrição do pacote e taxas de manuseio

1. Definir **[!UICONTROL Pickup Type]** ao método de retirada usado para remessas.

   - `DropOff at Fedex Location` - (Padrão) Indica que você entrega remessas em sua estação FedEx local.
   - `Contact Fedex to Schedule` - Indica que você deve entrar em contato com a FedEx para solicitar uma coleta.
   - `Use Scheduled Pickup` - Indica que a remessa foi retirada como parte de uma retirada regular programada.
   - `On Call` - Indica que a retirada está agendada ao chamar o FedEx.
   - `Package Return Program` - Indica que a remessa foi retirada pelo Programa de Devoluções de Pacotes Terrestres da FedEx.
   - `Regular Stop` - Indica que a remessa foi retirada na programação de coleta regular.
   - `Tag` - Indica que a retirada da remessa é específica para uma solicitação de retirada de etiqueta expressa ou de chamada em terra. Isso é aplicável somente para uma etiqueta de remessa de devolução.

1. Para **[!UICONTROL Packages Request Type]**, selecione o tipo de solicitação que melhor descreve sua preferência ao dividir uma ordem em várias entregas:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Para **[!UICONTROL Packaging]**, selecione o tipo de embalagem FedEx que você geralmente usa para enviar produtos de sua loja.

1. Definir **[!UICONTROL Weight Unit]** para a unidade de medida usada no seu local.

   - `Pounds`
   - `Kilograms`

1. Insira o **[!UICONTROL Maximum Package Weight]** permitido para remessas FedEx.

   O peso máximo padrão do FedEx é de 150 lb. Consulte sua transportadora para obter mais informações. O valor padrão é recomendado, a menos que você tenha feito acordos especiais com o FedEx. Consulte [Peso dimensional](carriers.md#dimensional-weight) para obter mais informações.

   ![Configurações do pacote FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configure as opções de taxa de manuseio de acordo com suas necessidades.

   A taxa de tratamento é opcional e não é visível durante o check-out. Se quiser incluir uma taxa de manuseio, faça o seguinte:

   - Definir **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - Para **[!UICONTROL Handling Applied]**, escolha um dos seguintes métodos para gerenciar taxas de manuseio:

      - `Per Order`
      - `Per Package`

   - Insira o **[!UICONTROL Handling Fee]** como uma `fixed` montante ou `percentage`, dependendo do método de cálculo.

1. Definir **[!UICONTROL Residential Delivery]** para um dos seguintes, dependendo se você vende B2C (Business-to-Consumer) ou B2B (Business-to-Business).

   - `Yes` - Para entregas residenciais B2C.
   - `No` - Para entregas residenciais B2B.

   ![Configurações da taxa de manuseio de FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Etapa 4: Métodos permitidos e países aplicáveis

1. Definir **[!UICONTROL Allowed Methods]** para cada método de entrega que você deseja oferecer.

   Ao escolher métodos, considere sua conta FedEx, a frequência e o tamanho de suas remessas e se você permitir remessas internacionais. Você pode oferecer quantos métodos quiser, como:

   - A Europa é a primeira prioridade
   - Opções de dia de entrega: Frete de 1 dia, Frete de 2 dias, 2 dias, AM de 2 dias, Frete de 3 dias
   - Opções domésticas - Economizador expresso, terra, primeiro, durante a noite, entrega em casa, padrão durante a noite
   - Opções internacionais-Economia Internacional, Intl Economia Frete, Internacional Primeiro, Terreno Internacional, Internacional, Prioridade Intl
   - Opções de prioridade - Frete, Prioridade noite
   - Smart Post-If oferecendo o método Smart Post (insira o **ID do Hub**)
   - Opções de frete - Frete, Frete Nacional

1. Se quiser fornecer uma [Envio gratuito](shipping-free.md) através da FedEx, defina as opções de envio gratuito.

   - Definir **[!UICONTROL Free Method]** para o método que deseja usar para frete grátis. Se você não quer oferecer frete grátis através de FedEx, escolha `None`.

   - Para exigir um valor de pedido mínimo que qualifique um pedido de frete gratuito com o FedEx, defina **[!UICONTROL Enable Free Shipping Threshold]** para `Enable`. Em seguida, insira o valor mínimo em **[!UICONTROL Free Shipping Amount Threshold]**.

   Essa configuração é semelhante à do método de envio gratuito padrão, mas é exibida na seção FedEx durante a finalização da compra, para que os clientes saibam qual método é usado para seu pedido.

1. Se necessário, altere o **[!UICONTROL Displayed Error Message]**.

   Essa caixa de texto é predefinida com uma mensagem padrão, mas você pode inserir uma mensagem diferente que deseja exibir se o FedEx não estiver disponível.

   ![Métodos de delivery permitidos pelo FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de entrega.

   - `Specific Countries` - Ao escolher essa opção, a variável _Países específicos para envio_ é exibida. Selecione cada país na lista onde esse método de entrega pode ser usado.

1. Se quiser manter um log de toda a comunicação entre o armazenamento e o sistema FedEx, defina **[!UICONTROL Debug]** para `Yes`.

1. Definir **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Mostra todos os métodos de envio FedEx para os clientes, independentemente da disponibilidade.
   - `No` - Mostra apenas os métodos de envio FedEx que se aplicam ao pedido.

1. Para **[!UICONTROL Sort Order]**, insira um número para determinar a sequência em que o FedEx aparece quando listado com outros métodos de delivery durante o checkout.

   `0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.

1. Clique em **[!UICONTROL Save Config]**.

   ![Países aplicáveis à FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>O Commerce sempre declara o preço do pedido completo para o FedEx ao calcular os encargos de envio. Esse comportamento não pode ser alterado.

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
