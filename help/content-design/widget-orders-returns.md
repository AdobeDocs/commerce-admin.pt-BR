---
title: Widget de Pedidos e devoluções
description: Saiba como usar o widget pedidos e devoluções para fornecer aos clientes a capacidade de verificar o status de seus pedidos, imprimir faturas e rastrear as remessas.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Widget de Pedidos e devoluções

O widget _Pedidos e devoluções_ oferece aos convidados a capacidade de verificar o status de seus pedidos, imprimir faturas e rastrear as remessas. Quando o widget é adicionado à loja, ele fica visível apenas para convidados e clientes que não estão conectados às suas contas. Os convidados podem encontrar pedidos fornecendo a ID do pedido, o sobrenome de faturamento e o endereço de email ou código postal.

![Widget de Pedidos e Devoluções na barra lateral na vitrine](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## O widget Pedidos e devoluções na loja

1. O cliente pode usar a opção **[!UICONTROL Find Order By]** para escolher um dos seguintes parâmetros a serem usados para localizar a ordem:

   - Endereço de e-mail
   - Código postal

1. O cliente insere o **[!UICONTROL Order ID]** e **[!UICONTROL Billing Last Name]**.

1. Insere o faturamento **[!UICONTROL Email Address]** ou **[!UICONTROL ZIP Code]** que está associado ao pedido.

1. Clica em **[!UICONTROL Search]** para recuperar a ordem.

   ![Informações do pedido exibidas na loja](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Configurar o dispositivo de Pedidos e Devoluções

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]**.

1. Na seção _[!UICONTROL Settings]_, faça o seguinte:

   - Defina **[!UICONTROL Type]** como `Orders and Returns`.

   - Escolha o **[!UICONTROL Design Theme]** que é usado pelo armazenamento.

1. Clique em **[!UICONTROL Continue]**.

1. Na seção _[!UICONTROL Storefront Properties]_, faça o seguinte:

   - Para **[!UICONTROL Widget Title]**, insira um título descritivo para o widget.

     Este título é visível somente do Administrador.

   - Para **[!UICONTROL Assign to Store Views]**, selecione as exibições de loja nas quais o widget está visível.

     Você pode selecionar um modo de exibição de loja específico ou `All Store Views`. Para selecionar várias exibições, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

   - (Opcional) Para **[!UICONTROL Sort Order]**, insira um número para determinar a ordem de exibição deste item com outros na mesma parte da página. (`0` = primeiro, `1` = segundo, `3` = terceiro e assim por diante.)

1. Na seção _[!UICONTROL Layout Updates]_, clique em **[!UICONTROL Add Layout Update]**&#x200B;e faça o seguinte:

   - Defina **[!UICONTROL Display On]** como o tipo de página em que você deseja que o widget apareça.

   - Para determinar onde o widget é exibido na página, preencha o restante das informações de atualização do layout.

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado a atualizar o cache, clique no link na mensagem na parte superior da página e siga as instruções.
