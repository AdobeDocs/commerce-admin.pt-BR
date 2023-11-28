---
title: Configurar listas de desejos
description: Saiba como configurar a funcionalidade da lista de desejos para seus clientes da loja.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Configurar listas de desejos

A configuração da lista de desejos ativa as listas de desejos e determina o modelo de email e o remetente de mensagens de email que são usadas quando uma lista de desejos é compartilhada.

## Ativar funcionalidade da lista de desejos

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Wish List]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL General Options]** e faça o seguinte:

   ![Configuração dos clientes - configurações gerais da lista de desejos](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Alternar **[!UICONTROL Enabled]** para `Yes`, que ativa o módulo da lista de desejos para a loja.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Alternar **[!UICONTROL Enable Multiple Wish Lists]** para `Yes`, que permite aos clientes criar e manter várias listas de desejos.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente no Adobe Commerce) Para limitar o número de listas de desejos que os clientes podem ter associados à sua conta, insira um valor para **[!UICONTROL Number of Multiple Wish Lists]**.

   - Alternar **[!UICONTROL Show in Sidebar]** para `Yes`, que exibe as listas de desejos na barra lateral.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Share Options]** e faça o seguinte:

   ![Configuração dos clientes - opções de compartilhamento da lista de desejos](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Defina o **[!UICONTROL Email Sender]** ao contato da loja que deve aparecer como remetente da mensagem. Opções: Contato Geral, Representante De Vendas, Suporte Ao Cliente, E-Mail Personalizado.

   - Defina o **[!UICONTROL Email Template]** a ser usado quando um cliente compartilha uma lista de desejos.

   - Para limitar o número total de emails que um cliente pode enviar, insira um **[!UICONTROL Max Emails Allowed to be Sent]** valor. O padrão é 10 e o máximo permitido é 10.000.

   - Para limitar o tamanho da mensagem, insira o valor de **[!UICONTROL Email Text Length Limit]**. O padrão é 255.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL My Wish List Link]** seção e definir **[!UICONTROL Display Wish List Summary]** a um dos seguintes:

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Configuração do cliente - exibição da lista de desejos](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Adicionar pesquisa da lista de desejos

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce)

Qualquer lista de desejos pública pode ser encontrada usando a Pesquisa de lista de desejos [widget](../content-design/widgets.md). O widget permite que um cliente pesquise pelo nome ou endereço de email do proprietário da lista de desejos. Os clientes da loja podem encontrar listas de desejos que pertencem a outros clientes, visualizá-las e solicitar produtos deles ou adicionar os produtos a suas próprias listas de desejos. Se um item for comprado de uma lista pública de desejos por outro cliente, ele não será removido da lista original de desejos. A variável _Pesquisa na lista de desejos_ o widget pode ser adicionado a qualquer página da sua loja para facilitar a localização das listas de desejos de amigos e familiares.

![Exemplo de vitrine - pesquisa da lista de desejos](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]**.

1. No _[!UICONTROL Settings]_faça o seguinte:

   - Definir **[!UICONTROL Type]** para `Wish List Search`.

   - Definir **[!UICONTROL Design Theme]** ao tema do armazenamento onde a lista de desejos é adicionada.

   - Clique em **[!UICONTROL Continue]**.

1. Conclua o _[!UICONTROL Storefront Properties]_:

   - Insira o **[!UICONTROL Widget Title]**.

   - Definir **[!UICONTROL Assign to Store Views]** para a exibição ou site onde o widget deve ser usado.

   - Para **[!UICONTROL Sort Order]**, insira um número para determinar o posicionamento do widget em seu container.

     `0` = first (default), `1` = segundo, `2` = terceiro e assim por diante.

1. No _[!UICONTROL Layout Updates]_clique em **[!UICONTROL Add Layout Update]**e defina **[!UICONTROL Display on]**a um dos seguintes:

   - _[!UICONTROL Categories]_

      - `Anchor Categories`
      - `Non-Anchor Categories`

   - _[!UICONTROL Products]_

      - `All Product Type`
      - `Simple Product`
      - `Virtual Product`
      - `Bundle Product`
      - `Configurable Product`
      - `Downloadable Product`
      - `Gift Card`
      - `Grouped Product`

   - _[!UICONTROL Generic Page]_

      - `All Pages`
      - `Specified Page`
      - `Page Layouts`

1. No **[!UICONTROL Container]** escolha a área do layout da página onde ele será colocado.

   ![Widget de pesquisa da lista de desejos - layout](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. No painel esquerdo, escolha **[!UICONTROL Widget Options]**.

1. Definir **[!UICONTROL Quick Search Form Types]** a um dos seguintes:

   - `All Forms` - Os clientes podem pesquisar por todos os parâmetros disponíveis.
   - `Owner Name` - Os clientes podem pesquisar listas de desejos por nome de proprietário.
   - `Owner Email` - Os clientes podem pesquisar listas de desejos por endereço de email do proprietário.

   >[!NOTE]
   >
   >Os endereços de envio não estão incluídos nas listas de desejos.

1. Configure quaisquer propriedades remanescentes do widget, conforme necessário, seguindo o padrão [instruções](../content-design/widget-create.md).

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado, atualize todos os caches inválidos.
