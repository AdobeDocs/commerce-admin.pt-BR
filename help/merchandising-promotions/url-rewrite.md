---
title: Substituições de URL
description: Saiba mais sobre substituições de URL e sobre como usar a ferramenta de regravação de URL do Commerce para alterar URLs associados a um produto, categoria ou página do CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Substituições de URL

>[!TIP]
>
>Para o Adobe Commerce as a Cloud Service, consulte as [diretrizes de SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=pt-BR) na documentação da Commerce Storefront

A ferramenta de regravação de URL permite alterar qualquer URL associado a um produto, categoria ou página do CMS. Quando a regravação entrar em vigor, os links que apontarem para o URL anterior serão redirecionados para o novo endereço.

>[!NOTE]
>
>Para atualizar regravações de URL para vários ou todos os produtos simultaneamente, consulte [Várias regravações de URL](url-rewrite-product.md#multiple-url-rewrites).

Os termos _rewrite_ e _redirect_ são frequentemente usados de forma intercambiável, mas se referem a processos ligeiramente diferentes. Uma regravação de URL altera a forma como um URL é exibido no navegador. Um redirecionamento de URL atualiza o URL armazenado no servidor. Um redirecionamento de URL pode ser temporário ou permanente. Sua loja usa regravações e redirecionamentos de URL para facilitar a alteração da chave de URL de um produto, categoria ou página e preservar os links existentes.

Por padrão, os [redirecionamentos automáticos de URL](url-redirect-product-automatic.md) estão habilitados para sua loja e a caixa de seleção **Criar redirecionamento permanente para URL antiga** está marcada no campo de chave de URL de cada produto.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![Otimização do mecanismo de pesquisa - criar redirecionamento de URL permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## URLs canônicos

Para fins de SEO, é uma boa ideia que cada uma de suas páginas da Web tenha apenas um URL distinto.

Se você tiver uma única página acessível por vários URLs ou páginas diferentes com conteúdo semelhante, o Google as verá como versões duplicadas da mesma página. O Google escolhe um URL como a versão canônica e rastreia esse URL, e todos os outros URLs são considerados URLs duplicados e são rastreados com menos frequência.

Se você não disser explicitamente à Google qual URL é canônico, ela fará a escolha para você ou poderá considerá-los de igual peso. Isso pode levar a um comportamento indesejado e corre o risco de um orçamento de rastreamento ineficaz e links de retorno distribuídos baixos.

Dependendo de como você configura o site, pode haver várias versões dele no índice, incluindo:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Para especificar uma página canônica, consulte a [documentação da Google Search Central](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## Configurar substituições de URL

Habilitar regravações do Apache do servidor Web faz parte da configuração inicial do Commerce. O Commerce geralmente usa substituições de URL para remover o nome de arquivo `index.php` que normalmente aparece na URL logo após a pasta raiz. Quando as Regravações do Servidor Web estão habilitadas, o sistema regrava cada URL para omitir `index.php`. A regravação remove palavras que não transmitem nada de valor para mecanismos de pesquisa ou clientes e não tem impacto no desempenho ou na classificação do site.

URL sem reescrita do servidor da Web

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL com regravação do servidor da Web

    http://www.yourdomain.com/magento/storeview/url-identifier

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo onde **[!UICONTROL General]** é expandido, escolha **[!UICONTROL Web]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]**.

   ![Configuração geral - Otimização do mecanismo de pesquisa da Web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Use Web Server Rewrites]** de acordo com sua preferência.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Criar regravações de URL

Você pode usar a ferramenta de regravação de URL para criar regravações de produtos e categorias e regravações personalizadas para qualquer página em sua loja. Quando a regravação entrar em vigor, todos os links existentes que apontarem para o URL anterior serão perfeitamente redirecionados para o novo endereço.

As substituições de URL podem ser usadas para adicionar palavras-chave de alto valor para melhorar a forma como o produto é indexado por mecanismos de pesquisa. Você também pode usar substituições para criar URLs adicionais para uma alteração sazonal temporária ou uma alteração permanente. As substituições podem ser criadas para qualquer caminho válido, incluindo páginas de conteúdo do CMS. Internamente, o sistema sempre faz referência a produtos e categorias pela ID. Independentemente da frequência com que o URL muda, a ID permanece a mesma. Estas são algumas maneiras pelas quais você pode usar uma regravação de URL:

URL do sistema

    http://www.example.com/catalog/category/id/6

URL original

    http://www.example.com/peripherals/keyboard.html

URL do produto redirecionado

    http://www.example.com/ergonomic-keyboard.html

URLs de categoria adicionais

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![A URL reescreve a grade](./assets/url-rewrites.png){width="700" zoomable="yes"}

O Commerce oferece estes tipos de reescrita de URL:

* [Substituições de produto](url-rewrite-product.md)
* [Substituições de Categoria](url-rewrite-category.md)
* [Substituições de página do CMS](url-rewrite-cms-page.md)
* [Substituições Personalizadas](url-rewrite-custom.md)

## Demonstração de regravações de URL

Assista a este vídeo para saber mais sobre o gerenciamento de regravações de URL:

>[!VIDEO](https://video.tv.adobe.com/v/3411958?quality=12&learn=on&captions=por_br)
