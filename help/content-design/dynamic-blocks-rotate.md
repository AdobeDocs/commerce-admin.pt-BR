---
title: Adicionar um bloco dinâmico giratório
description: Apresente uma apresentação de slides de conteúdo interativo na loja adicionando vários blocos dinâmicos a um rotador.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# Adicionar um bloco dinâmico giratório

{{ee-feature}}

Para apresentar uma apresentação de slides de conteúdo interativo, você pode adicionar vários [blocos dinâmicos](dynamic-blocks.md) a um rotador. A ferramenta [widget](widgets.md) é usada para colocar o rotor em um local específico em uma página única ou em várias páginas em toda a loja.

![Rotador de bloco dinâmico](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## Etapa 1: Criar blocos dinâmicos individuais

Para [criar os blocos dinâmicos](dynamic-blocks.md) que você deseja colocar no rotor, siga estas instruções:

## Etapa 2: Adicionar um widget rotador de bloco dinâmico

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]**.

1. Em _Configurações_, defina **[!UICONTROL Type]** como `Dynamic Blocks Rotator`.

1. Escolha o **[!UICONTROL Design Theme]** atual do armazenamento.

   Esta configuração identifica o pacote atual ou o [tema](themes.md) que determina o layout da página do armazenamento.

1. Clique em **[!UICONTROL Continue]**.

   ![Configurações do rotor de bloco dinâmico](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## Etapa 3: Conclua as opções

1. Em _Propriedades da vitrine_, defina as opções:

   - Insira um **[!UICONTROL Title]** para o rotor.

   - Na lista **[!UICONTROL Assign to Store Views]**, selecione as [exibições de loja](../getting-started/websites-stores-views.md) onde o rotor está disponível.

   - (Opcional) Insira um número **[!UICONTROL Sort Order]** para determinar a posição do rotor no contêiner de destino. É relativo a outros widgets que podem ser atribuídos ao mesmo container.

   ![Propriedades da vitrine do rotador](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. Em _Opções de Layout_, clique em **[!UICONTROL Add Layout Update]** e faça o seguinte:

   - Defina **[!UICONTROL Display on]** como a página, ou tipo de página, em que o rotador deve aparecer.

      - `Categories` - Exibe o rotor em [âncora](../catalog/navigation-layered.md) ou páginas de categoria sem âncora. Opções: Categorias de âncora / Categorias sem âncora
      - `Products` - Exibe o rotor em um tipo específico de página do produto ou em todas as páginas do produto. Opções: Todos os Tipos de Produto / [Produto Simples](../catalog/product-create-simple.md) / [Produto Virtual](../catalog/product-create-virtual.md) / [Produto Pacote](../catalog/product-create-bundle.md) / [Produto Baixável](../catalog/product-create-downloadable.md) / [Cartão-presente](../catalog/product-gift-card-create.md) / [Produto Configurável](../catalog/product-create-configurable.md) / [Produto Agrupado](../catalog/product-create-grouped.md)
      - `Generic Pages` - Exibe o rotor em todas as páginas, em uma página específica ou somente em páginas com um determinado layout. Opções: `All Pages` / `Specified Page` / `Page Layouts`

     No exemplo, o rotor deve ser colocado em um `Specified Page`.

   - Selecione o **[!UICONTROL Page]** específico onde o rotor deve aparecer.

   - Defina **[!UICONTROL Container]** como a parte do [layout de página](page-layout.md#standard-page-layouts) onde o rotador deve aparecer.

     Se outros widgets forem atribuídos ao mesmo container, eles aparecerão em sequência, de acordo com a ordem de classificação.

   - Aceitar `Dynamic Block Template` como o **[!UICONTROL Template]** padrão.

     Essa configuração determina o modelo usado para formatar o rotador, com base no fato de o rotador ser independente ou ser colocado dentro de texto existente.

     ![Atualizações do layout do Girador](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - Clique em **[!UICONTROL Save and Continue Edit]**.

1. No painel esquerdo, escolha **[!UICONTROL Widget Options]**.

1. Para **[!UICONTROL Dynamic Blocks to Display]**, aceite `Specified Dynamic Blocks`.

   Esta configuração determina o tipo de blocos dinâmicos que são incluídos no rotador.

   - `Specified Dynamic Blocks` - Inclui somente blocos dinâmicos específicos.
   - `Cart Price Rule Related` - Inclui somente blocos dinâmicos associados a uma regra de preço de carrinho.
   - `Catalog Price Rule Related` - Inclui somente blocos dinâmicos associados a uma regra de preço de catálogo.

1. Para **[!UICONTROL Restrict the Dynamic Block Types]** que pode ser usado com o widget, selecione `Content Area`.

   Essa configuração limita o banner a uma parte específica do layout da página.

   - `Content Area` - Coloca o bloco dinâmico na área de conteúdo principal da página.
   - `Footer` - Coloca o bloco dinâmico no rodapé da página.
   - `Header` - Coloca o bloco dinâmico no cabeçalho da página.
   - `Left Column` - Coloca o bloco dinâmico na coluna esquerda do layout da página, se disponível.
   - `Right Column` - Coloca o bloco dinâmico na coluna direita do layout da página, se disponível.

1. Defina **[!UICONTROL Rotation Mode]** como um dos seguintes:

   - `Display all instead of rotating` - Exibe uma pilha de blocos dinâmicos, onde todos estão visíveis.
   - `One at a time, Random` - Exibe os blocos dinâmicos especificados em uma ordem aleatória. Quando a página é atualizada, um bloco dinâmico diferente (e aleatório) é exibido.
   - `One at the time, Series` - Exibe os blocos dinâmicos especificados na sequência em que foram adicionados. Quando a página é atualizada, o próximo bloco dinâmico na sequência é exibido.
   - `One at the time, Shuffle` - Exibe um bloco dinâmico de cada vez em uma ordem embaralhada. Esta opção é semelhante à opção `One at a time, Random`, exceto que o mesmo bloco dinâmico não é repetido.

     ![Opções do widget Rotador](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. Na grade **[!UICONTROL Specify Dynamic Blocks]**, marque a caixa de seleção de cada bloco dinâmico que deseja incluir no rotor.

1. Quando terminar, clique em **[!UICONTROL Save]**.
