---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: Revise as configurações na página [!UICONTROL Catalog] > [!UICONTROL Email to a Friend] do Administrador do Commerce.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
TQID: https://experienceleague.adobe.com/TzkDDALdwE5MMIEuZBpBL4DnOgngN93-YEf4biNwYMI
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
source-wordcount: 172
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![Modelos de email](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Exibição da loja | Ativa o processo que oferece aos clientes a capacidade de enviar emails para amigos sobre produtos em sua loja. Opções: `Yes` / `No` |
| [!UICONTROL Select Email Template] | Exibição da loja | Identifica o modelo de email usado para mensagens geradas pela função _Enviar um Amigo por Email_. Modelo padrão: `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | Exibição da loja | Determina se o remetente deve ser um cliente registrado para enviar emails sobre um produto para amigos. Opções: `Yes` / `No` |
| [!UICONTROL Max Recipients] | Exibição da loja | Limita o número de pessoas que podem estar na lista de distribuição para um único email. |
| [!UICONTROL Max Products Sent in 1  Hour] | Exibição da loja | Limita o número de produtos que podem ser compartilhados por um único usuário no período de uma hora. |
| [!UICONTROL Limit Sending By] | Exibição da loja | Determina o método usado para identificar o remetente. As opções incluem: <br/>**`IP Address`**- (Recomendado) Identifica o remetente pelo endereço IP do computador usado para enviar os emails do produto.<br/>**`Cookie (unsafe)`** - Identifica o remetente por um cookie do navegador. Este método não é seguro porque o usuário pode excluir o cookie para evitar a restrição. |

{style="table-layout:auto"}
