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

As _Configurações de Envio de Emails_ oferecem a capacidade de encaminhar emails retornados ou respostas a emails para um endereço específico. Se o armazenamento estiver sendo executado em um servidor SMTP ou Windows, você poderá verificar as configurações do host e da porta.

>[!IMPORTANT]
>
>**Aviso de segurança** Todos os comerciantes devem definir imediatamente sua configuração de envio de email para proteger contra uma possível exploração de execução remota de código recentemente identificada. Até que esse problema seja resolvido, é altamente recomendável que você evite usar o [!DNL Sendmail] para comunicações por email. Em _[!UICONTROL Mail Sending Settings]_, verifique se_[!UICONTROL Set Return Path]_ está definido como `No`.

Para obter uma lista detalhada das definições de configuração, consulte [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) na _Referência de Configuração_.

## Configurar comunicações por email

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Mail Sending Settings]** e faça o seguinte:

   ![Configuração avançada - configurações de envio de email](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Se necessário, defina **[!UICONTROL Disable Email Communications]** como `No`.

   - Para **[!UICONTROL Transport]**, escolha o tipo de transporte para comunicações por email do armazenamento: `Sendmail` ou `SMTP`

   - Se estiver executando em um servidor SMTP ou Windows, verifique as seguintes configurações:

      - **[!UICONTROL Host]** - `localhost` ou outro

      - **[!UICONTROL Port (25)]** - `25` ou outro

   - Para **[!UICONTROL Set Return Path]**, escolha uma das seguintes opções:

      - `No` - (Medida de segurança recomendada) Roteia emails retornados ao endereço de email de armazenamento padrão.
      - `Yes` - Roteia o email retornado para o endereço de email de armazenamento padrão.
      - `Specified` - Roteia o email retornado para o endereço de email especificado em **[!UICONTROL Return Path Email]**.

   - Se estiver executando em um servidor SMTP, configure a conexão:

      - **[!UICONTROL Username]** - Digite o nome de usuário de logon do servidor SMTP.
      - **[!UICONTROL Password]** - Digite a senha para fazer logon no servidor SMTP.
      - **[!UICONTROL Auth]** - Escolha o tipo de autenticação para a conexão do servidor SMTP: `NONE`, `PLAIN` ou `LOGIN`
      - **[!UICONTROL SSL]** - Escolha o tipo de verificação para o certificado de segurança do servidor: `SSL` ou `TLS`

     ![Configuração avançada - configurações de envio de email](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales Emails]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL General Settings]**.

1. Defina **[!UICONTROL Asynchronous sending]** como `Enable`.

   ![Configuração de vendas - configurações gerais de email](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada das definições de configuração, consulte [_Configurações Gerais_](../configuration-reference/sales/sales-emails.md) na _Referência de Configuração_.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
