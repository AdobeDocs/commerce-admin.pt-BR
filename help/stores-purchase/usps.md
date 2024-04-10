---
title: Serviço Postal dos Estados Unidos (USPS)
description: Saiba como configurar o USPS como transportadora de remessa para sua loja.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Serviço Postal dos Estados Unidos (USPS)

O Serviço Postal dos Estados Unidos é o serviço postal independente do governo dos Estados Unidos, oferecendo serviços de transporte nacional e internacional por terra e ar.

## Etapa 1: abrir uma conta de remessa USPS

Abra um [Ferramentas da Web da USPS][1] conta. Após concluir o processo de registro, você receberá sua ID de usuário e um URL para o servidor de teste USPS.

Também é possível abrir uma [Ferramentas da Web da USPS][1] conta. Após concluir o processo de registro, você receberá sua ID de usuário e um URL para o servidor de teste USPS. Para saber mais sobre as Ferramentas da Web do USPS, consulte as [Documentação técnica][2].

## Etapa 2: Habilitar USPS para sua loja

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Delivery Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL USPS]** seção.

   >[!NOTE]
   >
   >Se necessário, primeiro desmarque a opção **[!UICONTROL Use system value]** para alterar as configurações a seguir, conforme descrito.

1. Definir **[!UICONTROL Enabled for Checkout]** para `Yes`.

1. Se necessário, insira o **[!UICONTROL Gateway URL]** para acessar as taxas de envio do USPS.

   >[!IMPORTANT]
   >
   >A partir de 24 de junho de 2021, as Ferramentas da Web do USPS removerão o suporte para todos os endpoints HTTP não seguros. Após essa alteração, todas as solicitações da API de Ferramentas da Web que direcionem para um endpoint HTTP não seguro falharão. Verifique se o seu **[!UICONTROL Gateway URL]** O usa o ponto de extremidade HTTPS seguro.

   O campo é predefinido por padrão e normalmente não precisa ser alterado.

1. Insira um **[!UICONTROL Title]** para este método de envio que aparece durante a finalização da compra.

1. Insira o **[!UICONTROL User ID]** e **[!UICONTROL Password]** para sua conta USPS.

1. Definir **[!UICONTROL Mode]** a um dos seguintes:

   - `Development` - Executa o USPS em um ambiente de teste. Depois de executar o USPS em um ambiente de desenvolvimento, retorne mais tarde e defina o Modo como `Live`.
   - `Live` - Executa o USPS em um ambiente de produção ativo.

## Etapa 3: Preencha a descrição da embalagem

1. Para determinar como o pedido é gerenciado se for enviado como vários pacotes, defina **[!UICONTROL Packages Request Type]** a um dos seguintes:

   - `Divide to Equal Weight` - (Uma Solicitação) A entrega de vários pacotes pode ser enviada como uma solicitação se os pacotes forem divididos por peso igual.
   - `Use Origin Weight` - (Várias solicitações) Vários pacotes devem ser enviados como solicitações separadas se o peso de origem for usado como a base para o cálculo do custo de envio.

1. Definir **[!UICONTROL Container]** ao tipo de embalagem normalmente usado para enviar produtos encomendados para seu armazenamento.

1. Defina o **[!UICONTROL Size]** do pacote típico enviado de sua loja.

1. Definir **[!UICONTROL Machinable]** a um dos seguintes:

   - `Yes` - Se o pacote típico puder ser processado por uma máquina.
   - `No` - Se o pacote típico precisar ser processado manualmente.

1. Insira o **[!UICONTROL Maximum Package Weight]** de acordo com os requisitos do transportador.

   ![Configurações de empacotamento USPS](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Etapa 4: Configurar taxas de manuseio

A taxa de manuseio é opcional e aparece como uma taxa extra que é adicionada ao custo de envio da DHL. Se quiser incluir uma taxa de manuseio, faça o seguinte:

1. Definir **[!UICONTROL Calculate Handling Fee]** a um dos seguintes métodos:

   - `Fixed`
   - `Percent`

1. Para determinar como a taxa de manuseio é aplicada, defina **[!UICONTROL Handling Applied]** a um dos seguintes:

   - `Per Order`
   - `Per Package`

1. Insira o valor do **[!UICONTROL Handling Fee]** a cobrar.

   Para inserir uma porcentagem, use o formato decimal. Por exemplo, insira `0.25` para 25%.

   ![Taxa de manuseio de USPS](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Etapa 5: Especificar métodos permitidos e países aplicáveis

1. Para **[!UICONTROL Allowed Methods]**, escolha cada método de envio do USPS que estará disponível para seus clientes.

   Os métodos aparecem em USPS durante o check-out. Para selecionar vários métodos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Se quiser fornecer uma [Envio gratuito](shipping-free.md) através do USPS, defina as opções de envio gratuito:

   - Definir **[!UICONTROL Free Method]** para o método que deseja usar para frete grátis. Se você não quer oferecer frete grátis através de USPS, escolha `None`.

   - Para exigir uma quantia mínima da ordem que qualifique uma ordem para entrega gratuita com USPS, defina **[!UICONTROL Enable Free Shipping Threshold]** para `Enable`. Em seguida, insira o valor mínimo em **[!UICONTROL Free Shipping Amount Threshold]**.

1. Se necessário, altere o **[!UICONTROL Displayed Error Message]**.

   Essa caixa de texto é predefinida com uma mensagem padrão, mas você pode inserir uma mensagem diferente que você deseja exibir se o USPS ficar indisponível.

   ![Métodos permitidos pelo USPS](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Ship to Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de entrega.
   - `Specific Countries` - Ao escolher essa opção, a variável _Países específicos para envio_ é exibida. Selecione cada país na lista onde esse método de entrega pode ser usado.

   ![Países aplicáveis ao USPS](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Show Method if Not Applicable]** a um dos seguintes:

   - `Yes` - Lista todos os métodos de entrega USPS disponíveis durante a finalização da compra, incluindo métodos que não se aplicam à entrega.
   - `No` - Lista apenas os métodos de entrega do USPS que são aplicáveis à entrega.

1. Para criar um arquivo de log com os detalhes das remessas USPS feitas em sua loja, defina **[!UICONTROL Debug]** para `Yes`.

1. Para **[!UICONTROL Sort Order]**, digite um número para determinar a sequência em que a USPS aparece quando listada com outros métodos de delivery durante o checkout.

   `0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.

1. Clique em **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
