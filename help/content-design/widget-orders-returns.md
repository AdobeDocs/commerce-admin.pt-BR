---
title: Widget de Pedidos e devoluções
description: Saiba como usar o widget pedidos e devoluções para fornecer aos clientes a capacidade de verificar o status de seus pedidos, imprimir faturas e rastrear as remessas.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/jWpFWPBwvKr5EnMXdV5-3zAqagGuzPrvOL6-gMiEw-M
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 382
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
