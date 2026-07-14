---
title: '[!UICONTROL Security] > [!UICONTROL 2FA]'
description: Revise as configurações na página [!UICONTROL Security] > [!UICONTROL 2FA] do Administrador do Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/-5t8bTj14iB%2D%2D%2D88TotUNefATWwE80LTswPO3xVWU70
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 97a3e3469e45ec9c7e3316f1ce5ca7894ea2ddb7
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 2%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>As lojas que ativaram a autenticação do Adobe Identity Management Services (IMS) têm a Adobe Commerce nativa e a autenticação de dois fatores (2FA) da Magento Open Source desativadas. Os usuários administradores que estão conectados à instância do Adobe Commerce com suas credenciais do Adobe não precisam se autenticar novamente para muitas tarefas administrativas. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [Visão geral da integração do Adobe Commerce com o Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Para obter mais informações sobre como alterar essas configurações, consulte [Autenticação de dois fatores (2FA)](../../systems/security-two-factor-authentication.md) no _Guia de Sistemas de Administração_.

## [!UICONTROL General]

![Geral](./assets/2fa-general.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Indica os métodos de autenticação de dois fatores necessários. Se você selecionar mais de um provedor, cada usuário deverá configurar cada método 2FA na próxima vez que fizer logon. |
| [!UICONTROL Configuration Email URL for Web API] | Global | Para implementações personalizadas, a URL para um link alternativo de configuração de email que é enviado aos usuários _Administrador_ no primeiro logon. No modelo de email, use o espaço reservado `:tfat` para indicar onde o token é inserido. |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | Global | Determina quantas vezes um administrador pode inserir um [!DNL one-time password (OTP)] antes que sua conta seja temporariamente desabilitada. Padrão: `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | Global | Determina quanto tempo (em segundos) um administrador pode esperar para inserir um [!DNL one-time password (OTP)] antes que sua conta seja temporariamente desabilitada. Padrão: `300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Determina quanto tempo (em segundos) o sistema aceita o [!DNL one-time-password (OTP)] de um administrador após a expiração. Não pode ser maior do que o tempo de vida de um único OTP (geralmente 30 segundos). Padrão: `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Dupla de Segurança](./assets/2fa-duo-security.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Client Id] | Global | A ID do cliente da sua conta [!DNL Duo Security]. |
| [!UICONTROL Client Secret] | Global | O Segredo do Cliente da sua conta [!DNL Duo Security]. |
| [!UICONTROL Integration Key] | Global | A chave de integração da sua conta de API [!DNL Duo Security]. |
| [!UICONTROL Secret Key] | Global | A chave secreta da sua conta de API do [!DNL Duo Security]. |
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
