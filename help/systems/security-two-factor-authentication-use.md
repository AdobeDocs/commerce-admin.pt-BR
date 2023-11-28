---
title: Configuração da autenticação de dois fatores para contas de usuário
description: Saiba como configurar a autenticação de dois fatores durante o logon inicial do Administrador e autenticar sua identidade usando um aplicativo de dispositivo compatível.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Configuração da autenticação de dois fatores para contas de usuário

Estas instruções mostram como configurar a autenticação de dois fatores durante o logon inicial na Adobe Commerce ou no Magento Open Source e como autenticar sua identidade usando os seguintes aplicativos e dispositivos.

Para obter instruções completas, consulte [Logon de administrador](../getting-started/admin-signin.md).

>[!NOTE]
>
>Lojas que foram habilitadas [!DNL Adobe Identity Management Services] (IMS) têm o Adobe Commerce nativo e o Magento Open Source 2FA desabilitado. Os usuários administradores que estão conectados à instância do Commerce com suas credenciais de Adobe não precisam se autenticar novamente para muitas tarefas de administrador. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [[!DNL Adobe Identity Management Service] Visão geral da integração do (IMS)](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Etapa 1: configurar [!DNL Google Authenticator]

1. Digite as credenciais da conta e faça logon na _Admin_. Uma nova tela do autenticador é exibida com um código QR.

1. Abra o **[!UICONTROL Google Authenticator]** no dispositivo móvel.

1. Clique no sinal de mais ( **+** ) para adicionar uma entrada e alinhar a caixa vermelha com o código QR para digitalizar com a câmera em seu smartphone.

1. Quando o seu telefone reconhece o código QR e adiciona uma entrada, insira esse código de 6 dígitos no _Admin_ **[!UICONTROL Authenticator code]** campo.

1. Quando terminar, clique em **[!UICONTROL Confirm]**.

   ![Código QR do Google Authenticator](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Etapa 2: Fazer logon com [!DNL Google Authenticator]

1. Digite as credenciais da conta e faça logon no Commerce _Admin_.

   ![Autenticador do Google - Conectando](./assets/storefront-2fa-google-code.png){width="300"}

1. Abertura [!DNL Google Authenticator] no dispositivo móvel.

1. Quando solicitado, insira o código de autenticação de seis dígitos.

1. Para salvar a autenticação para logons futuros, selecione a **[!UICONTROL Trust this device, do not ask again]** caixa de seleção

1. Quando terminar, clique em **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] O oferece uma avaliação gratuita e cobra de acordo com o número de usuários associados à conta. Siga as suas [instruções para configurar sua conta e baixar o aplicativo](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Etapa 1: configurar [!DNL Duo Security]

1. Digite as credenciais da conta e faça logon na _Admin_.

1. Quando a variável [!DNL Duo] Configuração for exibida, clique em **[!UICONTROL Start setup]** e faça o seguinte:

   ![Exemplo de vitrine - Configuração do Duo](./assets/storefront-2fa-duo-user1.png){width="300"}

1. Selecione seu dispositivo.

1. Quando solicitado, insira seu número de telefone e clique em **[!UICONTROL Continue]**.

   Este exemplo solicita seu número de telefone, pois estamos usando um dispositivo móvel.

1. Quando solicitado a instalar [!DNL Duo Mobile] para o tipo de telefone, clique em **[!UICONTROL I have Duo Mobile]**.

1. Abertura [!DNL Duo Mobile] e digitalize o código QR para sincronizar o autenticador com o Adobe Commerce. Uma marca de seleção é exibida quando a ativação é concluída.

1. Para definir as configurações do dispositivo, escolha a ação que deseja realizar ao entrar.

   - `Ask me to choose an authenticator method` — Permite que o usuário selecione ao efetuar login e autenticar na _Admin_.
   - `Automatically send this device a Duo Push` — Envia uma mensagem para seu dispositivo para aceitar ou negar acesso.
   - `Automatically call this device` — Chama e fornece uma senha para entrar para acesso.

   ![Ações de verificação Duo](./assets/storefront-2fa-duo-user7.png){width="300"}

### Etapa 2: Fazer logon com [!DNL Duo Security]

O exemplo a seguir mostra as opções para `Ask me to choose an authenticator method`:

1. Quando solicitado, insira o _Admin_ credenciais para entrar.

   ![Duo - entrada](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Escolha o método que deseja usar para autenticar:

   - `Send Me a Push` — Clique para receber um aviso por push para [!DNL Duo Mobile]. Aceitar para autenticar.
   - `Call Me` — Clique nessa opção, receba uma chamada com um código e insira a senha.
   - `Enter a Passcode` — Clique nesta opção para receber e inserir uma senha.

1. Conclua o push ou o código para fazer logon completo na _Admin_.

## [!DNL Authy]

[!DNL Authy] O oferece seu aplicativo e serviço sem custo para os usuários. Siga as instruções para baixar e configurar o aplicativo para seu dispositivo ou navegador. Para saber mais, consulte a [[!DNL Authy] documentação](https://authy.com/features/setup/).

### Etapa 1: configurar o Authy

1. Digite as credenciais da conta e faça logon na _Admin_.

   ![[!DNL Authy] registro](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Quando solicitado a se registrar no Authy, faça o seguinte:

   - Selecione seu país.

   - Insira seu número de telefone.

   - Selecione o **[!UICONTROL Verification method]**: `SMS` ou `Call Me`

   Clique em **[!UICONTROL Continue]**. Uma mensagem é enviada ao seu telefone por SMS ou uma chamada.

1. Insira o código de verificação recebido e clique em **[!UICONTROL Verify]**.

1. Quando terminar, clique em **[!UICONTROL Confirm]**.

   ![[!DNL Authy] código de verificação](./assets/storefront-2fa-authy-verify.png){width="300"}

### Etapa 2: Fazer logon com [!DNL Authy]

1. Digite as credenciais da conta e faça logon na _Admin_.

   ![[!DNL Authy] - fazendo logon](./assets/storefront-2fa-authy-access.png){width="300"}

1. Escolha um dos seguintes métodos para autenticar:

   - `Use one touch` — Envia um alerta para o [!DNL Authy] aplicativo. No aplicativo, aceite o acesso.
   - `Use authy token` — Solicitações para inserir um código de seu [!DNL Authy] aplicativo.

1. Se tiver problemas para fazer logon, escolha o método que deseja usar para receber o código. Em seguida, insira o código que você recebe para acessar o _Admin_.

   O aplicativo inclui esses métodos de emergência adicionais.

   - `Send me a code via SMS` — Uma mensagem SMS de texto é enviada para o dispositivo móvel configurado.
   - `Send me a code via phone call` — O usuário recebe um telefonema com um código.

   Sua conta foi verificada e aberta.

## U2F ([!DNL Yubikey] e outros dispositivos)

Siga as instruções do provedor de soluções para configurar seu dispositivo U2F. Para obter mais informações, consulte a documentação do fornecedor, como [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) por [!UICONTROL Yubico].

1. Digite as credenciais da conta e faça logon na _Admin_.

   ![Acesso à chave U2F](./assets/storefront-2fa-u2f.png){width="300"}

1. Pressione o botão na tecla.

   A autenticação aciona e abre imediatamente o _Admin_.

1. Insira o **[!UICONTROL U2F key]** em uma porta USB no computador.
