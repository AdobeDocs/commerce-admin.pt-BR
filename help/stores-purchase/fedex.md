---
title: FedEx
description: Saiba como configurar o FedEx como uma transportadora de remessa para sua loja.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: ad5da1d77b63bf6bcc0227a5c467e369b7bb8d89
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# FedEx

A FedEx é uma das maiores empresas de serviços de transporte marítimo do mundo, fornecendo serviços de transporte aéreo, de carga e terrestre com vários níveis de prioridade.

![Opções de Envio do FedEx na Finalização da Compra](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>A FedEx pode usar [peso](carriers.md#dimensional-weight) dimensionais para determinar algumas taxas de envio. No entanto, Adobe Systems Comércio e Magento Open Source suportam apenas peso cálculo de custo de envio baseado em peso.

## Etapa 1: Registrar-se na produção de serviços web da FedEx

Um comerciante FedEx conta e registro para acesso de produção de serviços web FedEx é necessário. Depois de criar uma conta FedEx, leia as informações de conta de produção página e clique _na link Obter chave_ de produção na parte inferior do página para registrar e obter uma chave.

>[!NOTE]
>
>Certifique-se de copiar ou gravar a chave de autenticação. É necessário configurar o FedEx nas configurações de envio Comércio.

## Etapa 2: Ativar o FedEx para sua loja

1. Na barra lateral do __ Administrador, vá até **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Delivery Methods]**.

1. Expanda ![a expansão seletor](../assets/icon-display-expand.png) **[!UICONTROL FedEx]** seção.

1. Defina **[!UICONTROL Enabled for Checkout]** como `Yes`.

1. Para **[!UICONTROL Title]**, insira um título que identifique o método de envio FedEx durante o check-out.

1. Insira as seguintes informações da sua conta FedEx:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. Se você tiver credenciais de API de rastreamento separadas, ative a seguinte configuração:

   - **[!UICONTROL Enable Tracking API credentials]**

1. Insira as seguintes informações da sua conta FedEx:

   - **[!UICONTROL Tracking API Key]**
   - **[!UICONTROL Tracking API Secret Key]**

1. Se você tiver configurado uma sandbox fedex e quiser trabalhar no ambiente de teste, defina **[!UICONTROL Sandbox Mode]** como `Yes`.

   >[!NOTE]
   >
   >Lembre-se de definir o Modo Sandbox para `No` quando estiver pronto para oferta FedEx como um método de envio para seus clientes.

   ![Configurações da conta FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Etapa 3: Descrição do pacote e taxas de manipulação

1. Defina **[!UICONTROL Pickup Type]** para o método de retirada usado para remessas.

   - `DropOff at Fedex Location` - (Padrão) Indica que você entrega remessas em sua estação FedEx local.
   - `Contact Fedex to Schedule` - Indica que você contatou o FedEx para solicitar uma retirada.
   - `Use Scheduled Pickup` - Indica que o carregamento foi captado como parte de uma coleta agendada regular.
   - `On Call` Indica que a coleta está agendada ligando para a FedEx.
   - `Package Return Program` - Indica que a remessa foi captada pelo Programa de devoluções do Pacote Base do FedEx.
   - `Regular Stop` - Indica que o carregamento foi pego na programação normal de coleta.
   - `Tag` - Indica que a coleta de carregamento é específica de uma chamada do Express tag ou Ground tag solicitação. Isso é aplicável somente para um rótulo de envio de retorno.

1. Em **[!UICONTROL Packages Request Type]** seguida, selecione o tipo de solicitação que melhor descreve sua preferência ao dividir um solicitar em vários envios:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Para **[!UICONTROL Packaging]**, selecione o tipo de pacote FedEx que você normalmente usa para enviar produtos do seu armazenamento.

1. Defina **[!UICONTROL Weight Unit]** para a unidade de medida usada no seu local.

   - `Pounds`
   - `Kilograms`

1. Insira os **[!UICONTROL Maximum Package Weight]** envios permitidos para FedEx.

   O peso máximo padrão da FedEx é de 150 lbs. Consulte sua operadora de transporte para obter mais informações. O valor padrão é recomendado, a menos que você tenha feito acordos especiais com a FedEx. Consulte [Peso dimensional](carriers.md#dimensional-weight) para obter mais informações.

   ![Configurações do Pacote FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configure as opções de taxa de manuseio de acordo com suas necessidades.

   A taxa de manuseio é opcional e não fica visível durante o check-out. Se quiser incluir uma taxa de manipulação, faça o seguinte:

   - Defina **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - Para **[!UICONTROL Handling Applied]**, escolha um dos seguintes métodos para gerenciar as taxas de manipulação:

      - `Per Order`
      - `Per Package`

   - Insira o **[!UICONTROL Handling Fee]** como um valor de `fixed` ou `percentage`, dependendo do método de cálculo.

1. Defina **[!UICONTROL Residential Delivery]** como um dos seguintes, dependendo se você vende B2C (Business-to-Consumer) ou B2B (Business-to-Business).

   - `Yes` - Para entregas B2C residenciais.
   - `No` - Para entregas B2B residenciais.

   ![Configurações da Taxa de Manuseio de FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Etapa 4: métodos permitidos e países aplicáveis

1. Defina **[!UICONTROL Allowed Methods]** para cada método de envio que deseja oferta.

   Ao escolher métodos, considere sua conta FedEx, a frequência e o tamanho de seus envios e se você permitir envios internacionais. Você pode oferta quantos métodos desejar, como:

   - Prioridade da Europa
   - Opções de dia de entrega: 1 Frete de dia, 2 dias de frete, 2 dias, 2 dias am, 3 dias de frete
   - Opções domésticas - Economizador expresso, terra, primeiro, durante a noite, entrega em casa, padrão durante a noite
   - Opções internacionais-Economia Internacional, Intl Economia Frete, Internacional Primeiro, Terreno Internacional, Internacional, Prioridade Intl
   - Opções de prioridade- Frete, Prioridade durante a noite
   - Smart Post–Se estiver oferecendo o método smart Post (insira a ID **do** Hub)
   - Opções de frete - Frete, Frete Nacional

1. Se você quiser fornecer uma [opção de envio gratuito](shipping-free.md) por meio da FedEx, defina as grátis opções de envio.

   - Defina **[!UICONTROL Free Method]** com o método que deseja usar para envio gratuito. Se você não quiser oferta grátis envio por Meio da FedEx, escolha `None`.

   - Para exigir um valor de pedido mínimo que qualifique um pedido para envio gratuito com FedEx, defina **[!UICONTROL Enable Free Shipping Threshold]** como `Enable`. Em seguida, insira o valor mínimo em **[!UICONTROL Free Shipping Amount Threshold]**.

   Essa configuração é semelhante à do método de envio gratuito padrão, mas é exibida na seção FedEx durante a finalização da compra, para que os clientes saibam qual método é usado para seu pedido.

1. Se necessário, altere o **[!UICONTROL Displayed Error Message]**.

   Essa caixa de texto é predefinida com uma mensagem padrão, mas você pode inserir uma mensagem diferente que deseja exibir se o FedEx ficar indisponível.

   ![Métodos de entrega permitidos para FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clientes de todos os [países especificados](../getting-started/store-details.md#country-options) na configuração de armazenamento podem usar esse método delivery.

   - `Specific Countries` - Ao escolher essa opção, o _navio para países específicos_ lista aparece. Selecione cada país no lista em que esse método delivery pode ser usado.

1. Se você quiser manter um registro de toda a comunicação entre a sua armazenamento e o sistema FedEx, defina **[!UICONTROL Debug]** como `Yes`.

1. Defina **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Mostra todos os métodos de envio fedex para os clientes, independentemente de sua disponibilidade.
   - `No` - Mostra apenas os métodos de envio fedex que se aplicam ao solicitar.

1. Para **[!UICONTROL Sort Order]**, insira um número para determinar a sequência em que a FedEx aparece quando listada com outros métodos delivery durante o check-out.

   `0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.

1. Clique em **[!UICONTROL Save Config]**.

   ![Países aplicáveis ao FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Comércio sempre declara o preço total do solicitar para a FedEx ao calcular as taxas de envio. Este comportamento não pode ser alterado.
