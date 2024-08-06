---
title: Habilitar recursos B2B
description: Saiba mais sobre como ativar recursos B2B para sua loja da Adobe Commerce, incluindo contas da empresa, métodos padrão de pagamento e envio, ordens de compra e aprovações de pedidos.
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 7e36d0b7c9b414cb072118b87cd903b3374bb9de
workflow-type: tm+mt
source-wordcount: '1630'
ht-degree: 0%

---

# Habilitar recursos B2B

Por padrão, todos os recursos B2B são inicialmente desativados. Um administrador de loja pode ativar ou desativar os recursos B2B conforme necessário para lojas Commerce. Para obter uma lista completa de definições de configuração B2B, consulte [Referência de configuração de Recursos B2B](../configuration-reference/general/b2b-features.md).

Quando você habilita o suporte para empresas do cliente, os recursos B2B adicionais são habilitados automaticamente:

- [!DNL Shared Catalog]

  Oferece suporte à configuração de preço personalizado para diferentes empresas e também permite permissões de categoria para todas as lojas.

- [!DNL Enable Shared Catalog direct products price assigning]

  Melhora o desempenho do site, armazenando somente os produtos atribuídos a um catálogo compartilhado no índice de preços. Habilitar esse recurso é uma prática recomendada para comerciantes que têm muitos catálogos compartilhados para gerenciar preços personalizados para diferentes empresas.

- [!DNL B2B Quotes]

  Oferece aos vendedores e compradores da empresa a capacidade de negociar preços.

- [!DNL B2B default payment and shipping methods]

  Determina a seleção das opções de pagamento e envio disponíveis para compradores B2B na loja.

As definições das configurações desses recursos ficam visíveis somente quando [!DNL Enable Company] está definido como `Yes`.

Os recursos [!DNL Quick Order] e [!DNL Requisition List] B2B podem ser habilitados e desabilitados independentemente.

## Configurar recursos B2B

As opções para configurar recursos B2B do Adobe Commerce estão disponíveis apenas em projetos Commerce que têm a [extensão B2B do Adobe Commerce instalada](install.md).

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   Se você tiver uma instalação multissite, defina o controle **[!UICONTROL Store View]** no canto superior esquerdo para o site onde a configuração se aplica.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL B2B Features]**:

   ![Configuração B2B - geral](./assets/b2b-features.png){width="600"}

   - Permitir que os clientes gerenciem suas próprias contas da empresa e habilitem o suporte para recursos B2B adicionais definindo **[!UICONTROL Enable Company]** como `Yes`.

     Quando você ativa o suporte da empresa, o Catálogo compartilhado, a Cotação B2B, os Métodos de pagamento B2B e os Métodos de envio B2B são ativados automaticamente.

   - Para permitir que clientes e convidados façam pedidos rapidamente com base no SKU ou no nome do produto, defina **[!UICONTROL Enable Quick Order]** como `Yes`.

   - Para permitir que os clientes criem e gerenciem listas de requisições a partir do painel de contas, defina **[!UICONTROL Enable Requisition List]** como `Yes`.

     Você também pode [configurar o número máximo de listas](configure-requisition-lists.md) que um cliente pode ter para sua conta.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar métodos padrão de pagamento e envio B2B

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Default B2B Payment Methods]**.

1. Para estabelecer os métodos de pagamento padrão para ordens B2B, defina **[!UICONTROL Applicable Payment Methods]** como um dos seguintes:

   - `All Payment Methods`

   - `Selected Payment Methods`

     Para a opção específica, selecione o **[!UICONTROL Payment Methods]** que você deseja disponibilizar para seus clientes mantendo pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) enquanto clica em cada opção.

   A lista de [métodos de pagamento](../configuration-reference/sales/payment-methods.md) mostra quais opções estão atualmente habilitadas ou desabilitadas em sua loja. Além dos métodos de pagamento padrão, a lista também inclui o seguinte:

   - Nenhuma informação de pagamento é necessária
   - [Pagamento por conta](#configure-payment-on-account)
   - Contas armazenadas
   - Cartões armazenados

   ![Configuração B2B - configurações do método de pagamento padrão](./assets/b2b-features-default-payment-methods.png){width="600"}

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Default B2B Shipping Methods]**.

1. Para especificar os métodos de envio padrão para ordens B2B, defina **[!UICONTROL Applicable Shipping Methods]** como um dos seguintes:

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     Para a opção específica, selecione o **[!UICONTROL Shipping Methods]** que você deseja disponibilizar para seus clientes mantendo pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) enquanto clica em cada opção.

     A lista de métodos de envio mostra quais estão atualmente [habilitados ou desabilitados](../configuration-reference/sales/delivery-methods.md).

   ![Configuração B2B - métodos de envio padrão](./assets/b2b-features-shipping-methods.png){width="600"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar opções de email da empresa

O [representante de vendas](account-company-manage.md#assign-a-sales-representative) que é atribuído como o contato principal de uma empresa é configurado por padrão como o remetente de muitas mensagens de email automatizadas enviadas para a empresa.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Company Configuration]**.

1. Se necessário, defina **[!UICONTROL Store View]** para o modo de exibição de repositório para definir o [escopo](../getting-started/websites-stores-views.md#scope-settings) da configuração.

1. Conclua a seção **[!UICONTROL Company Registration]**:

   >[!NOTE]
   >
   >Desmarque a caixa de seleção **[!UICONTROL Use system value]** para tornar o campo editável.

   - Defina **[!UICONTROL Company Registration Email Recipient]** como [contato da loja](../getting-started/store-details.md#store-email-addresses) que deverá ser notificado quando uma nova solicitação de registro da empresa for recebida.

   - Para **[!UICONTROL Send Company Registration Email Copy To]**, insira o endereço de email de cada pessoa que receberá uma cópia da notificação de registro. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **Método de cópia de email** como um dos seguintes:

      - `Bcc` - Envia uma _cópia de cortesia oculta_ ao incluir o destinatário no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você preparou um modelo de email que deve ser usado em vez do padrão, defina **[!UICONTROL Default Company Registration Email]** como o nome do modelo. Por padrão, o modelo `Company Registration Request` é usado.

     ![Configuração de clientes - registro de empresa](./assets/company-email-options-company-registration.png){width="600"}

1. Conclua a seção **[!UICONTROL Customer-Related Emails]**:

   Se você preparou modelos de email alternativos a serem usados em vez dos padrões, escolha o modelo que deseja usar para cada um dos seguintes:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuração dos clientes - emails relacionados ao cliente](./assets/company-email-options-customer-related-emails.png){width="600"}

1. Conclua a seção **[!UICONTROL Company Status Change]**:

   - Para **[!UICONTROL Send Company Status Change Email Copy To]**, insira o endereço de email de cada pessoa que receberá uma cópia da notificação de alteração de status. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **Método de cópia de email** como um dos seguintes:

      - `Bcc` - Envia uma _cópia de cortesia oculta_ ao incluir o destinatário no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa mudar de `Pending Approval` para `Active`, defina **[!UICONTROL Default 'Company Status Change to Active 1' Email]** como o nome do modelo. Por padrão, o modelo `Company Status Active 1` é usado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa mudar de `Rejected` ou `Blocked` para `Active`, defina **[!UICONTROL Default 'Company Status Change to Active 2' Email]** para o nome do modelo. Por padrão, o modelo `Company Status Active 2` é usado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa for alterado para `Rejected`, defina **[!UICONTROL Default 'Company Status Change to Rejected' Email]** para o nome do modelo. Por padrão, o modelo `Company Status Rejected` é usado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa for alterado para `Blocked`, defina **[!UICONTROL Default 'Company Status Change to Blocked' Email]** para o nome do modelo. Por padrão, o modelo `Company Status Blocked` é usado.

   - Se você preparou um modelo de email a ser usado quando o status da empresa for alterado para `Pending Approval`, defina **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** para o nome do modelo. Por padrão, o modelo `Company Status Pending Approval` é usado.

   ![Configuração de clientes - alteração do status da empresa](./assets/company-email-options-company-status-change.png){width="600"}

1. Conclua a seção **[!UICONTROL Company Credit Emails]**:

   - Defina **[!UICONTROL Company Credit Change Email Sender]** como [contato da loja](../getting-started/store-details.md#store-email-addresses) que deverá ser notificado quando for feita uma alteração no limite de crédito atribuído a uma empresa. Por padrão, a notificação é enviada para o _Representante de vendas_.

   - Para **[!UICONTROL Send Company Credit Change Email Copy To]**, insira o endereço de email de cada pessoa que receberá uma cópia da notificação de alteração de crédito. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **Método de cópia de email** como um dos seguintes:

      - `Bcc` - Envia uma _cópia de cortesia oculta_ ao incluir o destinatário no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
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

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL General]** e escolha **[!UICONTROL B2B Features]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Order Approval Configuration]**.

   ![Configuração de aprovação de pedido](./assets/b2b-features-order-approval.png){width="600"}

1. Para permitir que as empresas criem suas próprias ordens de compra, defina **[!UICONTROL Enable Purchase Orders]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

   O recurso de pedidos de compra é ativado no nível do site. Para habilitar este tipo de pedido para uma empresa, faça o mesmo com as configurações apropriadas em cada [perfil da empresa](account-company-manage.md).

## Configurar ordens de compra

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Localize a empresa na lista e clique em **[!UICONTROL Edit]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advanced Settings]**.

1. Defina **[!UICONTROL Enable Purchase Orders]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save]**.

Após a ativação, a seção **[!UICONTROL Approval Rules]** é exibida no [Painel de Contas](../customers/account-dashboard.md) da vitrine para um administrador de empresa.

>[!NOTE]
>
>O acesso à ordem de compra na loja deve ser concedido pelo administrador da empresa com base em [permissões de função de usuário da empresa](account-company-roles-permissions.md).

## Configurar pagamento por conta

Pagamento em Conta é um método de pagamento offline que permite que as empresas façam compras até o limite de crédito especificado em seus perfis. O pagamento por conta pode ser ativado globalmente ou por empresa e é exibido durante o check-out somente se estiver ativado. Quando o _Pagamento na Conta_ for usado como método de pagamento, uma mensagem aparecerá na parte superior do pedido indicando o status da conta. Para configurar este método de pagamento para uma empresa específica, consulte [Gerenciar Contas da Empresa](account-company-manage.md).

>[!NOTE]
>
>O pagamento por conta não é suportado para pedidos com [vários endereços de envio](../stores-purchase/shipping-settings.md#multiple-addresses) e não aparece entre as opções de pagamento para esses pedidos.

Para habilitar o Pagamento por Conta na sua loja:

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Payment Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Payment on Account]**.

   ![Pagamento na conta](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >Se necessário, primeiro desmarque a caixa de seleção **[!UICONTROL Use system value]** para alterar essas configurações.

1. Para permitir o pagamento por conta, defina **[!UICONTROL Enabled]** como `Yes`.

1. Insira um **[!UICONTROL Title]** que identifique o método de pagamento durante o check-out ou você pode aceitar o título padrão `Payment on Account`.

1. Se os pedidos normalmente esperam por aprovação, aceite o padrão **[!UICONTROL New Order Status]** como `Pending` até que seja aprovado.

   Se preferir, você pode usar o status `Processing` ou `Suspected Fraud` para novos pedidos com esta forma de pagamento.

1. Defina **[!UICONTROL Payment from Applicable Countries]** como um dos seguintes:

   - `All Allowed Countries` - Clientes de todos os [países](../getting-started/store-details.md#country-options) especificados na sua configuração de loja podem usar esta forma de pagamento.
   - `Specific Countries` - Depois que você escolher essa opção, a lista _[!UICONTROL Payment from Specific Countries]_será exibida. Para selecionar vários países, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

1. Defina **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** para os valores do pedido necessários para se qualificar para este método de pagamento.

   >[!NOTE]
   >
   >Um pedido é qualificado se o total cair entre, ou exatamente corresponder, aos valores totais mínimo ou máximo.

1. Insira um número **[!UICONTROL Sort Order]** que defina a posição deste item na lista de métodos de pagamento exibidos durante o check-out.

   O valor é relativo aos outros métodos de pagamento. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
