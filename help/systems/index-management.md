---
title: Gerenciamento de índice
description: Saiba mais sobre o gerenciamento de índice, incluindo as ações que acionam a reindexação e as práticas recomendadas.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 0%

---

# Gerenciamento de índice

O Adobe Commerce e o Magento Open Source reindexam automaticamente sempre que um ou mais itens são alterados. As ações que acionam a reindexação incluem alterações de preço, criação de regras de preço de catálogo ou carrinho de compras, adição de novas categorias e assim por diante. Para otimizar o desempenho, o Commerce acumula dados em tabelas especiais usando indexadores. À medida que os dados são alterados, as tabelas indexadas devem ser atualizadas ou reindexadas. O Commerce reindexa como um processo em segundo plano e seu armazenamento permanece acessível durante os processos.

A reindexação de dados acelera o processamento e reduz o tempo de espera do cliente. Por exemplo, se você alterar o preço de um item de US$ 4,99 para US$ 3,99, o Commerce reindexa os dados para mostrar a alteração de preço na loja. Sem a indexação, a Commerce teria que calcular o preço de cada produto em tempo real; lidando com regras de preço de carrinho de compras, preços de pacotes, descontos, preços de camada e assim por diante. O carregamento do preço de um produto pode demorar mais do que o cliente está disposto a esperar.

Os indexadores podem ser definidos para atualizar ao salvar ou de acordo com a programação. Todos os índices podem usar qualquer uma das opções, exceto a Grade do Cliente, que oferece suporte apenas ao salvar. Ao indexar ao salvar, o Commerce inicia uma reindexação nas ações salvas. A página Gerenciamento de índice conclui a atualização e libera o cache, com a mensagem de reindexação aparecendo dentro de um ou dois minutos. Ao reindexar em uma programação, uma reindexação é executada de acordo com uma programação como um trabalho cron. Uma mensagem do sistema será exibida se um [trabalho do cron](cron.md) não estiver disponível para atualizar indexadores que se tornarem inválidos. Seu armazenamento permanece acessível durante os processos de reindexação.

>[!NOTE]
> Os comerciantes do Adobe Commerce que usam o Live Search, o Serviço de Catálogo ou as Recomendações de Produto têm a opção de usar um [indexador de preços baseado em SaaS](https://experienceleague.adobe.com/docs/commerce/price-indexer/index.html).

Quando uma reindexação é necessária, uma notificação é exibida na parte superior da página. O índice e a mensagem são apagados com base no modo de reindexação e nas possíveis ações que você realizar. Para obter informações mais detalhadas sobre indexação, consulte [Como o aplicativo implementa a indexação](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) no _Guia do Desenvolvedor do PHP_.

![Gerenciamento de índice - ações](./assets/index-management.png){width="700" zoomable="yes"}

- O Gerenciamento de índice tem uma apresentação ligeiramente diferente para catálogos de produtos simples.
- Para evitar problemas quando vários usuários Administradores atualizarem objetos que acionam a reindexação automática, é recomendável configurar todos os indexadores para serem executados de acordo com o agendamento como [trabalhos cron](cron.md). Caso contrário, sempre que um objeto for salvo, qualquer objeto com interdependências poderá causar um deadlock. Os sintomas de um impasse incluem alto uso de CPU e erros de MySQL. Como prática recomendada, é recomendável usar a indexação programada.
- ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Por padrão, as ações de administrador, como reindexação, são registradas pelo sistema e podem ser exibidas no [Relatório de Logs de Ação](action-log-report.md). O log de ações pode ser configurado no [Log de Ações do Administrador](action-log.md) nas configurações administrativas avançadas do seu armazenamento.

## Práticas recomendadas para reindexação

A reindexação e o armazenamento em cache têm diferentes finalidades no Commerce. Os índices rastreiam as informações do banco de dados para melhorar o desempenho da pesquisa, recuperar dados mais rapidamente para vitrines e muito mais. [Os caches](cache-management.md) salvam dados, imagens, formatos e outros itens carregados para melhorar o desempenho do carregamento e do acesso à loja.

- Normalmente, você deseja reindexar ao atualizar dados no Commerce.
- Se você tiver uma grande loja ou várias lojas, convém definir indexadores como categoria e produtos para trabalhos cron agendados devido à possibilidade de loop de reindexação. Talvez você queira definir o reindexação em um cronograma durante horas que não sejam de pico.
- Ao reindexar, não é necessário executar também um cache de liberação.
- Para novas instalações do Commerce, você deve liberar o cache e reindexar.
- A limpeza de caches e reindexação não limpa o cache do navegador da Web do computador. Limpe o cache do navegador após concluir as atualizações na loja.

## Alterar o modo de índice

>[!IMPORTANT]
>
>Para armazenamentos que usam o [Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=pt-BR) e definiram o Elasticsearch como o indexador de texto completo (`catalogsearch_fulltext`): o índice de texto completo deve ser executado novamente após qualquer alteração de permissões em massa ou quando o indexador &quot;permissões&quot; estiver no modo &quot;Agendado&quot;.

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Marque a caixa de seleção para cada indexador que você deseja alterar.

1. Defina **[!UICONTROL Actions]** como um dos seguintes:

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >A Grade de Clientes só pode ser reindexada usando `Update on Save`. Este índice **_não_** oferece suporte a `Update by Schedule`.

1. Clique em **[!UICONTROL Submit]** para aplicar a alteração a cada indexador selecionado.

   **Colunas de Gerenciamento de Índice**

   | Coluna | Descrição |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | O nome do indexador. |
   | [!UICONTROL Description] | Uma descrição do indexador. |
   | [!UICONTROL Mode] | Indica o modo de atualização atual de cada indexador. Opções: <br/>**[!UICONTROL Update on Save]**- O índice é definido para atualização sempre que uma alteração de entidade é salva. Essas entidades incluem produtos, categorias e clientes. Quando a ação de salvamento for concluída, uma série de etapas começará a capturar as alterações e a atualizar o índice. A página Gerenciamento de índice atualiza e libera a mensagem de reindexação em um ou dois minutos.<br/>**[!UICONTROL Update on Schedule]** - O índice está definido para ser atualizado de acordo com a agenda, de acordo com um [trabalho do cron](cron.md). O trabalho cron inclui o intervalo de agendamento para reindexação, gravando atualizações no índice quando executado. |
   | [!UICONTROL Schedule Status] | Exibe as atualizações de status do agendamento. |
   | [!UICONTROL Status] | Exibe um dos seguintes: <br/>**[!UICONTROL Ready]**— O índice está atualizado.<br/>**[!UICONTROL Suspended]** - Reindexação em pausa. <br/>**[!UICONTROL Processing]**- Reindexação em execução no momento.<br/>**[!UICONTROL Reindex Required]** - Foi feita uma alteração que requer reindexação, mas os indexadores não podem ser atualizados automaticamente. Verifique se [cron](cron.md) está disponível e configurado corretamente. |
   | [!UICONTROL Updated] | Indica a data e a hora em que um índice foi atualizado pela última vez. |

   {style="table-layout:auto"}

## Reindexar usando a linha de comando

O Commerce fornece opções adicionais de reindexação usando a linha de comando. Para obter detalhes completos e opções de comando, consulte [Reindexar](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html?lang=pt-BR#reindex){:target="blank"} no _Guia de Configuração_.

## Eventos de gatilho de índice

## Reindexação de acionadores

| Tipo de índice | Reindexação de evento |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Adicionar grupo de clientes<br/>Alterar definições de configuração |
| [!UICONTROL Flat catalog product data] | Adicionar repositório<br/>Adicionar grupo de repositório<br/>Adicionar, editar ou excluir atributo (para pesquisa e filtragem) |
| [!UICONTROL Flat catalog category data] | Adicionar repositório<br/>Adicionar grupo de repositório<br/>Adicionar, editar ou excluir atributo (para pesquisa e filtragem) |
| [!UICONTROL Catalog category/product index] | Adicionar, editar ou excluir produtos (único, em massa e importação)<br/>Alterar relações entre produtos e categorias<br/>Adicionar, editar ou excluir categorias<br/>Adicionar ou excluir lojas<br/>Excluir grupos de lojas<br/>Excluir sites |
| [!UICONTROL Catalog search index] | Adicionar, editar ou excluir produtos (único, em massa e importação)<br/>Adicionar ou excluir lojas<br/>Excluir grupos de lojas<br/>Excluir sites |
| [!UICONTROL Stock status index] | Alterar as configurações de inventário. |
| [!UICONTROL Category permissions index] | Adicionar repositório<br/>Adicionar grupo de repositório<br/>Adicionar, excluir ou atualizar atributo (para pesquisa e filtragem) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>O uso de um catálogo simples não é mais recomendado como prática recomendada. O uso continuado desse recurso é conhecido por causar degradação de desempenho e outros problemas de indexação. Consulte [Usar produto de catálogo simples](../catalog/catalog-flat.md) para obter mais informações.

## Indexar ações e controles

| Ação | Resultado | Controles |
| ------ | ------ | -------- |
| Criando uma loja, um novo grupo de clientes ou qualquer ação listada em `Actions that Cause a Full Reindex` | Reindexação completa | A reindexação completa é executada de acordo com a programação determinada pelo trabalho cron do Adobe Commerce ou do Magento Open Source. |
| Carregamento de itens em massa (importação/exportação do Commerce, consulta SQL direta e qualquer outro método que adicione, altere ou exclua dados diretamente) | Reindexação parcial (somente os itens alterados são reindexados) | Na frequência determinada pelo trabalho cron do Commerce. |
| Alteração do escopo (por exemplo, de global para site) | Reindexação parcial (somente os itens alterados são reindexados) | Na frequência determinada pelo trabalho cron do Commerce. |

{style="table-layout:auto"}

## Eventos que acionam a reindexação completa

| Indexador | Evento |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Criar um repositório Web<br/>Criar uma exibição de repositório Web<br/>Criar ou excluir um atributo que seja qualquer um dos seguintes:<br/>- Pesquisável ou visível na pesquisa avançada<br/>- Filtrável<br/>- Filtrável na pesquisa<br/>- Usado para classificação<br/>Alterar um atributo existente para que ele seja qualquer um dos anteriores.<br/>Habilitar opções de vitrine de categoria simples |
| [!UICONTROL Catalog Product Flat Indexer] | Criar um repositório Web<br>Criar uma exibição de repositório Web<br/>Criar ou excluir um atributo que seja qualquer um dos seguintes:<br/>- Pesquisável ou visível na pesquisa avançada<br>- Filtrável<br>- Filtrável na pesquisa<br/>- Usado para classificação <br/>Alterar um atributo existente para ser qualquer um dos anteriores.<br/>Habilitar opções de vitrine de categoria simples |
| [!UICONTROL Stock status indexer] | Quando as _Opções de inventário de catálogo_ a seguir forem alteradas na configuração do sistema:<br/>`Stock Options` - Exibir Produtos sem Estoque<br/>`Product Stock Options` - Gerenciar Estoque |
| [!UICONTROL Price Indexer] | Adicionando um grupo de clientes.<br/>Quando qualquer uma das opções de Inventário de Catálogo a seguir for alterada na configuração do sistema:<br/>`Stock Options` - Exibir Produtos sem Estoque<br/>`Product Stock Options` - Gerenciar Estoque<br/>`Price` - Escopo do Preço do Catálogo |
| [!UICONTROL Category or Product Indexer] | Criar ou excluir uma exibição de loja<br/>Excluir uma loja<br/>Excluir um site |

{style="table-layout:auto"}
