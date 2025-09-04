---
title: Elementos - Código HTML
description: Saiba mais sobre o tipo de conteúdo do Código HTML, usado para adicionar trechos de código HTML, CSS e JavaScript no estágio  [!DNL Page Builder] .
exl-id: b6e2dff5-ceac-4c7e-a87f-f95a542ada28
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# Elementos - Código HTML

Use o tipo de conteúdo _Código HTML_ para adicionar trechos de código HTML, CSS e JavaScript no [[!DNL Page Builder] estágio](workspace.md#stage). Por exemplo, talvez você queira adicionar um HTML personalizado, declare uma classe CSS que possa ser aplicada a um elemento na página. Ou você pode adicionar um trecho de código para um logotipo, botão ou banner recebido de um provedor de terceiros.

## Caixa de ferramentas Código HTML

![Caixa de ferramentas do HTML Code](./assets/pb-elements-html-code-toolbox.png){width="500" zoomable="yes"}

| Ferramenta | Ícone | Descrição |
| --------- | ---------- | ----------------- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o contêiner do Código HTML para outro local válido na página. |
| Configurações | ![Ícone de configurações](./assets/pb-icon-settings.png){width="25"} | Abre a página Editar código HTML, onde é possível alterar as propriedades do container. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o contêiner do Código HTML. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o contêiner de código HTML oculto. |
| Duplicar | ![Ícone duplicado](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do contêiner do Código HTML. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o contêiner do Código HTML e seu conteúdo do estágio. |

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Adicionar código HTML

O exemplo a seguir demonstra como incorporar o código [Google Font][1] e declarar classes de cabeçalho personalizadas que substituem a folha de estilos atual.

### Etapa 1: Escolher uma fonte do Google

1. Visite o site [Google Fonts][1] e escolha a família de fontes que deseja usar.

1. Copie o código gerado que deve ser incorporado na seção `<head>` da página e cole-o temporariamente em um editor de texto.

   - Incorporar código de fonte
   - Regra CSS

1. Adicione a regra font-family a cada classe de cabeçalho, colocando as classes de cabeçalho em uma tag `<style>`.

   Este código foi colado em [!DNL Page Builder].

   ```html
   <style>
      h1 {color: teal; font-family: 'Khand', sans-serif; }
      h2 {color: teal; font-family: 'Khand', sans-serif; }
      h3 {color: teal; font-family: 'Khand', sans-serif; }
   </style>
   ```

### Etapa 2: adicionar o código à página

1. Na barra lateral _Admin_ do seu armazenamento, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Localize a página onde a fonte deve estar disponível e abra-a no modo de edição.

1. Role para baixo e expanda a seção **[!UICONTROL Content]**.

1. No painel [!DNL Page Builder], expanda **[!UICONTROL Elements]** e arraste um espaço reservado **[!UICONTROL HTML Code]** para uma linha, coluna ou conjunto de guias no estágio.

   Use a diretriz vermelha para posicionar o divisor antes ou depois de outro contêiner de conteúdo no conjunto de linhas, colunas ou guias.

   ![Arrastando um espaço reservado do Código HTML para o estágio](./assets/pb-elements-html-code-drag.png){width="600" zoomable="yes"}

1. Passe o mouse sobre o contêiner HTML para exibir a caixa de ferramentas e escolha o ícone _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ).

1. Na caixa de texto, cole as declarações de código e estilo incorporadas do Google Fonts que você preparou.

   Para facilitar a leitura, você pode digitar alguns espaços para recuar o código.

   ![Código e estilos do HTML](./assets/pb-elements-html-code-example.png){width="500" zoomable="yes"}

1. Atualize as configurações restantes conforme necessário (consulte [Alterar configurações de código do HTML](#html-settings) para obter detalhes).

1. No canto superior direito, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao espaço de trabalho [!DNL Page Builder].

   A nova fonte é renderizada quando a página é visualizada em um navegador.

### Etapa 3: visualizar a página

1. Na seção _[!UICONTROL Currently Active]_, defina **[!UICONTROL Enable Page]**como `Yes`.

   ![Habilitando a página](./assets/pb-elements-html-code-enable-page.png){width="600" zoomable="yes"}

1. No canto superior direito, clique na seta **[!UICONTROL Save]** e escolha **[!UICONTROL Save & Close]**.

1. Localize a página na grade e selecione **[!UICONTROL View]** na coluna _[!UICONTROL Actions]_.

   ![Visualizar os cabeçalhos da página com a nova família de fontes](./assets/pb-elements-html-code-preview.png){width="700" zoomable="yes"}

## Alterar configurações de código do HTML {#html-settings}

1. Passe o mouse sobre o contêiner HTML para exibir a caixa de ferramentas e escolher o ícone _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ).

1. Na caixa de texto, edite o código conforme necessário.

   Há suporte para código HTML, CSS e JavaScript. Os trechos de código que pertencem à seção `<head>` da página podem ser inseridos aqui.

   O editor também fornece botões para inserir elementos especiais no código:

   | Botão | Descrição |
   | ------ | ----------- |
   | Inserir widget... | Clique para inserir um widget na posição do cursor na caixa de texto do HTML. |
   | Inserir imagem... | Clique para inserir uma imagem carregada ou uma imagem da Galeria na posição do cursor na caixa de texto HTML. |
   | Inserir variável... | Clique em para inserir uma variável na posição do cursor na caixa de texto do HTML. |

1. Atualize as configurações de _[!UICONTROL Advanced]_conforme necessário.

   - Para controlar o posicionamento do código no contêiner pai, escolha um **[!UICONTROL Alignment]**:

     | Opção | Descrição |
     | ------ | ----------- |
     | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
     | `Left` | Alinha a lista ao longo da borda esquerda do contêiner principal, com permissão para qualquer preenchimento especificado. |
     | `Center` | Alinha a lista no centro do contêiner pai, com permissão para qualquer preenchimento especificado. |
     | `Right` | Alinha o bloco ao longo da borda direita do contêiner principal, com permissão para qualquer preenchimento especificado. |

     No exemplo a seguir, as opções são definidas para usar um alinhamento central para o bloco de código renderizado.

     ![Divisor com alinhamento de centro](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - Defina o estilo **[!UICONTROL Border]** aplicado a todos os quatro lados do contêiner de código:

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

   - Se você definir um estilo de borda diferente de `None`, conclua as opções de exibição de borda:

     | Opção | Descrição |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Especifique a cor escolhendo uma amostra, clicando no seletor de cores ou inserindo um nome de cor válido ou um valor hexadecimal equivalente. |
     | [!UICONTROL Border Width] | Insira o número de pixels para a largura da linha de borda. |
     | [!UICONTROL Border Radius] | Insira o número de pixels para definir o tamanho do raio usado para arredondar cada canto da borda. |

     {style="table-layout:auto"}

   - (Opcional) Especifique os nomes de **[!UICONTROL CSS classes]** da folha de estilos atual para aplicar ao contêiner.

     Separe vários nomes de classe com um espaço.

   - Insira valores, em pixels, para que **[!UICONTROL Margins and Padding]** determine as margens externas e o preenchimento interno do contêiner de código.

     Insira os valores correspondentes no diagrama.

     | Área de contêiner | Descrição |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. Opções: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. Opções: `Top` / `Right` / `Bottom` / `Left` |

[1]: https://fonts.google.com/

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
