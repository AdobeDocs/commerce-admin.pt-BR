---
title: Escopo da conta do cliente
description: O escopo das contas do cliente pode ser limitado ao site onde a conta foi criada ou compartilhado com todos os sites e lojas na hierarquia da loja.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
TQID: 'https://experienceleague.adobe.com/ah5XmCeeX4Kc9czcllRq9zZX4W3rkkqkzcoUXtJjo5I'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
    internal-label: 2FA
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 117720d06227a9122059a1f72fa498465b8cc644
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%
---
# Escopo da conta do cliente

O cabeçalho de cada página da sua loja estende um convite para que os compradores _façam logon ou se registrem_ em uma conta da sua loja. Os clientes que abrem uma conta desfrutam de uma variedade de benefícios, incluindo:

* **Criar conta de cliente** - Os visitantes podem criar uma conta de cliente para que possam usar a vitrine como um cliente registrado.
* **Criar uma conta da empresa** Dependendo da configuração, um visitante do seu armazenamento pode optar por criar uma conta da empresa. Para obter mais informações, consulte [Adobe Commerce B2B](../b2b/introduction.md).
* **Check-out mais rápido** — Os clientes registrados passam pelo check-out mais rapidamente porque muitas das informações já estão em suas contas.
* **Autoatendimento** — Os clientes registrados podem atualizar suas informações, verificar o status dos pedidos e até mesmo reordenar de suas contas.

Os clientes podem acessar suas contas clicando no link **[!UICONTROL My Account]** no cabeçalho da loja. Em suas contas, os clientes podem visualizar e modificar informações, incluindo endereços antigos e atuais, preferências de faturamento e de envio, assinaturas de boletim informativo, lista de desejos e muito mais.

![Minha conta](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Definir o escopo das contas do cliente

O escopo das contas do cliente pode ser limitado ao site onde a conta foi criada ou compartilhado com todos os sites e lojas na hierarquia da loja.

>[!NOTE]
>
>Se o site for excluído do grupo de clientes, o cliente não poderá fazer logon no site quando o escopo das contas do cliente for limitado ao site ou compartilhado com todos os sites. Consulte [Criar um grupo de clientes](customer-groups.md#create-a-customer-group) para obter mais informações sobre como excluir sites de grupos.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > **[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Customer Configuration]**.

1. Expanda a seção **[!UICONTROL Account Sharing Options]**.

   ![Opções de Compartilhamento de Conta](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Share Customer Accounts]** como um dos seguintes:

   | Opção | Descrição |
   | --- | --- |
   | `Global` | Compartilha informações de conta do cliente com cada site e loja na instalação. |
   | `Per Website` | Limita as informações da conta do cliente ao site onde a conta foi criada. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Se necessário, desmarque a caixa de seleção **[!UICONTROL User system value]** para fazer a alteração.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Quando `Global` é selecionado, as informações do cliente em **Minha Conta** (endereços e informações da conta, como detalhes de contato) são compartilhadas.
