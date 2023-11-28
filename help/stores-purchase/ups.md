---
title: UPS (United Parcel Service, serviço de encomendas unificado)
description: Saiba como configurar o UPS como uma transportadora para sua loja.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# UPS (United Parcel Service, serviço de encomendas unificado)

A United Parcel Service (UPS) oferece serviços de transporte nacional e internacional por terra e ar para mais de 220 países.

{{ups-api}}

>[!NOTE]
>
>UPS pode usar [peso dimensional](carriers.md#dimensional-weight) para determinar algumas taxas de envio. No entanto, o Adobe Commerce suporta apenas o cálculo de custo de envio com base em peso.

## Etapa 1: Abrir uma Conta de Entrega UPS

Para oferecer esse método de envio aos seus clientes, primeiro abra uma conta na UPS.

## Etapa 2: Habilitar UPS para sua loja

{{beta2-updates}}

1. No _Barra lateral de administração_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel à esquerda, em **[!UICONTROL Sales]**, escolha **[!UICONTROL Delivery Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL UPS]** seção.

1. Definir **[!UICONTROL Enabled for Checkout]** para `Yes`.

1. Para uma conta UPS XML (padrão), defina **[!UICONTROL UPS Type]** para `United Parcel Service XML` e faça o seguinte:

   - Insira suas credenciais de UPS: **[!UICONTROL User ID]**, **[!UICONTROL Access License Number]** (a conta UPS de 16 dígitos `Access Key`) e **[!UICONTROL Password]**

   - Definir **[!UICONTROL Mode]** para `Live` para enviar dados ao sistema de envio da UPS através de uma conexão segura. (O modo de desenvolvimento não envia dados por uma conexão segura.)

   - Verifique se **[!UICONTROL Gateway XML URL]** que é necessário para enviar solicitações por arquivo XML.

   - Definir **[!UICONTROL Origin of the Shipment]** para a região de origem da entrega.

   - Se você tiver taxas especiais com UPS, defina **[!UICONTROL Enable Negotiated Rates]** para `Yes` e insira o caractere de seis dígitos **[!UICONTROL Shipper Number]** atribuído a você pela UPS.

1. Para uma conta UPS padrão, defina **[!UICONTROL UPS Type]** para `United Parcel Service` e faça o seguinte:

   >[!NOTE]
   >
   >O tipo padrão United Parcel Service está agendado para desativação. Para novas configurações, você deve usar o padrão  `United Parcel Service XML` tipo. O tipo XML também é necessário para gerar [etiquetas de remessa](shipping-labels.md).

   - Definir **[!UICONTROL Live Account]** a um dos seguintes:

      - `Yes` - Executa UPS no modo de produção e oferece UPS como um método de envio para seus clientes.
      - `No` - Executa o no-break em um modo de teste.

   - No **[!UICONTROL Gateway URL]** insira o URL usado para calcular as taxas de envio UPS.

     >[!IMPORTANT]
     >
     >O UPS descontinuará o suporte para HTTP, que é usado no padrão atual (valor do sistema). Limpe a **[!UICONTROL Use system value]** e modifique o URL para usar HTTPS. Exemplo: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Para **[!UICONTROL Title]**, insira o nome desta opção de envio como deseja que ele seja exibido durante a finalização da compra.

   Por padrão, esse campo está definido como `United Parcel Service`.

   ![Ativar UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Etapa 3: completar a descrição do contêiner

1. Definir **[!UICONTROL Packages Request Type]** a um dos seguintes:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Para **[!UICONTROL Container]**, especifique o tipo de embalagem típico que é usado para a remessa:

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

1. Definir **[!UICONTROL Weight Unit]** ao sistema usado para medir o peso do produto.

   O sistema de peso suportado pela UPS varia de acordo com o país. Em caso de dúvida, pergunte ao UPS qual sistema de peso você deve usar. As opções incluem:

   - `LBS`
   - `KGS`

1. Definir **[!UICONTROL Destination Type]** a um dos seguintes:

   - `Residential` - A maioria de suas remessas são B2C (B2C).
   - `Commercial` - A maioria de suas remessas é B2B (B2B).

1. Insira o **[!UICONTROL Maximum Package Weight]** pelo transportador.

1. Definir **[!UICONTROL Pickup Method]** a um dos seguintes:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Insira o **[!UICONTROL Minimum Package Weight]** pelo transportador.

   ![Descrição do contêiner](./assets/ups2.png){width="600" zoomable="yes"}

## Etapa 4: Configurar taxas de manuseio

A taxa de manuseio é opcional e aparece como um custo extra que é adicionado ao custo de envio da UPS. Se quiser incluir uma taxa de manuseio, faça o seguinte:

1. Definir **[!UICONTROL Calculate Handling Fee]** a um dos seguintes métodos:

   - `Fixed`
   - `Percent`

1. Para determinar como a taxa de manuseio é aplicada, defina **[!UICONTROL Handling Applied]** a um dos seguintes:

   - `Per Order`
   - `Per Package`

1. Insira o valor do **[!UICONTROL Handling Fee]** a cobrar.

   Para inserir uma porcentagem, use o formato decimal. Por exemplo, insira `0.25` para 25%.

   ![Taxa de manuseio](./assets/ups3.png){width="600" zoomable="yes"}

## Etapa 5: Especificar métodos permitidos e países aplicáveis

1. Para **[!UICONTROL Allowed Methods]**, escolha cada método de envio UPS que estará disponível para seus clientes.

   Os métodos aparecem em UPS durante o check-out. Para selecionar vários métodos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Se quiser fornecer uma [Envio gratuito](shipping-free.md) através do UPS, defina as opções de envio gratuito:

   - Definir **[!UICONTROL Free Method]** para o método que deseja usar para frete grátis. Se você não quiser oferecer frete grátis através do UPS, escolha `None`.

   - Para exigir uma quantia mínima de ordem que qualifique uma ordem para entrega gratuita com UPS, defina **[!UICONTROL Enable Free Shipping Threshold]** para `Enable`. Em seguida, insira o valor mínimo em **[!UICONTROL Free Shipping Amount Threshold]**.

1. Se necessário, altere o **[!UICONTROL Displayed Error Message]**.

   Essa caixa de texto é predefinida com uma mensagem padrão, mas você pode inserir uma mensagem diferente que você deseja exibir se o UPS se tornar indisponível.

   ![Métodos permitidos](./assets/ups4.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Ship to Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de entrega.
   - `Specific Countries` - Ao escolher essa opção, a variável _Países específicos para envio_ é exibida. Selecione cada país na lista onde esse método de entrega pode ser usado.

1. Definir **[!UICONTROL Show Method if Not Applicable]** a um dos seguintes:

   - `Yes` - Lista todos os métodos de entrega UPS disponíveis durante a finalização da compra, incluindo métodos que não se aplicam à entrega.
   - `No` - Lista apenas os métodos de entrega UPS que são aplicáveis à entrega.

   ![Países aplicáveis](./assets/ups5.png){width="600" zoomable="yes"}

1. Para criar um arquivo de log com os detalhes das remessas UPS feitas de sua loja, defina **[!UICONTROL Debug]** para `Yes`.

1. Para **[!UICONTROL Sort Order]**, digite um número para determinar a sequência em que o UPS aparece quando listado com outros métodos de delivery durante o checkout.

   `0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.

1. Clique em **[!UICONTROL Save Config]**.

## Etapa 6: configurar endereço de origem da remessa

1. Verifique se o seu [Armazenar informações](../getting-started/store-details.md#store-information) está concluído.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e selecione **[!UICONTROL Shipping Settings]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Origin]** na página e configure o endereço de origem da remessa.

   ![Configuração de vendas - opções de endereço de origem da remessa](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.

>[!NOTE]
>
>O Commerce não declara o preço total do pedido à UPS ao calcular os encargos de remessa. Esse comportamento não pode ser alterado.
