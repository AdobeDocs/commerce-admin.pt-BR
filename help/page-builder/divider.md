---
title: Elementos - Divisor
description: Saiba mais sobre o tipo de conteúdo Divider, usado para adicionar uma regra como uma quebra visual entre seções de conteúdo no estágio  [!DNL Page Builder] .
exl-id: e1052170-6d2f-4893-a78b-a845a8b6c0d9
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Elementos - Divisor

Use o tipo de conteúdo _Divider_ para adicionar uma regra como uma quebra visual entre seções de conteúdo no [[!DNL Page Builder] estágio](workspace.md#stage). É possível especificar a cor, a espessura e a largura da linha do divisor. Você também pode controlar o alinhamento, definir as margens e o preenchimento e o formato da borda do container. Por padrão, o divisor é uma regra de traço que estende a largura total do contêiner, com permissão para preenchimento.

![Divisor padrão em um contêiner sem borda](./assets/pb-elements-divider-default.png){width="500" zoomable="yes"}

Embora a maioria dos contêineres divisores seja invisível, o exemplo a seguir exibe o contêiner com uma borda tracejada vermelha para que você possa ver a relação entre o divisor, o preenchimento e o contêiner. Você pode ajustar o preenchimento na parte superior e inferior do divisor para controlar o espaçamento entre os elementos.

![Divisor com preenchimento no contêiner com borda tracejada](./assets/pb-elements-divider-default-border-dashed.png){width="500" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Caixa de ferramentas Divisor

| Ferramenta | Ícone | Descrição |
| ---- | --------------------| ------------|
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o contêiner do divisor para outro local válido na página. |
| (rótulo) | DIVISOR | Identifica o contêiner atual como um elemento divisor. |
| Configurações | ![Ícone de configurações](./assets/pb-icon-settings.png){width="25"} | Abre a página Editar Divisor, onde você pode alterar as propriedades do divisor e seu contêiner. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o contêiner do divisor. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o contêiner divisor oculto. |
| Duplicar | ![Ícone duplicado](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do contêiner divisor. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o contêiner divisor e seu conteúdo do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar um divisor

1. No painel [!DNL Page Builder], expanda **[!UICONTROL Elements]** e arraste um espaço reservado **[!UICONTROL Divider]** para uma linha, coluna ou conjunto de guias no estágio.

   Use a diretriz vermelha para referência ao posicionar o divisor antes ou depois de outro contêiner de conteúdo no estágio.

   ![Arrastando um divisor para o estágio](./assets/pb-elements-divider-drag.png){width="600" zoomable="yes"}

   No exemplo a seguir, o divisor marca o início de uma nova seção de texto.

   ![Divisor separando seções de texto](./assets/pb-elements-dividers-multiple-text-row.png){width="500" zoomable="yes"}

1. Para especificar as configurações do novo divisor, siga o próximo procedimento.

## Alterar as configurações do divisor

1. Passe o mouse sobre o contêiner do divisor para exibir a caixa de ferramentas e escolher o ícone _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ).

   ![Caixa de ferramentas Divisor](./assets/pb-elements-divider-toolbox.png){width="500" zoomable="yes"}

1. Altere o divisor **[!UICONTROL Line Color]** usando um dos seguintes métodos:

   - Insira um [nome de cor do HTML][1] válido. Por exemplo, `Teal`.
   - Insira o valor de cor hexadecimal. Por exemplo, `#008080`.

   Quando terminar, clique em **[!UICONTROL Apply]**.

   ![Definindo a cor da linha](./assets/pb-elements-divider-settings-line-color.png){width="600" zoomable="yes"}

1. Insira o **[!UICONTROL Line Thickness]** em pixels.

1. Para indicar a unidade de medida, insira o **[!UICONTROL Line Width]** seguido por `px` ou `%`.

   ![Definindo a cor, a espessura e a largura da linha](./assets/pb-elements-divider-settings-line-color-thickness-width.png){width="600" zoomable="yes"}

1. Atualize as configurações de _[!UICONTROL Advanced]_conforme necessário.

   - Para controlar o posicionamento do divisor no contêiner pai, escolha o **[!UICONTROL Alignment]**:

     | Opção | Descrição |
     | ------ | ----------- |
     | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
     | `Left` | Alinha a lista ao longo da borda esquerda do contêiner principal, com permissão para qualquer preenchimento especificado. |
     | `Center` | Alinha a lista no centro do contêiner pai, com permissão para qualquer preenchimento especificado. |
     | `Right` | Alinha o bloco ao longo da borda direita do contêiner principal, com permissão para qualquer preenchimento especificado. |

     {style="table-layout:auto"}

     No exemplo a seguir, as opções são definidas para usar um alinhamento central para o divisor.

     ![Divisor com alinhamento de centro](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - Defina o estilo **[!UICONTROL Border]** aplicado a todos os quatro lados do contêiner divisor:

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

   - Insira valores, em pixels, para **[!UICONTROL Margins and Padding]** para determinar as margens externas e o preenchimento interno do contêiner divisor.

     Insira os valores correspondentes no diagrama.

     | Área de contêiner | Descrição |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. Opções: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. Opções: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao espaço de trabalho [!DNL Page Builder].

   ![Divisor centralizado em uma linha](./assets/pb-elements-divider-settings-2px-centered.png){width="500" zoomable="yes"}

## Duplicar um divisor

Para um divisor formatado com configurações específicas, é mais eficiente fazer uma duplicata, em vez de começar novamente com um novo espaço reservado.

1. Passe o mouse sobre o contêiner do divisor para exibir a caixa de ferramentas e escolher o ícone _Duplicar_ ( ![Duplicar ícone](./assets/pb-icon-duplicate.png){width="20"} ).

   O contêiner de divisor duplicado aparece logo abaixo do original.

   ![Divisor duplicado](./assets/pb-elements-divider-duplicate.png){width="500" zoomable="yes"}

1. Passe o mouse sobre o novo contêiner do divisor para exibir a caixa de ferramentas e escolher o ícone _Mover_ ( ![Ícone Mover](./assets/pb-icon-move.png){width="20"} ).

   ![Movendo um divisor](./assets/pb-elements-divider-move.png){width="500" zoomable="yes"}

1. Selecione e arraste o divisor até que a diretriz vermelha marque a nova posição.

   As bordas superior e inferior de cada contêiner são exibidas como linhas tracejadas enquanto o divisor é movido.

   ![Movendo o divisor duplicado para a posição](./assets/pb-elements-divider-move-guideline.png){width="500" zoomable="yes"}

[1]: https://en.wikipedia.org/wiki/Web_colors

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
