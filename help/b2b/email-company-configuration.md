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

O [representante de vendas](account-company-manage.md) que é atribuído como o contato principal de uma empresa é configurado por padrão como o remetente de muitas mensagens de email automatizadas enviadas para a empresa.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Company Configuration]**.

1. Se necessário, defina **[!UICONTROL Store View]** para o modo de exibição de repositório para definir o [escopo](../getting-started/websites-stores-views.md#scope-settings) da configuração.

1. Conclua a seção **[!UICONTROL Company Registration]**:

   >[!NOTE]
   >
   >Desmarque a caixa de seleção **[!UICONTROL Use system value]** para tornar o campo editável.

   - Defina **[!UICONTROL Company Registration Email Recipient]** como [contato da loja](../getting-started/store-details.md#store-email-addresses) que deverá ser notificado quando uma nova solicitação de registro da empresa for recebida.

   - No campo **[!UICONTROL Send Company Registration Email Copy To]**, insira o endereço de email de cada pessoa que receberá uma cópia da notificação de registro. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **[!UICONTROL Send Email Copy Method]** como um dos seguintes:

      - `Bcc` - Envia uma _cópia de cortesia oculta_ ao incluir o destinatário no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você preparou um modelo de email que deve ser usado em vez do padrão, defina **[!UICONTROL Default Company Registration Email]** como o nome do modelo. Por padrão, o modelo `Company Registration Request` é usado.

     ![Configuração de clientes - registro de empresa](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Conclua a seção **[!UICONTROL Customer-Related Emails]**:

   Se você preparou modelos de email alternativos a serem usados em vez dos padrões, escolha o modelo que deseja usar para cada um dos seguintes:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuração dos clientes - emails relacionados ao cliente](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Conclua a seção **[!UICONTROL Company Status Change]**:

   - Defina **[!UICONTROL Company Status Change for Email Recipient]** como [contato da loja](../getting-started/store-details.md#store-email-addresses) que deverá ser notificado quando o status de uma empresa for alterado.

   - No campo **[!UICONTROL Send Company Status Change Email Copy To]**, insira o endereço de email de cada pessoa que receberá uma cópia da notificação de alteração de status. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **[!UICONTROL Send Email Copy Method]** como um dos seguintes:

      - `Bcc` - Envia uma _cópia de cortesia oculta_ ao incluir o destinatário no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você tiver um modelo de email preparado para ser usado em vez do padrão quando o status da empresa mudar de `Pending Approval` para `Active`, defina **[!UICONTROL Default 'Company Status Change to Active 1' Email]** para esse modelo. Por padrão, o modelo `Company Status Active 1` é usado.

   - Se você tiver um modelo de email preparado para ser usado em vez do padrão quando o status da empresa mudar de `Rejected` ou `Blocked` para `Active`, defina **[!UICONTROL Default 'Company Status Change to Active 2' Email]** para esse modelo. Por padrão, o modelo `Company Status Active 2` é usado.

   - Se você tiver um modelo de email preparado para ser usado em vez do padrão quando o status da empresa for alterado para `Rejected`, defina **[!UICONTROL Default 'Company Status Change to Rejected' Email]** para esse modelo. Por padrão, o modelo `Company Status Rejected` é usado.

   - Se você tiver um modelo de email preparado para ser usado em vez do padrão quando o status da empresa for alterado para `Blocked`, defina **[!UICONTROL Default 'Company Status Change to Blocked' Email]** para esse modelo. Por padrão, o modelo `Company Status Blocked` é usado.

   - Se você tiver um modelo de email preparado para ser usado em vez do padrão quando o status da empresa for alterado para `Pending Approval`, defina **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** para esse modelo. Por padrão, o modelo `Company Status Pending Approval` é usado.

     ![Configuração de clientes - alteração do status da empresa](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Conclua a seção **[!UICONTROL Company Credit Emails]**:

   - Defina **[!UICONTROL Company Credit Change Email Sender]** como [contato da loja](../getting-started/store-details.md#store-email-addresses) que deverá ser notificado quando for feita uma alteração no limite de crédito atribuído a uma empresa. Por padrão, a notificação é enviada para o _Representante de vendas_.

   - No campo **[!UICONTROL Send Company Credit Change Email Copy To]**, insira o endereço de email de cada pessoa que receberá uma cópia da notificação de alteração de crédito. Separe vários endereços de email com vírgula.

   - Para determinar como a cópia da notificação é enviada, defina **[!UICONTROL Send Email Copy Method]** como um dos seguintes:

      - `Bcc` - Envia uma _cópia de cortesia oculta_ ao incluir o destinatário no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
      - `Separate Email` - Envia a cópia como um email separado.

   - Se você preparou modelos de e-mail a serem usados em vez dos padrões, escolha o modelo para cada uma das notificações a seguir enviadas ao administrador da empresa.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configuração dos clientes - emails de crédito da empresa](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
