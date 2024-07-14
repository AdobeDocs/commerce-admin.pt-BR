---
title: Atributos de endereço do cliente
description: Saiba mais sobre os atributos de endereço do cliente e como configurar essas propriedades de atributo.
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 0%

---

# Atributos de endereço do cliente

{{ee-feature}}

O conjunto de atributos Endereço do Cliente determina as propriedades dos endereços que são inseridos no [catálogo de endereços](account-dashboard-address-book.md) a partir da conta do cliente ou durante o [check-out](../stores-purchase/checkout-process.md).

Os atributos de endereço personalizados podem ser configurados para fornecer informações adicionais, como um endereço de email opcional, conta Skype, número de telefone alternativo, prédio ou município. O atributo personalizado pode ser incorporado ao [modelo de endereço](address-templates.md) usado para produzir documentos de vendas. O processo para criar um atributo de endereço personalizado é quase o mesmo que criar um [atributo de cliente](attribute-properties.md).

Os atributos de endereço do cliente são usados nos seguintes formulários:

- [Registro de endereço do cliente](account-create.md)
- [Endereço da conta do cliente](account-dashboard-address-book.md)

![Administrador - Atributos de endereço do cliente](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## Etapa 1: Preencha as propriedades do atributo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Attribute]**.

   ![Propriedades do atributo do cliente](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. Na seção **[!UICONTROL Attribute Properties]**, faça o seguinte:

   - Digite um **[!UICONTROL Default Label]** que identifique o atributo durante a entrada de dados.

   - Digite um **[!UICONTROL Attribute Code]** que identifique o atributo no sistema.

     O código do atributo deve começar com uma letra e pode incluir qualquer combinação de letras minúsculas (a-z) e números (0-9). O código deve ter menos de 30 caracteres e não pode incluir caracteres especiais ou espaços. O caractere de sublinhado (_) pode ser usado para indicar um espaço.

     >[!TIP]
     >
     >**_Atalho:_** Para preencher apenas os campos obrigatórios, role até [!UICONTROL Storefront Properties], digite o [!UICONTROL Sort Order] e salve.

1. Para determinar o tipo de controle de entrada usado para entrada de dados, defina **[!UICONTROL Input Type]** como um dos seguintes:

   - `Text Field` - Um campo de texto de linha única.
   - `Text Area` - Uma área de texto multilinha.
   - `Multiple Line` - Cria várias linhas de texto para o atributo, semelhantes a um endereço de várias linhas. O número de linhas de entrada de dados separadas pode ser de 2 a 20. Use o `Default Value` para especificar o valor inicial do campo.
   - `Date` - Exibe um campo de data com um calendário pop-up. Propriedades adicionais: use `Default Value` para especificar o valor inicial do campo. <br/>Use `Minimal Value` para especificar a data mais antiga que pode ser inserida.  Use `Maximum Value` para especificar a última data que pode ser inserida.
   - `Dropdown` - Uma lista suspensa que aceita apenas um valor a ser selecionado.
   - `Multiple Select` - Uma lista suspensa que aceita vários valores a serem selecionados.
   - `Yes/No` - Um campo que oferece apenas uma opção de `Yes` ou `No` valores.
   - `File (attachment)` - Um campo que permite que um arquivo seja carregado e associado ao atributo do cliente como um anexo.
   - `Image File` - Um campo que permite que uma imagem seja carregada na galeria e associada ao atributo do cliente.

1. Se o cliente precisar inserir um valor no campo, defina **[!UICONTROL Values Required]** como `Yes`.

1. Para atribuir um valor inicial ao campo, insira um **[!UICONTROL Default Value]**.

1. Para verificar a precisão dos dados inseridos no campo antes que o registro seja salvo, defina **[!UICONTROL Input Validation]** como o tipo de dados que será permitido no campo. Os valores disponíveis dependem do _[!UICONTROL Input Type]_especificado.

   - `None` - O campo não tem validação de entrada durante a entrada de dados.
   - `Alphanumeric` - Aceita qualquer combinação de números (0-9) e caracteres alfabéticos (a-z, A-Z) durante a entrada de dados. Para incluir caracteres especiais, consulte [!UICONTROL Escape HTML Entities] na próxima etapa.
   - `Alphanumeric with Space` - Aceita qualquer combinação de números (0-9), caracteres alfabéticos (a-z, A-Z) e espaços durante a entrada de dados.
   - `Numeric Only` - Aceita somente números (0-9) durante a entrada de dados.
   - `Alpha Only` - Aceita somente caracteres alfabéticos (a-z, A-Z) durante a entrada de dados.
   - `URL` - Aceita apenas uma URL durante a entrada de dados.
   - `Email` - Aceita apenas um endereço de email durante a entrada de dados.
   - `Length Only` - Valida a entrada com base no comprimento dos dados inseridos no campo.

1. Para aplicar um filtro de pré-processamento a valores inseridos em um campo de texto, área de texto ou tipo de entrada de várias linhas, defina **[!UICONTROL Input/Output Filter]** como um dos seguintes:

   - `None` - Não aplica um filtro ao texto inserido no campo.
   - `Strip HTML Tags` - Remove marcas de HTML do texto. Esse filtro pode ajudar a limpar dados que estão colados em um campo de outra fonte que inclui tags HTML.
   - `Escape  HTML Entities` - Converte caracteres especiais encontrados no texto em uma sequência de HTML de escape válida, como `&;`. As sequências de escape são delimitadas entre um E comercial e um ponto e vírgula, e são frequentemente usadas para aspas inteligentes, direitos autorais e símbolos de marca comercial do tipógrafo. As sequências de escape também são usadas para identificar caracteres como os símbolos menor que (`<`) e maior que (`>`) e o caractere E comercial (&amp;) que também são usados no código. Este filtro pode ajudar a limpar os caracteres especiais que às vezes são colados nos campos do banco de dados a partir de processadores de texto.

1. Complete as propriedades da grade e do segmento do cliente:

   - Para poder incluir a coluna na grade Clientes, defina **[!UICONTROL Add to Column Options]** como `Yes`.

   - Para filtrar a grade Clientes por este atributo, defina **[!UICONTROL Use in Filter Options]** como `Yes`.

   - Para filtrar a grade Clientes por atributo de texto com condições de correspondência de filtros diferentes, defina **[!UICONTROL Grid Filter Condition Type]** como `Partial Match`, `Prefix Match` ou `Full Match`. Isso não afeta o campo _Pesquisar por palavra-chave_ da grade.

   - Para pesquisar a grade Clientes por esse atributo, defina **[!UICONTROL Use in Search Options]** como `Yes`.

   - Para disponibilizar este atributo para [segmentos de clientes](customer-segments.md), defina **[!UICONTROL Use in Customer Segment]** como `Yes`.

## Etapa 2: concluir as propriedades da loja

1. Role até a seção **[!UICONTROL Storefront Properties]**.

   ![Atributos de endereço do cliente - Propriedades da vitrine eletrônica](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. Para tornar o atributo visível para os clientes, defina **[!UICONTROL Show on Storefront]** como `Yes`.

1. Insira um número no campo **[!UICONTROL Sort Order]**, que determina sua ordem de aparência quando listado com outros atributos.

1. Defina **[!UICONTROL Forms to Use]** para cada formulário que deverá incluir o atributo.

   Para escolher ambas as opções, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) enquanto clica em cada formulário.

   - [Registro de Endereço do Cliente](account-create.md)
   - [Endereço da Conta do Cliente](account-dashboard-address-book.md)

## Etapa 3: preencha o rótulo e salve

1. No painel à esquerda, escolha **[!UICONTROL Manage Labels/Options]**.

1. Em **[!UICONTROL Manage Titles]**, insira um rótulo para identificar o atributo para cada [exibição de armazenamento](../getting-started/websites-stores-views.md).

1. Quando terminar, clique em **[!UICONTROL Save Attribute]**.

   ![Atributos de endereço do cliente - rótulos/opções](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## Descrições dos campos

### [!UICONTROL Attribute Properties]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Default Label] | O rótulo padrão que identifica o atributo no Admin e na loja. |
| [!UICONTROL Attribute Code] | Um código exclusivo que identifica o atributo no sistema. O código pode ter até 21 caracteres e não pode incluir espaços ou caracteres especiais. O símbolo de sublinhado pode ser usado em vez de um espaço. |
| [!UICONTROL Input Type] | Determina o [controle de entrada](../catalog/attributes-input-types.md) usado para entrada de dados. Opções: <br/>**`Text Field`**- Um campo de texto de linha única.<br/>**`Text Area`** - Uma área de texto multilinha. <br/>**`Multiple Line`**- Cria várias linhas de texto para o atributo, semelhantes a um endereço de várias linhas. O número de linhas de entrada de dados separadas pode ser de 2 a 20.<br/>**`Date`** - Exibe um campo de data com um calendário pop-up.<br/>**`Dropdown`**- Uma lista suspensa que aceita apenas um valor a ser selecionado.<br/>**`Multiple Select`** - Uma lista suspensa que aceita vários valores a serem selecionados. <br/>**`Yes/No`**- Um campo que oferece apenas uma opção de `Yes` ou `No` valores.<br/>**`File (attachment)`** - Um campo que permite que um arquivo seja carregado e associado ao atributo do cliente como um anexo. <br/>**`Image File`**- Um campo que permite que uma imagem seja carregada na galeria e associada ao atributo do cliente. |
| [!UICONTROL Values Required] | Determina se um valor deve ser inserido no campo. Opções: `Yes` / `No` |
| [!UICONTROL Default Value] | Especifica o valor inicial do atributo. |
| [!UICONTROL Input Validation] | A seleção de opções é determinada pelo tipo de entrada. Opções: <br/>**`None`**- O campo não tem validação de entrada durante a entrada de dados.<br/>**`Alphanumeric`** - Aceita qualquer combinação de números (0-9) e caracteres alfabéticos (a-z, A-Z) durante a entrada de dados. <br/>**`Alphanumeric with Space`**- Permite que espaços no endereço cumpram com os requisitos de comprimento máximo da transportadora. Durante a finalização da compra, o cliente pode inserir qualquer combinação de números (0-9), caracteres alfabéticos (a-z, A-Z) e espaços no endereço do recipient e do remetente. Quaisquer espaços extras são cortados quando o endereço é salvo.<br/>**`Numeric Only`** - Aceita somente números (0-9) durante a entrada de dados. <br/>**`Alpha Only`**- Aceita somente caracteres alfabéticos (a-z, A-Z) durante a entrada de dados.<br/>** URL **- Aceita apenas uma URL durante a entrada de dados.<br/>**`Email`** - Aceita apenas um endereço de email durante a entrada de dados. <br/>**`Length Only`**- Valida a entrada com base no comprimento dos dados inseridos no campo. |
| [!UICONTROL Input/Output Filter] | Aplica um filtro de pré-processamento aos valores inseridos em um campo de texto, área de texto ou tipo de entrada de várias linhas antes de o registro ser salvo. Opções: <br/>**`None`**- Não aplica um filtro ao texto inserido no campo.<br/>**`Strip HTML Tags`** - Remove marcas de HTML do texto. Esse filtro pode ajudar a limpar dados que estão colados em um campo de outra fonte que inclui tags HTML. <br/>**`Escape HTML Entities`**- Converte caracteres especiais encontrados no texto em uma sequência de HTML de escape válida, como `amp;`. As sequências de escape são delimitadas entre um E comercial e um ponto e vírgula, e são frequentemente usadas para aspas inteligentes do tipógrafo, símbolos de direitos autorais e símbolos de marca comercial. As sequências de escape também são usadas para identificar caracteres como os símbolos menor que (`<`) e maior que (`>`) e o caractere E comercial (&amp;) que também são usados no código. Este filtro pode ajudar a limpar os caracteres especiais que às vezes são colados nos campos do banco de dados a partir de processadores de texto. |
| [!UICONTROL Add to Column Options] | Especifica se o atributo está incluído como uma coluna na grade [Clientes](./customers-all.md). Opções: `Yes` / `No` |
| Usar em Opções de Filtro | Especifica se o atributo pode ser usado como filtro para operações de pesquisa na grade. Opções: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Especifica condições de correspondência de filtros para atributos em operações de pesquisa da grade. Isso não afeta o campo _[!UICONTROL Search by keyword]_da grade. Opções: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Especifica se o valor do atributo pode ser usado como uma palavra-chave em operações de pesquisa. Opções: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Determina se o atributo está incluído nas condições do [segmento de cliente](./customer-segments.md). Opções: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Show on Storefront] | Determina se o atributo aparece como um campo nas informações do cliente na loja. Opções: `Yes` / `No` |
| [!UICONTROL Sort Order] | Especifica a ordem de classificação deste atributo em relação a outros atributos do cliente. A ordem de classificação determina a sequência em que os campos recebem foco durante a entrada de dados ao usar a navegação pelo teclado. |
| [!UICONTROL Forms to Use in] | Determina as páginas com formulários de entrada de dados em que o atributo aparece. Opções: <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
