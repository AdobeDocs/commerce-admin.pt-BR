---
title: Autenticação de dois fatores (2FA)
description: Saiba mais sobre autenticação de dois fatores suporte para garantir a segurança do seu sistema e de dados.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 4997c4c01f11d6e0355eb8e02f8f099db685b400
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---

# Autenticação de dois fatores (2FA)

O administrador Comércio __ da sua Adobe Systems Comércio ou Magento Open Source instalação fornece acesso aos seus dados de armazenamento, pedidos e clientes. Para evitar o acesso não autorizado aos seus dados, todos os usuários que tentarem fazer logon no _Administrador_ devem concluir um processo de autenticação para verificar sua identidade.

>[!NOTE]
>
>Essa implementação de autenticação de dois fatores (2FA) se aplica somente ao _Administrador_ e não está disponível para contas do cliente. A autenticação de dois fatores que protege sua Comércio conta possui uma configuração separada. Para saber mais, acesse [Secure your Comércio conta](../getting-started/commerce-account-secure.md).

A autenticação de dois fatores é amplamente usada e é comum gerar códigos de acesso para diferentes sites no mesmo aplicativo. Essa autenticação adicional garante que somente você possa fazer logon na usuário conta. Se você perder sua senha ou uma bot o adivinha, autenticação de dois fatores adiciona uma camada de proteção. Por exemplo, você pode usar o Google Authenticator para gerar códigos para o administrador da sua loja, sua conta da Commerce e a conta da Google.

![Iphone de configuração de segurança - 2FA](./assets/google-authenticator-iphone.png){width="300"}

A Adobe Commerce oferece suporte a métodos 2FA de vários provedores. Alguns exigem a instalação de um aplicativo que gera uma OTP (senha única) que os usuários inserem na entrada para verificar sua identidade. Dispositivos de segundo fator universal (U2F) se parecem com um fob de chave e geram uma chave exclusiva para verificar a identidade. Outros dispositivos verificam a identidade quando são inseridos em uma porta USB. Como administrador de armazenamento, você pode exigir um ou mais dos métodos 2FA disponíveis para verificar a identidade do usuário. Sua configuração 2FA se aplica a todos os sites e lojas associados à instalação do Adobe Commerce.

Na primeira vez em que um usuário faz logon _no Admin_, eles devem configurar cada [método 2FA](../configuration-reference/security/2fa.md) necessário e verificar sua identidade usando o aplicativo ou o dispositivo associado. Após essa configuração inicial, os usuário devem ser autenticados com um dos métodos configurados cada vez que eles se conectarem. As informações do 2FA de cada usuário são registradas na _conta de administração_ e podem ser [redefinidas](security-two-factor-authentication-manage.md) se necessário. Para saber mais sobre o processo de logon, acesse [_Admin_ Sign In](../getting-started/admin-signin.md).

>[!NOTE]
>
>As lojas que habilitaram a autenticação Adobe Systems Identity Management Services (IMS) têm nativo Adobe Systems Comércio e Magento Open Source 2FA desabilitadas. Os usuários administradores que fazem logon em suas Comércio instância com suas credenciais Adobe Systems não precisam reauttenticar para muitas tarefas de administrador. Authentication é tratado por Adobe Systems IMS quando o administrador usuário faz logon em sua sessão atual. Consulte [Adobe Systems visão geral da integração do Identity Management serviço de Identity Management (IMS).](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html)

É possível assistir a essa [demonstração](https://video.tv.adobe.com/v/339104?quality=12&learn=on) de vídeo para ter uma visão geral de autenticação de dois fatores na Administração.

## Configure seus provedores 2FA necessários

1. Na barra lateral do __ Administrador, vá até **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Security]** e escolha **[!UICONTROL 2FA]**.

1. _[!UICONTROL General]_&#x200B;Na seção, selecione os provedores a serem usados.

   | Provedor | Função |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Gera uma senha única no aplicativo para usuário autenticação. |
   | [!UICONTROL Duo Security] | Fornece SMS e notificação de push. |
   | [!UICONTROL Authy] | Gera um código de seis dígitos dependente de tempo e fornece proteção ou token SMS ou chamada de voz 2FA. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Usa uma dispositivo física para autenticar, como [[!DNL YubiKey]](https://www.yubico.com/). |

   Para selecionar vários métodos, mantenha a tecla Ctrl (PC) ou a tecla Comando (Mac) e clique em cada item.

1. Conclua as [configurações](../configuration-reference/security/2fa.md) para cada método 2FA necessário.

   ![Configuração de segurança - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

   Na primeira vez que os usuários entrarem no _Admin_, eles deverão configurar cada método 2FA necessário. Após essa configuração inicial, eles devem se autenticar com um dos métodos configurados sempre que entrarem.

## Configurações do provedor 2FA

Todos os Apps as configurações para cada método 2FA necessário.

### Google

Para alterar por quanto tempo a senha única (OTP) está disponível durante o logon, limpe a **[!UICONTROL Use system value]** caixa de seleção. Em seguida, insira o número de segundos que deseja **[!UICONTROL OTP Window]** que seja válido.

![Configuração de segurança - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>No Adobe Commerce 2.4.7 e versões posteriores, a configuração da janela OTP controla por quanto tempo (em segundos) o sistema aceita a senha ocasional (OTP) de um administrador após sua expiração. Esse valor deve ser menor que 30 segundos. A configuração padrão do sistema é `29`.<br><br> Na versão 2.4.6, a configuração de janela OTP determina o número de códigos OTP passados e futuros que permanecem válidos. Um valor `1` indica que o código OTP atual mais um código no passado e um código no futuro permanecem válidos em qualquer ponto no tempo.

### [!DNL Duo Security]

Insira as seguintes credenciais da sua conta de segurança do Duo:

- ID do cliente
- Senha do cliente
- Chave de integração
- Chave secreta
- Nome de host da API

![Configuração de segurança - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Insira a chave de API da sua conta [!DNL Authy].

1. Para alterar a mensagem padrão que aparece durante a autenticação, desmarque a caixa de seleção **[!UICONTROL Use system value]**. Em seguida, insira a **[!UICONTROL OneTouch Message]** página que deseja exibir.

   ![Configuração de segurança - Autenticação](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### Dispositivos U2F ([!DNL Yubikey] e outros)

O domínio armazenamento é usado por padrão durante o processo de autenticação. Para usar um domínio personalizado para desafios de autenticação, limpe a **[!UICONTROL Use system value]** caixa de seleção. Em seguida, insira o **[!UICONTROL WebAPi Challenge Domain]** caractere .

![Configuração de segurança - Dispositivos U2F](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
