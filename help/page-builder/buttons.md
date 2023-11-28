---
title: Elementos - Botões
description: Saiba mais sobre o tipo de conteúdo Botões, usado para adicionar um botão individual ou um conjunto de botões na [!DNL Page Builder] estágio.
exl-id: 9f1681c5-04b0-4259-aaf6-5d8081bd8cdb
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 0%

---

# Elementos - Botões

Use o _Botões_ tipo de conteúdo para adicionar um botão individual ou um conjunto de botões na [[!DNL Page Builder] estágio](workspace.md#stage). Você pode organizar botões horizontal ou verticalmente e adicioná-los diretamente a linhas, colunas, guias e banners no palco.

![Banner com um botão na loja](./assets/pb-storefont-banner-with-button.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Toolboxes

Ao trabalhar com o tipo de conteúdo Botões, você adiciona e edita botões individuais e o container de botões que contém um ou mais botões. Cada uma tem sua própria caixa de ferramentas que é usada para criar botões na [!DNL Page Builder] estágio.

### Caixa de ferramentas de botão Individual

![Caixa de ferramentas do botão](./assets/pb-elements-button-settings.png){width="500" zoomable="yes"}

| Ferramenta | Ícone | Descrição |
| --------- | -------- | -------------- |
| Configurações | ![Ícone Configurações](./assets/pb-icon-settings.png){width="25"} | Abre a página Editar Botão, onde é possível alterar as propriedades do botão. |
| Duplicar | ![Ícone Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do botão. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o botão do estágio. |

{style="table-layout:auto"}

### Caixa de ferramentas do contêiner de botões

![Caixa de ferramentas do contêiner de botões](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

| Ferramenta | Ícone | Descrição |
| --------- | ----------------- | ----------- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o contêiner de botão para outro local válido na página. |
| Adicionar | ![Ícone Adicionar](./assets/pb-icon-add-button.png){width="25"} | Adiciona um botão ao container. |
| (rótulo) | Botão | Identifica o container atual como um elemento de botão. |
| Configurações | ![Ícone Configurações](./assets/pb-icon-settings.png){width="25"} | Abre a página Editar botões, onde é possível alterar as propriedades do container. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o contêiner do botão. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o contêiner do botão oculto. |
| Duplicar | ![Ícone Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do contêiner do botão. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o contêiner de botão e seu conteúdo do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar um botão individual

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Elements]** e arraste uma **[!UICONTROL Buttons]** espaço reservado para uma linha, coluna ou conjunto de guias no estágio.

   ![Arrastar um botão para o estágio](./assets/pb-elements-button-drag.png){width="500" zoomable="yes"}

1. Passe o mouse sobre o botão para exibir a caixa de ferramentas e escolher o _Configurações_ (![Ícone Configurações](./assets/pb-icon-settings.png)) ícone.

1. Insira o **[!UICONTROL Button Text]** para ser exibido no botão.

   ![Configurações básicas do botão](./assets/pb-elements-button-settings-button-text.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Button Type]** a um dos seguintes:

   | Tipo | Descrição |
   | ------ | ----------- |
   | `Primary` | Aplica o estilo de botão primário da folha de estilos atual. |
   | `Secondary` | Aplica o estilo de botão secundário da folha de estilos atual, se aplicável. |
   | `Link` | Cria um hiperlink em vez de um botão. |

   {style="table-layout:auto"}

   ![Exemplo de botão Principal e secundário](./assets/pb-elements-button-settings-button-primary-secondary.png){width="500" zoomable="yes"}

1. Defina o **[!UICONTROL Button Link]** usando um dos seguintes tipos:

   - **[!UICONTROL URL]** - Insira o URL de destino do link.

     O URL pode ser um link relativo para um produto ou página em sua loja, ou um URL totalmente qualificado.

     Exemplo de URL relativo - `../luma-analog-watch.html`

     Exemplo de URL totalmente qualificado - `http://mystore.com/luma-analog-watch.html`

     Se o link for para um site diferente, é possível manter a página atual aberta na loja abrindo o link em uma nova guia do navegador.

     Para impedir que o visitante saia da sua loja, selecione a variável **[!UICONTROL Open in new tab]** caixa de seleção

   - **[!UICONTROL Product]** - Digite um nome de produto (parcial ou completo) ou SKU e escolha o nome do produto na lista.

     >[!NOTE]
     >
     >Os produtos são exibidos na lista de acordo com as _Mostrar produtos esgotados_ configurações. Para comerciantes de várias origens que usam [Inventory management](../inventory-management/introduction.md), a lista de produtos é limitada pela fonte atribuída somente ao site padrão.

     ![Escolha de um produto para o link do botão](./assets/pb-elements-button-settings-button-link-product-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Insira um nome de categoria (parcial ou completo) ou clique no campo em branco para exibir a árvore de categorias. Em seguida, escolha o nome da categoria na árvore.

     ![Escolha de uma categoria para o link do botão](./assets/pb-elements-button-settings-button-link-category-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Insira o nome de uma página CMS (parcial ou completa) ou clique no campo em branco para exibir a lista completa. Em seguida, escolha o nome da página na lista de resultados da pesquisa.

     ![Escolha a página CMS para o link do botão](./assets/pb-elements-button-settings-button-link-page-search.png){width="600" zoomable="yes"}

1. Conclua o [configurações avançadas][advanced-settings] conforme necessário.

1. Quando terminar, clique em **[!UICONTROL Save]** no canto superior direito para aplicar as configurações e retornar à tag [!DNL Page Builder] espaço de trabalho.

## Adição de um conjunto de botões

As seções a seguir descrevem uma série de etapas para começar com um botão individual e criar um conjunto de três botões em um contêiner de botão. Se você ainda não tiver um botão individual, siga as instruções anteriores para adicionar um botão individual ao estágio.

### Etapa 1: criar o segundo botão

1. Passe o mouse sobre o contêiner do botão para exibir a caixa de ferramentas e escolher o _Adicionar_ ( ![Ícone Adicionar](./assets/pb-icon-add-button.png){width="20"} ) ícone.

   ![Adição de outro botão](./assets/pb-elements-buttons-toolbox-add.png){width="500" zoomable="yes"}

1. Digite o texto que você deseja que apareça no segundo botão.

1. Clique no botão new para exibir sua caixa de ferramentas e escolha a _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

   ![Edição do botão](./assets/pb-elements-button-set-edit-button2-toolbox.png){width="500" zoomable="yes"}

1. Definir **[!UICONTROL Button Type]** para `Secondary`.

1. Configurar o **[!UICONTROL Button Link]** conforme necessário.

   No exemplo a seguir, o link é um URL relativo que vai para a variável [Entre em contato](../getting-started/store-details.md#contact-us-form) página.

   ![Configurações do botão Fale Conosco](./assets/pb-elements-button-set-edit-button2-toolbox-settings.png){width="600" zoomable="yes"}

1. Conclua o [configurações avançadas][advanced-settings] conforme necessário.

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

### Etapa 2: criar o terceiro botão

1. Clique no segundo botão novamente no palco e escolha a variável _Duplicar_ ( ![Ícone Duplicar](./assets/pb-icon-duplicate.png){width="20"} ) ícone.

   ![Duplicação de um botão](./assets/pb-elements-button-set-contact-us-toolbox-duplicate.png){width="500" zoomable="yes"}

1. Digite o texto que você deseja que apareça no terceiro botão.

1. Clique no terceiro botão para exibir a caixa de ferramentas e escolha o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

   ![Caixa de ferramentas do terceiro botão](./assets/pb-elements-button-set-find-us-toolbox-settings.png){width="500" zoomable="yes"}

1. Atualize o **[!UICONTROL Button Link]** conforme necessário.

1. No canto superior direito, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

### Etapa 3: atualizar o contêiner de botão

1. Passe o mouse sobre o contêiner do botão para exibir a caixa de ferramentas e escolher o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

   ![Caixa de ferramentas do contêiner de botões](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

1. Em _[!UICONTROL Appearance]_, escolha **[!UICONTROL Stacked]**.

1. Definir **[!UICONTROL All Buttons are same size]** para `Yes`.

   ![Botões empilhados do mesmo tamanho](./assets/pb-elements-buttons-settings-appearance-stacked.png){width="300"}

1. Atualize as configurações restantes conforme necessário, usando as descrições de [Alterar configurações de um contêiner de botão][button-container].

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

   O conjunto completo de botões empilhados aparece no palco, com um botão principal e dois botões secundários.

   ![Botões empilhados no palco](./assets/pb-elements-buttons-stacked.png){width="500" zoomable="yes"}

## Mover um botão

1. Clique no botão que deseja mover.

1. Selecione e arraste o botão Mover ( ![Ícone Mover](./assets/pb-icon-move.png){width="20"} ), que aparece antes do texto do botão, para uma nova posição para o botão no contêiner do botão.

   ![Mover um botão](./assets/pb-elements-button-set-move-button.png){width="500" zoomable="yes"}

## Alterar configurações de um botão

1. Clique no botão no palco para exibir a caixa de ferramentas e escolha a _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

   ![Caixas de ferramentas de botão](./assets/pb-elements-button-toolboxes.png){width="500" zoomable="yes"}

1. Atualize as configurações padrão conforme necessário.

   - **[!UICONTROL Button Text]** - Insira o texto a ser exibido no botão (também pode ser atualizado diretamente do estágio).

   - **[!UICONTROL Button Type]** - Determina o formato do botão.

     | Tipo | Descrição |
     | ------ | ----------- |
     | `Primary` | Aplica o estilo de botão primário da folha de estilos atual. |
     | `Secondary` | Aplica o estilo de botão secundário da folha de estilos atual, se aplicável. |
     | `Link` | Cria um hiperlink em vez de um botão. |

     {style="table-layout:auto"}

   - **[!UICONTROL Button Link]** - Determina a página de destino a ser apresentada ao clicar no botão.

     | Opção | Descrição |
     | ------ | ----------- |
     | `URL` | Usa um URL relativo ou totalmente qualificado para identificar a página de destino. |
     | `Product` | Identifica a página de destino com base no nome do produto ou SKU. O nome do produto pode ser pesquisado com base em um nome parcial ou completo. O produto é então escolhido na lista de resultados da pesquisa. |
     | `Category` | Identifica a página de destino como uma categoria ou subcategoria específica na árvore de categorias. |
     | `Page` | Identifica a página de destino como uma página CMS específica. |

     {style="table-layout:auto"}

1. Conclua o [configurações avançadas][advanced-settings] conforme necessário.

1. Para salvar as configurações e retornar para a [!DNL Page Builder] espaço de trabalho, clique **[!UICONTROL Save]** no canto superior direito.

## Alterar configurações de um contêiner de botão

1. Passe o mouse sobre o contêiner do botão para exibir a caixa de ferramentas e escolher o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

1. Atualize o **[!UICONTROL Appearance]** conforme necessário.

   - Use as opções de disposição para exibir os botões na horizontal ou na vertical no contêiner:

     | Opção | Descrição |
     | ------ | ----------- |
     | `Inline` | Organiza os botões horizontalmente. |
     | `Stacked` | Organiza os botões verticalmente. |

     {style="table-layout:auto"}

   - Defina o **[!UICONTROL All buttons are same size]** de acordo com sua preferência.

     Quando definido como `Yes`, todos os botões no contêiner têm um tamanho consistente, com base no comprimento do texto mais longo do botão.

1. Conclua o [Configurações avançadas][advanced-settings] conforme necessário.

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

## Alterar configurações avançadas

Você pode modificar a variável _[!UICONTROL Advanced]_configurações para botões individuais e para o contêiner de botão.

1. Para controlar o posicionamento no contêiner pai, escolha o **[!UICONTROL Alignment]**:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
   | `Left` | Alinha o conteúdo ao longo da borda esquerda do contêiner principal, com permissão para qualquer preenchimento especificado. |
   | `Center` | Alinha o conteúdo no centro do contêiner principal, com permissão para qualquer preenchimento especificado. |
   | `Right` | Alinha o conteúdo ao longo da borda direita do contêiner principal, com permissão para qualquer preenchimento especificado. |

   {style="table-layout:auto"}

1. Defina o **[!UICONTROL Border]** estilo aplicado aos quatro lados do botão ou contêiner de botões:

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

1. Se você definir um estilo de borda diferente de `None`, conclua as opções de exibição da borda:

   | Opção | Descrição |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Especifique a cor escolhendo uma amostra, clicando no seletor de cores ou inserindo um nome de cor válido ou um valor hexadecimal equivalente. |
   | [!UICONTROL Border Width] | Insira o número de pixels para a largura da linha de borda. |
   | [!UICONTROL Border Radius] | Insira o número de pixels para definir o tamanho do raio usado para arredondar cada canto da borda. |

   {style="table-layout:auto"}

1. (Opcional) Especifique os nomes dos **[!UICONTROL CSS classes]** na folha de estilos atual a ser aplicada ao botão ou contêiner de botões.

   Separe vários nomes de classe com um espaço.

1. Insira valores, em pixels, para o **[!UICONTROL Margins and Padding]** para determinar as margens externas e o preenchimento interno do botão ou contêiner de botões.

   Insira os valores correspondentes no diagrama.

   | Área de contêiner | Descrição |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. Opções: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. Opções: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

[advanced-settings]: #change-advanced-settings
[button-container]: #change-settings-for-a-button-container
