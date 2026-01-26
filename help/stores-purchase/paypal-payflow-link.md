---
title: Link do fluxo de pagamento do PayPal
description: Saiba como configurar o PayPal Payflow Link como uma solução de pagamento online em sua loja.
exl-id: dba4057e-1fea-4a23-8594-cc85f619d664
feature: Payments
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2178'
ht-degree: 0%

---

# Link do fluxo de pagamento do PayPal

O PayPal Payflow Link está disponível somente para comerciantes nos Estados Unidos e Canadá. Os clientes não precisam ter uma conta pessoal do PayPal e inserir suas informações de cartão de crédito em um formulário hospedado pelo PayPal. As informações nunca são armazenadas em seu servidor Adobe Commerce ou Magento Open Source. O Link do fluxo de pagamento não pode ser usado para pedidos criados do Administrador.

Os avisos de crédito são suportados para reembolsos online e offline. No entanto, vários reembolsos online não são suportados.

>[!IMPORTANT]
>
>Requisitos do **PSD2:** <br/>
>A partir de 14 de setembro de 2019, os bancos europeus poderão recusar pagamentos que não atendam aos requisitos do [PSD2](../getting-started/compliance-payment-services-directive.md). Para estar em conformidade com o PSD2, o PayPal Payflow Link deve ser integrado ao Cardeal Commerce. Para saber mais, consulte [Segurança 3D para Fluxo de Pagamento](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

## Requisitos

- [Conta Comercial do PayPal](https://www.paypal.com/webapps/mpp/how-to-sell-online) O gateway do PayPal Payflow Pro vincula a conta do comerciante no PayPal ao site do comerciante, atuando como uma conta de gateway e de comerciante.

- Se você gerenciar vários sites do Commerce, deve ter uma conta de comerciante do PayPal separada para cada site.

## Fluxo de trabalho do cliente

1. **O cliente vai ao check-out** - Durante o check-out, o cliente opta por pagar com o link de Fluxo de Pagamento do PayPal e insere as informações do cartão de crédito. O cliente não precisa ter uma conta pessoal do PayPal.
1. **O cliente escolhe Pagar Agora** - O cliente toca no botão Pagar Agora para enviar o pedido.
1. **O cliente insere informações de cartão de crédito** - O cliente insere as informações de cartão de crédito em um formulário hospedado pelo PayPal. Se o cliente clicar no link _Cancelar Pagamento_, ele retornará ao estágio Informações de Pagamento do check-out e o status do pedido será alterado para _Cancelado_.
1. **O cliente envia o pedido** - As informações de cartão de crédito são enviadas diretamente para o PayPal e não são retidas em nenhum lugar do site do Commerce.

## Solicitar fluxo de trabalho

1. **O PayPal recebe a solicitação** - O PayPal recebe a solicitação do cliente para pagar agora.
1. **O PayPal verifica as informações de pagamento** - O PayPal verifica as informações de cartão de crédito e atribui o status apropriado:
   - **Pagamento Verificado:** Se verificado, o status _Pagamento Pendente_ é atribuído inicialmente ao pedido até que a transação seja liquidada.
   - **Processando** - A transação foi bem-sucedida.
   - **Pagamento Pendente** - O sistema não recebeu uma resposta do PayPal.
   - **Cancelada** - A transação não foi bem-sucedida por algum motivo.
   - **Suspeita de Fraude** - A transação não passou alguns dos [filtros de fraude do PayPal](paypal.md#paypal-fraud-management-filters). O sistema recebe a resposta do PayPal informando que a transação está sendo analisada pelo Serviço de Fraude.
   - **Cancelar Pagamento:** Se o cliente clicar no link _Cancelar Pagamento_, ele retornará ao estágio Informações de Pagamento do check-out e o status da ordem será alterado para _Cancelado_.
1. **O cliente é redirecionado para a página de confirmação** - Se a transação for concluída com êxito, o cliente será redirecionado para a página de confirmação de pedido em sua loja. Se a transação falhar por algum motivo, uma mensagem de erro será exibida na página de finalização da compra e o cliente será direcionado para repetir o processo de finalização da compra. Essas situações são gerenciadas pelo PayPal.
1. **O comerciante atende à ordem** - As faturas do comerciante e envia a ordem como de costume.

## Configurar sua conta do PayPal

1. Faça logon em sua [conta comercial do PayPal](https://manager.paypal.com/).

1. Configure as [Páginas de Check-out Hospedadas](https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager) usando o PayPal Manager com as seguintes configurações:

   - Em **[!UICONTROL Security Options]**, conclua as seguintes configurações:

     **[!UICONTROL AVS]**: `No`

     **[!UICONTROL CSC]**: `No`

     **[!UICONTROL Enable Secure Token]**: `Yes`

   - Escolha **[!UICONTROL Customize]** e depois **[!UICONTROL Layout C]**.

     O layout C mostra apenas campos de cartão de crédito e débito, e pode ser emoldurado em seu site ou usado como um pop-up independente. O tamanho é fixado em 490 x 565 pixels, com espaço extra para mensagens de erro. Em alguns sistemas, essa configuração corrige um problema de redirecionamento transparente.

1. Quando as configurações estiverem concluídas, clique em **[!UICONTROL Save and Publish]**.

1. Configurar um usuário extra (recomendado pelo PayPal):

   - Na segunda linha do menu principal, clique em **[!UICONTROL Manage Users]**.

   - Para adicionar outro usuário à conta, clique em **[!UICONTROL Add User]**.

   - Preencha os campos obrigatórios nas seguintes seções do formulário _Adicionar Usuário_:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Clique em **[!UICONTROL Update]**.

## Configurar Link do Fluxo de Pagamento do PayPal

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

1. Expanda **[!UICONTROL PayPal Payment Gateways]** (se necessário) e clique em **[!UICONTROL Configure]** para **[!UICONTROL Payflow Link]**.

   ![Link do Fluxo de Pagamento - Configurar](./assets/payflow-link.png){width="600" zoomable="yes"}

### Etapa 2: concluir as configurações necessárias do PayPal

![Configurações necessárias do PayPal - Link do fluxo de pagamento do PayPal](./assets/payflow-required-link.png){width="600" zoomable="yes"}

1. (Opcional) Insira o **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Os endereços de email diferenciam maiúsculas de minúsculas. Para receber o pagamento, o endereço de email deve corresponder ao endereço de email especificado em sua conta de comerciante do PayPal.

1. Digite uma das credenciais a seguir que você usa para fazer logon em sua conta de comerciante do PayPal:

   - **[!UICONTROL Partner]** - Sua ID de parceiro do PayPal.
   - **[!UICONTROL User]** - A ID de outro usuário que está configurado em sua conta do PayPal.
   - **[!UICONTROL Vendor]** - Seu nome de logon de usuário do PayPal.

1. Digite o **[!UICONTROL Password]** que está associado à sua conta do PayPal.

1. Para executar transações de teste, defina **[!UICONTROL Test Mode]** como `Yes`.

   Ao testar a configuração em uma sandbox, use apenas [números de cartão de crédito](https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm) recomendados pelo PayPal. Quando estiver pronto para entrar na produção, volte para a configuração e defina o Modo de Teste como `No`.

1. Se o sistema usar um servidor proxy para estabelecer a conexão com o sistema PayPal, defina **[!UICONTROL Test Mode]** como `Yes` e faça o seguinte:

   - Digite o endereço IP de **[!UICONTROL Proxy Host]**.

   - Insira o número da porta de **[!UICONTROL Proxy Port]**.

     Um proxy é usado quando o firewall do servidor impede o acesso direto ao servidor do PayPal. Nesse caso, um servidor de terceiros é usado para retransmitir o tráfego.

1. Defina **[!UICONTROL Enable Payflow Link]** como `Yes`.

1. Se você deseja habilitar as opções de [Check-out Expresso do PayPal](paypal-express-checkout.md) para clientes, defina **[!UICONTROL Enable Express Checkout]** como `Yes`.

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

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) as seções restantes e repita as etapas anteriores para a configuração da página inicial:

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

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Basic Settings - PayPal Payflow Link]**.

   ![Configurações Básicas - Link de Fluxo de Pagamento do PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, insira um título que identifique o Link do Fluxo de Pagamento do PayPal durante o check-out.

   É recomendável usar o título _Cartão de Débito ou Crédito_.

1. Se você oferecer vários métodos de pagamento, insira um número para **[!UICONTROL Sort Order]** para determinar a sequência em que o Vínculo de Fluxo de Pagamento aparecerá quando listado com os outros métodos de pagamento.

   Esse número é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Defina **[!UICONTROL Payment Action]** como um dos seguintes:

   - `Authorization` - Aprova a compra e suspende os fundos. O valor não é sacado até que seja capturado pelo comerciante.
   - `Sale` - O valor da compra é autorizado e imediatamente retirado da conta do cliente.

### Etapa 5: concluir as configurações avançadas

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advanced Settings]**.

   ![Configurações Avançadas - Link do Fluxo de Pagamento do PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-advanced-settings.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Payment Applicable From]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` - Depois de escolher esta opção, a lista _[!UICONTROL Payment from Specific Countries]_&#x200B;é exibida. Mantenha pressionada a tecla Ctrl e selecione cada país na lista onde os clientes podem fazer compras na sua loja.

1. Para gravar comunicações com o sistema de pagamento no arquivo de log, defina **[!UICONTROL Debug Mode]** como `Yes`.

   >[!NOTE]
   >
   >De acordo com os padrões de segurança de dados do PCI, as informações de cartão de crédito não são gravadas no arquivo de registro.

1. Para habilitar a verificação de autenticidade do host, defina **[!UICONTROL Enable SSL Verification]** como `Yes`.

1. Se você quiser que o cliente corrija a entrada do código de segurança de três dígitos do CVV na parte de trás de um cartão de crédito, defina **[!UICONTROL CVV Entry is Editable]** como `Yes`.

1. Para exigir que os clientes insiram um código CVV, defina **[!UICONTROL Require CVV Entry]** como `Yes`.

1. Para enviar uma confirmação do pagamento ao cliente, defina **[!UICONTROL Send Email Confirmation]** como `Yes`.

1. Para determinar o método usado para trocar informações com o servidor do PayPal durante uma transação, defina o **[!UICONTROL URL method for Cancel URL and Return URL]** como um dos seguintes:

   - `GET` - Recupera informações que são o resultado de um processo (método padrão).
   - `POST` - Fornece um bloco de dados, como dados inseridos em um formulário, para um processo de manipulação de dados.

   A _URL de Cancelamento_ e a _URL de Retorno_ referem-se à página em que o cliente retorna após concluir ou cancelar a parte de pagamento do processo de finalização de compra no servidor PayPal

1. Preencha as seguintes seções, conforme necessário para sua loja:

   - [Configurações do relatório de liquidação](#settlement-report-settings)
   - [Configurações de experiência de front-end](#frontend-experience-settings)

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

Use o _[!UICONTROL Frontend Experience Settings]_&#x200B;para escolher quais logotipos do PayPal aparecem em seu site, e para personalizar a aparência das suas páginas de comerciante do PayPal.

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

   ![Configurações básicas](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png){width="600" zoomable="yes"}

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

   ![Configurações avançadas](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

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
