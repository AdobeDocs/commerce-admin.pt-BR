---
title: Mídia - Imagem
description: Saiba mais sobre o tipo de conteúdo de Imagem, usado para adicionar uma imagem JPG, GIF ou PNG ao estágio  [!DNL Page Builder] .
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 0%

---

# Mídia - Imagem

Use o tipo de conteúdo _Image_ para adicionar uma imagem JPG GIF, PNG ou PNG ao [[!DNL Page Builder] stage](workspace.md#stage). Além da imagem de desktop padrão, você pode especificar uma imagem secundária para dispositivos móveis. Você também pode adicionar uma legenda que aparece abaixo da imagem e vincular a imagem a qualquer URL, produto, categoria ou página.

>[!TIP]
>
>Você pode usar a [Integração do Adobe Stock](../content-design/adobe-stock.md) para localizar e salvar um ativo apropriado entre os milhões fornecidos pela [Adobe Stock](https://stock.adobe.com). Consulte [Usando imagens do Adobe Stock](../content-design/adobe-stock-manage.md) para obter detalhes sobre como pesquisar, refinar e salvar ativos do Adobe Stock na galeria.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Caixa de ferramentas Imagem

A caixa de ferramentas da imagem é exibida ao passar o mouse sobre o container de imagem.

![Caixa de ferramentas Imagem](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| Ferramenta | Ícone | Descrição |
|--- |--- |--- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move a imagem para outra posição no palco. |
| (rótulo) | Imagem | Identifica o container de conteúdo atual como uma imagem. Passe o mouse sobre o contêiner de imagem para ver a caixa de ferramentas. |
| Configurações | ![Ícone de configurações](./assets/pb-icon-settings.png){width="25"} | Abre a página _Editar Imagem_, na qual você pode alterar as propriedades da imagem e do contêiner. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta a imagem atual. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra a imagem oculta. |
| Duplicar | ![Ícone duplicado](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia da imagem. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui a imagem do estágio. |
| Carregar nova imagem |  | Faz upload de uma imagem do seu sistema de arquivos local para a galeria. |
| Selecionar na Galeria |  | Escolhe uma imagem existente da galeria. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar uma imagem

1. No painel [!DNL Page Builder], expanda **[!UICONTROL Media]** e arraste um espaço reservado **[!UICONTROL Image]** para o contêiner de destino.

   É possível adicionar uma imagem a uma linha, coluna ou guia. No exemplo a seguir, a imagem é arrastada para uma coluna vazia.

   ![Arrastando um tipo de conteúdo de imagem para o estágio](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Use um dos métodos a seguir para adicionar o ativo de imagem:

   ![Carregar Imagem ou Selecionar nas ferramentas da Galeria no estágio](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >O tamanho máximo do arquivo é 4 MB. Os tipos de arquivos compatíveis são JPG, GIF e PNG.

   - _&#x200B;**Carregar uma nova imagem**&#x200B;_: use este método para carregar um novo arquivo de imagem do seu sistema.

      - Clique em **[!UICONTROL Upload Image]**.

      - Localize e escolha a imagem para adicioná-la à galeria e ao container de destino.

     Como alternativa, você também pode arrastar um arquivo de imagem de seu sistema e soltá-lo no ícone da _Câmera_ ( ![Ícone de Câmera](./assets/pb-icon-camera.png){width="20"} ).

   - _&#x200B;**Selecionar um ativo existente**&#x200B;_: use este método para selecionar um ativo de imagem existente do armazenamento de mídia/galeria.

      - Clique em **[!UICONTROL Select from Gallery]**.

      - Use a árvore para navegar até a imagem.

      - Clique na miniatura e em **[!UICONTROL Add Selected]**.

        ![Adicionando uma imagem selecionada](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _&#x200B;**Pesquise e selecione uma imagem do Adobe Stock**&#x200B;_: use este método para localizar uma imagem do Adobe Stock.

     >[!NOTE]
     >
     >Este método requer uma [integração com o Adobe Stock](../content-design/adobe-stock.md) configurada para o Administrador.

      - Clique em **[!UICONTROL Search Adobe Stock]** e procure uma imagem.

      - Salve a imagem de visualização ou licenciada na galeria.

        Consulte [Usando imagens do Adobe Stock](../content-design/adobe-stock-manage.md) para obter mais informações sobre como trabalhar com ativos do Adobe Stock.

      - Selecione a miniatura do ativo na galeria e clique em **[!UICONTROL Add Selected]**.

   A imagem é exibida no container de destino no local do espaço reservado. Diferentemente de uma imagem de plano de fundo, você pode mover a imagem para uma posição diferente no contêiner atual ou para um contêiner diferente.

   >[!NOTE]
   >
   >Os tipos de conteúdo [Banner](banner.md) e [Slider](slider.md) também incluem as opções _Carregar Imagem_ e _Selecionar na Galeria_ para adicionar imagens.

   ![Imagem em uma coluna](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## Alterar configurações da imagem

1. Passe o mouse sobre o contêiner de imagem para exibir a caixa de ferramentas e escolha o ícone _Configurações_ (![Configurações](./assets/pb-icon-settings.png){width="20"} ).
O nome do arquivo, as dimensões e o tamanho do arquivo aparecem abaixo da imagem atual.

   ![Imagem atual](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. Para alterar o **[!UICONTROL Image]** atual, siga um destes procedimentos:

   - _&#x200B;**Carregar uma nova imagem**&#x200B;_: use este método para carregar um novo arquivo de imagem do seu sistema.

      - Clique em **[!UICONTROL Upload Image]**.

      - Localize e escolha a imagem para adicioná-la à galeria e ao container de destino.

   - _&#x200B;**Selecionar um ativo existente**&#x200B;_: use este método para selecionar um ativo de imagem existente do armazenamento de mídia/galeria.

      - Clique em **[!UICONTROL Select from Gallery]**.

      - Use a árvore para navegar até a imagem.

      - Clique na miniatura e em **[!UICONTROL Add Selected]**.

        ![Adicionando uma imagem selecionada](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Pesquise e selecione uma imagem do Adobe Stock**: use este método para localizar uma imagem do Adobe Stock.

     >[!NOTE]
     >
     >Este método requer uma [integração com o Adobe Stock](../content-design/adobe-stock.md) configurada para o Administrador.

      - Clique em **[!UICONTROL Search Adobe Stock]** e procure uma imagem.

      - Salve a imagem de visualização ou licenciada na galeria.

        Consulte [Usando imagens do Adobe Stock](../content-design/adobe-stock-manage.md) para obter mais informações sobre como trabalhar com ativos do Adobe Stock.

      - Selecione a miniatura do ativo na galeria e clique em **[!UICONTROL Add Selected]**.

1. Para adicionar um **[!UICONTROL Mobile Image]**, use os mesmos métodos descritos na etapa anterior para selecionar uma imagem a ser usada para exibição em dispositivos móveis.

   ![Imagem móvel](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. Se necessário, especifique um **[!UICONTROL Link]** para a imagem.

   O link é a página de destino exibida quando o cliente clica na imagem. Você pode usar um dos três tipos de link:

   - **[!UICONTROL URL]** - Links para uma URL relativa ou totalmente qualificada.

   - **[!UICONTROL Product]** - Identifica a página de destino com base no nome do produto ou SKU. Procure o produto por nome com base em um nome parcial ou completo. Escolha o produto na lista de resultados da pesquisa.

     ![Escolhendo um produto para vincular](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifica a página de destino como uma categoria ou subcategoria específica na árvore de categorias. Procure a categoria com base em um nome parcial ou completo. Escolha a categoria na seção expandida da árvore exibida.

     ![Escolhendo uma categoria para vincular](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Identifica a página de destino como uma página de conteúdo específica. Procure a página com base em um nome parcial ou completo. Escolha a página na lista de resultados da pesquisa.

     ![Escolhendo uma página para vincular](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   Se quiser impedir que o visitante saia do armazenamento, marque a caixa de seleção **[!UICONTROL Open in new tab]**. Quando a caixa de seleção é desmarcada, o destino vinculado é aberto na mesma guia do navegador, o que pode efetivamente afastar o visitante da loja.

1. Para adicionar um **[!UICONTROL Image Caption]**, digite o texto que você deseja que apareça abaixo da imagem.

   O formato da legenda é determinado pela folha de estilos associada ao tema atual.

   Normalmente, a legenda aparece abaixo da imagem e fornece informações sobre a imagem para visitantes e mecanismos de pesquisa. Se o site estiver disponível em vários idiomas, você poderá usar a mesma imagem, mas traduzir a legenda. No HTML, a marca `<figcaption>` é um subconjunto da marca `<figure>`. `<figcaption>This is the image caption</figcaption>`

1. Atualize qualquer uma das outras configurações conforme necessário:

   - [Otimização do mecanismo de pesquisa](#search-engine-optimization)
   - [Avançado](#advanced)

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao espaço de trabalho [!DNL Page Builder].

## Mover uma imagem

1. Passe o mouse sobre o contêiner de imagem para exibir a caixa de ferramentas e escolha o ícone _Mover_ (![Mover](./assets/pb-icon-move.png){width="20"} ).

   ![Movendo uma imagem](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. Selecione e arraste a imagem para a nova posição, logo abaixo da linha de guia vermelha.

   ![Usando a diretriz vermelha para posicionar a imagem](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## Remover uma imagem

1. Passe o mouse sobre o contêiner de imagem para exibir a caixa de ferramentas e escolha o ícone _Remover_ ( ![Remover ícone](./assets/pb-icon-remove.png){width="20"} ).

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

## Otimização do mecanismo de pesquisa

O texto dessas configurações está visível para mecanismos de pesquisa e melhora a forma como a página é indexada.

- Para **[!UICONTROL Alternative Text]**, insira uma descrição de texto _alt_ para que as ferramentas de acessibilidade digital sejam exibidas.

  O uso do texto alternativo é uma prática recomendada de acessibilidade e é exigido por lei em alguns locais. No HTML, o atributo `alt` é um subconjunto da marca `image`: `<image title="tooltip" alt="description" src="image.jpg">`.

- Para **[!UICONTROL Title Attribute]**, insira o texto a ser exibido como uma dica de ferramenta ao passar o mouse.

  Como prática recomendada, escolha um título descritivo e rico em palavras-chave para melhorar a forma como a imagem é indexada por mecanismos de pesquisa. No HTML, o atributo `title` é um subconjunto da marca `image`: `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- Para controlar o posicionamento horizontal das imagens adicionadas ao contêiner, escolha um **[!UICONTROL Alignment]**.

  | Opção | Descrição |
  | ------ | ----------- |
  | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
  | `Left` | Alinha o conteúdo da imagem na borda esquerda do contêiner de imagem, permitindo qualquer preenchimento especificado. |
  | `Center` | Alinha o conteúdo da imagem no centro do contêiner de imagem, permitindo qualquer preenchimento especificado. |
  | `Right` | Alinha o conteúdo da imagem na borda direita do contêiner de imagem, permitindo qualquer preenchimento especificado. |

  {style="table-layout:auto"}

- Defina o estilo **[!UICONTROL Border]** aplicado a todos os quatro lados do contêiner de imagem:

  | Opção | Descrição |
  | ------ | ----------- |
  | `Default` | Aplica o estilo de borda padrão especificado pela folha de estilos associada. |
  | `None` | Não fornece nenhuma indicação visível das bordas do contêiner. |
  | `Dotted` | A borda do contêiner aparece como uma linha pontilhada. |
  | `Dashed` | A borda do contêiner aparece como uma linha tracejada. |
  | `Solid` | A borda do contêiner aparece como uma linha sólida. |
  | `Double` | A borda do contêiner aparece como uma linha dupla. |
  | `Groove` | A borda do contêiner é exibida como uma linha com ranhura. |
  | `Ridge` | A borda do contêiner aparece como uma linha estriada. |
  | `Inset` | A borda do contêiner aparece como uma linha interna. |
  | `Outset` | A borda do contêiner aparece como uma linha de saída. |

  {style="table-layout:auto"}

- Se você definir um estilo de borda diferente de `None`, conclua as opções de exibição de borda:

  ![Cor da Borda](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Opção | Descrição |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Especifique a cor escolhendo uma amostra, clicando no seletor de cores ou inserindo um nome de cor válido ou um valor hexadecimal equivalente. |
  | [!UICONTROL Border Width] | Insira o número de pixels para a largura da linha de borda. |
  | [!UICONTROL Border Radius] | Insira o número de pixels para definir o tamanho do raio usado para arredondar cada canto da borda. |

  {style="table-layout:auto"}

- (Opcional) Especifique os nomes de **[!UICONTROL CSS classes]** da folha de estilos atual para aplicar ao contêiner de imagem.

  Separe vários nomes de classe com um espaço.

- Insira valores, em pixels, para que **[!UICONTROL Margins and Padding]** especifique as margens externas e o preenchimento interno do contêiner de imagem.

  Insira cada valor correspondente no diagrama de contêiner de imagem.

  | Área de contêiner | Descrição |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. |
  | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. |

  {style="table-layout:auto"}
