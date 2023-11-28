---
title: Mídia - Vídeo
description: Saiba mais sobre o tipo de conteúdo Vídeo, usado para adicionar um vídeo hospedado no YouTube ou Vimeo à [!DNL Page Builder] estágio.
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 0%

---

# Mídia - Vídeo

Use o _Vídeo_ tipo de conteúdo para adicionar um vídeo hospedado em [YouTube][1] ou [Vimeo][2] para o [[!DNL Page Builder] estágio](workspace.md#stage). É fácil incorporar vídeos em uma página ou bloco ou em descrições de produtos e categorias.

![Vídeo na página inicial da loja](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Caixa de ferramentas Vídeo

![Caixa de ferramentas Vídeo](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| Ferramenta | Ícone | Descrição |
|--- |--- |--- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o vídeo para outra posição no palco. |
| (rótulo) | [!UICONTROL Video] | Identifica o contêiner de conteúdo atual como um vídeo. Passe o mouse sobre o contêiner de imagem para ver a caixa de ferramentas. |
| Configurações | ![Ícone Configurações](./assets/pb-icon-settings.png){width="25"} | Abre a _[!UICONTROL Edit Video]_página, onde é possível alterar as propriedades do vídeo e do container. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o vídeo atual. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o vídeo oculto. |
| Duplicar | ![Ícone Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do vídeo. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o vídeo do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar um vídeo

1. Antes de começar, navegue até o [YouTube][1] ou [Vimeo][2] vídeo que deseja incorporar e copie o link.

   Como alternativa, você também pode copiar um link direto para um arquivo de vídeo válido. Consulte [Configurações básicas de vídeo](#basic-video-settings) para links válidos.

1. No [!DNL Commerce] Administrador, volte para a guia [!DNL Page Builder] espaço de trabalho ao qual você deseja adicionar o vídeo.

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Media]** e arraste uma **[!UICONTROL Video]** espaço reservado para o estágio.

   ![Arrastar um espaço reservado de vídeo para o estágio](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. Passe o mouse sobre o contêiner de vídeo para exibir a caixa de ferramentas e escolher _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

1. Para **[!UICONTROL Video URL]**, cole o URL do vídeo que você copiou.

   O URL do [!DNL Page Builder] o vídeo usado neste exemplo é: `https://www.youtube.com/watch?v=Y0KNS7C5dZA`.

1. Para limitar o **[!UICONTROL Maximum Width]** do vídeo, digite a largura máxima em pixels.

   Se estiver em branco, o vídeo terá a largura permitida pelo contêiner, permitindo margens e preenchimento.

1. No canto superior direito, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

## Alterar configurações de vídeo

1. Passe o mouse sobre o contêiner de vídeo para exibir a caixa de ferramentas e escolher _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

1. Modifique as configurações de acordo com as seguintes seções:

   - [Básico](#basic-video-settings)
   - [Avançado](#advanced)

1. No canto superior direito, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

### Configurações básicas de vídeo

1. Para alterar o vídeo atual, atualize o **[!UICONTROL Video URL]**.

   Insira um URL de vídeo válido. Os URLs válidos do vídeo podem ser links para:

   - Vídeos do YouTube: `https://youtu.be/CoDhMRUUjeI`
   - Vídeos do Vimeo: `https://vimeo.com/190156113`
   - Arquivos de vídeo válidos (`.mp4` é recomendado): `https://myvideos.com/spiral.mp4`

1. Para alterar a largura permitida para o vídeo na vitrine, insira o novo **[!UICONTROL Maximum Width]** em pixels.

   Se estiver em branco, o vídeo estende a largura total do contêiner, menos espaço para margens e preenchimento.

1. Para iniciar o vídeo automaticamente depois que a página for carregada, defina **[!UICONTROL Autoplay]** para `Yes`.

   Se a reprodução automática estiver definida como `Yes`, o vídeo é silenciado na reprodução de acordo com a política. No entanto, mesmo com essa configuração, os dispositivos móveis não podem reproduzir automaticamente seus vídeos. Para obter mais informações sobre essas políticas, consulte os seguintes recursos do desenvolvedor:

   - [Política de reprodução automática do Vimeo](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [Política de reprodução automática do Google (Chrome/YouTube)](https://developer.chrome.com/blog/autoplay/)
   - [Política de reprodução automática para vídeos locais](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   Se a reprodução automática estiver definida como `No`, o vídeo é reproduzido somente sob demanda do usuário.

### [!UICONTROL Advanced]

1. Para controlar o posicionamento horizontal do vídeo no container, escolha uma **[!UICONTROL Alignment]**:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
   | `Left` | Alinha o conteúdo ao longo da borda esquerda do contêiner de vídeo, com permissão para qualquer preenchimento especificado. |
   | `Center` | Alinha o conteúdo no centro do contêiner de vídeo, permitindo qualquer preenchimento especificado. |
   | `Right` | Alinha o conteúdo ao longo da borda direita do contêiner de vídeo, com permissão para qualquer preenchimento especificado. |

   {style="table-layout:auto"}

- Defina o **[!UICONTROL Border]** estilo aplicado aos quatro lados do contêiner de vídeo:

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

- Se você definir um estilo de borda diferente de `None`, conclua as opções de exibição da borda:

  ![Cor da borda](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Opção | Descrição |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Especifique a cor escolhendo uma amostra, clicando no seletor de cores ou inserindo um nome de cor válido ou um valor hexadecimal equivalente. |
  | [!UICONTROL Border Width] | Insira o número de pixels para a largura da linha de borda. |
  | [!UICONTROL Border Radius] | Insira o número de pixels para definir o tamanho do raio usado para arredondar cada canto da borda. |

  {style="table-layout:auto"}

- (Opcional) Especifique os nomes dos **[!UICONTROL CSS classes]** na folha de estilos atual para aplicar ao contêiner de vídeo.

  Separe vários nomes de classe com um espaço.

- Insira valores, em pixels, para o **[!UICONTROL Margins and Padding]** para especificar as margens externas e o preenchimento interno do container de vídeo.

  Insira cada valor correspondente no diagrama do contêiner de vídeo.

  | Área de contêiner | Descrição |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. |
  | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. |

  {style="table-layout:auto"}

## Mover um vídeo

1. Passe o mouse sobre o contêiner de vídeo para exibir a caixa de ferramentas e escolher _Mover_ ( ![Ícone Mover](./assets/pb-icon-move.png){width="20"} ) ícone.

   ![Mover um vídeo](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. Selecione e arraste o vídeo para a nova posição, logo abaixo da diretriz vermelha.

   ![Usar a diretriz vermelha para inserir o vídeo](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"}

## Remover um vídeo do palco

1. Passe o mouse sobre o contêiner de vídeo para exibir a caixa de ferramentas e escolher _Remover_ (![Ícone Remover](./assets/pb-icon-remove.png)) ícone.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
