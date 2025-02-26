---
title: Referência de atributos de dados do produto
description: Use essa referência de atributos de dados do produto ao trabalhar com importações e exportações de dados do produto.
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: 976efad9fb4bb53f6f102fde534001d254cd3b9c
workflow-type: tm+mt
source-wordcount: '2496'
ht-degree: 0%

---

# Referência de atributos de dados do produto

A tabela a seguir lista os atributos de uma exportação de produto típica, na ordem padrão em que são exibidos. Cada atributo é representado no arquivo CSV como uma coluna e os registros de produto são representados por linhas. As colunas que começam com um sublinhado contêm dados de serviço, como propriedades ou valores de opção para dados complexos. Você pode [exportar](data-export.md) um produto do seu catálogo para ver como cada atributo é representado nos dados.

A instalação usada para exportar esses dados tem os dados de amostra instalados e tem dois sites e várias exibições de loja. Embora esta lista inclua todas as colunas que normalmente são exportadas, o `sku` é o único valor necessário. Para importar dados, você pode incluir apenas as colunas com alterações. `sku` deve ser a primeira coluna, mas a ordem do restante dos atributos não importa.

## Estrutura de arquivo CSV de produto simples

| Atributo | Descrição |
|--- |--- |
| `sku` | (Obrigatório) A unidade de manutenção de estoque é um identificador alfanumérico exclusivo usado para rastrear o inventário. Um SKU pode ter até 64 caracteres. Por exemplo: `sku123`<br/>**_Observação:_**uma SKU com mais de 64 caracteres faz com que a importação falhe. |
| `store_view_code` | Identifica as exibições de loja específicas em que o produto está disponível. Se estiver em branco, o produto estará disponível na visualização padrão da loja. Por exemplo: `storeview1`, `english`, `spanish` |
| `attribute_set_code` | Atribui o produto a um conjunto de atributos ou modelo de produto específico, de acordo com o tipo de produto. Por exemplo: `default`<br><br>Depois que o produto é criado, o conjunto de atributos não pode ser alterado usando a funcionalidade de importação. No entanto, você pode alterar o conjunto de atributos de Admin e reexportar o produto para atualizar o arquivo CSV. |
| `product_type` | Indica o tipo de produto. Valores:<br/>`simple` — Itens tangíveis que normalmente são vendidos como unidades únicas ou em quantidades fixas.<br/>`grouped` — Um grupo de produtos separados que são vendidos como um conjunto.<br/>`configurable` — Um produto com várias opções que o cliente deve selecionar antes de fazer uma compra. O inventário pode ser gerenciado para cada conjunto de variações porque representam um produto separado com uma SKU distinta. Por exemplo, uma combinação de cor e tamanho para um produto configurável está associada a uma SKU específica no catálogo.<br/>`virtual` — Um produto incorpóreo que não requer remessa e não é mantido em estoque. Os exemplos incluem serviços, associações e assinaturas.<br/>`bundle` — Um conjunto de produtos personalizáveis de produtos simples vendidos em conjunto. |
| `categories` | Indica cada categoria atribuída ao produto. Separe as categorias e subcategorias com uma barra. Para indicar vários caminhos de categoria, separe cada caminho com uma barra vertical \| símbolo. Por exemplo: `Default Category/Gear\|Default Category/Gear/Bags` |
| `product_websites` | O código de cada site onde o produto está disponível. Um único produto pode ser atribuído a vários sites ou limitado a um. Se especificar vários sites, separe-os com vírgula e sem espaço. Por exemplo: `base` ou `base,website2` |
| `name` | O nome do produto é exibido em todas as listas de produtos e é o nome que os clientes usam para identificar o produto. |
| `description` | A descrição do produto fornece informações detalhadas sobre ele e pode incluir tags simples do HTML. |
| `short_description` | O uso da descrição curta do produto depende do tema. Ele pode aparecer nas listagens de produtos e, às vezes, é usado nas listagens de feed RSS enviadas para sites de compras. |
| `weight` | O peso do produto individual. O peso real do produto é determinado pela transportadora no momento da remessa. |
| product_online | Determina se o produto está disponível para venda na loja. Valores:<br/>`1` — (Sim) O produto está habilitado e disponível para venda.<br/>`2` — (Não) O produto está desabilitado e não está disponível para venda. |
| `tax_class_name` | O nome da classe de imposto associada a este produto. |
| `visibility` | Determina se o produto está visível no catálogo e se foi disponibilizado para pesquisa. Valores:<br/>`Not Visible Individually` — O produto não está incluído nas listagens de produtos, embora possa estar disponível como uma variação de outro produto.<br/>`Catalog` — O produto aparece em todas as listagens de catálogos.<br/>`Search` — O produto está disponível para operações de pesquisa.<br/>`Catalog, Search` — O produto está incluído nas listagens do catálogo e também está disponível para pesquisa. |
| `price` | O preço que o produto é oferecido para venda em sua loja. |
| `special_price` | O preço com desconto do produto durante o período especificado. |
| `special_price_from_date` | A data inicial do período em que o preço especial está em vigor. |
| `special_price_to_date` | A última data do período de tempo em que o preço especial está em vigor. |
| `url_key` | A parte do URL que identifica o produto. O valor padrão é baseado no nome do produto. Por exemplo: `product-name` |
| save_rewrites_history | Quando fornecido com o valor `1` com um novo `url_key`, uma nova regravação de URL 301 é gerada para que o URL antigo seja redirecionado para o novo URL. |
| `meta_title` | O metatítulo é exibido na barra de título e na guia do navegador e nas listas de resultados da pesquisa. O metatítulo deve ser exclusivo do produto, incorporar palavras-chave de alto valor e ter menos de 70 caracteres. |
| `meta_keywords` | As palavras-chave meta são visíveis somente em mecanismos de pesquisa e são ignoradas por alguns mecanismos de pesquisa. Escolha palavras-chave de alto valor, separadas por vírgula. Por exemplo: `keyword1`, `keyword2`, `keyword3` |
| `meta_description` | As meta descrições fornecem uma breve visão geral do produto para listagens de resultados de pesquisa. Idealmente, uma meta descrição deve ter entre 150 e 160 caracteres de comprimento, embora o campo aceite até 255 caracteres. |
| `base_image` | O caminho relativo da imagem principal na página do produto. O Commerce armazena arquivos internamente em uma estrutura de pastas alfabética. Você pode ver o local exato de cada imagem nos dados exportados. Por exemplo: `/sample_data/m/b/mb01-blue-0.jpg`<br/>Para carregar uma nova imagem ou gravar sobre uma imagem existente, digite o nome do arquivo, precedido por uma barra. Por exemplo: `/image.jpg` |
| `base_image_label` | O rótulo associado à imagem base. |
| `small_image` | O nome de arquivo da imagem pequena que é usada em páginas de catálogo, precedida por uma barra. Por exemplo: `/image.jpg` |
| `small_image_label` | O rótulo associado à imagem pequena. Por exemplo: `Small Image 1`, `Small Image 2` |
| `thumbnail_image` | Os nomes dos arquivos de qualquer imagem em miniatura que serão exibidos na galeria na página do produto, precedidos por uma barra. Por exemplo: `/image.jpg` |
| `thumbnail_image_label` | O rótulo associado a quaisquer imagens em miniatura. Por exemplo: `Thumbnail 1`, `Thumbnail 2` |
| `created_at` | Indica a data de criação do produto. A data é gerada automaticamente quando o produto é criado, mas pode ser editada posteriormente. |
| `updated_at` | Indica a data em que o produto foi atualizado pela última vez. |
| `new_from_date` | Especifica a data &quot;de&quot; para novas listagens de produtos e determina se o produto é apresentado como um novo produto. |
| `new_to_date` | Especifica a data &quot;até&quot; para novas listagens de produtos e determina se o produto é apresentado como um novo produto. |
| `display_product_options_in` | Se o produto tiver várias opções, o determinará onde elas são exibidas na página do produto. Valores: Coluna Informações do Produto / Bloquear após a Coluna Informações |
| `map_price` | O preço mínimo anunciado do produto. (Aparece somente se o MAP estiver ativado.) |
| `msrp_price` | O preço de varejo sugerido pelo fabricante para o produto. (Aparece somente se o MAP estiver ativado.) |
| `map_enabled` | Determina se o Preço mínimo anunciado está habilitado na configuração. Valores:<br/>`1` — (Sim) MAP está habilitado.<br/>`0` (ou em branco) — (Não) MAP não está habilitado. |
| `gift_message_available` | Determina se uma mensagem de presente pode ser incluída na compra do produto. Valores:<br/>`1` — (Sim) A opção para incluir uma mensagem de presente é apresentada ao cliente.<br/>`0` (ou em branco) — (Não) A opção para incluir uma mensagem de presente não é apresentada ao cliente. |
| `custom_design` | Lista os temas disponíveis que podem ser aplicados à página do produto. |
| `custom_design_from` | Especifica a data de início quando o tema selecionado é aplicado à página do produto. |
| `custom_design_to` | Especifica a data de término quando o tema selecionado é aplicado à página do produto. |
| `custom_layout_update` | Código XML adicional que é aplicado como uma atualização de layout à página do produto. |
| `page_layout` | Determina o layout da página do produto. Valores:<br/>`No layout updates` — Não é feita nenhuma alteração no layout da página.<br/>`1 column` — Aplica um layout de uma coluna à página do produto.<br/>`2 columns with left bar` — Aplica um layout de duas colunas com uma barra lateral esquerda à página do produto.<br/>`2 columns with right bar` — Aplica um layout de duas colunas com uma barra lateral direita à página do produto.<br/>`3 columns` — Aplica um layout de três colunas à página do produto.<br/>`empty` — Aplica um layout em branco à página do produto. |
| `product_options_container` | Se o produto tiver várias opções, o determinará onde elas são exibidas na página do produto. Valores: Coluna Informações do Produto / Bloquear após a Coluna Informações |
| `msrp_display_actual_price_type` | Determina onde o preço real de um produto é visível para o cliente. Valores:<br/>`In Cart` — Exibe o preço real do produto no carrinho de compras.<br/>`Before Order Confirmation` — Exibe o preço real do produto no final do processo de finalização, antes da confirmação do pedido.<br/>`On Gesture` — Exibe o preço real do produto em um pop-up quando o cliente clica em _Clicar para preço_ ou _O que é isso?Link_. |
| `country_of_manufacture` | Identifica o país onde o produto foi fabricado. |
| `additional_attributes` | Atributos adicionais criados para o produto. Por exemplo: <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | A quantidade do produto atualmente em estoque. |
| `out_of_stock_qty` | O nível de estoque que determina se o produto está indisponível. |
| `use_config_min_qty` | Determina se o valor padrão da configuração é usado e corresponde à caixa de seleção Usar configurações. Valores:<br/>`1` — (Sim) A definição de configuração padrão é usada para o valor deste atributo.<br/>`0` (ou em branco) — (Não) A configuração padrão pode ser substituída pelo valor deste atributo. |
| `is_qty_decimal` | Determina se o atributo de quantidade tem um valor decimal. Valores:<br/>`1` — (Sim) O valor do atributo qty é um valor decimal.<br/>`0` (ou em branco) — (Não) O valor do atributo qty é um número inteiro (inteiro). |
| `allow_backorders` | Determina se a loja permite pedidos pendentes e como eles são gerenciados. |
| `use_config_backorders` | Determina se a configuração padrão para backorders é usada e corresponde ao estado da caixa de seleção Usar configurações. Valores:<br/>`1` — (Sim) O valor do atributo qty é um valor decimal.<br/>`0` (ou em branco) — (Não) O valor do atributo qty é um número inteiro (inteiro). |
| `min_cart_qty` | Especifica a quantidade mínima do item que pode ser comprado em um único pedido. |
| `use_config_min_sale_qty` | Determina se a configuração padrão para quantidade mínima é usada e corresponde ao estado da caixa de seleção Usar configurações. Valores:<br/>`1` — (Sim)<br/>`0` (ou em branco) — (Não) |
| `max_cart_qty` | Especifica a quantidade máxima do produto que pode ser comprado em um único pedido. |
| `use_config_max_sale_qty` | Determina se a configuração padrão para quantidade máxima é usada e corresponde ao estado da caixa de seleção Usar configurações. Valores:<br/>`1` — (Sim)<br/>`0` (ou em branco) — (Não) |
| `is_in_stock` | Indica se o produto está em estoque. |
| `notify_on_stock_below` | Especifica o nível de estoque que aciona uma notificação _de falta de estoque_. |
| `use_config_notify_stock_qty` | Determina se a configuração padrão é usada para acionar a notificação no nível do estoque e corresponde ao estado da caixa de seleção Usar configurações. Valores:<br/>`1` — (Sim)<br/>`0` (ou em branco) — (Não) |
| `manage_stock` | Determina se o controle de estoque é usado para gerenciar o produto. Valores:<br/>`1` — (Sim) Ativa o controle de estoque completo para gerenciar os níveis de estoque do produto.<br/>`0` (ou em branco) — (Não) O sistema não rastreia o número de itens que estão atualmente em estoque. |
| `use_config_manage_stock` | Determina se a configuração padrão para gerenciar o estoque é usada e corresponde ao estado da caixa de seleção Usar configurações. Valores:<br/>`1` — (Sim)<br/>`0` (ou em branco) — (Não) |
| `use_config_qty_increments` | Determina se a configuração padrão para incrementos de quantidade é usada e corresponde ao estado da caixa de seleção Usar configurações. Valores:<br/>`1` — (Sim)<br/>`0` (ou em branco) — (Não) |
| `qty_increments` | Estabelece o número de produtos que compõem um incremento de quantidade. |
| `use_config_enable_qty_inc` | Determina se a configuração padrão para habilitar os incrementos de quantidade é usada e corresponde ao estado da caixa de seleção Usar configurações. Valores:<br/>`1` — (Sim)<br/>`0` (ou em branco) — (Não) |
| `enable_qty_increments` | Determina se os incrementos de quantidade estão habilitados para o produto. |
| `is_decimal_divided` | Determina se partes do produto podem ser enviadas separadamente. Opções: `Yes` / `No` |
| `website_id` | Para instalações com vários sites, o código identifica um site específico em que o produto está disponível. Se estiver em branco, o produto estará disponível em todos os sites. |
| `related_skus` | Lista o SKU de cada produto identificado como um produto relacionado. Por exemplo: `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | Determina a posição (ordem de classificação) das SKUs listadas como Produtos Relacionados na coluna related_skus. Por exemplo: `1,2,3,4` |
| `crosssell_skus` | Lista o SKU de cada produto identificado como venda cruzada. |
| `crosssell_position` | Determina a posição (ordem de classificação) das SKUs listadas como Produtos de Venda Cruzada na coluna `crosssell_skus`. |
| `upsell_skus` | Lista o SKU de cada produto identificado como uma Venda adicional. |
| `upsell_position` | Determina a posição (ordem de classificação) das SKUs listadas como produtos de venda suplementar na coluna `upsell_skus`. |
| `additional_images` | Os nomes de arquivos de qualquer imagem adicional a ser associada ao produto, precedida por uma barra. Por exemplo: `/image.jpg` |
| `additional_image_labels` | Os rótulos associados a quaisquer imagens adicionais. Por exemplo: `Label 1`, `Label 2` |
| `custom_options` | Especifica as propriedades e os valores atribuídos a cada opção personalizada. Por exemplo: <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## Dados de serviço para variações de produtos

| Atributo | Descrição | Aplicável a |
|--- |--- | --- |
| `_super_products_sku` | O SKU gerado para uma variação de produto configurável. Por exemplo: WB03-XS-Green | Produtos configuráveis |
| `_super_attribute_code` | O código de atributo de uma variação de produto configurável. Por exemplo: cor | Produtos configuráveis |
| `_super_attribute_option` | O valor de uma variação de produto configurável. Por exemplo: verde | Produtos configuráveis |
| `_super_attribute_price_corr` | Um ajuste de preço associado a uma variação de produto configurável. | Produtos configuráveis |
| `_associated_sku` | O SKU de um produto associado a um produto agrupado. | Produtos agrupados <br/>Produtos agrupados |
| `_associated_default_qty` | Determina a quantidade do produto associado incluído. | Produtos Configuráveis<br/>Produtos Agrupados<br/>Produtos Agrupados |
| `_associated_position` | Determina a posição do produto associado quando listado com outros produtos associados. | Produtos Configuráveis<br/>Produtos Agrupados<br/>Produtos Agrupados |

{style="table-layout:auto"}

## Atributos complexos de dados do produto

O termo dados complexos refere-se aos dados associados a várias opções de produto. Os seguintes tipos de produtos usam dados originários de produtos separados para criar variações de produtos e várias opções.

- [Configurável](../catalog/product-create-configurable.md)
- [Agrupado](../catalog/product-create-grouped.md)
- [Pacote](../catalog/product-create-bundle.md)

Se exportar um produto configurável, você encontrará os atributos padrão que compõem um produto simples, além dos atributos adicionais necessários para gerenciar dados complexos.

![Produto configurável - dados exportados](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### Produtos configuráveis

| Atributo | Descrição |
|--- |--- |
| `configurable_variation_labels` | Rótulos que identificam variações de produtos. Por exemplo: `Choose Color:` ou `Choose Size:` |
| `configurable_variations` | Descreve os valores associados a uma variação de produto. Por exemplo: `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### Produtos agrupados

| Atributo | Descrição |
|--- |--- |
| `associated_skus` | Identifica as SKUs dos produtos individuais que compõem o grupo. |

{style="table-layout:auto"}

### Produtos do pacote

| Atributo | Descrição |
|--- |--- |
| `bundle_price_type` | Determina se o preço de um item do pacote é fixo ou dinâmico. |
| `bundle_sku_type` | Determina se cada item recebe uma SKU variável, dinâmica, ou se uma SKU fixa é usada para o pacote. Opções: Fixa/Dinâmica |
| `bundle_weight_type` | Determina se o peso de um item do pacote é variável ou fixo. |
| `bundle_values` | Descreve o valor de aprendizado associado a uma opção de pacote. Por exemplo: `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## Atributos de precificação avançada

A Importação/Exportação de Preço Avançado permite atualizar rapidamente as informações de preço para grupos de produtos e preços de camada. O processo para [importar](data-import.md) e [exportar](data-export.md) dados de preço avançado é o mesmo que qualquer outro tipo de entidade. O arquivo CSV de amostra contém preços de camada e grupo para cada tipo de produto compatível com preços avançados. A alteração de preços avançados não afeta o restante do registro do produto.

![Exemplo de dados de exportação - preços avançados](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| Atributo | Descrição |
|--- |--- |
| `sku` | (Obrigatório) A unidade de manutenção de estoque é um identificador alfanumérico exclusivo usado para rastrear o inventário. Um SKU pode ter até 64 caracteres. Por exemplo: `sku123`<br/>**_Observação:_**uma SKU com mais de 64 caracteres faz com que a importação falhe. |
| `tier_price_website` | O [código do site](../stores-purchase/stores.md#add-websites) identifica cada site em que os preços de camada estão disponíveis. Por exemplo: `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | Identifica os [grupos de clientes](../customers/customer-groups.md) nos quais os preços de camada estão disponíveis. Por exemplo: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | Identifica os grupos de clientes em que os preços de camada estão disponíveis. Por exemplo: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | A quantidade do produto que deve ser solicitada para receber o desconto de nível de preço. |
| `tier_price` | O preço de camada com desconto do produto. Para [produtos agrupados](../catalog/product-create-bundle.md), o preço da camada é calculado como uma porcentagem. |
| `group_price_website` | O [código de site](../stores-purchase/stores.md#add-websites) de cada site em que os preços de grupo estão disponíveis. Se especificar vários sites, separe-os com vírgula e sem espaço. Por exemplo: `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | Identifica os grupos de clientes nos quais os preços de grupo estão disponíveis. Por exemplo: `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | O preço de grupo com desconto do produto. Para [produtos agrupados](../catalog/product-create-bundle.md), o preço de grupo é calculado como uma porcentagem. |

{style="table-layout:auto"}
