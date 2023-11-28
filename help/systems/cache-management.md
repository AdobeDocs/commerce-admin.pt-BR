---
title: Gerenciamento de cache
description: Saiba como usar as ferramentas de gerenciamento de cache, que fornecem uma maneira fácil de melhorar o desempenho do seu site.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 0%

---

# Gerenciamento de cache

O sistema de gerenciamento de cache do Adobe Commerce e do Magento Open Source oferece uma maneira fácil de melhorar o desempenho do seu site. Sempre que um cache exigir uma atualização, um aviso será exibido na parte superior do espaço de trabalho para orientá-lo pelo processo. Siga o link para o Gerenciamento de cache e atualize os caches inválidos.

![Salvar atributo de produto - Mensagem de atualização do cache](./assets/product-attribute-save-msg-update-cache.png){width="500"}

>[!NOTE]
>
>Quando entidades de catálogo são alteradas, isso pode afetar outras páginas e invalidar vários caches simultaneamente. Ao revisar a página de gerenciamento de cache, você pode ver itens inválidos que exigem atualização quando foram _**não editado diretamente**_. Por exemplo, essa invalidação ocorre ao editar qualquer produto no catálogo e ele é atribuído a qualquer categoria, ou ao alterar qualquer regra de produto relacionada.

A variável _[!UICONTROL Cache Management]_A página mostra o status de cada cache principal e sua tag associada. Os botões grandes no canto superior direito podem ser usados para liberar o cache ou o Armazenamento de cache completo. Na parte inferior da página, há botões adicionais para liberar o cache de imagens do produto de catálogo e o cache de JavaScript/CSS.

Depois de limpar um cache, sempre atualize o navegador para garantir que você possa ver os arquivos mais recentes. A limpeza do cache do Commerce não limpa o cache do navegador da Web. Talvez seja necessário limpar o cache do navegador para ver o conteúdo atualizado.

Para obter mais informações técnicas, consulte [Visão geral do cache](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} no _Guia de desenvolvimento de front-end do Commerce_.

Acesse o _[!UICONTROL Cache Management]_ao executar uma das ações a seguir:

- Clique em **[!UICONTROL Cache Management]** na mensagem acima do espaço de trabalho.
- No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Gerenciamento de cache](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Práticas recomendadas para armazenamento em cache

A reindexação e o armazenamento em cache têm diferentes finalidades no Commerce. [Índices](index-management.md) rastreie informações do banco de dados para obter melhor desempenho de pesquisa, recuperação mais rápida de dados para vitrines e muito mais. Os caches salvam dados, imagens, formatos e similares carregados para melhorar o desempenho e acessar a loja.

- Sempre limpe o cache após instalar extensões/módulos. Você pode instalar uma ou mais extensões e, em seguida, liberar o cache.
- Liberar o cache após instalar o Commerce. Para instalações novas, você também deve reindexar.
- Liberar o cache após a atualização de uma versão do Open Source ou do Commerce para outra.
- Ao liberar caches, considere o tipo de cache e programe a liberação durante horários que não sejam de pico. Por exemplo, escolha um horário em que poucos clientes possam acessar o site, como tarde da noite ou manhã cedo. A limpeza de alguns tipos de cache durante os horários de pico resulta em uma carga alta para o administrador e pode resultar em um site inativo até a conclusão.
- Quando [reindexação](index-management.md), não é necessário executar também um cache de liberação.

## Recursos de função de gerenciamento de cache

O acesso a ações específicas de manutenção de cache pode ser atribuído aos usuários por função, incluindo opções para exibir, alternar e liberar caches. A Adobe recomenda ativar ações de liberação somente para usuários de nível de administrador. Fornecer acesso a todos os recursos de gerenciamento de cache pode afetar o desempenho da loja.

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

1. Definir **[!UICONTROL Actions]** para `Refresh` e clique em **[!UICONTROL Submit]**.

## Executar atualização de ação em massa

1. Para selecionar um grupo de caches, defina **[!UICONTROL Mass Actions]** a um dos seguintes:

   - `Select All`
   - `Select Visible`

1. Marque a caixa de seleção de cada cache a ser direcionado pela ação.

1. Definir **[!UICONTROL Actions]** para `Refresh` e clique em **[!UICONTROL Submit]**.

## Liberar o cache de imagem do produto

1. Em _[!UICONTROL Additional Cache Management]_, clique em **[!UICONTROL Flush Catalog Images Cache]**para limpar arquivos de imagem de produto pré-gerados.

   A variável `Image cache was cleaned` será exibida na parte superior do espaço de trabalho.

1. Limpe o cache do seu navegador.

## Liberar o cache JavaScript/CSS

1. Em _[!UICONTROL Additional Cache Management]_, clique em **[!UICONTROL Flush JavaScript/CSS Cache]**para limpar qualquer arquivo JavaScript e CSS que tenha sido mesclado em um único arquivo.

   A variável `The JavaScript/CSS cache has been cleaned` será exibida na parte superior do espaço de trabalho.

1. Limpe o cache do seu navegador.

## Liberar usando a linha de comando

O Commerce fornece opções adicionais de cache de liberação usando a linha de comando. Essas opções podem exigir o suporte do desenvolvedor para serem concluídas. Para obter detalhes completos e opções de comando, consulte [Gerenciar o cache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-cache.html){:target=&quot;_blank&quot;} no _Guia de configuração_.

## Controles

| Controle | Descrição |
|--- |--- |
| [!UICONTROL Mass Actions] | Marca a caixa de seleção de vários caches. Opções: <br/>**[!UICONTROL Select All]**— Seleciona a caixa de seleção de todos os caches.<br/>** Desmarcar tudo **— Limpa a caixa de seleção de todos os caches.<br/>**[!UICONTROL Select Visible]** — Marca a caixa de seleção de todos os caches visíveis. <br/>**[!UICONTROL Unselect Visible]**— Desmarca a caixa de seleção de todos os caches visíveis. |
| [!UICONTROL Actions] | Determina a ação a ser aplicada a todos os caches selecionados. Opções: <br/>**[!UICONTROL Enable]**— Habilita todos os caches selecionados.<br/>**[!UICONTROL Disable]** — Desativa todos os caches selecionados. <br/>**[!UICONTROL Refresh]**— Atualiza todos os caches selecionados. |
| [!UICONTROL Submit] | Aplica a ação a todos os caches selecionados. |

{style="table-layout:auto"}

### Botões

| Botão | Descrição |
|--- |--- |
| [!UICONTROL Flush Magento Cache] | Remove todos os itens no cache padrão do Commerce (`var/cache`), de acordo com as tags Commerce associadas. |
| [!UICONTROL Flush Cache Storage] | Remove todos os itens do cache, independentemente da tag de Comércio. Se o sistema usar um local de cache alternativo, todos os arquivos em cache usados por outros aplicativos serão removidos no processo. |
| [!UICONTROL Flush Catalog Images Cache] | Remove todas as imagens de catálogo redimensionadas e com marca d&#39;água automaticamente armazenadas no `media/catalog/product/cache`. Se as imagens carregadas recentemente não forem refletidas no catálogo, tente limpar o catálogo e atualizar o navegador. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Remove a cópia mesclada de arquivos JavaScript e CSS do cache. Se as alterações recentes na folha de estilos ou no JavaScript não forem refletidas no armazenamento, tente liberar o cache do JavaScript/CSS e atualizar o navegador. |
| [!UICONTROL Flush Static Files Cache] | Remove arquivos de visualização pré-processados e arquivos estáticos. |

{style="table-layout:auto"}

### Caches

| Cache | Descrição | Tag associada |
| ----- | ----------- | -------------- |
| [!UICONTROL Configuration] | Várias configurações XML que foram coletadas em módulos e mescladas.<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** -  `config.xml` | `CONFIG` |
| [!UICONTROL Layouts] | Instruções de criação de layout. | `LAYOUT_GENERAL_CACHE_TAG` |
| [!UICONTROL Blocks HTML output] | HTML de blocos de página. | `BLOCK_HTML` |
| [!UICONTROL Collections Data] | Arquivos de dados de coleção. | `COLLECTION_DATA` |
| [!UICONTROL Reflection Data] | Limpa os dados de reflexão da interface da API, que normalmente são gerados durante o tempo de execução. | `REFLECTION` |
| [!UICONTROL Database DDL operations] | Resultados de consultas DDL, como a descrição de tabelas ou índices. | `DB_DDL` |
| [!UICONTROL Compiled Config] | Resultados da compilação de código. | `COMPILED_CONFIG` |
| [!UICONTROL EAV types and attributes] | Cache de declaração de tipos de entidade. | `EAV` |
| [!UICONTROL Customer Notification] | Notificações temporárias exibidas na interface do usuário. | `CUSTOMER_NOTIFICATION` |
| [!UICONTROL Integrations Configuration] | Arquivo de configuração de integração. | `INTEGRATION` |
| [!UICONTROL Integrations API Configuration] | Arquivo de configuração da API de integrações. | `INTEGRATION_API_CONFIG` |
| [!UICONTROL Page Cache] | Armazenamento em cache de página inteira. | `FPC` |
| [!UICONTROL Translations] | Arquivos de tradução. | `TRANSLATE` |
| [!UICONTROL Web Services Configuration] | Configurações REST e SOAP, arquivo WSDL gerado. | `WEBSERVICE` |
| [!UICONTROL Target Rule] | Índice de regras de destino | `TARGET_RULE` |

{style="table-layout:auto"}

## Armazenamento em cache de página inteira

O Adobe Commerce e o Magento Open Source usam o cache de página inteira no servidor para exibir rapidamente páginas de categoria, produto e CMS. O armazenamento em cache de página inteira melhora o tempo de resposta e reduz a carga no servidor. Sem o armazenamento em cache, cada página pode precisar executar blocos de código e recuperar informações do banco de dados. No entanto, com o cache de página inteira ativado, uma página totalmente gerada pode ser lida diretamente do cache.

>[!NOTE]
>
>Recomenda-se que [Cache de verniz](https://varnish-cache.org/){:target=&quot;_blank&quot;} ser usado somente em um ambiente de produção.

O conteúdo em cache pode ser usado para processar as solicitações de tipos semelhantes de visitas. Como resultado, as páginas exibidas para um visitante casual podem ser diferentes daquelas exibidas para um cliente. Para fins de armazenamento em cache, cada visita é um dos três tipos:

- `Non-sessioned` - Durante uma visita sem sessão, o comprador visualiza as páginas, mas não interage com a loja. O sistema armazena em cache o conteúdo de cada página visualizada e o envia para outros compradores não sessão.
- `Sessioned` - Durante uma visita em sessão, os compradores que interagem com a loja — por meio de atividades como comparar produtos ou adicionar produtos ao carrinho — recebem uma ID de sessão. As páginas em cache geradas durante a sessão são usadas somente por esse comprador durante a sessão.
- `Customer` - As sessões do cliente são criadas para aqueles que se registraram em uma conta da sua loja e loja enquanto faziam logon nas respectivas contas. Durante a sessão, os clientes podem receber ofertas especiais, promoções e preços com base no grupo de clientes atribuído.

Para obter informações técnicas, consulte [Configurar e usar verniz](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=&quot;_blank&quot;} e [Usar Redis para a página Comércio e o cache padrão](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=&quot;_blank&quot;} no _Guia de configuração_.

**_Para configurar o cache de página inteira:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Full Page Cache]** seção.

   ![Configuração avançada - cache de página inteira](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Caching Application]** a um dos seguintes:

   - `Built-in Application`
   - `Varnish Caching`

1. Para definir o tempo limite do cache de páginas, insira o **[!UICONTROL TTL for public content]**. (O valor padrão é `86400`)

1. Se estiver usando verniz, preencha o **[!UICONTROL Varnish Configuration]** seção, como segue:

   - **[!UICONTROL Access list]** - Insira os endereços IP que podem limpar a configuração de verniz para gerar um arquivo de configuração. Separe várias entradas com uma vírgula. O valor padrão é `localhost`.

   - **[!UICONTROL Backend host]** - Digite o endereço IP do host de back-end que gera arquivos de configuração. O valor padrão é `localhost`.

   - **[!UICONTROL Backend port]** - Identifique a porta de back-end usada para gerar arquivos de configuração. O valor padrão é: `8080`.

   - **[!UICONTROL Grace period]** - Especifique o número de segundos a ser usado como um período de carência para gerar arquivos de configuração. Consulte [Configuração avançada de verniz](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) no _Guia de configuração_.

   - Para exportar a configuração como um `varnish.vcl` clique no botão da versão de Verniz que você usa.

   ![Configuração avançada - verniz de cache de página inteira](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
