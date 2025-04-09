---
title: Redirecionamentos automáticos
description: Aprenda a configurar redirecionamentos automáticos para serem gerados sempre que o URL chave de um produto ou categoria alterações no seu Comércio armazenamento.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: d088d5833b9c61e7b1c90a0839fdf38527929ce5
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Redirecionamentos automáticos

Suas armazenamento podem ser configuradas para gerar automaticamente uma redirecionar permanente sempre que a chave URL de um produto ou categoria for alterada. Na seção Search Otimização de mecanismos, a caixa de seleção abaixo da chave URL indica se os redirecionamentos permanentes estão ativados. Se sua loja já estiver configurada para redirecionar automaticamente URLs de catálogo, um redirecionamento é uma atualização simples da chave do URL. O processo para criar uma redirecionar automática é o mesmo para produtos e categorias.

>[!NOTE]
>
>Quando os redirecionamentos automáticos são ativados e você salva uma categoria, todos os produtos e categoria regravações são gerados em tempo real e armazenados em tabelas de banco de dados por padrão. Isso pode resultar em problemas significativos de desempenho para categorias com muitos produtos atribuídos. A solução é alterar esse padrão e ignorar a geração de regravações de categoria/products URL para produtos em categoria salvar. Nesse caso, reescritas de produto são geradas apenas para o produto canônico URL.

## Configurar redirecionamentos automáticos

1. Na barra lateral do __ Administrador, vá até **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]**.

   ![Configuração do catálogo - otimização do mecanismo de pesquisa](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** como `Yes`.

1. Ao concluir, clique **[!UICONTROL Save Config]** em .


>[!NOTE]
>
> URL reescritas podem ser geradas para o visualização de armazenamento ou escopo do site. Defina o escopo de regravação de URL do Administrador em **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]****[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**. Selecione o escopo no campo_[!UICONTROL Product URL Rewrite Scope]_.

## Redirecionar URLs de produtos automaticamente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Encontre o produto na lista e clique em para abrir o registro.

1. Expandir ![Seletor de expansão ](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]**.

   ![otimização de mecanismo de pesquisa do produto - redirecionar permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL URL Key]**, faça o seguinte:

   - Certifique-se de que a **[!UICONTROL Create Permanent Redirect for old URL]** caixa de seleção esteja selecionada. Caso contrário, seguir as instruções para [ativar os redirecionamentos automáticos](url-rewrite.md#configure-url-rewrites).

   - Atualize o **[!UICONTROL URL Key]** conforme necessário, usando todos os caracteres em minúsculas e hifens não finais entre esses caracteres em vez de espaços.

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado a atualizar o cache, seguir os links na mensagem na parte superior do espaço de trabalho.

   A redirecionar permanente agora está em vigor para o produto e quaisquer URLs categoria associados.

## Redirecionar automaticamente categoria URLs

1. Na barra lateral do _Administrador_ , vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Encontre a categoria na árvore e clique para abrir o registro.

1. Expanda ![a expansão seletor](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]** seção.

1. Para **[!UICONTROL URL Key]**, faça o seguinte:

   - Verifique se a caixa de seleção **[!UICONTROL Create Permanent Redirect for old URL]** está marcada. Caso contrário, siga as instruções para [habilitar redirecionamentos automáticos](url-rewrite.md#configure-url-rewrites).

   - Atualize o **[!UICONTROL URL Key]** conforme necessário, usando todos os caracteres em minúsculas e hifens não finais entre esses caracteres em vez de espaços.

1. Ao concluir, clique **[!UICONTROL Save]** em .

1. Quando solicitado a atualizar o cache, seguir os links na mensagem na parte superior do espaço de trabalho.

   O redirecionamento permanente agora está em vigor para a categoria e qualquer URL de produto associado.

## Ignorar geração de regravações de URL de produto para salvamento de categoria {#skip-rewrite}

>[!WARNING]
>
>Desativar a geração automática de substituições de URL de categoria/produtos resulta na remoção permanente de todas as substituições de URL de categoria/tipo de produto existentes, que não podem ser restauradas. Isso pode causar conflitos não resolvidos de URL de tipo de categoria/produto que exigem uma atualização manual da chave do URL para serem resolvidos.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expanda ![a expansão seletor](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]** seção.

1. Defina **[!UICONTROL Generate "category/product" URL Rewrites]** como `No`.

1. Na caixa de diálogo de confirmação, clique **[!UICONTROL OK]** para confirmar a alteração e a remoção de regravações de URL existentes.

   ![Desativar substituições de URL de categoria/produto - confirmar](./assets/seo-rewrite-off.png){width="350"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
