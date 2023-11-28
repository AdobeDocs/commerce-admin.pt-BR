---
title: Criar uma conta de empresa
description: Saiba mais sobre a criação de contas da empresa no Administrador do Adobe Commerce e na loja.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 1123cf4b257a83a61914c378104c43e952512e7d
workflow-type: tm+mt
source-wordcount: '1770'
ht-degree: 0%

---

# Criar uma conta de empresa

As contas da empresa podem ser configuradas na loja pelo cliente ou pelo administrador. Todas as solicitações para criar uma conta da empresa devem ser aprovadas pelo administrador de armazenamento antes que a conta se torne ativa.

A pessoa que configura uma conta de empresa na loja recebe uma função como a [administrador da empresa](account-company-admin.md). Depois que a solicitação para criar uma conta da empresa for aprovada, o administrador da empresa poderá definir uma senha de conta e fazer logon na conta.

## Método 1: o cliente cria a conta da loja

>[!IMPORTANT]
>
>Para dar suporte a esse método (permitindo que os clientes registrem a empresa na loja), verifique se [Recursos B2B](enable-basic-features.md) são configurados para que **[!UICONTROL Allow Company Registration from the Storefront]** está definida como `Yes`.

1. No canto superior direito do cabeçalho da loja, o cliente clica em **[!UICONTROL Create an Account]** e escolhe **[!UICONTROL Create New Company Account]**.

   ![Criar nova conta da empresa](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >Se um visitante estiver conectado a uma conta de usuário registrada, poderá criar uma conta da empresa navegando até _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**. Após a criação da conta da empresa, a conta do cliente é atribuída como o contato principal. Caso contrário, o sistema criará um cliente, que receberá um email para definir uma senha.

1. No _[!UICONTROL Company Information]_, o cliente faz o seguinte:

   - Preenche os campos obrigatórios:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Preenche os campos restantes, conforme aplicável:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Re-seller ID]**

   ![Informações da Empresa](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. Preenche os campos obrigatórios na _[!UICONTROL Legal Address]_seção.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

   ![Endereço legal](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. No _[!UICONTROL Company Administrator]_faz o seguinte:

   - Insere o **[!UICONTROL Email address]** para o administrador da empresa.

     O endereço de email do administrador da empresa pode ser igual ao endereço de email da empresa ou um endereço de email diferente. Se um endereço de email diferente for inserido, uma conta de usuário da empresa será criada, além da conta de administrador da empresa.

   - Insere o **[!UICONTROL First Name]** e **[!UICONTROL Last Name]** do administrador da empresa.

   - Opcionalmente, preenche os seguintes campos:

      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**

   ![Administrador da empresa](./assets/company-administrator-account-storefront.png)

1. Conclui a validação se o reCAPTCHA estiver habilitado para esta função de loja.

1. Quando as informações estiverem completas, clique em **[!UICONTROL Submit]**.

   Quando a solicitação para criar uma conta da empresa é aprovada pelo comerciante, a notificação por email é enviada ao administrador da empresa.

   ![Exemplo de email de boas-vindas](./assets/company-admin-welcome-email.png){width="500"}

   Quando a senha é definida, o administrador da empresa pode [fazer logon](../customers/customer-sign-in.md) para a conta.

## Método 2: o comerciante cria a conta do administrador

O processo de criação de uma empresa pelo Administrador é essencialmente o mesmo da loja, mas com campos adicionais.

![Nova Empresa](./assets/company-update.png){width="700" zoomable="yes"}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Clique em **[!UICONTROL Add New Company]** e faça o seguinte:

   - Preencha estes campos obrigatórios:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Se você não estiver pronto para ativar a conta, defina **[!UICONTROL Status]** para `Pending Approval`. (Defina como `Active` por padrão.)

   - Se aplicável, escolha a conta de administrador do **[!UICONTROL Sales Representative]** quem gerenciará a conta.

1. No _[!UICONTROL Account Information]_faça o seguinte:

   - Preencha os seguintes campos conforme aplicável:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   - Para **[!UICONTROL Comment]**, insira quaisquer informações adicionais sobre o cliente que possam ser necessárias.

     Os comentários são visíveis somente no Administrador.

   ![Informações da conta](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. Na criação inicial da empresa, a variável _[!UICONTROL Company Hierarchy]_A grade fica vazia quando você a expande. Depois de salvar a empresa, você pode incluí-la em uma hierarquia de empresa. Consulte [Gerenciamento da Empresa](manage-companies.md).

1. No _[!UICONTROL Legal Address]_preencha estes campos obrigatórios:

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City Country]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

1. No _[!UICONTROL Company Admin]_faça o seguinte:

   - Preencha estes campos obrigatórios:

      - **[!UICONTROL Email]**
      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**

   - Preencha as seguintes partes opcionais do nome, que podem ser aplicáveis a alguns nomes de clientes mais do que outros e podem ser usadas a seu critério:

      - **[!UICONTROL Prefix]**
      - **[!UICONTROL Middle Name/Initial]**
      - **[!UICONTROL Suffix]**

   - Se as informações estiverem disponíveis, preencha os campos restantes para descrever o administrador da empresa:

      - **[!UICONTROL Website]**
      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**
      - **[!UICONTROL Send Welcome Email From]**

   ![Administrador da empresa](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. No _[!UICONTROL Company Credit]_que exibe um resumo da atividade de crédito do cliente, preencha quantos campos na parte inferior da seção forem aplicáveis:

   - **[!UICONTROL Credit Currency]**
   - **[!UICONTROL Credit Limit]**
   - **[!UICONTROL Allow to Exceed Credit Limit]**
   - **[!UICONTROL Reason for Change]**

   ![Crédito da empresa](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. No _[!UICONTROL Advanced Settings]_faça o seguinte:

   >[!NOTE]
   >
   >A atribuição do grupo de clientes determina qual catálogo compartilhado está disponível para a empresa e seus funcionários. Por padrão, a empresa é atribuída ao grupo de clientes definido como padrão na configuração.

   - Você pode alterar a **[!UICONTROL Customer Group]** atribuição da empresa e seus funcionários a um grupo que tenha acesso a um catálogo compartilhado diferente ou a um grupo de clientes padrão. Você será solicitado a confirmar antes que o grupo seja alterado.

     ![Alterando o grupo de clientes](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   - Se você quiser permitir que os funcionários da empresa gerem cotações a partir de sua conta, defina **[!UICONTROL Allow Quotes]** para `Yes`.

   - Se você quiser permitir que os funcionários da empresa criem e usem ordens de compra a partir de suas contas, defina **[!UICONTROL Enable Purchase Orders]** para `Yes`.

   - Para alterar o **[!UICONTROL Applicable Payment Methods]** que estiverem disponíveis para a empresa, limpe a **[!UICONTROL Use config settings]** e escolha uma das seguintes opções:

     | Opção | Descrição |
     | ------ | ----------- |
     | `B2B Payment Methods` | (Padrão) Habilita tudo [métodos de pagamento definidos como padrão](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods) para ordens B2B. |
     | `All Enabled Payment Methods` | Torna tudo [métodos de pagamento ativados](../configuration-reference/sales/payment-methods.md) disponível para contas de clientes associadas à conta da empresa. |
     | `Selected Payment Methods` | Permite selecionar os métodos de pagamento disponíveis para contas de clientes associadas à conta da empresa. Para selecionar vários métodos de pagamento, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção. |

     {style="table-layout:auto"}

   - Para alterar o **[!UICONTROL Applicable Shipping Methods]** que estiverem disponíveis para a empresa, limpe a **[!UICONTROL Use config settings]** e escolha uma das seguintes opções:

     | Opção | Descrição |
     | ------ | ----------- |
     | `B2B Shipping Methods` | (Padrão) Habilita tudo [métodos de envio definidos como padrão](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) para ordens B2B. |
     | `All Enabled Shipping Methods` | Torna tudo [métodos de envio ativados](../configuration-reference/sales/delivery-methods.md) disponível para contas de clientes associadas à conta da empresa. |
     | `Selected Shipping Methods` | Permite selecionar os métodos de entrega disponíveis para contas de clientes associadas à conta da empresa. Para selecionar vários métodos de envio, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção. |

     {style="table-layout:auto"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

   Quando a solicitação para criar uma conta da empresa é aprovada pelo comerciante, uma notificação por email é enviada para o endereço de email do administrador da empresa.

   Quando a senha é definida, o administrador da empresa pode [fazer logon](../customers/customer-sign-in.md) para a conta.

## Barra de botões

| Botão | Descrição |
|------- | ----------- |
| [!UICONTROL Back] | Retorna à página Empresas sem salvar as alterações. |
| [!UICONTROL Reset] | Restaura os valores originais em todos os campos com alterações não salvas. |
| [!UICONTROL Save] | Salva as alterações na empresa e mantém o perfil aberto. |
| [!UICONTROL Save & Close] | Salva as alterações na empresa e fecha o perfil. |

{style="table-layout:auto"}

## Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Company Name] | O nome da empresa é inserido quando a conta da empresa é criada pela primeira vez e pode ser uma versão reduzida do nome legal completo. |
| [!UICONTROL Status] | (Somente administrador) Indica o estado atual da conta da empresa. Opções: <br/>**[!UICONTROL Active]**- A conta da empresa foi aprovada pelo administrador de armazenamento. O administrador da empresa e os membros associados podem fazer logon na conta da loja e fazer compras.<br/>**[!UICONTROL Pending Approval]** - Uma solicitação para abrir uma conta da empresa foi enviada, mas ainda não foi aprovada pelo administrador de armazenamento. <br/>**[!UICONTROL Rejected]**- Uma solicitação para abrir uma conta da empresa foi enviada, mas não foi aprovada pelo administrador de armazenamento. As credenciais de logon iniciais usadas para enviar a solicitação estão bloqueadas.<br/>** Bloqueado **- Os membros da empresa podem fazer logon e acessar o catálogo, mas não podem fazer compras. O administrador de armazenamento pode bloquear uma conta da empresa que não esteja em boa posição. O bloqueio na conta pode ser removido pelo administrador de armazenamento a qualquer momento. |
| [!UICONTROL Company Email] | O endereço de email associado à conta da empresa. |
| [!UICONTROL Sales Representative] | (Somente administrador) O usuário administrador que é o contato principal da conta da empresa. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Company Legal Name] | O nome legal completo da empresa. |
| [!UICONTROL VAT / TAX ID] | A variável [imposto sobre o valor acrescentado](../stores-purchase/vat.md) número atribuído à empresa por algumas jurisdições para fins de relatório de imposto. Para configurar a ID de IVA/IMPOSTO do cliente para aparecer na loja, consulte [Criar novas opções de conta](../configuration-reference/customers/customer-configuration.md). <br/> **_Nota:_** O administrador da empresa e outros utilizadores da empresa não têm os seus próprios números de identificação IVA/FISCAL separados nas suas contas de clientes. |
| [!UICONTROL Reseller ID] | O número de revenda atribuído à empresa para fins de relatório de imposto. |
| [!UICONTROL Comment] | (Somente administrador) Essas notas sobre a conta da empresa são para referência e visíveis somente do administrador. |

{style="table-layout:auto"}

### [!UICONTROL Company Hierarchy]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Company ID] | O número de ID da empresa. |
| [!UICONTROL Company Name] | O nome completo da empresa. <br/>A `current company indicator` aparece na linha da empresa que está sendo editada. |
| [!UICONTROL Company Email] | O endereço de email associado à conta da empresa. |
| [!UICONTROL Phone Number] | O número de telefone principal da empresa. |
| [!UICONTROL State/Province] | O estado ou província onde a empresa está registrada para realizar negócios. |
| [!UICONTROL City] | A cidade onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Customer Group] | (Somente administrador) Indica a [grupo de clientes](../customers/customer-groups.md) ou [catálogo compartilhado](catalog-shared.md) que é atribuído à empresa. |
| [!UICONTROL Company Admin] | O nome completo do administrador da empresa. |
| [!UICONTROL Action] | A lista de ações possíveis para essa linha de empresa. |

{style="table-layout:auto"}

### [!UICONTROL Legal Address]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Street Address] | O endereço onde a empresa está registrada para realizar negócios. |
| [!UICONTROL City] | A cidade onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Country] | O país onde a empresa está registrada para realizar negócios. |
| [!UICONTROL State/Province] | O estado ou província onde a empresa está registrada para realizar negócios. |
| [!UICONTROL ZIP/Postal Code] | O CEP ou código postal onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Phone Number] | O número de telefone principal da empresa. |

{style="table-layout:auto"}

### [!UICONTROL Company Admin]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Website] | Determina o site ao qual o administrador da empresa pertence. |
| [!UICONTROL Job Title] | O título do administrador da empresa que gerencia a conta da empresa. |
| [!UICONTROL Email] | O endereço de email do administrador da empresa pode ser igual ao endereço de email da empresa. Se um endereço de email diferente for inserido, uma conta individual separada será criada para o administrador da empresa, além da conta da empresa. |
| [!UICONTROL Prefix] | Se aplicável, o prefixo associado ao nome do administrador da empresa (como `Mr.`, `Ms.`, `Mrs.`ou `Dr.`). Dependendo da configuração, o campo de entrada pode ser um campo de texto ou lista. |
| [!UICONTROL First Name] | O nome do administrador da empresa. |
| [!UICONTROL Middle Name/Initial] | O nome do meio ou a inicial do administrador da empresa. |
| [!UICONTROL Last Name] | O sobrenome do administrador da empresa. |
| [!UICONTROL Suffix] | Se aplicável, o sufixo associado ao nome do administrador da empresa (como `Jr.`, `Sr.`ou `III.`). Dependendo da configuração, o campo de entrada pode ser um campo de texto ou lista. |
| [!UICONTROL Gender] | O sexo do administrador da empresa. Opções: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | A exibição de loja da qual o email de boas-vindas deve ser enviado. |

{style="table-layout:auto"}

### [!UICONTROL Company Credit]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Credit Currency] | (Somente administrador) A moeda aceita pela loja para compras em crédito da empresa. |
| [!UICONTROL Credit Limit] | (Somente Administrador) O limite de crédito estendido para a conta da empresa. |
| [!UICONTROL Allow to Exceed Credit Limit] | (Somente Administrador) Indica se a empresa tem permissão para exceder o limite de crédito. Opções: `Yes` / `No` |
| [!UICONTROL Reason for Change] | (Somente administrador) Uma nota que explica por que a empresa tem ou não permissão para exceder o limite de crédito. Este campo só estará ativo se a permissão para exceder o limite de crédito for alterada. |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Customer Group] | (Somente administrador) Indica a [grupo de clientes](../customers/customer-groups.md) ou [catálogo compartilhado](catalog-shared.md) que é atribuído à empresa. |
| [!UICONTROL Allow Quotes] | (Somente Administrador) Determina se os membros da empresa podem preparar e enviar cotações negociáveis em nome da empresa. |
| [!UICONTROL Enable Purchase Orders] | (Somente Administrador) Determina se os membros da empresa podem enviar pedidos como [ordens de compra](account-dashboard-my-purchase-orders.md) em nome da empresa. |
| Métodos de pagamento aplicáveis | (Somente Administrador) Indica os métodos de pagamento disponíveis para compras da empresa. Opções: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | (Somente Administrador) Fica ativo se métodos de pagamento específicos estiverem ativados. Para disponibilizar vários métodos de pagamento para a conta da empresa, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção. |
| [!UICONTROL Applicable Shipping Methods] | (Somente Administrador) Indica os métodos de envio disponíveis para compras da empresa. Opções: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | (Somente administrador) Fica ativo se métodos específicos de envio forem ativados. Para disponibilizar vários métodos de pagamento para a conta da empresa, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção. |

{style="table-layout:auto"}
