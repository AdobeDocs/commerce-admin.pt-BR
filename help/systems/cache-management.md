---
title: Gerenciamento de cache
description: Saiba como usar as ferramentas de gerenciamento de cache, que fornecem uma maneira fácil de melhorar o desempenho do seu site.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '1828'
ht-degree: 0%

---

# Gerenciamento de cache

O sistema de gerenciamento de cache do Adobe Commerce e do Magento Open Source oferece uma maneira fácil de melhorar o desempenho do seu site. Sempre que um cache exigir uma atualização, uma notificação é exibida com um link para a página [!UICONTROL Cache Management] para concluir a atualização.

![Salvar atributo de produto - Mensagem de atualização do cache](./assets/product-attribute-save-msg-update-cache.png){width="500"}

A página _[!UICONTROL Cache Management]_&#x200B;mostra o status de cada cache primário e sua marca associada. Os botões grandes no canto superior direito podem ser usados para liberar o cache ou o Armazenamento de cache completo. Na parte inferior da página, botões adicionais permitem liberar o cache de imagens do produto de catálogo e o cache do JavaScript/CSS.

>[!IMPORTANT]
>
>Quando entidades de catálogo são alteradas, isso pode afetar outras páginas e invalidar vários caches simultaneamente. Ao revisar a página de gerenciamento de cache, você pode ver itens inválidos que exigem atualização quando _&#x200B;**não foram editados diretamente**&#x200B;_. Por exemplo, essa invalidação ocorre ao editar qualquer produto no catálogo atribuído a qualquer categoria ou ao alterar qualquer regra de produto relacionada.

Depois de limpar um cache, sempre atualize o navegador para garantir que você possa ver os arquivos mais recentes. Limpar o cache do Commerce não limpa o cache do navegador da Web. Talvez seja necessário limpar o cache do navegador para ver o conteúdo atualizado.

Informações técnicas adicionais sobre o cache do Adobe Commerce estão disponíveis na [Visão geral do cache](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target="_blank"} no _Guia de Desenvolvimento de Front-end do Commerce_.

Acesse a página _[!UICONTROL Cache Management]_&#x200B;seguindo um destes procedimentos:

- Clique no link **[!UICONTROL Cache Management]** na mensagem acima do espaço de trabalho.
- Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Gerenciamento de cache](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Práticas recomendadas para armazenamento em cache

A reindexação e o armazenamento em cache têm diferentes finalidades no Commerce. [Índices](index-management.md) rastreiam informações do banco de dados para obter melhor desempenho de pesquisa, recuperação de dados mais rápida para vitrines e muito mais. Os caches salvam dados, imagens, formatos e similares carregados para melhorar o desempenho e acessar a loja.

- Sempre limpe o cache após instalar extensões/módulos. Você pode instalar uma ou mais extensões e, em seguida, liberar o cache.
- Limpe o cache após instalar o Commerce. Para instalações novas, você também deve reindexar.
- Limpe o cache após atualizar de uma versão do Open Source ou Commerce para outra.
- Ao liberar caches, considere o tipo de cache e programe a liberação durante horários que não sejam de pico. Por exemplo, escolha uma hora em que poucos clientes usam o site, como tarde da noite ou manhã cedo. A limpeza dos tipos de cache durante o pico de demanda pode aumentar a carga no Administrador e fazer com que o site fique inativo até que a operação seja concluída.
- Ao [reindexar](index-management.md), não é necessário liberar o cache.

## Recursos de função de gerenciamento de cache

Você pode atribuir acesso a ações específicas de manutenção de cache para usuários por função, incluindo opções para exibir, alternar e liberar caches. A Adobe recomenda ativar ações de liberação somente para usuários de nível de administrador. Fornecer acesso a todos os recursos de gerenciamento de cache pode afetar o desempenho da loja.

![Recursos de função - gerenciamento de cache](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

Para obter informações sobre como atribuir recursos para conceder acesso a contas de usuário administrador, consulte [Recursos de função](permissions-user-roles.md#role-resources). Os seguintes recursos controlam o acesso às ferramentas de gerenciamento de cache:

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## Atualizar caches específicos

1. Para cada cache a ser atualizado, marque a caixa de seleção no início da linha.

1. Defina **[!UICONTROL Actions]** como `Refresh` e clique em **[!UICONTROL Submit]**.

## Executar atualização de ação em massa

1. Para selecionar um grupo de caches, defina **[!UICONTROL Mass Actions]** como um dos seguintes:

   - `Select All`
   - `Select Visible`

1. Marque a caixa de seleção para cada cache a ser atualizado.

1. Defina **[!UICONTROL Actions]** como `Refresh` e clique em **[!UICONTROL Submit]**.

## Liberar o cache de imagem do produto

1. Em _[!UICONTROL Additional Cache Management]_, clique em **[!UICONTROL Flush Catalog Images Cache]**&#x200B;para limpar os arquivos de imagem de produto pré-gerados.

   A mensagem `Image cache was cleaned` aparece na parte superior do espaço de trabalho.

1. Limpe o cache do seu navegador.

## Liberar o cache do JavaScript/CSS

1. Em _[!UICONTROL Additional Cache Management]_, limpe os arquivos JavaScript e CSS que foram mesclados em um único arquivo clicando em **[!UICONTROL Flush JavaScript/CSS Cache]**.

   A mensagem `The JavaScript/CSS cache has been cleaned` aparece na parte superior do espaço de trabalho.

1. Limpe o cache do seu navegador.

## Liberar usando a linha de comando

Os administradores de sistema e desenvolvedores com acesso ao servidor de aplicativos do Commerce também podem gerenciar a configuração de cache e cache a partir da linha de comando usando a CLI do Commerce. Consulte [Gerenciar o cache](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-cache#clean-and-flush-cache-types){:target="_blank"} no _Guia de Configuração_.

## Controles

| Controle | Descrição |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | Marca a caixa de seleção de vários caches. Opções: <br/>**[!UICONTROL Select All]**— Marca a caixa de seleção de todos os caches.<br/>**&#x200B; Desmarcar Tudo &#x200B;**— Limpa a caixa de seleção de todos os caches.<br/>**[!UICONTROL Select Visible]** — Marca a caixa de seleção de todos os caches visíveis. <br/>**[!UICONTROL Unselect Visible]**— Limpa a caixa de seleção de todos os caches visíveis. |
| [!UICONTROL Actions] | Determina a ação a ser aplicada a todos os caches selecionados. Opções: <br/>**[!UICONTROL Enable]**— Habilita todos os caches selecionados.<br/>**[!UICONTROL Disable]** — Desabilita todos os caches selecionados. <br/>**[!UICONTROL Refresh]**— Atualiza todos os caches selecionados. |
| [!UICONTROL Submit] | Aplica a ação a todos os caches selecionados. |

{style="table-layout:auto"}

### Botões

| Botão | Descrição |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | Remove todos os itens no cache padrão do Commerce (`var/cache`), de acordo com suas marcas Commerce associadas. |
| [!UICONTROL Flush Cache Storage] | Remove todos os itens do cache, independentemente da tag do Commerce. Se o sistema usar um local de cache alternativo, todos os arquivos em cache usados por outros aplicativos serão removidos no processo. |
| [!UICONTROL Flush Catalog Images Cache] | Remove todas as imagens de catálogo redimensionadas e com marca d&#39;água automaticamente armazenadas em `media/catalog/product/cache`. Se as imagens carregadas recentemente não forem refletidas no catálogo, tente limpar o catálogo e atualizar o navegador. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Remove a cópia mesclada dos arquivos JavaScript e CSS do cache. Se as alterações recentes na folha de estilos ou no JavaScript não forem refletidas no armazenamento, tente liberar o cache do JavaScript/CSS e atualizar o navegador. |
| [!UICONTROL Flush Static Files Cache] | Remove arquivos de visualização pré-processados e arquivos estáticos. |

{style="table-layout:auto"}

### Caches

A página [!UICONTROL Cache Management] lista os tipos de cache que você pode gerenciar do Administrador com seus status atuais. Esta seção descreve os tipos de cache padrão compatíveis com o Adobe Commerce. As colunas _Marca do Cache_ e _ID do Cache_ descrevem os valores usados no código do aplicativo Commerce:

- `cache_type_id` define o identificador exclusivo de um tipo de cache.

- `%CACHE_TYPE_TAG%` define a marca exclusiva a ser usada no escopo do tipo de cache.

Desenvolvedores e integradores de sistema usam esses valores para configurar e gerenciar o armazenamento em cache ao personalizar ou integrar com o Adobe Commerce, por exemplo, desenvolvendo integrações usando APIs do GraphQL.

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} O `cache_type_id` também é usado para gerenciamento de cache a partir da linha de comando do servidor de aplicativos usando a CLI do Commerce. Por exemplo, ` bin/magento cache:status config` exibe o status atual do cache de Configuração.

>[!NOTE]
>
>Desenvolvedores e integradores de sistemas podem personalizar e estender o sistema de gerenciamento de cache do Commerce para suportar módulos e integrações personalizados. Para obter detalhes, consulte [Configurar o armazenamento em cache](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/caching-overview) no _Guia de Configuração do Adobe Commerce_.

<!-- prettier-ignore -->

#### Detalhes da lista de cache

| Cache | Descrição | Armazenar tag em cache | ID do cache |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | O Commerce coleta a configuração XML de todos os módulos, mescla-a e salva o resultado mesclado no cache.<br>**[!UICONTROL System]**- `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br>Este cache também contém configurações específicas de armazenamento armazenadas no sistema de arquivos e no banco de dados. Limpar ou liberar esse tipo de cache após modificar os arquivos de configuração. | `CONFIG` | `config` |
| [!UICONTROL Layouts] | Layouts de página compilados, ou seja, os componentes de layout de todos os componentes. Limpar ou liberar este tipo de cache após modificar arquivos de layout. | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | Fragmentos de página do HTML por bloco. Limpe ou limpe esse tipo de cache após modificar a camada de exibição. | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | Arquivos de dados de coleção que armazenam os resultados de consultas de banco de dados. Se necessário, o Commerce limpa esse cache automaticamente, mas desenvolvedores de terceiros podem colocar quaisquer dados em qualquer segmento do cache. Limpe ou limpe esse tipo de cache se o módulo personalizado usar uma lógica que resulte em entradas de cache que o Commerce não pode limpar. | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | Limpa os dados de reflexão da interface da API, que normalmente são gerados durante o tempo de execução. | `REFLECTION` | `reflection` |
| `Database DDL operations` | Esquema de banco de dados. Se necessário, o Commerce limpa esse cache automaticamente, mas desenvolvedores de terceiros podem colocar quaisquer dados em qualquer segmento do cache. Limpe ou limpe esse tipo de cache depois de fazer alterações personalizadas no esquema do banco de dados. (Em outras palavras, essas são atualizações que o Commerce não cria.) Uma maneira de atualizar o esquema do banco de dados automaticamente é usando o comando de atualização setup:db-schema:do magento. | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | Resultados da compilação de código. | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | Armazena em cache respostas a solicitações de webhook. Para obter mais informações, consulte o [Guia do Webhooks](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2) na documentação do desenvolvedor do Commerce. | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | Armazena em cache a declaração de tipos de entidade para metadados relacionados a atributos de valor de atributo de entidade (EAV). Os atributos incluem rótulos de loja, links para código PHP relacionado, renderização de atributo, configurações de pesquisa e assim por diante. Normalmente, não é necessário limpar ou liberar esse tipo de cache. | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | Notificações temporárias exibidas na interface do usuário. | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | Armazena em cache os resultados dos resolvedores de consultas do GraphQL para entidades da galeria de mídia de clientes, páginas do CMS, blocos do CMS e produtos. Mantenha esse cache ativado para melhorar o desempenho do GraphQL. | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | Arquivo de configuração de integração. Limpe ou limpe esse cache após alterar ou adicionar integrações. | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | Configuração de APIs de integração compilada para integrações de loja. | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | Armazena personalizações em cache para o Administrador. Consulte [Configuração e teste de administrador](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/) no _Guia do SDK da interface do usuário do administrador_. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | Armazenamento em cache de página inteira. | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | Índice de regras de destino | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | Armazenamento em cache da estrutura da API da Web. | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | Arquivos de tradução. | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## Armazenamento em cache de página inteira

O Adobe Commerce e o Magento Open Source usam o armazenamento em cache de página inteira no servidor para exibir rapidamente páginas de categoria, produto e CMS. O armazenamento em cache de página inteira melhora o tempo de resposta e reduz a carga no servidor. Sem o armazenamento em cache, cada página pode precisar executar blocos de código e recuperar informações do banco de dados. No entanto, com o cache de página inteira ativado, uma página totalmente gerada pode ser lida diretamente do cache.

>[!NOTE]
>
>É recomendável que o [Cache de Verniz](https://varnish-cache.org/){:target="_blank"} seja usado somente em um ambiente de produção.

O conteúdo em cache pode ser usado para processar as solicitações de tipos semelhantes de visitas. Como resultado, as páginas exibidas para um visitante casual podem ser diferentes das páginas exibidas para um cliente. Para fins de armazenamento em cache, cada visita é um dos três tipos:

- `Non-sessioned` - Durante uma visita sem sessão, o comprador visualiza páginas, mas não interage com o armazenamento. O sistema armazena em cache o conteúdo de cada página visualizada e o envia para outros compradores não sessão.
- `Sessioned` - Durante uma visita em sessão, os compradores que interagem com o armazenamento recebem uma ID de sessão. As interações incluem atividades como comparar produtos ou adicionar produtos ao carrinho. As páginas em cache geradas durante a sessão são usadas somente por esse comprador durante a sessão.
- `Customer` - Sessões de clientes são criadas para clientes que fazem login e fazem compras usando suas contas registradas. Durante a sessão, os clientes podem receber ofertas especiais, promoções e preços com base no grupo de clientes atribuído.

Para obter informações técnicas, consulte [Configurar e Usar Verniz](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target="_blank"} e [Usar Redis para a página do Commerce e o cache padrão](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target="_blank"} no _Guia de Configuração_.

**_Para configurar o cache de página inteira:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Full Page Cache]**.

   ![Configuração avançada - cache de página inteira](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Caching Application]** como um dos seguintes:

   - `Built-in Application`
   - `Varnish Caching`

1. Para definir o tempo limite do cache de páginas, insira o **[!UICONTROL TTL for public content]**. (O valor padrão é `86400`)

1. Para especificar o número máximo de [identificadores de layout](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) a serem processados no ponto de extremidade HTTP [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html), digite o **[!UICONTROL Handles param size]**. Restringir o tamanho pode melhorar a segurança e o desempenho. (O valor padrão é `100`)

1. Se estiver usando verniz, conclua a seção **[!UICONTROL Varnish Configuration]** da seguinte maneira:

   - **[!UICONTROL Access list]** - Insira os endereços IP que podem limpar a configuração de verniz para gerar um arquivo de configuração. Separe várias entradas com uma vírgula. O valor padrão é `localhost`.

   - **[!UICONTROL Backend host]** - Insira o endereço IP do host de back-end que gera arquivos de configuração. O valor padrão é `localhost`.

   - **[!UICONTROL Backend port]** - Identifique a porta de back-end usada para gerar arquivos de configuração. Valor padrão: `8080`.

   - **[!UICONTROL Grace period]** - Especifique o número de segundos a ser usado como um período de carência para gerar arquivos de configuração. Consulte [Configuração avançada de verniz](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) no _Guia de Configuração_.

   - Para exportar a configuração como um arquivo `varnish.vcl`, clique no botão da versão de Verniz que você usa.

   ![Configuração avançada - verniz de cache de página inteira](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
