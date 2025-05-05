---
title: Entregas
description: Saiba como criar registros de remessa para faturas e cancelar remessas.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# Entregas

A grade _[!UICONTROL Shipments]_&#x200B;lista o registro de remessa de todas as faturas que foram preparadas para remessa. Um registro de remessa pode ser gerado quando um pedido é [faturado](invoices.md) ou posterior.

A Adobe Commerce e o Magento Open Source dão suporte ao envio parcial e completo do pedido, com opções adicionais disponíveis na [Inventory management](../inventory-management/introduction.md) e em extensões de terceiros.

![Grade de remessas](./assets/shipments.png){width="600" zoomable="yes"}

## Descrições da coluna

| Coluna ou controle | Descrição |
|--- |--- |
| [!UICONTROL Select] | Marque a caixa de seleção para que cada cotação esteja sujeita a uma ação ou use o controle de seleção no cabeçalho da coluna. Opções: `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | Um número sequencial exclusivo que é atribuído quando uma nova entrega é salva pela primeira vez |
| [!UICONTROL Ship Date] | Data de remessa |
| [!UICONTROL Order] | Número exclusivo do pedido |
| [!UICONTROL Order Date] | A data e a hora em que o pedido foi feito |
| [!UICONTROL Ship-to Name] | O nome da pessoa para quem a ordem é remetida |
| [!UICONTROL Total Quantity] | Quantidade total de itens a serem remetidos |
| [!UICONTROL Action] | Exibir abre a remessa no modo de edição |

{style="table-layout:auto"}

Colunas adicionais:

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Order Status] | Indica o status do pedido |
| [!UICONTROL Purchased From] | Indica o site, loja e exibição de loja onde o pedido foi feito |
| [!UICONTROL Customer Name] | O nome do cliente ou comprador que colocou a ordem |
| [!UICONTROL Email] | O endereço de email de um cliente registrado |
| [!UICONTROL Customer Group] | O nome do grupo de clientes ou catálogo compartilhado ao qual o cliente está atribuído |
| [!UICONTROL Billing Address] | O nome do cliente ou comprador que colocou a ordem |
| [!UICONTROL Shipping Address] | O nome da pessoa para quem a ordem é remetida |
| [!UICONTROL Payment Method] | O método de pagamento a ser usado para a ordem |
| [!UICONTROL Shipping Information] | O método a ser usado para enviar a ordem |

{style="table-layout:auto"}

## Criar uma remessa

As instruções a seguir orientam você no processo de criação de uma remessa no Adobe Commerce ou no Magento Open Source. Se o Inventory management estiver habilitado, talvez você queira revisar [Criar Remessas Múltiplas do Source](../inventory-management/shipments-create.md) e selecionar uma origem (ou local) e uma quantidade para enviar por item de linha.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Localize a ordem na grade e abra-a.

1. Se o pedido estiver pago, faturado e pronto para ser enviado, clique em **[!UICONTROL Ship]**.

   As seções na parte superior da entrega contêm o nome, o endereço e as informações de pagamento da ordem de venda.

1. Preencha cada seção do formulário de entrega usando as instruções nas seções a seguir.

### [!UICONTROL Items to Ship]

Para cada item de linha na ordem, modifique o **[!UICONTROL Qty to Ship]** conforme necessário.

### [!UICONTROL Shipping Information]

**Método 1:** usando a página de ordem

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Na coluna **[!UICONTROL Action]** da ordem selecionada, clique em **[!UICONTROL View]**.

1. Clique em **[!UICONTROL Ship]**.

1. Role para baixo até o bloco _[!UICONTROL Payment & Shipping Method]_&#x200B;e clique em **[!UICONTROL Add Tracking Number]**.

1. Conjunto **[!UICONTROL Carrier]**:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Para acompanhar a remessa, insira o **[!UICONTROL Title]** e **[!UICONTROL Number]**.

**Método 2:** usando a página de remessa

Esse método só será permitido se a remessa do pedido já tiver sido criada na página do pedido.
Você pode modificar as informações de remessa e rastreamento conforme necessário usando a página de remessa direta:

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Localizar e abrir a remessa no modo de edição.

1. Role para baixo até o bloco _[!UICONTROL Payment & Shipping Method]_.

1. Selecione o **[!UICONTROL Carrier]**.

1. Insira um **[!UICONTROL Title]** para o pacote.

1. Insira o rastreamento **[!UICONTROL Number]**.

1. Clique em **[!UICONTROL Add]**.

1. Para enviar um email com informações de rastreamento ao cliente, clique em **[!UICONTROL Send Tracking Information]** e confirme a ação.

   Para acompanhar a localização de qualquer remessa, abra a remessa necessária no modo de edição e clique em **[!UICONTROL Track this shipment]**.

   ![Informações de Envio e Acompanhamento](./assets/tracking-information.png){width="600" zoomable="yes"}

### Botões

| Botão | Descrição |
|--- |--- |
| **[!UICONTROL Back]** | Fecha o formulário Nova Remessa e retorna à ordem |
| **[!UICONTROL Submit Shipment]** | Adiciona a remessa do pedido. |
| **[!UICONTROL Reset]** | Restaura todos os campos aos valores originais. |

{style="table-layout:auto"}

### Comentários da remessa

1. Digite **Comentários** para a remessa, se necessário.

1. Quando a remessa estiver pronta, clique em **Enviar Remessa**.

## Configurar comentários para remessas

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Em _[!UICONTROL Sales]_, selecione **[!UICONTROL Sales Email]**.

1. Expanda a seção **Comentários da Remessa** e modifique as configurações conforme necessário:

   ![Configuração do comentário da remessa](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - A opção **[!UICONTROL Enabled]** está definida como `Yes` por padrão, o que significa que o email é enviado a um cliente quando um comentário de remessa é inserido.

   - Para **[!UICONTROL Shipment Comment Email Sender]**, selecione a pessoa da qual o email de comentário de remessa é enviado. O padrão oferece cinco endereços de email.

   - Para **[!UICONTROL Shipment Comment Email Template]**, selecione o modelo com base no seu requisito ou selecione a opção padrão.

   - Para **[!UICONTROL Shipment Comment Email Template for Guests]**, escolha o modelo usado para clientes que não têm uma conta em sua loja.

   - Para **[!UICONTROL Shipment Comment Email Copy To]**, insira os endereços de email para enviar uma cópia do email de comentário de remessa. Separe vários endereços de email com vírgula.

   - Para **[!UICONTROL Shipment Comment Email Copy Method]**, selecione `bcc` (cópia oculta) ou o método `separate email copy` de acordo com sua preferência.

1. Clique em **[!UICONTROL Save Config]**.

## Cancelar uma remessa

Antes de uma remessa ser despachada para uma transportadora, ela pode ser cancelada abrindo a ordem e navegando até a remessa, desde que a transportadora suporte cancelamentos. Algumas operadoras restringem ou limitam cancelamentos após uma reserva. Por exemplo, a UPS permite cancelamentos, mas exige que você aguarde 24 horas após a remessa ser registrada. Se uma entrega for cancelada, o cancelamento não poderá ser revertido. O único recurso é recriar a ordem.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Localize a ordem na grade.

1. Na coluna _Ação_, escolha **[!UICONTROL View]**.

1. No painel esquerdo, escolha **[!UICONTROL Shipments]**.

   Se a remessa puder ser cancelada, _[!UICONTROL Cancel Shipment]_&#x200B;aparecerá como uma opção na barra de botões superior.

1. Clique em **[!UICONTROL Cancel Shipment]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

O status da remessa é alterado para `Canceled`. Se a transportadora não suportar cancelamentos, uma mensagem de erro será exibida e explicará por que a entrega não pôde ser cancelada.

## Descrições do campo de remessa

### [!UICONTROL Shipping Information]

| Campo | Descrição |
|-----|-----------|
| [!UICONTROL Carrier] | O nome da transportadora selecionada |
| [!UICONTROL Title] | Um nome descritivo atribuído ao pacote pela operadora. |
| [!UICONTROL Number] | O número de rastreamento vinculado atribuído ao pacote. |
| [!UICONTROL Action] | ![Ícone de Lixeira](../assets/icon-delete-trashcan-solid.png) - Exclui as informações do pacote do registro de remessa. |
| [!UICONTROL Add] | Adicionar outro pacote à remessa. |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| Campo | Descrição |
|-----|-----------|
| [!UICONTROL Origin Location] | Exibe uma lista de locais disponíveis. |
| [!UICONTROL International] | Se estiver marcada, identifica a entrega como uma entrega internacional. |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| Campo | Descrição |
|-----|-----------|
| [!UICONTROL Description] | A descrição do item. |
| [!UICONTROL SKU] | A Unidade de Manutenção de Estoque do item. |
| [!UICONTROL Weight] | O peso do item. |
| [!UICONTROL Qty Ordered] | A quantidade do item que foi solicitada. |
| [!UICONTROL Qty Shipped] | A quantidade de itens que foram remetidos. |
| [!UICONTROL Qty Packed] | O número de itens incluídos neste pacote. |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| Campo | Descrição |
|-----|-----------|
| [!UICONTROL Comments] | Os comentários sobre a entrega são para uso interno. |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| Campo | Descrição |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** - Baixar o rótulo do pacote de remessa. Tamanho: A6 (105 x 148mm; 4,1 x 5,6 pol) |

{style="table-layout:auto"}
