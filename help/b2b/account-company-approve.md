---
title: Aprovar uma conta de empresa
description: Saiba como aprovar solicitações de conta da empresa no Administrador.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
TQID: https://experienceleague.adobe.com/ZpDdYMYaSnG1lOwV22mmrkYjBvf90pUJVZxP2r526pw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 0%

---

# Aprovar uma conta de empresa

O status das solicitações recebidas da loja para criar uma empresa é `Pending Approval` até que a solicitação seja revisada pelo administrador da loja e seja aprovada ou rejeitada. O status de uma conta de empresa pode ser definido como qualquer um dos seguintes:

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

Você também pode usar o [Controle de ações](account-company-manage.md) para aprovar várias solicitações de empresa.

![Aprovação pendente](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Aprovar uma conta de empresa pendente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   Você pode usar o seletor _[!UICONTROL Columns]_acima da grade para exibir a coluna **[!UICONTROL Status]**.

1. Na coluna _[!UICONTROL Action]_, clique em **[!UICONTROL Edit]**.

1. Defina **[!UICONTROL Company Status]** como `Active`.

   ![Definir o status da empresa](./assets/company-status-active.png){width="700" zoomable="yes"}

1. Quando for solicitada a confirmação, clique em **[!UICONTROL Change status]**.

   O administrador da empresa recebe uma notificação por email informando que a empresa está ativa no momento.

1. Se aplicável, defina **[!UICONTROL Sales Representative]** para uma conta de usuário Admin específica.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Account Information]** e use o campo **[!UICONTROL Comment]** para inserir observações sobre a conta.

   Os comentários não estão visíveis na loja.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   Um email de confirmação é enviado à empresa e ao administrador da empresa informando que a conta da empresa foi aprovada.

## Status da empresa

| Status | Descrição |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | A empresa é aprovada e pode ser gerenciada na loja pelo administrador da empresa. |
| [!UICONTROL Pending Approval] | Uma solicitação para criar uma conta de empresa foi enviada da loja, mas ainda não foi revisada. |
| [!UICONTROL Rejected] | A solicitação para criar uma conta de empresa foi rejeitada pelo administrador de armazenamento. |
| [!UICONTROL Blocked] | A conta da empresa não está mais em boa posição. O cliente pode acessar a conta na loja, mas não pode fazer compras. |

{style="table-layout:auto"}
