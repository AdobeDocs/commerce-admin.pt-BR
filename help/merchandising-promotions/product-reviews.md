---
title: Resenhas do produto
description: Saiba como as análises de produtos podem aprimorar sua loja e dar mais credibilidade aos seus produtos.
exl-id: 82f96b24-626f-4b2d-be42-3d655d08dfda
feature: Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Resenhas do produto

Resenhas de produtos ajudam a construir um senso de comunidade e são consideradas mais críveis do que qualquer dinheiro de publicidade pode comprar. Na verdade, alguns mecanismos de pesquisa dão aos sites com análises de produtos uma classificação mais alta do que aqueles sem análises. Para aqueles que encontram seu site procurando por um produto específico, uma análise do produto é essencialmente a página inicial da sua loja. As análises de produtos ajudam as pessoas a encontrar sua loja, mantê-las envolvidas e geralmente levam a vendas.

O Commerce inclui um recurso nativo de análises de produtos que pode ser gerenciado pelo administrador. Você também pode usar uma extensão do [Commerce Marketplace](../getting-started/commerce-marketplace.md) para usar um sistema de gerenciamento de revisão hospedado.

>[!NOTE]
>
>O Adobe Commerce e o Magento Open Source versões 2.4.0 a 2.4.3 incluíam a extensão desenvolvida pelo fornecedor do Yotpo. A partir da versão 2.4.4, essa extensão não é mais fornecida com a versão principal e deve ser instalada e atualizada do Commerce Marketplace. O Marketplace também fornece acesso à documentação atual fornecida pelo desenvolvedor da extensão.
><br><br>
>Se você tiver a extensão agrupada ativada e configurada, deverá atualizar o arquivo composer.json como parte do processo de atualização 2.4.4 e gerenciar as atualizações de extensão a partir de agora. Consulte [Atualizar módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=pt-BR) no _Guia de Atualização_ para obter mais informações.

## Resenhas de produtos na loja

Quando a função Nativa Revisões de produto estiver ativada, os clientes poderão escrever revisões para qualquer produto em seu catálogo. As análises podem ser escritas na página do produto clicando em:

- **Adicione sua Revisão** para produtos com revisões existentes.

- **Seja o primeiro a analisar este produto** para produtos sem análises existentes.

A guia [!UICONTROL Reviews] lista todas as revisões atuais e o formulário que foi usado para enviar uma revisão.

Sua configuração determina se os clientes devem abrir uma conta na loja antes de escrever análises de produtos ou se podem enviar análises como convidados. Exigir que os revisores abram uma conta impede envios anônimos e melhora a qualidade das análises.

![Exemplo de vitrine - Adicione sua Revisão](./assets/storefront-review-this-product.png){width="700" zoomable="yes"}

O número de estrelas indica o índice de satisfação do produto. Os visitantes podem clicar no link para ler as revisões e escrever as suas próprias. Como incentivo, os clientes podem receber pontos de recompensa pelo envio de uma revisão. Quando uma revisão é enviada, ela é enviada ao administrador para moderação. Quando aprovada, a revisão é publicada na loja.

![Exemplo de vitrine - Guia Avaliações](./assets/storefront-reviews-tab.png){width="700" zoomable="yes"}

### [!UICONTROL My Product Reviews]

A seção _[!UICONTROL My Product Reviews]_&#x200B;do painel da conta do cliente lista todas as revisões enviadas pelo cliente e aprovadas para publicação. Cada resumo de revisão inclui a data em que a revisão foi enviada, links para a página do produto e detalhes da revisão.

![Minhas análises de produto](./assets/account-dashboard-my-product-reviews.png){width="700" zoomable="yes"}

1. Na barra lateral da conta, o cliente escolhe **[!UICONTROL My Product Reviews]**.

1. Para exibir a revisão completa, clique em **[!UICONTROL See Details]**.

   ![Detalhes da Revisão](./assets/account-dashboard-my-product-reviews-details.png){width="700" zoomable="yes"}

## Habilitar recursos de análise do produto

A função Revisões de produto do Commerce é ativada por padrão.

>[!NOTE]
>
>Para definir esses campos como `No` e desabilitar as Revisões de Produtos do Commerce, desmarque as caixas de seleção **Usar valor do sistema**.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e selecione **[!UICONTROL Catalog]** abaixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Product Reviews]**.

   ![Configuração do catálogo - análises de produtos da Commerce](../configuration-reference/catalog/assets/catalog-product-reviews.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Enabled]** como `Yes`.

   Essa é a configuração padrão que permite revisões de produtos.

1. Defina **[!UICONTROL Allow Guests to Write Reviews]** como `Yes`.

   Essa é a configuração padrão que determina se os clientes devem abrir uma conta na loja para poderem escrever análises de produtos.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Criar classificações personalizadas

Com as Revisões de produto do Commerce, os clientes podem atribuir classificações ao enviar uma revisão de produto. As classificações padrão são qualidade, preço e valor. Além dessas, você pode adicionar suas próprias classificações personalizadas. A média das classificações de cinco estrelas exibidas nas páginas do catálogo é calculada para cada produto.

![Exemplo de vitrine - classificações personalizadas](./assets/attribute-custom-ratings-review.png){width="700" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Rating]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Rating]**.

   ![Administrador - Classificações](./assets/product-reviews-rating.png){width="700" zoomable="yes"}

1. Na seção _[!UICONTROL Rating Title]_, digite o **[!UICONTROL Default Value]**&#x200B;para a nova classificação.

   Se aplicável, insira também a tradução para cada exibição de loja.

   ![Configurações do título de classificação](./assets/product-rating-title.png){width="600" zoomable="yes"}

1. Na seção _Visibilidade de Classificação_, defina **[!UICONTROL Visibility In]** para o modo de exibição de repositório onde a classificação será usada.

   Para selecionar várias exibições de loja, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada item.

   >[!NOTE]
   >
   >As classificações não estarão visíveis, a menos que atribuídas a uma visualização de loja.

1. Para **[!UICONTROL Sort Order]**, insira um número para determinar a ordem dessa classificação quando listada com outras pessoas.

1. Para mostrar sua classificação na loja, marque a caixa de seleção **[!UICONTROL Is Active]**.

   ![Configurações de visibilidade de classificação](./assets/product-rating-visibility.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Rating]**.

   A classificação média de todas as revisões é exibida para cada produto na página de grade de produtos do catálogo.

   ![Página de catálogo](./assets/catalog-rating-page.png){width="700" zoomable="yes"}
