---
title: Widget de Pedidos e devoluções
description: Saiba como usar o widget pedidos e devoluções para fornecer aos clientes a capacidade de verificar o status de seus pedidos, imprimir faturas e rastrear as remessas.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Widget de Pedidos e devoluções

A variável _Pedidos e Devoluções_ O widget oferece aos convidados a capacidade de verificar o status de seus pedidos, imprimir faturas e rastrear remessas. Quando o widget é adicionado à loja, ele fica visível apenas para convidados e clientes que não estão conectados às suas contas. Os convidados podem encontrar pedidos fornecendo a ID do pedido, o sobrenome de faturamento e o endereço de email ou código postal.

![Widget de Pedidos e devoluções na barra lateral na loja](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## O widget Pedidos e devoluções na loja

1. O cliente pode usar o **[!UICONTROL Find Order By]** opção para escolher um dos seguintes parâmetros a serem usados para localizar a ordem:

   - Endereço de e-mail
   - Código postal

1. O cliente informa o **[!UICONTROL Order ID]** e **[!UICONTROL Billing Last Name]**.

1. Insere o faturamento **[!UICONTROL Email Address]** ou **[!UICONTROL ZIP Code]** que está associado ao pedido.

1. Cliques **[!UICONTROL Search]** para recuperar o pedido.

   ![Informações do pedido exibidas na vitrine](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Configurar o dispositivo de Pedidos e Devoluções

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]**.

1. No _[!UICONTROL Settings]_faça o seguinte:

   - Definir **[!UICONTROL Type]** para `Orders and Returns`.

   - Escolha o **[!UICONTROL Design Theme]** que é usado pela loja.

1. Clique em **[!UICONTROL Continue]**.

1. No _[!UICONTROL Storefront Properties]_faça o seguinte:

   - Para **[!UICONTROL Widget Title]**, insira um título descritivo para o widget.

     Este título é visível somente do Administrador.

   - Para **[!UICONTROL Assign to Store Views]**, selecione as exibições de loja onde o widget está visível.

     Você pode selecionar uma visualização de loja específica, ou `All Store Views`. Para selecionar várias exibições, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

   - (Opcional) Para **[!UICONTROL Sort Order]**, insira um número para determinar a ordem em que esse item aparece com outros na mesma parte da página. (`0` = primeiro, `1` = segundo, `3` = terceiro e assim por diante.)

1. No _[!UICONTROL Layout Updates]_clique em **[!UICONTROL Add Layout Update]**e faça o seguinte:

   - Definir **[!UICONTROL Display On]** ao tipo de página em que você deseja que o widget apareça.

   - Para determinar onde o widget é exibido na página, preencha o restante das informações de atualização do layout.

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado a atualizar o cache, clique no link na mensagem na parte superior da página e siga as instruções.
