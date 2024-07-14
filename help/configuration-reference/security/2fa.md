---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Revise as configurações na página [!UICONTROL Security] &gt; [!UICONTROL 2FA] do Administrador do Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: d6f9c5186276b28cada318cbe765e2271d34bb58
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>As lojas que têm a autenticação IMS (Adobe Identity Management Services) habilitada têm o Adobe Commerce nativo e o 2FA (autenticação de dois fatores de Magento Open Source) desabilitado. Os usuários administradores que estão conectados à instância do Adobe Commerce com suas credenciais de Adobe não precisam se autenticar novamente para muitas tarefas de administrador. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [Visão geral da integração do Adobe Commerce com o Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Para obter mais informações sobre como alterar essas configurações, consulte [Autenticação de dois fatores (2FA)](../../systems/security-two-factor-authentication.md) no _Guia de Sistemas de Administração_.

## [!UICONTROL General]

![Geral](./assets/2fa-general.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Indica os métodos de autenticação de dois fatores necessários. Se você selecionar mais de um provedor, cada usuário deverá configurar cada método 2FA na próxima vez que fizer logon. |
| [!UICONTROL Configuration Email URL for Web API] | Global | Para implementações personalizadas, a URL para um link alternativo de configuração de email que é enviado aos usuários _Administrador_ no primeiro logon. No modelo de email, use o espaço reservado `:tfat` para indicar onde o token é inserido. |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Determina quanto tempo (em segundos) o sistema aceita a senha ocasional (OTP) de um administrador após a expiração. Não pode ser maior do que o tempo de vida de um único OTP (geralmente 30 segundos). Padrão: `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Dupla de Segurança](./assets/2fa-duo-security.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Global | A chave de integração da sua conta [!DNL Duo Security]. |
| [!UICONTROL Secret Key] | Global | A chave secreta da sua conta [!DNL Duo Security]. |
| [!UICONTROL API Hostname] | Global | O nome de host da API da sua conta [!DNL Duo Security]. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | A chave de API da sua conta [!DNL Authy]. |
| [!UICONTROL OneTouch Message] | Global | A mensagem que aparece no autenticador [!DNL Authy] no logon. Padrão: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![Chave U2F](./assets/2fa-u2f-key.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | O domínio usado para emitir e processar desafios do [!DNL WebAuthn] para implementações WebAPI personalizadas. |

{style="table-layout:auto"}
