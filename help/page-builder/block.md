---
title: Adicionar conteúdo - Bloquear
description: Saiba mais sobre o tipo de conteúdo Bloco, usado para adicionar um bloco reutilizável ao estágio  [!DNL Page Builder] .
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Adicionar conteúdo - Bloquear

Use o tipo de conteúdo _Bloco_ para adicionar um [bloco](../content-design/blocks.md) ativo existente ao [[!DNL Page Builder] estágio](workspace.md#stage). No exemplo a seguir, a primeira coluna contém o bloco com um menu lateral para a página. A segunda coluna contém uma imagem.

![Bloquear com um menu lateral](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Bloquear caixa de ferramentas

| Ferramenta | Ícone | Descrição |
| --------- | -------- | ------------- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png) | Move o contêiner de bloco e seu conteúdo para outra posição no palco. |
| Configurações | ![Ícone de configurações](./assets/pb-icon-settings.png) | Abre a página Editar Bloco, onde você pode escolher o bloco e alterar as propriedades do contêiner. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png) | Oculta o container de bloco atual e seu conteúdo. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png) | Mostra o contêiner de bloco oculto e seu conteúdo. |
| Duplicar | ![Ícone duplicado](./assets/pb-icon-duplicate.png) | Faz uma cópia do contêiner de bloco e de seu conteúdo. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png) | Exclui o contêiner de bloco e seu conteúdo do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar um bloco existente

1. Navegue até o espaço de trabalho [!DNL Page Builder] na página de destino, bloco, bloco dinâmico, produto ou categoria.

1. No painel [!DNL Page Builder], expanda **[!UICONTROL Add Content]** e arraste um espaço reservado **[!UICONTROL Block]** para o estágio.

   ![Arrastando um bloco para o palco](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. Passe o mouse sobre o contêiner de blocos vazios para exibir a caixa de ferramentas e escolha o ícone _Configurações_ ( ![Configurações](./assets/pb-icon-settings.png){width="25"} ).

1. Clique em **[!UICONTROL Select Block]**.

   ![Selecionando um bloco](./assets/pb-add-content-block-select.png){width="200"}

1. Na linha do bloco que deseja adicionar, clique em **[!UICONTROL Select]** na última coluna.

   ![Bloco selecionado](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   O nome do bloco selecionado aparece na página.

   ![Nome do bloco](./assets/pb-add-content-block-name.png){width="200"}

1. Preencha as configurações restantes conforme necessário, usando as descrições de campo no final desta página para referência.

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao espaço de trabalho [!DNL Page Builder].

### Configurações avançadas

1. Para controlar o posicionamento do bloco no contêiner pai, escolha um **[!UICONTROL Alignment]**:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
   | `Left` | Alinha a lista ao longo da borda esquerda do contêiner principal, com permissão para qualquer preenchimento especificado. |
   | `Center` | Alinha a lista no centro do contêiner pai, com permissão para qualquer preenchimento especificado. |
   | `Right` | Alinha o bloco ao longo da borda direita do contêiner principal, com permissão para qualquer preenchimento especificado. |

   {style="table-layout:auto"}

1. Defina um estilo **[!UICONTROL Border]** que seja aplicado a todos os quatro lados do contêiner de bloco:

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

1. Insira valores, em pixels, para que **[!UICONTROL Margins and Padding]** determine as margens externas e o preenchimento interno do contêiner de blocos.

   Insira os valores correspondentes no diagrama.

   | Área de contêiner | Descrição |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. Opções: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. Opções: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Editar configurações de bloco

1. Passe o mouse sobre o contêiner de blocos e escolha o ícone _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="25"} ) na caixa de ferramentas.

   ![Caixa de Ferramentas de Bloqueio](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Para escolher um bloco diferente, clique em **[!UICONTROL Select Block]**.

   - Na lista de blocos ativos, clique no bloco **[!UICONTROL Select]** que deseja adicionar.
   - Clique em **[!UICONTROL Add Selected]**.

1. Atualize as configurações restantes conforme necessário, usando as descrições de campo no final desta página para referência.

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao espaço de trabalho [!DNL Page Builder].

## Duplicar um bloco

1. Passe o mouse sobre o contêiner de blocos para exibir a caixa de ferramentas e escolha o ícone _Duplicar_ (![Duplicar ícone](./assets/pb-icon-duplicate.png)).

   A duplicata é exibida logo abaixo do original.

1. Para mover o novo bloco para uma nova posição, passe o mouse sobre o contêiner e clique em _Mover_ (![ícone Mover](./assets/pb-icon-move.png)) na caixa de ferramentas.

1. Selecione e arraste o bloco até que a diretriz vermelha apareça na nova posição.

   As bordas superior e inferior de cada contêiner são exibidas como linhas tracejadas enquanto o bloco é movido.

## Remover um bloco do estágio

1. Passe o mouse sobre o contêiner de blocos para exibir a caixa de ferramentas e escolha o ícone _Remover_ (![Remover ícone](./assets/pb-icon-remove.png)).

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.
