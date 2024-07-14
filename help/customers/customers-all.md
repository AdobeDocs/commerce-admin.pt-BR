---
title: Lista de clientes
description: A grade Clientes lista todos os clientes que se registraram em uma conta na loja ou que foram adicionados pelo administrador.
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Lista de clientes

No Administrador, a grade [!UICONTROL Customers] lista todos os clientes que se registraram em uma conta na sua loja ou que foram adicionados pelo administrador. Use os [controles de grade](../getting-started/admin-grid-controls.md) padrão para filtrar a lista e ajustar o layout da coluna. Para saber mais, consulte [Gerenciar contas de clientes](../customers/manage-account.md).

![Lista de clientes](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## Atualizar informações do cliente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Encontre o registro do cliente e clique em [!UICONTROL **Editar**] na coluna _[!UICONTROL Action]_.

1. No painel esquerdo, escolha as informações que deseja editar e faça as alterações necessárias.

   >[!NOTE]
   >
   >Para saber mais, consulte [Atualizar contas de clientes](../customers/update-account.md).

1. Quando terminar, clique em **[!UICONTROL Save Customer]**.

## Controles do Workspace

| Controle | Descrição |
| --- | --- |
| **[!UICONTROL Add New Customer]** | Cria uma conta de cliente. |
| **[!UICONTROL Search]** | Inicia uma pesquisa por clientes com base nos filtros atuais. |
| **[!UICONTROL Filters]** | Define um conjunto de parâmetros de pesquisa usados para filtrar os registros que aparecem na [grade](../getting-started/admin-grid-controls.md). |
| **[!UICONTROL Default View]** | Determina a coluna padrão [layout](../getting-started/admin-grid-controls.md) da grade. |
| **[!UICONTROL Columns]** | Determina a seleção de [colunas](../getting-started/admin-grid-controls.md) e suas contas na grade. O layout da coluna pode ser alterado e salvo como uma _exibição_. Por padrão, apenas algumas colunas são incluídas na grade. |
| **[!UICONTROL Export]** | Exporta os registros selecionados como um arquivo CSV ou XML do Excel. |

{style="table-layout:auto"}

## Colunas

| Coluna | Descrição |
| --- | --- |
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
| **[!UICONTROL Date of Birth]** | A data de nascimento do cliente. <br><br>**_Importante:_**de acordo com as práticas recomendadas atuais de segurança e privacidade, esteja ciente de todos os possíveis riscos legais e de segurança associados ao armazenamento da data de nascimento completa do cliente (mês, dia, ano) com outros identificadores pessoais. É recomendável limitar o armazenamento das datas de nascimento completas dos clientes e sugerir que você use o ano de nascimento do cliente como alternativa. |
| **[!UICONTROL Tax / VAT Number]** | Se aplicável, o número do imposto ou o número do [imposto sobre valor agregado](../stores-purchase/vat.md) atribuído ao cliente. <br/><br/>Este campo não é o mesmo que o Número IVA. |
| **[!UICONTROL Gender]** | O sexo do cliente. |
| **[!UICONTROL Action]** | Editar - abre a conta da empresa no modo de edição. |

{style="table-layout:auto"}

### Colunas adicionais

Estas colunas estão disponíveis ao alterar o [layout da coluna](../getting-started/admin-grid-controls.md) da grade.

| Coluna | Descrição |
| --- | --- |
| **[!UICONTROL Company]** | O nome da empresa do cliente. |
| **[!UICONTROL Street Address]** | O endereço do cliente. |
| **[!UICONTROL City]** | A cidade onde o cliente está localizado. |
| **[!UICONTROL Fax]** | O número de fax do cliente, se aplicável. |
| **[!UICONTROL Billing Firstname]** | O nome no endereço de cobrança do cliente. |
| **[!UICONTROL Billing Lastname]** | O sobrenome no endereço de cobrança do cliente. |
| **[!UICONTROL Billing Address]** | O endereço para onde as informações de cobrança devem ser enviadas. |
| **[!UICONTROL Shipping Address]** | O endereço para onde os pedidos devem ser enviados. |
| **[!UICONTROL VAT Number]** | O número de imposto sobre valor agregado associado ao endereço do cliente. Para [bens digitais](../stores-purchase/taxes.md) vendidos na UE, o IVA é baseado no endereço de cobrança do cliente. <br/><br/>Este campo não é igual ao Número do Imposto/IVA. |
| **[!UICONTROL Account Lock]** | Indica o status da conta. Como medida de segurança, as contas de cliente podem ser [bloqueadas](../customers/password-options.md) após muitas tentativas de logon. Valores: `Locked` / `Unlocked` |

{style="table-layout:auto"}
