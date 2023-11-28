---
title: Enviar email para um amigo
description: Saiba como fornecer um link de email que facilita o compartilhamento de links para produtos com seus amigos pelos clientes.
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Enviar email para um amigo

O link Email facilita o compartilhamento de links para produtos entre seus clientes e os amigos deles. Na loja de demonstração Luma, o link de email é exibido como um ícone de envelope. O template de mensagem pode ser personalizado para sua voz e marca. Para evitar spam, você pode limitar o número de recipients para cada email e o número de produtos que podem ser compartilhados por um período de uma hora.

![Exemplo de vitrine - enviar um email a um amigo](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## Configurar email-a-friend

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Email to a Friend]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Email Templates]** e defina as opções:

   ![Configuração do catálogo - modelos de email](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Modelos de e-mail](../configuration-reference/catalog/email-to-a-friend.md) no _Guia de referência de configuração_.

   Para alterar a configuração padrão de qualquer campo, desmarque a opção **[!UICONTROL Use system value]** para tornar o campo editável.

   - Definir **[!UICONTROL Enabled]** para `Yes`.

   - Definir **[!UICONTROL Select Email Template]** ao template que deseja usar como base das mensagens.

   - Se quiser exigir que somente clientes registrados possam enviar emails para amigos, defina **[!UICONTROL Allow for Guests]** para `No`.

   - Para **[!UICONTROL Max Recipients]**, digite o número máximo de amigos que podem estar na lista de distribuição para uma única mensagem.

   - Para **[!UICONTROL Max Products Sent in 1 Hour]**, insira o número máximo de produtos que podem ser compartilhados por um único usuário com amigos em um período de uma hora.

   - Definir **[!UICONTROL Limit Sending By]** para um dos seguintes métodos para identificar o remetente dos emails:

     `IP Address`  - (Recomendado) Identifica o remetente pelo endereço IP do computador usado para enviar os emails.

     `Cookie (unsafe)` - Identifica o remetente pelo cookie do navegador. Esse método é menos eficaz porque o remetente pode excluir o cookie para ignorar o limite.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Enviar email para um amigo na loja

Quando esse recurso estiver configurado, os clientes da loja seguirão estas etapas para compartilhar informações do produto com amigos.

1. Em uma página de catálogo, o cliente clica em **[!UICONTROL Email]** link.

1. Se o recurso estiver configurado apenas para usuários registrados, o executará um dos seguintes procedimentos:

   - Faz logon na conta do cliente.
   - Cadastra-se para obter uma nova conta.

1. Conclui o **[!UICONTROL Message]** e insere o recipient **[!UICONTROL Name]** e **[!UICONTROL Email Address]**.

   Se necessário, o cliente pode adicionar mais recipients:

   - Cliques **[!UICONTROL Add Invitee]**.

   - Insere o **[!UICONTROL Name]** e **[!UICONTROL Email Address]** da pessoa adicional.

     Eles podem enviar a mensagem para quantas pessoas adicionais a configuração permitir. Eles podem remover o convite adicionado clicando no ícone **[!DNL Remove]** link.

1. Quando estiver pronto para enviar a mensagem, clique em **[!UICONTROL Send Email]**.

   ![Exemplo de vitrine - enviar email para um amigo](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
