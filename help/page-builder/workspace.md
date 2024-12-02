---
title: Workspace [!DNL Page Builder]
description: Saiba mais sobre as ferramentas disponíveis no  [!DNL Page Builder] espaço de trabalho ao criar páginas básicas, páginas de produtos e catálogos, blocos e blocos dinâmicos.
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# Workspace [!DNL Page Builder]

Quando [[!DNL Page Builder] está habilitado](setup.md), a seção _[!UICONTROL Content]_e o processo de criação de conteúdo são modificados para aproveitar as ferramentas [!DNL Page Builder] avançadas para páginas [do CMS](../content-design/page-add.md), [produtos](../catalog/product-content.md) e [categorias](../catalog/categories-content-settings.md), [blocos](../content-design/block-add.md) e [blocos dinâmicos](../content-design/dynamic-blocks.md). Esta seção inclui um campo_ Cabeçalho do Conteúdo _, uma visualização do conteúdo e acesso fácil ao espaço de trabalho [!DNL Page Builder] em tela cheia.

![Seção de conteúdo com [!DNL Page Builder] visualização](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## Cabeçalho do conteúdo

Como os mecanismos de pesquisa procuram cabeçalhos de nível um (H1), adicionar um cabeçalho de nível um é uma maneira fácil de garantir que a página seja indexada corretamente.

>[!NOTE]
>
>O campo _[!UICONTROL Content Heading]_exibido na parte superior da página é um campo herdado que oferece suporte ao conteúdo criado com versões anteriores do [!DNL Commerce]. No entanto, ele não faz parte de [!DNL Page Builder]. O [!UICONTROL Content Heading] é formatado como um cabeçalho H1 de acordo com a folha de estilos associada ao tema atual. Ele está posicionado logo acima da área de conteúdo ativa definida pelo estágio [!DNL Page Builder].

Para obter o melhor controle sobre o posicionamento e o formato dos cabeçalhos de todos os níveis, é recomendável deixar o campo _[!UICONTROL Content Heading]_vazio e usar o tipo de conteúdo [!DNL Page Builder] [Cabeçalho](heading.md).

![Cabeçalho do conteúdo e outros cabeçalhos](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## Visualização

Quando você expande a seção _[!UICONTROL Content]_e há conteúdo existente criado com [!DNL Page Builder], ela exibe uma visualização do conteúdo como ele apareceria em uma página. Clique em **[!UICONTROL Edit with Page Builder]**ou dentro da área de visualização de conteúdo para abrir o espaço de trabalho [!DNL Page Builder], onde você pode fazer as atualizações necessárias.

![Visualização da descrição do produto](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Para os formulários de produto e categoria, essa pré-visualização de conteúdo é habilitada por padrão, mas pode ser desabilitada. Se o desempenho for afetado pelo carregamento da visualização, você poderá desabilitar a visualização nas configurações de [Gerenciamento de conteúdo](../configuration-reference/general/content-management.md#advanced-content-tools).

## Estágio

Ao abrir o espaço de trabalho [!DNL Page Builder] a partir da visualização, o estágio é a área de trabalho principal onde você pode criar e formatar conteúdo e até fazer edições rápidas no conteúdo ativo. O estágio está inicialmente vazio, fornecendo a superfície de design onde você pode arrastar linhas, colunas e guias do painel esquerdo.

>[!NOTE]
>
>A partir da versão 2.4.1, a edição de conteúdo agora é em tela cheia apenas para todas as áreas controladas pelo [!DNL Page Builder] — páginas do CMS, páginas de produto e categoria, blocos e blocos dinâmicos. A edição em tela cheia coloca o foco no conteúdo e fornece uma visualização que melhor corresponde à experiência do usuário na loja.

![Preparar com conteúdo de página](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Visores

Um _viewport_ é a área visível de uma página da Web que um usuário vê. No modo de design de tela cheia, os botões de visor são exibidos acima do estágio [!DNL Page Builder] para mostrar o conteúdo conforme o usuário do site o vê na loja.

![Botões Viewport](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder] também define pontos de interrupção para visores. Os pontos de interrupção definem as larguras mínimas e máximas nas quais determinados estilos são aplicados. As janelas de visualização [!DNL Page Builder] fornecem os seguintes pontos de interrupção de conteúdo:

- **Ponto de interrupção da área de trabalho**—`min-width: 1024px`. Esse ponto de interrupção aplica estilos definidos para larguras de visor de 1024 pixels ou mais.
- **Pontos de interrupção móveis**—`max-width: 768px, min-width: 640px`. Esses pontos de interrupção aplicam estilos definidos para larguras de visor entre 768 e 640 pixels.

[!DNL Page Builder] visores fornecem dois recursos: **_visualizações de conteúdo_** e **_configurações de ponto de interrupção_**.

### Visualizações de conteúdo

Por padrão, [!DNL Page Builder] fornece duas visualizações de visor:

- **Área de Trabalho** — Exibe a visualização do conteúdo sem uma largura predefinida. Estilos definidos pela área de trabalho (usando a largura mínima do ponto de interrupção de 1024 pixels) ainda são aplicados à página. Mas a largura da janela de visualização da área de trabalho é definida pelas configurações para tipos de conteúdo de contêiner, como Linhas. A seleção da janela de visualização do desktop mostra como o conteúdo é estilizado na loja quando a largura da página do navegador é de 1024 pixels e mais.

  ![Visualização do viewport da área de trabalho com largura mínima de 1024 pixels](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **Dispositivo móvel** — Exibe a visualização de conteúdo em uma largura predefinida de 768 pixels. Ao contrário do visor desktop, o visor móvel mostra o conteúdo da página com uma largura de 768 pixels, juntamente com os estilos definidos para as larguras de ponto de interrupção de 768 pixels (máximo) e 640 pixels (mínimo).

  ![Visualização do viewport móvel com largura mínima de 768 pixels](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### Configurações de ponto de interrupção

Os botões visor também fornecem a opção para aplicar diferentes estilos de ponto de interrupção a tipos de conteúdo com base no visor selecionado. Por padrão, o [!DNL Page Builder] fornece configurações de ponto de interrupção para os campos _[!UICONTROL Minimum Height]_de Linhas, Colunas, Guias, Itens de Guia, Banners, Controles Deslizantes e Slides. Ao selecionar a janela de visualização móvel e abrir o editor para um desses tipos de conteúdo, você pode inserir valores de campo específicos para os pontos de interrupção da janela de visualização móvel. Os campos de tipo de conteúdo que permitem configurações específicas de ponto de interrupção exibem um ícone à direita do campo, semelhante ao exemplo a seguir para uma Linha:

![Indicador de ícone para configuração de ponto de interrupção](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"}

## Painel

O painel [!DNL Page Builder] está localizado à esquerda do estágio e contém tipos de conteúdo que podem ser arrastados para o estágio. Um contêiner específico ao tipo de conteúdo é exibido com uma caixa de ferramentas de opções. Os tipos de conteúdo são organizados no painel da seguinte maneira:

### Layout

A seção _[!UICONTROL Layout]_do painel [!DNL Page Builder] é usada para adicionar linhas, colunas ou guias ao estágio. Ao arrastar um tipo de conteúdo do painel para o estágio, um contêiner é exibido com uma caixa de ferramentas de opções específicas ao tipo de conteúdo.

Por padrão, o estágio [!DNL Page Builder] está vazio. Ao arrastar tipos de conteúdo de layout do painel para o palco, você pode colocá-los acima, abaixo ou dentro de outros contêineres de layout na página. As linhas só podem ser adicionadas diretamente ao estágio.

Painel ![[!DNL Page Builder] com tipos de conteúdo de layout e estágio](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}

| Tipo de conteúdo de layout | Descrição |
| ------------------- |------------ |
| [Linha](row.md) | Uma nova linha só pode ser arrastada do painel para o estágio e posicionada acima ou abaixo de outra linha, guia ou grupo de colunas. Também é possível usar a opção Duplicate para fazer uma cópia de uma linha existente. |
| [Coluna](column.md) | Uma coluna pode ser arrastada do painel para o palco ou para linhas e guias. O número máximo de colunas que podem ser adicionadas é determinado pelo número de divisões de grade especificado na [configuração](setup.md). |
| [Guias](tabs.md) | Uma única guia pode ser arrastada do painel para o palco ou para linhas e colunas. Guias adicionais podem ser adicionadas na caixa de ferramentas. |

{style="table-layout:auto"}

### Elementos

Use a seção _[!UICONTROL Elements]_do painel [!DNL Page Builder] para adicionar texto, cabeçalhos, botões, divisores e código HTML a qualquer contêiner de layout no [[!DNL Page Builder] estágio](workspace.md#stage). Ao arrastar um tipo de conteúdo do painel para uma linha ou coluna, ou para um conjunto de guias no palco, um container é exibido. Use a caixa de ferramentas de tipo de conteúdo para acessar as configurações específicas do tipo.

Painel ![[!DNL Page Builder] com tipos de conteúdo de Elemento](./assets/pb-elements.png){width="600" zoomable="yes"}

| Tipo de conteúdo do elemento | Descrição |
| -------------------- | ----------- |
| [Texto](text.md) | Adiciona um contêiner de texto e um editor ao estágio. |
| [Cabeçalho](heading.md) | Adiciona um contêiner de cabeçalho ao estágio. |
| [Botões](buttons.md) | Adiciona um contêiner a um botão individual ou a um conjunto de botões ao estágio. |
| [Divisor](divider.md) | Adiciona um contêiner de um divisor ao estágio. |
| [Código HTML](html-code.md) | Adiciona um contêiner para código HTML ao estágio. |

{style="table-layout:auto"}

### Mídia

Use a seção _[!UICONTROL Media]_do painel [!DNL Page Builder] para adicionar imagens, vídeo, banners, controles deslizantes e [!DNL Google Maps] a qualquer contêiner de layout no [[!DNL Page Builder] estágio](workspace.md#stage). Quando um tipo de conteúdo de mídia é arrastado do painel para o palco, um container é exibido com uma caixa de ferramentas de opções específicas ao tipo de conteúdo.

Painel ![[!DNL Page Builder] com tipos de conteúdo de mídia](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| Tipo de conteúdo de mídia | Descrição |
| ------------------- | ------------------------------------------ |
| [Imagem](image.md) | Adiciona um contêiner de imagem ao estágio. |
| [Vídeo](video.md) | Adiciona um contêiner de vídeo ao estágio. |
| [Banner](banner.md) | Adiciona um contêiner de banner ao estágio. |
| [Controle deslizante](slider.md) | Adiciona um contêiner de controle deslizante ao estágio. |
| [Mapa](map.md) | Adiciona um contêiner [!DNL Google Maps] ao estágio. |

{style="table-layout:auto"}

### Adicionar conteúdo

Use a seção _[!UICONTROL Add Content]_do painel [!DNL Page Builder] para adicionar conteúdo existente ao [[!DNL Page Builder] estágio](workspace.md#stage). Quando você arrasta um tipo de conteúdo de mídia do painel para o palco, um container é exibido. Use a caixa de ferramentas de tipo de conteúdo para acessar as_ Configurações _específicas do tipo.

Painel ![[!DNL Page Builder] com Adicionar tipos de conteúdo](./assets/pb-add-content.png){width="600" zoomable="yes"}

| Tipo de conteúdo | Descrição |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [Bloquear](block.md) | Adiciona um bloco existente ao estágio. |
| [Bloco Dinâmico](dynamic-block.md) | Adiciona um bloco dinâmico existente ao estágio. |
| [Produtos](products.md) | Adiciona uma lista de produtos ao estágio. |
| ![Somente Adobe Commerce](../assets/adobe-logo.svg) [Product Recommendations](recommendations.md) | Adiciona uma unidade de recomendação ao estágio. |

{style="table-layout:auto"}

## Toolbox

Cada container de conteúdo no estágio tem uma caixa de ferramentas de opções. As opções variam de acordo com o tipo de conteúdo, mas normalmente incluem Mover, Configurações, Ocultar/Mostrar, Duplicar e Remover.

### Mostrar a caixa de ferramentas

Passe o mouse sobre o container para exibir a caixa de ferramentas e escolher uma opção.

![Opções de caixa de ferramentas de linha](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### Opções da caixa de ferramentas

| Opção | Ícone | Descrição |
| --------- | ---------------------------------------- | ------------ |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o contêiner de conteúdo atual para outra posição no estágio. |
| Adicionar | ![Ícone Adicionar](./assets/pb-icon-add.png){width="25"} | Adiciona elementos secundários, como um botão, slide ou guia. |
| (rótulo) |           | Identifica o tipo de conteúdo do container. |
| Configurações  | ![Ícone de configurações](./assets/pb-icon-settings.png){width="25"} | Abre as propriedades do container de conteúdo no modo de edição. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o contêiner de conteúdo atual. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o contêiner de conteúdo atual. |
| Duplicar | ![Ícone duplicado](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do container de conteúdo atual. |
| Remover | ![Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o contêiner de conteúdo atual do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}
