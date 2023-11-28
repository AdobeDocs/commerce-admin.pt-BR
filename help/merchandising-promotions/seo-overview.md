---
title: Otimização do mecanismo de pesquisa
description: Saiba mais sobre as ferramentas de otimização de mecanismo de pesquisa (SEO) para sites do Commerce e as práticas recomendadas para SEO ideal.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Visão geral da SEO

_Otimização do mecanismo de pesquisa_ (SEO) é a prática de ajustar o conteúdo e a apresentação de um site para melhorar a forma como as páginas são indexadas por mecanismos de pesquisa. O Commerce inclui vários recursos para dar suporte ao seu esforço contínuo de SEO.

## Metadados

Saiba mais sobre como adicionar e aprimorar palavras-chave ricas [metadados](meta-data.md) para seu site e loja.

## Uso de um mapa de site

A [mapa do site](sitemap-xml.md) melhora a maneira como sua loja é indexada por mecanismos de pesquisa e é projetada para encontrar páginas que podem ser ignoradas por rastreadores da web. Um mapa do site pode ser configurado para indexar todas as páginas e imagens.

## Substituições de URL

A variável [Regravação de URL](url-rewrite.md) A ferramenta permite alterar qualquer URL associado a um produto, categoria ou página do CMS.

## Robôs do mecanismo de pesquisa

A configuração do Commerce inclui configurações para gerar e gerenciar instruções para rastreadores da Web e bots que indexam seu site. Se o pedido de `robots.txt` alcançar o Commerce (em vez de um arquivo físico), ele é roteado dinamicamente para o controlador de robôs. As instruções são diretivas reconhecidas e seguidas pela maioria dos mecanismos de pesquisa.

Por padrão, o arquivo robots.txt gerado pelo Commerce contém instruções para que o crawler da Web evite indexar determinadas partes do site que contêm arquivos usados internamente pelo sistema. Você pode usar as configurações padrão ou definir suas próprias instruções personalizadas para todos ou para mecanismos de pesquisa específicos. Há muitos artigos online que exploram o assunto em detalhes.

### Exemplo de instruções personalizadas

**Permite acesso total**

    User-agent:*
    Não permitir:

**Não permite acesso a todas as pastas**

    User-agent:*
    Não permitir: /

**Instruções padrão**

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

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize o **[!UICONTROL Global]** na primeira linha da grade e clique em **[!UICONTROL Edit]**.

   ![Configuração de design global](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Search Engine Robots]** e faça o seguinte:

   ![Configuração de design - robôs de mecanismo de pesquisa](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Definir **[!UICONTROL Default Robots]** a um dos seguintes:

     | Opção | Descrição |
     |------|------------|
     | `INDEX, FOLLOW` | Instrui os rastreadores da web a indexar o site e verificar novamente mais tarde se há alterações. |
     | `NOINDEX, FOLLOW` | Instrui os rastreadores da Web a evitar a indexação do site, mas a verificar novamente mais tarde se há alterações. |
     | `INDEX, NOFOLLOW` | Instrui os rastreadores da web a indexar o site uma vez, mas a não verificar novamente mais tarde se há alterações. |
     | `NOINDEX, NOFOLLOW` | Instrui os rastreadores da web a evitar a indexação do site e a não verificar novamente se há alterações. |

     {style="table-layout:auto"}

   - Se necessário, insira instruções personalizadas na caixa **[!UICONTROL Edit Custom instruction of robots.txt file]** caixa. Por exemplo, enquanto um site estiver em desenvolvimento, talvez você queira proibir o acesso a todas as pastas.

   - Para restaurar as instruções padrão, clique em **[!UICONTROL Reset to Default]**.

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.
