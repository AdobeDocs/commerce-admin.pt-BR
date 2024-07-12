---
title: Lista de produtos
description: Saiba mais sobre a página _[!UICONTROL Products]_ no Admin, onde você pode criar produtos e editar os existentes.
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 270a549af1a3eeda6c01f806171ede9d8a41b5d2
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Lista de produtos

Todos os produtos no catálogo podem ser acessados na página _[!UICONTROL Products]_do Administrador, onde você pode criar produtos e editar os existentes. Para uma instalação em vários sites, cada site pode oferecer uma seleção diferente de produtos para venda no mesmo catálogo.

A lista _[!UICONTROL Products]_inclui todos os produtos no catálogo, indica os sites em que eles estão disponíveis e se estão habilitados para venda no momento. Em instalações B2B do Adobe Commerce com [catálogos compartilhados](../b2b/catalog-shared.md) habilitados, a grade inclui uma coluna que indica quais produtos têm preços de desconto alternativos em um catálogo compartilhado.

Você pode navegar pela página da lista por página ou pesquisar por produtos específicos. Use os [controles](../getting-started/admin-grid-controls.md) padrão para classificar e filtrar a lista e aplicar [ações](../getting-started/admin-actions-control.md) aos produtos selecionados.

![Grade de produtos](./assets/products-grid.png){width="700" zoomable="yes"}

## Limitar exibição do produto

Para melhorar o desempenho de catálogos grandes, é recomendável limitar o número de produtos exibidos na grade. É possível limitar as grades de produtos exibidas para:

- Página Produtos
- Adicionar produtos relacionados/venda adicional/venda cruzada
- Adicionar produtos ao produto do pacote
- Adicionar produtos ao produto do grupo
- Criar pedido (Administrador)

Essa configuração da limitação de exibição do produto é desabilitada por padrão. Ao ativá-la, é possível limitar o número de produtos na grade a um valor específico. Se estiver ativado e o número de produtos correspondentes para a exibição de grade for maior que o limite de registros, uma coleção limitada de registros será retornada. Quando o limite é atingido, o total de registros encontrados, o número de registros selecionados e os elementos de paginação não aparecem no cabeçalho da grade.

>[!NOTE]
>
>Se não quiser que a grade de produtos seja limitada, use filtros com mais precisão para produzir uma coleção com menos itens do que o número especificado no campo _[!UICONTROL Records Limit]_.

**_Para configurar a limitação de exibição do produto:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL Admin]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Admin Grids]** e faça o seguinte:

   - Defina **[!UICONTROL Limit Number of Products in Grid]** como `Yes`.

   - (Opcional) Insira um valor no campo **[!UICONTROL Records Limit]** para limitar o número de produtos na grade a um valor específico. O valor mínimo padrão é `20000`.

   ![Configurações de grades de administração](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Controles de página

| Controle | Descrição |
|--- |--- |
| [!UICONTROL Add Product] | Inicia o processo para criar um novo produto simples. Para escolher um tipo de produto específico, clique na seta para baixo. Opções: [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | Lista todas as ações que podem ser aplicadas aos produtos selecionados na lista. Para aplicar uma ação a um produto ou grupo de produtos, marque a caixa de seleção na primeira coluna de cada produto. Opções: `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | Inicia uma pesquisa no catálogo com base nos filtros atuais. |
| [!UICONTROL Default View] | Indica o layout de coluna da grade atual. Se houver exibições de colunas de grade salvas, você poderá escolher outra. |
| [!UICONTROL Columns] | Lista todas as ações que podem ser aplicadas aos produtos selecionados na lista. Para aplicar uma ação a um produto ou grupo de produtos, marque a caixa de seleção na primeira coluna de cada produto. |
| [!UICONTROL Search by keyword] | A caixa de pesquisa, no canto superior esquerdo, é usada para localizar produtos por palavra-chave. |
| [!UICONTROL Edit] | Abre o produto no modo de edição. Você pode fazer a mesma coisa clicando em qualquer lugar na linha. |

{style="table-layout:auto"}

## Colunas padrão

| Coluna | Descrição |
|--- |--- |
| (Caixa de seleção) | Seleciona vários registros para serem sujeitos a uma ação. A caixa de seleção na primeira coluna de cada registro selecionado está marcada. Opções: <br/>**[!UICONTROL Select All]**- Seleciona todos os registros encontrados que correspondem às configurações de filtro atuais.<br/>**[!UICONTROL Select All on This Page]** - Seleciona somente os registros encontrados na página atual que correspondem às configurações de filtro. |
| [!UICONTROL ID] | Um número sequencial exclusivo atribuído quando um novo produto é salvo pela primeira vez. |
| [!UICONTROL Thumbnail] | Exibe uma miniatura da imagem principal do produto. |
| [!UICONTROL Name] | O nome do produto. |
| [!UICONTROL Type] | O tipo de produto. |
| [!UICONTROL Attribute Set] | O nome do conjunto de atributos usado como modelo para o produto. |
| [!UICONTROL SKU] | A Unidade de Manutenção de Estoque exclusiva atribuída ao produto. |
| [!UICONTROL Price] | O preço unitário do produto. |
| [!UICONTROL Quantity] | A quantidade em estoque. |
| [!UICONTROL Salable Quantity] | A soma de todas as unidades disponíveis deste produto. |
| [!UICONTROL Visibility] | Indica onde o produto está visível no catálogo. Opções: `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | Indica o status do produto. Opções: `Enabled` e `Disabled` |
| [!UICONTROL Websites] | Indica os sites nos quais o produto está disponível. |
| [!UICONTROL Remote Media URL] | Se os ativos de mídia do produto forem gerenciados usando a [Integração do AEM Assets para Commerce](../content-design/aem-assets.md), esse campo exibirá a URL para exibir o ativo do Commerce AEM no armazenamento do Gerenciamento de ativos digitais do, o repositório centralizado onde os ativos são mantidos. Esse campo é exibido somente se a integração do AEM Assets estiver habilitada. |
| [!UICONTROL Action] | Abre o produto no modo Editar. |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponível somente com [Adobe Commerce B2B](./b2b/../introduction.md)) Indica os catálogos compartilhados que contêm preços personalizados para o produto. |

{style="table-layout:auto"}

## Outras colunas

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Short Description] | Breve descrição do produto. |
| [!UICONTROL Special Price From Date] | A primeira data da promoção de preço especial. |
| [!UICONTROL Special Price To Date] | A última data da promoção de preço especial. |
| [!UICONTROL Cost] | O custo real do item. |
| [!UICONTROL Manufacturer] | O fabricante do produto. |
| [!UICONTROL Meta Keywords] | Metapalavras-chave do produto. |
| [!UICONTROL Color] | A cor do produto. |
| [!UICONTROL Set Product as New from Date] | A primeira data do produto definido como uma nova promoção. |
| [!UICONTROL Set Product as New to Date] | A última data do produto definido como uma nova promoção. |
| [!UICONTROL Active From / To] | As datas de início e término do produto. |
| [!UICONTROL Layout] | O layout do produto. |
| [!UICONTROL Minimum Advertised Price] | O preço mínimo anunciado do produto. |
| [!UICONTROL Allow Gift Message] | A mensagem de presente para clientes que compram um cartão-presente. |
| [!UICONTROL Special Price] | Preço especial do produto. |
| [!UICONTROL Weight] | O peso do produto. |
| [!UICONTROL Meta Title] | Metatítulo do produto. |
| [!UICONTROL Meta Description] | A descrição dos metadados do produto. |
| [!UICONTROL Country of Manufacture] | O país de fabricação. |
| [!UICONTROL New Theme] | Tema personalizado aplicado ao produto. |
| [!UICONTROL URL Key] | A Chave de URL do produto. |
| [!UICONTROL Tax Class] | A classe de imposto do produto. |
| [!UICONTROL Allow Gift Message] | Exibe a disponibilidade da opção de mensagem de presente para o produto. |

{style="table-layout:auto"}
