---
title: Definições de configuração de imposto
description: Saiba como definir configurações de imposto básicas, incluindo classes de imposto, cálculo e o destino de imposto padrão.
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# Definições de configuração de imposto

As instruções a seguir orientam você pela configuração básica de imposto para sua instância do Commerce. Antes de configurar seus impostos, verifique se você está familiarizado com as exigências de impostos do seu [localidade](store-localize.md#step-3-change-the-locale-of-the-store-view). Em seguida, conclua a configuração de imposto de acordo com suas necessidades.

Admin [permissões](../systems/permissions.md) pode ser definido como restrito [acesso](../systems/permissions-user-roles.md) para tributar recursos, com base na empresa _precisa saber_. Para criar uma função de Administrador com acesso às configurações de imposto, escolha os recursos Vendas/Imposto e Sistema/Imposto. Se estiver configurando um site para uma região diferente do ponto de origem de remessa padrão, você também deve permitir acesso aos recursos Sistema/Remessa da função. As configurações de entrega determinam a alíquota de imposto da loja usada para preços de catálogo.

## Definir as configurações gerais de imposto

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Para uma configuração multissite, defina **[!UICONTROL Store View]** ao site e à loja que é o destino da configuração.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Tax]**.

1. Complete as definições de configuração a seguir.

   Se necessário, limpe a **[!UICONTROL Use system value]** caixa de seleção de quaisquer configurações esmaecidas.

### [!UICONTROL Tax Classes]

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Tax Classes]** seção.

   ![Classes de Impostos](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Classe de Imposto para Entrega** — Defina para a classe apropriada. As classes padrão são: `None` e `Taxable Goods`
   - **Classe de Imposto para Opções de Presente** — ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Defina para a classe apropriada. As classes padrão são: `None` e `Taxable Goods`
   - **Classe de Imposto Padrão do Produto** — Defina para a classe apropriada. As classes padrão são: `None` e `Taxable Goods`
   - **Classe de Imposto Padrão do Cliente** — Defina para a classe apropriada. A classe padrão é: `Retail Customer` e `Wholesale Customer`

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. Expanda a **[!UICONTROL Calculation Settings]** seção.

   ![Configurações de Cálculo](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Tax Calculation Method Based On]** a um dos seguintes:

   - `Unit Price` - O preço de cada produto
   - `Row Total` - O total do item de linha no pedido, menos descontos
   - `Total` - O total do pedido

1. Definir **[!UICONTROL Tax Calculation Based On]** a um dos seguintes:

   - `Shipping Address` - O endereço para onde o pedido deve ser enviado
   - `Billing Address` - O endereço de cobrança do cliente ou da empresa
   - `Shipping Origin` - O endereço especificado como o endereço [ponto de origem](shipping-settings.md#point-of-origin) para sua loja

1. Definir **[!UICONTROL Catalog Prices]** para `Excluding Tax` ou `Including Tax`.

1. Definir **[!UICONTROL Shipping Prices]** para `Excluding Tax` ou `Including Tax`.

1. Definir **[!UICONTROL Apply Customer Tax]** a um dos seguintes itens para determinar se o imposto é aplicado ao preço original ou com desconto: `After Discount` ou `Before Discount`

1. Definir **[!UICONTROL Apply Discount on Prices]** a um dos seguintes itens para determinar se os descontos incluem ou excluem imposto: `Excluding Tax` ou `Including Tax`

1. Definir **[!UICONTROL Apply Tax On]** para `Custom price if available` ou `Original price only`.

1. Definir **[!UICONTROL Enable Cross-Border Trade]** a um dos seguintes:

   - `Yes` - Use preços consistentes em diferentes alíquotas de imposto. Se o preço do catálogo incluir imposto, escolha essa configuração para fixar o preço independentemente da alíquota de imposto do cliente.
   - `No` - Variar o preço por taxa de imposto.

   >[!IMPORTANT]
   >
   >Se [comércio transfronteiriço](#cross-border-price-consistency) estiver ativado, a margem de lucro será alterada por taxa de imposto. O lucro é determinado pela fórmula (`Revenue - CustomerVAT - CostOfGoodsSold`). Para permitir o comércio transfronteiriço, os preços devem ser definidos para incluir o imposto.

### [!UICONTROL Default Tax Destination Calculation]

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Default Tax Destination Calculation]** seção.

   ![Cálculo do Destino do Imposto Padrão](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Especifique a **[!UICONTROL Default Country]** para cálculos de imposto.

1. Se aplicável, especifique o **[!UICONTROL Default State]** para cálculos de imposto.

1. Se aplicável, especifique o **[!UICONTROL Default Post Code]** para cálculos de imposto.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Algumas combinações de configurações relacionadas a uma exibição de preço que incluem e excluem imposto podem ser confusas para o cliente. Para evitar o acionamento de uma mensagem de aviso, consulte a [configurações recomendadas](taxes.md#warning-messages).

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Price Display Settings]** seção.

   ![Configurações de exibição de preço](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Display Product Prices in Catalog]** a um dos seguintes:

   - `Excluding Tax` - Os preços de catálogo que aparecem na loja não incluem imposto.
   - `Including Tax` - Os preços de catálogo na loja incluem imposto somente se uma regra de imposto corresponder à origem do imposto ou se o endereço do cliente corresponder à regra de imposto. Isso pode acontecer depois que um cliente cria uma conta, faz logon ou usa a ferramenta de Estimativa de imposto e remessa no carrinho.
   - `Including and Excluding Tax` - Os preços do catálogo que aparecem na loja são exibidos com e sem imposto.

1. Definir **[!UICONTROL Display Shipping Prices]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Shopping Cart Display Settings]** seção.

   ![Configurações de exibição do carrinho de compras](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Para cada uma das seguintes configurações, escolha como deseja que os impostos e preços sejam exibidos no carrinho, de acordo com os requisitos da loja e do local:

   - Definir **[!UICONTROL Display Prices]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

   - Definir **[!UICONTROL Display Subtotal]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

   - Definir **[!UICONTROL Display Shipping Amount]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Definir **[!UICONTROL Display Gift Wrapping Prices]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Definir **[!UICONTROL Display Printed Card Prices]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

1. Defina as seguintes opções de exibição para `Yes` ou `No`, de acordo com suas necessidades:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Expandir ![Expansão](../assets/icon-display-expand.png) o **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** seção.

   ![Configurações de Exibição de Ordens, NFFs, Avisos de Crédito](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Especifique como os preços e os impostos aparecem nas ordens, NFFs e avisos de crédito:

   - Definir **[!UICONTROL Display Prices]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

   - Definir **[!UICONTROL Display Subtotal]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

   - Definir **[!UICONTROL Display Shipping Amount]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Definir **[!UICONTROL Display Gift Wrapping Prices]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Definir **[!UICONTROL Display Printed Card Prices]** para `Excluding Tax`, `Including Tax`ou `Including and Excluding Tax`.

1. Defina as seguintes opções de exibição como `Yes` ou `No`, de acordo com suas necessidades:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Fixed Product Taxes]** seção.

   ![Impostos Fixos sobre Produtos](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Enable FPT]** para ou para `Yes` ou `No`, de acordo com suas necessidades.

1. Se o FPT estiver ativado, especifique as opções de exibição do FPT:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - Os preços exibidos incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente.
   - `Including FPT and FPT description` - Os preços exibidos incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.
   - `Excluding FPT. Including FPT description and final price` - Os preços exibidos não incluem impostos fixos sobre o produto. O valor de FPT é exibido separadamente.
   - `Excluding FPT` - Os preços exibidos não incluem impostos fixos sobre o produto. O valor FPT não é exibido separadamente.

1. Definir **[!UICONTROL Apply Discounts to FPT]** para `Yes` ou `No`, de acordo com suas necessidades.

1. Definir **[!UICONTROL FPT Tax Configuration]** para determinar o modo de cálculo do FPT.

   - `Not Taxed` - Selecione esta opção se sua jurisdição de tributação não tributar FPT. (Por exemplo, Califórnia.)
   - `Taxed` - Selecione esta opção se sua jurisdição de tributação tributa FPT. (Por exemplo, Canadá.)
   - `Loaded and Displayed with Tax` - Clique nesta opção se FPT for adicionado ao total do pedido antes de aplicar o imposto. (Por exemplo, países da UE.)

1. Definir **[!UICONTROL Include FPT in Subtotal]** para `Yes` ou `No`, de acordo com suas necessidades.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Coerência dos preços transfronteiras

O comércio transfronteiriço (também conhecido como consistência de preços) apoia a União Europeia (UE) e outros comerciantes que desejam manter preços consistentes para clientes cujas taxas de imposto são diferentes da taxa de imposto da loja.

Os comerciantes que operam entre regiões e geografias podem exibir um único preço incluindo o imposto no preço do produto. Os preços são limpos e desorganizados, independentemente das estruturas e taxas de imposto que variam de país para país. Essas configurações exigem que uma extensão de cálculo de imposto seja instalada do [Marketplace](../getting-started/commerce-marketplace.md), como _Vertex Cloud_.

>[!NOTE]
>
>Quando o comércio transfronteiriço estiver habilitado, sua margem de lucro será alterada por alíquota de imposto. O lucro é determinado pela fórmula:<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_Para permitir a coerência dos preços transfronteiras:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Para uma configuração multissite, defina **[!UICONTROL Store View]** ao site e à loja que é o destino da configuração.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Tax]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Calculation Settings]** seção.

1. Definir **[!UICONTROL Catalog Prices]** para `Including Tax`.

1. Para permitir a coerência dos preços transfronteiras, **[!UICONTROL Enable Cross Border Trade]** para `Yes`.

   ![Habilitar Configurações de Comércio Transfronteiriço](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
