---
title: Blocos dinâmicos
description: Use blocos dinâmicos para criar conteúdo avançado e interativo que é orientado pela lógica das regras de preço e dos segmentos de clientes.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Blocos dinâmicos

{{ee-feature}}

Crie um conteúdo avançado e interativo que seja orientado pela lógica de [regras de preço](../merchandising-promotions/introduction.md#price-rules) e [segmentos de clientes](../customers/customer-segments.md). Existente [blocos dinâmicos](../page-builder/dynamic-block.md) pode ser adicionado diretamente ao [!DNL Page Builder] [estágio](../page-builder/workspace.md). Para obter um exemplo detalhado e passo a passo para usar blocos dinâmicos, consulte [Tutorial 2: blocos](../page-builder/2-blocks.md).

>[!NOTE]
>
>A variável _[!UICONTROL Banner]_opção no [[!UICONTROL Content] menu](content-menu.md) foi descontinuado na versão 2.3.1 e removido na versão 2.4.0. Sua funcionalidade é substituída por Blocos dinâmicos.

![[!DNL Page Builder] - bloco dinâmico com regra de preço e segmento do cliente](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## Etapa 1: criar um bloco dinâmico

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Lista de blocos dinâmicos](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. No canto superior direito, clique em **[!UICONTROL Add Dynamic Block]**.

   ![Novo bloco dinâmico](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Se aplicável, defina **[!UICONTROL Store View]** para uma exibição de loja específica onde o bloco dinâmico deve aparecer.

1. Para ativar o bloco dinâmico, defina **[!UICONTROL Enable Dynamic Block]** para `Yes`.

1. Para referência interna, insira um descritivo **[!UICONTROL Dynamic Block Name]**.

1. Definir **[!UICONTROL Dynamic Block Type]** à área da página em que deseja que o bloco dinâmico seja exibido e clique em **[!UICONTROL Done]**.

   ![Configuração do tipo de bloco dinâmico](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. No **[!UICONTROL Customer Segment]** marque a caixa de seleção de cada segmento que você deseja ver o bloco dinâmico e clique em **[!UICONTROL Done]** para salvar a configuração.

   ![Escolha de um segmento de cliente](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- Se nenhum Segmento for criado, o bloco dinâmico será visível para todos.
   >- Se o cliente não pertencer a nenhum segmento e o bloco dinâmico for criado para todos os segmentos, o conteúdo do bloco dinâmico ainda será exibido.
   >- Se todos os segmentos de clientes atribuídos a um Bloco dinâmico forem excluídos, seu conteúdo ficará visível para todos.

### Usar públicos do Real-Time CDP em blocos dinâmicos

Se você [instalado](../customers/audience-activation.md#install-the-extension) e [configurado](../customers/audience-activation.md#configure-the-extension) o [!DNL Audience Activation] extensão, você verá uma seção chamada **[!UICONTROL Audiences]**.

![Escolha um público-alvo da Real-Time CDP](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

No **[!UICONTROL Real-Time CDP Audience]** , marque a caixa de seleção de cada público-alvo que você deseja ver no bloco dinâmico e clique em **[!UICONTROL Done]** para salvar a configuração.

## Etapa 2: concluir o conteúdo

Use o [!DNL Page Builder] [espaço de trabalho](../page-builder/workspace.md) para concluir o conteúdo.

![[!DNL Page Builder] - espaço de trabalho de bloco dinâmico](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## Etapa 3: Escolher uma promoção relacionada

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. Clique no tipo de promoção que deseja associar ao bloco dinâmico:

   - **[!UICONTROL Add Cart Price Rules]** (consulte [Regras de preço do carrinho](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (consulte [Regras de preço de catálogo](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >As regras de preço de catálogo não são compatíveis com públicos-alvo da Real-Time CDP.

1. Na lista de regras disponíveis, marque a caixa de seleção de cada regra que deseja usar e clique em **[!UICONTROL Add Selected]**.

1. Quando o bloco dinâmico estiver concluído, clique em **[!UICONTROL Save]**.

## Etapa 4: adicionar o bloco dinâmico a uma página

1. Abra a página onde deseja que o bloco dinâmico apareça.

1. Use o [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) tipo de conteúdo para adicionar o bloco dinâmico ao estágio.

## Descrições de campo e ferramenta

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Store View] | Especifica as exibições de armazenamento onde o bloco dinâmico deve estar disponível. |
| [!UICONTROL Enable Dynamic Block] | Ativa ou desativa o bloco dinâmico. Opções: Sim / Não |
| [!UICONTROL Dynamic Block Name] | Um nome descritivo que identifica o bloco dinâmico no Administrador. |
| [!UICONTROL Dynamic Block Type] | Identifica o local na [layout de página padrão](layout-updates.md) onde o bloco dinâmico é colocado. Opções: <br/>**[!UICONTROL Content Area]**- Coloca o bloco dinâmico no local principal [área de conteúdo](layout-updates.md) da página.<br/>**[!UICONTROL Footer]** - Coloca o bloco dinâmico na página [rodapé](page-setup.md#footer). <br/>**[!UICONTROL Header]**- Coloca o bloco dinâmico na página [cabeçalho](page-setup.md#header).<br/>**[!UICONTROL Left Column]** - Coloca o bloco dinâmico na [barra lateral esquerda](page-layout.md#standard-page-layouts) de um layout de duas ou três colunas. <br/>**[!UICONTROL Right Column]**- Coloca o bloco dinâmico na [barra lateral direita](page-layout.md#standard-page-layouts) de um layout de duas ou três colunas. |
| Segmento do cliente | Associa um segmento de cliente ao bloco dinâmico para determinar quais clientes podem visualizá-lo. |
| Público-alvo da Real-Time CDP | Associa um [Público-alvo do Real-Time CDP](../customers/audience-activation.md) com o bloco dinâmico para determinar quais clientes podem visualizá-lo. |

{style="table-layout:auto"}

### Conteúdo

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Layout] | Adicione linhas, colunas ou guias ao estágio. |
| [!UICONTROL Elements] | Adicione texto, cabeçalhos, botões, divisores e código HTML a qualquer contêiner de layout no palco. |
| [!UICONTROL Media] | Adicione imagens, vídeos, banners, controles deslizantes e Google Maps a qualquer contêiner de layout existente no palco. |
| [!UICONTROL Add Content] | Adicionar blocos existentes, blocos dinâmicos e produtos ao estágio. |

{style="table-layout:auto"}

### Promoções relacionadas

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** - Associar um existente [regra de preço do carrinho](../merchandising-promotions/price-rules-cart.md) com o bloco dinâmico como uma promoção. |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** - Associar um existente [regra de preço de catálogo](../merchandising-promotions/price-rules-catalog.md) com o bloco dinâmico como uma promoção. |

{style="table-layout:auto"}
