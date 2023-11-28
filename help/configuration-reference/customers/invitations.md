---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Invitations]'
description: Revise as configurações no [!UICONTROL Customers] &gt; [!UICONTROL Invitations] página do Administrador do Commerce.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![Geral](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | Global | Determina se o módulo Convites está habilitado. Opções: `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | Site | Determina se os convites podem ser gerenciados na loja. Opções: `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | Exibição da loja | Determina o grupo de clientes do convite. Opções: <br/>**`Same as Inviter`**- Os convidados são atribuídos automaticamente ao mesmo grupo de clientes que os clientes que os convidaram.<br/>**`Default Customer Group from Configuration`** - Convidados têm automaticamente o padrão [grupo de clientes](../../customers/customer-groups.md). |
| [!UICONTROL New Accounts Registration] | Exibição da loja | Determina como os convidados podem criar uma conta. Opções: <br/>**`By Invitation Only`**- Os convidados devem seguir o link no email de convite para criar uma conta.<br/>**`Available to All`** - Os convidados podem usar o formulário de registro de conta disponível na loja. |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | Exibição da loja | Determina se há um campo no formulário Convite no qual o emissor do convite pode adicionar uma mensagem personalizada enviada ao convidado por email. Isso não afeta a capacidade do administrador de adicionar uma mensagem a um Convite. Opções: `Yes` / `No`. |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | Exibição da loja | Determina o número máximo de convites que o emissor do convite pode enviar simultaneamente. Um convite diferente é enviado para cada endereço de email que o emissor do convite inclui no formulário. Isso protege os recursos do servidor, impedindo que um grande número de convites seja enviado de uma só vez, e torna menos provável que os convites sejam enviados como spam. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Email]

![Email](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | Exibição da loja | Determina o remetente do email que os convidados recebem quando um email de convite é enviado. Valor padrão: `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | Exibição da loja | Determina o modelo do email que os convidados recebem quando um email de convite é enviado. Modelo padrão: `Customer Invitation` |

{:style=&quot;table-layout:auto&quot;}
