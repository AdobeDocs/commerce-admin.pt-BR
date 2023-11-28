---
title: '[!DNL Page Builder] Passo a passo parte 2: blocos'
description: Saiba mais sobre a diferença entre blocos simples e blocos dinâmicos ao usar o [!DNL Page Builder].
exl-id: 864a3078-8cb3-4add-bdb7-14189aba535e
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '2053'
ht-degree: 0%

---

# [!DNL Page Builder] Passo a passo parte 2: blocos

O exercício seguinte ilustra a diferença entre [blocos simples](../content-design/blocks.md) e [blocos dinâmicos](dynamic-block.md)e como usar [!DNL Page Builder] para criar cada tipo de bloco.

>[!NOTE]
>
>[!DNL Page Builder] tem um novo tipo de conteúdo chamado _Banner_, que é apresentado no primeiro exercício de explicação passo a passo e não está relacionado à funcionalidade anterior do banner. O que era anteriormente a opção Banner no [Menu Conteúdo](../content-design/content-menu.md), agora é _Bloco dinâmico_.

![Bloco dinâmico na loja](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

Este exercício pressupõe que você tenha concluído [Parte 1: Página simples](1-simple-page.md), incluindo os pré-requisitos e [arquivos de amostra baixados](./assets/simple-page-assets.zip). Siga as partes deste exercício de explicação em ordem.

>[!NOTE]
>
>Estes exercícios de explicação são atualizados para refletir as alterações [!DNL Page Builder] no espaço de trabalho na versão 2.4.1. Se você estiver usando uma versão anterior do Adobe Commerce, use o [!DNL Page Builder] exercícios incluídos na [[!DNL Commerce] Guia do usuário da versão 2.3](https://docs.magento.com/user-guide/v2.3/cms/page-builder-learn.html).

## Parte 1: Criar um bloco simples

Neste exercício de explicação passo a passo, você cria um bloco simples com conteúdo de [!DNL Google Maps]. Blocos simples às vezes são chamados de _Blocos CMS_ ou _blocos estáticos_, pois o conteúdo não é alterado. Um bloco simples é ideal para conteúdo que você possa querer reutilizar.

### Etapa 1: criar um bloco

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Block]**.

1. Para **[!UICONTROL Block Title]**, insira `Google Map`.

1. Para **[!UICONTROL Identifier]**, insira `google-map`.

1. Escolha o **[!UICONTROL Store View]** onde o bloco deve estar disponível.

   ![Informações de bloco](./assets/pb-tutorial2-block-new-google-map.png){width="600" zoomable="yes"}

1. No canto superior direito, clique em **[!UICONTROL Save]**.

### Etapa 2: adicionar um [!DNL Google Map]

1. Role para baixo até [!DNL Page Builder] pré-visualização de conteúdo (atualmente vazia) e clique em **[!UICONTROL Edit with Page Builder]**.

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Media]** e arraste uma **[!UICONTROL Map]** espaço reservado para o estágio.

   ![Arrastar um mapa para o estágio](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Um mapa para o local da loja será exibido se [!DNL Google Maps] está configurado para sua loja.

   ![Mapa do Google configurado para sua loja](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Um mapa de espaço reservado será exibido se [!DNL Google Maps] ainda não está configurado para a sua loja.

   ![[!DNL Google Maps] espaço reservado](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

1. No canto superior direito do estágio, clique na guia _Fechar tela cheia_ (![Ícone Fechar tela inteira](./assets/pb-icon-reduce.png)) ícone.

   Clicar nesse ícone retornará para a _[!UICONTROL Content]_seção do bloco com a pré-visualização exibida.

1. No canto superior direito, clique na guia **[!UICONTROL Save]** seta e escolha **[!UICONTROL Save & Close]**.

### Etapa 3: configurar [!DNL Google Maps]

Se [!DNL Google Maps] já estiver configurado para o armazenamento, ignore esta etapa e prossiga para a próxima.

1. Vá para a [Console da Google Cloud Platform](https://console.cloud.google.com/google/maps-apis/overview).

1. Clique na lista suspensa do projeto e selecione ou crie o projeto ao qual deseja adicionar uma chave de API.

1. Para configurar suas credenciais de API, siga o [instruções][1] no [!DNL Google Maps] documentação.

1. Copie sua chave de API na área de transferência.

1. Retorne para a [!DNL Commerce] Administrador e acesse **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Ferramentas de conteúdo avançadas](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Para obter mais informações sobre o [!UICONTROL Content Management Advanced Tools] opções de configuração, consulte a seção [_Guia de referência de configuração_](../configuration-reference/general/content-management.md).

1. Para **[!UICONTROL Google Maps API Key]**, cole a chave copiada.

1. Clique em **[!UICONTROL Test Key]**.

   Se houver um problema com sua chave, volte para a guia [!DNL Google Maps] Site da plataforma para resolver o problema. Em seguida, tente novamente.

1. Após verificar sua chave, clique em **[!UICONTROL Save Config]**.

### Etapa 4: adicionar o bloco a uma página

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Na grade, localize o _[!UICONTROL Simple Page]_que você criou no primeiro tutorial e selecione **[!UICONTROL Edit]**no_[!UICONTROL Action]_ coluna.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Content]** e clique em **[!UICONTROL Edit with Page Builder]** ou dentro da área de visualização de conteúdo.

1. No [!DNL Page Builder] painel em _[!UICONTROL Layout]_, arraste um **[!UICONTROL Row]**espaço reservado até a parte superior do estágio.

   ![Adição da linha à parte superior do estágio](./assets/pb-tutorial2-elements-row-drag-top.png){width="600" zoomable="yes"}

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Add Content]** e arraste uma **[!UICONTROL Block]** espaço reservado para a nova linha.

1. Passe o mouse sobre o container de bloco vazio para exibir a caixa de ferramentas e escolher o _Configurações_ (![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

   ![Bloquear caixa de ferramentas](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Na página Editar Bloco, clique em **[!UICONTROL Select Block]**.

   ![Selecionar bloco](./assets/pb-add-content-block-settings-block-select.png){width="600" zoomable="yes"}

1. Na caixa de pesquisa, digite `map` e pressione a tecla Enter/Return para localizar o bloco criado.

   ![Localizar Bloco na Lista](./assets/pb-add-content-block-settings-block-find.png){width="600" zoomable="yes"}

1. Na grade, clique em **[!UICONTROL Select]** para escolher o [!DNL Google Maps] bloco.

1. No canto superior direito, clique em **[!UICONTROL Save]** para salvar as configurações e retornar para a [!DNL Page Builder] espaço de trabalho.

1. No canto superior direito do estágio, clique na guia _Fechar tela cheia_ (![Ícone Fechar tela inteira](./assets/pb-icon-reduce.png)) ícone.

   Clicar nesse ícone retornará para a _[!UICONTROL Content]_para a página com a pré-visualização exibida.

1. No canto superior direito, clique na guia **[!UICONTROL Save]** seta e escolha **[!UICONTROL Save & Close]**.

**Parabéns!** Você concluiu a primeira parte do exercício Bloquear. Certifique-se de manter seu trabalho como referência.

## Parte 2: Criar um bloco dinâmico

Um bloco dinâmico inclui uma lógica que determina onde, quando e para quem ele aparece. Neste exercício de explicação passo a passo, você cria um bloco dinâmico para uma promoção que é acionada quando as condições da regra de preço são atendidas e que é exibida somente para um segmento de cliente específico. O resultado desse exemplo é semelhante ao banner criado no primeiro exercício, mas com uma lógica que controla quando ele aparece na loja.

![Exemplo de promoção em árvore Luma](./assets/pb-tutorial2-dynamic-block-row-page.png){width="600" zoomable="yes"}

### Etapa 1: criar um novo bloco dinâmico

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Lista de blocos dinâmicos](./assets/pb-tutorial2-block-dynamic-add.png){width="700" zoomable="yes"}

1. No canto superior direito, clique em **[!UICONTROL Add Dynamic Block]**.

   ![Nova página Bloco dinâmico](./assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Conclua as configurações básicas do novo bloco dinâmico:

   - Definir **[!UICONTROL Enable Dynamic Block]** para `Yes`.

   - Para **[!UICONTROL Dynamic Block Name]**, insira `Tee Shirt Promo`.

   - Definir **[!UICONTROL Dynamic Block Type]** para `Content Area` e clique em **[!UICONTROL Done]**.

     O Tipo de bloco dinâmico determina onde [layout de página](../content-design/page-layout.md) que o bloco é colocado. Ao configurar um bloco dinâmico para sua loja, considere o layout da página e o [tema](../content-design/themes.md), para que você possa usar bem o espaço disponível. Algumas lojas têm uma área de conteúdo ativa limitada a uma largura fixa, enquanto outras estendem a largura total da tela.

     ![Configuração de Tipo de bloco dinâmico](./assets/pb-dynamic-block-type.png){width="600" zoomable="yes"}

   - Para **[!UICONTROL Customer Segment]**, marque a caixa de seleção de cada segmento que deseja aplicar ao bloco dinâmico e clique em **Concluído** para salvar a lista de segmentos.

     Para o exemplo a seguir, há dois [segmentos de clientes](../customers/customer-segments.md) que identificam os clientes registrados por gênero. Esse bloco dinâmico aparece somente para clientes fêmeas registrados que estão conectados às suas contas enquanto fazem compras em sua loja.

     ![Escolha dos segmentos de clientes](./assets/pb-dynamic-block-customer-segment.png){width="600" zoomable="yes"}

### Etapa 2: Concluir as configurações

Role para baixo até _[!UICONTROL Content]_seção, que exibe uma tag em branco [!DNL Page Builder] pré-visualização de conteúdo e clique em **[!UICONTROL Edit with Page Builder]**. Em seguida, conclua as seguintes tarefas:

**Tarefa 1:** Adicionar uma imagem de plano de fundo

1. Passe o mouse sobre o contêiner de linha para exibir a caixa de ferramentas e escolher o _Configurações_ (![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

1. Em _[!UICONTROL Appearance]_, escolha **[!UICONTROL Full Bleed]**.

1. Para **[!UICONTROL Minimum Height]**, insira `400px`.

1. Role para a _[!UICONTROL Background]_e defina o **[!UICONTROL Background Image]**clicando em **[!UICONTROL Select from Gallery]**e escolhendo o `wide-banner-background.png` imagem carregada no primeiro tutorial.

1. No canto superior direito, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

   ![Linha com a imagem](./assets/pb-tutorial2-row-image.png){width="600" zoomable="yes"}

**Tarefa 2:** Adicionar colunas

No [!DNL Page Builder] painel em _[!UICONTROL Layout]_, arraste um **[!UICONTROL Column]**espaço reservado na linha.

![Arrastar o tipo de coluna para a linha](./assets/pb-tutorial2-column-drag.png){width="600" zoomable="yes"}

A linha agora é dividida em duas colunas de igual largura.

**Tarefa 3:** Adicionar texto

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Elements]** e arraste uma **Texto** espaço reservado para a segunda coluna.

   ![Arrastar uma caixa de texto para a segunda coluna](./assets/pb-tutorial2-column-text-drag.png){width="600" zoomable="yes"}

1. Insira as três linhas de texto a seguir no editor:

   `Even more ways to mix and match.`

   `Buy 3 Luma tees and get a 4th free.`

   `Shop Tees >`

   ![Inserção de texto para a coluna](./assets/pb-tutorial2-column-text-editor.png){width="600" zoomable="yes"}

1. Selecione todas as três linhas de texto e use a barra de ferramentas para definir a **Altura da linha** para `40px`.

   ![Definição da altura da linha](./assets/pb-tutorial2-column-text-editor-line-height.png){width="600" zoomable="yes"}

1. Defina o **[!UICONTROL Font Size]** para cada linha, da seguinte forma:

   | Linha | Tamanho da fonte |
   |-----| ---------- |
   | Linha 1: | `28px` |
   | Linha 2: | `24px` |
   | Linha 3: | `18px` |

   Como esse bloco pode ser colocado em qualquer lugar da página, use o estilo de parágrafo padrão, em vez dos níveis de cabeçalho. Além disso, não se preocupe se o texto ainda não for quebrado corretamente na coluna.  

   ![Texto formatado](./assets/pb-tutorial2-column-text-editor-text-formatted.png){width="600" zoomable="yes"}

**Tarefa 4:** Adicionar um link

No primeiro exercício, você aprendeu a usar o [Botão](buttons.md) tipo de conteúdo para criar um link. Este exemplo mostra como inserir um link da barra de ferramentas do editor.

1. Em outra guia do navegador, abra a loja e navegue até a página que deve ser o destino do link.

   Você pode usar o URL totalmente qualificado ou um URL relativo que omita a referência ao domínio da loja.

   URL completo: `https://mystore.com/women/tops-women/tees-women.html`

   URL relativo: `../women/tops-women/tees-women.html`

1. Retorne para a [!DNL Page Builder] guia espaço de trabalho e editor de texto, selecione a `Shop Tees >` texto na terceira linha e escolha **Negrito** (![Botão Negrito](./assets/editor-btn-bold.png)) na barra de ferramentas do editor.

1. Com o `Shop Tees >` texto na terceira linha ainda selecionado, escolha **Inserir/editar link** (![Botão Inserir/editar link](./assets/pb-icon-add-link.png)) na barra de ferramentas do editor.

   ![Inserção de um link](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL URL]**, insira o link relativo preparado.

1. Definir **[!UICONTROL Target]** para `None`.

   Essa configuração abre a página na mesma janela do navegador, em vez de abrir uma nova guia.

1. Para **[!UICONTROL Title]**, insira `Shop Tees`.

   O atributo Title link é usado por alguns navegadores como uma dica de ferramenta.

1. Para salvar o link e retornar para a [!DNL Page Builder] espaço de trabalho, clique **[!UICONTROL OK]**.

   ![Detalhes do link](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="600" zoomable="yes"}

1. No canto superior direito do estágio, clique na guia _Fechar tela cheia_ (![Ícone Fechar tela inteira](./assets/pb-icon-reduce.png)) ícone.

   Clicar nesse ícone retornará para a _[!UICONTROL Content]_seção do bloco dinâmico com a pré-visualização exibida.

1. No canto superior direito, clique em **[!UICONTROL Save]**.

### Etapa 3: Adicionar uma regra de preço

1. Abra o _Camiseta Promocional_ bloco dinâmico no modo de edição novamente.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Related Promotions]** e clique em **[!UICONTROL Add Cart Price Rules]**.

   ![Promoções relacionadas](./assets/pb-dynamic-blocks-related-promotions.png){width="600" zoomable="yes"}

1. No _Adicionar Regras de Preço do Carrinho Relacionadas_ , marque a caixa de seleção da _Compre 3 camisetas e obtenha a 4ª gratuitamente_ regra de preço e clique **[!UICONTROL Add Selected]**.

   ![Adição de uma regra de preço de carrinho relacionada](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

   A regra de preço aparece na variável _Promoções relacionadas_ seção, em _Regra de preço do carrinho relacionada_. Você pode associar várias regras de preço a um bloco dinâmico. No entanto, esse exemplo simples usa apenas um.

   ![Regra de preço do carrinho selecionada](./assets/pb-dynamic-block-related-cart-price-rule-list.png){width="600" zoomable="yes"}

1. No canto superior direito, clique em **[!UICONTROL Save]**.

### Etapa 4: adicionar o bloco dinâmico a uma página

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**

1. Localize o _Página simples_ que você criou na [primeiro exercício de explicação passo a passo](1-simple-page.md) e abra-o no modo de edição.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Content]** e clique em **[!UICONTROL Edit with Page Builder]**.

1. Passe o mouse sobre a linha superior com a mesma imagem do bloco dinâmico para exibir a caixa de ferramentas e a _Remover_ ( ![Ícone Remover](./assets/pb-icon-remove.png){width="20"} ) ícone.

   Para confirmar a remoção da linha da página, clique em  **[!UICONTROL OK]** .

1. No [!DNL Page Builder] painel em _[!UICONTROL Layout]_, arraste um novo **[!UICONTROL Row]**espaço reservado até a parte superior do estágio.

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Add Content]** e arraste uma **[!UICONTROL Dynamic Block]** espaço reservado para a nova linha.

   ![Arrastar um bloco dinâmico para a linha](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. Passe o mouse sobre o container de bloco dinâmico para exibir a caixa de ferramentas e escolher o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

   ![Caixa de ferramentas de bloco dinâmico](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. No _[!UICONTROL Edit Dynamic Block]_clique em **[!UICONTROL Select Dynamic Block]**.

   ![Selecionar bloco dinâmico](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

1. Localize o _[!DNL Tee Shirt Promo]_bloco dinâmico criado e clique em **[!UICONTROL Select]**.

   Um resumo das informações de bloco dinâmico aparece abaixo.

   ![Informações de bloco dinâmico](./assets/pb-tutorial2-dynamic-block-edit.png){width="600" zoomable="yes"}

1. Aceitar o padrão **[!UICONTROL Template]**, `Dynamic Block Block Template`.

1. Quando terminar, clique em **[!UICONTROL Save]** para salvar as configurações e retornar para a [!DNL Page Builder] espaço de trabalho.

   ![Bloco dinâmico na visualização da página](./assets/pb-tutorial2-dynamic-block-on-page.png){width="600" zoomable="yes"}

1. No canto superior direito do estágio, clique na guia _Fechar tela cheia_ (![Ícone Fechar tela inteira](./assets/pb-icon-reduce.png)) ícone.

   Clicar nesse ícone retornará para a _[!UICONTROL Content]_para a página com a pré-visualização exibida.

1. No canto superior direito, clique na guia **[!UICONTROL Save]** seta e escolha **[!UICONTROL Save & Close]**.

Você concluiu a segunda parte do exercício Bloquear. Certifique-se de manter seu trabalho como referência.

## Parte 3: Atualizar o bloco dinâmico

Nesta parte final do exercício, você edita um bloco dinâmico enquanto a página está ativa na loja. Em seguida, faça logon na loja como um membro do segmento do cliente para que o bloco apareça.

![Exemplo de bloco dinâmico na vitrine](./assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

### Etapa 1: Editar o bloco dinâmico

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Encontre o seu _[!DNL Tee Shirt Promo]_bloco dinâmico na grade e abra-o no modo de edição.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Content]** e clique em **[!UICONTROL Edit with Page Builder]**.

1. Alterar a largura da coluna:

   - Passe o mouse sobre a borda entre as duas colunas.

   - Mantenha pressionado o botão do mouse e arraste a borda duas divisões para a esquerda.

     ![Divisões da grade](./assets/pb-tutorial2-dynamic-block-edit-column-width.png){width="600" zoomable="yes"}

     A primeira coluna é agora quatro de 12 (4/12) divisões de grade de largura, e a segunda coluna é oito de 12 (8/12) divisões de largura.

     ![Duas colunas desiguais](./assets/pb-tutorial2-dynamic-block-edit-column-width-changed.png){width="600" zoomable="yes"}

1. Alterar a cor do texto:

   - Selecione as duas primeiras linhas de texto.

   - Na barra de ferramentas do editor, escolha **[!UICONTROL Text Color]** e clique no link **[!UICONTROL White]** amostra.

   ![Cor do texto](./assets/pb-tutorial2-dynamic-block-edit-text-color.png){width="600" zoomable="yes"}

1. No canto superior direito do estágio, clique na guia _Fechar tela cheia_ (![Ícone Fechar tela inteira](./assets/pb-icon-reduce.png)) ícone.

   Clicar nesse ícone retornará para a _[!UICONTROL Content]_seção do bloco dinâmico com a pré-visualização exibida.

1. No canto superior direito, clique em **[!UICONTROL Save]**.

### Etapa 2: visualizar o bloco dinâmico

Como esse bloco dinâmico é visível somente para membros de um segmento de cliente específico, você deve fazer logon como um cliente que é membro do segmento de cliente para ver a promoção. Neste exemplo, o bloco aparece somente para clientes do sexo feminino.

1. Abra uma janela de navegador na loja.

1. Para exibir sua página de exemplo, modifique o URL na barra de endereços da seguinte maneira:

   mystore.com/sample-page

   Se o armazenamento estiver configurado para incluir o sufixo html, inclua o sufixo da seguinte maneira:

   mystore.com/sample-page.html

1. Fazer logon como uma cliente do sexo feminino:

   - No canto superior direito da home page, clique em **[!UICONTROL Sign In]**.

   - Se os dados do exemplo do Luma estiverem instalados no sistema, use as seguintes credenciais:

     **[!UICONTROL Email]** - `roni_cost@example.com`

     **[!UICONTROL Password]** -  `roni_cost3@example.com`

   - Clique em **[!UICONTROL Sign In]**.

   - Retorne à página de exemplo para ver o bloco dinâmico criado com a Promoção Camiseta.

   ![Bloco dinâmico exibido para um segmento de cliente](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

Você concluiu o exercício Bloquear. Certifique-se de manter seu trabalho como referência.

Quando estiver pronto, prossiga para [Parte 3: Conteúdo do catálogo](3-catalog-content.md)

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
