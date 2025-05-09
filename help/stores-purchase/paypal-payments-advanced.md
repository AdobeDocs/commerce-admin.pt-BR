---
title: Pagamentos do PayPal Avançados
description: Saiba como configurar o PayPal Payments Advanced como uma solução de pagamento online em sua loja.
exl-id: 018dd999-2f17-4650-8f61-624809ae76c6
feature: Payments
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2161'
ht-degree: 0%

---

# Pagamentos do PayPal Avançados

O [PayPal Payments Advanced][4] é uma solução [compatível com PCI](../getting-started/compliance-pci.md) que permite que seus clientes paguem por débito ou cartão de crédito sem sair do site. Ele inclui uma página de check-out incorporada que pode ser personalizada para criar uma experiência de check-out contínua e segura.

Mesmo clientes sem uma conta do PayPal podem fazer compras através do gateway de pagamento seguro do PayPal. Os cartões aceitos incluem Visa, MasterCard, Switch/Maestro e cartões de crédito Solo nos Estados Unidos e Reino Unido. Para maior comodidade, PayPal Express Check-out está incluído com PayPal Pagamentos Avançados.

>[!IMPORTANT]
>
>Requisitos do **PSD2:** <br/>
>A partir de 14 de setembro de 2019, os bancos europeus poderão recusar pagamentos que não atendam aos requisitos do [PSD2](../getting-started/compliance-payment-services-directive.md). Para estar em conformidade com o PSD2, o PayPal Payments Advanced deve ser integrado a um plug-in de terceiros. Para saber mais, consulte [Segurança 3D para Fluxo de Pagamento](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

>[!NOTE]
>
>Pagamentos Avançados do PayPal não podem ser usados para pedidos criados do Administrador da sua loja.

## Requisitos

- [Conta comercial do PayPal][1]
- Se você gerenciar vários sites do Adobe Commerce e do Magento Open Source, deverá ter uma conta de comerciante do PayPal separada para cada site.

## Fluxo de trabalho de check-out

1. **O cliente escolhe o método de pagamento** - Durante o check-out, o cliente opta por pagar com o PayPal Payments Advanced. O botão Pagar agora é exibido em vez do botão Fazer pedido.

1. **Pagar agora** - O cliente clica/toca em _Pagar agora_ e um formulário hospedado no PayPal é exibido. O cliente insere as informações do cartão e ele é verificado. Se for bem-sucedido, a página de confirmação do pedido será exibida.

   **Pagar com PayPal** - O formulário também inclui o botão _Pagar com PayPal_, que redireciona o cliente para o site do PayPal, onde o pagamento pode ser feito com o Check-out expresso do PayPal.

1. **Solução de problemas** - Se a transação falhar por algum motivo, uma mensagem de erro será exibida na página de check-out e o cliente será instruído a tentar novamente. Quaisquer problemas são gerenciados pelo PayPal.

## Fluxo de trabalho de processamento de pedidos

Processar pedidos com Pagamentos do PayPal Avançado é o mesmo para qualquer pedido PayPal comum. Os pedidos são faturados e entregues, e os avisos de crédito são gerados para reembolsos on-line e off-line. No entanto, vários reembolsos online não estão disponíveis para pedidos pagos com o PayPal Payments Advanced.

1. **O cliente faz o pedido** - No estágio final do check-out, o cliente toca no botão Fazer pedido.

1. **Resposta do PayPal** - O PayPal avalia a solicitação. Se for considerado válido, o PayPal processa a transação.

1. **A Commerce define o status do pedido** - A Commerce recebe uma resposta do PayPal e define o status do pedido como um dos seguintes:

   - **Processando** - A transação foi bem-sucedida.
   - **Pagamento Pendente** - O sistema não recebeu nenhuma resposta do PayPal.
   - **Cancelada** - A transação não foi bem-sucedida por algum motivo
   - **Suspeita de Fraude** - A transação não passou alguns dos [filtros de fraude do PayPal](paypal.md#paypal-fraud-management-filters). O sistema recebe a resposta do PayPal informando que a transação está sendo analisada pelo Serviço de Fraude.

1. **O comerciante atende ao pedido** - O comerciante fatura e envia o pedido.

## Configurar sua conta do PayPal

Antes de configurar o PayPal Payments Advanced no Commerce, você deve configurar sua conta no site do PayPal.

1. Faça logon em sua [conta comercial do PayPal][2].

1. Vá para **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up Menu]** e conclua as seguintes configurações:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. **[!UICONTROL Save]** as configurações.

   >[!NOTE]
   >
   >Se você tiver vários sites do Commerce, deverá criar uma conta separada do PayPal Payments Advanced para cada um.

1. Quando solicitado a criar um layout, faça o seguinte:

   - Na parte superior da página, clique em **[!UICONTROL Customize]**.

   - Escolha **[!UICONTROL Layout C]**.

   - Clique em **[!UICONTROL Save and Publish]**.

1. Configurar outro usuário (recomendado pelo PayPal):

   - Faça logon em sua [conta comercial do PayPal][2].

   - Para configurar outro usuário, siga as instruções.

   - **[!UICONTROL Save]** as alterações.

## Configurar Pagamentos do PayPal Avançados no Commerce

>[!NOTE]
>
>Você pode ter duas soluções PayPal ativas ao mesmo tempo: Check-out expresso, além de qualquer solução All-In-One ou Payment Gateway. Se você alterar as soluções de pagamento, a que foi usada anteriormente será desabilitada.

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

1. Expanda **[!UICONTROL PayPal All-in-One Payment Solution]** e clique em **[!UICONTROL Configure]** para **[!UICONTROL Payments Advanced]**.

   ![Pagamentos do PayPal Avançados](./assets/paypal-payments-advanced.png){width="600" zoomable="yes"}

### Etapa 2: concluir as configurações necessárias

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Required PayPal Settings]**, se necessário.

   ![Configurações Avançadas Necessárias - Pagamentos do PayPal Avançados](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-required.png){width="600" zoomable="yes"}

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

   Ao testar a configuração em uma sandbox, use apenas [números de cartão de crédito][3] recomendados pelo PayPal. Quando estiver pronto para entrar na produção, volte para a configuração e defina o Modo de Teste como `No`.

1. Se o sistema usar um servidor proxy para estabelecer a conexão com o sistema PayPal, defina **[!UICONTROL Use Proxy]** como `Yes` e faça o seguinte:

   - Digite o endereço IP de **[!UICONTROL Proxy Host]**.

   - Insira o número da porta de **[!UICONTROL Proxy Port]**.

     Um proxy é usado quando o firewall do servidor impede o acesso direto ao servidor do PayPal. Nesse caso, um servidor de terceiros é usado para retransmitir o tráfego.

1. Defina **[!UICONTROL Enable this Solution]** como `Yes`.

1. Se você deseja oferecer o [Crédito do PayPal](paypal.md#paypal-credit-and-pay-later) aos seus clientes, defina o **[!UICONTROL Enable PayPal Credit]** como `Yes`.

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

   ![Anunciar Configurações da Página Inicial de Crédito do PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) as seções restantes e repita as etapas anteriores:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Anunciar PayPal PayLater

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advertise PayPal PayLater]**.

1. Defina **[!UICONTROL Enable PayPal PayLater]** como `Yes`.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Home Page]**.

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

   ![Anunciar Configurações da Página Inicial de Crédito do PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) as seções restantes e repita as etapas anteriores:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Etapa 4: concluir as configurações básicas

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Basic Settings - PayPal Payments Advanced]**, se necessário.

   ![Configurações Básicas Avançadas do PayPal Payments](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-basic-settings.png){width="600" zoomable="yes"}

1. Para identificar Pagamentos do PayPal Avançados durante o check-out, insira um **[!UICONTROL Title]**.

   É recomendável usar o título _Cartão de Débito ou Crédito_.

1. Se você oferecer vários métodos de pagamento, insira um número para **[!UICONTROL Sort Order]** para determinar a sequência em que Pagamentos do PayPal Avançados será exibido quando listado com outros métodos de pagamento durante o check-out.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Defina **[!UICONTROL Payment Action]** como um dos seguintes:

   - `Authorization` - Aprova a compra, mas suspende os fundos. O valor não é retirado até ser _capturado_ pelo comerciante.
   - `Sale` - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

### Etapa 5: concluir as configurações avançadas

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advanced Settings]**.

   ![Configurações Avançadas - Pagamentos do PayPal Avançados](./assets/paypal-payments-advanced2.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Payment Applicable From]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` - Depois de escolher esta opção, a lista _[!UICONTROL Payment from Specific Countries]_&#x200B;é exibida. Mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada país na lista onde os clientes podem fazer compras na sua loja.

1. Para gravar comunicações com o sistema de pagamento no arquivo de log, defina **[!UICONTROL Debug Mode]** como `Yes`.

   O arquivo de log do PayPal Payments Advanced é `payments_payflow_advanced.log`.

   >[!NOTE]
   >
   >De acordo com os padrões de segurança de dados do PCI, as informações de cartão de crédito não são gravadas no arquivo de registro.

1. Para habilitar a verificação de autenticidade do host, defina **[!UICONTROL Enable SSL Verification]** como `Yes`.

1. Para permitir que o cliente corrija a entrada do código de segurança CVV de três dígitos da parte traseira de um cartão de crédito, defina **[!UICONTROL CVV Entry is Editable]** como `Yes`.

1. Para exigir que os clientes insiram um código CVV, defina **[!UICONTROL Require CVV Entry]** como `Yes`.

1. Para enviar uma confirmação do pagamento ao cliente, defina **[!UICONTROL Send Email Confirmation]** como `Yes`.

1. Para determinar o método usado para trocar informações com o servidor do PayPal durante uma transação, defina o **[!UICONTROL URL method for Cancel URL and Return URL]** como um dos seguintes:

   - `GET` - (Padrão) Recupera informações que são o resultado de um processo.
   - `POST` - Fornece um bloco de dados, como dados inseridos em um formulário, para um processo de manipulação de dados.

   A _URL de Cancelamento_ e a _URL de Retorno_ referem-se à página em que o cliente retorna após concluir ou cancelar a parte de pagamento do processo de finalização de compra no servidor PayPal.

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

   - Para executar relatórios de teste antes de entrar em funcionamento, defina **[!UICONTROL Sandbox Mode]** como `Yes`.

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

Use o _[!UICONTROL Frontend Experience Settings]_&#x200B;para escolher quais logotipos do PayPal aparecem em seu site e para personalizar a aparência das suas páginas de comerciante do PayPal.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Frontend Experience Settings]**.

   ![Configurações da Experiência de Front-end do PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png){width="600" zoomable="yes"}

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

### Etapa 6: Concluir as configurações básicas do Check-out do PayPal Express

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Basic Settings - PayPal Express Checkout]**.

   ![Configurações Básicas de Check-out do PayPal Express](../configuration-reference/sales/assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, insira um título que identifique este método de pagamento durante o check-out.

   É recomendável definir o título como _PayPal_ para cada exibição de loja.

1. Se você oferecer vários métodos de pagamento, insira um número para **[!UICONTROL Sort Order]** para determinar a sequência em que o Check-out do PayPal Express é exibido quando listado com os outros métodos de pagamento.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Defina **[!UICONTROL Payment Action]** como um dos seguintes:

   - `Authorization` - Aprova a compra e suspende os fundos. O valor não é retirado até ser _capturado_ pelo comerciante.
   - `Sale` - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

1. Para exibir o botão _[!UICONTROL Check out with PayPal]_&#x200B;na página do produto, defina **[!UICONTROL Display on Product Details Page]**&#x200B;como `Yes`.

### Etapa 7: Concluir configurações avançadas - Finalização de compra do PayPal Express

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advanced Settings]**.

   ![Configurações Avançadas de Check-out do PayPal Express](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png){width="600" zoomable="yes"}

1. Para disponibilizar o Check-out Expresso do PayPal do carrinho de compras e do minicarrinho, defina **[!UICONTROL Display on Shopping Cart]** como `Yes`.

1. Defina **[!UICONTROL Payment Applicable From]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` |Depois de escolher esta opção, a _Lista de Pagamentos de Países Específicos_ é exibida. Mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada país da lista onde os clientes podem fazer compras na sua loja.

1. Para gravar comunicações com o sistema de pagamento no arquivo de log, defina **[!UICONTROL Debug Mode]** como `Yes`.

   >[!NOTE]
   >
   >De acordo com os [Padrões de Segurança de Dados PCI](../getting-started/compliance-pci.md), as informações de cartão de crédito não são gravadas no arquivo de log.

1. Para habilitar a verificação de autenticidade do host, defina **[!UICONTROL Enable SSL Verification]** como `Yes`.

1. Para exibir um resumo completo do pedido do cliente por item de linha do site do PayPal, defina **[!UICONTROL Transfer Cart Line Items]** como `Yes`.

1. Para permitir que o cliente conclua a transação no site do PayPal sem retornar ao seu armazenamento para Revisão do Pedido, defina **[!UICONTROL Skip Order Review Step]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/gs-ppa-hosted-pages/
