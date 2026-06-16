---
title: Notificação de falha de pagamento
description: Saiba como configurar comunicações por email para um método de pagamento que não conclui uma transação.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
TQID: https://experienceleague.adobe.com/ZnVr9N90qZ58fJARyOw4rAecOhQF6KLmJZSBJflgMKc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 235
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
