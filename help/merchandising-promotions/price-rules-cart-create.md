---
title: Criar uma regra de preço de carrinho
description: Saiba como criar uma regra de preço de carrinho com base nos atributos de carrinho ou produto.
exl-id: 7260e7c3-3b1e-43e5-9c09-c40538e37378
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: bf52884cb0eccd4d9c7326a95f8600a3ed950918
workflow-type: tm+mt
source-wordcount: '2885'
ht-degree: 0%

---

# Criar uma regra de preço de carrinho

Complete as etapas a seguir para adicionar uma regra, descrever as condições e definir as ações. Preencha também os rótulos e teste a regra. As condições da regra de preço podem ser baseadas no carrinho ou [atributos do produto](../catalog/product-attributes.md) ou [Públicos da Real-Time CDP](#use-real-time-cdp-audiences-to-set-a-condition), mas não em [opções personalizáveis](../catalog/settings-advanced-custom-options.md).

## Etapa 1: adicionar uma regra

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

1. Clique em **[!UICONTROL Add New Rule]** e faça o seguinte:

   - Em _[!UICONTROL Rule Information]_, conclua o **[!UICONTROL Rule Name]**e **[!UICONTROL Description]**.

   - Se não quiser que a regra entre em vigor imediatamente, defina **[!UICONTROL Active]** para `No`.

   ![Regra de preço do carrinho - informações da regra](./assets/price-rule-cart-new.png){width="600" zoomable="yes"}

1. Para estabelecer o [escopo](../getting-started/websites-stores-views.md#scope-settings) da regra, faça o seguinte:

   - Selecione o **[!UICONTROL Websites]** onde a promoção deve estar disponível.

   - Selecione o **[!UICONTROL Customer Groups]** a que a promoção se aplica.

     Se quiser que a promoção esteja disponível somente para clientes registrados, **_não_** escolha o `NOT LOGGED IN` opção.

1. Defina a regra a ser aplicada com ou sem um [cupom](price-rules-cart-coupon.md) do seguinte modo:

   - Para aplicar a regra do carrinho sem o uso de um código de cupom, defina **[!UICONTROL Coupon]** para `No Coupon` e pule para a etapa 5.

   - Para associar um cupom a uma regra de preço, defina **[!UICONTROL Coupon]** para `Specific Coupon` e faça o seguinte:

      - Inserir um texto livre **[!UICONTROL Coupon Code]** que o cliente deve inserir para receber o desconto.

      - Para definir um limite no número de vezes que o cupom pode ser usado, complete as seguintes opções:

     | Opção | Descrição |
     |------|-----------|
     | `Uses per Coupon` | Determina quantas vezes o código do cupom pode ser usado. Se não houver limite, deixe o campo em branco. |
     | `Uses per Customer` | Determina quantas vezes a regra de preço do carrinho pode ser usada pelo mesmo cliente registrado que pertence a qualquer um dos grupos de clientes selecionados. A configuração não se aplica a compradores de convidados que são membros do grupo de clientes NÃO CONECTADO, ou a clientes que compram sem fazer logon em suas contas. Se não houver limite, deixe o campo em branco. |

     {style="table-layout:auto"}

     Para saber mais, consulte [Códigos de cupom](price-rules-cart-coupon.md).

     ![Regra de preço do carrinho - configurações de cupom](./assets/price-rule-cart-coupon-settings-ee.png){width="600" zoomable="yes"}

   - ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) Use o _Calendário_ (![Ícone de calendário](../assets/icon-calendar.png)) para escolher o **[!UICONTROL From]** e **[!UICONTROL To]** intervalo de datas da promoção.

1. Insira um número para definir o **[!UICONTROL Priority]** desta regra de preço em relação às Configurações de ação de outras regras de preço que estão ativas ao mesmo tempo.

   >[!NOTE]
   >
   >A configuração de Prioridade é importante quando duas regras de carrinho/códigos de cupom são válidas para o mesmo produto ao mesmo tempo. A regra com a configuração de Prioridade mais alta (`1` sendo a mais alta) controla a ação do carrinho. Consulte _Descartar Regras de Preços Subsequentes_ no _Definir as ações_ etapa.

   >[!NOTE]
   >
   >As regras de preço do carrinho com a mesma prioridade não resultam em um desconto combinado. Cada regra é aplicada à correspondência de produtos separadamente, um por um.

1. Para aplicar a regra a ser publicada [RSS feeds](social-rss.md#rss-feeds), definir **Público no RSS Feed** para `Yes`.

1. Clique em **[!UICONTROL Save and Continue Edit]**.

   - ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) Depois que a regra é salva, o nome da regra de preço do carrinho é exibido na parte superior da página.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente no Adobe Commerce) Depois que a regra é salva, o nome da regra de preço do carrinho e a variável [Alterações Agendadas](price-rule-cart-scheduled-changes.md) é exibida na parte superior da página.

     ![Regra de preço do carrinho - alterações programadas](./assets/price-rule-cart-scheduled-changes.png){width="600" zoomable="yes"}

## Etapa 2: descrever as condições

Nesta etapa, são descritas as condições que devem ser atendidas para que um pedido se qualifique para a promoção. A regra entra em ação sempre que o conjunto de condições é atendido.

Se você estiver usando públicos-alvo da Real-Time CDP, pule para [nesta seção](#use-real-time-cdp-audiences-to-set-a-condition).

>[!NOTE]
>
>A regra de preço do carrinho é aplicada a **_cada_** produto no carrinho de compras sempre que o conjunto de condições no _[!UICONTROL Conditions]_é atendida. Adicionar condições no_[!UICONTROL Actions]_ para limitar o número de produtos afetados pela regra de preço do carrinho.

>[!NOTE]
>
>Se pelo menos um atributo condicional de produto tiver um valor vazio, a regra de preço do carrinho não será aplicada ao produto.

1. No painel esquerdo, selecione **[!UICONTROL Conditions]**.

   ![Regra de preço do carrinho - condições](./assets/conditions.png){width="600" zoomable="yes"}

   A primeira condição é exibida por padrão e declara:

   `If **ALL** of these conditions are **TRUE**:`

   A instrução tem dois links em negrito nos quais você pode clicar para exibir a seleção de opções dessa parte da instrução. Você pode criar condições diferentes alterando a combinação desses valores. Siga um destes procedimentos:

   - Clique em **[!UICONTROL ALL]** e selecione `ALL` ou `ANY`.
   - Clique em **[!UICONTROL TRUE]** e selecione `TRUE` ou `FALSE`.
   - Deixe a condição inalterada para aplicar a regra a todos os produtos.

1. Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) no início da próxima linha e selecione uma opção para a condição, como atributo do carrinho, subseleção de produto ou combinação.

   Para este exemplo, complete a próxima parte da condição da seguinte maneira:

   - Quando solicitado a **[!UICONTROL Choose the condition to add]**, escolha `Products Subselection`.

     ![Condição de regra de preço do carrinho - subseleção de produtos](./assets/price-rule-cart-condition-products-subselection.png){width="600" zoomable="yes"}

   - Na declaração de condição, clique em **[!UICONTROL total quantity]** e selecione `total quantity` ou `total amount`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Total amount] é um total de linha, portanto, os impostos não são incluídos na `total amount` para o [!UICONTROL Products Subselection] condição da regra de preço do carrinho. Use o [!UICONTROL Subtotal (Incl. Tax)] condição para incluir impostos.

   - Na declaração de condição, clique em **[!UICONTROL is]** e selecione `greater than`.

1. Quando a próxima parte da condição for exibida, clique nos elementos da instrução para que você possa ver onde cada link com valores de variável está localizado.

1. Clique no link &quot;mais&quot; (...) e digite `100`.

   Essa condição exige que a quantidade total do carrinho seja `101` ou superior.

   ![Condição de regra de preço do carrinho - valor de quantidade total](./assets/condition-products-subselection3.png){width="600" zoomable="yes"}

1. Clique em **Adicionar** (![Ícone Adicionar](../assets/icon-add-green-circle.png)) no início da próxima linha e, em seguida, adicione uma condição que se baseie em **Categoria**.

   ![Condição de regra de preço do carrinho - categoria de atributo do produto](./assets/condition-products-subselection4.png){width="600" zoomable="yes"}

1. Na próxima parte da condição, clique no link _mais_ (**..**) para exibir o campo de entrada e, em seguida, abra o _Seletor_ (![Ícone de Lista](../assets/icon-list-chooser.png)) para exibir a árvore de categorias.

1. Marque a caixa de seleção da categoria que deseja usar como uma condição para a regra de preço e clique no ![Ícone Adicionar](../assets/icon-checkmark-green-circle.png) ícone para aceitar as seleções de categoria.

   A condição pode ser baseada em qualquer categoria secundária da loja [categoria raiz](../catalog/category-root.md).

   ![Condição da regra de preço do carrinho - categoria do produto](./assets/subselection-category.png){width="600" zoomable="yes"}

1. Para adicionar mais condições, clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) e definir outra condição.

   Você pode repetir o processo quantas vezes forem necessárias para descrever as condições que devem ser atendidas para a regra de preço. Veja alguns exemplos:

   **Exemplo 1:** Regra de Preço Regional

   Para criar uma regra de preço regional, use um dos seguintes atributos do carrinho:

   - `Shipping Postcode`
   - `Shipping Region`
   - `Shipping State/Province`
   - `Shipping Country`

   **Exemplo 2:** Totais do carrinho de compras

   Para basear a condição nos totais do carrinho de compras, use um dos seguintes atributos do carrinho:

   - `Subtotal`
   - `Total Items Quantity`
   - `Total Weight`

>[!NOTE]
>
>Em caso de várias promoções paralelas, a _Subtotal_ A condição é aplicada à variável _base_ subtotal do carrinho de compras **_antes_** quaisquer descontos.

>[!IMPORTANT]
>
>**Somente para ordens de compra**: Quando uma regra de preço do carrinho é definida com base em um ou mais métodos de pagamento específicos, o desconto é aplicado ao total quando uma ordem de compra é criada. Depois que a ordem de compra é criada, o desconto permanece aplicado ao total se o método de pagamento for alterado para um que não é coberto pela regra de preço do carrinho.

### Adicionar um atributo de produto às regras de preço do carrinho

1. Ir para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**e abra o atributo do produto.

1. No painel esquerdo, selecione **[!UICONTROL Storefront Properties]**.

1. Definir **[!UICONTROL Use for Promo Rule Conditions]** para `Yes`.

1. Clique em **[!UICONTROL Save Attribute]**.

1. Ir para **[!UICONTROL Marketing]** > **[!UICONTROL Cart Price Rules]** e abra a regra de preço do carrinho necessária.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Condition]** e selecione **[!UICONTROL Product attribute combination]**.

1. Defina essa condição com um dos seguintes valores:

   - Clique em **[!UICONTROL FOUND]** e selecione `FOUND` ou `NOT FOUND`.

   - Clique em **[!UICONTROL ALL]** e selecione `ALL` ou `ANY`.

1. Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) e selecione o botão **[!UICONTROL Product Attribute]** que você configurou para condições de regra promocional.

1. Clique em **[!UICONTROL Save]**.

>[!NOTE]
>
>Ao usar o `is not one of` condição com um _SKU_ atributo do produto e produto configurável, os SKUs do produto principal e secundário devem ser selecionados. Para evitar listar todos os SKUs filhos na regra, você pode usar o `does not contain` com partes SKU comuns de um produto configurável e seus produtos derivados.

### Usar públicos da Real-Time CDP para definir uma condição

É possível definir uma condição para uma regra de preço do carrinho com base em um Real-Time CDP [público](../customers/audience-activation.md).

1. Expandir **[!UICONTROL Conditions]**, clique no ícone &quot;+&quot; e selecione **[!UICONTROL Real-Time CDP Audience]** da lista.

   ![Selecionar condição de público-alvo do Real-Time CDP](./assets/rtcdp-conditions.png){width="300"}

1. Selecione o _Mais_ (**..**), clique em **[!UICONTROL Open Chooser]** e exiba todos os públicos-alvo do Real-Time CDP disponíveis.

   ![Exibir públicos-alvo da Real-Time CDP](./assets/rtcdp-conditions-chooser.png){width="600" zoomable="yes"}

1. Selecione o público-alvo do Real-Time CDP que deseja usar para a regra de preço do carrinho.

   | Opção | Descrição |
   |------|-----------|
   | `ID` | Um identificador interno do público-alvo usado no Administrador |
   | `Real-Time CDP Audience ID` | Identificador exclusivo do público-alvo quando ele foi criado no Experience Platform |
   | `Name` | Nome do público-alvo, como `Orders over $50` |
   | `Description` | Descrição do público-alvo, como `People who placed an order over $50 in the last month.`. |
   | `Source` | Indica a origem do público-alvo, como `Experience Platform`. |
   | `Website` | Indica qual site você vinculou à sequência de dados que contém os públicos-alvo. Você cria esse link ao conectar a instância do Commerce ao Experience Platform pelo [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html) extensão. |

   {style="table-layout:auto"}

Na próxima etapa, você define a ação a ser executada quando a condição for atendida.

## Etapa 3: definir as ações

As ações de regra de preço do carrinho de compras descrevem como os preços são atualizados quando as condições são atendidas.

1. Role para baixo até **[!UICONTROL Actions]** e expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção.

   ![Regra de preço do carrinho - ações ](./assets/price-rule-cart-actions.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Apply]** para uma das seguintes opções de desconto:

   | Opção | Descrição |
   |------|-----------|
   | `Percent of product price discount` | Descontos, subtraindo uma porcentagem do preço original. O desconto se aplica a cada item qualificado no carrinho. Por exemplo: Enter `10` in [!UICONTROL Discount Amount] por um preço atualizado 10% inferior ao preço original. |
   | `Fixed amount discount` | Descontos subtraindo um valor fixo do preço original de cada item qualificado do carrinho. Por exemplo: Enter `10` in [!UICONTROL Discount Amount] por um preço atualizado inferior em US$ 10 ao preço original. |
   | Desconto de valor fixo para o carrinho inteiro | Desconta o carrinho inteiro subtraindo um valor fixo do total do carrinho. Por exemplo: insira 10 em [!UICONTROL Discount Amount] para subtrair $10 do total do carrinho. Por padrão, o desconto se aplica somente ao subtotal do carrinho. Para aplicar o desconto ao subtotal e ao envio separadamente, use o _[!UICONTROL Apply to Shipping Amount]_opção. |
   | `Buy X get Y free` | Define uma quantidade que o cliente deve comprar para receber uma quantidade gratuitamente. (O [!UICONTROL Discount Amount] é Y.) |

   {style="table-layout:auto"}

   - Insira o **[!UICONTROL Discount Amount]** como um número, sem símbolos. Por exemplo, dependendo da opção de desconto selecionada, o número 10 pode indicar uma porcentagem, um valor fixo ou uma quantidade de itens.

   - Para um _Comprar X obter Y Gratuito_ desconto, insira a quantidade no campo **[!UICONTROL Discount Qty Step (Buy X)]** campo que o cliente deve comprar para receber o desconto.

   - No **[!UICONTROL Maximum Qty Discount is Applied To]** insira a quantidade máxima do mesmo produto que pode se qualificar para o desconto na mesma compra.

   - Definir **[!UICONTROL Apply to Shipping Amount]** (![Alternar opção](../assets/toggle-yes.png)) do seguinte modo:

     | Opção | Descrição |
     |------|-----------|
     | `Yes` | Aplica o valor do desconto separadamente aos valores de subtotal e remessa. |
     | `No` | Aplica o valor do desconto somente ao subtotal. |

     {style="table-layout:auto"}

   - Para interromper o processamento de outras regras depois que essa regra for aplicada, defina **[!UICONTROL Discard Subsequent Rules]** (![Alternar opção](../assets/toggle-yes.png)) para `Yes`. Essa configuração impede que vários descontos sejam aplicados ao mesmo produto.

     | Opção | Descrição |
     |------|-----------|
     | `Yes` | Impede que quaisquer outras regras de preços que possam ser aplicadas a um produto sejam aplicadas. Quando várias regras de preço se aplicam ao mesmo produto, somente a regra de preço com a prioridade mais alta definida (em uma regra [!UICONTROL Priority] (campo ) é aplicado ao produto qualificado. Isso impede que várias regras de preços sejam empilhadas e ofereçam descontos adicionais não intencionais. |
     | `No` | Permite que várias regras de preços sejam aplicadas ao mesmo produto. Isso pode resultar no empilhamento e no fornecimento de vários descontos aplicados ao preço da sua lista. |

     {style="table-layout:auto"}

     >[!IMPORTANT]
     >
     >Para descartar regras subsequentes, uma regra de preço deve usar as prioridades definidas no campo Prioridade de cada regra, e várias regras não devem ter a mesma prioridade definida. Consulte **[!UICONTROL Priority]** no _Adicionar uma nova regra_ etapa.

1. Para definir o **_exato_** produtos no carrinho de compras afetados pela regra de preço do carrinho, adicione a **_adicional_** condições necessárias para a ação.

   Para determinar se a entrega gratuita é aplicada a ordens que atendem às condições, defina **[!UICONTROL Free Shipping]** a um dos seguintes:

   | Opção | Descrição |
   |------|-----------|
   | `No` | O frete gratuito não está disponível. |
   | `For matching items only` | O frete gratuito está disponível somente para itens que correspondem às condições da regra. |
   | `For shipment with matching items` | O frete gratuito está disponível para qualquer remessa que inclua itens correspondentes. A variável [Envio gratuito](../stores-purchase/shipping-free.md) o método de delivery deve estar habilitado para usar essa opção. |

   {style="table-layout:auto"}

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Para **[!UICONTROL Add Rewards Points]**, insira o número fixo de pontos que o cliente ganha **_uma vez_** por pedido sempre que a regra de preço do carrinho for aplicada.

   Se os pontos de premiação não estiverem ativados, deixe este campo em branco.

1. Quando terminar, clique em **[!UICONTROL Save and Continue Edit]**.

## Etapa 4: preencher os rótulos

O rótulo aparece na seção totais do pedido para identificar o desconto. O texto da etiqueta está entre parênteses, depois da palavra `Discount`. Você pode inserir um rótulo padrão para todas as exibições de loja ou inserir um rótulo diferente para cada exibição.

![Carrinho de vitrine - rótulos de desconto](./assets/order-totals-section-discount-special.png){width="600"}

1. Role para baixo até **[!UICONTROL Labels]** e expandir ![Seletor de expansão](../assets/icon-display-expand.png)a seção.

1. Insira o texto que deseja usar como **[!UICONTROL Default Rule Label for All Store Views]**.

   ![Regra de preço do carrinho - etiqueta padrão](./assets/label-default.png){width="600" zoomable="yes"}

1. Se a loja tiver várias exibições ou vários sites com várias exibições, insira o texto do rótulo apropriado para cada uma.

   Por exemplo, se cada exibição de loja estiver em um idioma diferente, insira a tradução do rótulo para cada exibição.

   ![Armazenar rótulos específicos](./assets/label-store-specific.png){width="600" zoomable="yes"}

## Etapa 5: adicionar blocos dinâmicos relacionados (opcional)

{{ee-feature}}

[Blocos dinâmicos](../content-design/dynamic-blocks.md) que estão associados à regra aparecem na loja sempre que as condições são atendidas.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Related Dynamic Blocks]** seção.

1. Use o [filtros de pesquisa](../getting-started/admin-workspace.md) para localizar os blocos que deseja associar à regra.

1. Marque a caixa de seleção na primeira coluna para associar o bloco à regra.

   Para saber mais, consulte [Blocos Dinâmicos em Regras de Preço](../content-design/dynamic-blocks-price-rules.md).

## Etapa 6: salvar e testar a regra

1. Quando terminar, clique em **[!UICONTROL Save Rule]**.

1. Teste a regra para verificar se ela funciona corretamente.

   As regras de preço são processadas automaticamente com outras regras do sistema todas as noites. Ao criar uma regra de preço, aguarde tempo suficiente para ela entrar no sistema. Teste a regra também para verificar se ela funciona corretamente. À medida que novas regras são adicionadas, o Commerce recalcula os preços e as prioridades de acordo.

## Demonstração da regra de preço do carrinho

Assista a este vídeo para saber mais sobre como criar regras de preço de carrinho:

>[!VIDEO](https://video.tv.adobe.com/v/343835?quality=12)

## Descrições dos campos

### [!UICONTROL Rule Information]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Rule Name] | (Obrigatório) O nome da regra é para referência interna. |
| [!UICONTROL Description] | Uma descrição da regra deve incluir a finalidade da regra e explicar como ela é usada. |
| [!UICONTROL Active] | (Obrigatório) Determina se a regra está ativa no armazenamento. Opções: `Yes` / `No` |
| [!UICONTROL Websites] | (Obrigatório) Identifica os sites nos quais a regra pode ser usada. |
| [!UICONTROL Customer Groups] | (Obrigatório) Identifica os grupos de clientes aos quais a regra se aplica. |
| [!UICONTROL Coupon] | (Obrigatório) Indica se um cupom está associado à regra. Opções: <br/>**[!UICONTROL No Coupon]**- Nenhum cupom está associado à regra.<br/>**[!UICONTROL Specific Coupon]** - Um cupom específico está associado à regra. <br/>**[!UICONTROL Coupon Code]**- Quando solicitado, insira o Código do Cupom que o cliente deve inserir para aproveitar a promoção.<br/>**[!UICONTROL Use Auto Generation]** - Marque a caixa de seleção para gerar automaticamente vários códigos de cupom que podem ser usados com a promoção. <br/>**[!UICONTROL Auto]**- Exibe o _[!UICONTROL Manage Coupon Codes]_seção para definir o formato dos códigos de cupom a serem gerados. |
| [!UICONTROL Uses per Coupon] | Determina quantas vezes o código do cupom pode ser usado. Se não houver limite, deixe o campo em branco. |
| [!UICONTROL Uses per Customer] | Determina quantas vezes a regra de preço do carrinho pode ser usada pelo mesmo cliente registrado que pertence a qualquer grupo de clientes selecionado. Não se aplica a compradores de convidados que são membros do grupo de clientes NÃO CONECTADOS, ou a clientes que compram sem fazer logon em suas contas. Para sem limite, deixe em branco. |
| [!UICONTROL Priority] | Um número que indica a prioridade dessa regra em relação a outras. A prioridade mais alta é número `1`. |
| [!UICONTROL Public in RSS Feed] | Determina se a promoção está incluída no RSS feed público da loja. Opções:  `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) A primeira data em que o cupom pode ser usado. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) A última data em que o cupom pode ser usado. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Especifica as condições que devem ser atendidas antes que a regra de preço do carrinho entre em ação. Se deixado em branco, a regra se aplica a todos os produtos no carrinho. As condições podem ser baseadas em qualquer combinação de carrinho e atributos de produto. No entanto, [opções personalizáveis](../catalog/settings-advanced-custom-options.md) não pode ser referenciado nas condições da regra de preço do carrinho.

### [!UICONTROL Actions]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Apply] | Determina o tipo de cálculo aplicado à compra. Opções: <br/>**[!UICONTROL Percent of product price discount]**- Descontos, subtraindo uma porcentagem do preço original. Por exemplo: Enter `10` in _[!UICONTROL Discount Amount]_por um preço atualizado 10% inferior ao preço original.<br/>**[!UICONTROL Fixed amount discount]**- Descontos subtraindo um valor fixo do preço original de cada item qualificado do carrinho. Por exemplo: Enter `10` in_[!UICONTROL Discount Amount]_ por um preço atualizado inferior em US$ 10 ao preço original. <br/>**[!UICONTROL Fixed amount discount for whole cart]**- Desconta o carrinho inteiro subtraindo um valor fixo do subtotal do carrinho. Por exemplo: Enter `10` in _[!UICONTROL Discount Amount]_para subtrair $10 do subtotal do carrinho. Por padrão, o desconto se aplica somente ao subtotal do carrinho. Para aplicar o desconto ao subtotal e ao envio separadamente, consulte_Aplicar ao Valor de Remessa _.<br/>**[!UICONTROL Buy X Get Y Free (discount amount is Y)]**- Define uma quantidade que o cliente deve comprar para receber uma quantidade gratuitamente. (O_[!UICONTROL Discount Amount]_ é Y.) |
| [!UICONTROL Discount Amount] | (Obrigatório) A quantia de desconto oferecida. |
| [!UICONTROL Maximum Qty Discount is Applied To] | Define o número máximo de produtos aos quais o desconto pode ser aplicado na mesma compra. |
| [!UICONTROL Discount Qty Step (Buy X)] | Define o número de produtos representados por `X` em um `Buy X Get Y Free` promoção. |
| [!UICONTROL Apply to Shipping Amount] | Determina se o desconto é aplicado separadamente aos valores de subtotal e remessa. Caso contrário, será aplicado somente ao subtotal. Opções: `Yes` / `No` |
| [!UICONTROL Discard Subsequent Rules] | Determina se regras de prioridade mais baixa (1 é a prioridade mais alta) podem ser aplicadas ao produto quando esta regra de preço do carrinho é uma correspondência. Habilite esta opção para impedir que vários descontos sejam aplicados ao mesmo produto. Opções: `Yes` / `No` |
| [!UICONTROL Free Shipping] | Determina se a remessa gratuita está incluída na promoção e, nesse caso, para quais itens. Opções: <br/>**[!UICONTROL No]**- O frete gratuito não está disponível para a regra atual.<br/>**[!UICONTROL For matching items only]** - O frete gratuito está disponível somente para itens específicos no carrinho que correspondem à regra. <br/>**[!UICONTROL For shipment with matching items]**- O frete gratuito está disponível para todos os itens no carrinho. A variável [Envio gratuito](../stores-purchase/shipping-free.md) o método de delivery deve estar habilitado para usar essa opção. |
| [!UICONTROL Add Reward Points] | ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Especifica o número de [pontos de premiação](rewards-loyalty.md) que são ganhos pelo cliente sempre que a regra de preço é aplicada. |

{style="table-layout:auto"}

### [!UICONTROL Labels]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Default Rule Label for All Store Views] | Um rótulo padrão que identifica o desconto e pode ser usado para todas as exibições de loja. |
| [!UICONTROL Store View Specific Labels] | Se aplicável, especifica um rótulo diferente para identificar o desconto para cada exibição de loja. |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifica qualquer [blocos dinâmicos](../content-design/dynamic-blocks.md) que estão associados à regra.
