---
title: Tags de marcação
description: Saiba mais sobre tags de marcação que contêm trechos de código para fazer referência a um objeto em seu armazenamento.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# Tags de marcação

Uma tag de marcação é uma diretiva que contém um trecho de código com uma referência relativa a um objeto no armazenamento, como uma variável, URL, imagem ou bloco. As tags de marcação podem ser usadas em qualquer lugar em que o editor estiver disponível e incorporado no HTML de [email](email-templates.md) e [informativo](../merchandising-promotions/newsletter-template.md) bem como outros tipos de [conteúdo](../content-design/introduction.md#content).

As tags de marcação são colocadas entre chaves e duplas e podem ser geradas pela ferramenta Widget ou digitadas diretamente no conteúdo HTML. Por exemplo, em vez de codificar o caminho completo para uma página, você pode usar uma tag de marcação para representar a URL de armazenamento. As tags de marcação apresentadas nos exemplos a seguir incluem:

{{$include /help/_includes/directives-caution.md}}

## Variável personalizada

A tag de marcação Variável pode ser usada para inserir um [variável personalizada](variables-custom.md) em um modelo de email, blocos, informativos e páginas de conteúdo.

\{\{CustomVar code= &quot;my_custom_variable&quot;}}

## Armazenar URL

A tag de marcação de URL de loja representa o URL de base do site e é usada como um substituto para a primeira parte de um URL completo, incluindo o nome de domínio. Há duas versões dessa tag de marcação: uma que vai diretamente para o armazenamento e a outra com uma barra (`/`) no final usado quando um caminho é adicionado.

\{\{store url=&#39;apparel/shoes/womens&#39;}}

## URL de mídia

A tag de marcação de URL de mídia dinâmica representa o local e o nome do arquivo de uma imagem armazenada em uma rede de entrega de conteúdo (CDN). A tag pode ser usada para colocar uma imagem em um modelo de página, bloco, banner ou email.

\{\{media url=&#39;shoes-sale.jpg&#39;}}

## ID do bloco

A tag de marcação de ID de bloco é uma das mais fáceis de usar e pode ser usada para colocar um bloco diretamente em uma página do CMS ou até mesmo aninhado dentro de outro bloco. Você pode usar essa técnica para modificar um bloco para promoções ou idiomas diferentes. A tag de marcação de ID de bloco faz referência a um bloco por seu identificador.

\{\{block id=&#39;block-id&#39;}}

## Tag de modelo

Uma tag de modelo faz referência a um arquivo de modelo PHTML e pode ser usada para exibir o bloco em uma página CMS ou em um bloco estático. O código no exemplo a seguir pode ser adicionado a uma página ou bloco para exibir o formulário Fale Conosco.

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_Contact::form.phtml&quot;}}

O código no próximo exemplo pode ser adicionado a uma página ou bloco para exibir uma lista de produtos em uma categoria específica, por ID de categoria.

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}}

## Código do widget

A ferramenta Widget pode ser usada para exibir listas de produtos ou inserir links complexos, como um que vai para uma página de produto específica, com base na ID do produto. O código gerado inclui a referência do bloco, o local do módulo de código e o modelo PHTML correspondente. Depois que o código é gerado, é possível copiá-lo e colá-lo de um local para outro.

O código no exemplo a seguir pode ser adicionado a uma página ou bloco para exibir a lista de novos produtos.

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

O código no próximo exemplo pode ser adicionado a uma página ou bloco para exibir um link para um produto específico, por ID do produto.

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;My Product Link&quot; title=&quot;My Product Link&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## Usar tags de marcação em links

É possível usar tags de marcação com tags de âncora HTML e vincular diretamente a qualquer página na loja. O link pode ser incorporado a páginas de conteúdo, blocos ou modelos de email e boletim informativo. Também é possível usar essa técnica para vincular uma imagem a uma página específica.

### Etapa 1. Identificar o URL de destino

Se possível, navegue até a página que deseja vincular e copie o URL completo da barra de endereços do seu navegador. A parte do URL necessária vem após a variável `.com/`. Caso contrário, copie a chave do URL da página CMS que você deseja usar como destino do link.

#### URL completo da página de categoria

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### URL completo da página do produto

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### URL completo da página CMS

`https://mystore.com/about-us`

### Etapa 2. Adicionar a marcação ao URL

A tag Store URL representa o URL de base do site e é usada como um substituto para a parte do endereço HTTP do URL de armazenamento, incluindo o nome de domínio e `.com`. Há duas versões da tag, que podem ser usadas dependendo dos resultados que você deseja obter.

`store direct_url` - Links diretamente para uma página.

`store url` - Coloca uma barra no final, para que referências adicionais possam ser anexadas como um caminho.

Nos exemplos a seguir, a Chave de URL está entre aspas simples e a tag de marcação inteira está entre chaves duplas. Quando usada com uma tag de âncora, a tag de marcação é colocada dentro das aspas duplas da âncora. Para evitar confusão, é possível alternar usando aspas simples e duplas para cada conjunto aninhado de aspas.

Se você estiver começando com um URL completo, exclua o endereço HTTP (`http://` ou `https://`) parte do URL, até e incluindo o `.com/`. Em seu lugar, insira a tag de marcação Armazenar URL, por meio das aspas simples de abertura.

#### Armazenar tag de marcação de URL

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

Caso contrário, insira a primeira parte da tag Store URL markup e cole a chave ou o caminho do URL copiado anteriormente.

### Armazenar tag de marcação de URL com chave de URL

`{{store url=`

Para concluir a tag de marcação, insira as aspas duplas e as chaves duplas de fechamento.

`{{store url='apparel/shoes/womens'}}`

### Etapa 3. Preencha a tag de âncora

Envolva a tag de marcação concluída em uma tag de âncora, usando a tag de marcação em vez do URL de destino. Em seguida, adicione o texto do link e feche a tag de âncora.

#### Marcação na tag de âncora

\&lt;a href=&quot;\{\{markup tag goes here}}&quot;>Texto do link\&lt;/a>

Cole a tag âncora preenchida no código de qualquer página, bloco, banner ou modelo de email do CMS onde deseja que o link apareça.

### Link completo com marcação

\&lt;a href=&quot;\{\{store url=&amp;#39;apparel/shoes&amp;#39;}}&quot;>Venda de sapatos\&lt;/a>
