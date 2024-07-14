---
title: Adicionar conteúdo - Bloco dinâmico
description: Saiba mais sobre o tipo de conteúdo Bloco Dinâmico, usado para adicionar um bloco dinâmico reutilizável ao estágio  [!DNL Page Builder] .
exl-id: 04c90f47-9e32-4d34-ac0d-a2f2cec95ffc
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# Adicionar conteúdo - Bloco dinâmico

Use o tipo de conteúdo Bloco Dinâmico para adicionar um [bloco dinâmico](../content-design/dynamic-blocks.md) existente ao [[!DNL Page Builder] estágio](workspace.md#stage).

![Bloco dinâmico na loja](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Caixa de ferramentas Bloco dinâmico

| Ferramenta | Ícone | Descrição |
| --------- | ------------- | ----------------- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o contêiner de bloco e seu conteúdo para outra posição no palco. |
| Configurações | ![Ícone de configurações](./assets/pb-icon-settings.png){width="25"} | Abre a página _Editar Bloco_, na qual você pode escolher o bloco e alterar as propriedades do contêiner. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o container de bloco atual e seu conteúdo. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o contêiner de bloco oculto e seu conteúdo. |
| Duplicar | ![Ícone duplicado](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do contêiner de bloco e de seu conteúdo. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o contêiner de bloco e seu conteúdo do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar um bloco dinâmico existente ao estágio

1. Navegue até o espaço de trabalho [!DNL Page Builder] na página de destino, bloco, produto ou categoria.

1. No painel [!DNL Page Builder], expanda **[!UICONTROL Add Content]** e arraste um espaço reservado **[!UICONTROL Dynamic Block]** para o estágio.

   ![Arrastando um espaço reservado para bloco dinâmico para o estágio](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. Passe o mouse sobre o contêiner de bloco dinâmico vazio para exibir a caixa de ferramentas e escolha o ícone _Configurações_ ( ![Configurações](./assets/pb-icon-settings.png){width="20"} ).

   ![Caixa de ferramentas Bloco Dinâmico](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. Na página _Editar Bloco Dinâmico_, clique em **[!UICONTROL Select Dynamic Block]** e use a lista para selecionar o bloco.

   ![Selecionando um bloco dinâmico](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

   Na lista, localize o bloco dinâmico que deseja inserir e clique em **[!UICONTROL Select]**. Em seguida, clique em **[!UICONTROL Add Selected]**.

   ![Selecionando um bloco dinâmico na lista](./assets/pb-add-content-dynamic-block-select-list.png){width="600" zoomable="yes"}

   Um resumo das informações de bloco dinâmico aparece abaixo.

   ![Resumo de Bloqueios Dinâmicos](./assets/pb-add-content-dynamic-block-summary.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Template]** como um dos seguintes:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Dynamic Block Block Template` | Adiciona um bloco independente. |
   | `Dynamic Block Inline Template` | Insere o conteúdo do bloco no texto. |

   {style="table-layout:auto"}

   ![Modelo de bloco dinâmico](./assets/pb-add-content-dynamic-block-template.png){width="200"}

1. Complete as Configurações avançadas, conforme necessário.

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao espaço de trabalho [!DNL Page Builder].

### Configurações avançadas

1. Para controlar o posicionamento do bloco dinâmico no contêiner pai, escolha um **[!UICONTROL Alignment]**:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
   | `Left` | Alinha a lista ao longo da borda esquerda do contêiner principal, com permissão para qualquer preenchimento especificado. |
   | `Center` | Alinha a lista no centro do contêiner pai, com permissão para qualquer preenchimento especificado. |
   | `Right` | Alinha o bloco ao longo da borda direita do contêiner principal, com permissão para qualquer preenchimento especificado. |

   {style="table-layout:auto"}

1. Defina o estilo **[!UICONTROL Border]** que é aplicado a todos os quatro lados do contêiner de bloco dinâmico:

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

1. Se você definir um estilo de borda diferente de `None`, conclua as opções de exibição de borda:

   | Opção | Descrição |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Especifique a cor escolhendo uma amostra, clicando no seletor de cores ou inserindo um nome de cor válido ou um valor hexadecimal equivalente. |
   | [!UICONTROL Border Width] | Insira o número de pixels para a largura da linha de borda. |
   | [!UICONTROL Border Radius] | Insira o número de pixels para definir o tamanho do raio usado para arredondar cada canto da borda. |

   {style="table-layout:auto"}

1. (Opcional) Especifique os nomes de **[!UICONTROL CSS classes]** da folha de estilos atual para aplicar ao contêiner.

   Separe vários nomes de classe com um espaço.

1. Insira valores, em pixels, para que **[!UICONTROL Margins and Padding]** determine as margens externas e o preenchimento interno do contêiner de bloco dinâmico.

   Insira os valores correspondentes no diagrama.

   | Área de contêiner | Descrição |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. Opções: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. Opções: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Editar configurações de contêiner de bloco dinâmico

1. Passe o mouse sobre o contêiner de bloco dinâmico para exibir a caixa de ferramentas e escolher o ícone _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ).

   ![Caixa de ferramentas Bloco Dinâmico](./assets/pb-add-content-dynamic-block-toolbox.png){width="500" zoomable="yes"}

1. Se necessário, altere o bloco dinâmico:

   - Clique em **[!UICONTROL Select Dynamic Block]**.

     ![Selecionando outro bloco dinâmico](./assets/pb-add-content-dynamic-block-select.png){width="20"}

   - Na lista de blocos dinâmicos ativos, clique em **[!UICONTROL Select]** para o bloco que deseja adicionar.

1. Atualize as configurações restantes conforme necessário.

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao espaço de trabalho [!DNL Page Builder].

## Duplicar um bloco dinâmico

1. Passe o mouse sobre o contêiner de bloco dinâmico para exibir a caixa de ferramentas e escolher o ícone _Duplicar_ ( ![Duplicar ícone](./assets/pb-icon-duplicate.png){width="20"} ).

   A duplicata é exibida logo abaixo do original.

   ![Duplicando um bloco dinâmico](./assets/pb-add-content-dynamic-block-duplicate.png){width="500" zoomable="yes"}

1. Para mover o novo bloco dinâmico para uma posição diferente, passe o mouse sobre o contêiner e escolha _Mover_ ( ![ícone Mover](./assets/pb-icon-move.png){width="20"} ) na caixa de ferramentas.

1. Selecione e arraste o bloco dinâmico até que a diretriz vermelha apareça na nova posição.

   As bordas superior e inferior de cada contêiner são exibidas como linhas tracejadas enquanto o bloco dinâmico é movido.

## Remover um bloco dinâmico do estágio

1. Passe o mouse sobre o contêiner de bloco dinâmico para exibir a caixa de ferramentas e escolha o ícone _Remover_ ( ![Remover ícone](./assets/pb-icon-remove.png){width="20"} ).

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.
