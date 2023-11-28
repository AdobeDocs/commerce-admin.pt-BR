---
title: Retorna atributo
description: Saiba mais sobre os atributos de retorno e como criar os atributos necessários para processar retornos em sua loja.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Retorna atributo

{{ee-feature}}

Os atributos de devolução são usados para armazenar informações necessárias durante o processo de devolução do produto. Os atributos padrão incluem a condição do produto devolvido, o motivo da devolução e um campo que indica como a devolução foi resolvida. O processo para criar um atributo de retornos é semelhante à criação de um [atributo do cliente](../customers/attribute-properties.md).

![Administrador - Retorna atributos](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Criar um atributo returns

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Attribute]**.

   ![Novo retorno - propriedades do atributo](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Definir as propriedades

1. Para identificar o atributo durante a entrada de dados, defina o **[!UICONTROL Default Label]**.

1. Para **[!UICONTROL Attribute Code]**, informe um código que identifique o atributo no sistema.

1. Para determinar o tipo de controle de entrada usado para entrada de dados, defina **[!UICONTROL Input Type]** a um dos seguintes:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Para tornar o campo um item obrigatório, defina **[!UICONTROL Values Required]** para `Yes`.

1. Para atribuir um valor inicial ao campo, insira um **[!UICONTROL Default Value]**.

1. Para validar a precisão dos dados inseridos no campo antes do salvamento do registro, defina **[!UICONTROL Input Validation]** a um dos seguintes:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Para o `Text Field` e `Text Area` tipos de entrada, insira o **[!UICONTROL Minimum Text Length]** e **[!UICONTROL Maximum Text Length]**.

1. Para aplicar um filtro de pré-processamento, defina **[!UICONTROL Input/Output Filter]** a um dos seguintes:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Para tornar o atributo visível para os clientes, defina **[!UICONTROL Show on Storefront]** para `Yes` no _[!UICONTROL Storefront Properties]_seção.

1. (Opcional) Para **[!UICONTROL Sort Order]**, digite um número para determinar onde esse atributo aparece em relação aos outros na mesma parte da página. (`0` = primeiro, `1` = segundo, `2` = terceiro e assim por diante.)

### Gerenciar rótulos/opções

1. No painel esquerdo, escolha **[!UICONTROL Manage Labels/Options]**.

1. No **[!UICONTROL Manage Titles (Size, Color, etc.)]** insira o rótulo para cada exibição de loja.

   ![Gerenciar rótulos](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Se a variável **[!UICONTROL Input Type]** para o atributo é `Dropdown`, gerencie as opções no **[!UICONTROL Manage Options (Values of Your Attribute)]** seção.

   - Para adicionar uma opção, clique em **[!UICONTROL Add Option]** e insira o rótulo para Admin e cada visualização de loja.
   - Para tornar uma opção o padrão selecionado, escolha **[!UICONTROL Is Default]**.
   - Para remover uma opção, clique em **[!UICONTROL Delete]**.

1. Para salvar as alterações, clique em **[!UICONTROL Save Attribute]**.
