---
title: '[!UICONTROL Services] > [!UICONTROL OAuth]'
description: Revise as configurações na página [!UICONTROL Services] > [!UICONTROL OAuth] do Administrador do Commerce.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/gwRxAaSnEul4D-LjjoGIcEiUCLl8ZrKjcSaMTvlGUKY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![Expiração do token de acesso](./assets/oauth-token-expire.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Global | Determina o tempo em horas antes que um token de API do cliente expire. O token do cliente nunca expira se o campo estiver vazio. Valor padrão: `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Global | Determina o tempo em horas antes que um token de API de administrador expire. O token do administrador nunca expira se o campo estiver vazio. Valor padrão: `4` |

{style="table-layout:auto"}

>[!NOTE]
>
>Os algoritmos de Duração do token da API de cliente e administrador do portador e de criptografia são controlados pelas configurações de [Autenticação JWT](magento-web-api.md#jwt-authentication).

## [!UICONTROL Cleanup Settings]

![Configurações de Limpeza](./assets/oauth-cleanup.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Global | Especifica o número de solicitações OAuth antes que a limpeza seja iniciada. Não insira `0` para desabilitar a limpeza. |
| [!UICONTROL Enable WSDL Cache] | Global | Determina a idade das entradas em minutos, antes de serem limpas. |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![Configurações do consumidor](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Global | Especifica o número de segundos que leva para o sistema expirar quando os clientes postam suas credenciais. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Global | Especifica o número máximo de redirecionamentos relacionados a um lançamento de credenciais do consumidor. |
| [!UICONTROL Expiration Period] | Global | Determina o número de segundos antes de uma chave/segredo não utilizado expirar após o início da troca de tokens OAuth. |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![Bloqueios de Autenticação](./assets/oauth-locks.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Global | Especifica o Número Máximo de falhas de autenticação para bloquear a conta. |
| [!UICONTROL Lockout Time (seconds)] | Global | Especifica o período em segundos após o qual a conta é desbloqueada. |

{style="table-layout:auto"}
