---
title: Otimização do mecanismo de pesquisa
description: Saiba mais sobre as ferramentas de otimização de mecanismo de pesquisa (SEO) para sites do Commerce e as práticas recomendadas para SEO ideal.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: c8649d9107a92b15a1c9af8ae5d2ad0e8e34e64e
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Visão geral da SEO

A _Otimização do mecanismo de pesquisa_ (SEO) é a prática de ajustar o conteúdo e a apresentação de um site para melhorar a forma como as páginas são indexadas pelos mecanismos de pesquisa. O Commerce inclui vários recursos para dar suporte ao seu esforço contínuo de SEO.

>[!TIP]
>
>Para o Adobe Commerce as a Cloud Service, consulte as [diretrizes de SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=pt-BR) na documentação da Commerce Storefront

## Metadados

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

Saiba mais sobre como adicionar e aprimorar [metadados](meta-data.md) ricos em palavras-chave para seu site e loja.

## Uso de um mapa de site

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

Um [mapa do site](sitemap-xml.md) melhora a forma como o armazenamento é indexado pelos mecanismos de pesquisa e foi projetado para localizar páginas que podem ser ignoradas pelos rastreadores da Web. Um mapa do site pode ser configurado para indexar todas as páginas e imagens.

## Substituições de URL

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

A ferramenta [Reescrita de URL](url-rewrite.md) permite alterar qualquer URL associada a um produto, categoria ou página do CMS.

## Robôs do mecanismo de pesquisa

A configuração do Commerce inclui configurações para gerar e gerenciar instruções para crawlers e bots da Web que indexam seu site. Se a solicitação de `robots.txt` atingir o Commerce (em vez de um arquivo físico), ela será roteada dinamicamente para o controlador de robôs. As instruções são diretivas reconhecidas e seguidas pela maioria dos mecanismos de pesquisa.

Por padrão, o arquivo robots.txt gerado pelo Commerce contém instruções para o crawler da Web evitar a indexação de determinadas partes do site que contêm arquivos usados internamente pelo sistema. Você pode usar as configurações padrão ou definir suas próprias instruções personalizadas para todos ou para mecanismos de pesquisa específicos. Há muitos artigos online que exploram o assunto em detalhes.

### Exemplo de instruções personalizadas

**Permite Acesso Completo**

    User-agent:*
    Não permitir:

**Não permite acesso a todas as pastas**

    User-agent:*
    Não permitir: /

**Instruções Padrão**

    User-agent: *
    Não permitir: /index.php/
    Não permitir: /*?
    Não permitir: /checkout/
    Não permitir: /app/
    Não permitir: /lib/
    Não permitir: /*.php$
    Não permitir: /pkginfo/
    Não permitir: /report/
    Não permitir: /var/
    Não permitir: /catalog/
    Não permitir: /customer/
    Não permitir: /sendfriend/
    Não permitir: /review/
    Não permitir: /*SID=

### Configurar `robots.txt`

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a configuração **[!UICONTROL Global]** na primeira linha da grade e clique em **[!UICONTROL Edit]**.

   ![Configuração de design global](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Robots]** e faça o seguinte:

   ![Configuração de design - robôs de mecanismo de pesquisa](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Defina **[!UICONTROL Default Robots]** como um dos seguintes:

     | Opção | Descrição |
     |------|------------|
     | `INDEX, FOLLOW` | Instrui os rastreadores da web a indexar o site e verificar novamente mais tarde se há alterações. |
     | `NOINDEX, FOLLOW` | Instrui os rastreadores da Web a evitar a indexação do site, mas a verificar novamente mais tarde se há alterações. |
     | `INDEX, NOFOLLOW` | Instrui os rastreadores da Web a indexar o site uma vez, mas não siga os links na página. |
     | `NOINDEX, NOFOLLOW` | Instrui os rastreadores da Web a evitar a indexação do site e a não seguir nenhum link na página. |

     {style="table-layout:auto"}

   - Se necessário, insira instruções personalizadas na caixa **[!UICONTROL Edit Custom instruction of robots.txt file]**. Por exemplo, enquanto um site estiver em desenvolvimento, talvez você queira proibir o acesso a todas as pastas.

   - Para restaurar as instruções padrão, clique em **[!UICONTROL Reset to Default]**.

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.
