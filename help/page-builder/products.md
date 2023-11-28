---
title: Adicionar conteúdo - Produtos
description: Saiba mais sobre o tipo de conteúdo Produtos, usado para adicionar uma lista de produtos à [!DNL Page Builder] estágio.
exl-id: 8ef38669-a6f6-493b-b963-b0fc4e3bbff4
feature: Page Builder, Page Content, Products
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1912'
ht-degree: 0%

---

# Adicionar conteúdo - Produtos

Use o _Produtos_ tipo de conteúdo para adicionar uma lista de produtos à [[!DNL Page Builder] estágio](workspace.md#stage), utilizando um layout de grade ou carrossel. Use o [Adicionar conteúdo - Bloquear](block.md) ferramenta para colocar o bloco na [!DNL Page Builder] e, em seguida, coloque uma lista de produtos no bloco. Ou você pode adicionar a lista de produtos diretamente em uma linha em uma página.

## Diretrizes para usar o carrossel de produtos

O carrossel de produtos oferece uma maneira avançada e atraente de exibir seus produtos. Para aproveitar ao máximo o, são recomendadas as seguintes diretrizes:

- Adicione carrosséis de produtos diretamente a contêineres de largura de página, como linhas, guias ou layouts de uma coluna. O uso de layouts de largura de página garante a melhor exibição responsiva de seus produtos. [!DNL Page Builder] reduz o número de produtos exibidos dependendo da largura da página, não da largura do container.

- Não adicione um carrossel de produtos a uma coluna estreita. Como mencionado, [!DNL Page Builder], por padrão, determina o número de produtos a serem exibidos com base na largura da página, não na largura da coluna.

- Se desejar que a rolagem automática do carrossel do produto seja contínua, defina ambos **[!UICONTROL Autoplay]** e **[!UICONTROL Infinite Loop]** para `Yes`. Se a reprodução automática estiver definida como `Yes` mas o Loop Infinito está definido como `No`, a rolagem automática para no final da lista de produtos.

- Defina o **[!UICONTROL Carousel Mode]** para `Continuous` para destacar, centralizar e rolar um produto de cada vez no carrossel. Os outros produtos são visíveis na lista, mas transparentes para destacar o produto centralizado.

  ![Lista de produtos no modo carrossel contínuo](./assets/pb-products-settings-carousel-continuous.png){width="600"}

- Para exibir e rolar até cinco produtos de cada vez no carrossel, mantenha a **[!UICONTROL Carousel Mode]** definir como `Default`.

  ![Lista de produtos no modo carrossel padrão](./assets/pb-products-settings-carousel-default.png){width="600"}

As instruções a seguir mostram como adicionar uma lista de produtos a um bloco. Em seguida, você pode usar um [widget](../content-design/widgets.md) para colocar o bloco em um local específico em qualquer página da loja.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Caixa de ferramentas Produtos

| Ferramenta | Ícone | Descrição |
| --------- | ------------- | ----------------- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o contêiner de produtos e seu conteúdo para outra posição no estágio. |
| Configurações | ![Ícone Configurações](./assets/pb-icon-settings.png){width="25"} | Abre a _Editar produtos_ página, onde é possível escolher a lista de produtos e alterar as propriedades do container. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o container de produtos atual e seu conteúdo. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o contêiner de produtos ocultos e seu conteúdo. |
| Duplicar | ![Ícone Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do container de produtos e de seu conteúdo. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o contêiner de produtos e seu conteúdo do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Criar um bloco de lista de produtos

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Clique em **[!UICONTROL Add New Block]**.

1. Insira o **[!UICONTROL Block Title]** e **[!UICONTROL Identifier]**.

1. Escolha o **[!UICONTROL Store View]** onde o bloco deve estar disponível.

1. Role para baixo e clique em **[!UICONTROL Edit with Page Builder]** ou dentro da área de pré-visualização de conteúdo para abrir o [!DNL Page Builder] espaço de trabalho.

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Add Content]** e arraste uma **[!UICONTROL Products]** espaço reservado para o estágio.

   ![Adicionar tipo de conteúdo de produtos](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

## Configurar o container da lista de produtos

Passe o mouse sobre o vazio _Produtos_ contêiner para exibir a caixa de ferramentas e clique no _Configurações_ (![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

![Caixa de ferramentas Produtos](./assets/pb-add-content-products-toolbox.png){width="500" zoomable="yes"}

Conclua o _Configurações_ de acordo com as seguintes seções:

### Aparência

1. Para determinar como a lista de produtos é exibida na página, escolha um dos tipos de aparência:

   | Tipo | Descrição |
   | ---- | ----------- |
   | Grade de produtos | Exibe os produtos em uma grade que mostra cinco produtos por linha (por padrão), com quantas linhas forem necessárias para exibir o número inserido no **[!UICONTROL Number of Products to Display]** configuração. |
   | Carrossel de produtos | Exibe os produtos em um carrossel (também conhecido como controle deslizante). O carrossel mostra até cinco produtos por slide. <br/><br/>**Alerta de capacidade de resposta**: ao selecionar essa aparência, é melhor adicionar o tipo de conteúdo Produtos diretamente a um layout de linha, guia ou uma coluna, onde ele seja responsivo, mostrando menos produtos por lado em telas menores. Se você adicioná-lo a tipos de conteúdo mais estreitos do que a largura da página (como uma coluna estreita), o carrossel exibirá mais produtos por slide do que o container permite, independentemente do tamanho da tela. |

   {style="table-layout:auto"}

   ![Aparência do produto](./assets/pb-products-appearances.png){width="300"}

   Se você escolher o carrossel do produto, também deverá configurar o [Configurações do carrossel](#carousel-settings).

1. Para **[!UICONTROL Select Products By]**, escolha o método para seleção de produtos:

   Você pode selecionar seus produtos por categoria, SKU ou condição. Essas opções são mutuamente exclusivas. Por exemplo, você não pode selecionar a opção Categoria, usar o seletor Categoria e alternar para a opção Condição para adicionar algumas condições. Seus produtos são selecionados com base apenas no que você definiu para _um_ opções.

   - **[!UICONTROL Category]** - Escolha esta opção para exibir produtos usando uma categoria selecionada.

     ![Seleção de produtos por categoria](./assets/pb-products-settings_category.png){width="500"}

     Quando selecionada, esta opção fornece uma **[!UICONTROL Category]** seletor. Clique na seta e faça drill-down para escolher a categoria de produtos a serem exibidos. Por exemplo, na variável [!DNL Commerce] dados de amostra, como fazer drill-in e selecionar o _Mulheres > Topos > Tees_ exibe todos os produtos para essa categoria.

     ![Seleção de uma categoria de catálogo](./assets/pb-select-products-by-category.png){width="500"}

   - **[!UICONTROL SKU]** - Escolha esta opção para exibir produtos usando uma ou mais SKUs

     Quando selecionada, esta opção fornece uma **[!UICONTROL Product SKUs]** caixa de texto onde você deve inserir uma lista separada por vírgulas de SKUs a serem exibidas.

     ![Seleção de produtos por SKU](./assets/pb-products-settings_sku.png){width="500"}

   - **[!UICONTROL Condition]** - Escolha essa opção para exibir produtos de acordo com uma ou mais condições definidas.

     Quando selecionada, há ferramentas disponíveis para adicionar condições à seleção de produtos. Por exemplo, você pode selecionar apenas produtos com um Sexo definido como Unisex.

     ![Seleção de produtos por condição](./assets/pb-products-settings_condition.png){width="500"}

     >[!NOTE]
     >
     >Selecionar a opção Categoria ou SKU fornece a **[!UICONTROL Sort By]** opção de `Position`. Com essa opção de classificação, os produtos aparecem na mesma ordem em que aparecem no catálogo.</br>
     >
     >Para a opção Categoria, a classificação por posição exibe os produtos na mesma ordem em que aparecem no catálogo. Para a opção SKU, a classificação por posição exibe os produtos na ordem em que você os insere na **[!UICONTROL Product SKUs]** caixa de texto.

1. Para **[!UICONTROL Sort By]**, escolha a ordem de classificação dos produtos na lista:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Position` (somente para opções de Categoria e SKU) | Ao selecionar a opção Categoria, a Posição exibe os produtos na mesma ordem de sua posição no catálogo. Quando você seleciona a opção SKU, a Posição exibe os produtos na mesma ordem que os SKUs na caixa de texto SKUs do produto. |
   | `Newest products first` | Classifica os produtos pela data em que foram adicionados ao catálogo, exibindo primeiro os produtos com as datas de entrada mais recentes. |
   | `Oldest products first` | Classifica os produtos pela data em que foram adicionados ao catálogo, exibindo primeiro os produtos com as datas de entrada mais antigas. |
   | `Name: A - Z` | Classifica os produtos em ordem alfabética. |
   | `Name: Z - A` | Classifica produtos em ordem alfabética inversa. |
   | `SKU: ascending` | Classifica produtos por SKU em ordem alfanumérica. |
   | `SKU: descending` | Classifica produtos por SKU em ordem alfanumérica inversa. |
   | `Stock: low stock first` | Classifica produtos do estoque mais baixo para o mais alto disponível. |
   | `Stock: high stock first` | Classifica produtos do estoque mais alto para o mais baixo disponível. |
   | `Price: high to low` | Classifica os produtos do preço mais alto ao mais baixo. |
   | `Price: low to high` | Classifica os produtos do preço mais baixo para o mais alto. |

   {style="table-layout:auto"}

   ![Opções de classificação de produtos](./assets/pb-products-sortby.png){width="300"}

1. Insira o **[!UICONTROL Number of Products to Display]** no carrossel ou na grade.

   Os valores podem ser de `1` para `999`. O padrão é `5` para uma grade e `20` para um carrossel.

   >[!NOTE]
   >
   >Alguns produtos nas configurações Categoria, SKU ou Condição podem não aparecer na grade de produtos ou no carrossel. Por exemplo, os produtos com deficiência, os produtos marcados como não visíveis, os produtos indisponíveis e os produtos atribuídos a outro site não são exibidos.

   >[!IMPORTANT]
   >
   >Os preços dos produtos configuráveis, agrupados e agrupados (preço dinâmico) não são definidos no Admin. Portanto, esses produtos não são exibidos na **[!UICONTROL Preview]** se os produtos forem filtrados pelo preço. Esses produtos não podem ser solicitados corretamente no **[!UICONTROL Preview]** se solicitado pelo preço.

### Configurações do carrossel

1. Para determinar como os produtos são exibidos no carrossel, escolha a **[!UICONTROL Carousel Mode]**:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Default` | Por padrão, o carrossel exibe cinco produtos por slide e reduz esse número com agilidade, conforme necessário. |
   | `Continuous` | O carrossel exibe cinco produtos por slide por padrão (com metade de um produto à direita e à esquerda), mas centraliza e rola um produto de cada vez em um loop infinito. Os produtos à direita e à esquerda do produto centralizado ficam esmaecidos para que o produto central fique realçado. |

   {style="table-layout:auto"}

   Se você alternar entre esses dois modos, as outras configurações do carrossel serão mantidas, exceto pelo **[!UICONTROL Infinite Loop]** que está sempre definida como `Yes` no modo Continuous e o campo está desativado.

   ![Configurações do carrossel](./assets/pb-products-carousel-settings.png){width="600" zoomable="yes"}

1. Se necessário, defina a variável **[!UICONTROL Autoplay]** opção para `Yes`.

   Quando a reprodução automática está ativada, o carrossel começa a rolar automaticamente quando a página é carregada. Se deixar a configuração padrão (`No`), o cliente deverá clicar na navegação do slide (pontos ou setas) para exibir cada slide em sequência.

   Se você habilitar esse recurso, insira **[!UICONTROL Autoplay Speed]** para especificar o atraso em milissegundos entre cada slide. O valor padrão é `4000` (4 segundos).

1. Se necessário, defina a variável **[!UICONTROL Infinite Loop]** opção para `Yes`.

   Quando o loop infinito é ativado, a apresentação de slides é reproduzida indefinidamente enquanto a página está aberta. Se deixar a configuração padrão (`No`), a apresentação de slides é reproduzida apenas uma vez.

   >[!NOTE]
   >
   >Se você definir **[!UICONTROL Infinite Loop]** para `No` e **[!UICONTROL Autoplay]** definir como `Yes`, a reprodução automática pára no final do número de produtos a serem exibidos.

1. Se necessário, defina a variável **[!UICONTROL Show Arrows]** opção para `Yes`.

   Quando esta opção está habilitada, cada slide inclui _próximo_ e _anterior_ setas de navegação nos lados esquerdo e direito. Se deixar a configuração padrão (`No`), os slides não exibem setas de navegação.

1. Se necessário, defina a variável **[!UICONTROL Show Dots]** opção para `No`.

   Quando definido para a configuração padrão (`Yes`), os pontos de navegação são exibidos na parte inferior do controle deslizante do carrossel. Se você desativar essa configuração, o controle deslizante do carrossel não exibirá pontos de navegação.

### Avançado

1. Para controlar o posicionamento da lista Produtos no container principal, escolha o **[!UICONTROL Alignment]**:

   | Opção | Descrição |
   | ------ | ----------- |
   | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
   | `Left` | Alinha a lista ao longo da borda esquerda do contêiner principal, com permissão para qualquer preenchimento especificado. |
   | `Center` | Alinha a lista no centro do contêiner pai, com permissão para qualquer preenchimento especificado. |
   | `Right` | Alinha a lista ao longo da borda direita do contêiner principal, com permissão para qualquer preenchimento especificado. |

   {style="table-layout:auto"}

1. Defina o **[!UICONTROL Border]** estilo aplicado aos quatro lados do contêiner Produtos:

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

1. Insira valores, em pixels, para o **[!UICONTROL Margins and Padding]** para determinar as margens externas e o preenchimento interno do contêiner Produtos.

   Insira os valores correspondentes no diagrama.

   | Área de contêiner | Descrição |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. Opções: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. Opções: `Top` / `Right` / `Bottom` / `Left` |


## Salvar e visualizar no estágio

No canto superior direito, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

Se você tiver configurado um carrossel de produtos, ele deverá ser semelhante ao seguinte exemplo:

![Carrossel de produtos no palco](./assets/pb-products-admin-carousel.png){width="600"}

Agora você pode usar um [widget](../content-design/widgets.md) para colocar esse bloco onde quiser que ele apareça na loja. Ou você pode usar [Adicionar conteúdo - Bloquear](block.md) para adicionar o bloco a uma página, guia ou bloco existente.
