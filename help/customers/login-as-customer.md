---
title: Fornecer assistência ao comprador
description: Ao usar o recurso Fazer logon como cliente, você pode ver o que os clientes veem e fazer atualizações em seu nome.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Fornecer assistência ao comprador

Às vezes, os clientes precisam de ajuda com seu pedido. Os administradores de armazenamento podem usar _Fazer logon como cliente_, que permite que eles vejam o que o cliente vê e façam atualizações para ajudá-los.

Quaisquer ações executadas durante o logon como cliente são aplicadas à conta do cliente real.

Quando estiver ativado para um _Admin_ usuário, a variável _[!UICONTROL Login as Customer]_O botão é exibido em várias páginas:

* [Página Customer Edit](../customers/update-account.md)
* [Página de exibição de pedidos](../stores-purchase/order-processing.md)
* [Página de Exibição da Fatura](../stores-purchase/invoices.md)
* [Página de Exibição da Remessa](../stores-purchase/shipments.md)
* [Página View de Aviso de Crédito](../stores-purchase/credit-memo-create.md)

![Fazer logon como cliente](assets/login-as-customer.png){width="600" zoomable="yes"}

## Ativar o login como cliente

Ativando _Fazer logon como cliente_ exige que você ative o recurso na instância do Commerce e, em seguida, ative o acesso para usuários Administradores nas permissões de função de usuário.

### Ativar o recurso

1. Na barra lateral Admin, acesse  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha  **[!UICONTROL Login as Customer]**.

   ![Opções de configuração - Fazer logon como cliente](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Enable Login as Customer]** para `Yes`.

1. _(Opcional)_ Definir **[!UICONTROL Disable Page Cache for Admin User]** para `No` para habilitar o cache da página quando o usuário administrador faz logon como cliente.

   >[!WARNING]
   >
   > Desabilitação do cache de páginas (`Yes` - padrão) garante que o usuário que está fazendo logon como Cliente obtenha dados novos e não armazenados em cache.

1. _(Opcional)_ Definir **[!UICONTROL Store View to Log in]** para `Manual Selection` se você tiver uma configuração de vários sites e/ou de várias lojas e quiser que o usuário administrador selecione a visualização de loja ao fazer logon como cliente.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Habilitar o acesso para usuários administradores

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _Permissões_ > **[!UICONTROL User Roles]**.

1. Clique na função na lista.

1. No [!UICONTROL _Informações da função_] painel esquerdo, clique em **[!UICONTROL Role Resources]**.

1. Alterar **[!UICONTROL Role Resources]** na página para `Custom`.

   >[!INFO]
   >
   > Com essa opção selecionada, a hierarquia de recursos é exibida na página.

1. Role para a  **[!UICONTROL Customers]** item pai e a variável **[!UICONTROL Login as Customer]** item abaixo. Em seguida, selecione os recursos que deseja habilitar para a função:

   * **[!UICONTROL Allow Login as Customer]** - Permite que o usuário administrador use a variável _Fazer logon como cliente_ recurso.
   * **[!UICONTROL View Login as Customer Log]** - Permite que o usuário administrador veja a variável _Fazer logon como cliente_ Log.

   ![Recursos da função - Fazer logon como cliente](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Clique em **[!UICONTROL Save Role]**.

## Faça logon como cliente no Administrador

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > [!UICONTROL _Todos os Clientes_].

1. Abra um usuário no modo de edição.

1. No **[!UICONTROL Customer Information]** escolha o **[!UICONTROL Account Information]** seção.

1. Defina o **[!UICONTROL Allow remote shopping assistance]** para `Yes`.

   >[!INFO]
   >
   >O administrador agora pode fazer logon como usuário sem a permissão da loja.

## Permissão de conta do cliente para assistência remota a compras

Para habilitar o acesso à conta para a equipe de suporte da loja do Administrador, um cliente deve habilitar o recurso para sua conta:

1. O cliente acessa o **[!UICONTROL Account Information]** página.

1. Seleciona o **[!UICONTROL Allow remote shopping assistance]** caixa de seleção

1. Cliques do cliente **[!UICONTROL Save]**.

![Página de informações da conta](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>Sem essa permissão, um usuário administrador não pode fazer logon como esse cliente.

## Usar o login como cliente

>[!INFO]
>
>Para usar _Fazer logon como cliente_, certifique-se de que seu Administrador esteja configurado conforme descrito anteriormente.

_Fazer logon como cliente_ O permite que você veja o site da mesma forma que o cliente, e que você solucione problemas e execute outras ações para o cliente. Se você tiver uma função de usuário atribuída com as permissões necessárias:

1. Você pode clicar em **[!UICONTROL Login as Customer]** nas páginas listadas na seção anterior.
1. As ações Fazer logon como cliente estão disponíveis no Relatório de ações.

>[!WARNING]
>
>Qualquer ação realizada durante o logon [!UICONTROL _como cliente_] (como adicionar/remover produtos) são aplicados ao pedido real do cliente. Na loja, um banner é exibido quando você está `logged in as customer_name` para fornecer um lembrete do estado especial.

## Fazer logon como Registro do cliente

{{ee-feature}}

O Adobe Commerce fornece um registro para a _Fazer logon como cliente_ ações. Ela lista todas as sessões em que um usuário administrador acessa o recurso. Para acessar as ações registradas, vá para a [Relatório de ações do administrador](../systems/action-log-report.md).

É possível filtrar a configuração do relatório **[!UICONTROL Action Group]** para `Login As Customer` na parte superior da página e clicando em **[!UICONTROL Search]**.

![Filtrar o relatório de ações](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
