---
title: "Configurar [!DNL Inventory Management] opções do produto"
description: Saiba como configurar o [!DNL Inventory Management] opções de configuração do produto.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# Configurar [!DNL Inventory Management] opções de produto

Essas configurações se aplicam somente ao produto editado, substituindo todas as configurações no nível global do site. Modifique essas configurações ao editar um produto, por meio da _[!UICONTROL Sources]_seção e_[!UICONTROL Advanced Inventory]_ página.

- Configurar opções do produto por origem
- Configurar opções de produto para inventário avançado

## Opções de produto por origem

Definir as quantidades e as configurações adicionais por [fonte adicionada](sources-add.md) para o produto.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra um produto no modo de edição.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Sources]** e defina as configurações do produto para cada origem:

   - Insira um **[!UICONTROL Qty]** (quantidade) valor.

   - Defina o **[!UICONTROL Source Item Status]** as `In Stock` ou `Out of Stock`.

   - Para modificar a Notificação para Quantidade Inferior por origem, desmarque ou selecione a opção **[!UICONTROL Notify Quantity Use Default]** caixa de seleção

     Se desmarcado, insira o valor do nível de estoque que aciona o aviso de falta de estoque do item. O valor inserido é subtraído da Quantidade Venável do item no nível de estoque.

     `Select to use Default` - [!DNL Commerce] verifica as opções de configurações do Inventário avançado do produto.
     `Clear to Modify` - Informe um valor para Notificar Quantidade, sobrepondo as definições de configuração do Inventário Avançado e da Loja.

   ![Seção de origens de um produto](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Done]**, depois **[!UICONTROL Save]**.

### Descrições dos campos

| Campo | Escopo | Descrição |
|--|--|--|
| [!UICONTROL Source Code] | Global | O código exclusivo de um [origem](sources-manage.md). |
| [!UICONTROL Name] | Global | O nome exclusivo de uma origem. |
| [!UICONTROL Status] | Global | O produto está ativado ou desativado no catálogo. |
| [!UICONTROL Source Item Status] | Global | Determina a disponibilidade atual do produto. Opções:<br />`In Stock` - Disponibiliza o produto para compra.<br />`Out of Stock` - A menos que Backorders sejam ativados, impede que o produto esteja disponível para compra e remove a listagem do catálogo. |
| [!UICONTROL Qty] | Global | Valores de estoque disponível para cada origem ou local. |
| [!UICONTROL Notify Quantity] | Global | Um valor para o _[!UICONTROL Notify for Quantity Below]_para esta fonte específica se_[!UICONTROL Notify Quantity Use Default]_ não está selecionado. |
| [!UICONTROL Notify Quantity Use Default] | Global | Indica o uso da configuração padrão para _[!UICONTROL Notify for Quantity Below]_no produto_[!UICONTROL Advanced Inventory]_ ou global na configuração de armazenamento. |

## Opções avançadas do produto

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra um produto no modo de edição.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Sources]** e clique em **[!UICONTROL Advanced Inventory]**.

1. Para habilitar [controle de inventário](enable.md) para o catálogo, defina **[!UICONTROL Manage Stock]** para `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] as configurações em produtos secundários substituem um produto configurável.

   ![Inventário avançado de um produto](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Insira um valor para a variável **[!UICONTROL Out-of-Stock Threshold]**:

   | Valor | Descrição |
   | ----- | ----- |
   | Valor positivo | Com _[!UICONTROL Backorders]_desabilitado, insira um valor positivo. |
   | Zero | Com _[!UICONTROL Backorders]_ativado, inserção `0` permite ordens pendentes infinitas. |
   | Valor negativo | Com _[!UICONTROL Backorders]_ativado, é recomendável inserir um valor negativo. O valor é adicionado à Quantidade Venável. Por exemplo, insira `-50` para permitir pedidos até esse valor. |

1. Insira o **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. Insira o **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. Definir **[!UICONTROL Qty uses Decimals]** para `Yes` se os clientes puderem usar um valor decimal em vez de um número inteiro ao informar a quantidade solicitada.

1. Definir **[!UICONTROL Allow Multiple Boxes for Shipping]** para `Yes` se o produto puder ser vendido separadamente, em muitas caixas. Essa opção estará visível quando **[!UICONTROL Qty Uses Decimals]** está definida como `Yes` somente.

1. Definir **[!UICONTROL Backorders]** a um dos seguintes:

   | Opção | Descrição |
   | ----- | ----- |
   | `No Backorders` | Para não aceitar pedidos pendentes quando o produto estiver indisponível. |
   | `Allow Qty Below 0` | Para aceitar backorders quando a quantidade cair abaixo de zero. |
   | `Allow Qty Below 0 and Notify Customer` | Para aceitar backorders quando a quantidade cair abaixo de zero, e notificar o cliente que o pedido ainda pode ser feito. |

   Para obter mais informações, consulte [Configurando Backorders](backorders.md).

1. Para ativar incrementos de quantidade para o produto, defina **[!UICONTROL Enable Qty Increments]** para `Yes` e insira o número de itens que devem ser comprados para atender ao requisito na **[!UICONTROL Qty Increments]** campo.

   Por exemplo, um item vendido em incrementos de seis pode ser comprado em quantidades de 6, 12, 18 e assim por diante.

   **[!UICONTROL Qty Increments]** O campo define quantos itens de produto devem ser comprados como um único produto e como um filho de produtos configuráveis, agrupados e agrupados.

1. Quando terminar, clique em **[!UICONTROL Done]** e depois **[!UICONTROL Save]**.

### Descrições dos campos

| Campo | Escopo | Descrição |
|--|--|--|
| [!UICONTROL Manage Stock] | Global | Determina se o controle de estoque é usado para gerenciar este produto no catálogo. Definir para habilitar ou desabilitar tudo [!DNL Inventory Management] recursos. Quando você conclui uma devolução ou um aviso de crédito, a quantidade do produto é automaticamente retornada à quantidade de origem afetada. Talvez você queira desativar se estiver usando um sistema ERP de terceiros. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Determina o nível de estoque no qual um produto é considerado indisponível. Opções:<br />Valor positivo - Com ordens pendentes desativadas, informe um valor positivo.<br />Zero (0) - Com backorders ativadas, inserir zero permite backorders infinitos.<br />Valor negativo - Com ordens pendentes ativadas, é recomendável informar uma quantia negativa. O valor é adicionado à Quantidade Venável. Por exemplo, insira `-50` para permitir pedidos até esse valor. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Determina o número mínimo do produto que pode ser comprado em um único pedido. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Global | Determina o número máximo do produto que pode ser comprado em um único pedido. |
| [!UICONTROL Qty Uses Decimals] | Global | Determina se os clientes podem usar um valor decimal em vez de um número inteiro ao inserir a quantidade solicitada. Opções:<br />`Yes` - Permite que os valores sejam inseridos como decimais, em vez de números inteiros. As casas decimais são adequadas para produtos vendidos por peso, volume ou comprimento.<br />`No` - Exige que os valores de quantidade sejam inseridos como números inteiros. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Global | Determina se partes do produto podem ser enviadas separadamente. Essa opção estará visível quando **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Global | Determina como as ordens pendentes são gerenciadas. As ordens pendentes não alteram o status de processamento da ordem. Os fundos ainda são autorizados ou capturados imediatamente quando o pedido é feito, independentemente do produto estar em estoque. Os produtos são enviados à medida que ficam disponíveis. Quando ativado, é recomendável inserir um valor negativo para o Limite de indisponibilidade. Opções:<br/>`No Backorders` - Não aceita pedidos pendentes quando o produto está esgotado.<br />`Allow Qty Below 0` - Aceita ordens pendentes quando a quantidade cai abaixo de zero.<br />`Allow Qty Below 0 and Notify Customer` - Aceita backorders quando a quantidade cai abaixo de zero, mas notifica os clientes que os pedidos ainda podem ser feitos. |
| [!UICONTROL Enable Qty Increments] | Global | Determina se o produto pode ser vendido em incrementos de quantidade. Os incrementos definem quantos itens de produto devem ser comprados como um único produto e como um filho de produtos configuráveis, agrupados e agrupados. |

>[!NOTE]
>
>A configuração simples de um produto substitui as configurações configuráveis de um produto específico.
