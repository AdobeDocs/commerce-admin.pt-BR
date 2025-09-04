---
title: Elementos - Cabeçalho
description: Saiba mais sobre o tipo de conteúdo Cabeçalho, usado para adicionar um contêiner de texto com um nível de cabeçalho de H1 a H6 para o estágio  [!DNL Page Builder] .
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Elementos - Cabeçalho

Os níveis de cabeçalho estabelecem uma hierarquia que organiza o conteúdo e ajuda os mecanismos de pesquisa a indexarem cada página. Use o tipo de conteúdo _Cabeçalho_ no [[!DNL Page Builder] estágio](workspace.md#stage) para adicionar um contêiner de texto com um nível de cabeçalho de H1 a H6 ao estágio. Os títulos são formatados de acordo com a folha de estilos associada ao tema atual.

O campo [Cabeçalho do Conteúdo](workspace.md) na seção _[!UICONTROL Content]_pode ser usado para adicionar um cabeçalho H1 à parte superior da página. No entanto, o campo é herdado das versões [!DNL Commerce] anteriores e é fornecido para dar suporte a conteúdo mais antigo. Este campo não aproveita os recursos avançados do [!DNL Page Builder]. É recomendável deixar o campo Cabeçalho do Conteúdo em branco e usar o tipo de conteúdo Cabeçalho [!DNL Page Builder] para adicionar cabeçalhos de qualquer nível à página.

O exemplo a seguir mostra como o Cabeçalho de conteúdo e o tipo de conteúdo Cabeçalho aparecem quando formatados pelo tema Luma.

![Níveis de Cabeçalho e Cabeçalho de Conteúdo na loja](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

Você pode arrastar um cabeçalho da seção _Elementos_ do painel [!DNL Page Builder] para uma linha, coluna ou conjunto de guias no estágio. O nível do cabeçalho e o alinhamento podem ser controlados na barra de ferramentas do editor no palco ou usando o controle _Configurações_ ( ![Ícone de configurações](./assets/pb-icon-settings.png){width="20"} ).

{{$include /help/_includes/page-builder-save-timeout.md}}

## Editor de cabeçalho

![Editor de cabeçalho com a barra de ferramentas](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## Caixa de ferramentas do contêiner de cabeçalho

Como em todos os contêineres de conteúdo, a caixa de ferramentas aparece quando você passa o mouse sobre o contêiner.

![Caixa de ferramentas do contêiner de cabeçalho](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| Ferramenta | Ícone | Descrição |
| --------- | ----------------- | ---------------------- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o container de cabeçalho para outro local válido na página. |
| (rótulo) | Cabeçalho | Identifica o contêiner atual como um cabeçalho. |
| Configurações | ![Ícone de configurações](./assets/pb-icon-settings.png){width="25"} | Abre a página Editar cabeçalho, onde é possível alterar as propriedades do container. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o contêiner de cabeçalho. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o contêiner de cabeçalho oculto. |
| Duplicar | ![Ícone duplicado](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do contêiner de cabeçalho. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o contêiner de cabeçalho e seu conteúdo do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar um cabeçalho

1. No painel [!DNL Page Builder], expanda **[!UICONTROL Elements]** e arraste um espaço reservado **[!UICONTROL Heading]** para uma linha, coluna ou conjunto de guias no estágio.

   ![Arrastando um cabeçalho para o estágio](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. No editor, insira o texto do cabeçalho sobre o espaço reservado `Edit Heading Text`.

   Por padrão, o texto de cabeçalho recebe um tipo de cabeçalho de nível dois (H2).

   ![Espaço reservado no editor de cabeçalho](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. Na barra de ferramentas, escolha o tipo de cabeçalho apropriado entre H1 e H6.

1. Altere o alinhamento, se necessário.

## Editar configurações de cabeçalho

1. Passe o mouse sobre o contêiner de cabeçalho para exibir a caixa de ferramentas e escolha o ícone _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ).

   ![Caixa de ferramentas de cabeçalho](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. Atualize o conteúdo do cabeçalho (**[!UICONTROL Heading Type]** e **[!UICONTROL Heading Text]**), se necessário.

   Você também pode atualizar esse conteúdo no editor de cabeçalho.

1. Atualize as configurações de _[!UICONTROL Advanced]_conforme necessário.

   - Para controlar o posicionamento do cabeçalho no contêiner pai, escolha um **[!UICONTROL Alignment]**:

     | Opção | Descrição |
     | ------ | ----------- |
     | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
     | `Left` | Alinha a lista ao longo da borda esquerda do contêiner principal, com permissão para qualquer preenchimento especificado. |
     | `Center` | Alinha a lista no centro do contêiner pai, com permissão para qualquer preenchimento especificado. |
     | `Right` | Alinha o bloco ao longo da borda direita do contêiner principal, com permissão para qualquer preenchimento especificado. |

     {style="table-layout:auto"}

   - Defina o estilo **[!UICONTROL Border]** aplicado a todos os quatro lados do contêiner de cabeçalho:

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

     | Opção | Descrição |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Especifique a cor escolhendo uma amostra, clicando no seletor de cores ou inserindo um nome de cor válido ou um valor hexadecimal equivalente. |
     | [!UICONTROL Border Width] | Insira o número de pixels para a largura da linha de borda. |
     | [!UICONTROL Border Radius] | Insira o número de pixels para definir o tamanho do raio usado para arredondar cada canto da borda. |

     {style="table-layout:auto"}

   - (Opcional) Especifique os nomes de **[!UICONTROL CSS classes]** da folha de estilos atual para aplicar ao contêiner.

     Separe vários nomes de classe com um espaço.

   - Insira valores, em pixels, para que **[!UICONTROL Margins and Padding]** determine as margens externas e o preenchimento interno do contêiner de cabeçalho.

     Insira os valores correspondentes no diagrama.

     | Área de contêiner | Descrição |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. Opções: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. Opções: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao espaço de trabalho [!DNL Page Builder].

## Duplicar um cabeçalho

Para um cabeçalho formatado com configurações específicas, é mais eficiente duplicar o cabeçalho, em vez de começar novamente com um novo espaço reservado.

1. Passe o mouse sobre o contêiner de cabeçalho para exibir a caixa de ferramentas e escolha o ícone _Duplicar_ ( ![Duplicar ícone](./assets/pb-icon-duplicate.png){width="20"} ).

   A duplicata é exibida logo abaixo do original.

   ![Duplicando um contêiner de cabeçalho](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. Passe o mouse sobre o novo contêiner de cabeçalho para exibir a caixa de ferramentas e escolha o ícone _Mover_ ( ![Ícone Mover](./assets/pb-icon-move.png){width="20"} ).

   ![Movendo um cabeçalho](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. Selecione e arraste o cabeçalho até que a linha de guia vermelha marque a nova posição.

   As bordas superior e inferior de cada contêiner são exibidas como linhas tracejadas enquanto o cabeçalho é movido.

   ![Movendo o cabeçalho duplicado para a posição](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. Se quiser alterar o nível do cabeçalho, clique no texto do cabeçalho e escolha o novo nível na barra de ferramentas do editor.

   ![Escolhendo um novo nível de cabeçalho](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
