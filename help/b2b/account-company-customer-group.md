---
title: Atribuir um grupo de clientes a uma empresa
description: Saiba como atribuir um grupo de clientes a uma conta de empresa em sua loja da Adobe Commerce.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
TQID: https://experienceleague.adobe.com/O03eRkYyE78HIHjmwYRXqfOR2A7k1KFL11AspJGCi-U
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 236
ht-degree: 0%

---

# Atribuir um grupo de clientes a uma empresa

Atribuir um grupo de clientes a uma empresa é basicamente o mesmo que atribuir um catálogo compartilhado. Se o Catálogo Compartilhado não estiver [habilitado na configuração](enable-basic-features.md), um Grupo de Clientes — em vez de um Catálogo Compartilhado — será atribuído a uma empresa.

- Somente um grupo de clientes ou catálogo compartilhado pode ser atribuído a uma empresa de cada vez. Um grupo de clientes associado a um catálogo compartilhado não pode ser excluído.
- Alterar o grupo de clientes atribuído à empresa atualiza os perfis de todos os membros da empresa.
- Se a atribuição do grupo de clientes for alterada de um catálogo compartilhado para um grupo de clientes comum, os membros da empresa perderão o acesso ao catálogo compartilhado e o catálogo principal ficará disponível para eles na loja.
- Depois de alterar o grupo de empresas, um usuário da empresa deve fazer logoff e logon na Loja para ver os novos preços no catálogo.

## Alterar o grupo de clientes

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Localize a empresa na grade e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

   ![Editar Empresa](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Na página da empresa, role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) na seção **[!UICONTROL Advanced Settings]**.

1. Defina o **[!UICONTROL Customer Group]** apropriado.

   A lista [!UICONTROL Customer Group] inclui todos os catálogos compartilhados existentes, mesmo se os Catálogos Compartilhados estiverem desabilitados na configuração.

   ![Alterar grupo de clientes ou catálogo compartilhado](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. Quando for solicitada a confirmação, clique em **[!UICONTROL Proceed]**.

1. Clique em **[!UICONTROL Save]**.
