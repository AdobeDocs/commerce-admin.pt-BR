---
title: Localização da loja
description: Saiba como localizar uma visualização de loja ou loja.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Localização da loja

A maioria do texto que parece ser codificado nas páginas em toda a loja pode ser alterada instantaneamente para um idioma diferente, alterando o local da exibição. Alterar o local não traduz realmente o texto palavra por palavra, mas simplesmente faz referência a uma tabela de tradução diferente que fornece o texto da interface usado em toda a loja. O texto que pode ser alterado inclui títulos de navegação, rótulos, botões e links como _Meu carrinho_ e _Minha conta_. Você também pode usar a variável [Tradução integrada](../configuration-reference/advanced/developer.md) ferramenta para retocar o texto na interface.

Os pacotes de idiomas podem ser encontrados em [Traduções e localização][1]{:target=&quot;_blank&quot;} no Commerce Marketplace. Novas extensões são adicionadas continuamente ao Marketplace, portanto, verifique com frequência.

## Etapa 1: instalar um pacote de idiomas

Siga as instruções padrão para instalar a extensão de pacote de idiomas. Para obter informações detalhadas sobre a instalação de uma extensão, consulte [Instalação geral da CLI][2] no _Guia de extensões_.

## Etapa 2: criar uma exibição de loja para o idioma

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Clique em **[!UICONTROL Create Store View]**.

1. Defina as opções para a nova exibição de loja:

   - **[!UICONTROL Store]** — Escolha o armazenamento que é o pai da exibição.

   - **[!UICONTROL Name]** — Digite um nome para a exibição de armazenamento. Por exemplo: Português.

     No cabeçalho da loja, o nome aparece no campo _seletor de idioma_.

   - **[!UICONTROL Code]** — Insira um código em caracteres minúsculos para identificar a exibição. Por exemplo: `portuguese`.

   - **[!UICONTROL Status]** — Para ativar a visualização, defina como `Enabled`.

   - **[!UICONTROL Sort Order]** — (Opcional) Informe um número para determinar a sequência na qual essa view é listada com outras views.

1. Quando terminar, clique em **[!UICONTROL Save Store View]**.

## Etapa 3: alterar o local da exibição de loja

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No canto superior esquerdo, defina **[!UICONTROL Store View]** à visualização específica onde a configuração deve ser aplicada.

1. Quando solicitado a confirmar a alternância do escopo, clique em **[!UICONTROL OK]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Locale Options]** seção.

1. Limpe a **[!UICONTROL Use Website]** caixa de seleção e definir **[!UICONTROL Locale]** ao idioma que você deseja atribuir à exibição.

   Se houver várias variações do idioma disponível, escolha uma para a região ou dialeto específico.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

   Depois de alterar o idioma do local, o conteúdo restante que você criou, incluindo nomes e descrições de produtos, categorias, [CMS](../content-design/page-translate.md) as páginas e os blocos devem ser traduzidos separadamente para cada exibição de loja.

## Localizar produtos

Se sua loja tiver várias visualizações em diferentes idiomas, os mesmos produtos estarão disponíveis em cada visualização de loja. Você pode usar as mesmas informações básicas do produto, como SKU, preço e nível de inventário, independentemente do idioma. Em seguida, traduza somente o nome do produto, os campos de descrição e os metadados, conforme necessário, para cada idioma.

### Etapa 1: Traduzir campos de produto

1. No _Admin_ barra lateral, vá para  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Na grade, localize o produto a ser traduzido e abra-o no modo de edição.

1. No canto superior esquerdo, defina **[!UICONTROL Store View]** à exibição para a tradução e clique em **[!UICONTROL OK]** quando solicitado a confirmar.

1. Para cada campo a ser editado, faça o seguinte:

   - Desmarque a opção **[!UICONTROL Use Default Value]** à direita do campo.

   - Cole ou digite o texto traduzido no campo.

   Certifique-se de traduzir todos os campos de texto, incluindo [imagem](../catalog/catalog-images-video.md) rótulos e texto alternativo, [Otimização do mecanismo de pesquisa](../catalog/product-search-engine-optimization.md) campos e qualquer [Opções personalizadas](../catalog/settings-advanced-custom-options.md) informações.

1. Quando terminar, clique em **[!UICONTROL Save]**.

### Etapa 2: Traduzir rótulos de campo

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Na lista, localize o atributo a ser traduzido e aberto no modo de edição.

1. No painel esquerdo, escolha **[!UICONTROL Manage Labels]**.

1. No _[!UICONTROL Manage Titles]_insira um rótulo traduzido para cada exibição de loja.

   ![Inserir rótulos traduzidos](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Attribute]**.

### Etapa 3: Traduzir todas as categorias

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **Categorias**.

1. No canto superior esquerdo, defina **[!UICONTROL Store View]** à exibição para a tradução e clique em **[!UICONTROL OK]** quando solicitado a confirmar.

1. Na árvore, localize a categoria a ser traduzida e abra-a no modo de edição.

1. Para _Informações básicas_, traduzir **[!UICONTROL Category Name]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o _[!UICONTROL Content]_seção e tradução **[!UICONTROL Description]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Search Engine Optimization Settings]** e traduza os seguintes campos:

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. No _[!UICONTROL Search Engine Optimization Settings]_faça o seguinte para traduzir a **[!UICONTROL URL Key]**:

   - Limpe a **[!UICONTROL Use Default Value]** à direita do campo.

   - Insira o texto traduzido.

   - Certifique-se de que a variável **[!UICONTROL Create Permanent Redirect for old URL]** está marcada.

   ![Traduzir a chave do URL](./assets/category-translate-url-key.png)

1. Quando terminar, clique em **[!UICONTROL Save Category]**.

1. Repita o processo para todas as categorias usadas no armazenamento.

### Etapa 4: Traduzir atributos do produto e opções de atributos

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Selecione o atributo a ser traduzido.

1. Escolher **[!UICONTROL Manage Labels]** à esquerda e defina o **[!UICONTROL Managed Titles]** opções para definir as traduções de título do atributo.

1. Escolher **[!UICONTROL Properties]** à esquerda e insira as opções de atributo traduzido nas **[!UICONTROL Manage Options]** seção.

   ![Gerenciar opções](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
