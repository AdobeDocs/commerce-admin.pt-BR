---
title: Configurar  [!DNL Inventory Management] opções do produto
description: Saiba como definir as  [!DNL Inventory Management] opções de configuração do produto.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# Configurar opções do produto [!DNL Inventory Management]

Essas configurações se aplicam somente ao produto editado, substituindo todas as configurações no nível global do site. Modifique essas configurações ao editar um produto, por meio da seção _[!UICONTROL Sources]_&#x200B;e da página&#x200B;_[!UICONTROL Advanced Inventory]_.

- Configurar opções do produto por origem
- Configurar opções de produto para inventário avançado

## Opções de produto por origem

Defina as quantidades e as configurações adicionais por [origem adicionada](sources-add.md) para o produto.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra um produto no modo de edição.

1. Expanda o ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Sources]** e defina as configurações do produto para cada origem:

   - Insira um valor de **[!UICONTROL Qty]** (quantidade).

   - Defina o **[!UICONTROL Source Item Status]** como `In Stock` ou `Out of Stock`.

   - Para modificar a Notificação de Quantidade Inferior por origem, desmarque ou marque a caixa de seleção **[!UICONTROL Notify Quantity Use Default]**.

     Se desmarcado, insira o valor do nível de estoque que aciona o aviso de falta de estoque do item. O valor inserido é subtraído da Quantidade Venável do item no nível de estoque.

     `Select to use Default` - [!DNL Commerce] verifica as opções de inventário avançado do produto para obter as configurações.
     `Clear to Modify` - Insira um valor para a Quantidade de Notificação, substituindo as configurações de Inventário Avançado e Armazenamento.

   ![Seção de fontes para um produto](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Done]** e depois em **[!UICONTROL Save]**.

### Descrições dos campos

| Campo | Escopo | Descrição |
|--|--|--|
| [!UICONTROL Source Code] | Global | O código exclusivo de uma [origem](sources-manage.md). |
| [!UICONTROL Name] | Global | O nome exclusivo de uma origem. |
| [!UICONTROL Status] | Global | O produto está ativado ou desativado no catálogo. |
| [!UICONTROL Source Item Status] | Global | Determina a disponibilidade atual do produto. Opções:<br />`In Stock` - Disponibiliza o produto para compra.<br />`Out of Stock` - A menos que os Backorders estejam ativados, impede que o produto esteja disponível para compra e remove a listagem do catálogo. |
| [!UICONTROL Qty] | Global | Valores de estoque disponível para cada origem ou local. |
| [!UICONTROL Notify Quantity] | Global | Um valor para _[!UICONTROL Notify for Quantity Below]_&#x200B;para esta origem específica se&#x200B;_[!UICONTROL Notify Quantity Use Default]_ não estiver selecionado. |
| [!UICONTROL Notify Quantity Use Default] | Global | Indica o uso da configuração padrão para _[!UICONTROL Notify for Quantity Below]_&#x200B;no produto&#x200B;_[!UICONTROL Advanced Inventory]_ ou da configuração global na configuração da loja. |

## Opções avançadas do produto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra um produto no modo de edição.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Sources]** e clique em **[!UICONTROL Advanced Inventory]**.

1. Para habilitar o [controle de inventário](enable.md) para o catálogo, defina **[!UICONTROL Manage Stock]** como `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] configurações em produtos derivados substituem um produto configurável.

   ![Inventário avançado de um produto](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Digite um valor para **[!UICONTROL Out-of-Stock Threshold]**:

   | Valor | Descrição |
   | ----- | ----- |
   | Valor positivo | Com _[!UICONTROL Backorders]_&#x200B;desabilitado, insira um valor positivo. |
   | Zero | Com o _[!UICONTROL Backorders]_&#x200B;habilitado, inserir `0` permite infinitas ordens pendentes. |
   | Valor negativo | Com _[!UICONTROL Backorders]_&#x200B;habilitado, é recomendável inserir um valor negativo. O valor é adicionado à Quantidade Venável. Por exemplo, insira `-50` para permitir pedidos até esse valor. |

1. Insira o **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. Insira o **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. Defina **[!UICONTROL Qty uses Decimals]** como `Yes` se os clientes puderem usar um valor decimal em vez de um número inteiro ao inserir a quantidade solicitada.

1. Defina de **[!UICONTROL Allow Multiple Boxes for Shipping]** a `Yes` se o produto puder ser vendido separadamente, em muitas caixas. Esta opção fica visível quando **[!UICONTROL Qty Uses Decimals]** está definida somente como `Yes`.

1. Defina **[!UICONTROL Backorders]** como um dos seguintes:

   | Opção | Descrição |
   | ----- | ----- |
   | `No Backorders` | Para não aceitar pedidos pendentes quando o produto estiver indisponível. |
   | `Allow Qty Below 0` | Para aceitar backorders quando a quantidade cair abaixo de zero. |
   | `Allow Qty Below 0 and Notify Customer` | Para aceitar backorders quando a quantidade cair abaixo de zero, e notificar o cliente que o pedido ainda pode ser feito. |

   Para obter mais informações, consulte [Configurando Backorders](backorders.md).

1. Para ativar incrementos de quantidade para o produto, defina **[!UICONTROL Enable Qty Increments]** como `Yes` e insira o número dos itens que devem ser comprados para atender à exigência no campo **[!UICONTROL Qty Increments]**.

   Por exemplo, um item vendido em incrementos de seis pode ser comprado em quantidades de 6, 12, 18 e assim por diante.

   O campo **[!UICONTROL Qty Increments]** define quantos itens de produto devem ser comprados como um único produto e como um filho de produtos configuráveis, agrupados e agrupados.

1. Quando terminar, clique em **[!UICONTROL Done]** e depois em **[!UICONTROL Save]**.

### Descrições dos campos

| Campo | Escopo | Descrição |
|--|--|--|
| [!UICONTROL Manage Stock] | Global | Determina se o controle de estoque é usado para gerenciar este produto no catálogo. Defina para habilitar ou desabilitar todos os recursos do [!DNL Inventory Management]. Quando você conclui uma devolução ou um aviso de crédito, a quantidade do produto é automaticamente retornada à quantidade de origem afetada. Talvez você queira desativar se estiver usando um sistema ERP de terceiros. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Determina o nível de estoque no qual um produto é considerado indisponível. Opções:<br />Valor positivo - Com ordens pendentes desabilitadas, insira um valor positivo.<br />Zero (0) - Com Backorders habilitados, inserir zero permite backorders infinitos.<br />Valor negativo - Com ordens pendentes habilitadas, é recomendável inserir um valor negativo. O valor é adicionado à Quantidade Venável. Por exemplo, insira `-50` para permitir pedidos até esse valor. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Determina o número mínimo do produto que pode ser comprado em um único pedido. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Global | Determina o número máximo do produto que pode ser comprado em um único pedido. |
| [!UICONTROL Qty Uses Decimals] | Global | Determina se os clientes podem usar um valor decimal em vez de um número inteiro ao inserir a quantidade solicitada. Opções:<br />`Yes` - Permite que valores sejam inseridos como decimais, em vez de números inteiros. As casas decimais são adequadas para produtos vendidos por peso, volume ou comprimento.<br />`No` - Requer que os valores de quantidade sejam inseridos como números inteiros. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Global | Determina se partes do produto podem ser enviadas separadamente. Esta opção fica visível quando **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Global | Determina como as ordens pendentes são gerenciadas. As ordens pendentes não alteram o status de processamento da ordem. Os fundos ainda são autorizados ou capturados imediatamente quando o pedido é feito, independentemente do produto estar em estoque. Os produtos são enviados à medida que ficam disponíveis. Quando ativado, é recomendável inserir um valor negativo para o Limite de indisponibilidade. Opções:<br/>`No Backorders` - Não aceita pedidos pendentes quando o produto está esgotado.<br />`Allow Qty Below 0` - Aceita ordens pendentes quando a quantidade cai abaixo de zero.<br />`Allow Qty Below 0 and Notify Customer` - Aceita ordens pendentes quando a quantidade cai abaixo de zero, mas notifica os clientes que as ordens ainda podem ser feitas. |
| [!UICONTROL Enable Qty Increments] | Global | Determina se o produto pode ser vendido em incrementos de quantidade. Os incrementos definem quantos itens de produto devem ser comprados como um único produto e como um filho de produtos configuráveis, agrupados e agrupados. |

>[!NOTE]
>
>A configuração simples de um produto substitui as configurações configuráveis de um produto específico.
