---
title: Imposto fixo sobre o produto (FPT)
description: Saiba como configurar um imposto de produto fixo (FPT) que deve ser adicionado a determinados tipos de produtos.
exl-id: f1b475cb-a6fe-4b51-a0c3-7d0a202bd332
feature: Checkout, Invoices, Taxes, Products
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---

# Imposto fixo sobre o produto (FPT)

Algumas jurisdições de imposto têm um imposto fixo que deve ser adicionado a determinados tipos de produtos. Você pode configurar um _imposto fixo de produto_ (FPT) conforme necessário para os cálculos de imposto da loja. Em alguns países, a FPT pode ser usada para criar um imposto sobre resíduos de equipamentos elétricos e eletrônicos (WEEE). Esse imposto também é conhecido como _imposto ecológico_ ou _imposto ecológico_, e é coletado em certos tipos de eletrônicos para compensar o custo da reciclagem. É uma quantidade fixa, em vez de uma porcentagem do preço do produto.

Impostos fixos do produto se aplicam no nível do item, com base no produto. Em algumas jurisdições, esse imposto está sujeito a um cálculo de imposto de % extra. Sua jurisdição de imposto também pode ter regras sobre como o preço do produto aparece para os clientes, com ou sem imposto. Compreenda as regras e defina as opções de exibição do FPT de acordo.

Tenha cuidado ao cotar os preços da FPT no email, pois a diferença de preço pode afetar a confiança do cliente em seus pedidos. Por exemplo, se você exibir os preços de Revisão da Ordem sem mostrar FPT, os clientes que compram itens com FPT associado verão um total que inclui a quantia de imposto FPT, mas sem uma divisão discriminada. A diferença de preço pode levar alguns clientes a abandonar seus carrinhos porque o total difere do valor esperado.

## Preços de exibição do FPT

| FPT | Exibir configuração e cálculo | |
|--- |--- |---|
| Não Tributado | **[!UICONTROL Excluding FPT]** | O FPT aparece como uma linha separada no carrinho e o valor é usado nos cálculos de imposto apropriados. |
| | **[!UICONTROL Including FPT]** | O FPT é adicionado ao preço base de um item, mas não é incluído nos cálculos baseados em regra de imposto. |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | Os preços aparecem sem a quantia ou descrição FPT. O FPT não está incluído nos cálculos baseados em regras de imposto. |
| Tributado | **[!UICONTROL Excluding FPT]** | O FPT aparece como uma linha separada no carrinho e o valor é usado nos cálculos de imposto apropriados. |
| | **[!UICONTROL Including FPT]** | FPT é incluído no preço de um item, e nenhuma alteração nos cálculos de imposto é necessária. |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | Os preços aparecem sem a quantia ou descrição do FPT. No entanto, o FPT é incluído nos cálculos baseados em regras de imposto. |

{style="table-layout:auto"}

## Configurar FPT

O [tipo de entrada](../catalog/attributes-input-types.md) de Imposto Fixo sobre Produtos (FPT) cria uma seção de campos para gerenciar impostos para cada região.

As instruções a seguir mostram como configurar um imposto de produto fixo para sua loja, usando &quot;imposto ecológico&quot; como exemplo. Após definir o escopo do imposto e os países e estados onde o imposto se aplica, e dependendo das opções escolhidas, os campos de entrada podem mudar de acordo com os requisitos locais. Para saber mais, consulte [Criar atributos de produto](../catalog/attribute-product-create.md).

### Etapa 1: Ativar imposto fixo sobre o produto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Tax]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Fixed Product Taxes]**.

1. Defina **[!UICONTROL Enable FPT]** como `Yes`.

1. Para determinar como os impostos fixos do produto são usados nos preços de armazenamento, escolha a configuração FPT para cada um dos seguintes locais de exibição de preço:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Prices on Product View Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   Opções (as mesmas para cada uma):

   - `Including FPT Only`
   - `Including FPT and FPT description`
   - `Excluding FPT. Including FPT description and final price`
   - `Excluding FPT`

1. Defina **[!UICONTROL Apply Tax to FPT]** conforme necessário.

1. Defina **[!UICONTROL Include FPT in Subtotal]** conforme necessário.

   ![Impostos Fixos sobre Produtos](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Impostos Fixos sobre Produtos](../configuration-reference/sales/tax.md#fixed-product-taxes) no _Guia de Referência de Configuração_.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Etapa 2: Criar um atributo FPT

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Attribute]** e faça o seguinte:

   - Para **[!UICONTROL Default Label]**, insira um rótulo que identifique o atributo.

   - Defina **[!UICONTROL Catalog Input for Store Owner]** como `Fixed Product Tax`.

   ![Propriedades do atributo](./assets/tax-fpt-attribute-properties.png){width="600" zoomable="yes"}

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Advanced Attribute Properties]** e defina as opções de propriedade:

   - **[!UICONTROL Attribute Code]** - Digite um identificador exclusivo em minúsculas, sem espaços ou caracteres especiais. O comprimento máximo é de 30 caracteres. É possível deixar o campo em branco para o texto do campo Rótulo padrão.

   - **[!UICONTROL Add to Column Options]** - Se você quiser que o campo FPT apareça na [Lista de produtos](../catalog/products-list.md), defina como `Yes`.

   - **[!UICONTROL Use in Filter Options]** - Se quiser poder [filtrar](../getting-started/admin-workspace.md) produtos na grade com base no valor do campo FPT, defina como `Yes`.

   ![Propriedades Avançadas de Atributo](./assets/tax-fpt-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. (Opcional) No painel esquerdo, escolha **[!UICONTROL Manage Labels]** e insira um rótulo para usar em vez do rótulo padrão para cada exibição de loja.

   ![Gerenciar rótulos](./assets/attribute-new-manage-labels.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Attribute]**.

1. Quando solicitado, atualize o [cache](../systems/cache-management.md).

### Etapa 3: Adicionar o atributo FPT a um conjunto de atributos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Na lista, clique no conjunto de atributos para abrir o registro no modo de edição.

   ![Lista de conjuntos de atributos](./assets/attribute-sets-list.png){width="600" zoomable="yes"}

1. Arraste o atributo FPT da lista de **[!UICONTROL Unassigned Attributes]** à direita da lista **[!UICONTROL Groups]** na coluna central.

   Cada pasta de grupo corresponde a uma seção de informações do produto. Você pode colocar o atributo onde quiser que ele apareça quando o produto estiver aberto no modo de edição.

   ![Editar Conjunto de Atributos](./assets/tax-fpt-attribute-set-drag.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Repita esta etapa para cada conjunto de atributos que deve incluir o imposto fixo do produto.

### Etapa 4: Aplicar o FPT a produtos específicos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra o produto que precisa de um imposto de produto fixo no modo de edição.

1. Encontre a seção **[!UICONTROL FPT]** dos campos que você adicionou ao conjunto de atributos e clique em **[!UICONTROL Add Tax]**.

1. Especifique o imposto aplicável ao produto:

   ![Imposto de Produto Fixo para o Canadá](./assets/tax-product-fpt-canada.png){width="600" zoomable="yes"}

   - Se sua instância do Commerce tiver vários sites, escolha o **[!UICONTROL Website]** apropriado e a moeda base. Neste exemplo, o campo é definido por padrão como `All Websites [USD]`.

   - Defina **[!UICONTROL Country/State]** para a região na qual o imposto fixo do produto se aplica.

   - Para **[!UICONTROL Tax]**, insira o imposto fixo sobre produtos como um valor decimal.

1. Para adicionar mais impostos fixos do produto, clique em **[!UICONTROL Add Tax]** e repita o processo.

1. Quando terminar, clique em **[!UICONTROL Save]**.
