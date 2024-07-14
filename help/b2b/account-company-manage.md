---
title: Gerenciar contas da empresa
description: Saiba como gerenciar contas da empresa para sua loja da Adobe Commerce usando a página Empresas e as ferramentas disponíveis na grade.
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: fa8083570a4637c4bf67f7657ef9d0d48f962c50
workflow-type: tm+mt
source-wordcount: '2493'
ht-degree: 0%

---

# Gerenciar contas da empresa

A página _[!UICONTROL Companies]_lista todas as contas da empresa atual, independentemente do status. Todas as solicitações pendentes de aprovação são exibidas na parte superior da lista. Os [controles de local de trabalho](../getting-started/admin-workspace.md) padrão podem ser usados para filtrar a lista, alterar o [layout da coluna](../getting-started/admin-grid-controls.md), salvar exibições ou exportar dados.

O controle _[!UICONTROL Actions]_acima da grade pode ser usado para aplicar uma ação a vários registros da empresa. Por exemplo, em vez de aprovar cada solicitação individual de empresa, você pode selecionar várias solicitações e ativar as contas em uma única ação. As ações disponíveis dependem das [permissões](../systems/permissions.md) para a função atribuída à sua conta de usuário administrador.

Use a função _[!UICONTROL Search]_para localizar empresas na grade **Empresas**por palavra-chave. A pesquisa indexa palavras-chave das colunas **Nome da Empresa**e **Pai**. Você pode filtrar por **Tipo de Empresa**para mostrar somente empresas únicas, somente empresas principais ou somente empresas secundárias.

![Grade de Empresas](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Recursos de função da empresa

As configurações de [Recursos de Função](../systems/permissions-user-roles.md#role-resources) determinam a capacidade de:

- Adicionar uma empresa
- Excluir uma empresa
- Aplicar um reembolso de saldo
- Exibir empresas

Esses recursos de função devem ser definidos para a [Função de Usuário](../systems/permissions-user-roles.md) atribuída à conta de usuário Administrador.

## Aplicar uma ação

As ações a seguir podem ser aplicadas a um ou a vários registros.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Na primeira coluna da grade, marque a caixa de seleção de cada registro que deseja atualizar e siga as instruções para a ação que deseja aplicar:

### Ativar contas da empresa

1. No controle **[!UICONTROL Actions]**, selecione **[!UICONTROL Set Active]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

### Definir como ativo/inativo

Os clientes com contas inativas não podem fazer login ou compras nas contas deles. Há dois métodos para definir uma conta de cliente como ativa ou inativa:

Método 1: **Na grade Clientes**

1. Na barra lateral _Administrador_, vá para [!UICONTROL **Clientes**] > [!UICONTROL **Todos os Clientes**].

1. No menu **[!UICONTROL Actions]**, selecione uma das seguintes opções:

   - **[!UICONTROL Active]**
   - **[!UICONTROL Inactive]**

1. Quando solicitado, selecione **[!UICONTROL OK]** para aplicar a alteração.

Método 2: **Na página de edição da conta**

1. Na barra lateral _Administrador_, vá para [!UICONTROL **Clientes**] > [!UICONTROL **Todos os Clientes**].

1. Na grade, localize o registro do cliente a ser editado.

1. Na coluna _Ações_ na extremidade direita, selecione [!UICONTROL **Editar**].

1. Selecione a guia [!UICONTROL **Informações da conta**].

1. Defina o [!UICONTROL **Cliente Ativo**] como `Yes` ou `No`.

1. Clique em [!UICONTROL **Salvar Cliente**].

### Bloquear contas da empresa

Os usuários associados a uma conta de empresa bloqueada podem fazer logon e acessar o catálogo, mas não podem fazer compras. Uma empresa com uma conta que não esteja em boa situação pode ser temporariamente bloqueada até que o problema seja resolvido.

1. No controle **[!UICONTROL Actions]**, selecione **[!UICONTROL Block]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

### Excluir contas da empresa

As contas da empresa excluídas não podem ser restauradas. O status das contas de usuário associadas à empresa está definido como `Inactive` e a ID da Empresa é removida dos perfis das contas de usuário. As informações sobre a atividade da empresa e as transações são retidas no sistema.

1. No controle **[!UICONTROL Actions]**, selecione **[!UICONTROL Delete]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

### Converter a moeda de crédito

O crédito nas contas das empresas selecionadas é convertido na taxa atual da moeda selecionada.

1. No controle **[!UICONTROL Actions]**, selecione **[!UICONTROL Convert Currency]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

1. Escolha o **[!UICONTROL Credit Currency]** a ser usado para as contas da empresa selecionadas.

   Os valores são recalculados de acordo com as taxas de conversão atuais, se disponíveis. Se não estiver disponível, você poderá inserir manualmente as taxas de conversão personalizadas. O sistema exibe quantos cálculos de conversão são necessários para a moeda de crédito usada pelas empresas selecionadas.

1. Clique em **[!UICONTROL Proceed]** para concluir a conversão.

## Editar uma conta de empresa

Método 1: **Edição rápida**

1. Na primeira coluna, marque a caixa de seleção da conta da empresa a ser editada.

1. No controle **[!UICONTROL Actions]**, selecione **[!UICONTROL Edit]**.

   Cada valor que pode ser atualizado aparece em uma caixa de texto.

   ![Edição rápida de uma conta de empresa](./assets/companies-grid-quick-edit.png){width="700" zoomable="yes"}

1. Atualize qualquer um dos valores a seguir, conforme necessário:

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. Clique em **[!UICONTROL Save]**.

Método 2: **Edição completa**

1. Na grade, localize o registro da empresa a ser editado.

1. Selecione **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Faça as alterações necessárias nas informações da empresa.

Para obter descrições dos campos, consulte [Criar uma conta de empresa](account-company-create.md).

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Atribuir um representante de vendas

O representante de vendas é um [usuário administrador](../systems/permissions.md), que é atribuído como ponto de contato para uma conta da empresa e recebe todas as [mensagens de email](../b2b/enable-basic-features.md#configure-company-email-options) automatizadas relacionadas à empresa. Somente um representante de vendas pode ser atribuído por conta da empresa, mas um único representante de vendas pode gerenciar várias contas da empresa. A conta de usuário Admin padrão é atribuída como representante de vendas, a menos que um usuário Admin diferente seja atribuído.

O nome e o endereço de e-mail do representante de vendas atribuído ficam visíveis para os membros da empresa na página conta e cotações da empresa.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Localize a empresa na grade e abra-a no modo de edição.

1. Defina **[!UICONTROL Sales Representative]** como o usuário Administrador que você deseja atribuir como ponto de contato para a empresa.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   O representante de vendas atribuído recebe notificação por email da atribuição.

## Atualizar um perfil de empresa

O perfil da empresa pode ser mantido na vitrine pelo administrador da empresa, e também pelo Administrador, por um administrador da loja.

![Perfil da empresa](./assets/company-update.png){width="700" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Localize a empresa na grade e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Atualize os valores de campo em cada seção, conforme necessário, usando as descrições de campo para referência.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Demonstração da conta da empresa

Você pode aprender sobre como gerenciar contas da empresa assistindo a este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/344447?quality=12)

## Gerenciamento da empresa

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponível somente para participantes do programa Beta"}

Depois que uma empresa é criada, os usuários administradores com as permissões apropriadas podem usar a seção [!UICONTROL Company Hierarchy] para criar uma organização de empresa principal, editando a empresa principal designada e atribuindo empresas relacionadas.

Se uma empresa foi adicionada a uma hierarquia, a grade [!UICONTROL Company Hierarchy] exibe a empresa principal e todas as empresas atribuídas na grade.

Consulte [Gerenciar hierarquia da empresa](assign-companies.md) para obter mais informações.

## Opções e colunas da empresa

As seções a seguir fornecem uma referência para as ações, opções e informações exibidas disponíveis para gerenciar contas da empresa.

### Opções de controle de ações

| Opção | Descrição |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | Define o status de todos os registros de empresa selecionados como `Active`. Os administradores da empresa recebem instruções para definir suas senhas para que possam acessar suas contas e gerenciar suas empresas na loja. |
| [!UICONTROL Block] | Restringe as contas da empresa que não estão em boa posição, preservando a conta. Os membros da empresa podem fazer logon e acessar o catálogo, mas não podem fazer pedidos em nome da empresa. |
| [!UICONTROL Delete] | Exclui as contas da empresa selecionadas. O status das contas de usuário associadas a uma empresa excluída está definido como `Inactive` e a ID da Empresa é removida dos perfis das contas de usuário. As informações sobre a atividade da empresa e as transações são retidas no sistema. |
| [!UICONTROL Edit] | Permite que alguns valores do registro de empresa selecionado sejam editados na grade. Por padrão, os valores Nome da empresa, Email da empresa e Número de telefone estão disponíveis para uma edição rápida. |
| [!UICONTROL Convert Credit] | Converte o crédito em conta para as empresas selecionadas de acordo com as taxas da moeda especificada. |

{style="table-layout:auto"}

### Descrições da coluna


#### Layout de coluna padrão

| Coluna | Descrição |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | As caixas de seleção usadas para selecionar registros de empresa que serão sujeitos a uma ação ou usar o controle de seleção no cabeçalho da coluna para marcar/desmarcar tudo. |
| [!UICONTROL ID] | Um identificador numérico exclusivo que é atribuído quando a solicitação para criar uma empresa é enviada. |
| [!UICONTROL Company Name] | O nome da empresa é inserido quando a conta da empresa é criada pela primeira vez e pode ser uma versão reduzida do nome legal completo. |
| [!UICONTROL Company Type] | O tipo de [empresa](manage-companies.md). Opções: <br/>**[!UICONTROL Company]**- Por padrão, novas empresas são criadas como empresas únicas.<br/>**[!UICONTROL Parent]** - A empresa é uma empresa principal de outras empresas. <br/>**[!UICONTROL Child]**- Esta empresa está relacionada a uma empresa principal. |
| [!UICONTROL Parent] | Mostra a empresa principal desta linha de empresa específica. |
| [!UICONTROL Company Email] | O endereço de email associado à conta da empresa. |
| [!UICONTROL Phone Number] | O número de telefone principal da empresa. |
| [!UICONTROL Country] | O país onde a empresa está registrada para realizar negócios. |
| [!UICONTROL State Province] | O estado ou província onde a empresa está registrada para realizar negócios. |
| [!UICONTROL City] | A cidade onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Group/Shared Catalog] | O nome da coluna depende se o Catálogo Compartilhado está habilitado na configuração. Opções: <br/>**[!UICONTROL Customer Group]**- Se o Catálogo Compartilhado não estiver habilitado na configuração, especifica o nome do [grupo de clientes](../customers/customer-groups.md) ao qual a empresa pertence.<br/>**[!UICONTROL Shared Catalog]** - Se o Catálogo Compartilhado estiver habilitado na configuração, especifica o nome do catálogo compartilhado atribuído ao cliente. |
| [!UICONTROL Outstanding Balance] | O saldo pendente na conta da empresa. a coluna ficará em branco se a empresa não tiver um histórico de crédito e seu limite de crédito for zero. |
| [!UICONTROL Company Admin] | O nome e sobrenome do administrador da empresa. |
| [!UICONTROL Job Title] | O cargo do administrador da empresa. |
| [!UICONTROL Email] | O endereço de email do administrador da empresa. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Abre a conta da empresa no modo de edição. |

{style="table-layout:auto"}

#### Colunas adicionais

As seguintes colunas estão disponíveis alterando o [layout da coluna](../getting-started/admin-grid-controls.md) da grade.

| Coluna | Descrição |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | O nome legal completo da empresa. |
| [!UICONTROL Street Address] | O endereço onde a empresa está registrada para realizar negócios. |
| [!UICONTROL ZIP] | O CEP ou código postal onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Reseller ID] | O número de revenda atribuído à empresa para fins de relatório de imposto. |
| [!UICONTROL VAT/TAX ID] | O número de [imposto sobre valor agregado](../stores-purchase/vat.md) atribuído à empresa por algumas jurisdições para fins de relatório de imposto. Para configurar a ID de IVA/IMPOSTO do cliente para aparecer na loja, consulte [Criar Novas Opções de Conta](../configuration-reference/customers/customer-configuration.md). |
| [!UICONTROL Credit Limit] | O limite de crédito estendido para a conta da empresa. |
| [!UICONTROL Credit Currency] | A moeda aceita pela loja para compras em crédito da empresa. |
| [!UICONTROL Status] | Indica o [status](account-company-approve.md) da conta da empresa. Opções: <br/>**[!UICONTROL Active]**- A conta da empresa foi aprovada pelo administrador de armazenamento. O administrador da empresa e os membros associados podem fazer logon na conta da loja e fazer compras.<br/>**[!UICONTROL Pending Approval]** - Uma solicitação para abrir uma conta da empresa foi enviada, mas ainda não foi aprovada pelo administrador de armazenamento. <br/>**[!UICONTROL Rejected]**- Uma solicitação para abrir uma conta da empresa foi enviada, mas não foi aprovada pelo administrador de armazenamento. As credenciais de logon iniciais usadas para enviar a solicitação estão bloqueadas.<br/>**[!UICONTROL Blocked]** - Os membros da empresa podem fazer logon e acessar o catálogo, mas não podem fazer compras. O administrador de armazenamento pode bloquear uma conta da empresa que não esteja em boa posição. O bloqueio na conta pode ser removido pelo administrador de armazenamento a qualquer momento. |
| [!UICONTROL Gender] | O sexo do administrador da empresa. Opções: Masculino/Feminino/Não Especificado |
| [!UICONTROL Comment] | Observações sobre a conta da empresa para referência e visível somente do administrador. |

{style="table-layout:auto"}

### Barra de botões

| Botão | Descrição |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Retorna à página Empresas sem salvar as alterações. |
| [!UICONTROL Login as Customer] | Permite que um usuário administrador [faça logon na loja como cliente](../customers/login-as-customer.md) e ajude em seus pedidos. |
| [!DNL Delete Company] | Exclui a conta da empresa. O status das contas de usuário associadas à empresa está definido como `Inactive` e a ID da Empresa é removida dos perfis das contas de usuário. As informações sobre a atividade da empresa e as transações são retidas no sistema. |
| [!DNL Reset] | Restaura os valores originais em todos os campos com alterações não salvas. |
| [!DNL Reimburse Balance] | Permite que o administrador reembolse o saldo do crédito da loja, referenciado pelo número da OC. |
| [!DNL Save] | Salva as alterações na empresa e mantém o perfil aberto. |
| [!UICONTROL Save & Close] | Salva as alterações na empresa e fecha o perfil. |

{style="table-layout:auto"}

### Descrições dos campos

| Campo | Descrição |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | O nome da empresa é inserido quando a conta da empresa é criada pela primeira vez e pode ser uma versão reduzida do nome legal completo. |
| [!UICONTROL Status] | Indica o [status](account-company-approve.md) da conta da empresa. Opções: <br/>**[!UICONTROL Active]**- A conta da empresa foi aprovada pelo administrador de armazenamento. O administrador da empresa e os membros associados podem fazer logon na conta da loja e fazer compras.<br/>**[!UICONTROL Pending Approval]** - Uma solicitação para abrir uma conta da empresa foi enviada, mas ainda não foi aprovada pelo administrador de armazenamento. <br/>**[!UICONTROL Rejected]**- Uma solicitação para abrir uma conta da empresa foi enviada, mas não foi aprovada pelo administrador de armazenamento. As credenciais de logon iniciais usadas para enviar a solicitação estão bloqueadas.<br/>**[!UICONTROL Blocked]** - Os membros da empresa podem fazer logon e acessar o catálogo, mas não podem fazer compras. O administrador de armazenamento pode bloquear uma conta da empresa que não esteja em boa posição. O bloqueio na conta pode ser removido pelo administrador de armazenamento a qualquer momento. |
| [!UICONTROL Company Email] | O endereço de email associado à conta da empresa. |
| [!UICONTROL Sales Representative] | O usuário Administrador que é o contato principal da conta da empresa. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Campo | Descrição |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | O nome legal completo da empresa. |
| [!UICONTROL VAT / TAX ID] | O número de imposto ou [imposto sobre valor agregado](../stores-purchase/vat.md) atribuído à empresa para fins de relatório de imposto. |
| [!UICONTROL Reseller ID] | O número de revenda atribuído à empresa para fins de relatório de imposto. |
| [!UICONTROL Comment] | Essas notas sobre a conta da empresa são para referência e visíveis apenas do administrador. |
| **[!UICONTROL Legal Address]** |                                                                                                                            |
| [!UICONTROL Street Address] | O endereço onde a empresa está registrada para realizar negócios. |
| [!UICONTROL City] | A cidade onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Country] | O país onde a empresa está registrada para realizar negócios. |
| [!UICONTROL State/Province] | O estado ou província onde a empresa está registrada para realizar negócios. |
| [!UICONTROL ZIP/Postal Code] | O CEP ou código postal onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Phone Number] | O número de telefone principal da empresa. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponível somente para participantes do programa Beta"}

| Colunas | Descrição |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | O número de ID da empresa. |
| [!UICONTROL Company Name] | O nome completo da empresa. <br/>Um `current company indicator` aparece na linha da empresa que está sendo editada. |
| [!UICONTROL Company Email] | O endereço de email associado à conta da empresa. |
| [!UICONTROL Phone Number] | O número de telefone principal da empresa. |
| [!UICONTROL State/Province] | O estado ou província onde a empresa está registrada para realizar negócios. |
| [!UICONTROL City] | A cidade onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Customer Group] | (Somente Administrador) Indica o [grupo de clientes](../customers/customer-groups.md) ou o [catálogo compartilhado](catalog-shared.md) atribuído à empresa. |
| [!UICONTROL Company Admin] | O nome completo do administrador da empresa. |
| [!UICONTROL Action] | A lista de ações possíveis para essa linha de empresa. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Campo | Descrição |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Job Title] | O título do administrador da empresa que gerencia a conta da empresa. |
| [!UICONTROL Email] | O endereço de email do administrador da empresa pode ser igual ao endereço de email da empresa. Se um endereço de email diferente for inserido, uma conta individual separada será criada para o administrador da empresa, além da conta da empresa. |
| [!UICONTROL Prefix] | Se aplicável, o prefixo associado ao nome do administrador da empresa (como `Mr.`, `Ms.`, `Mrs.` ou `Dr.`). Dependendo da configuração, o campo de entrada pode ser um campo de texto ou lista. |
| [!UICONTROL First Name] | O nome do administrador da empresa. |
| [!UICONTROL Middle Name/Initial] | O nome do meio ou a inicial do administrador da empresa. |
| [!UICONTROL Last Name] | O sobrenome do administrador da empresa. |
| [!UICONTROL Suffix] | Se aplicável, o sufixo associado ao nome do administrador da empresa (como `Jr.`, `Sr.` ou `III`). Dependendo da configuração, o campo de entrada pode ser um campo de texto ou lista. |
| [!UICONTROL Gender] | O sexo do administrador da empresa. Opções: `Male` / `Female` / `Not Specified` |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Campo | Descrição |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | A moeda aceita pela loja para compras em crédito da empresa. |
| [!UICONTROL Credit Limit] | O limite de crédito estendido para a conta da empresa. |
| [!UICONTROL Allow to Exceed Credit Limit] | Indica se a empresa tem permissão para exceder o limite de crédito. Opções: Sim / Não |
| [!UICONTROL Reason for Change] | Uma nota que explica as circunstâncias em que a empresa pode ou não exceder o limite de crédito. Este campo só estará ativo se a permissão para exceder o limite de crédito for alterada. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| Campo | Descrição |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | Indica o [grupo de clientes](../customers/customer-groups.md) ou o [catálogo compartilhado](catalog-shared.md) atribuído à empresa. |
| [!UICONTROL Allow Quotes] | Determina se os membros da empresa podem preparar e enviar cotações negociáveis em nome da empresa. |
| [!UICONTROL Enable Purchase Orders] | Determina se as Ordens de Compra são permitidas para a empresa. Para que as ordens de compra funcionem para contas de membros da empresa, o administrador da empresa também deve habilitar esse recurso na loja. |
| [!UICONTROL Applicable Payment Methods] | Indica os métodos de pagamento disponíveis para compras da empresa. Opções: `B2B Payment Methods` / `All Enabled Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | (Somente administrador) Fica ativo se métodos de pagamento específicos forem indicados. Para selecionar vários métodos de pagamento, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção. |

{style="table-layout:auto"}
