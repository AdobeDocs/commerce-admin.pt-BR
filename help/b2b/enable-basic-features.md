---
title: Habilitar recursos B2B
description: Saiba mais sobre como ativar recursos B2B para sua loja da Adobe Commerce, incluindo contas da empresa, métodos padrão de pagamento e envio, ordens de compra e aprovações de pedidos.
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---

# Habilitar recursos B2B

Por padrão, todos os recursos B2B são inicialmente desativados. Um administrador de loja pode ativar ou desativar os recursos B2B conforme necessário para lojas do Commerce. Para obter uma lista completa das definições de configuração B2B, consulte [Referência de configuração de recursos B2B](../configuration-reference/general/b2b-features.md).

Quando você habilita o suporte para empresas do cliente, os recursos B2B adicionais são habilitados automaticamente:

- [!DNL Shared Catalog]

  Oferece suporte à configuração de preço personalizado para diferentes empresas e também permite permissões de categoria para todas as lojas.

- [!DNL Enable Shared Catalog direct products price assigning]

  Melhora o desempenho do site, armazenando somente os produtos atribuídos a um catálogo compartilhado no índice de preços. Habilitar esse recurso é uma prática recomendada para comerciantes que têm muitos catálogos compartilhados para gerenciar preços personalizados para diferentes empresas.

- [!DNL B2B Quotes]

  Oferece aos vendedores e compradores da empresa a capacidade de negociar preços.

- [!DNL B2B default payment and shipping methods]

  Determina a seleção das opções de pagamento e envio disponíveis para compradores B2B na loja.

As configurações desses recursos ficam visíveis somente quando [!DNL Enable Company] está definida como `Yes`.

B2B [!DNL Quick Order] e [!DNL Requisition List] os recursos do podem ser ativados e desativados independentemente.

## Configurar recursos B2B

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   Se você tiver uma instalação de vários sites, defina a variável **[!UICONTROL Store View]** no canto superior esquerdo para o site onde a configuração se aplica.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL B2B Features]**:

   ![Configuração B2B - geral](./assets/b2b-features.png){width="600"}

   - Permitir que os clientes gerenciem suas próprias contas da empresa e habilitem o suporte para recursos B2B adicionais definindo **[!UICONTROL Enable Company]**  para `Yes`.

     Quando você ativa o suporte da empresa, o Catálogo compartilhado, a Cotação B2B, os Métodos de pagamento B2B e os Métodos de envio B2B são ativados automaticamente.

   - Para permitir que clientes e convidados façam pedidos rapidamente com base no SKU ou no nome do produto, defina **[!UICONTROL Enable Quick Order]** para `Yes`.

   - Para permitir que os clientes criem e gerenciem listas de requisições a partir do painel de instrumentos da conta, defina **[!UICONTROL Enable Requisition List]** para `Yes`.

     Também é possível [configurar o número máximo de listas](configure-requisition-lists.md) um cliente pode ter para sua conta.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar métodos padrão de pagamento e envio B2B

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Default B2B Payment Methods]** seção.

1. Para estabelecer os métodos de pagamento padrão para ordens B2B, defina **[!UICONTROL Applicable Payment Methods]** a um dos seguintes:

   - `All Payment Methods`

   - `Selected Payment Methods`

     Para a opção específica, selecione o **[!UICONTROL Payment Methods]** que você deseja disponibilizar para os clientes mantendo pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) enquanto clica em cada opção.

   A lista de [métodos de pagamento](../configuration-reference/sales/payment-methods.md) mostra quais opções estão habilitadas ou desabilitadas no momento em sua loja. Além dos métodos de pagamento padrão, a lista também inclui o seguinte:

   - Nenhuma informação de pagamento é necessária
   - [Pagamento por conta](#configure-payment-on-account)
   - Contas armazenadas
   - Cartões armazenados

   ![Configuração B2B - configurações do método de pagamento padrão](./assets/b2b-features-default-payment-methods.png){width="600"}

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Default B2B Shipping Methods]** seção.

1. Para especificar os métodos de entrega padrão para ordens B2B, defina **[!UICONTROL Applicable Shipping Methods]** a um dos seguintes:

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     Para a opção específica, selecione o **[!UICONTROL Shipping Methods]** que você deseja disponibilizar para os clientes mantendo pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) enquanto clica em cada opção.

     A lista de métodos de envio mostra quais estão [ativado ou desativado](../configuration-reference/sales/delivery-methods.md).

   ![Configuração B2B - métodos de envio padrão](./assets/b2b-features-shipping-methods.png){width="600"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar opções de email da empresa

A variável [representante de vendas](account-company-manage.md#assign-a-sales-representative) atribuído como contato principal de uma empresa é configurado por padrão como remetente de muitas mensagens de email automatizadas enviadas para a empresa.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Company Configuration]**.

1. Se necessário, defina **[!UICONTROL Store View]** à exibição de loja para definir o [escopo](../getting-started/websites-stores-views.md#scope-settings) da configuração.

1. Conclua o **[!UICONTROL Company Registration]** seção:

   >[!NOTE]
   >
   >Limpe a **[!UICONTROL Use system value]** para tornar o campo editável.

   - Definir **[!UICONTROL Company Registration Email Recipient]** para o [armazenar contato](../getting-started/store-details.md#store-email-addresses) quem será notificado quando for recebida uma nova solicitação de registro de empresa.

   - Para **[!UICONTROL Send Company Registration Email Copy To]**, insira o endereço de email de cada pessoa que receberá uma cópia da notificação de registro. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **Método de cópia de email de envio** a um dos seguintes:

      - `Bcc` - Envia um _cópia cega de cortesia_ incluindo o recipient no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você preparou um template de email que deve ser usado em vez do padrão, defina **[!UICONTROL Default Company Registration Email]** ao nome do template. Por padrão, a variável `Company Registration Request` modelo é usado.

     ![Configuração de clientes - registro da empresa](./assets/company-email-options-company-registration.png){width="600"}

1. Conclua o **[!UICONTROL Customer-Related Emails]** seção:

   Se você preparou modelos de email alternativos a serem usados em vez dos padrões, escolha o modelo que deseja usar para cada um dos seguintes:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuração dos clientes - emails relacionados ao cliente](./assets/company-email-options-customer-related-emails.png){width="600"}

1. Conclua o **[!UICONTROL Company Status Change]** seção:

   - Para **[!UICONTROL Send Company Status Change Email Copy To]**, insira o endereço de email de cada pessoa que receberá uma cópia da notificação de alteração de status. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **Método de cópia de email de envio** a um dos seguintes:

      - `Bcc` - Envia um _cópia cega de cortesia_ incluindo o recipient no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa mudar de `Pending Approval` para `Active`, definir **[!UICONTROL Default 'Company Status Change to Active 1' Email]** ao nome do template. Por padrão, a variável `Company Status Active 1` modelo é usado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa mudar de `Rejected` ou `Blocked` para `Active`, definir **[!UICONTROL Default 'Company Status Change to Active 2' Email]** ao nome do template. Por padrão, a variável `Company Status Active 2` modelo é usado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa for alterado para `Rejected`, definir **[!UICONTROL Default 'Company Status Change to Rejected' Email]** ao nome do template. Por padrão, a variável `Company Status Rejected` modelo é usado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa for alterado para `Blocked`, definir **[!UICONTROL Default 'Company Status Change to Blocked' Email]** ao nome do template. Por padrão, a variável `Company Status Blocked` modelo é usado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa for alterado para `Pending Approval`, definir **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** ao nome do template. Por padrão, a variável `Company Status Pending Approval` modelo é usado.

   ![Configuração dos clientes - alteração do status da empresa](./assets/company-email-options-company-status-change.png){width="600"}

1. Conclua o **[!UICONTROL Company Credit Emails]** seção:

   - Definir **[!UICONTROL Company Credit Change Email Sender]** para o [armazenar contato](../getting-started/store-details.md#store-email-addresses) quem deve ser notificado quando for feita uma alteração no limite de crédito atribuído a uma empresa. A notificação é enviada para _Representante de Vendas_.

   - Para **[!UICONTROL Send Company Credit Change Email Copy To]**, insira o endereço de email de cada pessoa que receberá uma cópia da notificação de alteração de crédito. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **Método de cópia de email de envio** a um dos seguintes:

      - `Bcc` - Envia um _cópia cega de cortesia_ incluindo o recipient no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você preparou modelos de e-mail a serem usados em vez dos padrões, escolha o modelo para cada uma das notificações a seguir enviadas ao administrador da empresa.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configuração dos clientes - emails de crédito da empresa](./assets/company-email-options-company-credit.png){width="600"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar aprovação de pedidos

A capacidade de rastrear o processamento de pedidos e ordens de compra dá aos administradores da empresa o controle sobre as ações dos compradores da empresa. A funcionalidade de aprovação de ordem está disponível quando o recurso de ordens de compra é habilitado por um administrador de loja.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL General]** e escolha **[!UICONTROL B2B Features]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Order Approval Configuration]** seção.

   ![Configuração de aprovação de pedido](./assets/b2b-features-order-approval.png){width="600"}

1. Para permitir que as empresas criem suas próprias ordens de compra, defina **[!UICONTROL Enable Purchase Orders]** para `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

   O recurso de pedidos de compra é ativado no nível do site. Para habilitar esse tipo de pedido para uma empresa, faça o mesmo com as configurações apropriadas em cada [perfil da empresa](account-company-manage.md).

## Configurar ordens de compra

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Localize a empresa na lista e clique em **[!UICONTROL Edit]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Advanced Settings]** seção.

1. Definir **[!UICONTROL Enable Purchase Orders]** para `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save]**.

Após a ativação, a variável **[!UICONTROL Approval Rules]** seção é exibida na loja [Painel da conta](../customers/account-dashboard.md) para um administrador de empresa.

>[!NOTE]
>
>O acesso à ordem de compra na loja deve ser concedido pelo administrador da empresa com base em [permissões de função de usuário da empresa](account-company-roles-permissions.md).

## Configurar pagamento por conta

Pagamento em Conta é um método de pagamento offline que permite que as empresas façam compras até o limite de crédito especificado em seus perfis. O pagamento por conta pode ser ativado globalmente ou por empresa e é exibido durante o check-out somente se estiver ativado. Quando _Pagamento por conta_ for usada como um método de pagamento, uma mensagem será exibida na parte superior do pedido indicando o status da conta. Para configurar esse método de pagamento para uma empresa específica, consulte [Gerenciar contas da empresa](account-company-manage.md).

>[!NOTE]
>
>O pagamento por conta não é suportado para pedidos com [vários endereços de entrega](../stores-purchase/shipping-settings.md#multiple-addresses) e não aparecerá entre as opções de pagamento para esses pedidos.

Para habilitar o Pagamento por Conta na sua loja:

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Payment on Account]** seção.

   ![Pagamento por conta](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >Se necessário, primeiro desmarque a opção **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para permitir pagamento por conta, defina **[!UICONTROL Enabled]** para `Yes`.

1. Insira um **[!UICONTROL Title]** que identifica o método de pagamento durante a finalização da compra, ou você pode aceitar a `Payment on Account` título padrão.

1. Se os pedidos normalmente aguardam aprovação, aceite o padrão **[!UICONTROL New Order Status]** as `Pending` até ser aprovado.

   Se preferir, você pode usar o `Processing` ou `Suspected Fraud` status de novos pedidos com este método de pagamento.

1. Definir **[!UICONTROL Payment from Applicable Countries]** a um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificado na configuração da loja pode usar esse método de pagamento.
   - `Specific Countries` - Após escolher essa opção, a variável _[!UICONTROL Payment from Specific Countries]_é exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Definir **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** aos valores do pedido necessários para se qualificar para este método de pagamento.

   >[!NOTE]
   >
   >Um pedido é qualificado se o total cair entre, ou exatamente corresponder, aos valores totais mínimo ou máximo.

1. Insira um **[!UICONTROL Sort Order]** número que define a posição deste item na lista de métodos de pagamento exibida durante o check-out.

   O valor é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
