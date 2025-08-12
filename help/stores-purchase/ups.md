---
title: UPS (United Parcel Service, serviço de encomendas unificado)
description: Saiba como configurar o UPS como uma transportadora para sua loja.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: a925827f2d939eeb9e6b3e57c023792ae358cbfc
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# UPS (United Parcel Service, serviço de encomendas unificado)

A United Parcel Service (UPS) oferece serviços de transporte nacional e internacional por terra e ar para mais de 220 países.

{{ups-api}}

>[!NOTE]
>
>A UPS pode usar [peso dimensional](carriers.md#dimensional-weight) para determinar algumas taxas de envio. No entanto, o Adobe Commerce suporta apenas o cálculo de custo de envio com base em peso.

## Etapa 1: Abrir uma Conta de Entrega UPS

Para oferecer esse método de envio aos seus clientes, primeiro abra uma conta UPS e conclua o aplicativo para obter um número de conta do Transportador. Consulte [Abrir uma conta gratuita do UPS](https://www.ups.com/us/en/business-solutions/open-an-account).

## Etapa 2: obter credenciais OAUTH do UPS

Siga as etapas no [Guia de Introdução às APIs do UPS](https://developer.ups.com/get-started) para obter as credenciais de API (ID do cliente e segredo do cliente) para habilitar a integração do UPS. Você deve criar um aplicativo UPS para obter as credenciais.

Ao definir as configurações da UPS no Administrador, use os valores de credencial para o `username` e `password`.

## Etapa 3: Habilitar UPS para sua loja

1. Na _barra lateral do administrador_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel à esquerda, em **[!UICONTROL Sales]**, escolha **[!UICONTROL Delivery Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL UPS]**.

1. Defina **[!UICONTROL Enabled for Checkout]** como `Yes`.

1. Para uma conta REST UPS (padrão), faça o seguinte:

   - Insira suas credenciais de UPS: UPS ClientID como **[!UICONTROL User ID]**, UPS Client Secret como **[!UICONTROL Password]**.

   - Defina **[!UICONTROL Mode]** como `Live` para enviar dados ao sistema de envio do UPS através de uma conexão segura. (O modo de desenvolvimento não envia dados por uma conexão segura.)

   - Verifique o **[!UICONTROL Gateway URL]** que é necessário para enviar solicitações. Use uma URL de sandbox (`https://wwwcie.ups.com/api/rating/`) para o modo de teste e uma URL de produção para solicitações ativas (`https://onlinetools.ups.com/api/rating/`). Certifique-se de usar os respectivos endpoints para cada solicitação com o host fornecido.

   - Verifique o **[!UICONTROL Tracking URL]** que é necessário para obter informações de rastreamento. Use uma URL de sandbox (`https://wwwcie.ups.com/api/track/`) para o modo de teste e uma URL de produção para solicitações ativas (`https://onlinetools.ups.com/api/track/`). Certifique-se de usar os respectivos endpoints para cada solicitação com o host fornecido.

   - Defina **[!UICONTROL Origin of the Shipment]** para a região de origem da remessa.

   - Se você tiver taxas especiais com UPS, defina **[!UICONTROL Enable Negotiated Rates]** como `Yes` e insira o **[!UICONTROL Shipper Number]** de seis dígitos atribuído a você pelo UPS.

   - Defina **[!UICONTROL Live Account]** como um dos seguintes:

      - `Yes` - Executa UPS no modo de produção e oferece UPS como um método de envio para seus clientes. Use os endpoints corretos em URL do gateway e URL de rastreamento.
      - `No` - Executa UPS em um modo de teste. Use os endpoints corretos em URL do gateway e URL de rastreamento.

   >[!NOTE]
   >
   >O tipo padrão United Parcel Service está agendado para desativação. Para novas configurações, use o tipo `United Parcel Service REST` padrão. O tipo REST também é necessário para gerar [rótulos de remessa](shipping-labels.md).<br/>
   >Para a versão 2.4.7, **[!UICONTROL UPS Type]** foi removido porque os tipos `UPS` e `UPS XML` estão agendados para substituição e `UPS REST` é o padrão. As APIs do United Parcel Service (UPS) usadas pela integração nativa do Adobe Commerce estão temporariamente obsoletas porque, no momento, ele não oferece suporte ao modelo de segurança OAuth 2.0.

   >[!IMPORTANT]
   >
   >O UPS descontinuará o suporte para HTTP, que é usado no padrão atual (valor do sistema). Desmarque a caixa de seleção **[!UICONTROL Use system value]** e modifique a URL para usar HTTPS. Exemplo: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Para **[!UICONTROL Title]**, insira o nome desta opção de remessa como deseja que ele apareça durante o check-out.

   Por padrão, este campo está definido como `United Parcel Service`.

   ![Habilitar UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Etapa 3: completar a descrição do contêiner

1. Defina **[!UICONTROL Packages Request Type]** como um dos seguintes:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Para **[!UICONTROL Container]**, especifique o tipo de embalagem típico que é usado para remessa:

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. Defina **[!UICONTROL Weight Unit]** para o sistema usado para medir o peso do produto.

   O sistema de peso suportado pela UPS varia de acordo com o país. Em caso de dúvida, pergunte ao UPS qual sistema de peso você deve usar. As opções incluem:

   - `LBS`
   - `KGS`

1. Defina **[!UICONTROL Destination Type]** como um dos seguintes:

   - `Residential` - A maioria de suas remessas é B2C (B2C).
   - `Commercial` - A maioria de suas remessas é B2B (B2B) de empresa para empresa.

1. Insira o **[!UICONTROL Maximum Package Weight]** permitido pela operadora.

1. Defina **[!UICONTROL Pickup Method]** como um dos seguintes:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Insira o **[!UICONTROL Minimum Package Weight]** permitido pela operadora.

   ![Descrição do contêiner](./assets/ups2.png){width="600" zoomable="yes"}

## Etapa 5: Configurar taxas de manuseio

A taxa de manuseio é opcional e aparece como um custo extra que é adicionado ao custo de envio da UPS. Se quiser incluir uma taxa de manuseio, faça o seguinte:

1. Defina **[!UICONTROL Calculate Handling Fee]** com um dos seguintes métodos:

   - `Fixed`
   - `Percent`

1. Para determinar como a taxa de manuseio de material é aplicada, defina **[!UICONTROL Handling Applied]** como uma das seguintes opções:

   - `Per Order`
   - `Per Package`

1. Insira o valor de **[!UICONTROL Handling Fee]** a ser cobrado.

   Para inserir uma porcentagem, use o formato decimal. Por exemplo, digite `0.25` para 25%.

   ![Taxa de Manuseio](./assets/ups3.png){width="600" zoomable="yes"}

## Etapa 6: especificar os métodos permitidos e os países aplicáveis

1. Para **[!UICONTROL Allowed Methods]**, escolha cada método de envio UPS que estará disponível para seus clientes.

   Os métodos aparecem em UPS durante o check-out. Para selecionar vários métodos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Se você deseja fornecer uma opção de [Envio gratuito](shipping-free.md) por meio do UPS, defina as opções de envio gratuito:

   - Defina **[!UICONTROL Free Method]** com o método que deseja usar para envio gratuito. Se você não quiser oferecer frete grátis por meio do UPS, escolha `None`.

   - Para exigir um valor de pedido mínimo que qualifique um pedido de remessa gratuita com UPS, defina **[!UICONTROL Enable Free Shipping Threshold]** como `Enable`. Em seguida, insira o valor mínimo em **[!UICONTROL Free Shipping Amount Threshold]**.

1. Se necessário, altere o **[!UICONTROL Displayed Error Message]**.

   Essa caixa de texto é predefinida com uma mensagem padrão, mas você pode inserir uma mensagem diferente que você deseja exibir se o UPS se tornar indisponível.

   ![Métodos permitidos](./assets/ups4.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Ship to Applicable Countries]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar este método de entrega.
   - `Specific Countries` - Ao escolher essa opção, a lista _Remeter para Países Específicos_ é exibida. Selecione cada país na lista onde esse método de entrega pode ser usado.

1. Defina **[!UICONTROL Show Method if Not Applicable]** como um dos seguintes:

   - `Yes` - Lista todos os métodos de envio UPS disponíveis durante o check-out, incluindo os métodos que não se aplicam à remessa.
   - `No` - Lista somente os métodos de envio UPS aplicáveis à remessa.

   ![Países aplicáveis](./assets/ups5.png){width="600" zoomable="yes"}

1. Para criar um arquivo de log com os detalhes das remessas UPS feitas de sua loja, defina **[!UICONTROL Debug]** como `Yes`.

1. Para **[!UICONTROL Sort Order]**, insira um número para determinar a sequência em que o UPS aparece quando listado com outros métodos de entrega durante o check-out.

   `0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.

1. Clique em **[!UICONTROL Save Config]**.

## Etapa 7: configurar endereço de origem da remessa

1. Verifique se as [Informações da Loja](../getting-started/store-details.md#store-information) foram concluídas.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e selecione **[!UICONTROL Shipping Settings]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Origin]** na página e configure o endereço de origem da remessa.

   ![Configuração de vendas - opções de endereço de origem da remessa](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.

>[!NOTE]
>
>A Commerce não declara o preço total do pedido à UPS ao calcular as despesas de envio. Esse comportamento não pode ser alterado.
