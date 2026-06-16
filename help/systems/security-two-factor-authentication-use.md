---
title: Configuração da autenticação de dois fatores para contas de usuário
description: Saiba como configurar a autenticação de dois fatores durante o logon inicial do Administrador e autenticar sua identidade usando um aplicativo de dispositivo compatível.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/hLZcsjOdn1Pwx70nFCUIKe5RShnzyHaEciVyxmVpGK0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 806
ht-degree: 0%

---

# Configuração da autenticação de dois fatores para contas de usuário

Estas instruções mostram como configurar a autenticação de dois fatores durante o logon inicial na Adobe Commerce ou no Magento Open Source e como autenticar sua identidade usando os seguintes aplicativos e dispositivos.

Para obter instruções completas, consulte [Logon de administrador](../getting-started/admin-signin.md).

>[!NOTE]
>
>Os armazenamentos que habilitaram a autenticação [!DNL Adobe Identity Management Services] (IMS) têm o Adobe Commerce nativo e o Magento Open Source 2FA desabilitados. Os usuários administradores que estão conectados à instância do Commerce com suas credenciais do Adobe não precisam se autenticar novamente para muitas tarefas administrativas. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [[!DNL Adobe Identity Management Service] (IMS) Visão geral da integração](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Etapa 1: configurar [!DNL Google Authenticator]

1. Insira suas credenciais de conta e entre no _Administrador_. Uma nova tela do autenticador é exibida com um código QR.

1. Abra o aplicativo **[!UICONTROL Google Authenticator]** no dispositivo móvel.

1. Clique no sinal de mais ( **+** ) para adicionar uma entrada e alinhar a caixa vermelha com o código QR para digitalizar com a câmera no seu smartphone.

1. Quando o telefone reconhece o código QR e adiciona uma entrada, insira esse código de 6 dígitos no campo _Admin_ **[!UICONTROL Authenticator code]**.

1. Quando terminar, clique em **[!UICONTROL Confirm]**.

   ![Código QR do Google Authenticator](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Etapa 2: entrar com [!DNL Google Authenticator]

1. Insira suas credenciais de conta e entre no _Administrador_ da Commerce.

   ![Autenticador do Google - entrando](./assets/storefront-2fa-google-code.png){width="300"}

1. Abra o [!DNL Google Authenticator] em seu dispositivo móvel.

1. Quando solicitado, insira o código de autenticação de seis dígitos.

1. Para salvar a autenticação para logons futuros, marque a caixa de seleção **[!UICONTROL Trust this device, do not ask again]**.

1. Quando terminar, clique em **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

O [!DNL Duo] oferece uma avaliação gratuita e cobra de acordo com o número de usuários associados à conta. Siga as [instruções para configurar sua conta e baixar o aplicativo](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Etapa 1: configurar [!DNL Duo Security]

1. Insira suas credenciais de conta e entre no _Administrador_.

1. Quando a página Instalação do [!DNL Duo] for exibida, clique em **[!UICONTROL Get Started]** e faça o seguinte:

   ![Exemplo de vitrine - Configuração do Duo](./assets/storefront-2fa-duo-setup-options.png){width="300"}

1. Selecione sua opção. Você pode escolher Touch ID, Duo Mobile, Security Key ou Phone Number. Este exemplo mostra a opção Duo Mobile or Phone Number.

1. Quando solicitado, digite seu número de telefone e clique em **[!UICONTROL Continue]**.

   Confirme a propriedade enviando e verificando a senha no número de telefone.

1. Quando for solicitado instalar o [!DNL Duo Mobile] para o seu tipo de telefone, clique em **[!UICONTROL I have Duo Mobile]**.

1. Abra [!DNL Duo Mobile] e verifique o código QR para sincronizar o autenticador com o Adobe Commerce. Uma marca de seleção é exibida quando a ativação é concluída.

1. Você pode adicionar mais dispositivos (se necessário) ou ignorar. A configuração foi concluída e você pode fazer logon com o Duo.

   ![Ações de verificação de duplicidade](./assets/storefront-2fa-duo-setup-complete.png){width="300"}

### Etapa 2: entrar com [!DNL Duo Security]

O exemplo a seguir mostra as opções para `Ask me to choose an authenticator method`:

1. Quando solicitado, insira suas credenciais de _Administrador_ para entrar.

   ![Duo - Entrando](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Escolha &quot;Fazer logon com Duo&quot; para receber uma notificação por push no aplicativo Duo para dispositivos móveis, &quot;Fazer logon com Touch ID&quot; ou &quot;Prosseguir com outra opção configurada durante a configuração&quot;.

1. Aprove a solicitação do aplicativo Duo/Touch ID/Mensagem de texto e você será conectado com sucesso.

   ![Duo - Entrando](./assets/storefront-2fa-duo-success.png){width="300"}

## [!DNL Authy]

O [!DNL Authy] oferece seu aplicativo e serviço sem custo para os usuários. Siga as instruções para baixar e configurar o aplicativo para seu dispositivo ou navegador. Para saber mais, consulte a [[!DNL Authy] documentação](https://authy.com/features/setup/).

### Etapa 1: configurar o Authy

1. Insira suas credenciais de conta e entre no _Administrador_.

   ![[!DNL Authy] inscrição](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Quando solicitado a se registrar no Authy, faça o seguinte:

   - Selecione seu país.

   - Insira seu número de telefone.

   - Selecione o **[!UICONTROL Verification method]**: `SMS` ou `Call Me`

   Clique em **[!UICONTROL Continue]**. Uma mensagem é enviada ao seu telefone por SMS ou uma chamada.

1. Insira o código de verificação recebido e clique em **[!UICONTROL Verify]**.

1. Quando terminar, clique em **[!UICONTROL Confirm]**.

   ![[!DNL Authy] código de verificação](./assets/storefront-2fa-authy-verify.png){width="300"}

### Etapa 2: entrar com [!DNL Authy]

1. Insira suas credenciais de conta e entre no _Administrador_.

   ![[!DNL Authy] - entrada](./assets/storefront-2fa-authy-access.png){width="300"}

1. Escolha um dos seguintes métodos para autenticar:

   - `Use one touch` — Envia um alerta para o aplicativo [!DNL Authy]. No aplicativo, aceite o acesso.
   - `Use authy token` — Solicita que você insira um código do aplicativo [!DNL Authy].

1. Se tiver problemas para fazer logon, escolha o método que deseja usar para receber o código. Em seguida, insira o código recebido para acessar o _Admin_.

   O aplicativo inclui esses métodos de emergência adicionais.

   - `Send me a code via SMS` — Uma mensagem SMS de texto é enviada para o dispositivo móvel configurado.
   - `Send me a code via phone call` — O usuário recebe uma chamada telefônica com um código.

   Sua conta foi verificada e aberta.

## U2F ([!DNL Yubikey] e outros dispositivos)

Siga as instruções do provedor de soluções para configurar seu dispositivo U2F. Para obter mais informações, consulte a documentação do fornecedor, como [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) por [!UICONTROL Yubico].

1. Insira suas credenciais de conta e entre no _Administrador_.

   ![Acesso à chave U2F](./assets/storefront-2fa-u2f.png){width="300"}

1. Pressione o botão na tecla.

   A autenticação dispara imediatamente e abre o _Administrador_.

1. Insira o **[!UICONTROL U2F key]** em uma porta USB no computador.
