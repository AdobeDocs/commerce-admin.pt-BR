---
title: Atribuir um administrador de empresa
description: Saiba como atribuir uma conta de usuário da empresa como o administrador da empresa designado para a conta da empresa.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Atribuir um administrador de empresa

O administrador da empresa é atribuído inicialmente quando a conta da empresa é criada pela primeira vez e só pode ser modificado por um administrador de loja do Administrador.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Localize a empresa na lista e clique em **[!UICONTROL Edit]**.

   ![Empresas](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Company Admin]** seção.

   ![Administrador da empresa](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Insira o **[!UICONTROL Job Title]** do novo administrador de empresa e clique em **[!UICONTROL Proceed]** para continuar.

   Essa ação limpa o formulário e as _[!UICONTROL First Name]_e_[!UICONTROL Last Name]_ Os campos são realçados.

1. Insira o **[!UICONTROL Email]** endereço do novo administrador de empresa.

   Se o sistema não encontrar o endereço de email no banco de dados, você será solicitado a confirmar se deseja substituir o administrador da empresa.

   - Se não existir uma conta de usuário para o novo administrador da empresa, o sistema criará uma conta da `Company Admin` tipo.

   - Se a conta de usuário existir no sistema, ela será movida para a posição de administrador da empresa na estrutura da empresa.

1. Insira o **[!UICONTROL First Name]** e **[!UICONTROL Last Name]** e quaisquer outras informações aplicáveis ao novo administrador de empresa.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A conta individual do antigo administrador de empresa permanece no sistema como uma conta de usuário individual ativa na estrutura da empresa, atribuída à função de usuário padrão.

   O sistema envia uma notificação por email sobre a alteração para os administradores de empresas novos e antigos.
