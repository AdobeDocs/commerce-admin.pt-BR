---
title: Catálogos simples
description: Saiba mais sobre como criar um catálogo simples, em que cada linha contém todos os dados necessários sobre um produto ou categoria.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
TQID: https://experienceleague.adobe.com/7D7lHMHFVKh2J35S1Mpr5eudyLyicbpL4xqkvu-KatA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 704
ht-degree: 0%

---

# Catálogos simples

>[!IMPORTANT]
>
>O uso de um catálogo simples não é mais recomendado como prática recomendada. O uso continuado desse recurso é conhecido por causar degradação de desempenho e outros problemas de indexação. Uma descrição detalhada e uma solução estão disponíveis na [Central de Ajuda](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html).<br/><br/>As versões afetadas incluem: <br/>- Adobe Commerce na infraestrutura de nuvem, 2.3.x e superior<br/>- Adobe Commerce (No Local), 2.3.x e superior<br/>- Magento Open Source, 2.3.x e superior <br/><br/>Em qualquer versão de lançamento, algumas extensões funcionam apenas com tabelas simples, criando um risco se você desabilitar tabelas simples. Se você souber que tem algumas extensões que usam indexadores de Catálogo Simples, deverá estar ciente desse risco ao definir esses valores como `No`.

O Commerce geralmente armazena dados de catálogo em várias tabelas, com base no modelo Entity-Attribute-Value (EAV). Como os atributos do produto são armazenados em muitas tabelas, as consultas SQL às vezes são longas e complexas.

Por outro lado, um catálogo simples cria tabelas em tempo real, onde cada linha contém todos os dados necessários sobre um produto ou categoria. Um catálogo simples é atualizado automaticamente — a cada minuto ou de acordo com seu trabalho cron. A indexação de catálogos simples também pode acelerar o processamento de regras de catálogo e preço de carrinho. Um catálogo com até 500.000 SKUs pode ser indexado rapidamente como um catálogo simples.

>[!NOTE]
>
>Antes de habilitar um catálogo simples para uma loja em tempo real, teste a configuração em um ambiente de desenvolvimento.

## Etapa 1: Ativar o catálogo simples

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expanda a seção _Vitrine_ e faça o seguinte:

   - Defina **[!UICONTROL Use Flat Catalog Category]** como `Yes`. (Se necessário, desmarque a caixa de seleção **[!UICONTROL Use system value]**.)

   - Defina **[!UICONTROL Use Flat Catalog Product]** como `Yes`.

   ![Configuração de catálogo simples](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado a atualizar o cache, clique em **[!UICONTROL Cache Management]** na mensagem do sistema e siga as instruções para atualizar o cache.

## Etapa 2: verificar os resultados

Há dois métodos que podem ser usados para verificar os resultados.

### Método 1: verificar os resultados de um único produto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra um produto no modo de edição.

1. Para **[!UICONTROL Name]**, adicione o texto `_TEST` ao final do nome do produto.

1. Clique em **[!UICONTROL Save]**.

1. Em uma nova guia do navegador, navegue até a página inicial da loja e faça o seguinte:

   - Procure o produto que você editou.

   - Use a navegação para procurar o produto na categoria atribuída.

     Se necessário, atualize a página para ver os resultados. A alteração aparece dentro de um minuto ou de acordo com seu cronograma [Cron](../systems/cron.md).

   ![Vitrine com Catálogo Simples](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### Método 2: verificar os resultados de uma categoria

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. No canto superior esquerdo, verifique se **[!UICONTROL Store View]** está definido como `All Store Views`.

   Se solicitado, clique em **[!UICONTROL OK]** para confirmar.

1. Na árvore de categorias, selecione uma categoria existente, clique em **[!UICONTROL Add Subcategory]** e faça o seguinte:

   - Para **[!UICONTROL Category Name]**, digite `Test Category`.

   - Quando terminar, clique em **[!UICONTROL Save]**.

     ![Subcategoria de teste](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Products in Category]** e clique em **[!UICONTROL Reset Filter]** para exibir todos os produtos.

   - Marque a caixa de seleção de vários produtos a serem adicionados à nova categoria.

   - clique em **[!UICONTROL Save]**.

   ![Testar produtos da categoria](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. Em uma nova guia do navegador, navegue até a página inicial da loja e use a navegação para navegar até a categoria criada.

   Se necessário, atualize a página para ver os resultados. A alteração será exibida dentro de um minuto ou de acordo com a programação do cron.

## Etapa 3: Remover os dados de teste

Faça o seguinte para remover os dados de teste e restaurar o nome original do produto e a configuração do catálogo.

### Remover a categoria de teste

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Na árvore de categorias, selecione a subcategoria de teste criada.

1. No canto superior direito, clique em **[!UICONTROL Delete]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

   Essa remoção de categoria não remove os produtos atribuídos à categoria.

### Restaurar o nome original do produto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Abra o produto de teste no modo de edição.

1. Remova o texto `_TEST` adicionado ao **[!UICONTROL Product Name]**.

1. No canto superior direito, clique em **[!UICONTROL Save]**.

### Restaurar a configuração original do catálogo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expanda a seção _Vitrine_ e faça o seguinte:

   - Defina **[!UICONTROL Use Flat Catalog Category]** como `No`.

   - Defina **[!UICONTROL Use Flat Catalog Product]** como `No`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, atualize o cache.
