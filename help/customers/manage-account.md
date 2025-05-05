---
title: Gerenciar contas de clientes
description: Use a grade [!UICONTROL Customers] para localizar qualquer conta de cliente e acessar informações de contas de clientes individuais.
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Gerenciar contas de clientes

Use a grade _[!UICONTROL Customers]_&#x200B;para localizar qualquer conta de cliente. Você pode usar os [controles do local de trabalho](../getting-started/admin-workspace.md) padrão para filtrar a lista, alterar o [layout da coluna](../getting-started/admin-grid-controls.md), salvar exibições e exportar dados. O [Controle de ações](../getting-started/admin-actions-control.md) acima da grade pode ser usado para aplicar uma operação a vários registros de clientes.

![Todos os Clientes](assets/customers-all-customers.png){width="700" zoomable="yes"}

Consulte [Atualizar perfil de cliente](update-account.md) para obter informações sobre como fazer atualizações manuais em uma conta de cliente.

## Ações da conta do cliente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Na primeira coluna da grade, marque a caixa de seleção de cada registro que deseja atualizar.

1. Siga as instruções para a ação que deseja aplicar.

   >[!INFO]
   >
   >As ações a seguir podem ser aplicadas a um ou a vários registros.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Assinar informativo

Em configurações multilojas e multissites com um [escopo de conta de cliente](../customers/customer-account-scope.md) global, uma conta de cliente pode assinar boletins informativos para vários sites ou lojas. Se você aplicar a ação _Assinar_ a uma conta de cliente, ela ativará a assinatura do boletim informativo somente para a exibição padrão de site/loja.

* Defina o controle **[!UICONTROL Actions]** como `Subscribe to newsletter`.

Consulte [Gerenciar assinantes](../merchandising-promotions/newsletter-subscribers.md) para obter mais informações sobre como gerenciar assinaturas de boletim informativo para um cliente.

### Cancelar assinatura no informativo

Em configurações de vários sites e vários sites com um [escopo de conta de cliente](customer-account-scope.md) global, uma conta de cliente pode assinar boletins informativos para vários sites/lojas. Se você aplicar a ação _Cancelar assinatura_ a uma conta de cliente, todas as assinaturas ativas terão as assinaturas canceladas.

1. Defina o controle **[!UICONTROL Actions]** como `Unsubscribe to newsletter`.

1. Quando for solicitada a confirmação, clique em **OK**.

### Atribuir um grupo de clientes

1. Defina o controle **[!UICONTROL Actions]** como `Assign a customer group`.

1. Escolha o grupo de clientes ao qual todos os registros de cliente selecionados devem ser atribuídos.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

### Excluir contas de cliente

As contas de cliente excluídas não podem ser restauradas. As informações sobre a atividade do cliente e as transações são retidas no sistema.

1. Defina o controle **[!UICONTROL Actions]** como `Delete`.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

## Exportar contas de clientes

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. No Menu de Cabeçalho de Tabela, clique em **[!UICONTROL Export]** e selecione o formato desejado:

   * CSV
   * XML do Excel

1. Clique em **[!UICONTROL OK]**.

   O arquivo vai para a pasta de downloads padrão.

A instrução acima exporta todas as contas de clientes. Se desejar exportar um conjunto limitado, marque as caixas de seleção das contas que deseja exportar ou use filtros no painel de controle para selecionar uma variedade de contas de cliente.

## Ações/controles

| Opção | Descrição |
|--- |--- |
| **[!UICONTROL Delete]** | Exclui as contas de cliente selecionadas. Se a conta do cliente pertencer a um administrador de empresa para um armazenamento B2B, outro usuário da empresa deverá ser atribuído como administrador antes que a conta do cliente possa ser excluída. |
| **[!UICONTROL Subscribe to Newsletter]** | Inscreve os clientes selecionados no informativo. |
| **[!UICONTROL Unsubscribe from Newsletter]** | Cancela a assinatura de clientes selecionados no informativo. |
| **[!UICONTROL Assign a Customer Group]** | Atribui clientes selecionados a um grupo de clientes. |
| **[!UICONTROL Edit]** | Permite que alguns valores de um único registro de cliente selecionado sejam editados na grade. Por padrão, os seguintes valores estão disponíveis para edição rápida: Email, Grupo, Telefone, CEP, Site, Número IVA de Imposto e Gênero. |

{style="table-layout:auto"}

## Colunas

| Coluna | Descrição |
|--- |--- |
| **[!UICONTROL Select]** | Gerencia as seleções da caixa de seleção dos registros do cliente para a aplicação de uma ação. Você também pode usar o controle de seleção no cabeçalho da coluna para marcar/desmarcar tudo. |
| **[!UICONTROL ID]** | Um identificador numérico exclusivo que é atribuído quando a conta do cliente é criada. |
| **[!UICONTROL Name]** | O nome e sobrenome do cliente. |
| **[!UICONTROL Email]** | O endereço de email do cliente. |
| **[!UICONTROL Group]** | O grupo de clientes ao qual o cliente está atribuído. |
| **[!UICONTROL Phone]** | O telefone do cliente. |
| **[!UICONTROL ZIP]** | O CEP do cliente. |
| **[!UICONTROL Country]** | O país onde o cliente está localizado. |
| **[!UICONTROL State/Province]** | O estado ou província onde o cliente está localizado. |
| **[!UICONTROL Customer Since]** | A data e a hora em que a conta do cliente foi criada. |
| **[!UICONTROL Web Site]** | O site na hierarquia da loja à qual a conta do cliente está associada. |
| **[!UICONTROL Confirmed Email]** | Indica se um email de confirmação é necessário. |
| **[!UICONTROL Account Created In]** | Indica a exibição da loja a partir da qual a conta do cliente foi criada. |
| **[!UICONTROL Date of Birth]** | A data de nascimento do cliente. De acordo com as práticas recomendadas atuais de segurança e privacidade, esteja ciente de possíveis riscos legais e de segurança associados ao armazenamento da data de nascimento completa do cliente (mês, dia, ano) com outros identificadores pessoais. É recomendável limitar o armazenamento das datas de nascimento completas dos clientes e sugerir o uso do ano de nascimento do cliente como alternativa. |
| **[!UICONTROL Tax / VAT Number]** | Se aplicável, o número do imposto ou o número do [imposto sobre valor agregado](../stores-purchase/vat.md) atribuído ao cliente. <br/><br/> Este campo não é o mesmo que o número IVA. |
| **[!UICONTROL Gender]** | O sexo do cliente. |
| **[!UICONTROL Action]** | Editar - abre a conta da empresa no modo de edição. |

{style="table-layout:auto"}

### Colunas adicionais

Estas colunas estão disponíveis ao alterar o [layout da coluna](../getting-started/admin-grid-controls.md) da grade.

| Coluna | Descrição |
|--- |--- |
| **[!UICONTROL Company]** | O nome da empresa do cliente. |
| **[!UICONTROL Street Address]** | O endereço do cliente. |
| **[!UICONTROL City]** | A cidade onde o cliente está localizado. |
| **[!UICONTROL Fax]** | O número de fax do cliente, se aplicável. |
| **[!UICONTROL Billing Firstname]** | O nome no endereço de cobrança do cliente. |
| **[!UICONTROL Billing Lastname]** | O sobrenome no endereço de cobrança do cliente. |
| **[!UICONTROL Billing Address]** | O endereço para onde as informações de cobrança devem ser enviadas. |
| **[!UICONTROL Shipping Address]** | O endereço para onde os pedidos devem ser enviados. |
| **[!UICONTROL VAT Number]** | O número de imposto sobre valor agregado associado ao endereço do cliente. Para [bens digitais](../stores-purchase/taxes.md) vendidos na UE, o IVA é baseado no endereço de cobrança do cliente. <br/><br/> Este campo não é o mesmo que o Número de Imposto/IVA. |
| **[!UICONTROL Account Lock]** | Indica o status da conta. Como medida de segurança, as contas de cliente podem ser [bloqueadas](../customers/password-options.md) após muitas tentativas de logon. Valores: `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | O status atual do usuário. Opções: `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | Classificação do cliente. Opções: `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | O representante de vendas que é atribuído como ponto de contato para uma conta da empresa e recebe todas as mensagens de email automatizadas relacionadas à empresa. |

{style="table-layout:auto"}
