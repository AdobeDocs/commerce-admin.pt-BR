---
title: Contas da empresa
description: Saiba como as contas da empresa gerenciadas em sua loja da Adobe Commerce permitem associar vários compradores que pertencem à mesma empresa a uma única conta de empresa.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Contas da empresa

Ao incorporar contas de empresas B2B em sua loja, você pode simplificar a experiência de compra corporativa, permitindo que as empresas criem várias subcontas com permissões flexíveis com base nas funções de usuário em sua organização. Dependendo da empresa, um administrador de loja pode ajustar promoções e preços para atender às suas necessidades e criar ofertas altamente personalizadas que atendam às demandas dos compradores e aumentem os pedidos. Adição de uma associação de conta de empresa a um padrão [individual](../customers/account-create.md) permite que o cliente use os workflows de compras específicos definidos para a empresa.

Vantagens de uma conta de empresa:

- Ofertas ilimitadas [usuários da empresa](account-company-users.md) e a criação de contas adicionais, o que simplifica as compras corporativas.

- Inclui suporte para um _inteligente_ hierarquia de conta da empresa com diferente [funções e permissões](account-company-roles-permissions.md) para fazer pedidos.

- Fornece um mecanismo para os comerciantes aumentarem a renda oferecendo [crédito de loja da empresa](credit-company.md) como um método de pagamento.

- Oferece suporte ao [gerenciamento](account-company-manage.md) de todas as contas da empresa no Administrador.

## Exibir contas da empresa

A variável _Empresas_ a grade lista todas as contas ativas da empresa e solicitações pendentes, independentemente da configuração de status. Fornece também as ferramentas para [criando](account-company-create.md) e [gerenciando](account-company-manage.md) contas da empresa. Use os controles de grade padrão para filtrar a lista e ajuste o layout da coluna. Para obter uma lista de descrições de coluna, consulte _Descrições da coluna_ seção em [Gerenciar contas da empresa](account-company-manage.md).

Os clientes podem criar uma conta da empresa na loja ou um comerciante pode criar uma pelo Administrador. Por padrão, a capacidade de criar contas da empresa na loja está habilitada. Se permitido pela configuração, um visitante da loja pode solicitar a abertura de uma conta da empresa. Depois que a conta da empresa for aprovada, o administrador da empresa poderá configurar a estrutura da empresa e os usuários com vários níveis de permissão.

No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Grade de Empresas](./assets/companies-grid.png){width="700" zoomable="yes"}

A variável [!UICONTROL Companies] A grade lista todas as empresas, independentemente do status. O exemplo exibido mostra as contas de duas empresas: a empresa &quot;ACME&quot; e a empresa &quot;Vandelay&quot;.

## Administrador da empresa

O exemplo a seguir mostra o _Clientes_ grade com as contas iniciais de administrador da empresa.

![Grade de clientes com conta de administrador de empresa](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

É possível que a pessoa que atua como administrador da empresa tenha várias funções na empresa. Se um endereço de email separado for inserido para o administrador da empresa, a estrutura inicial da empresa incluirá o administrador da empresa e uma conta de usuário individual no nome do administrador da empresa. Nesse caso, o administrador da empresa pode fazer logon na conta como a empresa ou como um usuário individual.

Depois de criar a conta, o administrador da empresa define a estrutura da empresa de [equipes](account-company-structure.md), configura o [usuários da empresa](account-company-users.md)e estabelece [funções e permissões](account-company-roles-permissions.md) para cada.

### Definir senha do administrador da empresa antes da primeira entrada

1. O administrador da empresa encontra um email de boas-vindas da loja.

   ![Exemplo de email de boas-vindas](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >Os destinos de endereço de email e o conteúdo do email são determinados pelas opções especificadas na [opções de email da empresa](email-company-configuration.md) configuração.

1. Siga as instruções e clique em [!UICONTROL **link**] para definir sua senha.

1. Insere um [!UICONTROL **Nova senha**] para a conta deles e novamente para confirmar.

   A senha deve incluir pelo menos três dos seguintes tipos de caracteres:

   - Caracteres em minúsculas (abc...)
   - Caracteres em maiúsculas (ABC...)
   - Números (1234567890)
   - Caracteres especiais (!@#$...)

1. Cliques [!UICONTROL **Definir uma nova senha**].

   ![Logon do cliente - administrador da empresa](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. Quando a variável [!UICONTROL Customer Login] for exibida, o cliente inserirá sua [!UICONTROL **E-mail**] e [!UICONTROL **Senha**].

1. Cliques [!UICONTROL **Conectar**] para acessar o painel da conta.

   ![Painel da conta - empresa](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Estrutura da empresa

Uma conta de empresa pode ser configurada para refletir a estrutura da empresa. Inicialmente, a estrutura da empresa inclui apenas o administrador da empresa, mas pode ser expandida para incluir equipes de usuários. Os usuários podem ser associados a equipes ou organizados dentro de uma hierarquia de divisões e subdivisões dentro da empresa. A estrutura foi concebida para apoiar a utilização de [regras de aprovação](account-dashboard-approval-rules.md) para [ordens de compra](purchase-order-flow.md) (POs) associado à conta da empresa.

![Estrutura da Empresa com Divisões](./assets/company-structure-diagram.svg){width="450"}

No painel de contas do administrador da empresa, a estrutura da empresa é representada como uma árvore e consiste inicialmente apenas no administrador da empresa.

![Estrutura da empresa com o administrador da empresa](./assets/company-structure-tree-admin.png){width="600"}

Quando a conta é criada, o administrador da empresa pode usar o endereço de email da empresa ou receber um endereço de email diferente.

No exemplo a seguir, a estrutura inicial da empresa inclui o administrador da empresa mais uma conta de usuário individual no nome do administrador da empresa. Mas as funções de administrador da empresa (como estrutura da empresa e regras de aprovação) estão disponíveis somente quando estão conectadas à conta de usuário designada como administrador da empresa.

![Estrutura da empresa com administrador e conta de usuário](./assets/company-structure-tree-admin-user.png){width="600"}
