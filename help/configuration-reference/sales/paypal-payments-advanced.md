---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Advanced]'
description: Revise as configurações na seção [!UICONTROL PayPal Payments Advanced] na página [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] do Administrador do Commerce.
exl-id: c9159408-fbdf-4146-8292-9952cd5d01fa
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Advanced]

>[!IMPORTANT]
>
>Requisitos de **PSD2:** <br/>
>A partir de 14 de setembro de 2019, os bancos europeus poderão recusar pagamentos que não atendam aos requisitos de [PSD2](../../getting-started/compliance-payment-services-directive.md). Para estar em conformidade com o PSD2, [!DNL PayPal Payments Advanced] deve ser integrado com [!DNL Cardinal Commerce]. Para saber mais, consulte [Segurança 3D para Fluxo de Pagamento](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Configurações necessárias](./assets/payment-methods-paypal-payments-advanced-required.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Site | (Opcional) Qualquer endereço de email associado à sua conta de comerciante do PayPal. Os endereços de email diferenciam maiúsculas de minúsculas e devem corresponder exatamente aos endereços que estão em sua conta. |
| [!UICONTROL Partner] | Site | Sua ID de parceiro do PayPal, se aplicável. |
| [!UICONTROL Vendor] | Site | Seu nome de logon de usuário do PayPal. |
| Usuário | Site | A ID de outro usuário em sua conta do PayPal. |
| [!UICONTROL Password] | Site | A senha associada à sua conta de comerciante do PayPal. |
| [!UICONTROL Test Mode] | Site | Quando ativado, executa o PayPal Payments Advanced em um ambiente de teste. Desative o modo de teste quando estiver pronto para &quot;entrar em produção&quot;. Opções: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Site | Um proxy pode ser usado para redirecionar o tráfego quando o firewall do servidor impede o acesso direto ao servidor PayPal. Se aplicável, identifica o servidor proxy usado para estabelecer conexão com o servidor do PayPal. Opções: `Yes` / `No` <br/><br/>Se habilitada, defina as opções: <br/>**`Proxy Host`**- O endereço IP do host proxy.<br/>**`Proxy Port`** - O número da porta do proxy. |
| [!UICONTROL Enable this Solution] | Site | Determina se o PayPal Payments Advanced está disponível para seus clientes como um método de pagamento. |
| [!UICONTROL Enable PayPal Credit] | Site | Determina se o Crédito do PayPal está disponível para seus clientes como uma opção de pagamento. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![Anunciar Crédito do PayPal](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Site | A ID do Publicador associada à sua conta de Crédito do PayPal. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Busca a ID do editor no PayPal. |
| [!UICONTROL Home Page] | Site | Determina a posição e o tamanho do banner [!DNL PayPal Credit] na página inicial. Opções: <br/>**`Display`**- Determina se um banner [!DNL PayPal Credit] é exibido na home page da loja. Opções: `Yes` / `No`<br/>**`Position`** - Determina a posição do banner [!DNL PayPal Credit] na página inicial. Opções: Cabeçalho (centro) / Barra Lateral (direita) <br/>**`Size`**- Determina o tamanho do banner [!DNL PayPal Credit] na página inicial. Opções: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Site | Determina a posição e o tamanho do banner [!DNL PayPal Credit] nas páginas de categoria. Opções: (igual a [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Site | Determina a posição e o tamanho do banner [!DNL PayPal Credit] nas páginas do produto. Opções: (igual a [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Site | Determina a posição e o tamanho do banner [!DNL PayPal Credit] na página do carrinho. Opções: (igual a [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings]

![Configurações básicas](./assets/payment-methods-paypal-payments-advanced-basic-settings.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Title] | Exibição da loja | Um nome que identifica Pagamentos do PayPal Avançados como um método de pagamento durante o check-out. |
| [!UICONTROL Sort Order] | Exibição da loja | Um número que determina a ordem em que o PayPal Payments Advanced aparece quando listado com outros métodos de pagamento durante a finalização da compra. |
| [!UICONTROL Payment Action] | Site | Determina a ação tomada pelo PayPal quando um pedido é enviado. Opções: <br/>**`Authorization`**- Aprova a compra, mas suspende os fundos. A quantidade não é retirada até que seja &quot;capturada&quot; pelo comerciante.<br/>**`Sale`** - O valor da compra é autorizado e imediatamente retirado da conta do cliente. |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Configurações avançadas](./assets/paypal-advanced-settings2.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | Site | Determina o intervalo da seleção de país aplicável. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Site | Identifica cada país do qual o pagamento é aceito. Somente os clientes com um endereço de cobrança em um país selecionado podem fazer compras com este método de pagamento. |
| [!UICONTROL Debug Mode] | Site | Registra mensagens enviadas entre sua loja e o sistema de pagamento em um arquivo de log. Opções: `Yes` / `No` <br/><br/>**_Observação:_**&#x200B;O arquivo de log está armazenado no servidor e pode ser acessado apenas por desenvolvedores. De acordo com os padrões de segurança de dados do PCI, as informações de cartão de crédito não são gravadas no arquivo de registro. |
| [!UICONTROL Enable SSL Verification] | Site | Determina se o canal seguro no host é verificado antes que uma transação ocorra. Opções: `Yes` / `No` |
| [!UICONTROL CVV Entry is Editable] | Site | Determina se o cliente pode editar o CVV após ele ser inserido. Opções: `Yes` / `No` |
| [!UICONTROL Require CVV Entry] | Site | Determina se os clientes devem digitar o código CVV no verso do cartão de crédito. Opções: `Yes` / `No` |
| [!UICONTROL Send Email Confirmation] | Site | Determina se o cliente recebe a confirmação do pagamento por email. Opções: `Yes` / `No` |
| [!UICONTROL URL Method for Cancel URL and Return URL] | Site | Determina o método usado para trocar informações com o servidor do PayPal durante uma transação. Opções: <br/>**`GET`**- Recupera informações que são o resultado de um processo. (Este é o método padrão.)<br/>**`POST`** - Envia um bloco de dados, como os dados inseridos em um formulário, para o processo de manipulação de dados. |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![Configurações do relatório de liquidação](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Site | O nome de usuário necessário para fazer logon no Servidor FTP Seguro do PayPal. |
| [!UICONTROL Password] | Site | A senha necessária para fazer logon no Servidor FTP Seguro do PayPal. |
| [!UICONTROL Sandbox Mode] | Site | Quando ativado, executa relatórios em um ambiente de teste antes de entrar em funcionamento no ambiente de produção. Opções: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Site | O URL onde os relatórios de liquidação são gerenciados. Valor padrão: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Site | O caminho onde os relatórios de liquidação são salvos no servidor. Valor padrão: `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Site | Quando ativado, busca os relatórios de liquidação automaticamente de acordo com a programação. Opções: `Yes` / `No` |
| [!UICONTROL Schedule] | Global | Determina com que frequência os relatórios de liquidação são gerados pelo PayPal. Opções: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Global | Determina a hora, os minutos e o segundo em que os relatórios de liquidação são gerados. |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![Configurações da experiência de front-end](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Exibição da loja | Determina o logotipo do PayPal que aparece em sua loja. Há quatro estilos básicos em dois tamanhos. Opções: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | Exibição da loja | Determina a aparência da página do comerciante do PayPal. Valores permitidos: <br/>**`paypal`**- Usa o estilo de página do PayPal.<br/>**`primary`** - Usa o estilo de página identificado como &quot;primário&quot; no perfil da conta. <br/>**`your_custom_value`**- Usa um estilo de página de pagamento personalizado, que é especificado no perfil da conta. |
| [!UICONTROL Header Image URL] | Exibição da loja | O URL da imagem que aparece no canto superior esquerdo da página de check-out. O tamanho máximo é 750 x 90 pixels. <br/><br/>**_Observação:_**&#x200B;o PayPal recomenda que a imagem seja armazenada em um servidor seguro (https). Caso contrário, o navegador do cliente poderá avisar que &quot;a página contém itens seguros e não seguros&quot;. |
| [!UICONTROL Header Image Background Color] | Exibição da loja | O código de [cor hexadecimal](https://en.wikipedia.org/wiki/Web_colors) de seis caracteres para a cor de plano de fundo do cabeçalho na página de check-out. Você pode inserir o código em caracteres maiúsculos e minúsculos. |
| [!UICONTROL Header Image Border Color] | Exibição da loja | O código de cor hexadecimal de seis caracteres para a borda de dois pixels ao redor do cabeçalho. |
| [!UICONTROL Page Background Color] | Exibição da loja | O código de cor hexadecimal de seis caracteres para a cor de plano de fundo da página de check-out que aparece atrás do cabeçalho e do formulário de pagamento. |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Express Checkout]

![Configurações Básicas de Check-out do PayPal Express](./assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Title] | Exibição da loja | Um nome que identifica o método de pagamento do Check-out expresso do PayPal durante o check-out. |
| [!UICONTROL Sort Order] | Exibição da loja | Um número que determina a ordem em que o Check-out do PayPal Express é exibido quando listado com outros métodos de pagamento durante o check-out. Digite `0` no início da lista. |
| [!UICONTROL Payment Action] | Site | Determina a ação tomada pelo PayPal quando recebe um pedido. Opções: <br/>**`Authorization`**- Aprova a compra, mas suspende os fundos. A quantidade não é retirada até que seja &quot;capturada&quot; pelo comerciante.<br/>**`Sale`** - O valor da compra é autorizado e imediatamente retirado da conta do cliente. <br/>**`Order`**- representa um contrato com o PayPal que permite que o comerciante capture uma ou mais quantias até o total solicitado da conta do comprador do cliente, dentro de um período de tempo definido. Isso pode levar até 29 dias. Uma ou mais faturas devem ser geradas pelo administrador do Commerce para capturar os fundos. |
| [!UICONTROL URL Display on Product Details Page] | Exibição da loja | Determina se o botão &quot;Finalizar compra com o PayPal&quot; aparece nas páginas do produto. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL PayPal Express Checkout - Advanced Settings]

![Configurações Avançadas de Check-out do PayPal Express](./assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Exibição da loja | Determina se o Check-out do PayPal Express é exibido como uma opção de pagamento no carrinho de compras. Opções: `Yes` (recomendado) / `No` |
| [!UICONTROL Payment Action Applicable From] | Site | Determina o intervalo da seleção de país aplicável. Opções: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Site | Identifica cada país do qual o pagamento é aceito. Somente os clientes com um endereço de cobrança em um país selecionado podem fazer compras com este método de pagamento. |
| [!UICONTROL Debug Mode] | Site | Registra mensagens enviadas entre sua loja e o sistema de pagamento do PayPal em um arquivo de log. Opções: `Yes` / `No` <br/><br/>**_Observação:_**&#x200B;O arquivo de log está armazenado no servidor e pode ser acessado apenas por desenvolvedores. De acordo com os padrões de segurança de dados do PCI, as informações de cartão de crédito não são gravadas no arquivo de registro. |
| [!UICONTROL Enable SSL Verification] | Site | Habilita a verificação do certificado de segurança do host. Opções: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Site | Exibe um resumo completo dos itens de linha do carrinho de compras do cliente no site do PayPal. Opções: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Site | Determina se os clientes podem concluir a transação no site do PayPal ou se precisam retornar à loja e concluir a etapa Revisão do Pedido antes de enviar o pedido. Opções: `Yes` / `No` |

{style="table-layout:auto"}
