---
title: Configurar comunicações por email
description: Saiba como configurar comunicações por email, incluindo o roteamento de emails retornados ou respostas a um endereço de email específico.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Configurar comunicações por email

A variável _Configurações de envio de email_ fornecer a capacidade de encaminhar emails retornados ou respostas para um endereço específico. Se o armazenamento estiver sendo executado em um servidor SMTP ou Windows, você poderá verificar as configurações do host e da porta.

>[!IMPORTANT]
>
>**Aviso de segurança** Todos os comerciantes devem definir imediatamente sua configuração de envio de email para proteger contra uma possível exploração de execução remota de código recentemente identificada. Até que esse problema seja resolvido, é altamente recomendável que você evite usar [!DNL Sendmail] para comunicações por email. No _[!UICONTROL Mail Sending Settings]_, verifique se_[!UICONTROL Set Return Path]_ está definida como `No`.

Para obter uma lista detalhada das definições de configuração, consulte [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) no _Referência de configuração_.

## Configurar comunicações por email

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Mail Sending Settings]** e faça o seguinte:

   ![Configuração avançada - configurações de envio de email](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Se necessário, defina **[!UICONTROL Disable Email Communications]** para `No`.

   - Para **[!UICONTROL Transport]**, escolha o tipo de transporte para comunicações por email na loja: `Sendmail` ou `SMTP`

   - Se estiver executando em um servidor SMTP ou Windows, verifique as seguintes configurações:

      - **[!UICONTROL Host]** - `localhost` ou outro

      - **[!UICONTROL Port (25)]** - `25` ou outro

   - Para **[!UICONTROL Set Return Path]**, escolha uma das seguintes opções:

      - `No` - (Medida de segurança recomendada) Encaminha o email retornado para o endereço de email de armazenamento padrão.
      - `Yes` - Encaminha o email retornado para o endereço de email de armazenamento padrão.
      - `Specified` - Encaminha o email retornado para o endereço de email especificado em **[!UICONTROL Return Path Email]**.

   - Se estiver executando em um servidor SMTP, configure a conexão:

      - **[!UICONTROL Username]** - Digite o nome de usuário de login do servidor SMTP.
      - **[!UICONTROL Password]** - Digite a senha para fazer logon no servidor SMTP.
      - **[!UICONTROL Auth]** - Escolha o tipo de autenticação para a conexão do servidor SMTP: `NONE` , `PLAIN`ou `LOGIN`
      - **[!UICONTROL SSL]** - Escolha o tipo de verificação para o certificado de segurança do servidor: `SSL` ou `TLS`

     ![Configuração avançada - configurações de envio de email](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales Emails]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL General Settings]** seção.

1. Definir **[!UICONTROL Asynchronous sending]** para `Enable`.

   ![Configuração de vendas - configurações gerais de email](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada das definições de configuração, consulte [_Configurações gerais_](../configuration-reference/sales/sales-emails.md) no _Referência de configuração_.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
