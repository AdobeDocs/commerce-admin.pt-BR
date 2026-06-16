---
title: Atribuir um administrador de empresa
description: Saiba como atribuir uma conta de usuário da empresa como o administrador da empresa designado para a conta da empresa.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
TQID: https://experienceleague.adobe.com/5h4DaxiUVTz9UFOC3BZqd5ESPRLaLgvstCODPEEgCEk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 274
ht-degree: 0%

---

# Atribuir um administrador de empresa

O administrador da empresa é atribuído inicialmente quando a conta da empresa é criada pela primeira vez e só pode ser modificado por um administrador de loja do Administrador.

- Cada empresa só pode ter um administrador atribuído.
- Um usuário de empresa pode ser o administrador de apenas uma empresa.
- As alterações no administrador de empresa atribuído devem ser concluídas por um administrador de loja do Administrador.

## Alterar administrador de empresa atribuído

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Empresas](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Localize a empresa na lista e clique em **[!UICONTROL Edit]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Company Admin]**.

   ![Administrador da Empresa](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Insira o **[!UICONTROL Job Title]** do novo administrador de empresa.

   Esta ação limpa o formulário e os campos obrigatórios _[!UICONTROL First Name]_&#x200B;e_[!UICONTROL Last Name]_ estão realçados.

1. Digite o endereço **[!UICONTROL Email]** do novo administrador de empresa.

   Se o sistema não encontrar o endereço de email no banco de dados, você será solicitado a confirmar se deseja substituir o administrador da empresa.

   - Se não existir uma conta de usuário para o novo administrador de empresa, o sistema criará uma conta do tipo `Company Admin`.

   - Se a conta de usuário existir no sistema, ela será movida para a posição de administrador da empresa na estrutura da empresa.

1. Insira as **[!UICONTROL First Name]** e **[!UICONTROL Last Name]**, bem como qualquer outra informação, conforme aplicável, para o novo administrador de empresa.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A conta individual do antigo administrador de empresa permanece no sistema como uma conta de usuário ativa, atribuída à função de usuário padrão. Se esta for a única empresa associada à conta de usuário, o tipo de conta mudará de *[!UICONTROL Company user]* para *[!UICONTROL Individual user]*.

   O sistema envia uma notificação por email sobre a alteração para os administradores de empresas novos e antigos.

