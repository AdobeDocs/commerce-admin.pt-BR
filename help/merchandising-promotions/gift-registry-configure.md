---
title: Configurar registros de presentes
description: Saiba como habilitar registros de presentes e configurar as notificações por email relacionadas.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
TQID: https://experienceleague.adobe.com/a7DRiAPSkWhBIPdXPXnH3HB1uw9d4WY4vXOtfgg9kRY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 358
ht-degree: 0%

---

# Configurar registros de presentes

{{ee-feature}}

Antes de oferecer registros de presentes aos clientes, você deve habilitar os registros de presentes e configurar as notificações por email relacionadas. O Adobe Commerce envia as seguintes notificações por email em resposta a eventos no fluxo de trabalho de registro de presentes.

- Quando um novo registro de presente é criado, um email é enviado ao proprietário com um link para o registro que pode ser compartilhado.
- Como opção, a loja pode enviar uma notificação com um link para o registro do presente para amigos e familiares do proprietário do registro do presente.
- O proprietário é notificado quando os itens são comprados do registro de presentes, mas não indica o comprador.

A Adobe Commerce tem modelos predefinidos para cada uma dessas mensagens de email que podem ser personalizados para sua marca.

## Etapa 1. Habilitar Registros de Presentes

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Gift Registry]**

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL General Options]** e faça o seguinte:

   ![Configuração de clientes - registro geral do presente](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - O Registro de presentes é ativado por padrão. Se necessário, defina **[!UICONTROL Enable Gift Registry]** como `Yes`.

   - Para **[!UICONTROL Maximum Registrants]**, insira o número máximo de pessoas que podem ser convidadas para participar de um evento de registro de presente.

## Etapa 2. Configurar notificações por e-mail

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Owner Notification]** e faça o seguinte:

   ![Configuração de clientes - notificação de proprietário do Registro de presente](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Escolha o **[!UICONTROL Email Template]** que notifica os proprietários do registro de presentes quando seus registros são criados.

   - Escolha o [contato de armazenamento](../getting-started/store-details.md#store-email-addresses) que aparece como o **[!UICONTROL Email Sender]** da mensagem.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Gift Registry Sharing]** e faça o seguinte:

   ![Configuração de clientes - compartilhamento do registro de presentes](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Escolha o **[!UICONTROL Email Template]** que notifica os destinatários do Registro de presente quando um Registro é compartilhado com eles.

   - Escolha a identificação de armazenamento que aparece como o **[!UICONTROL Email Sender]** da mensagem.

   - Para **[!UICONTROL Maximum Sent Emails Threshold]**, insira o número máximo de emails que podem ser enviados de uma vez.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Gift Registry Update]** e faça o seguinte:

   ![Configuração de clientes - atualização do Registro de presentes](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Escolha o **[!UICONTROL Email Template]** que notifica os proprietários do Registro de presente sobre alterações no Registro.

   - Escolha a identificação de armazenamento que aparece como o **[!UICONTROL Email Sender]** da mensagem.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, atualize o cache.

   Depois que o cache for atualizado, o Registro de presentes será exibido no menu Lojas em Outras configurações e ficará disponível nas contas do cliente.
