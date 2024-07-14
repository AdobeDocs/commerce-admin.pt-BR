---
title: DHL
description: Saiba como configurar a DHL como transportadora de remessa para sua loja.
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# DHL

A DHL oferece serviços internacionais integrados e soluções personalizadas voltadas para o cliente para gerenciamento e transporte de cartas, mercadorias e informações.

## Etapa 1: Ativar DHL

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Delivery Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL DHL]**.

   >[!NOTE]
   >
   >Se necessário, primeiro desmarque a caixa de seleção **[!UICONTROL Use system value]** para alterar as configurações a seguir, conforme descrito.

1. Defina **[!UICONTROL Enabled for Checkout]** como `Yes`.

1. Normalmente, você pode aceitar o **[!UICONTROL Gateway URL]** padrão.

   Se a DHL tiver fornecido um URL alternativo, insira esse valor nesse campo.

1. Use as credenciais fornecidas pela DHL para preencher os seguintes campos:

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![Configurações de conta da DHL](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## Etapa 2; Inserir descrição do pacote e taxa de manuseio

1. Na lista **[!UICONTROL Content Type]**, selecione a opção que melhor descreve o tipo de pacote que você envia:

   - `Documents`
   - `Non documents`

1. Configure as opções de taxa de manuseio de acordo com suas necessidades.

   A taxa de manuseio é opcional e aparece como uma taxa extra que é adicionada ao custo de envio da DHL. Se quiser incluir uma taxa de manuseio, faça o seguinte:

   - Para **[!UICONTROL Calculate Handling Fee]**, selecione o método que deseja usar para calcular as taxas de manuseio:

      - `Fixed`
      - `Percentage`

   - Para **[!UICONTROL Handling Applied]**, selecione como deseja aplicar as taxas de tratamento:

      - `Per Order`
      - `Per Package`

   - Para **[!UICONTROL Handling Fee]**, insira o valor a ser cobrado, com base no método escolhido para calcular o valor.

     Por exemplo, se o encargo for baseado em uma taxa fixa, insira o valor como um valor decimal, como `4.90`. No entanto, se a taxa de manuseio se basear em uma porcentagem do pedido, insira o valor como uma porcentagem. Por exemplo, se você estiver cobrando seis por cento do pedido, insira o valor como `.06`.

   - Para permitir que o peso total do pedido seja dividido e garantir um cálculo preciso dos encargos de remessa, defina **[!UICONTROL Divide Order Weight]** como `Yes`.

   - Defina o **[!UICONTROL Weight Unit]** do pacote para um dos seguintes:

      - `Pounds`
      - `Kilograms`

   - Defina o **[!UICONTROL Size]** de um pacote típico para um dos seguintes:

      - `Regular`
      - `Specific`

     Se você escolher `Specific`, insira o **[!UICONTROL Height]**, **[!UICONTROL Depth]** e **[!UICONTROL Width]** do pacote em centímetros.

   ![Configurações do Pacote DHL](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## Etapa 3: Especificar métodos de entrega permitidos

1. Para **[!UICONTROL Allowed Methods]**, escolha cada método que você deseja que esteja disponível para os clientes.

   Para selecionar vários métodos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

   Para exibir a lista correta de métodos de entrega, primeiro especifique o [País de Origem](../configuration-reference/sales/shipping-settings.md).

1. Para **[!UICONTROL Ready Time]**, insira o número de horas após o envio de um pedido em que um pacote está pronto para ser enviado.

1. Edite o **[!UICONTROL Displayed Error Message]** conforme necessário.

   Esta mensagem é exibida quando um método selecionado não está disponível.

1. Se você deseja fornecer uma opção de [Envio gratuito](shipping-free.md) por meio da DHL, defina as opções de envio gratuito.

   - Para **[!UICONTROL Free Method]**, escolha o método que você prefere usar para envio gratuito.

   - Conjunto **[!UICONTROL Free Shipping Amount Threshold]**:

     `Enable` - Se estiver oferecendo Remessa Gratuita com Pedido Mínimo, insira o **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable` - Não aplica frete DHL gratuito a nenhum pedido.

     Esta configuração é semelhante à do método padrão _Envio gratuito_, mas aparece na seção DHL para que os clientes saibam qual método é usado para seu pedido.

   - Para **[!UICONTROL Free Shipping Amount Threshold]**, insira o valor mínimo para um pedido para se qualificar para remessa gratuita.

     ![Métodos permitidos pela DHL](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## Etapa 4: especificar os países aplicáveis

1. Defina **[!UICONTROL Ship to Applicable Countries]** como um dos seguintes:

   - `All Allowed Countries`
   - `Specific Countries`

   Se estiver enviando para países específicos, selecione cada país na lista **[!UICONTROL Ship to Specific Countries]**.

1. Conjunto **[!UICONTROL Show Method if Not Applicable]**:

   `Yes` - Mostra a DHL como um método de envio durante o check-out, mesmo se não for aplicável ao pedido.

   `No` - Mostra a DHL como um método de envio durante o check-out somente se aplicável.

1. Para criar um arquivo de log com os detalhes das remessas DHL feitas de sua loja, defina **[!UICONTROL Debug]** como `Yes`.

1. Para **[!UICONTROL Sort Order]**, insira um número para determinar a sequência em que o DHL aparece quando listado com outros métodos de entrega durante o check-out.

   `0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.

1. Clique em **[!UICONTROL Save Config]**.

   ![Países aplicáveis da DHL](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
