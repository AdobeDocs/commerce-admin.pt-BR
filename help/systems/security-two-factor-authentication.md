---
title: Autenticação de dois fatores (2FA)
description: Saiba mais sobre o suporte à autenticação de dois fatores para garantir a segurança do sistema e dos dados.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---

# Autenticação de dois fatores (2FA)

O _Administrador_ do Commerce para sua instalação do Adobe Commerce ou do Magento Open Source fornece acesso à loja, aos pedidos e aos dados do cliente. Para impedir o acesso não autorizado aos seus dados, todos os usuários que tentarem entrar no _Admin_ devem concluir um processo de autenticação para verificar sua identidade.

>[!NOTE]
>
>Esta implementação da autenticação de dois fatores (2FA) se aplica somente ao _Administrador_ e não está disponível para contas de clientes. A autenticação de dois fatores que protege a conta do Commerce tem uma configuração separada. Para saber mais, acesse [Proteger sua conta da Commerce](../getting-started/commerce-account-secure.md).

A autenticação de dois fatores é amplamente usada, e é comum gerar códigos de acesso para sites diferentes no mesmo aplicativo. Essa autenticação adicional garante que somente você possa fazer logon na sua conta de usuário. Se você perder sua senha ou um bot adivinhar, a autenticação de dois fatores adicionará uma camada de proteção. Por exemplo, você pode usar o Google Authenticator para gerar códigos para o administrador da sua loja, sua conta da Commerce e a conta da Google.

![Iphone de configuração de segurança - 2FA](./assets/google-authenticator-iphone.png){width="300"}

A Adobe Commerce oferece suporte a métodos 2FA de vários provedores. Alguns exigem a instalação de um aplicativo que gera uma OTP (senha única) que os usuários inserem na entrada para verificar sua identidade. Dispositivos de segundo fator universal (U2F) se parecem com um fob de chave e geram uma chave exclusiva para verificar a identidade. Outros dispositivos verificam a identidade quando são inseridos em uma porta USB. Como administrador de armazenamento, você pode exigir um ou mais dos métodos 2FA disponíveis para verificar a identidade do usuário. Sua configuração 2FA se aplica a todos os sites e lojas associados à instalação do Adobe Commerce.

Na primeira vez que um usuário entrar no _Admin_, ele deverá configurar cada método [2FA](../configuration-reference/security/2fa.md) necessário e verificar sua identidade usando o aplicativo ou dispositivo associado. Após essa configuração inicial, o usuário deverá se autenticar com um dos métodos configurados sempre que entrar. As informações de 2FA de cada usuário são registradas em sua conta de _Administrador_ e podem ser [redefinidas](security-two-factor-authentication-manage.md), se necessário. Para saber mais sobre o processo de entrada, vá para [_Entrada de Administrador_](../getting-started/admin-signin.md).

>[!NOTE]
>
>As lojas que habilitaram a autenticação do Adobe Identity Management Services (IMS) têm o Adobe Commerce nativo e o Magento Open Source 2FA desabilitado. Os usuários administradores que estão conectados à instância do Commerce com suas credenciais do Adobe não precisam se autenticar novamente para muitas tarefas administrativas. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [Visão Geral da Integração do Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html?lang=pt-BR).

Você pode assistir a esta [demonstração em vídeo](https://video.tv.adobe.com/v/339104?quality=12&learn=on) para obter uma visão geral da autenticação de dois fatores no Administrador.

## Configure os provedores 2FA necessários

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Security]** e escolha **[!UICONTROL 2FA]**.

1. Na seção _[!UICONTROL General]_, selecione os provedores a serem usados.

   | Provedor | Função |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Gera uma senha ocasional no aplicativo para autenticação do usuário. |
   | [!UICONTROL Duo Security] | Fornece SMS e notificação por push. |
   | [!UICONTROL Authy] | Gera um código de seis dígitos dependente do tempo e fornece proteção ou token de SMS ou Chamada de voz 2FA. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Usa um dispositivo físico para autenticação, como [[!DNL YubiKey]](https://www.yubico.com/). |

   Para selecionar vários métodos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada item.

1. Conclua as [configurações](../configuration-reference/security/2fa.md) para cada método 2FA necessário.

   ![Configuração de segurança - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

   Na primeira vez que os usuários entrarem no _Admin_, eles deverão configurar cada método 2FA necessário. Após essa configuração inicial, eles devem se autenticar com um dos métodos configurados sempre que entrarem.

## Configurações do provedor 2FA

Conclua as configurações para cada método 2FA necessário.

### Google

Para alterar por quanto tempo a OTP (senha ocasional) fica disponível durante a entrada, desmarque a caixa de seleção **[!UICONTROL Use system value]**. Em seguida, digite o número de segundos que você deseja que o **[!UICONTROL OTP Window]** seja válido.

![Configuração de segurança - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>No Adobe Commerce 2.4.7 e versões posteriores, a configuração da janela OTP controla por quanto tempo (em segundos) o sistema aceita a senha ocasional (OTP) de um administrador após sua expiração. Esse valor deve ser inferior a 30 segundos. A configuração padrão do sistema é `29`.<br><br> Na versão 2.4.6, a configuração da janela OTP determina o número de códigos OTP passados e futuros que permanecem válidos. Um valor de `1` indica que o código OTP atual mais um código no passado e um código no futuro permanecem válidos em qualquer momento determinado.

### [!DNL Duo Security]

Digite as seguintes credenciais da sua conta de Segurança Duo:

- ID do cliente
- Segredo do cliente
- Chave de integração
- Chave secreta
- Nome de host da API

![Configuração de segurança - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Insira a chave de API da sua conta [!DNL Authy].

1. Para alterar a mensagem padrão que aparece durante a autenticação, desmarque a caixa de seleção **[!UICONTROL Use system value]**. Em seguida, insira o **[!UICONTROL OneTouch Message]** que você deseja que apareça.

   ![Configuração de segurança - Authy](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### Dispositivos U2F ([!DNL Yubikey] e outros)

O domínio de armazenamento é usado por padrão durante o processo de autenticação. Para usar um domínio personalizado para desafios de autenticação, desmarque a caixa de seleção **[!UICONTROL Use system value]**. Em seguida, insira o **[!UICONTROL WebAPi Challenge Domain]**.

![Configuração de segurança - Dispositivos U2F](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
