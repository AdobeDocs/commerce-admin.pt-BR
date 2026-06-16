---
title: '[!UICONTROL Services] > [!UICONTROL Magento Web API]'
description: Revise as configurações na página [!UICONTROL Services] > [!UICONTROL Magento Web API] do Administrador do Commerce.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
TQID: https://experienceleague.adobe.com/62cy3cPVxGeI-W1LElSg1TEBEb0cZN30vGZQ74UNhm8
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
source-wordcount: 325
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![Configurações do SOAP](./assets/web-api-soap-settings.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | Exibição da loja | Determina o conjunto de caracteres padrão. Se estiver vazio, UTF-8 será usado. |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![Limites de Entrada GraphQl](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Exibição da loja | Determina se os limites de entrada estão habilitados para chamadas GraphQL. Valor Padrão: `No`. |
| [!UICONTROL Maximum Page Size] | Exibição da loja | Define o número máximo de itens permitidos em um resultado de pesquisa paginado na resposta do GraphQL. Esta opção não está disponível quando _Habilitar Limites de Entrada_ = `No`. |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Limites De Entrada Da Api Da Web](./assets/web-api-input-limits.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Exibição da loja | Determina se os limites de entrada estão habilitados para chamadas de API da Web. Valor Padrão: `No`. |
| Limite da lista de entrada | Exibição da loja | Define o número máximo de itens permitidos em uma propriedade de matriz de entidade na solicitação da API da Web. Esta opção não está disponível quando _Habilitar Limites de Entrada_ = `No`. |
| [!UICONTROL Maximum Page Size] | Exibição da loja | Define o número máximo de itens permitidos em um resultado de pesquisa paginado na resposta da API da Web. Esta opção não está disponível quando _Habilitar Limites de Entrada_ = `No`. |
| [!UICONTROL Default Page Size] | Exibição da loja | Define o número padrão de itens em um resultado de pesquisa paginado na resposta da API da Web. |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Segurança da API Web](./assets/web-api-security.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | Global | Determina se os convidados podem acessar anonimamente os recursos do CMS, do catálogo e da loja das APIs do SOAP e do REST. Por padrão, o acesso de convidado anônimo não é permitido. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![Autenticação JWT](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | Global | Especifica o tipo de algoritmo JWS ou JWE usado para a criptografia JWT (JSON Web Token) |
| [!UICONTROL Content encryption algorithm for JWEs] | Global | Especifica o tipo de algoritmo de criptografia de conteúdo usado para criptografia JWT quando o algoritmo JWE é selecionado. Essa opção é ignorada para algoritmos JWS. |
| [!UICONTROL Customer JWT Expires In] | Global | Define o tempo (em minutos) antes que um token de portador JWT do cliente expire. O token de portador JWT do cliente expira em 30 minutos se esse campo estiver vazio ou tiver um valor negativo. Valor padrão: `60` |
| [!UICONTROL Admin User JWT Expires In] | Global | Define o período de tempo (em minutos) antes que o token de portador do JWT Admin expire. O token de portador do JWT do administrador expira em 30 minutos se esse campo estiver vazio ou tiver um valor negativo. Valor padrão: `60` |

{style="table-layout:auto"}
