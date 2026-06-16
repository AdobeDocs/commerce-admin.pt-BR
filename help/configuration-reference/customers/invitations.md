---
title: '[!UICONTROL Customers] > [!UICONTROL Invitations]'
description: Revise as configurações na página [!UICONTROL Customers] > [!UICONTROL Invitations] do Administrador do Commerce.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
TQID: https://experienceleague.adobe.com/UOJF8r7CsXWK6qG7FjkJoJTIqnH2fPQhnRyZrJ7u4nE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 250
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![Geral](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | Global | Determina se o módulo Convites está habilitado. Opções: `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | Site | Determina se os convites podem ser gerenciados na loja. Opções: `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | Exibição da loja | Determina o grupo de clientes do convite. Opções: <br/>**`Same as Inviter`**- Os convidados são atribuídos automaticamente ao mesmo grupo de clientes que os clientes que os convidaram.<br/>**`Default Customer Group from Configuration`** - Os convidados têm automaticamente o [grupo de clientes](../../customers/customer-groups.md) padrão. |
| [!UICONTROL New Accounts Registration] | Exibição da loja | Determina como os convidados podem criar uma conta. Opções: <br/>**`By Invitation Only`**- Os convidados devem seguir o link no email de convite para criar uma conta.<br/>**`Available to All`** - Os convidados podem usar o formulário de registro de conta disponível no armazenamento. |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | Exibição da loja | Determina se há um campo no formulário Convite no qual o emissor do convite pode adicionar uma mensagem personalizada enviada ao convidado por email. Isso não afeta a capacidade do administrador de adicionar uma mensagem a um Convite. Opções: `Yes` / `No`. |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | Exibição da loja | Determina o número máximo de convites que o emissor do convite pode enviar simultaneamente. Um convite diferente é enviado para cada endereço de email que o emissor do convite inclui no formulário. Isso protege os recursos do servidor, impedindo que um grande número de convites seja enviado de uma só vez, e torna menos provável que os convites sejam enviados como spam. |

{style="table-layout:auto"}

## [!UICONTROL Email]

![Email](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | Exibição da loja | Determina o remetente do email que os convidados recebem quando um email de convite é enviado. Valor padrão: `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | Exibição da loja | Determina o modelo do email que os convidados recebem quando um email de convite é enviado. Modelo padrão: `Customer Invitation` |

{style="table-layout:auto"}
