---
title: Novas opções de conta de cliente
description: Saiba mais sobre as opções de configuração para novas contas de cliente em sua loja.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Novas opções de conta de cliente

No _[!UICONTROL Create New Account Options]_seção da configuração, as opções básicas da conta são combinadas com opções mais avançadas relacionadas à Validação de ID de IVA e integrações personalizadas. As instruções a seguir abordam apenas as opções usadas com mais frequência. Para saber mais sobre atribuições automáticas de grupo de clientes, consulte [Validação de IVA](../stores-purchase/vat.md).

![Criar novas opções de conta](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Configurar as opções básicas de conta de cliente

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Customer Configuration]**.

1. Expanda a **[!UICONTROL Create New Account Options]** seção:

   ![Configurações padrão para Criar Novas Opções de Conta](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Defina cada uma das opções de acordo com a experiência do cliente que você precisa para oferecer suporte na loja:

   - Definir **[!UICONTROL Default Group]** ao grupo de clientes atribuído a novos clientes quando uma conta é criada.

   - Se você tiver uma _Imposto sobre o Valor Agregado_ e quiser que fique visível para os clientes, defina **[!UICONTROL Show VAT Number on Storefront]** para `Yes`.

   - Para solicitar o email de um cliente durante a criação do pedido de Administrador para um cliente, defina **[!UICONTROL Email is required field for Admin order creation]** para `Yes`.

   - Insira o **[!UICONTROL Default Email Domain]** para o armazenamento, como `mystore.com`

   - Definir **[!UICONTROL Default Welcome Email]** ao modelo usado para o email de boas-vindas enviado a novos clientes.

   - Para exigir que os clientes confirmem sua solicitação para abrir uma conta na loja, defina **[!UICONTROL Require Emails Confirmation]** para `Yes`. Em seguida, defina **[!UICONTROL Confirmation Link Email]** ao template usado para o email de confirmação.

     >[!NOTE]
     >
     >A partir da versão 2.4.7, os clientes devem inserir novamente seu email e senha para fazer logon em sua conta após a confirmação por email, independentemente do navegador.

   - Definir **[!UICONTROL Welcome Email]** ao modelo usado para a mensagem Welcome enviada depois que a conta é confirmada.

   - Definir **[!UICONTROL Default Welcome Email without Password]** ao modelo que é usado quando uma conta de cliente criada que ainda não tem uma senha. Por exemplo, uma conta de cliente criada a partir do Administrador ainda não tem uma senha atribuída.

   - Definir **[!UICONTROL Email Sender]** ao contato da loja que aparece como remetente do email de boas-vindas.

   - Para exigir que os clientes confirmem sua solicitação para abrir uma conta na loja, defina **[!UICONTROL Require Emails Confirmation]** para `Yes`. Em seguida, defina **[!UICONTROL Confirmation Link Email]** ao template usado para o email de confirmação.

   ![Criar novas opções de conta com IVA ativado](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Para obter informações detalhadas sobre cada uma das opções disponíveis neste conjunto de opções de configuração, consulte o _Criar novas opções de conta_ [referência de configuração](../configuration-reference/customers/customer-configuration.md).

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
