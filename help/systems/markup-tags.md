---
title: Tags de marcação
description: Saiba mais sobre tags de marcação que contêm trechos de código para fazer referência a um objeto em seu armazenamento.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
TQID: https://experienceleague.adobe.com/Is9ZYbe3G4uXGAcoY8KjaaNVvTdHgYpTvmZBpj7SQpU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 5ad33b22f893986a79bbb746f476e8490080fb0d
workflow-type: tm+mt
source-wordcount: 914
ht-degree: 0%

---

# Tags de marcação

Uma tag de marcação é uma diretiva que contém um trecho de código com uma referência relativa a um objeto no armazenamento, como uma variável, URL, imagem ou bloco. As marcas de marcação podem ser usadas em qualquer lugar em que o editor estiver disponível e incorporado à HTML de modelos de [email](email-templates.md) e [informativo](../merchandising-promotions/newsletter-template.md), bem como de outros tipos de [conteúdo](../content-design/introduction.md#content).

As tags de marcação são colocadas entre chaves e duplas e podem ser geradas pela ferramenta Widget ou digitadas diretamente no conteúdo do HTML. Por exemplo, em vez de codificar o caminho completo para uma página, você pode usar uma tag de marcação para representar a URL de armazenamento. As tags de marcação apresentadas nos exemplos a seguir incluem:

{{$include /help/_includes/directives-caution.md}}

## Variável personalizada

A marca de marcação Variável pode ser usada para inserir uma [variável personalizada](variables-custom.md) em um modelo de email, blocos, informativos e páginas de conteúdo.

`{{CustomVar code= "my_custom_variable"}}`

## Armazenar URL

A tag de marcação de URL de loja representa o URL de base do site e é usada como um substituto para a primeira parte de um URL completo, incluindo o nome de domínio. Há duas versões dessa marca de marcação: Uma que vai diretamente para o armazenamento e a outra com uma barra (`/`) no final usada quando um caminho é adicionado.

`{{store url='apparel/shoes/womens'}}`

## URL de mídia

A tag de marcação de URL de mídia dinâmica representa o local e o nome do arquivo de uma imagem armazenada em uma rede de entrega de conteúdo (CDN). A tag pode ser usada para colocar uma imagem em um modelo de página, bloco, banner ou email.

`{{media url='shoe-sale.jpg'}}`

## ID do bloco

A tag de marcação de ID de bloco é uma das mais fáceis de usar e pode ser usada para colocar um bloco diretamente em uma página do CMS ou até mesmo aninhado dentro de outro bloco. Você pode usar essa técnica para modificar um bloco para promoções ou idiomas diferentes. A tag de marcação de ID de bloco faz referência a um bloco por seu identificador.

`{{block id='block-id'}}`

## Tag de modelo

Uma tag de modelo faz referência a um arquivo de modelo PHTML e pode ser usada para exibir o bloco em uma página do CMS ou em um bloco estático. O código no exemplo a seguir pode ser adicionado a uma página ou bloco para exibir o formulário Fale Conosco.

`{{block class="Magento\Contact\Block\ContactForm" name="contactForm" template="Magento_Contact::form.phtml"}}`

O código no próximo exemplo pode ser adicionado a uma página ou bloco para exibir uma lista de produtos em uma categoria específica, por ID de categoria.

`{{block type="catalog/product_list" category_id="22" template="catalog/product/list.phtml"}}`

## Código do widget

A ferramenta Widget pode ser usada para exibir listas de produtos ou inserir links complexos, como um que vai para uma página de produto específica, com base na ID do produto. O código gerado inclui a referência do bloco, o local do módulo de código e o modelo PHTML correspondente. Depois que o código é gerado, é possível copiá-lo e colá-lo de um local para outro.

O código no exemplo a seguir pode ser adicionado a uma página ou bloco para exibir a lista de novos produtos.

`{{widget type="catalog/product_widget_new" display_type="new_products" products_count="10" template="catalog/product/widget/new/content/new_grid.phtml"}}`

O código no próximo exemplo pode ser adicionado a uma página ou bloco para exibir um link para um produto específico, por ID do produto.

`{{widget type="catalog/product_widget_link" anchor_text="My Product Link" title="My Product Link" template="catalog/product/widgetlink/link_block.phtml" id_path="product/31"}}`

## Usar tags de marcação em links

É possível usar tags de marcação com tags de âncora do HTML e vincular diretamente a qualquer página na loja. O link pode ser incorporado a páginas de conteúdo, blocos ou modelos de email e boletim informativo. Também é possível usar essa técnica para vincular uma imagem a uma página específica.

### Etapa 1. Identificar o URL de destino

Se possível, navegue até a página que deseja vincular e copie o URL completo da barra de endereços do seu navegador. A parte da URL necessária vem após `.com/`. Caso contrário, copie a Chave do URL da página do CMS que você deseja usar como destino do link.

#### URL completo da página de categoria

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### URL completo da página do produto

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### URL completo da página do CMS

`https://mystore.com/about-us`

### Etapa 2. Adicionar a marcação ao URL

A marca Armazenar URL representa a URL de base do seu site e é usada como um substituto para a parte do endereço HTTP da URL de armazenamento, incluindo o nome de domínio e `.com`. Há duas versões da tag, que podem ser usadas dependendo dos resultados que você deseja obter.

`store direct_url` - Vincula diretamente a uma página.

`store url` - Coloca uma barra no final, para que referências adicionais possam ser anexadas como um caminho.

Nos exemplos a seguir, a Chave de URL está entre aspas simples e a tag de marcação inteira está entre chaves duplas. Quando usada com uma tag de âncora, a tag de marcação é colocada dentro das aspas duplas da âncora. Para evitar confusão, é possível alternar usando aspas simples e duplas para cada conjunto aninhado de aspas.

Se você estiver começando com uma URL completa, exclua a parte do endereço HTTP (`http://` ou `https://`) da URL, incluindo o `.com/`. Em seu lugar, insira a tag de marcação Armazenar URL, por meio das aspas simples de abertura.

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

`<a href="{{markup tag goes here}}">Link Text</a>`

Cole a tag de âncora preenchida no código de qualquer página, bloco, banner ou modelo de email do CMS em que deseja que o link seja exibido.

### Link completo com marcação

`<a href="{{store url='apparel/shoes'}}">Shoe Sale</a>`

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
