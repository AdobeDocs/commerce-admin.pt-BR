---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Revise as configurações no [!UICONTROL Security] &gt; [!UICONTROL 2FA] página do Administrador do Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>As lojas que têm a autenticação IMS (Adobe Identity Management Services) habilitada têm o Adobe Commerce nativo e o 2FA (autenticação de dois fatores de Magento Open Source) desabilitado. Os usuários administradores que estão conectados à instância do Adobe Commerce com suas credenciais de Adobe não precisam se autenticar novamente para muitas tarefas de administrador. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [Visão geral da integração do Adobe Commerce com o Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Para obter mais informações sobre como alterar essas configurações, consulte [Autenticação de dois fatores (2FA)](../../systems/security-two-factor-authentication.md) no _Guia de sistemas do administrador_.

## [!UICONTROL General]

![Geral](./assets/2fa-general.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Indica os métodos de autenticação de dois fatores necessários. Se você selecionar mais de um provedor, cada usuário deverá configurar cada método 2FA na próxima vez que fizer logon. |
| [!UICONTROL Configuration Email URL for Web API] | Global | Para implementações personalizadas, o URL de um link alternativo de configuração de email que é enviado para o _Admin_ usuários no primeiro logon. No modelo de email, use o espaço reservado `:tfat` para indicar onde o token foi injetado. |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | O tempo de vida em segundos de cada OTP (one-time password - senha ocasional) gerada pelo Google Authenticator. Padrão: `30` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Segurança Duo](./assets/2fa-duo-security.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Global | A chave de integração do seu [!DNL Duo Security] conta. |
| [!UICONTROL Secret Key] | Global | A chave secreta de seu [!DNL Duo Security] conta. |
| [!UICONTROL API Hostname] | Global | O nome do host da API do seu [!DNL Duo Security] conta. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | A chave de API do seu [!DNL Authy] conta. |
| [!UICONTROL OneTouch Message] | Global | A mensagem que aparece na variável [!DNL Authy] autenticador no logon. Padrão: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![Chave U2F](./assets/2fa-u2f-key.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | O domínio usado para emitir e processar [!DNL WebAuthn] desafios para implementações personalizadas de WebAPI. |

{style="table-layout:auto"}
