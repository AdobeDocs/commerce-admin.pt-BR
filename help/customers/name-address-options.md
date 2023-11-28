---
title: Opções de nome e endereço do cliente
description: As opções de nome e endereço do cliente determinam quais campos são incluídos nos formulários de nome e endereço.
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# Opções de nome e endereço do cliente

A variável _Opções de nome e endereço_ determinam quais campos são incluídos nos formulários de nome e endereço quando os clientes criam um [account](../customers/account-create.md) com sua loja.

![Formulário de inscrição da conta do cliente](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

As etapas para configurar as opções de nome e endereço são diferentes para Adobe Commerce e Magento Open Source.

## Configurar opções de nome e endereço para o Adobe Commerce

Você pode configurar as opções de nome e endereço que são apresentadas aos clientes na loja quando eles criam sua conta.

### Etapa 1: definir o escopo da configuração

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Customer Configuration]**.

1. Expanda a **[!UICONTROL Name and Address Options]** seção.

   >[!INFO]
   >
   >Observe que o escopo das opções de nome e endereço se aplica no `website` nível.

1. Role para cima até a parte superior da página e defina o escopo da configuração como um dos seguintes:

   - `Default Config`
   - `Main Website` (ou local específico para instalações em vários locais)

   >[!INFO]
   >
   >A variável _[!UICONTROL Name and Address Options]_não aparece quando o escopo é definido como `Default Store View`.

   ![Escopo da configuração](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### Etapa 2: configurar as opções de nome e endereço

1. Retorne para a [!UICONTROL _Opções de nome e endereço_] seção da página Configuração do cliente.

   >[!INFO]
   >
   > Se você não estiver usando o `Default config` definição de escopo, você deve limpar a variável `Use Default` para cada campo antes de alterar o valor.

   ![Opções de nome e endereço](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Prefix Dropdown Options]**, insira cada prefixo que deseja exibir na lista, separado por ponto e vírgula.

   >[!IMPORTANT]
   >
   >Coloque um ponto e vírgula antes do primeiro valor para exibir um valor em branco na parte superior da lista.

1. Para **[!UICONTROL Suffix Dropdown Options]**, insira cada sufixo que você deseja que apareça na lista, separado por ponto e vírgula.

1. Para incluir os seguintes campos em formulários de clientes, defina o valor de cada para `Optional` ou `Required`, conforme necessário.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Etapa 3: Salvar e atualizar

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Na mensagem na parte superior da página, clique em **[!UICONTROL Cache Management]** e [atualizar](../systems/cache-management.md) cada cache inválido.

## Configurar opções de nome e endereço para o Magento Open Source

Configure as opções de nome e endereço que são apresentadas aos clientes na loja quando eles criam sua conta.

![Formulário de inscrição da conta do cliente](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### Etapa 1: definir o escopo da configuração

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Customer Configuration]**.

1. Expanda a **[!UICONTROL Name and Address Options]** seção.

   >[!IMPORTANT]
   >
   > Observe que o escopo das opções de nome e endereço se aplica no `website` nível.

   ![Opções de nome e endereço](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. Role para trás até a parte superior da página e defina o escopo da configuração como um dos seguintes:

   - `Default Config`
   - `Main Website` (ou local específico para instalações em vários locais)

   >[!NOTE]
   >
   >A variável _Opções de nome e endereço_ não aparece quando o escopo é definido como `Default Store View`.

   ![Escopo da configuração](assets/configuration-scope.png){width="600" zoomable="yes"}

### Etapa 2: configurar as opções de nome e endereço

1. Retorne para a [!UICONTROL _Opções de nome e endereço_] seção da página Configuração do cliente.

   >[!INFO]
   >
   >Se você não estiver usando o `Default config` definição de escopo, você deve limpar a variável `Use Default` para cada campo antes de alterar o valor.

1. Para **Número de linhas em um endereço**, digite um número de 1 a 4.

   >[!WARNING]
   >
   >Por padrão, o endereço é de três linhas.

1. Para incluir um prefixo (como Sr. ou Sra.) como parte do nome, defina **Mostrar prefixo** para `Yes`.

   ![Prefixo no formulário de inscrição do cliente](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Para **Opções da lista suspensa Prefixo**, insira cada prefixo que deseja exibir na lista, separado por ponto e vírgula. Você pode colocar um ponto e vírgula antes do primeiro valor para exibir um valor em branco na parte superior da lista.

1. Para incluir um campo opcional para o nome do meio ou a inicial do cliente, defina **[!UICONTROL Show Middle Name (initial)]** para `Yes`.

1. Para incluir um sufixo (como Jr. ou Sr.) após o nome do cliente, defina **[!UICONTROL Show Suffix]** a um dos seguintes:

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >Para **Opções da lista suspensa Sufixo**, insira cada sufixo que você deseja que apareça na lista, separado por ponto e vírgula. Você pode colocar um ponto e vírgula antes do primeiro valor para exibir um valor em branco na parte superior da lista.

1. Para incluir a data de nascimento, defina **[!UICONTROL Show Date of Birth]** a um dos seguintes:

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >De acordo com as práticas recomendadas atuais de segurança e privacidade, esteja ciente de possíveis riscos legais e de segurança associados ao armazenamento da data de nascimento completa do cliente (mês, dia, ano) com outros identificadores pessoais. É recomendável limitar o armazenamento das datas de nascimento completas dos clientes e sugerir o uso do ano de nascimento do cliente como alternativa.

   Os clientes podem usar o ícone Calendário depois do campo para escolher a data de nascimento de um calendário pop-up.

   ![Data de nascimento no formulário de inscrição do cliente](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. Para permitir que os clientes informem seus impostos ou [IVA](../stores-purchase/vat.md) número, definir **[!UICONTROL Show Tax/VAT Number]** a um dos seguintes:

   - `Optional`
   - `Required`

1. Para incluir um campo para gênero no formulário do cliente, defina **[!UICONTROL Show Gender]** a um dos seguintes:

   - `Optional`
   - `Required`

   ![Opções de gênero no formulário de inscrição do cliente](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. Para incluir os seguintes campos em formulários de clientes, defina o valor de cada para `Optional` ou `Required`, conforme necessário.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Etapa 3: Salvar e atualizar

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Na mensagem na parte superior da página, clique em **[!UICONTROL Cache Management]** e [atualizar](../systems/cache-management.md) cada cache inválido.
