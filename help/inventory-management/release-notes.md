---
title: Notas de versão do [!DNL Inventory Management]
description: Revise as notas de versão para obter informações sobre todas as  [!DNL Inventory Management]  versões.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '3462'
ht-degree: 0%

---

# Notas de versão do [!DNL Inventory Management]

Essas notas de versão descrevem versões de [!DNL Inventory Management] e incluem:

![Novos](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e melhorias
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

[!DNL Inventory Management] é um projeto especial da Engenharia da Comunidade Magento Open Source aberto aos colaboradores. Para participar e contribuir, consulte o [repositório de projetos do GitHub](https://github.com/magento/inventory) e o [wiki](https://github.com/magento/inventory/wiki) para começar. Para discutir o projeto, ingresse no canal [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) ([autoinscrição](https://opensource.magento.com/slack)).

[Agendamento de lançamento](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html?lang=pt-BR){target="_blank"} para versões compatíveis e compatíveis.

## v1.2.7

As notas de versão do [!DNL Inventory Management] 1.2.7 estão incluídas nas [notas de versão do Core 2.4.7](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

O [!DNL Inventory Management] 1.2.6 (versão do módulo: `magento/inventory-metapackage = 1.2.6`) é compatível com a versão 2.4.6 e com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código do Magento Open Source.

![Problema corrigido](../assets/fix.svg) A loja agora exibe produtos compostos (configuráveis, agrupados e agrupados) como em estoque quando os produtos secundários que tinham sido vendidos são devolvidos ao estoque. Anteriormente, a loja indicou que o produto composto estava indisponível nessas condições. <!-- ACP2E-1106-->

![Problema corrigido](../assets/fix.svg) As opções de produto configuráveis agora são exibidas como esperado como indisponíveis na loja se a opção foi criada com a quantidade definida como 0 e **[!UICONTROL Display out-of-stock products]** está habilitada. <!-- ACP2E-1148-->

![Problema corrigido](../assets/fix.svg) Os caches de página de categoria não são mais invalidados quando a quantidade em estoque é alterada e o produto ainda está em estoque. O Adobe Commerce agora carrega as páginas do cache, em vez de regenerá-las quando a quantidade do produto (e nada mais) na página de categoria da loja muda. <!-- ACP2E-118-->

![Problema corrigido](../assets/fix.svg) A contagem de produtos da lista de categorias agora está correta ao usar o Estoque no modo de origem única com a configuração **[!UICONTROL Display Out-Of-Stock Products]** habilitada. O Adobe Commerce agora verifica se um produto pode ser vendido durante a contagem. <!-- ACP2E-1033-->

![Problema corrigido](../assets/fix.svg) As regras de preço do carrinho para entrega na loja agora funcionam como esperado quando o inventário é habilitado. Anteriormente, os descontos gerados pela regra de preço do carrinho não eram aplicados nessas condições. <!-- ACP2E-1015-->

![Problema corrigido](../assets/fix.svg) A atualização do inventário de produtos no modo agendado não limpa mais todos os caches. Anteriormente, o indexador de Inventário limpava todos os caches de configuração. <!-- ACP2E-1003-->

![Problema corrigido](../assets/fix.svg) O valor do atributo **[!UICONTROL Allow Multiple Boxes for Shipping]** de um produto no Inventário avançado agora é salvo conforme esperado. <!-- ACP2E-992-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora emite uma compensação de reserva precisa após um memorando de crédito de reembolso parcial para um pedido que foi feito com a retirada na loja. Anteriormente, uma reserva incorreta era salva na tabela `inventory_reservation` quando um usuário administrador criava um memorando de crédito sem marcar a caixa de seleção **[!UICONTROL Return to Stock]**. <!-- ACP2E-979-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais produtos configuráveis como esgotados na loja quando uma de suas variações é devolvida manualmente para estoque em implantações que implementam o inventário de várias origens. <!-- ACP2E-952-->

![Problema corrigido](../assets/fix.svg) A posição da coluna na grade de produtos (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) não é mais revertida para sua posição anterior depois que a página é recarregada em implantações com várias fontes de estoque configuradas. <!-- ACP2E-925-->

![Problema corrigido](../assets/fix.svg) A quantidade em estoque agora está correta após a emissão de um memorando de crédito para um produto virtual quando a caixa de seleção **[!UICONTROL Back to stock]** não está marcada. <!-- ACP2E-908-->

![Problema corrigido](../assets/fix.svg) Agora é possível salvar categorias com classificação automática de produto e escopo atribuídos a estoque não padrão. Anteriormente, o Adobe Commerce não salvava a categoria e exibia este erro: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Problema corrigido](../assets/fix.svg) O status configurável do estoque de produtos agora é atualizado conforme esperado quando o produto é criado com todas as variações configuráveis indisponíveis. <!-- ACP2E-813-->

![Correção de um problema](../assets/fix.svg) A ferramenta analisador de inconsistência de reserva agora funciona corretamente com pedidos parcialmente remetidos que contêm produtos configuráveis, agrupados e agrupados. Os tipos de produtos compostos são agora analisados. Anteriormente, os cancelamentos e reembolsos eram salvos apenas para produtos principais, não para itens de pedido de subprodutos de produtos configuráveis e de pacotes de entrega conjunta. <!-- ACP2E-924-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais um erro quando um usuário administrador tenta atribuir 200 ou mais fontes de estoque a um estoque ou produto. <!-- ACP2E-1180-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora oferece suporte à criação de um memorando de crédito para um pedido do qual um produto foi excluído. Anteriormente, os comerciantes não podiam criar um aviso de crédito quando os produtos tinham sido excluídos do pedido após a criação de uma fatura. O aplicativo exibiu este erro: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Problema corrigido](../assets/fix.svg) Os armazenamentos agora são filtrados com base em IDs de armazenamento únicas e múltiplas. O código de atributo de produto `event` foi adicionado à lista de códigos de atributo reservados. Anteriormente, o Relatório de estoque baixo gerava uma exceção quando o módulo Inventário era instalado. <!-- ACP2E-1017-->

![Problema corrigido](../assets/fix.svg) Os filtros de navegação em camadas agora funcionam como esperado, e os produtos indisponíveis agora são anexados à lista de produtos da categoria vitrine. O novo atributo de classificação `is_out_of_stock` usa o mapeador de campo dinâmico do Elasticsearch para a coleção de produtos da loja. <!-- ACP2E-748-->

![Problema corrigido](../assets/fix.svg) O status do estoque de produtos compostos (agrupados, agrupados e configuráveis) é atualizado conforme esperado quando o status do estoque de produtos derivados é alterado por uma chamada REST `POST /rest/V1/inventory/source-items`. <!-- ACP2E-1209-->

## v1.2.5

O [!DNL Inventory Management] 1.2.5 (versão do módulo: `magento/inventory-metapackage = 1.2.5`) é compatível com a versão 2.4.5 e com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código do Magento Open Source.

![Problema corrigido](../assets/fix.svg) O status padrão do estoque de estoque de produtos agrupados e de pacotes foi atualizado conforme esperado quando um comerciante cria uma remessa do Administrador. Anteriormente, o status desses produtos permanecia inalterado após a criação de uma remessa. <!--- ACP2E-418-->

![Problema corrigido](../assets/fix.svg) Os produtos configuráveis agora são devolvidos ao estoque quando uma das seguintes condições é atendida: 1. O produto principal tem pelo menos um filho salvo em estoque. 2. O próprio produto configurável foi atualizado e definido como **em estoque** e tinha pelo menos um filho em estoque. <!--- ACP2E-443-->

![Problema corrigido](../assets/fix.svg) As alterações de inventário implementadas por meio da API REST agora são refletidas, conforme esperado, nas páginas de detalhes do produto. O cache de produtos de catálogo agora é limpo depois de comparar o status do último estoque e o status atual. Anteriormente, a omissão da função de retorno de chamada resultava na avaliação incorreta de alterações no status do estoque, o que não acionava a limpeza necessária do cache. Como resultado, a loja não refletia as alterações de estoque. <!--- ACP2E-161-->

![Problema corrigido](../assets/fix.svg) Os produtos atribuídos ao estoque padrão e anteriormente indisponíveis agora ficam visíveis na loja após o item de origem ser atualizado usando o `/V1/inventory/source-items`. Anteriormente, esse ponto de extremidade de API REST definia o `stock_status` errado. <!--- ACP2E-562-->

![Correção de um problema](../assets/fix.svg) O cancelamento da atribuição de fontes de estoque por meio da ação em massa (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) agora funciona conforme esperado quando as fontes incluem SKUs duplicadas, exceto para um zero à esquerda (por exemplo, `01234` e `1234`). Anteriormente, o aplicativo não cancelava a atribuição de fontes de inventário e gerava um erro. <!--- ACP2E-2641-->

![Problema corrigido](../assets/fix.svg) O status do estoque de produtos agora é sempre **no estoque** na loja quando pedidos com atraso infinitos são habilitados e o produto é atribuído a um estoque personalizado, independentemente da quantidade com backorder. Anteriormente, os produtos ficavam sem estoque mesmo quando os pedidos pendentes eram ativados. <!--- ACP2E-664-->

![Problema corrigido](../assets/fix.svg) O estoque de produtos pai e filho configuráveis agora é atualizado corretamente depois que o item de origem é atualizado com `POST /V1/inventory/source-items`. Depois que o produto secundário é atualizado por meio da API do, um novo plug-in do Inventory para verificações de estoque padrão e atualiza a quantidade e o status configuráveis do produto. <!--- ACP2E-442-->

![Problema corrigido](../assets/fix.svg) Produtos agrupados indisponíveis não são mais listados na página Categoria da vitrine. <!--- ACP2E-2082-->

![Correção de um problema](../assets/fix.svg). Correção do nome do pacote em `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Problema corrigido](../assets/fix.svg) O status de pedidos pendentes agora é representado corretamente no Administrador após fazer um pedido com quantidade zero de produto em uma implantação de várias origens/estoque. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Problema corrigido](../assets/fix.svg) Os produtos de pacote indisponíveis não são mais exibidos na página Categoria da vitrine quando o produto de pacote é atualizado na seção de estoques. <!--- ACP2E-2012-->

![Problema corrigido](../assets/fix.svg) Problemas de compatibilidade com o PHP 7.4 são resolvidos. <!--- AC-3192-->

![Problema corrigido](../assets/fix.svg) O desempenho das operações de salvamento que incluem produtos de pacote que contêm muitas opções (várias 100) foi aprimorado. Anteriormente, salvar esses grandes pacotes de produtos levava vários minutos e, às vezes, resultava em tempos limite em implantações com os Serviços de inventário ativados. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Problema corrigido](../assets/fix.svg) A ferramenta de ação de produto em massa (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) agora funciona conforme esperado ao atribuir a origem de estoque a vários produtos quando as SKUs são duplicadas, exceto para um `0` principal (por exemplo, `01234` e `1234`). Anteriormente, apenas um produto recebia uma origem de inventário. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Problema corrigido](../assets/fix.svg) O campo `ProductInterface.only_x_left_in_stock` agora retorna 0 se o inventário for 0. Anteriormente, retornava um valor nulo. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Problema corrigido](../assets/fix.svg) Agora é possível editar o estoque padrão em Administrador **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Anteriormente, um erro do JavaScript era exibido no console quando você tentava adicionar ou remover fontes do estoque padrão, embora fosse possível atribuir sites ao estoque padrão. <!--- ACP2E-545-->

![Correção de um problema](../assets/fix.svg) <!--- ACP2E-274--> A contagem de produtos da lista de categorias agora está correta ao usar o modo de estoque de origem única com a configuração **[!UICONTROL Display Out-Of-Stock Products]** habilitada. Um novo plug-in agora usa `AreProductsSalableInterface` e `StockConfigurationInterface` para determinar o número total de produtos. Anteriormente, a lista de produtos da categoria retornava a quantidade de produto errada.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-322--> Os produtos configuráveis agora são movidos para a última posição na lista de produtos depois que o estoque é atualizado quando a configuração **[!UICONTROL Move out of stock to the bottom]** é habilitada. Uma nova consulta de banco de dados personalizada é implementada para negar a ordem de classificação do índice Elasticsearch, que ignora a ordem de classificação habilitada pelo Administrador. Anteriormente, os produtos configuráveis e seus produtos derivados não eram movidos para a parte inferior da lista quando essa configuração era ativada.

## v1.2.4

O Inventory management 1.2.4 (versão do módulo: `magento/inventory-metapackage = 1.2.4`) é compatível com a versão 2.4.4 e é compatível com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e com a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) O Commerce agora exibe um valor preciso de quantidade comercializável para todos os produtos na exibição da lista de produtos do Administrador. Anteriormente, ele exibia um valor em branco para a quantidade vendável de produtos em estoque com SKUs que continham caracteres especiais. <!--- MC-41936-->

![Problema corrigido](../assets/fix.svg) O desempenho melhorou nas ações de carrinho e check-out, como adicionar produtos ao carrinho em implantações com muitas (aproximadamente 10.000) fontes de inventário. <!--- MC-42570-->

![Correção de um problema](../assets/fix.svg) [!BADGE Somente para PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} O comando `bin/magento inventory:reservation:list-inconsistencies` agora lida corretamente com pedidos com remessas parciais, mesmo que as reservas sejam perdidas no banco de dados e o cache tenha sido limpo. Anteriormente, quando esse comando era executado com um cache previamente limpo, o Commerce exibia o seguinte erro: `Area code is not set`. <!--- MC-42142-->


![Problema corrigido](../assets/fix.svg) A indexação incremental de produtos filho de produtos agrupados não faz mais com que outros produtos agrupados sejam indexados incorretamente quando os filhos são compartilhados. <!--- MC-41963-->

![Problema corrigido](../assets/fix.svg) A página de categoria da loja agora exibe a contagem de produtos correta após remover um produto de uma categoria por API. Anteriormente, a contagem de produtos da página de categoria estava incorreta até que a reindexação ocorresse. <!--- MC-42287-->

![Problema corrigido](../assets/fix.svg) Os produtos configuráveis agora podem retornar ao estoque ao criar um memorando de crédito quando a opção **[!UICONTROL Manage Stock]** está desabilitada. Anteriormente, o Commerce não exibia a caixa de seleção **Retornar ao estoque** na página de criação do memorando de crédito quando essa opção estava desabilitada. <!--- MC-42002-->

![Problema corrigido](../assets/fix.svg) O gerenciamento do estoque de estoque que excede 10.000 itens foi aprimorado. Anteriormente, problemas de desempenho às vezes impediam os comerciantes de editar estoque no Admin antes de iniciar seu site. <!--- MC-42643-->

![Problema corrigido](../assets/fix.svg) A página **[!UICONTROL User Roles]** no Administrador é atualizada para fornecer aos administradores permissões restritas acesso à configuração de métodos de entrega. A seção _Métodos de remessa_ foi renomeada para _[!UICONTROL Delivery methods]_, e&#x200B;_[!UICONTROL In-Store Pickup]_ foi movido para a seção _[!UICONTROL Delivery methods]_. [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não cria mais uma reserva de produto duplicada depois que um memorando de crédito é atualizado pela API. <!--- MC-41757-->

![Correção do problema](../assets/fix.svg) Ao alternar da guia _[!UICONTROL Pick up in Store]_&#x200B;para a guia&#x200B;_[!UICONTROL Shipping]_ no fluxo de trabalho de check-out, o erro JavaScript não será mais disparado quando somente a Entrega de retirada na loja estiver disponível. <!--- MC-42808-->

![Problema corrigido](../assets/fix.svg) A quantidade de produtos comercializáveis e a quantidade de produtos em estoque agora estão sincronizadas corretamente. Anteriormente, a compensação da reserva de estoque não era recriada para pedidos cancelados. <!--- MC-42485-->

![Problema corrigido](../assets/fix.svg) O desempenho do validador foi otimizado para impedir a adição de uma nova origem ao produto filho de um produto agrupado com o tipo de remessa `Ship Together`. <!--- MC-43039-->

## 1.2.3

O [!DNL Inventory Management] 1.2.3 (versão do módulo: `magento/inventory-metapackage = 1.2.3`) é compatível com a versão 2.4.3 e com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código do Magento Open Source.

![Correção de um problema](../assets/fix.svg). Correção de vários problemas relacionados à visibilidade do produto composto no front-end.

![Correção de um problema](../assets/fix.svg) Melhoria no desempenho do gerenciamento de páginas do carrinho com a quantidade mínima necessária.

![Correção de um problema](../assets/fix.svg) Várias correções foram direcionadas para resolver problemas com criação de origem, itens esgotados, fornecimento de estoque, classificação de fontes alocadas, entrega na loja e comandos de inventário.

![Problema corrigido](../assets/fix.svg) [!DNL Commerce] agora dá suporte a códigos postais canadenses de três dígitos para entrega na loja. Códigos de seis dígitos não têm suporte devido a limitações definidas por `geonames.org`.

![Problema corrigido](../assets/fix.svg) Agora o Administrador exibe a quantidade correta de estoque padrão para produtos desabilitados na grade **Produtos** e na página **Editar Produto** para implantações de várias lojas.

![Problema corrigido](../assets/fix.svg) [!DNL Commerce] agora atualiza o cache do produto da categoria quando um produto de pacote volta ao estoque.

## 1.2.2

O [!DNL Inventory Management] 1.2.2 (versão do módulo: `magento/inventory-metapackage = 1.2.2`) é compatível com a versão 2.4.2 e com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código do Magento Open Source.

![Correção de um problema](../assets/fix.svg). Correção de vários problemas relacionados à visibilidade do produto composto no front-end.

![Correção de um problema](../assets/fix.svg) Melhoria no desempenho da página do carrinho durante a atualização da quantidade em B2B.

![Correção de um problema](../assets/fix.svg) Várias correções foram direcionadas para resolver problemas com coleta na loja, atualizações em massa e limite de inventário.

![Novo](../assets/new.svg) **Testes funcionais.** Introduziu novos testes funcionais e forneceu correções para testes existentes para torná-los mais estáveis.

## 1.2.1

O [!DNL Inventory Management] 1.2.1 (versão do módulo: `magento/inventory-metapackage = 1.2.1`) é compatível com a versão 2.4.1 e com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código do Magento Open Source.

![Correção de um problema](../assets/fix.svg). Correção de um problema conhecido relacionado ao trabalho `inventory_cleanup_reservations` do CRON e correção de um problema relacionado à funcionalidade de Seleção na Loja para produtos de pacote. Essa atualização também inclui melhorias gerais no cálculo de estoque, suporte a produtos de pacote e funcionalidade de backorder.

![Novo](../assets/new.svg) **Testes funcionais.** Introduziu novos testes funcionais para fornecer cobertura adicional à funcionalidade de Seleção na Loja.

## 1.2.0

Há suporte para o [!DNL Inventory Management] 1.2.0 (versão do módulo: `magento/inventory-metapackage = 1.2.0`) na versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e na base de código do Magento Open Source.

![Correção de um problema](../assets/fix.svg) Várias correções para resolver problemas de atribuição de código-fonte, suporte a recursos de ambiente escalável e compatibilidade com PHP 7.4, MySQL 8 e PHPUNIT 9.

![Novo](../assets/new.svg) **Método de entrega na loja.** Adicionada uma opção para que os usuários selecionem uma origem a ser usada como um local de retirada durante o check-out. Consulte [Entrega na loja](../stores-purchase/shipping-in-store-delivery.md) no _Guia de Experiência de Vendas e Compras_.

![Novo](../assets/new.svg) **Suporte ao produto de pacote para modo de várias origens.O Inventário do** suporta todos os tipos de produtos com múltiplas fontes.

![Novo](../assets/new.svg) **Reindexação assíncrona de estoque.** Adicionada a capacidade de reindexar o estoque de forma assíncrona e melhorar o desempenho de vários cenários críticos.

![Novas](../assets/new.svg) **Interfaces em massa.** Introdução de novas interfaces em massa para verificação de escalabilidade: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Novo](../assets/new.svg) **Maior cobertura de teste.** A nova funcionalidade é abordada com testes automatizados, incluindo cobertura estendida para problemas detectados e corrigidos.

![Problema conhecido](../assets/bug.svg) **Problema conhecido.** A ausência do campo `object_id` nos metadados das reservas está impedindo que o trabalho cron `inventory_cleanup_reservations` funcione corretamente. Esse problema foi introduzido no [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Solução alternativa:** Execute as seguintes consultas MySQL para limpar manualmente as reservas:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

O [!DNL Inventory Management] 1.1.6 (versão do módulo: `inventory-composer-metapackage = 1.1.6`) é compatível com a versão 2.3.6 e com a versão 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) Correções para resolver problemas relacionados a ordens pendentes, avisos de crédito, grade de relatório de baixo estoque, correções conectadas à ferramenta CLI &quot;resolver inconsistências&quot; e melhorias gerais.

![Novo](../assets/new.svg) **Reindexação assíncrona de estoque.** Adicionada a capacidade de reindexar o estoque de forma assíncrona e melhorar o desempenho de vários cenários críticos.

## 1.1.5

Há suporte para o [!DNL Inventory Management] 1.1.5 (versão do módulo: `inventory-composer-metapackage = 1.1.5`) com a versão 2.3.5 e ele é compatível com as versões 2.3.4, 2.3.3, 2.3.2, 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e Magento Open Source code base.

![Novo](../assets/new.svg) **Atualize o estoque assim que a SKU do produto for alterada.** Introdução a uma nova definição de configuração para alternar para o novo comportamento: &quot;Sincronizar com Catálogo&quot;.

![Novo](../assets/new.svg) **Testes funcionais.** Introdução de novos testes funcionais para eliminar a lacuna de cobertura de teste. Correção de vários problemas para tornar os testes mais estáveis e confiáveis).

![Problema conhecido](../assets/bug.svg) Correções para evitar a venda excessiva de produtos, visibilidade de produtos &quot;esgotados&quot; na loja, várias correções para suporte a ambientes escaláveis e melhorias na interface do usuário.

## 1.1.4

O [!DNL Inventory Management] 1.1.4 (versão do módulo: `inventory-composer-metapackage = 1.1.4`) é compatível com a versão 2.3.4 e com as versões 2.3.3, 2.3.2, 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e Magento Open Source code base.

![Problema corrigido &#x200B;](../assets/fix.svg)**Aumento de desempenho.** Lógica de agrupamento introduzida para o comando da CLI de Reservas de Inventário para reduzir o uso de memória e evitar casos em que o processo fica paralisado sem resposta.

![Novo &#x200B;](../assets/new.svg)**Maior cobertura de teste.** Apresentou vários novos testes funcionais. Quase todos os cenários de inventário manuais são cobertos por testes automatizados.

![Problema conhecido](../assets/bug.svg) Várias correções foram direcionadas para resolver problemas com avisos de crédito, produtos agrupados e ações de origem e de estoque em massa.

## 1.1.3

Há suporte para o [!DNL Inventory Management] 1.1.3 (versão do módulo: `inventory-composer-metapackage = 1.1.3`) na versão 2.3.3 e ele é compatível com as versões 2.3.2, 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e Magento Open Source code base.

![Problema corrigido &#x200B;](../assets/fix.svg)**Melhor integração com os recursos Adobe Commerce e B2B.** [!DNL Inventory Management] agora funciona corretamente com os seguintes recursos para sites que usam fontes e estoques de estoque não padrão:

- Fazer pedido por SKU (Adobe Commerce)
- Ordem rápida (B2B)
- Listas de requisições (B2B)

![Novo &#x200B;](../assets/new.svg)**Desempenho melhorado.O desempenho de navegação do catálogo da loja** foi aprimorado para sites que executam o estoque de estoque padrão e a fonte.

![Novo &#x200B;](../assets/new.svg)**Maior cobertura de teste.** A cobertura do teste funcional e de integração automatizado aumentou significativamente.

## 1.1.2

O [!DNL Inventory Management] 1.1.2 (versão do módulo: `inventory-composer-metapackage = 1.1.2`) é compatível com a versão 2.3.2 e com a versão 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código do Magento Open Source.

![Correção de um problema](../assets/fix.svg) Adicionada `source_code` à resposta para o ponto de extremidade REST do GET `/V1/shipments`. <!-- https://github.com/magento/inventory/pull/2142 -->

![Correção de um problema](../assets/fix.svg) Resolveu um problema para limpar corretamente as reservas e atualizar quantidades de produtos após emitir um memorando de crédito para uma ordem não remetida. Ao selecionar a opção para <!-- https://github.com/magento/inventory/pull/2179 -->

![Correção de um problema](../assets/fix.svg). Solução de um problema para salvar corretamente a quantidade de filhos de produtos configuráveis ao inserir quantidades durante a criação do produto. <!-- https://github.com/magento/inventory/pull/2158 -->

Os novos módulos do [!DNL Inventory Management] 1.1.2 Beta incluem:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Novo](../assets/new.svg) **Adição de um Ponto de Extremidade de Transferência de Estoque Parcial em Massa** - Os pontos de extremidade de transferência em massa atuais movem toda a quantidade atribuída de uma origem para uma origem de destino. O novo ponto de extremidade `/rest/V1/inventory/bulk-partial-source-transfer` permite que os comerciantes transfiram estoque parcial da origem para a origem como uma operação em massa. Para transferir uma quantidade específica de quantidade, insira uma solicitação para o ponto de extremidade com `sku`, `qty`, `origin_source_code` e `destination_source_code`. As transferências verificam se a origem está atribuída a `sku`, se existe quantidade suficiente para transferir e assim por diante. Consulte [Ações de massa de estoque](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} na documentação da API REST. <!-- https://github.com/magento/inventory/pull/2117 -->

![Novo](../assets/new.svg) **CLI de Reserva Adicionada** - Novos comandos fornecem opções para detectar e resolver inconsistências de reserva. À medida que os pedidos enviam e alteram o status, [!DNL Inventory Management] gera reservas e atualizações iniciais por meio de reservas de remuneração. Esses comandos retornam uma lista de inconsistências detectadas pelo ID do pedido, SKU e ID do estoque e criam reservas para resolver. Consulte a [CLI reference](cli.md) para obter mais informações. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Novo](../assets/new.svg) **Melhorias de desempenho para fontes e opções de SSA** - A classificação e seleção de fontes durante a remessa causou degradação de desempenho para estoques com um alto número de fontes. Esta versão oferece melhorias significativas de desempenho para listar e classificar origens disponíveis ao revisar e selecionar opções de SSA em entregas. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Novo](../assets/new.svg) **Suporte do GraphQL adicionado para o Inventory management** - Esta versão instala um novo módulo `magento/module-inventory-graph-ql`. Os [atributos ProductInterface](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} do GraphQL agora incluem os atributos `only_x_left_in_stock` e `stock_status` para suporte ao [!DNL Inventory Management]. <!-- https://github.com/magento/inventory/pull/2124 -->

![Novo](../assets/new.svg) **Interface simplificada para Fontes atribuídas** - A tabela Fontes atribuídas nas páginas de produto simplifica o conteúdo para facilitar as atualizações e aumentar o desempenho ao exibir muitas fontes. Todas as origens são listadas por nome de origem (passe o mouse sobre para `source_code`).

![Novo](../assets/new.svg) **Serviço de Exportação de Estoque Agregado** - Esta versão fornece um novo serviço de estoque agregado de exportação (mantendo reservas no sistema) para dar suporte a Canais de Vendas externos, como Amazon, eBay e anúncios de Compras da Google.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

O [!DNL Inventory Management] 1.1.0 (versão do módulo: `inventory-composer-metapackage = 1.1.0`) é compatível com a versão 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código do Magento Open Source. O [!DNL Inventory Management] 1.1.1 é lançado apenas como uma atualização de nome de pacote, com suporte para a versão 2.3.1 e compatível com a versão 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código do Magento Open Source.

![Problema corrigido](../assets/fix.svg) **Adição de suporte ao Elasticsearch para modos de origem única e múltipla** — Agora você pode configurar e usar o Elasticsearch com estoques personalizados. Consulte [Configurar serviço Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html?lang=pt-BR){target="_blank"} para obter informações sobre a instalação. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Problema corrigido](../assets/fix.svg) Resolveu problemas de desempenho com o Estoque padrão para aumentar drasticamente o desempenho com várias operações. As melhorias aumentam o desempenho para o modo de origem única, as páginas Transferir inventário para o Source, as páginas Categoria da vitrine e os cálculos de Quantidade Venável.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Problema corrigido](../assets/fix.svg) Problemas resolvidos com o status Fora de Estoque e Transferência de Estoque em massa para o Estoque de produtos configuráveis e agrupados. Selecionar os produtos principais e executar ações em massa não afeta o status do produto. Se o produto principal estava em estoque, ele permanece em estoque.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Novo](../assets/new.svg) **Algoritmo de Prioridade de Distância** — O Algoritmo de Prioridade de Distância é um novo Algoritmo de Seleção de Source pronto para uso para recomendações de remessa baseadas em distância. Este algoritmo compara o local do endereço de destino da entrega com os locais de origem para determinar a origem mais próxima para atender às entregas. A distância pode ser determinada pela distância física ou pelo tempo gasto viajando de um local para outro, usando dados de localização geocode importados ou direções do Google (direção de carro, caminhada ou bicicleta).

![Novo](../assets/new.svg) **Lista de quantidades de origem expandida** — Comerciantes com um alto número de fontes podem passar o mouse sobre todas as fontes por produto e exibi-las facilmente pela Grade de Produtos. Cada produto exibe no mínimo cinco fontes e quantidades correspondentes. Ao passar o cursor do mouse sobre as origens, você pode percorrer toda a lista de origens e quantidades atuais.

![Problema conhecido](../assets/bug.svg) Problema conhecido com o Magento Open Source e o Adobe Commerce v2.3.1 - A migração assíncrona de dados entre fontes encontra problemas devido a alterações nas APIs assíncronas com nomes de tópico que refletem nomes de classe e método PHP. É recomendável o uso de operações síncronas, configurando **[!UICONTROL Run asynchronously]** como `No`.
