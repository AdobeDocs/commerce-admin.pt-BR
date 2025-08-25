---
title: Criar uma conta de empresa
description: Saiba mais sobre a criação de contas da empresa no Administrador do Adobe Commerce e na loja.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 2e119bcb8278432bde1c12f3f44a112cde59fb18
workflow-type: tm+mt
source-wordcount: '2444'
ht-degree: 0%

---

# Criar uma conta de empresa

As contas da empresa permitem que as empresas B2B gerenciem suas compras, usuários e crédito no Adobe Commerce. Este tópico aborda o processo completo de criação, configuração e ativação de contas da empresa.

## Visão geral da criação da conta da empresa

As contas da empresa podem ser criadas por meio de dois métodos, cada um adequado para diferentes cenários de negócios:

* **Registro de vitrine**—Solicitações de conta de autoatendimento feitas por empresas
* **Criação de Administrador**—Configuração de conta assistida por vendas com detalhes pré-configurados

Todas as contas da empresa exigem aprovação do administrador antes de se tornarem ativas, garantindo a verificação e a configuração adequadas.

## Pré-requisitos

Antes de criar contas da empresa, verifique se os seguintes requisitos foram atendidos:

* **Requisitos do Sistema:**
   * [Os recursos B2B estão habilitados](enable-basic-features.md) na sua instalação do Adobe Commerce
   * O registro da empresa está habilitado para criação de vitrine eletrônica
   * As notificações por email estão configuradas para fluxos de trabalho de aprovação

* **Requisitos Comerciais:**
   * Os processos e as políticas de aprovação são estabelecidos
   * Os representantes de vendas são atribuídos (para contas criadas pelo administrador)
   * As políticas de crédito são definidas (se estiver usando crédito da empresa)
   * Grupos de clientes e catálogos compartilhados estão configurados

* **Acesso Administrativo:**
   * Permissões apropriadas para o gerenciamento da empresa
   * Acesso às seções de administração de clientes e empresas

O sistema atribui a função de [administrador de empresa](account-company-admin.md) à pessoa que configura uma conta de empresa na loja. Depois que o administrador de armazenamento aprovar a solicitação de criação de conta da empresa no Administrador, o administrador da empresa poderá definir uma senha de conta e fazer logon na conta.

## Método 1: o cliente cria a conta da loja

**Quando Usar Este Método:**

* O registro comercial por autoatendimento é preferido
* Os clientes têm todas as informações de negócios necessárias prontamente disponíveis
* O fluxo de trabalho de aprovação padrão é suficiente
* Nenhuma configuração especial ou pré-preenchimento é necessário

>[!IMPORTANT]
>
>Para dar suporte a este método (permitindo que os clientes registrem sua empresa na loja), verifique se os [Recursos B2B](enable-basic-features.md) estão habilitados.

1. No canto superior direito do cabeçalho da loja, o cliente clica em **[!UICONTROL Create an Account]** e escolhe **[!UICONTROL Create New Company Account]**.

   ![Criar nova conta da empresa](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >Se um visitante estiver conectado a uma conta de usuário registrada, ele poderá criar uma conta da empresa navegando até _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**.

1. Na seção _[!UICONTROL Company Information]_, o cliente faz o seguinte:

   * Preenche os campos obrigatórios:

      * **[!UICONTROL Company Name]**
      * **[!UICONTROL Company Email]**

   * Preenche os campos restantes, conforme aplicável:

      * **[!UICONTROL Company Legal Name]**
      * **[!UICONTROL VAT/TAX ID]**
      * **[!UICONTROL Reseller ID]**

   ![Informações da Empresa](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. Preenche os campos obrigatórios na seção _[!UICONTROL Legal Address]_.

   * **[!UICONTROL Street Address]**
   * **[!UICONTROL City]**
   * **[!UICONTROL Country]**
   * **[!UICONTROL State/Province]**
   * **[!UICONTROL ZIP/Postal Code]**
   * **[!UICONTROL Phone Number]**

   ![Endereço Legal](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. Na seção _[!UICONTROL Company Administrator]_, faz o seguinte:

   * Digite o **[!UICONTROL Email address]** para o administrador da empresa.

     O endereço de email do administrador da empresa pode ser igual ao endereço de email da empresa ou um endereço de email diferente. Se você inserir um endereço de email diferente, o sistema criará uma conta de usuário da empresa, além da conta de administrador da empresa.

   * Insira as **[!UICONTROL First Name]** e **[!UICONTROL Last Name]** do administrador da empresa.

   * Opcionalmente, preenche os seguintes campos:

      * **[!UICONTROL Job Title]**
      * **[!UICONTROL Work Phone Number]**
      * **[!UICONTROL Gender]**

   ![Administrador da empresa](./assets/company-administrator-account-storefront.png)

1. Conclui a validação se o reCAPTCHA estiver habilitado para esta função de loja.

1. Quando a informação estiver completa, selecione **[!UICONTROL Submit]**.

   Quando o comerciante aprova a solicitação para criar uma conta da empresa, o sistema envia uma notificação por email para o administrador da empresa.

   ![Exemplo de email de boas-vindas](./assets/company-admin-welcome-email.png){width="500"}

   Quando a senha é definida, o administrador da empresa pode [entrar](../customers/customer-sign-in.md) na conta.

## Método 2: o comerciante cria a conta do administrador

**Quando Usar Este Método:**

* A criação de contas assistidas por vendas é preferível
* Preenchimento prévio de detalhes da conta a partir de relacionamentos comerciais existentes
* A configuração personalizada é necessária (limites de crédito, preços especiais)
* É necessária a ativação imediata sem fluxo de trabalho de aprovação

O processo de criação de uma empresa pelo Administrador é essencialmente o mesmo da loja, mas com campos adicionais.

![Adicionar uma nova empresa do Administrador](./assets/company-add-new.png){width="700" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Clique em **[!UICONTROL Add New Company]** e faça o seguinte:

   * Preencha estes campos obrigatórios:

      * **[!UICONTROL Company Name]**
      * **[!UICONTROL Company Email]**

   * Se você não estiver pronto para ativar a conta, defina **[!UICONTROL Status]** como `Pending Approval`. (Definido como `Active` por padrão.)

   * Se aplicável, escolha a conta de administrador do **[!UICONTROL Sales Representative]** que gerenciará a conta.

1. Na seção _[!UICONTROL Account Information]_, faça o seguinte:

   * Preencha os seguintes campos conforme aplicável:

      * **[!UICONTROL Company Legal Name]**
      * **[!UICONTROL VAT/TAX ID]**
      * **[!UICONTROL Reseller ID]**

   * Para **[!UICONTROL Comment]**, insira todas as informações adicionais sobre o cliente que possam ser necessárias.

     Os comentários são visíveis somente no Administrador.

   ![Informações da conta](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. Ao criar uma empresa inicialmente, a grade _[!UICONTROL Company Hierarchy]_&#x200B;aparece vazia quando você a expande. Depois de salvar a empresa, você pode incluí-la em uma hierarquia de empresa. Consulte [Gerenciamento da Empresa](manage-companies.md).

1. Na seção _[!UICONTROL Legal Address]_, preencha estes campos obrigatórios:

   * **[!UICONTROL Street Address]**
   * **[!UICONTROL City]**
   * **[!UICONTROL Country]**
   * **[!UICONTROL ZIP/Postal Code]**
   * **[!UICONTROL Phone Number]**

1. Na seção _[!UICONTROL Company Admin]_, faça o seguinte:

   * Preencha estes campos obrigatórios:

      * **[!UICONTROL Email]**
      * **[!UICONTROL First Name]**
      * **[!UICONTROL Last Name]**

   * Preencha as seguintes partes opcionais do nome, que podem ser aplicáveis a alguns nomes de clientes mais do que outros e podem ser usadas a seu critério:

      * **[!UICONTROL Prefix]**
      * **[!UICONTROL Middle Name/Initial]**
      * **[!UICONTROL Suffix]**

   * Se as informações estiverem disponíveis, preencha os campos restantes para descrever o administrador da empresa:

      * **[!UICONTROL Website]**
      * **[!UICONTROL Job Title]**
      * **[!UICONTROL Work Phone Number]**
      * **[!UICONTROL Gender]**
      * **[!UICONTROL Send Welcome Email From]**

   ![Administrador da Empresa](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Na seção _[!UICONTROL Company Credit]_, que exibe um resumo da atividade de crédito do cliente, preencha quantos campos na parte inferior da seção forem aplicáveis:

   * **[!UICONTROL Credit Currency]**
   * **[!UICONTROL Credit Limit]**
   * **[!UICONTROL Allow to Exceed Credit Limit]**
   * **[!UICONTROL Reason for Change]**

   ![Crédito da empresa](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. Na seção _[!UICONTROL Advanced Settings]_, faça o seguinte:

   >[!NOTE]
   >
   >A atribuição do grupo de clientes determina qual catálogo compartilhado está disponível para a empresa e seus funcionários. Por padrão, o sistema atribui a empresa ao grupo de clientes configurado como padrão.

   * Você pode alterar a atribuição **[!UICONTROL Customer Group]** da empresa e de seus funcionários para um grupo que tenha acesso a um catálogo compartilhado diferente ou a um grupo de clientes padrão. O sistema solicita que você confirme antes de alterar o grupo.

     ![Alterando o grupo de clientes](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   * Se você quiser permitir que os funcionários da empresa gerem cotações a partir de suas contas, defina **[!UICONTROL Allow Quotes]** como `Yes`.

   * Se você quiser permitir que os funcionários da empresa criem e usem ordens de compra a partir de suas contas, defina **[!UICONTROL Enable Purchase Orders]** como `Yes`.

   * Para alterar os **[!UICONTROL Applicable Payment Methods]** que estão disponíveis para a empresa, desmarque a caixa de seleção **[!UICONTROL Use config settings]** e escolha uma das seguintes opções:

     | Opção | Descrição |
     |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Payment Methods` | (Padrão) Habilita todos os [métodos de pagamento definidos como padrão](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods) para ordens B2B. |
     | `All Enabled Payment Methods` | Disponibiliza todos os [métodos de pagamento habilitados](../configuration-reference/sales/payment-methods.md) para contas de clientes associadas à conta da empresa. |
     | `Selected Payment Methods` | Permite selecionar os métodos de pagamento disponíveis para contas de clientes associadas à conta da empresa. Para selecionar vários métodos de pagamento, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada opção. |

     {style="table-layout:auto"}

   * Para alterar os **[!UICONTROL Applicable Shipping Methods]** que estão disponíveis para a empresa, desmarque a caixa de seleção **[!UICONTROL Use config settings]** e escolha uma das seguintes opções:

     | Opção | Descrição |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | (Padrão) Habilita todos os [métodos de envio definidos como padrão](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) para pedidos B2B. |
     | `All Enabled Shipping Methods` | Disponibiliza todos os [métodos de envio habilitados](../configuration-reference/sales/delivery-methods.md) para contas de clientes associadas à conta da empresa. |
     | `Selected Shipping Methods` | Permite selecionar os métodos de entrega disponíveis para contas de clientes associadas à conta da empresa. Para selecionar vários métodos de envio, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada opção. |

     {style="table-layout:auto"}

1. Quando terminar, selecione **[!UICONTROL Save]**.

   Quando a solicitação para criar uma conta da empresa é aprovada pelo comerciante, uma notificação por email é enviada para o endereço de email do administrador da empresa.

   Quando a senha é definida, o administrador da empresa pode [entrar](../customers/customer-sign-in.md) na conta.

## Após a criação da conta

Depois que uma conta de empresa é criada, o seguinte processo ocorre:

### &#x200B;1. Workflow de Aprovação

* **Status pendente**—Novas contas aguardam revisão do administrador
* **Processo de Revisão** — Os administradores de armazenamento verificam as informações comerciais e aprovam/rejeitam solicitações
* **Atualizações de Status** — As empresas recebem notificações por email sobre alterações no status de aprovação

### &#x200B;2. Ativação da conta

* **Email de Boas-vindas**—Os administradores de empresas aprovados recebem instruções de configuração
* **Configuração de Senha** — Os administradores criam senhas seguras para acesso à conta
* **Logon Inicial** — Acesso pela primeira vez ao painel e aos recursos da empresa

### &#x200B;3. Próximas etapas para administradores de empresas

Após a ativação, os administradores da empresa devem:

* **[Configurar Estrutura da Empresa](account-company-structure.md)**—Configurar departamentos e hierarquia de usuários
* **[Gerenciar Usuários da Empresa](account-company-users.md)** — Adicione funcionários e atribua funções
* **[Configurar Ordens de Compra](purchase-order-flow.md)** — Configurar fluxos de trabalho de aprovação, se necessário
* **[Revisar Configurações de Crédito](credit-company.md)**—Compreender e gerenciar o crédito da empresa (se habilitado)

## Problemas comuns e solução de problemas

### Problemas de criação de conta

**Falha ao enviar o formulário de registro**

* Verifique se todos os campos obrigatórios foram preenchidos corretamente
* Verificar se os endereços de email são válidos e exclusivos
* Verifique se os recursos B2B estão habilitados e se o registro da empresa é permitido
* Limpe o cache do navegador e tente novamente

**O Nome Da Empresa Já Existe**

* Escolha um nome de empresa exclusivo
* Entre em contato com o administrador se você achar que é um erro
* Considere adicionar o identificador de local ou de unidade de negócios

**Problemas de endereço de email**

* Use endereços de email comerciais em vez de pessoais
* Garantir que o email do administrador da empresa esteja acessível
* Verifique se o domínio não está bloqueado por filtros de email

### Problemas de aprovação e ativação

**Email de aprovação não recebido**

* Verificar pastas de spam/lixo eletrônico
* Verifique se o endereço de email foi inserido corretamente durante o registro
* Entre em contato com o administrador da loja para verificar manualmente o status de aprovação
* Aguarde de 24 a 48 horas para processamento durante dias úteis

**Não É Possível Definir A Senha Após A Aprovação**

* Usar o link exato fornecido no email de aprovação
* Verifique se o link de ativação expirou
* Solicitar um novo email de ativação ao administrador

**Problemas de acesso após a ativação**

* Verifique se você está fazendo logon por meio do portal correto de contas da empresa
* Verifique se o status da sua conta é &quot;Ativo&quot;
* Verifique se você está usando as credenciais de administrador da empresa
* Entre em contato com o suporte se as permissões parecerem incorretas

## Práticas recomendadas de segurança

Ao criar e gerenciar contas da empresa:

* **Usar Senhas de Alta Segurança** — Exigir senhas complexas para administradores da empresa
* **Verificar Informações Comerciais** — Valide os detalhes da empresa durante o processo de aprovação
* **Monitorar Atividade da Conta**—Examine regularmente o acesso e as permissões dos usuários da empresa
* **Proteger Dados Confidenciais** — Garantir a segurança adequada das informações financeiras e de crédito

## Referência da interface de usuário da conta da empresa

### Barra de botões

| Botão | Descrição |
|---------------------------|------------------------------------------------------------------|
| [!UICONTROL Back] | Retorna à página Empresas sem salvar as alterações. |
| [!UICONTROL Reset] | Restaura os valores originais em todos os campos com alterações não salvas. |
| [!UICONTROL Save] | Salva as alterações na empresa e mantém o perfil aberto. |
| [!UICONTROL Save & Close] | Salva as alterações na empresa e fecha o perfil. |

{style="table-layout:auto"}

### Descrições dos campos

| Campo | Descrição |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | O nome da empresa é inserido quando a conta da empresa é criada pela primeira vez e pode ser uma versão reduzida do nome legal completo. |
| [!UICONTROL Status] | (Somente administrador) Indica o estado atual da conta da empresa. Opções: <br/>**[!UICONTROL Active]**- A conta da empresa foi aprovada pelo administrador de armazenamento. O administrador da empresa e os membros associados podem fazer logon na conta da loja e fazer compras.<br/>**[!UICONTROL Pending Approval]** - Uma solicitação para abrir uma conta da empresa foi enviada, mas ainda não foi aprovada pelo administrador de armazenamento. <br/>**[!UICONTROL Rejected]**- Uma solicitação para abrir uma conta da empresa foi enviada, mas não foi aprovada pelo administrador de armazenamento. As credenciais de logon iniciais usadas para enviar a solicitação estão bloqueadas.<br/>**&#x200B; Bloqueado &#x200B;**- Os membros da empresa podem fazer logon e acessar o catálogo, mas não podem fazer compras. O administrador de armazenamento pode bloquear uma conta da empresa que não esteja em boa posição. O bloqueio na conta pode ser removido pelo administrador de armazenamento a qualquer momento. |
| [!UICONTROL Company Email] | O endereço de email associado à conta da empresa. |
| [!UICONTROL Sales Representative] | (Somente administrador) O usuário administrador que é o contato principal da conta da empresa. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Campo | Descrição |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | O nome legal completo da empresa. |
| [!UICONTROL VAT / TAX ID] | O número de [imposto sobre valor agregado](../stores-purchase/vat.md) atribuído à empresa por algumas jurisdições para fins de relatório de imposto. Para configurar a ID de IVA/IMPOSTO do cliente para aparecer na vitrine, consulte [Criar Novas Opções de Conta](../configuration-reference/customers/customer-configuration.md). <br/> **_Observação:_** O administrador da empresa e outros usuários da empresa não têm seus próprios números de identificação de IVA/IMPOSTO separados em suas contas de cliente. |
| [!UICONTROL Reseller ID] | O número de revenda atribuído à empresa para fins de relatório de imposto. |
| [!UICONTROL Comment] | (Somente administrador) Essas notas sobre a conta da empresa são para referência e visíveis somente do administrador. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

| Campo | Descrição |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | O número de ID da empresa. |
| [!UICONTROL Company Name] | O nome completo da empresa. <br/>Um `current company indicator` aparece na linha da empresa que está sendo editada. |
| [!UICONTROL Company Email] | O endereço de email associado à conta da empresa. |
| [!UICONTROL Phone Number] | O número de telefone principal da empresa. |
| [!UICONTROL Country] | O país onde a empresa está registrada para realizar negócios. |
| [!UICONTROL State/Province] | O estado ou província onde a empresa está registrada para realizar negócios. |
| [!UICONTROL City] | A cidade onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Group/Shared Catalog] | (Somente Administrador) Mostra o [grupo de clientes](../customers/customer-groups.md) ou o [catálogo compartilhado](catalog-shared.md) atribuído à empresa. |
| [!UICONTROL Company Admin] | O nome completo do administrador da empresa. |
| [!UICONTROL Action] | A lista de ações possíveis para essa linha de empresa. |

{style="table-layout:auto"}

#### [!UICONTROL Legal Address]

| Campo | Descrição |
|------------------------------|-----------------------------------------------------------------------------|
| [!UICONTROL Street Address] | O endereço onde a empresa está registrada para realizar negócios. |
| [!UICONTROL City] | A cidade onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Country] | O país onde a empresa está registrada para realizar negócios. |
| [!UICONTROL State/Province] | O estado ou província onde a empresa está registrada para realizar negócios. |
| [!UICONTROL ZIP/Postal Code] | O CEP ou código postal onde a empresa está registrada para realizar negócios. |
| [!UICONTROL Phone Number] | O número de telefone principal da empresa. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Campo | Descrição |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Determina o site ao qual o administrador da empresa pertence. |
| [!UICONTROL Job Title] | O título do administrador da empresa que gerencia a conta da empresa. |
| [!UICONTROL Work Phone Number] | O número de telefone do administrador da empresa que gerencia a conta da empresa. |
| [!UICONTROL Email] | O endereço de email do administrador da empresa pode ser igual ao endereço de email da empresa. Se você inserir um endereço de email diferente, o sistema criará uma conta individual separada para o administrador da empresa, além da conta da empresa. |
| [!UICONTROL Prefix] | Se aplicável, o prefixo associado ao nome do administrador da empresa (como `Mr.`, `Ms.`, `Mrs.` ou `Dr.`). Dependendo da configuração, o campo de entrada pode ser um campo de texto ou lista. |
| [!UICONTROL First Name] | O nome do administrador da empresa. |
| [!UICONTROL Middle Name/Initial] | O nome do meio ou a inicial do administrador da empresa. |
| [!UICONTROL Last Name] | O sobrenome do administrador da empresa. |
| [!UICONTROL Suffix] | Se aplicável, o sufixo associado ao nome do administrador da empresa (como `Jr.`, `Sr.` ou `III.`). Dependendo da configuração, o campo de entrada pode ser um campo de texto ou lista. |
| [!UICONTROL Gender] | O sexo do administrador da empresa. Opções: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | A exibição de loja da qual o sistema envia o email de boas-vindas. |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Campo | Descrição |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | (Somente administrador) A moeda aceita pela loja para compras em crédito da empresa. |
| [!UICONTROL Credit Limit] | (Somente Administrador) O limite de crédito estendido para a conta da empresa. |
| [!UICONTROL Allow to Exceed Credit Limit] | (Somente Administrador) Indica se a empresa tem permissão para exceder o limite de crédito. Opções: `Yes` / `No` |
| [!UICONTROL Reason for Change] | (Somente administrador) Uma nota que explica por que a empresa tem ou não permissão para exceder o limite de crédito. Este campo só estará ativo se a permissão para exceder o limite de crédito for alterada. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

Você pode definir configurações avançadas para empresas individuais. Se você criar uma hierarquia de empresa, poderá simplificar as configurações de configuração definindo as configurações para a empresa principal e aplicando essas configurações a todas as empresas secundárias ou às empresas secundárias selecionadas, em vez de configurar cada empresa secundária individualmente. Para obter mais informações, consulte [Gerenciar a Hierarquia da Empresa](manage-company-hierarchy.md).

| Campo | Descrição |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | (Somente Administrador) Mostra o [grupo de clientes](../customers/customer-groups.md) ou o [catálogo compartilhado](catalog-shared.md) atribuído à empresa. |
| [!UICONTROL Allow Quotes] | (Somente Administrador) Determina se os membros da empresa podem preparar e enviar cotações negociáveis em nome da empresa. |
| [!UICONTROL Enable Purchase Orders] | (Somente Administrador) Determina se os membros da empresa podem enviar pedidos como [ordens de compra](account-dashboard-my-purchase-orders.md) em nome da empresa. |
| Métodos de pagamento aplicáveis | (Somente Administrador) Indica os métodos de pagamento disponíveis para compras da empresa. Opções: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | (Somente Administrador) Fica ativo se você ativar métodos de pagamento específicos. Para disponibilizar vários métodos de pagamento para a conta da empresa, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada opção. |
| [!UICONTROL Applicable Shipping Methods] | (Somente Administrador) Indica os métodos de envio disponíveis para compras da empresa. Opções: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | (Somente administrador) Fica ativo se você ativar métodos de envio específicos. Para disponibilizar vários métodos de envio para a conta da empresa, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e selecione cada opção. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Habilitar Recursos B2B](enable-basic-features.md)—Configurar funcionalidade B2B fundamental
>* [Estrutura de Conta de Empresa](account-company-structure.md)—Organize usuários e departamentos na loja
>* [Gerenciar Usuários da Empresa](account-company-users.md)—Adicione e configure contas de funcionários na loja
>* [Função de Administrador da Empresa](account-company-admin.md)—Entenda as responsabilidades do administrador
>* [Gerenciar Empresas](manage-companies.md)—Visão geral administrativa do gerenciamento da empresa
>* [Gerenciamento de Crédito da Empresa](credit-company.md)—Configure e gerencie o crédito da empresa com o Administrador
>* [Fluxo de Trabalho da Ordem de Compra](purchase-order-flow.md) — Configurar processos de aprovação do Administrador
>* [Funções e Permissões da Empresa](account-company-roles-permissions.md)—Controlar níveis de acesso de usuário do Administrador
>* [Referência de Configuração B2B](../configuration-reference/general/b2b-features.md)—Configurações detalhadas do sistema
