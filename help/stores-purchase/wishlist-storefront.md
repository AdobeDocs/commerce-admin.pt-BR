---
title: Experiência da vitrine da lista de desejos
description: Saiba mais sobre as ferramentas de gerenciamento da lista de desejos disponíveis para seus clientes na loja.
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Experiência da vitrine da lista de desejos

Uma lista de desejos é uma maneira conveniente para os clientes recuperarem os produtos de que gostam, mas que não estão prontos para comprar. Os itens de uma lista de desejos podem ser compartilhados com outras pessoas ou adicionados ao carrinho de compras. Se o cliente tiver várias listas de desejos, o nome da lista de desejos atual será exibido na parte superior da página. Os clientes podem gerenciar suas listas de desejos no painel de contas. Os administradores de loja também podem ajudar os clientes a gerenciar suas listas de desejos com o Administrador.

![Exemplo de vitrine - Minha lista de desejos](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) A Adobe Commerce oferece suporte ao uso de várias listas de desejos por conta de cliente.

![Magento Open Source](../assets/open-source.svg) A base de código Magento Open Source suporta o uso de uma única lista de desejos por conta de cliente.

## Criar uma lista de desejos

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce)

Na loja, um cliente pode criar uma lista de desejos a partir do painel da conta, uma página de produto, uma página de catálogo e o carrinho de compras.

### Método 1: de uma conta de cliente

1. Na barra lateral do painel da conta, o cliente escolhe **[!UICONTROL My Wish List]**.

1. No canto superior direito, clique em **[!UICONTROL Create New Wish List]**.

1. Insira o Nome da lista de desejos.

1. Para permitir que outros vejam sua lista de desejos, seleciona o **[!UICONTROL Public Wish List]** caixa de seleção

   >[!NOTE]
   >
   >A principal diferença entre `Public` e `Private` listas de desejos é que as listas de desejos privadas não são [pesquisável](wishlist-configuration.md#add-wish-list-search) por meio de listas de desejos.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   ![Criar nova lista de desejos](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### Método 2: na página do catálogo

1. Na loja, o cliente acessa a página do catálogo que contém o produto que deseja adicionar a uma lista de desejos.

1. Passe o mouse sobre o produto.

1. O cliente clica na seta ao lado da _Adicionar à lista de desejos_ e seleciona o **[!UICONTROL Create New Wish List]**.

1. Insere o nome da lista de desejos.

1. Para permitir que outros vejam sua lista de desejos, seleciona o **[!UICONTROL Public Wish List]** caixa de seleção

1. Ao concluir, clique em **[!UICONTROL Save]**.

### Método 3: na página de detalhes do produto

1. Na loja, o cliente acessa a página de detalhes do produto que deseja adicionar a uma lista de desejos.

1. Clica na seta ao lado de **[!UICONTROL Add to Wish List]** e escolhe **[!UICONTROL Create New Wish List]**.

1. Insere o **[!UICONTROL Wish List Name]**.

1. Para permitir que outros vejam sua lista de desejos, seleciona o **[!UICONTROL Public Wish List]** caixa de seleção

1. Ao concluir, clique em **[!UICONTROL Save]**.

   ![Criar nova lista de desejos na página Detalhes do produto](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### Método 4: do carrinho de compras

1. O cliente abre a **[!UICONTROL Shopping Cart]** página.

1. Sob o item, clique na seta ao lado de **[!UICONTROL Move to Wishlist]** e escolhe **[!UICONTROL Create New Wish List]**.

1. Insere o **[!UICONTROL Wish List Name]**.

1. Para permitir que outros vejam sua lista de desejos, seleciona o **[!UICONTROL Public Wish List]** caixa de seleção

1. Ao concluir, clique em **[!UICONTROL Save]**.

![Criar nova lista de desejos na página Carrinho de compras](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## Atualizar a lista de produtos

1. Na lista de desejos, o cliente aponta para o produto para exibir as opções.

1. Para adicionar um **[!UICONTROL Comment]** sobre o produto, insere o texto na caixa abaixo do preço.

   ![Editar opções](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. Para alterar a seleção das opções do produto, clique em **[!UICONTROL Edit]** e faz o seguinte:

   - Atualiza as opções na página de detalhes do produto.
   - Cliques **[!UICONTROL Update Wish List]**.

## Adicionar um produto da lista de desejos ao carrinho

1. Na lista de desejos, o cliente aponta para o produto que você deseja adicionar.

1. Atualiza o **[!UICONTROL Qty]** e edite as outras opções conforme necessário.

1. Cliques **[!UICONTROL Add to Cart]**.

## Compartilhar a lista de desejos

1. Cliques do cliente **[!UICONTROL Share Wishlist]**.

1. Insira o endereço de email de cada pessoa que receberá a lista de desejos, separada por vírgula.

1. Adiciona um **[!UICONTROL Message]** para ser incluído no email.

1. Cliques **[!UICONTROL Share Wish List]**.

   ![Compartilhar sua lista de desejos](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   A mensagem é enviada pelo seu principal [armazenar contato](../getting-started/store-details.md#store-email-addresses) e inclui uma imagem em miniatura de cada produto, com links para sua loja.

   ![Email da lista de desejos compartilhada](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## Editar listas de desejos

Os clientes podem modificar sua lista de desejos de várias maneiras no painel de contas.

### Mover itens para uma lista diferente

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce)

1. O cliente marca a caixa de seleção de cada item a ser movido.

1. Cliques **[!UICONTROL Move Selected to Wish List]** e executa um dos seguintes procedimentos:

   - Escolhe uma lista de desejos existente.
   - Cliques **[!UICONTROL Create New Wish List]**.

### Copiar itens para uma lista diferente

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce)

1. Marca a caixa de seleção de cada item a ser movido.

1. Cliques **[!UICONTROL Copy Selected to Wish List]** e executa um dos seguintes procedimentos:

   - Escolhe uma lista de desejos existente.
   - Cliques **[!UICONTROL Create New Wish List]**.

## Excluir uma lista de desejos

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce)

1. O cliente abre a lista de desejos a ser excluída.

1. Cliques **[!UICONTROL Delete Wish List]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

>[!IMPORTANT]
>
>Essa ação não pode ser desfeita.

## Transferir itens da lista de desejos para o carrinho

Para transferir todos os itens da lista de desejos para o carrinho, o cliente clica em **[!UICONTROL Add All to Cart]**.

Para adicionar um único item, o cliente faz o seguinte:

1. Passe o mouse sobre o item e entre no **[!UICONTROL Qty]** que deseja adicionar ao carrinho.

1. Cliques **[!UICONTROL Add to Cart]**.

## Localizar uma lista de desejos do cliente

Se a variável [Widget de pesquisa da lista de desejos](wishlist-configuration.md#add-wish-list-search) nas páginas incluídas na loja, os clientes podem pesquisar pelo nome ou endereço de email do proprietário da lista de desejos.

1. No widget de pesquisa da lista de desejos, o cliente seleciona uma opção de pesquisa.

1. Insere o nome ou endereço de email do proprietário da lista de desejos e clica em **[!UICONTROL Search]**.

   A variável _Pesquisa na lista de desejos_ será aberta e qualquer lista de desejos correspondente será exibida na seção de resultados da pesquisa.

   >[!NOTE]
   >
   >Somente as listas de desejos públicas são exibidas nos resultados da pesquisa — as listas de desejos privadas dos clientes não são exibidas publicamente.

1. Para exibir a lista de itens da lista de desejos, clique em **[!UICONTROL View]**.

   O nome do proprietário e a data da última atualização são exibidos para cada lista de desejos.

1. Para adicionar um produto ao carrinho, o cliente marca a caixa de seleção abaixo do produto e clica em **[!UICONTROL Add to Cart]**.

   Você também pode adicionar seus próprios itens de que gosta na lista de desejos de outro cliente.
