---
title: Criar uma regra de preço de catálogo
description: Saiba como criar uma regra de preço de catálogo que aplica um desconto a produtos específicos sempre que um conjunto de condições é atendido.
exl-id: 53c5745b-f1c4-4ee8-b995-d2c70f639c7d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 0%

---

# Criar uma regra de preço de catálogo

Siga estas instruções para aplicar um desconto a produtos específicos sempre que um conjunto de condições for atendido. Os descontos da regra de preço de catálogo entram em vigor antes de o produto ser colocado no carrinho de compras.

## Etapa 1: adicionar uma regra

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rule]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Rule]**.

   A variável _[!UICONTROL Rule Information]_inclui seções expansíveis para **[!UICONTROL Conditions]**e **[!UICONTROL Actions]**.

   ![Regra de preço de catálogo - informações](./assets/price-rule-catalog-new-ee.png){width="700" zoomable="yes"}

1. Conclua o **[!UICONTROL Rule Name]** e **[!UICONTROL Description]** campos.

   Esses campos são somente para sua referência interna.

1. Defina o **[!UICONTROL Status]** da regra de preços, conforme necessário.

   Por padrão, o status é `Inactive`.

   >[!NOTE]
   >
   >Após a criação da regra, é possível atualizar o status alterando o status para `Active` ou `Inactive` conforme necessário.

1. Selecione o **[!UICONTROL Websites]** onde a regra deve estar disponível.

1. Selecione o **[!UICONTROL Customer Groups]** aos quais esta regra se aplica.

   Para escolher vários grupos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

   >[!NOTE]
   >
   >As opções nessa lista dependem dos grupos de clientes criados e gerenciados no _Clientes_ > _Grupos de Clientes_.

1. ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) Insira o **[!UICONTROL From]** e **[!UICONTROL To]** datas para determinar quando a regra de preço está em vigor.

   É possível inserir as datas ou usar a variável **[!UICONTROL Calendar]** (![Ícone de calendário](../assets/icon-calendar.png)) para escolher as datas. Se você deixar as datas em branco, a regra será ativada quando a regra de preço for salva.

1. Insira um número para estabelecer o **[!UICONTROL Priority]** desta regra em relação a outras regras.

   >[!NOTE]
   >
   >A variável _[!UICONTROL Priority]_a configuração é importante quando o mesmo produto de catálogo atende às condições definidas para mais de uma regra de preço. A regra com a configuração de prioridade mais alta (1 sendo a mais alta) se torna ativa para o produto.

## Etapa 2: definir as condições

A maioria das condições disponíveis é baseada nos valores de atributo existentes. Para aplicar a regra a todos os produtos, deixe as condições em branco.

>[!NOTE]
>
>Se pelo menos um atributo condicional de produto tiver um valor vazio, a regra de preço de catálogo não será aplicada ao produto.

>[!NOTE]
>
>Para aplicar uma `Category` condição de atributo de produto para qualquer [pacote](../catalog/product-create-bundle.md) ou [agrupado](../catalog/product-create-grouped.md) produto, todos os produtos derivados devem ser atribuídos à mesma categoria para que a regra seja aplicada corretamente. Caso contrário, você pode usar um [Regra de preço do carrinho](price-rules-cart-create.md) promoção em vez disso.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Conditions]** seção.

   A primeira condição é exibida por padrão e declara:

   `If **ALL** of these conditions are **TRUE**:`

   ![Regra de preço de catálogo - linha de condição 1](./assets/catalog-condition1.png){width="400"}

   A instrução tem dois links em negrito nos quais você pode clicar para exibir a seleção de opções dessa parte da instrução. Você pode criar condições diferentes alterando a combinação desses valores.

1. Altere a instrução de qualquer uma das seguintes maneiras:

   - Clique em **[!UICONTROL ALL]** e selecione `ALL` ou `ANY`.
   - Clique em **[!UICONTROL TRUE]** e selecione `TRUE` ou `FALSE`.
   - Deixe a condição inalterada para aplicar a regra a todos os produtos.

   Você pode criar condições diferentes alterando a combinação desses valores. Neste exemplo, a condição padrão é usada.

1. Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) no início da próxima linha e selecione uma opção para a condição, como um atributo ou combinação de produto.

1. Na lista abaixo **[!UICONTROL Product Attribute]**, escolha o atributo que deseja usar como a base da condição.

   Neste exemplo, a condição é `Attribute Set`.

   ![Regra de preço de catálogo - linha de condição 2](./assets/catalog-condition2.png){width="400"}

   >[!NOTE]
   >
   >Para que um atributo seja exibido na lista, ele deve ser configurado para uso nas condições de regra promocional. Para saber mais, consulte [Atributos do produto](../catalog/product-attributes.md).

   >[!NOTE]
   >
   >Ao usar o `is not one of` condição com um _SKU_ atributo do produto e produto configurável, os SKUs do produto principal e secundário devem ser selecionados. Para evitar listar todos os SKUs filhos na regra, você pode usar o `does not contain` com partes SKU comuns de um produto configurável e seus produtos derivados.

   A condição selecionada aparece na instrução, seguida por mais dois links em negrito. As opções diferem dependendo do atributo de condição selecionado. A declaração agora diz:

   `If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …`

1. Clique em **[!UICONTROL is]** e escolha o operador de comparação que descreve a condição a ser atendida.

   Essas opções podem incluir uma opção para comparações diferentes. Neste exemplo, as opções são `is` e `is not`.

1. Selecione ou insira valores para a condição.

   Dependendo da condição, você pode selecionar produtos de uma grade ou lista, inserir um valor numérico e assim por diante.

   ![Regra de preço de catálogo - linha de condição 2](./assets/catalog-condition3.png){width="400"}

   O item selecionado aparece na instrução para concluir a condição.

   `If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**`

1. Para adicionar outra linha de condição à instrução, clique no link _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) e escolha uma das seguintes opções:

   - `Conditions Combination`
   - `Product Attribute`

   Repita o processo até que todas as condições desejadas sejam concluídas.

   Se, a qualquer momento, você quiser excluir parte da declaração de condição, clique no **[!UICONTROL Delete]** (![Ícone Excluir](../assets/icon-delete-red-circle.png) ícone no final da linha.

## Etapa 3: definir as ações

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png)o **[!UICONTROL Actions]** e faça o seguinte:

   ![Regra de preço de catálogo - ações](./assets/price-rule-catalog-actions.png){width="600" zoomable="yes"}

1. Em **[!UICONTROL Pricing Structure Rules]**, definir **[!UICONTROL Apply]** a um dos seguintes:

   - `Apply as percentage of original` - Descontos por subtração de uma porcentagem do preço normal. Por exemplo: Insira 10 em Valor do desconto para um preço final marcado para 10% abaixo do preço normal.
   - `Apply as fixed amount` - Descontos, subtraindo um valor fixo do preço normal. Por exemplo: Insira 10 em Quantia de Desconto para um preço final que seja US$ 10 a menos que o preço normal.
   - `Adjust final price to this percentage` - Ajusta o preço final por uma porcentagem do preço normal. Por exemplo: Insira 25 em Valor do Desconto para um preço final marcado 75% abaixo do preço normal.
   - `Adjust final price to discount value` - Define o preço final como um valor fixo e com desconto. Por exemplo: Insira 20 em Valor do Desconto para um preço final de US$ 20,00.

   >[!NOTE]
   >
   >_Preço normal_ refere-se ao preço base do produto sem nenhum desconto promocional ou de preço avançado (especial/nível/grupo). _Preço final_ refere-se ao preço com desconto que aparece no carrinho de compras. <br/>A variável **_final_** o preço do produto é calculado como a **_mínimo_** preço relevante, utilizando a seguinte fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

   >[!NOTE]
   >
   >**_Preço Fixo_** produto As opções personalizáveis são _não_ afetados pelas regras de Preço do Grupo, Preço da Camada, Preço Especial ou Preço do Catálogo.

1. Insira o **[!UICONTROL Discount Amount]**.

1. Para interromper o processamento de outras regras depois que essa regra for aplicada, defina **[!UICONTROL Discard Subsequent Rules]** para `Yes`.

   >[!NOTE]
   >
   >Configurar como `Yes` O é uma salvaguarda para impedir que o sistema aplique vários descontos (regras) ao mesmo produto.

## Etapa 4: adicionar blocos dinâmicos relacionados

{{ee-feature}}

[Blocos dinâmicos](../content-design/dynamic-blocks.md) que estão associados a uma regra de preço de catálogo aparecem na loja sempre que as condições são atendidas. Esta é uma etapa opcional.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png)o **[!UICONTROL Related Dynamic Blocks]** seção.

1. Use o [filtros de pesquisa](../getting-started/admin-workspace.md) para localizar os blocos dinâmicos que deseja associar à regra.

1. Marque a caixa de seleção na primeira coluna para associar o bloco dinâmico à regra.

   ![Regra de preço de catálogo - blocos dinâmicos relacionados](./assets/price-rule-catalog-related-dynamic-blocks.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save and Continue Edit]**.

## Etapa 5: agendar a regra

{{ee-feature}}

>[!NOTE]
>
>Definir a regra como ativa deve ser adicionado como uma atualização programada. Para saber mais, consulte [Alterações Agendadas](price-rule-catalog-scheduled-changes.md).

1. No _Alterações Agendadas_ clique em **[!UICONTROL Schedule New Update]** na parte superior da caixa).

   Se a regra tiver uma atualização programada existente, você poderá clicar em **[!UICONTROL View/Edit]** à direita da alteração listada.

   Você pode editar a atualização existente ou atribuir a regra de preço do catálogo a outra campanha. A variável **Editar Atualização Existente** for selecionada por padrão.

1. Para programar a regra, insira o **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** que a regra de preço deve estar ativa.

   Você pode inserir as datas ou escolher as datas no campo _Calendário_ (![Ícone de calendário](../assets/icon-calendar.png)).

   ![Regra de preço de catálogo - atualizar programação](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save]**.

1. No _Informações da regra_ , defina o **[!UICONTROL Status]** para `active`.

## Etapa 6: salvar e testar a regra

1. Quando terminar, salve a regra.

   - ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) Clique em **[!UICONTROL Save and Apply]**.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente no Adobe Commerce) Clique em **[!UICONTROL Save]**.

     A página Informações da regra exibe uma linha do tempo atualizada nas Alterações programadas da regra.

     ![Regras de preço de catálogo - Alterações agendadas](./assets/price-rule-scheduled-changes-updated.png){width="600" zoomable="yes"}

1. Atualizar propriedades de uma regra:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente no Adobe Commerce) Clique em **[!UICONTROL Edit]** para exibir o _[!UICONTROL Rule Information]_página.

   - ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) Clique na regra na lista para exibir a variável _[!UICONTROL Rule Information]_página.

1. Teste a regra para verificar se ela funciona corretamente.

   As regras de preço são processadas automaticamente com outras regras do sistema todas as noites. Ao criar uma regra de preço, aguarde tempo suficiente para que ela entre no sistema antes de testar a regra para verificar se ela funciona corretamente. À medida que novas regras são adicionadas, o Commerce recalcula os preços e as prioridades de acordo.

## Demonstração da regra de preço de catálogo

Assista a este vídeo para saber mais sobre como criar regras de preço de catálogo:

>[!VIDEO](https://video.tv.adobe.com/v/343834?quality=12)

## Descrições dos campos

### [!UICONTROL Rule Information]

| Campo | Descrição |
|-----|-----------|
| [!UICONTROL Rule name] | (Obrigatório) O nome da regra é para referência interna. |
| [!UICONTROL Description] | Uma descrição da regra deve incluir a finalidade da regra e explicar como ela é usada. |
| [!UICONTROL Websites] | (Obrigatório) Identifica os sites nos quais a regra pode ser usada. |
| [!UICONTROL Customer Groups] | (Obrigatório) Identifica os grupos de clientes aos quais a regra se aplica. |
| [!UICONTROL Priority] | Um número que indica a prioridade dessa regra em relação a outras. A prioridade mais alta é o número 1. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) Determina se a regra está ativa no armazenamento. Opções: `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) Especifica o primeiro dia em que a regra de preço está em vigor. Se deixado em branco, a regra de preço entra em vigor quando é salva. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) Especifica o último dia em que a regra de preço está em vigor. Se deixado em branco, a regra de preço continuará indefinidamente. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Especifica as condições que devem ser atendidas antes que a regra de preço de catálogo entre em ação. Se deixado em branco, a regra se aplica a todos os produtos.

### [!UICONTROL Actions]

| Campo | Descrição |
|-----|-----------|
| [!UICONTROL Apply] | Determina o tipo de cálculo aplicado à compra. Opções: <br/>**[!UICONTROL Apply as percentage of original]**- Descontos por subtração de uma porcentagem do preço normal.<br/>**[!UICONTROL Apply as fixed amount]** - Descontos, subtraindo um valor fixo do preço normal. <br/>**[!UICONTROL Adjust final price to this percentage]**- Ajusta o preço final por uma porcentagem do preço normal.<br/>**[!UICONTROL Adjust final price to discount value]** - Define o preço final como um valor fixo e com desconto. <br/><br/>**_Nota:_**Preço normal refere-se ao preço base do produto sem qualquer preço avançado (especial/nível/grupo) ou descontos promocionais. Preço final refere-se ao preço com desconto que aparece no carrinho de compras. <br/>A variável**_final _**o preço do produto é calculado como a**_mínimo _**preço relevante, utilizando a seguinte fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)` |
| [!UICONTROL Discount Amount] | (Obrigatório) A quantia de desconto oferecida. |
| [!UICONTROL Discard Subsequent Rules] | Determina se regras adicionais podem ser aplicadas a esta compra. Para evitar que vários descontos sejam aplicados à mesma compra, selecione `Yes`. Opções: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifica qualquer [blocos dinâmicos](../content-design/dynamic-blocks.md) que estão associados à regra.
