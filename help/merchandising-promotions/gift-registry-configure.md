---
title: Configurar registros de presentes
description: Saiba como habilitar registros de presentes e configurar as notificações por email relacionadas.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '356'
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

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Gift Registry]**

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL General Options]** e faça o seguinte:

   ![Configuração de clientes - Registro de presentes geral](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - O Registro de presentes é ativado por padrão. Se necessário, defina **[!UICONTROL Enable Gift Registry]** para `Yes`.

   - Para **[!UICONTROL Maximum Registrants]**, insira o número máximo de pessoas que podem ser convidadas para participar de um evento de registro de presentes.

## Etapa 2. Configurar notificações por e-mail

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Owner Notification]** e faça o seguinte:

   ![Configuração de clientes - Notificação do proprietário do registro de presentes](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Escolha o **[!UICONTROL Email Template]** que notifica os proprietários do registro de presentes quando seus registros são criados.

   - Escolha o [armazenar contato](../getting-started/store-details.md#store-email-addresses) que aparece como a **[!UICONTROL Email Sender]** da mensagem.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Gift Registry Sharing]** e faça o seguinte:

   ![Configuração dos clientes - Compartilhamento do registro de presentes](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Escolha o **[!UICONTROL Email Template]** que notifica os recipients do registro de presentes quando um registro é compartilhado com eles.

   - Escolha a identificação da loja que aparece como a **[!UICONTROL Email Sender]** da mensagem.

   - Para **[!UICONTROL Maximum Sent Emails Threshold]**, insira o número máximo de emails que podem ser enviados de uma vez.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Gift Registry Update]** e faça o seguinte:

   ![Configuração de clientes - Atualização do registro de presentes](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Escolha o **[!UICONTROL Email Template]** que notifica os proprietários do registro de presentes sobre alterações no registro.

   - Escolha a identificação da loja que aparece como a **[!UICONTROL Email Sender]** da mensagem.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, atualize o cache.

   Depois que o cache for atualizado, o Registro de presentes será exibido no menu Lojas em Outras configurações e ficará disponível nas contas do cliente.
