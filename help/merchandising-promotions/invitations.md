---
title: Convites de evento
description: Saiba como os clientes podem enviar e exibir convites para eventos e vendas privadas no painel de suas contas de clientes.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# Convites de evento

{{ee-feature}}

Quando os convites estão habilitados, os clientes podem enviar e exibir convites no painel de suas contas de cliente. O email de convite inclui um link para a página de logon do cliente da sua loja.

## Meus convites

A seção _[!UICONTROL My Invitations]_&#x200B;da conta do cliente lista todos os convites enviados pelo cliente. Os clientes podem enviar convites para amigos e familiares para eventos de loja, registros de presentes, listas de desejos e assim por diante.

![Meus convites](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Fluxo de trabalho do convite

1. **O cliente prepara os convites**: no painel de contas, o cliente prepara a lista de destinatários e conclui o convite. Uma mensagem personalizada pode ser incluída, dependendo da configuração.
1. **O cliente envia os convites**: quando estiver pronto, o cliente clica no botão _[!UICONTROL Send Invitations]_.
1. **O sistema gerencia a transmissão**: o sistema envia convites em lotes, de acordo com o número definido na configuração.
1. **Resposta do cliente ao monitoramento**: o cliente monitora o status de cada convite no painel de conta, como `Sent`, `Accepted` ou `Canceled`.

### Enviar um convite

1. Na barra lateral da conta na loja, o cliente escolhe **[!UICONTROL My Invitations]**.

1. Na página _Meu Convite_, clique em **[!UICONTROL Send Invitation]**.

1. Define o novo item de convite:

   - Preenche as informações de email.

   - (Opcional) Cria um convite com vários endereços clicando em **+** e adicionando outro endereço de email.

     Um único convite tem um limite de cinco endereços de email.

   - (Opcional) Insere uma mensagem de acompanhamento.

1. Quando terminar, clica em **[!UICONTROL Send Invitation]**.

Uma notificação de convite é enviada para o endereço de email do usuário convidado com o link de instruções para definir a conta.

>[!NOTE]
>
>Um usuário pode enviar apenas um convite para um endereço de email específico. Tentar reenviar um convite para o mesmo endereço de email resulta em uma mensagem de erro exibida e o convite não é enviado.

## Habilitar convites para sua loja

A configuração do convite habilita convites para a loja e determina como eles são enviados.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Invitations]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL General]**.

   ![Configuração de clientes - opções gerais de convites](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Enable Invitations Functionality]** como `Yes`.

1. Para permitir que os clientes gerenciem convites da vitrine, defina **Habilitar Convites na Vitrine** como `Yes`.

1. Defina **[!UICONTROL Referred Customer Group]** como um dos seguintes:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Defina **[!UICONTROL New Accounts Registration]** como um dos seguintes:

   - `By Invitation Only`
   - `Available to All`

1. Para **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**, selecione `Yes`.

1. Para limitar o número de convites que podem ser enviados de uma vez, insira o número no campo **[!UICONTROL Max Invitations Allowed to be Sent at One Time]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Email]** e faça o seguinte:

   ![Configuração de clientes - opções de email de convites](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Selecione a identidade de armazenamento a ser usada como **[!UICONTROL Customer Invitation Email Sender]**.

   - Selecione o **[!UICONTROL Customer Invitation Email Template]** usado para convites enviados.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Enviar e gerenciar convites no Administrador

Na seção [Relatórios de Vendas Particulares](../getting-started/private-sales-reports.md), você pode ver o número de convites enviados durante um período especificado ou de clientes para os quais você enviou convites.

### Criar um convite no Administrador

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. No canto superior direito, clique em **[!UICONTROL Add Invitations]**.

1. Na próxima tela, insira endereços de email para convidar novos clientes, adicionar uma mensagem personalizada, escolher um remetente e selecionar um grupo de convidados.

   Se você tiver vários modos de exibição de armazenamento, use a opção **[!UICONTROL Send From]** para especificar o modo de exibição de armazenamento a partir do qual um convite é enviado.

   ![Informações sobre convites](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

### Descartar convites para uma única entidade

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Encontre o convite necessário usando filtros e abra-o no modo de edição.

1. No canto superior direito, clique em **[!UICONTROL Discard Invitation]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

### Descartar convites para várias entidades

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Localize e selecione os convites a serem descartados.

1. Na parte superior esquerda, use o menu **[!UICONTROL Actions]** para escolher **[!UICONTROL Discard Selected]** e clique em **[!UICONTROL Submit]**.

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
