---
title: '[!UICONTROL Services] &gt; [!UICONTROL Magento Web API]'
description: Revise as configurações no [!UICONTROL Services] &gt; [!UICONTROL Magento Web API] página do Administrador do Commerce.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![Configurações SOAP](./assets/web-api-soap-settings.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | Exibição da loja | Determina o conjunto de caracteres padrão. Se estiver vazio, UTF-8 será usado. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL GraphQl Input Limits]

![Limites de entrada GraphQl](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Exibição da loja | Determina se os limites de entrada estão habilitados para chamadas GraphQL. Valor padrão: `No`. |
| [!UICONTROL Maximum Page Size] | Exibição da loja | Define o número máximo de itens permitidos em um resultado de pesquisa paginado na resposta do GraphQL. Essa opção não está disponível quando _Ativar limites de entrada_ = `No`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Web Api Input Limits]

![Limites De Entrada Da Api Da Web](./assets/web-api-input-limits.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Exibição da loja | Determina se os limites de entrada estão habilitados para chamadas de API da Web. Valor padrão: `No`. |
| Limite da lista de entrada | Exibição da loja | Define o número máximo de itens permitidos em uma propriedade de matriz de entidade na solicitação da API da Web. Essa opção não está disponível quando _Ativar limites de entrada_ = `No`. |
| [!UICONTROL Maximum Page Size] | Exibição da loja | Define o número máximo de itens permitidos em um resultado de pesquisa paginado na resposta da API da Web. Essa opção não está disponível quando _Ativar limites de entrada_ = `No`. |
| [!UICONTROL Default Page Size] | Exibição da loja | Define o número padrão de itens em um resultado de pesquisa paginado na resposta da API da Web. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Web API Security]

![Segurança da API da Web](./assets/web-api-security.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | Global | Determina se os convidados podem acessar anonimamente os recursos de CMS, catálogo e armazenamento das APIs SOAP e REST. Por padrão, o acesso de convidado anônimo não é permitido. Opções: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL JWT Authentication]

![Autenticação JWT](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | Global | Especifica o tipo de algoritmo JWS ou JWE usado para a criptografia JWT (JSON Web Token) |
| [!UICONTROL Content encryption algorithm for JWEs] | Global | Especifica o tipo de algoritmo de criptografia de conteúdo usado para criptografia JWT quando o algoritmo JWE é selecionado. Essa opção é ignorada para algoritmos JWS. |
| [!UICONTROL Customer JWT Expires In] | Global | Define o tempo (em minutos) antes que um token de portador JWT do cliente expire. O token de portador JWT do cliente expira em 30 minutos se esse campo estiver vazio ou tiver um valor negativo. Valor padrão: `60` |
| [!UICONTROL Admin User JWT Expires In] | Global | Define o período de tempo (em minutos) antes que o token de portador do JWT Admin expire. O token de portador do JWT do administrador expira em 30 minutos se esse campo estiver vazio ou tiver um valor negativo. Valor padrão: `60` |

{:style=&quot;table-layout:auto&quot;}
