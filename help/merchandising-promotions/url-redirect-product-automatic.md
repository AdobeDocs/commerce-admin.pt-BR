---
title: Redirecionamentos automáticos
description: Saiba como configurar redirecionamentos automáticos a serem gerados sempre que a chave do URL de um produto ou categoria for alterada na loja do Commerce.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/Vscg-TDdLnzKjdi-SMwrcpR-QDPvlHpPzgmcLe63-4Q
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 571
ht-degree: 0%

---

# Redirecionamentos automáticos

Sua loja pode ser configurada para gerar automaticamente um redirecionamento permanente sempre que a chave do URL de um produto ou categoria mudar. Na seção Otimização do mecanismo de pesquisa, a caixa de seleção abaixo da chave do URL indica se os redirecionamentos permanentes estão ativados. Se sua loja já estiver configurada para redirecionar automaticamente URLs de catálogo, um redirecionamento é uma atualização simples da chave do URL. O processo para criar um redirecionamento automático é o mesmo para produtos e categorias.

>[!NOTE]
>
>Quando redirecionamentos automáticos são ativados e você salva uma categoria, todas as regravações de produto e categoria são geradas em tempo real e armazenadas em tabelas de banco de dados por padrão. Isso pode resultar em problemas significativos de desempenho para categorias com muitos produtos atribuídos. A solução é alterar esse padrão e ignorar a geração de regravações de URL de categoria/produtos para produtos no salvamento da categoria. Nesse caso, as substituições de produto são geradas somente para o URL do produto canônico.

## Configurar redirecionamentos automáticos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]**.

   ![Configuração do catálogo - otimização do mecanismo de pesquisa](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.


>[!NOTE]
>
> As substituições de URL podem ser geradas para a exibição de loja ou o escopo do site. Defina o escopo de regravação de URL do Administrador em **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;**[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**. Selecione o escopo no campo&#x200B;_[!UICONTROL Product URL Rewrite Scope]_.

## Redirecionar URLs de produtos automaticamente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Encontre o produto na lista e clique em para abrir o registro.

1. Expandir ![Seletor de expansão &#x200B;](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]**.

   ![Otimização do mecanismo de pesquisa do produto - redirecionamento permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL URL Key]**, faça o seguinte:

   - Verifique se a caixa de seleção **[!UICONTROL Create Permanent Redirect for old URL]** está marcada. Caso contrário, siga as instruções para [habilitar redirecionamentos automáticos](url-rewrite.md#configure-url-rewrites).

   - Atualize o **[!UICONTROL URL Key]** conforme necessário, usando todos os caracteres em minúsculas e hifens não finais entre esses caracteres em vez de espaços.

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado a atualizar o cache, siga os links na mensagem na parte superior do espaço de trabalho.

   O redirecionamento permanente agora está em vigor para o produto e qualquer URL de categoria associado.

## Redirecionar URLs de categoria automaticamente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Localize a categoria na árvore e clique em para abrir o registro.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]**.

1. Para **[!UICONTROL URL Key]**, faça o seguinte:

   - Verifique se a caixa de seleção **[!UICONTROL Create Permanent Redirect for old URL]** está marcada. Caso contrário, siga as instruções para [habilitar redirecionamentos automáticos](url-rewrite.md#configure-url-rewrites).

   - Atualize o **[!UICONTROL URL Key]** conforme necessário, usando todos os caracteres em minúsculas e hifens não finais entre esses caracteres em vez de espaços.

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado a atualizar o cache, siga os links na mensagem na parte superior do espaço de trabalho.

   O redirecionamento permanente agora está em vigor para a categoria e qualquer URL de produto associado.

## Ignorar geração de regravações de URL de produto para salvamento de categoria {#skip-rewrite}

>[!WARNING]
>
>Desativar a geração automática de substituições de URL de categoria/produtos resulta na remoção permanente de todas as substituições de URL de categoria/tipo de produto existentes, que não podem ser restauradas. Isso pode causar conflitos não resolvidos de URL de tipo de categoria/produto que exigem uma atualização manual da chave do URL para serem resolvidos.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]**.

1. Defina **[!UICONTROL Generate "category/product" URL Rewrites]** como `No`.

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL OK]** para confirmar a alteração e a remoção das regravações de URL existentes.

   ![Desativar substituições de URL de categoria/produto - confirmar](./assets/seo-rewrite-off.png){width="350"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
