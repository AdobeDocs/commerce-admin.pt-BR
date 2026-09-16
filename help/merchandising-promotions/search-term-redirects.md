---
title: Redirecionamentos de termo de pesquisa e roteamento de vitrine eletrônica
description: Saiba como escolher redirecionamentos de termo de pesquisa, regravações de URL, regras do Live Search ou roteamento de vitrine por implantação para o Adobe Commerce e o Edge Delivery Services.
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 67a00b294f1946da5795cd8fb7ea9fac1c80edcd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%
---
# Redirecionamentos de termo de pesquisa e roteamento de vitrine eletrônica

Redirecionamentos de termo de pesquisa, redirecionamentos de URL e merchandising de pesquisa resolvem diferentes problemas. Use este guia para escolher a capacidade certa para a pesquisa padrão [!DNL Adobe Commerce], [!DNL Live Search] e [!DNL Commerce Storefront] viabilizada por [!DNL Edge Delivery Services].

## Entender os tipos de redirecionamento

Esses recursos diferem no que aciona o comportamento e no que o comprador vê:

* Um **redirecionamento de termo de pesquisa** envia um comprador que insere um termo de pesquisa específico para uma página designada.

* Um **redirecionamento de URL** envia uma solicitação de uma URL antiga para uma nova URL, geralmente com uma resposta HTTP 301 ou 302. A barra de endereços do navegador muda para o novo URL.

* **Merchandising de pesquisa** altera quais produtos aparecem, ou sua ordem, nos resultados da pesquisa sem alterar a URL solicitada.

* Uma **regravação de URL** mapeia uma URL para outra no servidor. A ferramenta de Reescrita de URL [!DNL Adobe Commerce] cria um redirecionamento permanente (301) para a URL antiga. Para obter mais informações, consulte [regravações de URL](url-rewrite.md).

## Escolha um recurso de roteamento

Use a orientação a seguir para identificar o recurso que corresponde aos seus requisitos:

| Requisito | Capacidade recomendada |
| --- | --- |
| Enviar uma consulta específica da pesquisa padrão [!DNL Adobe Commerce] para uma página | Configure um termo de pesquisa em [Gerenciar termos de pesquisa](../catalog/search-terms.md), onde houver suporte. |
| Alterar a classificação ou a visibilidade do produto nos resultados da pesquisa | Use [!DNL Live Search] [sinônimos](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/synonyms/synonyms) ou [regras de comercialização](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/rules/rules-add). |
| Redirecionar um produto, categoria ou URL do CMS antigo | Use a ferramenta [Reescrita de URL](url-rewrite.md) do Commerce quando ela se aplicar à sua implantação. |
| Redirecionar um caminho [!DNL Edge Delivery Services] | Use o roteamento de vitrine ou CDN. |
| Preservar URLs herdados após a migração de uma loja | Crie e teste um mapa de redirecionamento de URL herdado para novo. |

## Pesquisa padrão do Commerce

Com a pesquisa no catálogo padrão, você pode configurar um termo de pesquisa para abrir uma página de conteúdo, uma página de categoria, uma página de produto ou uma página externa na qual a implantação ofereça suporte a esse recurso. Use-a quando uma consulta inserida pelo comprador, como `gift cards` ou `returns`, precisar abrir uma campanha ou página informativa.

Para criar ou atualizar esse tipo de redirecionamento, consulte [Gerenciar termos de pesquisa](../catalog/search-terms.md). A configuração do termo de pesquisa é separada da ferramenta de regravação de URL porque o acionador é a consulta do comprador, não um URL existente.

>[!NOTE]
>
>Confirme se a loja usa a pesquisa padrão no catálogo e oferece suporte a redirecionamentos de termos de pesquisa nativos. O comportamento e a configuração disponível podem diferir para [!DNL Live Search], [!DNL Adobe Commerce as a Cloud Service] ou uma loja headless.

## Redirecionamentos e regravações de URL

Use uma regravação de URL quando a origem for um URL existente, em vez de um termo de pesquisa inserido pelo comprador. Exemplos comuns incluem redirecionamento:

* Um URL de produto antigo para um novo URL de produto.

* Um URL de categoria retirado para um URL de categoria substituto.

* Um URL desatualizado da página do CMS para um novo URL da página de conteúdo.

Para implantações que oferecem suporte à ferramenta de Reescrita de URL, vá para **[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]** para criar o redirecionamento. Para obter orientação passo a passo, consulte [regravações de URL](url-rewrite.md).

>[!NOTE]
>
>O tópico [URL reescreve](url-rewrite.md) e se aplica somente a PaaS. Para [!DNL Adobe Commerce as a Cloud Service] ou uma loja [!DNL Edge Delivery Services], use a orientação de roteamento para essa loja.

## Live Search

[!DNL Live Search] substitui a experiência de pesquisa padrão da loja e fornece recursos como sinônimos, facetas e regras de merchandising.

Use o [!DNL Live Search] quando precisar alterar a relevância da pesquisa, a classificação do produto ou a visibilidade do produto. Use sinônimos quando palavras diferentes devem retornar produtos semelhantes. Use as regras de merchandising quando os produtos precisarem ser promovidos, enterrados ou classificados de forma diferente.

O comportamento de pesquisa [!DNL Live Search] não deve ser tratado como uma substituição de menu suspenso para cada configuração de termo de pesquisa nativa do Commerce. Quando um query deve navegar para uma página de conteúdo ou campanha, implemente o redirecionamento na camada da vitrine ou do roteamento de borda que recebe a solicitação. Para obter mais informações, consulte a [[!DNL Live Search] documentação](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview).

## Edge Delivery Services

Para uma vitrine fornecida por [!DNL Edge Delivery Services], gerencie redirecionamentos na camada de vitrine ou de roteamento de borda. Não suponha que a URL de administrador [!DNL Adobe Commerce] reescreva o controle de cada solicitação.

Ao usar a criação de documentos, mantenha os mapeamentos de redirecionamento na configuração de redirecionamento do site. Para redirecionamentos que devem ser executados antes que uma solicitação atinja a origem, use a configuração apropriada de CDN ou borda. Para obter orientações de SEO relacionadas, consulte [diretrizes de SEO para a Commerce Storefront](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/).

## Migrar do Luma

Trate a migração de redirecionamento como parte da migração da loja. Preserve a jornada do cliente e a intenção da SEO e reimplemente o roteamento para a loja de destino.

Antes de alternar o tráfego para a nova loja:

1. Exporte e inventarie URLs do Luma existentes e páginas de aterrissagem de termos de pesquisa.

1. Classifique cada item como um redirecionamento de termo de pesquisa, redirecionamento de URL ou regra de merchandising.

1. Mapeie cada URL herdado para seu novo caminho de loja.

1. Implemente cada redirecionamento na camada que recebe a solicitação.

1. Códigos de status de teste, parâmetros de consulta, URLs canônicos, caminhos de localidade e loops de redirecionamento.

1. Monitore logs e análises após o lançamento para verificar se há URLs herdados não resolvidos.

## Solução de problemas de redirecionamentos

Use as seguintes verificações quando um redirecionamento não se comportar como esperado em [!DNL Adobe Commerce] exibições de pesquisa, roteamento de vitrine e loja.

| Problema | O que verificar |
| --- | --- |
| Um termo de pesquisa não é redirecionado | Confirme se a loja usa a pesquisa padrão no catálogo, se a consulta de pesquisa corresponde ao termo configurado e se o termo de pesquisa foi atribuído à exibição de loja correta. Se [!DNL Live Search] estiver habilitado, verifique se o redirecionamento está implementado na camada da loja ou da borda. |
| Um redirecionamento funciona no Luma, mas não no Edge Delivery Services | Confirme se o redirecionamento está configurado na [!DNL Edge Delivery Services] camada de vitrine ou de roteamento CDN. [!DNL Adobe Commerce] As substituições de URL de administrador podem não receber a solicitação. |
| O Live Search retorna resultados em vez de redirecionar | Use as regras de [!DNL Live Search] para a classificação e visibilidade do produto. Para navegar até uma página de conteúdo ou campanha, configure o redirecionamento na camada da loja ou da borda. |
| Um redirecionamento funciona em uma exibição de loja, mas não em outra | Verifique a exibição da loja atribuída ao termo de pesquisa ou à regra de URL. Teste o caminho completo do local e a consulta em cada exibição de armazenamento afetada. |

## Mais ajuda sobre este tópico

* [Visão geral e práticas recomendadas da SEO](seo-overview.md)

* [O que é vitrine eletrônica?](../getting-started/storefront.md)

* [Gerenciar termos de pesquisa](../catalog/search-terms.md)

* [Substituições de URL](url-rewrite.md)
