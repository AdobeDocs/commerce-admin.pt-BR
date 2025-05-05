---
title: Criar uma conta de cliente individual
description: Os visitantes podem criar facilmente uma conta de cliente individual para gerenciar suas compras.
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Criar uma conta de cliente individual

Os visitantes da sua loja podem abrir uma conta para gerenciar suas compras e atividades. Os clientes geralmente criam suas próprias contas na loja. No entanto, você também pode criar contas de clientes diretamente do Administrador, o que é útil para ajudar os clientes por telefone.

As instruções a seguir representam a configuração padrão da conta do cliente. Para alterar a seleção e o comportamento de alguns campos no formulário, consulte [Configurando Contas de Clientes](../customers/customer-account-scope.md).

Como administrador de loja, você também pode definir as [novas opções de conta](../customers/account-options-new.md) para enviar um email de confirmação para novos clientes registrados, o que ajuda a garantir que as contas registradas sejam válidas.

>[!NOTE]
>
>A partir da versão 2.4.7, os clientes devem inserir novamente seu email e senha para fazer logon em sua conta após a confirmação por email, independentemente do navegador.

## Criar conta da loja

Um cliente da loja cria uma conta na loja.

1. Na vitrine, clique em **[!UICONTROL Create an Account]** no canto superior direito do cabeçalho.

   ![Criar uma Conta](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. Em **[!UICONTROL Personal Information]**, insere seus **[!UICONTROL First Name]** e **[!UICONTROL Last Name]**.

   ![Informações pessoais](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. Se quiser adicionar seu nome e endereço de email à lista de assinantes do boletim informativo, o cliente marcará a caixa de seleção **[!UICONTROL Sign Up for Newsletter]**.

   >[!INFO]
   >
   > Essa opção será exibida mesmo se a loja não publicar um boletim informativo.

1. Se ele quiser que a equipe de suporte da loja [veja o que vê](../customers/login-as-customer.md) e forneça assistência remota, o cliente marcará a caixa de seleção **[!UICONTROL Allow remote shopping assistance]**.

1. Em **[!UICONTROL Sign-in Information]**, digite o endereço **[!UICONTROL Email]**.

   >[!INFO]
   >
   > Este endereço de email se torna parte de suas credenciais de logon e não pode ser associado a nenhuma outra conta de cliente.

   ![Informações de Entrada](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. Insira um **[!UICONTROL Password]** que inclua três dos seguintes tipos de informações:

   - Caracteres em minúsculas
   - Caracteres em maiúsculas
   - Números
   - Caracteres especiais

   Após pressionarem **[!UICONTROL Enter]**, a força da senha é avaliada e aparece abaixo do campo. Se a senha for considerada _Fraca_, tente outra até que seja avaliada como _Forte_.

   ![Uma senha forte é recomendada](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. Em seguida, o cliente o insere novamente em **[!UICONTROL Confirm Password]**.

1. Se necessário, clique em **[!UICONTROL Show Password]** para exibir a senha inserida.

1. Quando terminar, clique em **Criar uma Conta**.

O cliente pode então usar seu endereço de email e senha para [entrar](../customers/customer-sign-in.md) em sua conta e preencher as informações de endereço.

## Criar uma conta do Administrador

Como comerciante, você pode criar uma conta de cliente no Administrador.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Clique em **[!UICONTROL Add New Customer]**.

### Etapa 1: Preencher as informações da conta

![Informações sobre o Cliente](assets/new-information.png){width="700" zoomable="yes"}

1. Na seção **[!UICONTROL Account Information]**, faça o seguinte:

   - Para uma instalação multissite, defina **[!UICONTROL Associate to Website]** para o site onde a conta do cliente se aplica.
   - Se aplicável, atribua o cliente a um **[!UICONTROL Customer Group]** diferente.
   - Se você estiver usando a [Validação de ID de IVA](../stores-purchase/vat.md) e quiser **[!UICONTROL Disable Automatic Group Change Based on VAT ID]**, marque a caixa de seleção.

1. Preencha os campos obrigatórios:

   - **[!UICONTROL First Name]**
   - **[!UICONTROL Last Name]**
   - **[!UICONTROL Email]**

1. Preencha os campos opcionais conforme necessário:

   - **[!UICONTROL Name Prefix]**
   - **[!UICONTROL Middle Name/Initial]**
   - **[!UICONTROL Name Suffix]**
   - **[!UICONTROL Date of Birth]**
   - **[!UICONTROL Tax/VAT Number]**
   - **[!UICONTROL Gender]**

   >[!WARNING]
   >
   >De acordo com as práticas recomendadas atuais de segurança e privacidade, esteja ciente de possíveis riscos legais e de segurança associados ao armazenamento da data de nascimento completa do cliente (mês, dia, ano) com outros identificadores pessoais. É recomendável limitar o armazenamento das datas de nascimento completas dos clientes e sugerir que você use o ano de nascimento do cliente como alternativa.

1. Defina **[!UICONTROL Send Welcome Email From]** para o modo de exibição de armazenamento a partir do qual o email de _Boas-vindas_ será enviado.

   >[!INFO]
   >
   > Se o armazenamento tiver exibições para diferentes [idiomas](../stores-purchase/store-localize.md), essa configuração determinará o idioma do email de boas-vindas.

1. Clique em **[!UICONTROL Save and Continue Edit]** na parte superior da página.

   >[!INFO]
   >
   >Depois que a conta do cliente é salva, o conjunto completo de opções é exibido no painel esquerdo e no menu na parte superior da página. A guia _[!UICONTROL Customer View]_&#x200B;exibe um resumo da conta.

   ![Visualização de Cliente](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### Etapa 2: completar as informações de endereço

1. No painel esquerdo, escolha **[!UICONTROL Addresses]** e clique em **[!UICONTROL Add New Addresses]**.

1. Se o mesmo endereço for usado para faturamento e envio, alterne ambas as opções.

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![Adicionar informações de endereço do cliente](assets/information-addresses.png){width="600" zoomable="yes"}

1. Role para baixo e preencha os campos de endereço necessários na segunda coluna.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. Digite o **[!UICONTROL Phone Number]** para este endereço.

1. Se aplicável, insira o **[!UICONTROL VAT Number]** associado ao cliente.

1. Se este endereço for o único necessário para a conta, clique em **[!UICONTROL Save]**.

   Caso contrário, clique em **[!UICONTROL Save and Continue Edit]** e repita as etapas anteriores para adicionar mais endereços.

   O novo endereço é exibido na página [!UICONTROL Addresses] com os endereços _[!UICONTROL Default Billing]_&#x200B;e_[!UICONTROL Default Shipping]_ selecionados acima da lista completa.

   ![Exibição de endereços](assets/address-list.png){width="600" zoomable="yes"}

### Etapa 3: redefinir a senha

Inicialmente, as contas de cliente criadas com base no Administrador não têm senhas atribuídas.

1. Localize a nova conta de cliente na grade.

1. Clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Na barra de menus na parte superior da página, clique em **[!UICONTROL Reset Password]**.

1. Uma notificação é enviada ao proprietário da conta, com instruções para definir a senha.

## Barra de botões

Botões adicionais ficam disponíveis quando o perfil é salvo pela primeira vez. Para saber mais, consulte [Atualizar um perfil de cliente](../customers/update-account.md).

| Botão | Descrição |
|--- |--- |
| **[!UICONTROL Back]** | Retorna à página _[!UICONTROL Customers]_&#x200B;sem salvar as alterações. |
| **[!UICONTROL Delete Customer]** | Exclui o cliente atual. Os pedidos concluídos associados ao cliente não são removidos. |
| **[!UICONTROL Reset]** | Redefine quaisquer alterações não salvas no formulário do cliente para seus valores anteriores. |
| **[!UICONTROL Create Order]** | Cria um pedido para o cliente. |
| **[!UICONTROL Reset Password]** | Envia por email um link de [redefinição de senha](../customers/password-reset.md) para o cliente. |
| **[!UICONTROL Force Sign-in]** | Revoga os tokens de acesso OAuth associados à conta do cliente. Esta função pode ser usada somente com contas de clientes que receberam tokens OAuth como parte de uma [integração](../systems/integrations.md) da API da Web. Para saber mais, consulte [autenticação baseada em OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) na documentação do desenvolvedor. |
| **[!UICONTROL Manage Shopping Cart]** | Permite que o administrador gerencie o carrinho de compras do cliente. |
| **[!UICONTROL Save and Continue Edit]** | Salva as alterações e mantém o perfil do cliente aberto. |
| **[!UICONTROL Save Customer]** | Salva alterações e fecha o perfil do cliente. |

{style="table-layout:auto"}

## Descrições dos campos

### [!UICONTROL Account Information]

| Campo | Descrição |
|--- |--- |
| **[!UICONTROL Associate to Website]** | Identifica o site associado à conta do cliente. |
| **[!UICONTROL Group]** | Identifica o [grupo de clientes](../customers/customer-groups.md) do qual o cliente é membro. Se aplicável, marque a caixa de seleção para desativar a alteração automática do grupo com base no IVA. |
| **[!UICONTROL Name Prefix]** | Se usado, o prefixo associado ao nome do cliente (como Sr., Sra. ou Dr.). Os valores de prefixo são determinados pela [configuração](../configuration-reference/customers/customer-configuration.md). Dependendo da configuração, o controle de entrada pode ser um campo de texto ou uma lista de opções. |
| **[!UICONTROL First Name]** | O nome do cliente. |
| **[!UICONTROL Middle Name / Initial]** | O nome do meio ou a inicial do cliente. Este campo é incluído somente se especificado no tópico [configuração](../configuration-reference/customers/customer-configuration.md). |
| **[!UICONTROL Last Name]** | O sobrenome do cliente. |
| **[!UICONTROL Name Suffix]** | Se usado, o sufixo associado ao nome do cliente (como Jr., Sr. ou III). Os valores de sufixo são determinados pela [configuração](../configuration-reference/customers/customer-configuration.md). Dependendo da configuração, o controle de entrada pode ser um campo de texto ou uma lista suspensa de opções. |
| **[!UICONTROL Email]** | O endereço de email do cliente. |
| **[!UICONTROL Date of Birth]** | A data de nascimento do cliente. A data de nascimento é incluída se especificada no tópico [configuração](../configuration-reference/customers/customer-configuration.md). <br><br>Ao manter as práticas recomendadas atuais de segurança e privacidade, esteja ciente de todos os possíveis riscos legais e de segurança associados ao armazenamento da data de nascimento completa do cliente (mês, dia, ano) com outros identificadores pessoais. É recomendável limitar o armazenamento das datas de nascimento completas dos clientes e sugerir o uso do ano de nascimento do cliente como alternativa. |
| **[!UICONTROL Tax / VAT Number]** | O número do Imposto ou do Imposto sobre Valor Agregado do cliente, se aplicável. |
| **[!UICONTROL Gender]** | Identifica o sexo do cliente. O sexo é incluído se especificado na [configuração](../configuration-reference/customers/customer-configuration.md). Opções: `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | Se você tiver várias exibições de loja, essa configuração identifica a exibição de loja da qual a mensagem de boas-vindas é enviada. Se as exibições de loja forem usadas para idiomas diferentes, essa configuração determinará o idioma do email de boas-vindas. |

### [!UICONTROL Addresses]

| Campo | Descrição |
|--- |--- |
| **[!UICONTROL New Addresses]** | Identifica o tipo do novo endereço. Opções: `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | Exibe outra seção Novo Endereço para identificar o tipo do endereço a ser inserido. |
| **[!UICONTROL Company]** | O nome da empresa, se aplicável para este endereço. |
| **[!UICONTROL Street Address]** | O endereço do cliente. Uma segunda linha do endereço está disponível se especificada no tópico [configuração](../configuration-reference/customers/customer-configuration.md). |
| **[!UICONTROL City]** | A cidade onde o endereço do cliente está localizado. |
| **[!UICONTROL Country]** | O país onde o endereço do cliente está localizado. |
| **[!UICONTROL State/Province]** | O estado ou província onde o endereço do cliente está localizado. |
| **[!UICONTROL Zip/Postal Code]** | O CEP onde o endereço do cliente está localizado. |
| **[!UICONTROL Phone Number]** | O número de telefone do cliente associado ao endereço. |
| **[!UICONTROL VAT Number]** | Se aplicável, o número de imposto sobre o valor agregado que se aplica ao cliente neste endereço. |
