---
title: PayPal Payflow Pro
description: Saiba como configurar o PayPal Payflow Pro como uma solução de pagamento online em sua loja.
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2212'
ht-degree: 0%

---

# PayPal Payflow Pro

O gateway PayPal Payflow Pro, anteriormente conhecido como _Verisign_, está disponível para clientes dos Estados Unidos, Canadá, Austrália e Nova Zelândia. Ao contrário de outros métodos de pagamento PayPal, os comerciantes são cobrados uma taxa mensal fixa, além de uma taxa fixa para cada transação, independentemente do número.

![Check-out com PayPal](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>Requisitos do **PSD2:** <br/>
>A partir de 14 de setembro de 2019, os bancos europeus poderão recusar pagamentos que não atendam aos requisitos do [PSD2](../getting-started/compliance-payment-services-directive.md). Para estar em conformidade com o PSD2, o PayPal Payflow Pro deve ser integrado a um plug-in de terceiros. Para saber mais, consulte [Segurança 3D para Fluxo de Pagamento](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

## Requisitos

- [Conta Comercial do PayPal](https://www.paypal.com/webapps/mpp/how-to-sell-online) - O gateway PayPal Payflow Pro vincula a conta do comerciante no PayPal ao site do comerciante, atuando como uma conta de gateway e de comerciante.

- Se você gerenciar vários sites do Adobe Commerce e do Magento Open Source, deverá ter uma conta de comerciante do PayPal separada para cada site.

## Fluxo de trabalho do cliente

1. **O cliente vai ao check-out** - Durante o check-out, o cliente opta por pagar com o PayPal Payflow Pro e insere as informações de cartão de crédito. Os clientes não precisam ter contas pessoais do PayPal. No entanto, dependendo do país comerciante, os clientes também podem usar sua conta pessoal do PayPal para pagar o pedido.
1. **O cliente envia o pedido** - O cliente envia o pedido e as informações do pedido são enviadas ao PayPal para processamento. O cliente não sai da página de check-out do site.
1. **O PayPal conclui a transação**. Os pagamentos são aceitos no momento em que o pedido é feito. Dependendo da ação de pagamento especificada na configuração, uma ordem de venda ou uma ordem de venda e uma NFF serão criadas.

## Fluxo de trabalho de processamento de pedidos online

1. **O administrador envia uma fatura online** - O administrador de loja envia uma fatura online e, como resultado, uma transação e uma fatura correspondentes são criadas.
1. **PayPal recebe a transação** - As informações da ordem são enviadas para PayPal. Um registro da transação e uma fatura são gerados. Você pode exibir todas as transações do Payflow Pro Gateway em sua [conta de comerciante do PayPal](https://manager.paypal.com/).

>[!NOTE]
>
>Faturas parciais e reembolsos parciais não são suportados pelo PayPal Payflow Pro.

## Configurar sua conta do PayPal

1. Faça logon em sua [conta comercial do PayPal](https://manager.paypal.com/).

1. Configure as [Páginas de Check-out Hospedadas](https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager) usando o PayPal Manager com as seguintes configurações:

   - Em **[!UICONTROL Choose your settings]**, defina **[!UICONTROL Transaction Process Mode]** como `Live`.

   - Em **[!UICONTROL Display options on payment page]**, defina **Cancelar método de URL** como `POST`.

   - Em **[!UICONTROL Billing Information]**, marque as caixas de seleção do código de segurança do cartão **[!UICONTROL CSC]** para os campos obrigatórios e editáveis.

   - Em **[!UICONTROL Payment Confirmation]**, defina **[!UICONTROL Return URL Method]** como `POST`.

   - Em **[!UICONTROL Security Options]**, conclua as seguintes configurações:

      - **[!UICONTROL AVS]**: `No`
      - **[!UICONTROL CSC]**: `No`
      - **[!UICONTROL Enable Secure Token]**: `Yes`

   - Escolha **[!UICONTROL Customize]** e depois **[!UICONTROL Layout C]**.

     O layout C mostra apenas campos de cartão de crédito e débito, e pode ser emoldurado em seu site ou usado como um pop-up independente. O tamanho é fixado em 490 x 565 pixels, com espaço extra para mensagens de erro. Em alguns sistemas, essa configuração corrige um problema de redirecionamento transparente.

1. Quando as configurações estiverem concluídas, clique em **[!UICONTROL Save and Publish]**.

1. No menu do PayPal Manager, escolha **[!UICONTROL Account Administration]**.

1. Em **[!UICONTROL Manage Security]**, clique em **[!UICONTROL Transaction Settings]** e faça o seguinte:

   - Defina **[!UICONTROL Allow reference transactions]** como `Yes`.

   - Clique em **[!UICONTROL Confirm]**.

     >[!NOTE]
     >
     >Se você tiver vários sites do Commerce, deverá criar uma conta separada do PayPal Payments Advanced para cada um.

1. Configurar outro usuário (recomendado pelo PayPal):

   - Na segunda linha do menu principal, clique em **[!UICONTROL Manage Users]**.

   - Para adicionar outro usuário à conta, clique em **[!UICONTROL Add User]**. O link está localizado logo acima do título Gerenciar usuários.

   - Preencha os campos obrigatórios nas seguintes seções do formulário _[!UICONTROL Add User]_:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Clique em **[!UICONTROL Update]**.

1. Faça logout da sua conta do PayPal.

## Configurar PayPal Payflow Pro no Commerce

>[!TIP]
>
>Clique em **[!UICONTROL Save Config]** a qualquer momento para salvar seu progresso.

### Etapa 1: iniciar a configuração

Este método de configuração pressupõe que você tenha uma conta existente do PayPal.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Se a sua instalação do Commerce tiver vários sites, lojas ou modos de exibição, defina **[!UICONTROL Store View]** para o modo de exibição de loja onde deseja aplicar essa configuração.

1. Na seção _[!UICONTROL Merchant Location]_, selecione o **[!UICONTROL Merchant Country]**&#x200B;onde sua empresa está localizada.

   Esta configuração determina a seleção das Soluções do PayPal que aparecem na configuração.

   ![País do comerciante](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Expanda **[!UICONTROL PayPal Payment Gateways]** (se necessário) e clique em **[!UICONTROL Configure]** para **[!UICONTROL Payflow Pro]**.

   ![Configurar - Payflow Pro](./assets/payflow-pro.png){width="600" zoomable="yes"}

### Etapa 2: concluir as configurações necessárias do PayPal

![Configurações necessárias - PayPal Payflow Pro](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. (Opcional) Insira o **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Os endereços de email diferenciam maiúsculas de minúsculas. Para receber o pagamento, o endereço de email deve corresponder ao endereço de email especificado em sua conta de comerciante do PayPal.

1. Digite uma das credenciais a seguir que você usa para fazer logon em sua conta de comerciante do PayPal:

   - **[!UICONTROL Partner]** - Sua ID de parceiro do PayPal.
   - **[!UICONTROL User]** - Se você configurar um ou mais usuários adicionais na conta, esse valor será a ID do usuário autorizado a processar transações. No entanto, se você não tiver configurado usuários adicionais, **[!UICONTROL USER]** terá o mesmo valor que **[!UICONTROL Vendor]**.
   - **[!UICONTROL Vendor]** - Sua ID de logon de comerciante criada quando você se registrou na conta.

1. Digite o **[!UICONTROL Password]** que está associado à sua conta do PayPal.

1. Para executar transações de teste, defina **[!UICONTROL Test Mode]** como `Yes`.

   Ao testar a configuração em uma sandbox, use apenas [números de cartão de crédito](https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm) recomendados pelo PayPal. Quando estiver pronto para entrar na produção, volte para a configuração e defina o Modo de Teste como `No`.

1. Se o sistema usar um servidor proxy para estabelecer a conexão com o sistema PayPal, defina **[!UICONTROL Use Proxy]** como `Yes` e faça o seguinte:

   - Digite o endereço IP de **[!UICONTROL Proxy Host]**.

   - Insira o número da porta de **[!UICONTROL Proxy Port]**.

     Um proxy é usado quando o firewall do servidor impede o acesso direto ao servidor do PayPal. Nesse caso, um servidor de terceiros é usado para retransmitir o tráfego.

1. Defina **[!UICONTROL Enable this Solution]** como `Yes`.

1. Se você deseja oferecer o [Crédito do PayPal](paypal.md#paypal-credit-and-pay-later) aos seus clientes, defina o **[!UICONTROL Enable PayPal Credit]** como `Yes`.

1. Se você quiser armazenar com segurança os detalhes de pagamento/cartão de crédito do cliente, para que os clientes não precisem inserir novamente as informações de pagamento todas as vezes, defina **[!UICONTROL Vault Enabled]** como `Yes`.

### Etapa 3: Configurar Crédito do PayPal de Anúncio / Anunciar PayPal PayLater (opcional)

A partir da versão 2.4.3, o PayPal PayLater é compatível com implantações que incluem o PayPal. Esse recurso permite que os compradores paguem um pedido em prestações quinzenais em vez de pagar o valor total no momento da compra. A experiência do PayPal Credit está obsoleta.

Defina **[!UICONTROL Enable PayPal PayLater Experience]** como um dos seguintes:

- `Yes` - Para configurar Anunciar PayPal PayLater
- `No` - Para configurar o Crédito de Anúncio do PayPal

#### Anunciar Crédito do PayPal

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advertise PayPal Credit]**.

   ![Anunciar Crédito do PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Para obter as informações da sua conta, clique em **[!UICONTROL Get Publisher ID from PayPal]** e siga as instruções.

1. Insira seu **[!UICONTROL Publisher ID]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Home Page]**.

   ![Anunciar Configurações da Página Inicial de Crédito do PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Para colocar um banner na página, defina **[!UICONTROL Display]** como `Yes`.

1. Defina **[!UICONTROL Position]** como um dos seguintes:

   - `Header (center)`
   - `Sidebar (right)`

1. Defina **[!UICONTROL Size]** como um dos seguintes:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) as seções restantes e repita as etapas anteriores para as configurações de página inicial:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Anunciar PayPal PayLater

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advertise PayPal PayLater]**.

1. Defina **[!UICONTROL Enable PayPal PayLater]** como `Yes`.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Home Page]**.

   ![Anunciar Configurações da Página Inicial de Crédito do PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Para colocar um banner na página, defina **[!UICONTROL Display]** como `Yes`.

1. Defina **[!UICONTROL Position]** como um dos seguintes:

   - `Header (center)`
   - `Sidebar`

1. Defina **[!UICONTROL Style Layout]** como um dos seguintes:

   - `Text`
   - `Flex`

1. Somente para [!UICONTROL Style Layout] **[!UICONTROL Text]**, defina **[!UICONTROL Logo Type]** como um dos seguintes:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Somente para [!UICONTROL Style Layout] **[!UICONTROL Text]**, defina **[!UICONTROL Logo Position]** como um dos seguintes:

   - `Left`
   - `Right`
   - `Top`

1. Somente para [!UICONTROL Style Layout] **[!UICONTROL Text]**, defina **[!UICONTROL Text Color]** como um dos seguintes:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Somente para [!UICONTROL Style Layout] **[!UICONTROL Text]**, defina **[!UICONTROL Text Size]** como um dos seguintes:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Somente para [!UICONTROL Style Layout] **[!UICONTROL Flex]**, defina **[!UICONTROL Ratio]** como um dos seguintes:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Somente para [!UICONTROL Style Layout] **[!UICONTROL Flex]**, defina **[!UICONTROL Color]** como um dos seguintes:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) as seções restantes e repita as etapas anteriores:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Etapa 4: concluir as configurações básicas

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Basic Settings - PayPal Payflow Pro]**.

   ![Configurações Básicas - PayPal Payflow Pro_](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, insira um título que identifique PayPal Payflow Pro durante o check-out.

   É recomendável usar o título _Cartão de Débito ou Crédito_.

1. Se você oferecer vários métodos de pagamento, insira um número para **[!UICONTROL Sort Order]** para determinar a sequência em que o Payflow Pro aparece quando listado com os outros métodos de pagamento.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Defina **[!UICONTROL Payment Action]** como um dos seguintes:

   - `Authorization` - Aprova a compra e suspende os fundos. O valor não é sacado até que seja capturado pelo comerciante.
   - `Sale` - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

1. Para **[!UICONTROL Credit Card Settings]**, selecione os cartões de crédito que você aceita para pagamento em sua loja.

   Para selecionar várias placas, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada uma.

   >[!NOTE]
   >
   >American Express requer um acordo extra.

### Etapa 5: concluir as configurações avançadas

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advanced Settings]**.

   ![Configurações Avançadas - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Payment Applicable From]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` - Depois de escolher esta opção, a lista _[!UICONTROL Payment from Specific Countries]_&#x200B;é exibida. Mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada país na lista onde os clientes podem fazer compras na sua loja.

1. Para gravar comunicações com o sistema de pagamento no arquivo de log, defina **[!UICONTROL Debug Mode]** como `Yes`.

   >[!NOTE]
   >
   >De acordo com os padrões de segurança de dados do PCI, as informações de cartão de crédito não são gravadas no arquivo de registro.

1. Para habilitar a verificação de autenticidade do host, defina **[!UICONTROL Enable SSL Verification]** como `Yes`.

1. Para exigir que os clientes insiram um código CVV, defina **[!UICONTROL Require CVV Entry]** como `Yes`.

1. Preencha as seguintes seções, conforme necessário para sua loja:

   - [Configurações de CVV e AVS](#cvv-and-avs-settings)
   - [Configurações do relatório de liquidação](#settlement-report-settings)
   - [Configurações de experiência de front-end](#frontend-experience-settings)

#### Configurações de CVV e AVS

Para determinar quando uma transação deve ser rejeitada quando o Sistema de Verificação de Endereço identificar uma incompatibilidade, especifique como lidar com vários cenários.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL CVV and AVS Settings]**.

   ![Configurações de CVV e AVS - PayPal Payflow Pro](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. Para rejeitar uma transação com base em uma incompatibilidade de rua incompatível, defina **[!UICONTROL AVS Street Does Not Match]** como `Yes`.

1. Para rejeitar uma transação baseada em um CEP incompatível, defina **[!UICONTROL AVS Zip Does Not Match]** como `Yes`.

1. Para rejeitar uma transação com base no identificador de país incompatível, defina **[!UICONTROL International AVS Indicator Does Not Match]** como `Yes`.

1. Para rejeitar uma transação baseada em um código CVV incompatível, defina **[!UICONTROL International Card Security Code Does Not Match]** como `Yes`.

#### Configurações do relatório de liquidação

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Settlement Report Settings]**.

   ![Configurações do Relatório de Liquidação - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL SFTP Credentials]**, faça o seguinte:

   - Se você se inscreveu no servidor FTP seguro do PayPal, insira as seguintes credenciais de logon SFTP:

      - Logon
      - Senha

   - Para executar relatórios de teste antes de entrar em funcionamento com o Check-out expresso no site, defina **[!UICONTROL Sandbox Mode]** como `Yes`.

   - Insira o **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     O valor padrão é `reports.paypal.com`.

   - Insira o **[!UICONTROL Custom Path]** onde os relatórios são salvos.

     O valor padrão é `/ppreports/outgoing`.

1. Para gerar relatórios de acordo com um agendamento, conclua as configurações de **[!UICONTROL Scheduled Fetching]**:

   - Defina **[!UICONTROL Enable Automatic Fetching]** como `Yes`.

   - Defina **[!UICONTROL Schedule]** como um dos seguintes:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     O PayPal retém cada relatório por 45 dias.

   - Defina **[!UICONTROL Time of Day]** como hora, minuto e segundo quando quiser que os relatórios sejam gerados.

#### Configurações de experiência de front-end

Use as Configurações de experiência de front-end para escolher quais logotipos do PayPal aparecem em seu site e para personalizar a aparência das páginas do comerciante do PayPal.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Frontend Experience Settings]**.

   ![Configurações de Experiência de Front-end - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Selecione o **[!UICONTROL PayPal Product Logo]** que você deseja que apareça no bloco PayPal em sua loja.

   Os logotipos PayPal estão disponíveis em quatro estilos e dois tamanhos:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Para personalizar a aparência das páginas do comerciante do PayPal:

   - Digite o nome da **[!UICONTROL Page Style]** que você deseja aplicar às páginas de comerciante do PayPal:

      - `paypal` - Usa o estilo de página do PayPal.
      - `primary` - Usa o estilo de página identificado como _primário_ no perfil da conta.
      - `your_custom_value` - Usa um estilo de página de pagamento personalizado, que é especificado no perfil da conta.

   - Para **[!UICONTROL Header Image URL]**, insira a URL da imagem que você deseja que apareça no canto superior esquerdo da página de pagamento. O tamanho máximo do arquivo é de 750 pixels de largura por 90 pixels de altura.

     >[!NOTE]
     >
     >O PayPal recomenda que a imagem resida em um servidor seguro (https). Caso contrário, um navegador pode avisar que _a página contém itens seguros e não seguros_.

   - Para definir a cor das páginas, insira o código hexadecimal de seis caracteres, sem o símbolo `#`, para cada um dos seguintes itens:

      - **[!UICONTROL Header Background Color]** - Cor de fundo do cabeçalho da página de check-out.
      - **[!UICONTROL Header Border Color]** - Cor da borda de dois pixels ao redor do cabeçalho.
      - **[!UICONTROL Page Background Color]** - Cor de fundo da página de check-out e ao redor do cabeçalho e do formulário de pagamento.

### Etapa 6: completar as configurações básicas para PayPal Express Checkout

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Basic Settings - PayPal Express Checkout]**.

   ![Configurações Básicas de Check-out Expresso](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, insira um título que identifique este método de pagamento durante o check-out.

   É recomendável definir o título como _PayPal_ para cada exibição de loja.

1. Se você oferecer vários métodos de pagamento, insira um número para **[!UICONTROL Sort Order]** para determinar a sequência em que o Check-out do PayPal Express é exibido quando listado com os outros métodos de pagamento.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Defina **[!UICONTROL Payment Action]** como um dos seguintes:

   - `Authorization` - Aprova a compra e suspende os fundos. O valor não é retirado até ser _capturado_ pelo comerciante.
   - `Sale` - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

1. Para exibir o botão _[!UICONTROL Check out with PayPal]_&#x200B;na página do produto, defina **[!UICONTROL Display on Product Details Page]**&#x200B;como `Yes`.

### Etapa 7: completar as configurações avançadas para PayPal Express Checkout

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advanced Settings]**.

   ![Configuração Avançada de Check-out Expresso](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Display on Shopping Cart]** como `Yes`.

1. Defina **[!UICONTROL Payment Applicable From]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os países especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` - Depois de escolher esta opção, a lista _[!UICONTROL Payment from Specific Countries]_&#x200B;é exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada item.

1. Para gravar comunicações com o sistema de pagamento no arquivo de log, defina **[!UICONTROL Debug Mode]** como `Yes`.

   >[!NOTE]
   >
   >De acordo com os padrões de segurança de dados do PCI, as informações de cartão de crédito não são gravadas no arquivo de registro.

1. Para habilitar a verificação de autenticidade do host, defina **[!UICONTROL Enable SSL Verification]** como `Yes`.

1. Para exibir um resumo completo do pedido do cliente por item de linha do site do PayPal, defina **[!UICONTROL Transfer Cart Line Items]** como `Yes`.

1. Para permitir que o cliente conclua a transação no site do PayPal sem retornar ao seu armazenamento para Revisão do Pedido, defina **[!UICONTROL Skip Order Review Step]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Etapa 8: adicionar o Google reCAPTCHA

Para proteger melhor o checkout do PayPal Payflow Pro, ative o Google reCAPTCHA. Ele inclui opções para executar o reCAPTCHA usando uma interface clicável ou uma verificação invisível para validar o cliente. A opção invisível é recomendada para aumentar a conversão de vendas e proteger sua loja. Para obter detalhes, consulte [Google reCAPTCHA](../systems/security-google-recaptcha.md).
