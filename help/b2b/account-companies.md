---
title: Contas da empresa
description: Saiba como as contas da empresa gerenciadas em sua loja da Adobe Commerce permitem associar vários compradores que pertencem à mesma empresa a uma única conta de empresa.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Contas da empresa

Ao incorporar contas de empresas B2B em sua loja, você pode simplificar a experiência de compra corporativa, permitindo que as empresas criem várias subcontas com permissões flexíveis com base nas funções de usuário em sua organização.

Dependendo da empresa, um administrador de loja pode ajustar promoções e preços para atender às suas necessidades e criar ofertas altamente personalizadas que atendam às demandas dos compradores e aumentem os pedidos.

Adicionar uma associação de conta de empresa a um [indivíduo](../customers/account-create.md) padrão permite que o cliente use os fluxos de trabalho de compra específicos definidos para a empresa.

Vantagens de uma conta de empresa:

- Oferece um número ilimitado de [usuários da empresa](account-company-users.md) e a criação de contas adicionais, o que simplifica as compras corporativas.

- Inclui suporte para uma hierarquia de conta de empresa _inteligente_ com diferentes [funções e permissões](account-company-roles-permissions.md) para fazer pedidos.

- Fornece um mecanismo para comerciantes aumentarem a renda oferecendo [crédito de armazenamento da empresa](credit-company.md) como um método de pagamento.

- Dá suporte ao [gerenciamento](account-company-manage.md) de todas as contas da empresa do Administrador.

## Exibir contas da empresa

A grade _Empresas_ lista todas as contas ativas da empresa e solicitações pendentes, independentemente da configuração de status. Também fornece as ferramentas para [criar](account-company-create.md) e [gerenciar](account-company-manage.md) contas da empresa. Use os controles de grade padrão para filtrar a lista e ajuste o layout da coluna. Para obter uma lista das descrições da coluna, consulte a seção _Descrições da Coluna_ em [Gerenciando Contas da Empresa](account-company-manage.md).

Os clientes podem criar uma conta da empresa na loja ou um comerciante pode criar uma pelo Administrador. Por padrão, a capacidade de criar contas da empresa na loja está habilitada. Se permitido pela configuração, um visitante da loja pode solicitar a abertura de uma conta da empresa. Depois que a conta da empresa for aprovada, o administrador da empresa poderá configurar a estrutura da empresa e os usuários com vários níveis de permissão.

Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Grade de Empresas](./assets/companies-grid.png){width="700" zoomable="yes"}

A grade [!UICONTROL Companies] lista todas as empresas, independentemente do status. A listagem de empresas indica se uma empresa está associada a uma [hierarquia de empresas](manage-company-hierarchy.md) e fornece [informações detalhadas](/help/b2b/account-company-manage.md#company-options-and-columns) sobre a empresa, o administrador da empresa e outras informações. Personalize a exibição usando os [Controles de grade de administração](../getting-started/admin-grid-controls.md) para definir filtros, opções de exibição de coluna e muito mais.

## Administrador da empresa

O exemplo a seguir mostra a grade _Clientes_ com contas de administrador da empresa inicial.

![Grade de clientes com conta de administrador de empresa](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Cada empresa tem um único administrador de empresa identificado pelo endereço de email da conta e pelo nome e sobrenome do administrador. O administrador pode ser atribuído a outras empresas como um usuário, mas ele pode ser um administrador de apenas uma empresa.

Depois de criar a conta, o administrador da empresa define a estrutura da empresa de [equipes](account-company-structure.md), configura os [usuários da empresa](account-company-users.md) e estabelece [funções e permissões](account-company-roles-permissions.md) para cada um.

### Definir senha do administrador da empresa antes da primeira entrada

1. O administrador da empresa encontra um email de boas-vindas da loja.

   ![Exemplo de email de boas-vindas](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >Os destinos de endereço de email e o conteúdo do email são determinados pelas opções especificadas na configuração [opções de email da empresa](email-company-configuration.md).

1. Siga as instruções e clique em [!UICONTROL **link**] para definir sua senha.

1. Digite uma [!UICONTROL **Nova Senha**] e uma confirmação de senha para a conta.

   A senha deve incluir pelo menos três dos seguintes tipos de caracteres:

   - Caracteres em minúsculas (abc...)
   - Caracteres em maiúsculas (ABC...)
   - Números (1234567890)
   - Caracteres especiais (!@#$...)

1. Cliques [!UICONTROL **Definir uma nova senha**].

   ![Logon do cliente - administrador da empresa](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. Quando a página [!UICONTROL Customer Login] for exibida, o cliente digitará seu [!UICONTROL **Email**] e [!UICONTROL **Senha**].

1. Clica em [!UICONTROL **Entrar**] para acessar seu painel de conta.

   ![Painel de Contas - empresa](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Estrutura da empresa

Uma conta de empresa pode ser configurada para refletir a estrutura da empresa. Inicialmente, a estrutura da empresa inclui apenas o administrador da empresa, mas pode ser expandida para incluir equipes de usuários. Os usuários podem ser associados a equipes ou organizados dentro de uma hierarquia de divisões e subdivisões dentro da empresa. A estrutura foi projetada para dar suporte ao uso de [regras de aprovação](account-dashboard-approval-rules.md) para [ordens de compra](purchase-order-flow.md) (OCs) associadas à conta da empresa.

![Estrutura de Empresa com Divisões](./assets/company-structure-diagram.svg){width="450"}

No painel de contas do administrador da empresa, a estrutura da empresa é representada como uma árvore e consiste inicialmente apenas no administrador da empresa.

![Estrutura da Empresa com o Administrador da Empresa](./assets/company-structure-tree-admin.png){width="600"}

Quando a conta é criada, o administrador da empresa pode usar o endereço de email da empresa ou receber um endereço de email diferente.

No exemplo a seguir, a estrutura inicial da empresa inclui o administrador da empresa mais uma conta de usuário individual no nome do administrador da empresa. Mas as funções de administrador da empresa (como estrutura da empresa e regras de aprovação) estão disponíveis somente quando estão conectadas à conta de usuário designada como administrador da empresa.

![Estrutura da Empresa com Conta de Administrador e de Usuário](./assets/company-structure-tree-admin-user.png){width="600"}
