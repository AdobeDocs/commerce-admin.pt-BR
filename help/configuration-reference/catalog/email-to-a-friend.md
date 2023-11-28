---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend]'
description: Revise as configurações no [!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend] página do Administrador do Commerce.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![Modelos de e-mail](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://docs.magento.com/user-guide/marketing/email-template-configuration.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Exibição da loja | Ativa o processo que oferece aos clientes a capacidade de enviar emails para amigos sobre produtos em sua loja. Opções: `Yes` / `No` |
| [!UICONTROL Select Email Template] | Exibição da loja | Identifica o modelo de email usado para mensagens geradas pelo _Enviar para um amigo_ função. Modelo padrão: `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | Exibição da loja | Determina se o remetente deve ser um cliente registrado para enviar emails sobre um produto para amigos. Opções: `Yes` / `No` |
| [!UICONTROL Max Recipients] | Exibição da loja | Limita o número de pessoas que podem estar na lista de distribuição para um único email. |
| [!UICONTROL Max Products Sent in 1  Hour] | Exibição da loja | Limita o número de produtos que podem ser compartilhados por um único usuário no período de uma hora. |
| [!UICONTROL Limit Sending By] | Exibição da loja | Determina o método usado para identificar o remetente. As opções incluem: <br/>**`IP Address`**- (Recomendado) Identifica o remetente pelo endereço IP do computador usado para enviar os emails sobre o produto.<br/>**`Cookie (unsafe)`** - Identifica o remetente por um cookie do navegador. Este método não é seguro porque o usuário pode excluir o cookie para evitar a restrição. |

{:style=&quot;table-layout:auto&quot;}
