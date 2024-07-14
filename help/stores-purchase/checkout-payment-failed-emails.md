---
title: Notificação de falha de pagamento
description: Saiba como configurar comunicações por email para um método de pagamento que não conclui uma transação.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Notificação de falha de pagamento

Uma notificação será enviada ao contato da loja ou a um usuário Admin designado se o método de pagamento selecionado durante a finalização da compra não concluir a transação.

## Etapa 1: atualizar o modelo de email

Atualize o modelo de email necessário para refletir a marca. Para obter uma lista completa de modelos, consulte [Lista de Modelos de Email](../systems/email-templates.md#email-template-list).

## Etapa 2: configurar os emails de pagamento com falha

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Checkout]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Payment Failed Emails]**.

   ![Emails de Pagamento com Falha](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Defina as opções para emails de pagamento com falha:

   - Defina **[!UICONTROL Payment Failed Email Sender]** para o contato de armazenamento que aparece como remetente da mensagem.
   - Defina **[!UICONTROL Payment Failed Email Receiver]** para o contato de armazenamento que receberá notificações de falha nas transmissões de email.
   - Defina **[!UICONTROL Payment Failed Template]** com o modelo que é usado para o email enviado quando o método de pagamento falhar durante o check-out.

1. Para **[!UICONTROL Send Payment Failed Email Copy To]**, insira o endereço de email de qualquer pessoa que deva receber uma cópia da notificação de falha no pagamento.

   Se estiver enviando uma cópia para vários destinatários, separe cada endereço com uma vírgula.

1. Defina **[!UICONTROL Payment Failed Copy Method]** como um dos seguintes:

   - `Bcc` - Envia uma _cópia de cortesia oculta_ ao incluir o destinatário no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
   - `Separate Email` - Envia a cópia como um email separado.

1. Clique em **[!UICONTROL Save Config]**.
