---
title: Adicionar conteúdo - Recommendations do produto
description: Saiba mais sobre o tipo de conteúdo do Recommendations do produto, usado para adicionar uma lista de recomendações à [!DNL Page Builder] estágio.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 2f86421311b218d39c1abebaf117b8af0be5ea5d
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Adicionar conteúdo - Recommendations do produto

Use o _Recommendations do produto_ tipo de conteúdo para adicionar um existente, ativo [unidade de recomendação](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) para o [[!DNL Page Builder] estágio](workspace.md#stage) para uma página, bloco ou bloco dinâmico CMS.

>[!NOTE]
>
>A variável [!DNL Page Builder] _Recommendations do produto_ o tipo de conteúdo é compatível com o Adobe Commerce 2.4.4 e posterior e está disponível no [Produto Recommendations metapackage versões 3.0.x ou posterior](https://commercemarketplace.adobe.com/magento-product-recommendations.html). Para adicionar [!DNL Page Builder] suporte para Recommendations de produto, [consulte as informações de instalação](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure). **Este tipo de conteúdo não está disponível para o Magento Open Source.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Caixa de ferramentas do Recommendations do produto

| Ferramenta | Ícone | Descrição |
| --- | --| --- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o container de recomendação do produto e seu conteúdo para outra posição no estágio. |
| Configurações | ![Ícone Configurações](./assets/pb-icon-settings.png){width="25"} | Abre a página Editar recomendação do produto, na qual você pode escolher a unidade de recomendação e alterar as propriedades do container. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o container de recomendação do produto atual e seu conteúdo. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o contêiner de recomendação do produto oculto e seu conteúdo. |
| Duplicar | ![Ícone Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia duplicada do container de recomendação de produto e de seu conteúdo. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o container de recomendação do produto e seu conteúdo do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar uma unidade de recomendação existente

1. Verifique se você já [criou uma unidade de recomendação](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) para o [!DNL Page Builder] tipo de página.

>[!NOTE]
>
>É possível criar unidades de recomendação para o [!DNL Page Builder] tipo de página somente na visualização de loja padrão.

1. Abra a página, o bloco ou o bloco dinâmico no modo de edição.

1. Expanda a _[!UICONTROL Content]_e clique em **[!UICONTROL Edit with Page Builder]**ou dentro da área de pré-visualização de conteúdo para abrir o [!DNL Page Builder] espaço de trabalho.

1. No [!DNL Page Builder] painel em _[!UICONTROL Layout]_, arraste um **[!UICONTROL Row]**espaço reservado para o estágio.

1. No [!DNL Page Builder] painel em _[!UICONTROL Add Content]_, arraste um **[!UICONTROL Product Recommendation]**espaço reservado para a linha.

   ![Adição do tipo de conteúdo de recomendação do produto](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Siga um destes procedimentos:

   - Clique em **[!UICONTROL Edit Product Recommendation]**.
   - Passe o mouse sobre o container vazio para exibir a caixa de ferramentas e clique no _Configurações_ (![Ícone Configurações](./assets/pb-icon-settings.png)) ícone.

   ![Editar recomendação do produto](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. No _[!UICONTROL Selection]_clique em **[!UICONTROL Select]**.

1. Na lista de recomendações de produtos ativas, localize a linha com a unidade de recomendação que deseja adicionar e clique em **[!UICONTROL Select]** na última coluna.

   ![Recomendação de produto selecionada](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. No canto superior direito, clique em **[!UICONTROL Add Selected]**.

   O nome da recomendação do produto selecionado aparece na caixa _[!UICONTROL Selection]_seção do_[!UICONTROL Edit Product Recommendation]_ página.

1. Faça as alterações necessárias no [Configurações avançadas](#advanced-settings).

   ![Editar recomendação do produto](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. Quando terminar, faça o seguinte:

   - Se estiver trabalhando com uma janela do navegador totalmente maximizada, clique no botão _Fechar tela cheia_ (![Ícone Fechar tela inteira](./assets/pb-icon-reduce.png)) no canto superior direito do espaço de trabalho.

   - Clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

   Ao retornar ao estágio, as imagens de espaço reservado do produto são exibidas no contêiner.

## Editar configurações de unidade de recomendação

1. Passe o mouse sobre o contêiner de unidade de recomendação para exibir a caixa de ferramentas e clique no _Configurações_ (![Ícone Configurações](./assets/pb-icon-settings.png)) ícone.

   ![Caixa de ferramentas de recomendação](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Faça as alterações necessárias no [Configurações avançadas](#advanced-settings).

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

## Duplicar uma unidade de recomendação

1. Passe o mouse sobre o contêiner de unidade de recomendação para exibir a caixa de ferramentas e clique no _Duplicar_ (![Ícone Duplicar](./assets/pb-icon-duplicate.png)) na caixa de ferramentas.

   A duplicata é exibida logo abaixo do original.

1. Para mover a unidade de recomendação duplicada para uma nova posição, passe o mouse sobre o container e clique no _Mover_ (![Ícone Mover](./assets/pb-icon-move.png)) na caixa de ferramentas.

1. Selecione e arraste a unidade de recomendação até que a diretriz vermelha apareça na nova posição.

   As bordas superior e inferior de cada contêiner são exibidas como linhas tracejadas enquanto a unidade de recomendação é movida.

## Remover uma unidade de recomendação do estágio

1. Passe o mouse sobre o container de unidade de recomendação e clique no _Remover_ ( ![Ícone Remover](./assets/pb-icon-remove.png)) na caixa de ferramentas.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

## Configurações avançadas

1. Para controlar o posicionamento da unidade Recommendations do produto no contêiner principal, escolha a **[!UICONTROL Alignment]**:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
   | `Left` | Alinha a unidade ao longo da borda esquerda do contêiner pai, com permissão para qualquer preenchimento especificado. |
   | `Center` | Alinha a unidade no centro do contêiner pai, com permissão para qualquer preenchimento especificado. |
   | `Right` | Alinha a unidade ao longo da borda direita do contêiner pai, com permissão para qualquer preenchimento especificado. |

   {style="table-layout:auto"}

1. Defina o **[!UICONTROL Border]** Estilo aplicado aos quatro lados da unidade Recommendations do produto:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Default` | Aplica o estilo de borda padrão especificado pela folha de estilos associada. |
   | `None` | Não fornece nenhuma indicação visível das bordas unitárias. |
   | `Dotted` | A borda da unidade aparece como uma linha pontilhada. |
   | `Dashed` | A borda da unidade aparece como uma linha tracejada. |
   | `Solid` | A borda da unidade aparece como uma linha sólida. |
   | `Double` | A borda da unidade aparece como uma linha dupla. |
   | `Groove` | A borda da unidade aparece como uma linha entalhada. |
   | `Ridge` | A borda da unidade aparece como uma linha cortada. |
   | `Inset` | A borda da unidade aparece como uma linha interna. |
   | `Outset` | A borda da unidade aparece como uma linha de saída. |

   {style="table-layout:auto"}

1. Se você definir um estilo de borda diferente de `None`, conclua as opções de exibição da borda:

   | Opção | Descrição |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Especifique a cor escolhendo uma amostra, clicando no seletor de cores ou inserindo um nome de cor válido ou um valor hexadecimal equivalente. |
   | [!UICONTROL Border Width] | Insira o número de pixels para a largura da linha de borda. |
   | [!UICONTROL Border Radius] | Insira o número de pixels para definir o tamanho do raio usado para arredondar cada canto da borda. |

   {style="table-layout:auto"}

1. (Opcional) Especifique os nomes dos **[!UICONTROL CSS classes]** da folha de estilos atual a ser aplicada à unidade.

   Separe vários nomes de classe com um espaço.

1. Insira valores, em pixels, para o **[!UICONTROL Margins and Padding]** para determinar as margens externas e o preenchimento interno da unidade.

   Insira os valores correspondentes no diagrama.

   | Área de contêiner | Descrição |
   | ------ | ----------- |
   | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados da unidade. Opções: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados da unidade. Opções: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
