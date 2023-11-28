---
title: Adicionar um bloco dinâmico giratório
description: Apresente uma apresentação de slides de conteúdo interativo na loja adicionando vários blocos dinâmicos a um rotador.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---

# Adicionar um bloco dinâmico giratório

{{ee-feature}}

Para apresentar uma apresentação de slides de conteúdo interativo, você pode adicionar vários [blocos dinâmicos](dynamic-blocks.md) para um rotor. A variável [widget](widgets.md) A ferramenta é usada para colocar o rotor em um local específico em uma página única ou em várias páginas em toda a loja.

![Rotador de bloco dinâmico](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## Etapa 1: Criar blocos dinâmicos individuais

Para [criar os blocos dinâmicos](dynamic-blocks.md) que deseja colocar no rotador, siga estas instruções:

## Etapa 2: Adicionar um widget rotador de bloco dinâmico

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]**.

1. Em _Configurações_, definir **[!UICONTROL Type]** para `Dynamic Blocks Rotator`.

1. Escolher o atual **[!UICONTROL Design Theme]** da loja.

   Esta configuração identifica o pacote atual ou [tema](themes.md) que determina o layout da página da loja.

1. Clique em **[!UICONTROL Continue]**.

   ![Configurações do rotor de bloco dinâmico](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## Etapa 3: Conclua as opções

1. Em _Propriedades da vitrine_, defina as opções:

   - Insira um **[!UICONTROL Title]** para o rotador.

   - No **[!UICONTROL Assign to Store Views]** , selecione a [exibições de loja](../getting-started/websites-stores-views.md) onde o rotador está disponível.

   - (Opcional) Insira um **[!UICONTROL Sort Order]** número para determinar a posição do rotador no contêiner de destino. É relativo a outros widgets que podem ser atribuídos ao mesmo container.

   ![Propriedades da vitrine do girador](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. Em _Opções de layout_, clique em **[!UICONTROL Add Layout Update]** e faça o seguinte:

   - Definir **[!UICONTROL Display on]** para a página, ou o tipo de página, em que o rotador deve aparecer.

      - `Categories` - Exibe o rotor em qualquer um [âncora](../catalog/navigation-layered.md) ou páginas de categoria sem âncora. Opções: Categorias de âncora / Categorias sem âncora
      - `Products` - Exibe o rotador em um tipo específico de página do produto ou em todas as páginas do produto. Opções: todos os tipos de produtos / [Produto simples](../catalog/product-create-simple.md) /  [Produto virtual](../catalog/product-create-virtual.md) / [Produto do pacote](../catalog/product-create-bundle.md) / [Produto para download](../catalog/product-create-downloadable.md) / [Cartão-presente](../catalog/product-gift-card-create.md) / [Produto configurável](../catalog/product-create-configurable.md) / [Produto agrupado](../catalog/product-create-grouped.md)
      - `Generic Pages` - Exibe o rotador em todas as páginas, em uma página específica ou somente em páginas com um determinado layout. Opções: `All Pages` / `Specified Page` / `Page Layouts`

     No exemplo, o rotador deve ser colocado em um `Specified Page`.

   - Selecione o **[!UICONTROL Page]** onde deve aparecer o rotor.

   - Definir **[!UICONTROL Container]** à parte da [layout de página](page-layout.md#standard-page-layouts) onde deve aparecer o rotor.

     Se outros widgets forem atribuídos ao mesmo container, eles aparecerão em sequência, de acordo com a ordem de classificação.

   - Aceitar `Dynamic Block Template` como padrão **[!UICONTROL Template]**.

     Essa configuração determina o modelo usado para formatar o rotador, com base no fato de o rotador ser independente ou ser colocado dentro de texto existente.

     ![Atualizações do layout do girador](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - Clique em **[!UICONTROL Save and Continue Edit]**.

1. No painel esquerdo, escolha **[!UICONTROL Widget Options]**.

1. Para o **[!UICONTROL Dynamic Blocks to Display]**, aceitar `Specified Dynamic Blocks`.

   Esta configuração determina o tipo de blocos dinâmicos que são incluídos no rotador.

   - `Specified Dynamic Blocks` - Inclui apenas blocos dinâmicos específicos.
   - `Cart Price Rule Related` - Inclui somente blocos dinâmicos associados a uma regra de preço de carrinho.
   - `Catalog Price Rule Related` - Inclui somente blocos dinâmicos associados a uma regra de preço de catálogo.

1. Para **[!UICONTROL Restrict the Dynamic Block Types]** que pode ser usado com o widget, selecione `Content Area`.

   Essa configuração limita o banner a uma parte específica do layout da página.

   - `Content Area` - Coloca o bloco dinâmico na área de conteúdo principal da página.
   - `Footer` - Coloca o bloco dinâmico no rodapé da página.
   - `Header` - Coloca o bloco dinâmico no cabeçalho da página.
   - `Left Column` - Coloca o bloco dinâmico na coluna à esquerda do layout da página, se disponível.
   - `Right Column` - Coloca o bloco dinâmico na coluna à direita do layout da página, se disponível.

1. Definir **[!UICONTROL Rotation Mode]** a um dos seguintes:

   - `Display all instead of rotating` - Exibe uma pilha de blocos dinâmicos, onde todos são visíveis.
   - `One at a time, Random` - Exibe os blocos dinâmicos especificados em uma ordem aleatória. Quando a página é atualizada, um bloco dinâmico diferente (e aleatório) é exibido.
   - `One at the time, Series` - Exibe os blocos dinâmicos especificados na sequência em que foram adicionados. Quando a página é atualizada, o próximo bloco dinâmico na sequência é exibido.
   - `One at the time, Shuffle` - Exibe um bloco dinâmico de cada vez em uma ordem embaralhada. Essa opção é semelhante à opção `One at a time, Random` exceto que o mesmo bloco dinâmico não é repetido.

     ![Opções do widget girador](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. No **[!UICONTROL Specify Dynamic Blocks]** marque a caixa de seleção de cada bloco dinâmico que deseja incluir no rotador.

1. Quando terminar, clique em **[!UICONTROL Save]**.
