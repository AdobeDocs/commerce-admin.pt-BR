---
title: Substituições de URL
description: Saiba mais sobre substituições de URL e sobre como usar a ferramenta de regravação de URL do Commerce para alterar URLs associados a um produto, categoria ou página do CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 2f2db4926ff92adfa27692eeca872c1765fd31d6
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Substituições de URL

>[!TIP]
>
>Para o Adobe Commerce as a Cloud Service, consulte as [diretrizes de SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=pt-BR) na documentação da Commerce Storefront

A ferramenta de regravação de URL permite alterar qualquer URL associado a um produto, categoria ou página do CMS. Ao criar uma regravação de URL, o Commerce cria automaticamente um redirecionamento permanente (301) para que todos os links que apontem para o URL antigo sejam redirecionados para o novo endereço.

>[!NOTE]
>
>Para atualizar regravações de URL para vários ou todos os produtos simultaneamente, consulte [Várias regravações de URL](url-rewrite-product.md#multiple-url-rewrites).

>[!BEGINSHADEBOX &quot;Entendendo regravações e redirecionamentos&quot;]

Os termos _rewrite_ e _redirect_ são frequentemente usados alternadamente, mas são operações diferentes:

* **Reescrita de URL** — Um processo do lado do servidor que mapeia internamente uma URL para outra sem alterar o que aparece na barra de endereços do navegador. Quando um visitante solicita um URL, o servidor o processa como um URL diferente em segundo plano, mas o navegador continua a exibir o URL original.

* **Redirecionamento de URL** — Envia uma resposta HTTP para o navegador, instruindo-o a navegar para uma URL diferente. A barra de endereços do navegador é atualizada para mostrar o novo URL. Os redirecionamentos podem ser temporários (302) ou permanentes (301).

>[!ENDSHADEBOX]

## Como a ferramenta de regravação funciona

No Adobe Commerce, a ferramenta de reescrita de URL cria redirecionamentos permanentes (301) por padrão para preservar o valor de SEO ao alterar a chave de URL de um produto, categoria ou página. Esse comportamento garante que os links existentes continuem funcionando e as classificações do mecanismo de pesquisa sejam mantidas.

Por padrão, os [redirecionamentos automáticos de URL](url-redirect-product-automatic.md) estão habilitados para sua loja e a caixa de seleção **Criar redirecionamento permanente para URL antiga** está marcada no campo de chave de URL de cada produto.

{{url-rewrite-skip}}

![Otimização do mecanismo de pesquisa - criar redirecionamento de URL permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

{{url-rewrite-params}}

## Demonstração de regravações de URL

Assista ao vídeo a seguir para saber mais sobre o gerenciamento de regravações de URL:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)

## Criar regravações de URL

Use a ferramenta de regravações de URL para criar redirecionamentos de produtos e categorias e redirecionamentos personalizados para qualquer página em sua loja. Quando a configuração de reescrita de URL é aplicada, todos os links existentes que apontam para o URL anterior são perfeitamente redirecionados para o novo endereço.

Você pode criar regravações de URL em:

* Adicione palavras-chave de alto valor para melhorar a maneira como o produto é indexado por mecanismos de pesquisa.

* Adicione URLs adicionais para uma alteração sazonal temporária ou alteração permanente.

* Adicione um caminho válido para uma página, incluindo páginas de conteúdo do CMS. Por exemplo, você pode criar um URL para criar um URL mais amigável ao usuário ou à SEO em um sistema que sempre faz referência a produtos e categorias por sua ID interna.

As substituições de URL que você criar podem redirecionar para categorias existentes ou páginas personalizadas sem alterar a estrutura do site, facilitando a criação de URLs memoráveis para campanhas de marketing.

![A URL reescreve a grade](./assets/url-rewrites.png){width="700" zoomable="yes"}

O Commerce oferece estes tipos de reescrita de URL:

* [Substituições de produto](url-rewrite-product.md)
* [Substituições de Categoria](url-rewrite-category.md)
* [Substituições de página do CMS](url-rewrite-cms-page.md)
* [Substituições Personalizadas](url-rewrite-custom.md)

### Casos de uso e exemplos

As substituições de URL geralmente são usadas nestes cenários:

#### Alterar um URL interno do sistema para um URL compatível com SEO

O Commerce usa URLs baseados em ID internamente, mas você pode criar URLs amigáveis para SEO para clientes:

**URL do sistema (interno):**

    http://www.example.com/catalog/category/id/6

**URL voltada para o cliente:**

    http://www.example.com/peripherals/keyboard.html

#### Reformulação da marca do produto ou otimização de URL

Ao renomear um produto ou melhorar o URL para SEO, crie um redirecionamento para preservar os links existentes:

**URL Original:**

    http://www.example.com/peripherals/keyboard.html

**Nova URL otimizada:**

    http://www.example.com/ergonomic-keyboard.html

A ferramenta Rewrites cria automaticamente um redirecionamento 301 do URL antigo para o novo, para que os clientes e mecanismos de pesquisa sejam direcionados perfeitamente para a página correta.

#### Páginas de aterrissagem promocionais

Crie URLs personalizados temporários ou permanentes para campanhas de marketing:

**URLs promocionais:**

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

## Configuração de gerenciamento de URL adicional

As seções a seguir descrevem como configurar substituições de servidor Web e URLs canônicos para o Commerce.

### Configurar regravações do servidor Web

>[!NOTE]
>
>Esta seção descreve a reescrita de URL no nível do servidor Web, que é diferente do recurso da ferramenta Reescrita de URL. As substituições do servidor Web lidam com a formatação técnica de URL (como remover `index.php`), enquanto a ferramenta de regravação de URL gerencia redirecionamentos para alterações de conteúdo.

Ativar regravações do servidor da Web faz parte da configuração inicial do Commerce e geralmente é configurado durante a instalação. Quando habilitado, o servidor Web (Apache ou Nginx) remove automaticamente o nome de arquivo `index.php` das URLs, criando endereços mais limpos e mais amigáveis para SEO.
O exemplo a seguir mostra como os URLs são exibidos com e sem as regravações do servidor Web ativadas:

**URL sem uma Regravação de Servidor Web**

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

**URL com Regravação do Servidor Web**

    http://www.yourdomain.com/magento/storeview/url-identifier

#### Habilitar ou desabilitar Regravações de Servidor Web:

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo onde **[!UICONTROL General]** é expandido, escolha **[!UICONTROL Web]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]**.

   ![Configuração geral - Otimização do mecanismo de pesquisa da Web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Use Web Server Rewrites]** de acordo com sua preferência.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Especificar URLs canônicos

Para fins de SEO, cada uma das páginas da Web deve ter apenas um URL distinto.

Se você tiver uma única página acessível por vários URLs ou páginas diferentes com conteúdo semelhante, o Google as verá como versões duplicadas da mesma página. O Google escolhe um URL como a versão canônica e rastreia esse URL, e todos os outros URLs são considerados URLs duplicados e são rastreados com menos frequência.

Se você não disser explicitamente à Google qual URL é canônico, ela fará a escolha para você ou poderá considerá-los de igual peso. Isso pode levar a um comportamento indesejado e pode gerar um orçamento de rastreamento ineficaz e links de retorno distribuídos baixos.

Dependendo de como você configura o site, pode haver várias versões dele no índice, por exemplo:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Para especificar uma página canônica, consulte a [documentação da Google Search Central](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).
