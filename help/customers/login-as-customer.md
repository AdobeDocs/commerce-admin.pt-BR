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

Às vezes, os clientes precisam de ajuda com seu pedido. Os administradores de loja podem usar o _Logon como Cliente_, o que permite que eles vejam o que o cliente vê e façam atualizações para ajudá-los.

Quaisquer ações executadas durante o logon como cliente são aplicadas à conta do cliente real.

Quando habilitado para um usuário _Administrador_, o botão _[!UICONTROL Login as Customer]_aparece em várias páginas:

* [Página Customer Edit](../customers/update-account.md)
* [Página de exibição de pedidos](../stores-purchase/order-processing.md)
* [Página de Exibição da Fatura](../stores-purchase/invoices.md)
* [Página de Exibição da Remessa](../stores-purchase/shipments.md)
* [Página View de Aviso de Crédito](../stores-purchase/credit-memo-create.md)

![Fazer Logon Como Cliente](assets/login-as-customer.png){width="600" zoomable="yes"}

## Ativar o login como cliente

Habilitar o _Logon como Cliente_ exige que você habilite o recurso em sua instância do Commerce e, em seguida, habilite o acesso para usuários Administradores nas permissões de função de usuário.

### Ativar o recurso

1. Na barra lateral Admin, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Login as Customer]**.

   ![Opções de configuração - Fazer logon como cliente](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Enable Login as Customer]** como `Yes`.

1. _(Opcional)_ Defina **[!UICONTROL Disable Page Cache for Admin User]** como `No` para habilitar o cache de páginas quando o usuário Administrador fizer logon como cliente.

   >[!WARNING]
   >
   > Desabilitar o cache de página (`Yes` - padrão) garante que o usuário que está fazendo logon como Cliente obtenha dados novos e não armazenados em cache.

1. _(Opcional)_ Defina **[!UICONTROL Store View to Log in]** como `Manual Selection` se você tiver uma configuração de vários sites e/ou de várias lojas e quiser que o usuário Administrador selecione a exibição de loja ao fazer logon como cliente.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Habilitar o acesso para usuários administradores

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _Permissões_ > **[!UICONTROL User Roles]**.

1. Clique na função na lista.

1. No painel esquerdo [!UICONTROL _Informações da função_], clique em **[!UICONTROL Role Resources]**.

1. Alterar **[!UICONTROL Role Resources]** na página para `Custom`.

   >[!INFO]
   >
   > Com essa opção selecionada, a hierarquia de recursos é exibida na página.

1. Role até o item pai **[!UICONTROL Customers]** e o item **[!UICONTROL Login as Customer]** abaixo. Em seguida, selecione os recursos que deseja habilitar para a função:

   * **[!UICONTROL Allow Login as Customer]** - Permite que o usuário Administrador use o recurso _Fazer logon como Cliente_.
   * **[!UICONTROL View Login as Customer Log]** - Permite que o usuário Administrador veja o Log de _Logon como Cliente_.

   ![Recursos da função - Fazer logon como cliente](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Clique em **[!UICONTROL Save Role]**.

## Faça logon como cliente no Administrador

1. Na barra lateral _Administrador_, vá para **[!UICONTROL Customers]** > [!UICONTROL _Todos os Clientes_].

1. Abra um usuário no modo de edição.

1. No painel **[!UICONTROL Customer Information]**, escolha a seção **[!UICONTROL Account Information]**.

1. Defina o **[!UICONTROL Allow remote shopping assistance]** como `Yes`.

   >[!INFO]
   >
   >O administrador agora pode fazer logon como usuário sem a permissão da loja.

## Permissão de conta do cliente para assistência remota a compras

Para habilitar o acesso à conta para a equipe de suporte da loja do Administrador, um cliente deve habilitar o recurso para sua conta:

1. O cliente acessa a página **[!UICONTROL Account Information]**.

1. Marca a caixa de seleção **[!UICONTROL Allow remote shopping assistance]**.

1. O cliente clica em **[!UICONTROL Save]**.

![Página de informações da conta](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>Sem essa permissão, um usuário administrador não pode fazer logon como esse cliente.

## Usar o login como cliente

>[!INFO]
>
>Para usar o _Logon como Cliente_, verifique se seu Administrador está configurado conforme descrito anteriormente.

_Fazer logon como Cliente_ permite que você veja o site da mesma maneira que o cliente, e permite que você solucione problemas e execute outras ações para o cliente. Se você tiver uma função de usuário atribuída com as permissões necessárias:

1. Você pode clicar em **[!UICONTROL Login as Customer]** nas páginas listadas na seção anterior.
1. As ações Fazer logon como cliente estão disponíveis no Relatório de ações.

>[!WARNING]
>
>Todas as ações executadas durante o logon em [!UICONTROL _como Cliente_] (como adicionar/remover produtos) são aplicadas ao pedido real do cliente. Na loja, um banner é exibido quando você está `logged in as customer_name` para fornecer um lembrete do estado especial.

## Fazer logon como Registro do cliente

{{ee-feature}}

A Adobe Commerce fornece um log para as ações _Fazer Logon como Cliente_. Ela lista todas as sessões em que um usuário administrador acessa o recurso. Para acessar as ações registradas, vá para o [Relatório de Ações do Administrador](../systems/action-log-report.md).

Você pode filtrar a configuração do relatório **[!UICONTROL Action Group]** para `Login As Customer` na parte superior da página e clicar em **[!UICONTROL Search]**.

![Filtrar o Relatório de Ações](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
