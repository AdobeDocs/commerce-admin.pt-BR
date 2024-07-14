---
title: Estrutura de conta da empresa
description: Saiba mais sobre as estruturas da empresa e como um administrador de empresa pode defini-la para dar suporte a seus fluxos de trabalho e políticas de negócios.
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Estrutura de conta da empresa

Uma conta de empresa pode ser configurada para refletir a estrutura da empresa. Inicialmente, a estrutura da empresa inclui apenas o administrador da empresa, mas pode ser expandida para incluir equipes de usuários. Os usuários podem ser associados a equipes ou organizados dentro de uma hierarquia de divisões e subdivisões dentro da empresa.

![Estrutura de Empresa com Divisões](./assets/company-structure-diagram.svg){width="500"}

No painel de contas do administrador da empresa, a estrutura da empresa é representada como uma árvore e consiste inicialmente apenas no administrador da empresa.

![Estrutura da Empresa com o Administrador da Empresa](./assets/company-structure-tree-admin.png){width="600" zoomable="yes"}

Quando a conta é criada e aprovada, o administrador da empresa pode usar o endereço de email da empresa ou receber um endereço de email diferente.

É possível que a pessoa que atua como administrador da empresa tenha várias funções na empresa. Se um endereço de email separado for inserido para o administrador da empresa, a estrutura inicial da empresa incluirá o administrador da empresa e uma conta de usuário individual no nome do administrador da empresa. Nesse caso, o administrador da empresa pode fazer logon na conta como a empresa ou como um usuário individual.

![Estrutura da Empresa com Conta de Administrador e de Usuário](./assets/company-structure-tree-admin-user.png){width="600" zoomable="yes"}

Para comerciantes, a estrutura completa da empresa é refletida nas grades de _Empresas_ e _Clientes_ no Administrador. A grade Empresas lista todas as empresas independentemente do status. O exemplo a seguir mostra as contas de duas empresas: a empresa _ACME_ e a empresa _Vendelay_.

![Grade de Empresas](./assets/companies-grid.png){width="700" zoomable="yes"}

O exemplo a seguir mostra a grade [!UICONTROL Customers] com as contas de administrador da empresa inicial para essas empresas.

![Grade de clientes com conta de administrador de empresa](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Depois de criar a conta, o administrador da empresa deve definir a estrutura da empresa de [equipes](account-company-structure.md), configurar os [usuários da empresa](account-company-users.md) e estabelecer [funções e permissões](account-company-roles-permissions.md) para cada um.

## Ícones de estrutura da empresa

| Ícone | Descrição |
| ---- | ----------------- |
| ![Ícone de Administrador da Empresa](./assets/company-icon-admin.png) | Representa o administrador da empresa na estrutura da empresa. |
| ![Ícone da equipe](./assets/company-icon-team.png) | Representa uma equipe na estrutura da empresa. |
| ![Ícone de usuário](./assets/company-icon-user.png) | Representa um usuário na estrutura da empresa. |
| ![Ícone Mover](./assets/company-icon-move.png) | Move uma equipe para outra posição na estrutura da empresa. |
| ![Ícone de expansão](./assets/company-icon-expand.png) | Expande uma equipe na estrutura da empresa. |
| ![Ícone Recolher](./assets/company-icon-collapse.png) | Recolhe uma equipe na estrutura da empresa. |

{style="table-layout:auto"}

## Criar equipes da empresa

A estrutura de uma conta de empresa deve refletir a organização de compras, seja ela simples e simples ou uma organização complexa com equipes diferentes para cada subdivisão e divisão da empresa.

Se o armazenamento estiver [configurado](enable-basic-features.md) para permitir que as empresas gerenciem suas próprias contas, a configuração da estrutura da empresa é uma das primeiras tarefas que um administrador de empresa conclua após a aprovação da conta. Na conta da empresa, a estrutura da empresa é representada como uma árvore com o administrador da empresa na parte superior.

![Estrutura da empresa com equipes](./assets/company-structure-teams-diagram.svg){width="450"}

1. O administrador da empresa faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL Company Structure]**.

1. Em **[!UICONTROL Business Structure]**, clica em **[!UICONTROL Add Team]** e faz o seguinte:

   - Insira o **[!UICONTROL Team Title]** e **[!UICONTROL Description]**.

     O Título da equipe pode ser qualquer item que represente a estrutura da empresa, como uma equipe, escritório ou divisão na empresa

     ![Adicionar equipe](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Quando terminar, clica em **[!UICONTROL Save]**.

   - Cria quantas equipes forem necessárias.

     ![Estrutura da empresa com equipes](./assets/company-structure-teams.png){width="600" zoomable="yes"}

1. Para criar uma hierarquia de equipes, faz o seguinte:

   - Seleciona a equipe principal e clique em **[!UICONTROL Add Team]**.

     ![Estrutura de Empresa com Divisões](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Insira o **[!UICONTROL Team Title]** e **[!UICONTROL Description]**.

   - Cliques **[!UICONTROL Save]**.

1. Repete essas etapas para criar quantas equipes ou divisões e subdivisões forem necessárias.

   ![Estrutura da Empresa com Divisões e Subdivisões](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## Mover uma equipe

Como o administrador da empresa trabalha com a estrutura da empresa, ele pode arrastar equipes ou divisões para outros locais na estrutura.

1. O administrador da empresa localiza a equipe a ser movida.

1. Clica e arrasta a equipe para uma nova posição na estrutura da empresa.

## Excluir uma equipe

>[!NOTE]
>
>Antes de excluir um grupo, é recomendável verificar se o grupo correto está selecionado — os grupos excluídos não podem ser restaurados.

1. O administrador da empresa seleciona a equipe a ser excluída.

1. Cliques **[!UICONTROL Delete Selected]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL Delete]**.

## Expandir ou recolher a estrutura da equipe

Como o administrador da empresa trabalha com a estrutura da empresa, ele pode recolher ou expandir a árvore:

- Cliques **[!UICONTROL Collapse All]** ou **[!UICONTROL Expand All]**.

- Clica em ![Ícone Expandido](../assets/icon-display-collapse.png) para recolher uma equipe ou em ![Ícone Recolhido](../assets/icon-display-expand.png) para expandir uma equipe.

## Atribuir usuários às equipes

Quando equipes e usuários são adicionados pela primeira vez à [estrutura da empresa](account-company-structure.md), eles são colocados no mesmo nível sob o administrador da empresa.

![Estrutura da empresa com usuários e equipes](./assets/company-users-added.png){width="700" zoomable="yes"}

| Controle | Descrição |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Recolhe ou expande a árvore de estrutura de negócios |
| [!UICONTROL Add User] | Cria um usuário abaixo da equipe atual |
| [!UICONTROL Add Team] | Cria uma equipe |
| [!UICONTROL Edit Selected / Delete Selected] | Edita ou remove usuários da árvore de negócios |

{style="table-layout:auto"}

1. No painel esquerdo, o administrador da empresa escolhe **[!UICONTROL Company Structure]**.

1. Para atribuir um usuário a uma equipe existente, ele arrasta (![ícone Mover](../assets/icon-move.png)) o usuário para a equipe apropriada.

   ![Atribuições da equipe](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
