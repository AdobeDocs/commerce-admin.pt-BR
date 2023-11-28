---
title: Adicionar conteúdo - Bloquear
description: Saiba mais sobre o tipo de conteúdo Bloco, usado para adicionar um bloco reutilizável à [!DNL Page Builder] estágio.
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Adicionar conteúdo - Bloquear

Use o _Bloquear_ tipo de conteúdo para adicionar um existente, ativo [bloco](../content-design/blocks.md) para o [[!DNL Page Builder] estágio](workspace.md#stage). No exemplo a seguir, a primeira coluna contém o bloco com um menu lateral para a página. A segunda coluna contém uma imagem.

![Bloquear com um menu lateral](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Bloquear caixa de ferramentas

| Ferramenta | Ícone | Descrição |
| --------- | -------- | ------------- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png) | Move o contêiner de bloco e seu conteúdo para outra posição no palco. |
| Configurações | ![Ícone Configurações](./assets/pb-icon-settings.png) | Abre a página Editar Bloco, onde você pode escolher o bloco e alterar as propriedades do contêiner. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png) | Oculta o container de bloco atual e seu conteúdo. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png) | Mostra o contêiner de bloco oculto e seu conteúdo. |
| Duplicar | ![Ícone Duplicar](./assets/pb-icon-duplicate.png) | Faz uma cópia do contêiner de bloco e de seu conteúdo. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png) | Exclui o contêiner de bloco e seu conteúdo do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar um bloco existente

1. Navegue até a [!DNL Page Builder] espaço de trabalho na página de destino, bloco, bloco dinâmico, produto ou categoria.

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Add Content]** e arraste uma **[!UICONTROL Block]** espaço reservado para o estágio.

   ![Arrastar um bloco para o palco](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. Passe o mouse sobre o container de bloco vazio para exibir a caixa de ferramentas e escolher o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="25"} ) ícone.

1. Clique em **[!UICONTROL Select Block]**.

   ![Seleção de um bloco](./assets/pb-add-content-block-select.png){width="200"}

1. Na linha do bloco que deseja adicionar, clique em **[!UICONTROL Select]** na última coluna.

   ![Bloco selecionado](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   O nome do bloco selecionado aparece na página.

   ![Nome do bloco](./assets/pb-add-content-block-name.png){width="200"}

1. Preencha as configurações restantes conforme necessário, usando as descrições de campo no final desta página para referência.

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

### Configurações avançadas

1. Para controlar o posicionamento do bloco no container-pai, escolha uma **[!UICONTROL Alignment]**:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
   | `Left` | Alinha a lista ao longo da borda esquerda do contêiner principal, com permissão para qualquer preenchimento especificado. |
   | `Center` | Alinha a lista no centro do contêiner pai, com permissão para qualquer preenchimento especificado. |
   | `Right` | Alinha o bloco ao longo da borda direita do contêiner principal, com permissão para qualquer preenchimento especificado. |

   {style="table-layout:auto"}

1. Defina um **[!UICONTROL Border]** estilo aplicado aos quatro lados do contêiner de bloco:

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

1. (Opcional) Especifique os nomes dos **[!UICONTROL CSS classes]** na folha de estilos atual para aplicar ao contêiner.

   Separe vários nomes de classe com um espaço.

1. Insira valores, em pixels, para o **[!UICONTROL Margins and Padding]** para determinar as margens externas e o preenchimento interno do contêiner de bloco.

   Insira os valores correspondentes no diagrama.

   | Área de contêiner | Descrição |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. Opções: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. Opções: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Editar configurações de bloco

1. Passe o mouse sobre o contêiner de bloco e escolha o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="25"} ) na caixa de ferramentas.

   ![Bloquear caixa de ferramentas](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Para escolher um bloco diferente, clique em **[!UICONTROL Select Block]**.

   - Na lista de blocos ativos, clique em **[!UICONTROL Select]** o bloco que deseja adicionar.
   - Clique em **[!UICONTROL Add Selected]**.

1. Atualize as configurações restantes conforme necessário, usando as descrições de campo no final desta página para referência.

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

## Duplicar um bloco

1. Passe o mouse sobre o contêiner de bloco para exibir a caixa de ferramentas e escolher o _Duplicar_ (![Ícone Duplicar](./assets/pb-icon-duplicate.png)) ícone.

   A duplicata é exibida logo abaixo do original.

1. Para mover o novo bloco para uma nova posição, passe o mouse sobre o container e clique em _Mover_ (![Ícone Mover](./assets/pb-icon-move.png)) na caixa de ferramentas.

1. Selecione e arraste o bloco até que a diretriz vermelha apareça na nova posição.

   As bordas superior e inferior de cada contêiner são exibidas como linhas tracejadas enquanto o bloco é movido.

## Remover um bloco do estágio

1. Passe o mouse sobre o contêiner de bloco para exibir a caixa de ferramentas e escolher o _Remover_ (![Ícone Remover](./assets/pb-icon-remove.png)) ícone.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.
