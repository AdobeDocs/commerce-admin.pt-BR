---
title: Novo widget da lista de produtos
description: Saiba como usar o novo widget lista de produtos para exibir uma lista dos produtos adicionados mais recentemente.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Novo widget da lista de produtos

A lista de novos produtos é um exemplo de conteúdo dinâmico e consiste em dados em tempo real extraídos do catálogo de produtos. Por padrão, a lista _Novos produtos_ inclui os primeiros oito dos produtos adicionados mais recentemente. No entanto, também pode ser configurado para incluir apenas produtos em um intervalo de datas especificado.

![Nova lista de produtos na home page da loja](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Etapa 1: definir cada produto como novo

![Magento Open Source](../assets/open-source.svg) Esta etapa se aplica somente ao Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg) Para lojas Adobe Commerce, consulte [Agendando uma Atualização](content-staging-scheduled-update.md) e prossiga para a Etapa 2 nesta página.

A configuração de intervalo de datas _[!UICONTROL Set Product as New]_&#x200B;pode ser definida somente em atualizações agendadas.

Configurar um produto como novo adiciona o produto à lista _Novos produtos_. Você pode alterar a configuração de volta a qualquer momento quando não quiser mais incluí-la na lista.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Encontre cada produto que deseja incluir no recurso e abra-o no modo de edição.

1. Para **[!UICONTROL Set Product as New]**, alterne a opção para definir o produto como um novo produto ou não.

   ![Definindo o produto como novo](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando for solicitado que você reindexe e atualize o cache da página, clique nos links na parte superior da página e siga as instruções.

## Etapa 2: criar o widget

O código que determina o conteúdo da lista Novos produtos e sua colocação na loja é gerado pela ferramenta Widget.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]**.

1. Na seção _[!UICONTROL Settings]_, faça o seguinte:

   - Defina **[!UICONTROL Type]** como `Catalog New Products List`.

   - Escolha o **[!UICONTROL Design Theme]** que é usado pelo armazenamento.

1. Clique em **[!UICONTROL Continue]**.

   ![Configurações do novo widget lista de produtos](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Na seção _[!UICONTROL Storefront Properties]_, faça o seguinte:

   - Para **[!UICONTROL Widget Title]**, insira um título descritivo para o widget. (Este título é visível somente do _Administrador_.)

   - Para **[!UICONTROL Assign to Store Views]**, selecione as exibições de loja nas quais o widget está visível.

     Você pode selecionar um modo de exibição de loja específico ou `All Store Views`. Para selecionar várias exibições, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

   - (Opcional) Para **[!UICONTROL Sort Order]**, insira um número para determinar a ordem de exibição deste item com outros na mesma parte da página. (`0` = primeiro, `1` = segundo, `3` = terceiro e assim por diante.)

   ![Atualizações de layout](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## Etapa 3: Escolher o local

1. Na seção _[!UICONTROL Layout Updates]_, clique em **[!UICONTROL Add Layout Update]**.

1. Configurar **[!UICONTROL Display On]** para `Specified Page.`

1. Defina **[!UICONTROL Page]** como `CMS Home Page`.

1. Defina **[!UICONTROL Block Reference]** como `Main Content Area`.

1. Defina **[!UICONTROL Template]** como um dos seguintes:

   - `New Product List Template`
   - `New Products Grid Template`

     ![Atualizações de layout](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save and Continue Edit]**.

   Por enquanto, você pode ignorar a mensagem para atualizar o cache.

## Etapa 4: configurar a lista

1. No painel esquerdo, escolha **[!UICONTROL Widget Options]**.

1. Defina **[!UICONTROL Display Products]** como um dos seguintes:

   - `All Products` - Lista produtos em sequência, começando com os adicionados mais recentemente.
   - `New Products` - Lista somente os produtos identificados como _novos_. Um produto é considerado novo durante o período especificado em _[!UICONTROL Set Product As New From/To]_. A lista fica vazia se o intervalo de datas expirar sem nenhum produto novo definido.

1. Para fornecer controle de navegação para listas com várias páginas, defina **[!UICONTROL Display Page Control]** como `Yes`.

   Para **[!UICONTROL Number of Products per Page]**, insira o número de produtos que você deseja exibir em cada página.

1. Defina a opção **[!UICONTROL Number of Products to Display]** com o número de novos produtos que deseja incluir na lista.

   A configuração padrão é `10`.

1. Para **[!UICONTROL Cache Lifetime (Seconds)]**, escolha a frequência com que deseja atualizar a lista de novos produtos.

   Por padrão, o cache é definido como 86.400 segundos (24 horas).

   ![Opções de widget](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado a atualizar o cache, clique no link na mensagem na parte superior da página e siga as instruções.

## Etapa 5: visualizar seu trabalho

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Localize a página na grade onde a lista _Novos Produtos_ deve aparecer e clique no link **[!UICONTROL Preview]** na coluna _[!UICONTROL Action]_.
