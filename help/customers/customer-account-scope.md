---
title: Escopo da conta do cliente
description: O escopo das contas do cliente pode ser limitado ao site onde a conta foi criada ou compartilhado com todos os sites e lojas na hierarquia da loja.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Escopo da conta do cliente

O cabeçalho de cada página da loja estende um convite para que os compradores _Fazer logon ou se registrar_ para uma conta com seu armazenamento. Os clientes que abrem uma conta desfrutam de uma variedade de benefícios, incluindo:

* **Criar conta de cliente** - Os visitantes podem criar uma conta de cliente para que possam usar a loja como um cliente registrado.
* **Criar uma conta de empresa** Dependendo da configuração, um visitante da loja pode optar por criar uma conta da empresa. Para obter mais informações, consulte [Adobe Commerce B2B](../b2b/introduction.md).
* **Check-out mais rápido** — os clientes registrados passam pelo checkout mais rapidamente, pois grande parte das informações já está em suas contas.
* **Autoatendimento** — os clientes registrados podem atualizar suas informações, verificar o status dos pedidos e até mesmo fazer novos pedidos a partir de suas contas.

Os clientes podem acessar suas contas clicando no link **[!UICONTROL My Account]** no cabeçalho da loja. Em suas contas, os clientes podem visualizar e modificar informações, incluindo endereços antigos e atuais, preferências de faturamento e de envio, assinaturas de boletim informativo, lista de desejos e muito mais.

![Minha conta](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Definir o escopo das contas do cliente

O escopo das contas do cliente pode ser limitado ao site onde a conta foi criada ou compartilhado com todos os sites e lojas na hierarquia da loja.

>[!NOTE]
>
>Se o site for excluído do grupo de clientes, o cliente não poderá fazer logon no site quando o escopo das contas do cliente for limitado ao site ou compartilhado com todos os sites. Consulte [Criar um grupo de clientes](customer-groups.md#create-a-customer-group) para obter mais informações sobre como excluir sites de grupos.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Customer Configuration]**.

1. Expanda a **[!UICONTROL Account Sharing Options]** seção.

   ![Opções de compartilhamento de conta](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Share Customer Accounts]** a um dos seguintes:

   | Opção | Descrição |
   | --- | --- |
   | `Global` | Compartilha informações de conta do cliente com cada site e loja na instalação. |
   | `Per Website` | Limita as informações da conta do cliente ao site onde a conta foi criada. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Se necessário, limpe a **[!UICONTROL User system value]** para fazer a alteração.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Quando `Global` está selecionada para as informações do cliente em **Minha conta** (endereços e informações da conta, como detalhes de contato) são compartilhados.
