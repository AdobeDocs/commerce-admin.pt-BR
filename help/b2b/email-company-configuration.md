---
title: Configurar email da empresa
description: Saiba mais sobre as opções de email e modelos usados para enviar comunicações para contas da empresa.
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# Configurar opções de email da empresa

A variável [representante de vendas](account-company-manage.md) atribuído como contato principal de uma empresa é configurado por padrão como remetente de muitas mensagens de email automatizadas enviadas para a empresa.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Company Configuration]**.

1. Se necessário, defina **[!UICONTROL Store View]** à exibição de loja para definir o [escopo](../getting-started/websites-stores-views.md#scope-settings) da configuração.

1. Conclua o **[!UICONTROL Company Registration]** seção:

   >[!NOTE]
   >
   >Limpe a **[!UICONTROL Use system value]** para tornar o campo editável.

   - Definir **[!UICONTROL Company Registration Email Recipient]** para o [armazenar contato](../getting-started/store-details.md#store-email-addresses) quem será notificado quando for recebida uma nova solicitação de registro de empresa.

   - No **[!UICONTROL Send Company Registration Email Copy To]** insira o endereço de email de cada pessoa que receberá uma cópia da notificação de registro. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **[!UICONTROL Send Email Copy Method]** a um dos seguintes:

      - `Bcc` - Envia um _cópia cega de cortesia_ incluindo o recipient no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você preparou um template de email que deve ser usado em vez do padrão, defina **[!UICONTROL Default Company Registration Email]** ao nome do template. Por padrão, a variável `Company Registration Request` modelo é usado.

     ![Configuração de clientes - registro da empresa](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Conclua o **[!UICONTROL Customer-Related Emails]** seção:

   Se você preparou modelos de email alternativos a serem usados em vez dos padrões, escolha o modelo que deseja usar para cada um dos seguintes:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuração dos clientes - emails relacionados ao cliente](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Conclua o **[!UICONTROL Company Status Change]** seção:

   - Definir **[!UICONTROL Company Status Change for Email Recipient]** para o [armazenar contato](../getting-started/store-details.md#store-email-addresses) quem deve ser notificado quando o status de uma empresa mudar.

   - No **[!UICONTROL Send Company Status Change Email Copy To]** insira o endereço de email de cada pessoa que receberá uma cópia da notificação de alteração de status. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **[!UICONTROL Send Email Copy Method]** a um dos seguintes:

      - `Bcc` - Envia um _cópia cega de cortesia_ incluindo o recipient no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você tiver um modelo de email preparado que deve ser usado em vez do padrão quando o status da empresa mudar de `Pending Approval` para `Active`, definir **[!UICONTROL Default 'Company Status Change to Active 1' Email]** para esse modelo. Por padrão, a variável `Company Status Active 1` modelo é usado.

   - Se você tiver um modelo de email preparado que deve ser usado em vez do padrão quando o status da empresa mudar de `Rejected` ou `Blocked` para `Active`, definir **[!UICONTROL Default 'Company Status Change to Active 2' Email]** para esse modelo. Por padrão, a variável `Company Status Active 2` modelo é usado.

   - Se você tiver um template de email preparado que deve ser usado em vez do padrão quando o status da empresa for alterado para `Rejected`, definir **[!UICONTROL Default 'Company Status Change to Rejected' Email]** para esse modelo. Por padrão, a variável `Company Status Rejected` modelo é usado.

   - Se você tiver um template de email preparado que deve ser usado em vez do padrão quando o status da empresa for alterado para `Blocked`, definir **[!UICONTROL Default 'Company Status Change to Blocked' Email]** para esse modelo. Por padrão, a variável `Company Status Blocked` modelo é usado.

   - Se você tiver um template de email preparado que deve ser usado em vez do padrão quando o status da empresa for alterado para `Pending Approval`, definir **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** para esse modelo. Por padrão, a variável `Company Status Pending Approval` modelo é usado.

     ![Configuração dos clientes - alteração do status da empresa](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Conclua o **[!UICONTROL Company Credit Emails]** seção:

   - Definir **[!UICONTROL Company Credit Change Email Sender]** para o [armazenar contato](../getting-started/store-details.md#store-email-addresses) quem deve ser notificado quando for feita uma alteração no limite de crédito atribuído a uma empresa. A notificação é enviada para _Representante de Vendas_.

   - No **[!UICONTROL Send Company Credit Change Email Copy To]** insira o endereço de email de cada pessoa que receberá uma cópia da notificação de alteração de crédito. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **[!UICONTROL Send Email Copy Method]** a um dos seguintes:

      - `Bcc` - Envia um _cópia cega de cortesia_ incluindo o recipient no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você preparou modelos de e-mail a serem usados em vez dos padrões, escolha o modelo para cada uma das notificações a seguir enviadas ao administrador da empresa.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configuração dos clientes - emails de crédito da empresa](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
