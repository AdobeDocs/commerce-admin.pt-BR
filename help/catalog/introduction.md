---
title: Introdução ao gerenciamento de catálogos
description: Saiba como o catálogo e o escopo do produto funcionam no gerenciamento de catálogo.
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Introdução ao gerenciamento de catálogos

O Adobe Commerce e o Magento Open Source usam o termo _catálogo_ para se referir ao banco de dados do produto como um todo.

Uma das áreas mais importantes na criação e no gerenciamento de sua loja é a criação de produtos e categorias. O Administrador fornece várias ferramentas que você usa para a configuração inicial da sua loja e para manter sua loja e otimizar seus negócios.

>[!TIP]
>
>O Inventory management para Adobe Commerce e Magento Open Source oferece as ferramentas para gerenciar o inventário de produtos. Comerciantes com uma única loja para vários depósitos, lojas, locais de retirada, entregadores diretos e muito mais podem usar esses recursos para manter quantidades para vendas e controlar entregas para ordens completas. Para obter mais informações sobre esses recursos e como usá-los para gerenciar estoque em vários locais, consulte o [Guia do Usuário do Inventory management](../inventory-management/introduction.md).

## Escopo do catálogo

O acesso aos dados do catálogo é determinado por vários fatores, incluindo a configuração [scope](../getting-started/websites-stores-views.md#scope-settings), a configuração do catálogo e a [categoria raiz](category-root.md) atribuída ao armazenamento. O catálogo inclui produtos que estão habilitados e disponíveis para venda e produtos que atualmente não estão disponíveis para venda.

Em vendas, o termo _catálogo_ geralmente se refere a uma seleção de produtos com curadoria que está disponível para venda. Por exemplo, uma loja pode ter um &quot;Catálogo de primavera&quot; e um &quot;Catálogo de outono&quot;.

Como o índice de um catálogo impresso, o menu principal da sua loja — ou a _navegação superior_ — organiza os produtos por categoria para facilitar aos clientes encontrar o que desejam. O menu principal é baseado em uma _categoria raiz_, que é um contêiner do menu atribuído ao armazenamento. Como as opções de menu específicas são definidas no nível de exibição de loja, cada exibição pode ter um menu principal diferente com base na mesma categoria raiz. Em cada menu, você pode oferecer uma seleção de produtos com curadoria adequada para a loja.

![Diagrama de hierarquia de catálogo](./assets/catalog-hierarchy-scope.svg){width="550"}

## Escopo do produto

Para instalações com vários sites, lojas e visualizações, a configuração [scope](../getting-started/websites-stores-views.md#scope-settings) determina onde os produtos estão disponíveis para venda e as informações sobre o produto disponíveis para cada visualização da loja. Inicialmente, todos os produtos criados são publicados no site padrão, na loja e na visualização da loja.

![diagrama de repositório de vários sites](./assets/scope-multisite.svg){width="550"}

Se você tiver apenas um único armazenamento com o modo de exibição padrão, poderá executar seu armazenamento no [modo de armazenamento único](../getting-started/websites-stores-views.md#single-store-mode) para ocultar as configurações de escopo. No entanto, se o armazenamento tiver várias exibições, um indicador de escopo aparecerá abaixo do nome de cada campo.

- Para editar informações do produto para um modo de exibição específico, use o controle _Modo de Exibição de Loja_, no canto superior esquerdo, para escolher o modo de exibição. Controles adicionais se tornam disponíveis para qualquer campo que possa ser editado no nível de visualização da loja.

- Para definir o escopo de um produto em uma instalação multissite, consulte a seção [Produto em Sites](settings-basic-websites.md) das informações sobre o produto.

O processo de editar um produto para uma visualização da loja é como adicionar uma camada de informações do produto específica para a visualização.

Você só pode editar ou atribuir produtos ao site para o qual tem permissões, não a todos os sites aos quais o produto está atribuído.

Embora a exibição de loja _Espanhol_ esteja selecionada no exemplo a seguir, as informações do produto ainda aparecerão no idioma original da exibição de loja padrão. Para traduzir as informações do produto, você deve alternar para o modo de exibição de loja _Espanhol_ e traduzir os campos de texto — como título do produto, descrição e metadados. Para obter mais informações, consulte [Localizar produtos](../stores-purchase/store-localize.md#localize-products).

## Editar um produto para uma exibição diferente

>[!NOTE]
>
>O escopo _Todas as Exibições da Loja_ está desabilitado para usuários Administradores restritos a um escopo específico quando o produto também é publicado fora do escopo permitido. O primeiro escopo disponível para edição é selecionado por padrão porque os usuários restritos não podem executar ações _globais_ ou ações que afetam escopos onde eles não têm acesso.

1. No canto superior esquerdo, defina **[!UICONTROL Store View]** para o modo de exibição específico a ser editado.

1. Para confirmar a alteração do escopo, clique em **[!UICONTROL OK]**.

1. Atualize o campo com o novo valor para a exibição de loja.

   Uma caixa de seleção aparece abaixo de qualquer campo que possa ser editado para a visualização de loja. Para substituir o valor padrão, desmarque a caixa de seleção **Usar valor padrão**.

   ![Traduzindo nome do produto para exibição de loja em espanhol](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. No canto superior esquerdo, defina o seletor de **[!UICONTROL Store View]** novamente como o padrão.

1. Para verificar a alteração no armazenamento, faça o seguinte:

   - No canto superior direito, clique na seta de menu _Admin_ e escolha **[!UICONTROL Customer View]**.

     ![Visualização de cliente](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - No canto superior direito da loja, defina o **[!UICONTROL Language Chooser]** para o modo de exibição de loja do produto que você editou e localize o produto que você editou para o modo de exibição.

     ![Seletor de idiomas](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
