---
title: PayPal Payments Pro
description: Saiba como configurar o PayPal Payments Pro como uma solução de pagamento online em sua loja.
exl-id: 9cc5c3a6-d471-4198-85a2-c4cf9dfd378b
feature: Payments
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2257'
ht-degree: 0%

---

# PayPal Payments Pro

O [PayPal Payments Pro][3] oferece todos os benefícios de uma conta de comerciante e de um gateway de pagamento em um, além da capacidade de criar sua própria experiência de finalização de compra totalmente personalizada. O Check-out expresso do PayPal é ativado automaticamente com o PayPal Payments Pro, para que você possa acessar mais de 110 milhões de usuários ativos do PayPal.

![PayPal Payments Pro exibido no minicarrinho](./assets/storefront-mini-cart-payments-pro-racer-tank.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>Requisitos do **PSD2:** <br/>
>A partir de 14 de setembro de 2019, os bancos europeus poderão recusar pagamentos que não atendam aos requisitos do [PSD2](../getting-started/compliance-payment-services-directive.md). Para estar em conformidade com o PSD2, o PayPal Payments Pro deve ser integrado a um plug-in de terceiros.

>[!NOTE]
>
>Atualmente, o PayPal Payments Pro está disponível nos EUA, Reino Unido e Canadá.

## Requisitos

- [Conta de Comerciante do PayPal][1] (com Pagamentos Diretos ativados)

## Fluxo de trabalho de check-out

1. **O cliente vai ao check-out** - o cliente adiciona produtos ao carrinho e clica/toca _Prosseguir para o check-out_.|
1. **O cliente escolhe o método de pagamento** - Durante o check-out, o cliente escolhe a opção _Pagamento Direto do PayPal_ e insere as informações de cartão de crédito.
   - Se você estiver pagando com o PayPal Payments Pro, o cliente permanecerá em seu site durante o processo de finalização.
   - Se você estiver pagando com o Check-out do PayPal Express, o cliente será redirecionado para o site do PayPal para concluir a transação.

A pedido do cliente, o administrador da loja também pode criar um pedido do Administrador e processar a transação com o PayPal Payments Pro.

## Fluxo de trabalho de processamento de pedidos

1. **Pedido feito** - O pedido pode ser processado pelo Administrador da sua loja ou pela sua conta de comerciante do PayPal.

1. **[!UICONTROL Payment Action]** - A ação de pagamento especificada na configuração é aplicada ao pedido. As opções incluem:

   - **Autorizar** - a Commerce cria uma ordem de venda com o status _Processando_. Nesse caso, o montante a ser autorizado está pendente de aprovação.
   - **Venda** - a Commerce cria uma ordem de venda e uma fatura.
   - **Captura** - O PayPal transfere o valor do pedido do saldo do cliente, da conta bancária ou do cartão de crédito para a conta do comerciante.

1. **Faturamento** - Uma fatura é criada no Commerce depois que o PayPal envia uma mensagem de notificação de pagamento instantâneo à Commerce.

   Certifique-se de que as notificações de pagamento instantâneo estejam ativadas em sua conta de comerciante do PayPal.

   >[!NOTE]
   >
   >Se necessário, um pedido pode ser parcialmente faturado para uma quantidade especificada de produtos. Para cada NFF parcial enviada, uma transação de Captura separada com uma ID exclusiva torna-se disponível e uma NFF separada é gerada.

   As transações de pagamento somente com autorização são fechadas somente depois que a quantia total da ordem é capturada.

   Um pedido pode ser anulado on-line a qualquer momento até que o valor do pedido seja totalmente faturado.

1. **Devoluções** - Se o cliente devolver os produtos comprados e solicitar um reembolso, como no caso da captura do valor do pedido e da criação de faturas, você poderá criar um reembolso online pelo Administrador ou pela conta de comerciante do PayPal.

## Configurar sua conta do PayPal

Antes de configurar o PayPal Payments Pro no Commerce, você deve configurar sua conta de comerciante no site do PayPal.

1. Faça logon em sua [conta comercial do PayPal](https://manager.paypal.com/).

1. No menu do PayPal Manager, escolha **[!UICONTROL Service Settings]**.

1. Em **[!UICONTROL Hosted Checkout Pages]**, clique em **[!UICONTROL Set Up]**.

1. Em **[!UICONTROL Choose your settings]**, defina **[!UICONTROL Transaction Process Mode]** como `Live`.

1. Em **[!UICONTROL Display options on payment page]**, defina **[!UICONTROL Cancel URL Method]** como `POST`.

1. Em **[!UICONTROL Billing Information]**, marque as caixas de seleção do código de segurança do cartão **[!UICONTROL CSC]** para os campos obrigatórios e editáveis.

1. Em **[!UICONTROL Payment Confirmation]**, defina **[!UICONTROL Return URL Method]** como `POST`.

1. Em **[!UICONTROL Security Options]**, configure o seguinte:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. Clique em **[!UICONTROL Save Changes]**.

1. No menu _PayPal Manager_, escolha **[!UICONTROL Service Settings]** e, em _Páginas de Check-out Hospedadas_, escolha **[!UICONTROL Customize]**.

1. Escolha **[!UICONTROL Layout C]**.

   O layout C mostra apenas campos de cartão de crédito e débito, e pode ser emoldurado em seu site ou usado como um pop-up independente. O tamanho é fixado em 490 x 565 pixels, com espaço extra para mensagens de erro. Em alguns sistemas, essa configuração corrige um problema de redirecionamento transparente.

1. Clique em **[!UICONTROL Save and Publish]**.

1. No menu do PayPal Manager, escolha **[!UICONTROL Account Administration]**. Em **[!UICONTROL Manage Security]**, clique em **[!UICONTROL Transaction Settings]**.

1. Defina **[!UICONTROL Allow reference transactions]** como `Yes`.

1. Clique em **[!UICONTROL Confirm]**.

   >[!NOTE]
   >
   >Se você tiver vários sites do Commerce, deverá criar uma conta separada do PayPal Payments Pro para cada um.

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

## Configurar PayPal Payments Pro no Commerce

>[!NOTE]
>
>Você pode ter duas soluções PayPal ativas ao mesmo tempo: [Finalização Expressa do PayPal](paypal-express-checkout.md), além de qualquer uma das [soluções multifuncionais](paypal.md#paypal-all-in-one-payment-solutions). Se você alterar as soluções de pagamento, aquela usada anteriormente será automaticamente desabilitada.

>[!TIP]
>
>Clique em **[!UICONTROL Save Config]** a qualquer momento para salvar seu progresso.

### Etapa 1: iniciar a configuração

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Se a sua instalação do Commerce tiver vários sites, lojas ou modos de exibição, defina **[!UICONTROL Store View]** para o modo de exibição de loja onde deseja aplicar essa configuração.

1. Na seção _[!UICONTROL Merchant Location]_, selecione o **[!UICONTROL Merchant Country]**&#x200B;onde sua empresa está localizada.

   Esta configuração determina a seleção das Soluções do PayPal que aparecem na configuração.

   ![País do comerciante](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Expanda **[!UICONTROL PayPal All-in-One Payment Solution]** e clique em **[!UICONTROL Configure]** para **[!UICONTROL Payments Pro]**.

   ![PayPal Payments Pro](./assets/paypal-payments-pro.png){width="600" zoomable="yes"}

### Etapa 2: concluir as configurações necessárias do PayPal

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Payments Pro and Express Checkout]**.

   ![Configurações Necessárias do PayPal Payments Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-required.png){width="600" zoomable="yes"}

1. (Opcional) Insira o **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Os endereços de email diferenciam maiúsculas de minúsculas. Para receber o pagamento, o endereço de email deve corresponder ao endereço de email especificado em sua conta de comerciante do PayPal.

   Se você não tiver uma conta do PayPal, clique em **[!UICONTROL Start accepting payments via PayPal]**.

1. Digite uma das credenciais a seguir que você usa para fazer logon em sua conta de comerciante do PayPal:

   - **[!UICONTROL Partner]** - Sua ID de parceiro do PayPal.
   - **[!UICONTROL Vendor]** - Seu nome de logon de usuário do PayPal.
   - **[!UICONTROL User]** - A ID de outro usuário que está configurado em sua conta do PayPal.

1. Digite o **[!UICONTROL Password]** que está associado à sua conta do PayPal.

1. Para executar transações de teste, defina **[!UICONTROL Test Mode]** como `Yes`.

   Ao testar a configuração em uma sandbox, use apenas [números de cartão de crédito][2] recomendados pelo PayPal. Quando estiver pronto para entrar na produção, volte para a configuração e defina o Modo de Teste como `No`.

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

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) as seções restantes e repita as etapas anteriores:

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

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Basic Settings - PayPal Payments Pro]**.

   ![Configurações Básicas do PayPal Payment Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, insira um título que identifique PayPal Payments Pro durante o check-out.

   É recomendável usar o título _Cartão de Débito ou Crédito_.

1. Se você oferecer vários métodos de pagamento, insira um número para **[!UICONTROL Sort Order]** para determinar a sequência em que o PayPal Payments Pro será exibido quando listado com outros métodos de pagamento durante o check-out.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Defina **[!UICONTROL Payment Action]** como um dos seguintes:

   - `Authorization` - Aprova a compra, mas suspende os fundos. O valor não é retirado até ser _capturado_ pelo comerciante.
   - `Sale` - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

1. Para **[!UICONTROL Credit Card Settings]**, selecione os cartões de crédito que você aceita para pagamento em sua loja.

   Para selecionar várias placas, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada uma.

   >[!NOTE]
   >
   >American Express requer um acordo extra.

### Etapa 5: concluir as configurações avançadas

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advanced Settings]**.

   ![Configurações Avançadas do PayPal Payments Pro](./assets/paypal-payments-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Payment Applicable From]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` - Depois de escolher esta opção, a lista _[!UICONTROL Payment from Specific Countries]_&#x200B;é exibida. Mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada país na lista onde os clientes podem fazer compras na sua loja.

1. Para gravar comunicações com o sistema de pagamento no arquivo de log, defina **[!UICONTROL Debug Mode]** como `Yes`.

   >[!NOTE]
   >
   >De acordo com os padrões de segurança de dados do PCI, as informações de cartão de crédito não são gravadas no arquivo de registro.

1. Para habilitar a verificação de autenticidade do host, defina **[!UICONTROL Enable SSL Verification]** como `Yes`.

1. Para exigir que os clientes insiram um código CVV, defina **[!UICONTROL Require CVV Entry]** como `Yes`.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL CVV and AVS Settings]**.

1. Para determinar quando uma transação deve ser rejeitada quando o Sistema de Verificação de Endereço identificar uma incompatibilidade, especifique como tratar cada um dos seguintes cenários:

   - Para rejeitar uma transação com base em uma incompatibilidade de rua incompatível, defina **[!UICONTROL AVS Street Does Not Match]** como `Yes`.

   - Para rejeitar uma transação baseada em um CEP incompatível, defina **[!UICONTROL AVS Zip Does Not Match]** como `Yes`.

   - Para rejeitar uma transação baseada em um identificador de país incompatível, defina **[!UICONTROL International AVS Indicator Does Not Match]** como `Yes`.

   - Para rejeitar uma transação baseada em um código CVV incompatível, defina **[!UICONTROL International Card Security Code Does Not Match]** como `Yes`.

   ![Configurações Necessárias do PayPal Payments Pro - CVV e AVS](./assets/paypal-payments-pro-cvv-avs-settings.png){width="600" zoomable="yes"}

1. Preencha as seguintes seções, conforme necessário para sua loja:

   - [Configurações do relatório de liquidação](#settlement-report-settings)
   - [Configurações de experiência de front-end](#frontend-experience-settings)

#### Configurações do relatório de liquidação

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Settlement Report Settings]**.

   ![Configurações do Relatório de Liquidação do PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL SFTP Credentials]**, faça o seguinte:

   - Se você se inscreveu no Servidor FTP seguro do PayPal, insira as seguintes credenciais de logon SFTP:

      - Logon
      - Senha

   - Para executar relatórios de teste antes de entrar no site com o Payments Pro, defina **[!UICONTROL Sandbox Mode]** como `Yes`.

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

Use o _[!UICONTROL Frontend Experience Settings]_&#x200B;para escolher quais logotipos do PayPal aparecem em seu site, e para personalizar a aparência das suas páginas de comerciante do PayPal.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Frontend Experience Settings]**.

   ![Configurações da experiência de front-end](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Selecione o **[!UICONTROL PayPal Product Logo]** que você deseja que apareça no bloco PayPal em sua loja.

   Os logotipos PayPal estão disponíveis em quatro estilos e dois tamanhos:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Para personalizar a aparência das páginas do comerciante do PayPal, faça o seguinte:

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

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` - Depois de escolher esta opção, a lista _[!UICONTROL Payment from Specific Countries]_&#x200B;é exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada item.

1. Para gravar comunicações com o sistema de pagamento no arquivo de log, defina **[!UICONTROL Debug Mode]** como `Yes`.

   >[!NOTE]
   >
   >De acordo com os padrões de segurança de dados do PCI, as informações de cartão de crédito não são gravadas no arquivo de registro.

1. Para habilitar a verificação de autenticidade do host, defina **[!UICONTROL Enable SSL Verification]** como `Yes`.

1. Para exibir um resumo completo do pedido do cliente por item de linha do site do PayPal, defina **[!UICONTROL Transfer Cart Line Items]** como `Yes`.

1. Para permitir que o cliente conclua a transação no site do PayPal sem retornar ao seu armazenamento para Revisão do Pedido, defina **[!UICONTROL Skip Order Review Step]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/paypal-payments-pro/
