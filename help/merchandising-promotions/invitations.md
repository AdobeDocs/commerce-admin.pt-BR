---
title: Convites de evento
description: Saiba como os clientes podem enviar e exibir convites para eventos e vendas privadas no painel de suas contas de clientes.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Convites de evento

{{ee-feature}}

Quando os convites estão habilitados, os clientes podem enviar e exibir convites no painel de suas contas de cliente. O email de convite inclui um link para a página de logon do cliente da sua loja.

## Meus convites

A variável _[!UICONTROL My Invitations]_seção da conta do cliente lista todos os convites enviados pelo cliente. Os clientes podem enviar convites para amigos e familiares para eventos de loja, registros de presentes, listas de desejos e assim por diante.

![Meus convites](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Fluxo de trabalho do convite

1. **O cliente prepara os convites**: no painel de conta, o cliente prepara a lista de recipients e conclui o convite. Uma mensagem personalizada pode ser incluída, dependendo da configuração.
1. **O cliente envia convites**: Quando estiver pronto, o cliente clica no ícone _[!UICONTROL Send Invitations]_botão.
1. **O sistema gerencia a transmissão**: o sistema envia convites em lotes, de acordo com o número definido na configuração.
1. **O cliente monitora a resposta**: o cliente monitora o status de cada convite no painel de conta, conforme `Sent`, `Accepted`ou `Canceled`.

### Enviar um convite

1. Na barra lateral da conta na loja, o cliente escolhe **[!UICONTROL My Invitations]**.

1. No _Meu convite_ página, cliques **[!UICONTROL Send Invitation]**.

1. Define o novo item de convite:

   - Preenche as informações de email.

   - (Opcional) Cria um convite com vários endereços clicando em **+** e adicionar outro endereço de email.

     Um único convite tem um limite de cinco endereços de email.

   - (Opcional) Insere uma mensagem de acompanhamento.

1. Ao concluir, clique em **[!UICONTROL Send Invitation]**.

Uma notificação de convite é enviada para o endereço de email do usuário convidado com o link de instruções para definir a conta.

>[!NOTE]
>
>Um usuário pode enviar apenas um convite para um endereço de email específico. Tentar reenviar um convite para o mesmo endereço de email resulta em uma mensagem de erro exibida e o convite não é enviado.

## Habilitar convites para sua loja

A configuração do convite habilita convites para a loja e determina como eles são enviados.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Invitations]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL General]** seção.

   ![Configuração dos clientes - opções gerais de convites](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Enable Invitations Functionality]** para `Yes`.

1. Para permitir que os clientes gerenciem convites da loja, defina **Habilitar Convites na Loja** para `Yes`.

1. Definir **[!UICONTROL Referred Customer Group]** a um dos seguintes:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Definir **[!UICONTROL New Accounts Registration]** a um dos seguintes:

   - `By Invitation Only`
   - `Available to All`

1. Para **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**, selecione `Yes`.

1. Para limitar o número de convites que podem ser enviados de uma vez, insira o número na caixa **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** campo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Email]** e faça o seguinte:

   ![Configuração do cliente - Opções de email de convites](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Selecione a identidade da loja a ser usada como **[!UICONTROL Customer Invitation Email Sender]**.

   - Selecione o **[!UICONTROL Customer Invitation Email Template]** usado para convites enviados.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Enviar e gerenciar convites no Administrador

No [Relatórios de Vendas Privadas](../getting-started/private-sales-reports.md) você pode ver o número de convites enviados durante um período especificado ou de clientes para os quais você enviou convites.

### Criar um convite no Administrador

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. No canto superior direito, clique em **[!UICONTROL Add Invitations]**.

1. Na próxima tela, insira endereços de email para convidar novos clientes, adicionar uma mensagem personalizada, escolher um remetente e selecionar um grupo de convidados.

   Se você tiver várias exibições de loja, use o **[!UICONTROL Send From]** opção para especificar a exibição de loja da qual um convite é enviado.

   ![Informações de convites](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

### Descartar convites para uma única entidade

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Encontre o convite necessário usando filtros e abra-o no modo de edição.

1. No canto superior direito, clique em **[!UICONTROL Discard Invitation]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

### Descartar convites para várias entidades

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Localize e selecione os convites a serem descartados.

1. No canto superior esquerdo, use a **[!UICONTROL Actions]** menu para escolher **[!UICONTROL Discard Selected]** e clique em **[!UICONTROL Submit]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

### Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Select] | Marque a caixa de seleção para selecionar os convites que serão sujeitos a uma ação ou use o controle de seleção no cabeçalho da coluna. Opções: `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | O número de ID interno de um convite |
| [!UICONTROL Email] | Um endereço de email de cliente correspondente |
| [!UICONTROL Invitee] | Email do usuário convidado |
| [!UICONTROL Sent] | Hora e data em que um convite foi enviado |
| [!UICONTROL Registered] | Hora e dados em que um cliente foi registrado |
| [!UICONTROL Status] | Status do convite. Opções: `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | O site correspondente |
| [!UICONTROL Invitee Group] | Um grupo de clientes de um convidado |

{style="table-layout:auto"}
