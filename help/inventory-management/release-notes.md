---
title: '[!DNL Inventory Management] notas de versão'
description: Revise as notas de versão para obter informações sobre tudo [!DNL Inventory Management] versões.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '3361'
ht-degree: 0%

---

# [!DNL Inventory Management] notas de versão

Estas notas de versão descrevem versões do [!DNL Inventory Management] e incluem:

![Novo](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e aprimoramentos
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

[!DNL Inventory Management] é um projeto especial de Engenharia da Comunidade do Magento Open Source aberto aos colaboradores. Para participar e contribuir, consulte [Projeto do GitHub](https://github.com/magento/inventory) repositório e [wiki](https://github.com/magento/inventory/wiki) para começar. Para discutir o projeto, participe da [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) canal ([autoinscrição](https://opensource.magento.com/slack)).

[Programação de lançamento](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} para versões compatíveis e compatíveis.

## v1.2.6

[!DNL Inventory Management] 1.2.6 (versão do módulo: `magento/inventory-metapackage = 1.2.6`) é compatível com a versão 2.4.6 e compatível com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) A loja agora exibe produtos compostos (configuráveis, agrupados e agrupados) como em estoque quando os produtos secundários que foram vendidos são devolvidos ao estoque. Anteriormente, a loja indicou que o produto composto estava indisponível nessas condições. <!-- ACP2E-1106-->

![Problema corrigido](../assets/fix.svg) As opções de produto configuráveis agora são exibidas conforme esperado, como indisponível na loja, se a opção foi criada com a quantidade definida como 0 e **[!UICONTROL Display out-of-stock products]** está ativado. <!-- ACP2E-1148-->

![Problema corrigido](../assets/fix.svg) Os caches de página de categoria não são mais invalidados quando a quantidade em estoque mudar e o produto ainda estiver em estoque. O Adobe Commerce agora carrega as páginas do cache, em vez de regenerá-las quando a quantidade do produto (e nada mais) na página de categoria da loja muda. <!-- ACP2E-118-->

![Problema corrigido](../assets/fix.svg) A contagem de produtos da lista de categorias agora está correta ao usar o Inventory no modo de origem única com o **[!UICONTROL Display Out-Of-Stock Products]** configuração ativada. O Adobe Commerce agora verifica se um produto pode ser vendido durante a contagem. <!-- ACP2E-1033-->

![Problema corrigido](../assets/fix.svg) As regras de preço do carrinho para entrega na loja agora funcionam como esperado quando o inventário é ativado. Anteriormente, os descontos gerados pela regra de preço do carrinho não eram aplicados nessas condições. <!-- ACP2E-1015-->

![Problema corrigido](../assets/fix.svg) A atualização do inventário de produtos no modo agendado não limpa mais todos os caches. Anteriormente, o indexador de Inventário limpava todos os caches de configuração. <!-- ACP2E-1003-->

![Problema corrigido](../assets/fix.svg) O valor para a variável **[!UICONTROL Allow Multiple Boxes for Shipping]** o atributo de um produto no Inventário avançado agora é salvo conforme esperado. <!-- ACP2E-992-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora emite uma compensação de reserva precisa após um aviso de crédito de reembolso parcial para um pedido que foi feito com a retirada na loja. Anteriormente, uma reserva incorreta era salva na variável `inventory_reservation` quando um usuário administrador criou um aviso de crédito sem selecionar a variável **[!UICONTROL Return to Stock]** caixa de seleção <!-- ACP2E-979-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais produtos configuráveis como indisponíveis na loja quando uma de suas variações é devolvida manualmente para estoque em implantações que implementam o inventário de várias origens. <!-- ACP2E-952-->

![Problema corrigido](../assets/fix.svg) Posição da coluna na grade de produtos (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) não reverte mais para sua posição anterior depois que a página é recarregada nas implantações com várias fontes de inventário configuradas. <!-- ACP2E-925-->

![Problema corrigido](../assets/fix.svg) A quantidade em estoque agora está correta depois que um aviso de crédito é emitido para um produto virtual quando o **[!UICONTROL Back to stock]** não está marcada. <!-- ACP2E-908-->

![Problema corrigido](../assets/fix.svg) Agora é possível salvar categorias com a classificação automática de produtos e o escopo atribuídos ao estoque não padrão. Anteriormente, o Adobe Commerce não salvava a categoria e exibia este erro: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Problema corrigido](../assets/fix.svg) O status configurável do estoque do produto agora é atualizado conforme esperado quando o produto é criado com todas as variações configuráveis de produto indisponível. <!-- ACP2E-813-->

![Problema corrigido](../assets/fix.svg) A ferramenta analisador de inconsistência de reserva agora funciona corretamente com pedidos parcialmente enviados que contêm produtos configuráveis, agrupados e agrupados. Os tipos de produtos compostos são agora analisados. Anteriormente, os cancelamentos e reembolsos eram salvos apenas para produtos principais, não para itens de pedido de subprodutos de produtos configuráveis e de pacotes de entrega conjunta. <!-- ACP2E-924-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais um erro quando um usuário administrador tenta atribuir 200 ou mais fontes de inventário a um estoque ou produto. <!-- ACP2E-1180-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora permite a criação de um memorando de crédito para um pedido do qual um produto foi excluído. Anteriormente, os comerciantes não podiam criar um aviso de crédito quando os produtos tinham sido excluídos do pedido após a criação de uma fatura. O aplicativo exibiu este erro: `Following products with requested skus were not found: s00001`. t <!-- ACP2E-1138-->

![Problema corrigido](../assets/fix.svg) As lojas agora são filtradas com base em IDs de loja únicas e múltiplas. A variável `event` o código de atributo do produto foi adicionado à lista de códigos de atributo reservados. Anteriormente, o Relatório de estoque baixo gerava uma exceção quando o módulo Inventário era instalado. <!-- ACP2E-1017-->

![Problema corrigido](../assets/fix.svg) Os filtros de navegação em camadas agora funcionam como esperado e os produtos indisponíveis agora são anexados à lista de produtos da categoria de vitrine. O novo `is_out_of_stock` o atributo sorting usa o mapeador de campo dinâmico Elasticsearch para a coleção de produtos da loja. <!-- ACP2E-748-->

![Problema corrigido](../assets/fix.svg) O status do estoque de produtos compostos (agrupados, configuráveis) é atualizado conforme esperado quando o status do estoque de produtos secundários é alterado por um REST `POST /rest/V1/inventory/source-items` chame. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (versão do módulo: `magento/inventory-metapackage = 1.2.5`) é compatível com a versão 2.4.5 e compatível com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) O status padrão do estoque de estoque de pacotes e produtos agrupados agora é atualizado conforme esperado quando um comerciante cria uma remessa do Administrador. Anteriormente, o status desses produtos permanecia inalterado após a criação de uma remessa. <!--- ACP2E-418-->

![Problema corrigido](../assets/fix.svg) Os produtos configuráveis agora são devolvidos ao estoque quando uma das seguintes condições é atendida: 1. O produto principal tem pelo menos um filho salvo em estoque. 2. O produto configurável foi atualizado e definido como **em estoque** e teve pelo menos um filho em estoque. <!--- ACP2E-443-->

![Problema corrigido](../assets/fix.svg) As alterações de inventário implementadas por meio da REST API agora são refletidas, conforme esperado, nas páginas de detalhes do produto. O cache de produtos de catálogo agora é limpo depois de comparar o status do último estoque e o status atual. Anteriormente, a omissão da função de retorno de chamada resultava na avaliação incorreta de alterações no status do estoque, o que não acionava a limpeza necessária do cache. Como resultado, a loja não refletia as alterações de estoque. <!--- ACP2E-161-->

![Problema corrigido](../assets/fix.svg) Os produtos atribuídos ao estoque padrão e que estavam anteriormente indisponíveis agora ficam visíveis na loja depois que o item de origem é atualizado usando `/V1/inventory/source-items`. Anteriormente, esse endpoint da REST API definia o incorreto `stock_status`. <!--- ACP2E-562-->

![Problema corrigido](../assets/fix.svg) Desatribuindo origens de estoque por meio da ação em massa (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) agora funciona conforme esperado quando as fontes incluem SKUs que são duplicatas, exceto para um zero à esquerda (por exemplo, `01234` e `1234`). Anteriormente, o aplicativo não cancelava a atribuição de fontes de inventário e gerava um erro. <!--- ACP2E-2641-->

![Problema corrigido](../assets/fix.svg) O status do estoque do produto agora é sempre **em estoque** na loja quando pedidos com atraso infinitos são ativados e o produto é atribuído a um estoque personalizado, independentemente da quantidade com backorder. Anteriormente, os produtos ficavam sem estoque mesmo quando os pedidos pendentes eram ativados. <!--- ACP2E-664-->

![Problema corrigido](../assets/fix.svg) O estoque de produto principal e secundário configurável agora é atualizado corretamente depois que o item de origem é atualizado com `POST /V1/inventory/source-items`. Depois que o produto secundário é atualizado por meio da API do, um novo plug-in do Inventory para verificações de estoque padrão e atualiza a quantidade e o status configuráveis do produto. <!--- ACP2E-442-->

![Problema corrigido](../assets/fix.svg) Os produtos agrupados indisponíveis não estão mais listados na página Categoria da vitrine eletrônica. <!--- ACP2E-2082-->

![Problema corrigido](../assets/fix.svg) Correção do nome do pacote em `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Problema corrigido](../assets/fix.svg) O status do pedido pendente agora é representado corretamente no administrador depois de fazer um pedido com quantidade zero de produto em uma implantação de várias origens/estoque. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Problema corrigido](../assets/fix.svg) Os produtos de pacote indisponíveis não são mais exibidos na página Categoria da loja quando o produto de pacote é atualizado na seção de estoques. <!--- ACP2E-2012-->

![Problema corrigido](../assets/fix.svg) Problemas de compatibilidade com o PHP 7.4 são resolvidos. <!--- AC-3192-->

![Problema corrigido](../assets/fix.svg) O desempenho das operações de salvamento que incluem pacotes de produtos com muitas opções (várias 100) é aprimorado. Anteriormente, salvar esses grandes pacotes de produtos levava vários minutos e, às vezes, resultava em tempos limite em implantações com os Serviços de inventário ativados. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Problema corrigido](../assets/fix.svg) A ferramenta de ação de produto em massa (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) agora funciona conforme esperado ao atribuir a origem do inventário a vários produtos quando as SKUs são duplicadas, exceto para uma entrega à esquerda `0` (por exemplo, `01234` e `1234`). Anteriormente, apenas um produto recebia uma origem de inventário. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Problema corrigido](../assets/fix.svg) A variável `ProductInterface.only_x_left_in_stock` O campo agora retorna 0 se o estoque for 0. Anteriormente, retornava um valor nulo. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Problema corrigido](../assets/fix.svg) Agora você pode editar o estoque padrão na guia Administrador **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Anteriormente, um erro de JavaScript era exibido no console quando você tentava adicionar ou remover fontes do estoque padrão, embora fosse possível atribuir sites ao estoque padrão. <!--- ACP2E-545-->

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-274--> A contagem de produtos da lista de categorias agora está correta ao usar o modo de origem única de estoque com o **[!UICONTROL Display Out-Of-Stock Products]** configuração ativada. Um novo plug-in agora usa `AreProductsSalableInterface` e `StockConfigurationInterface` para determinar o número total de produtos. Anteriormente, a lista de produtos da categoria retornava a quantidade de produto errada.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-322--> Os produtos configuráveis agora são movidos para a última posição na lista de produtos depois que o estoque é atualizado quando o **[!UICONTROL Move out of stock to the bottom]** está ativada. Uma nova consulta de banco de dados personalizada é implementada para negar a ordem de classificação do índice Elasticsearch, que ignora a ordem de classificação habilitada pelo administrador. Anteriormente, os produtos configuráveis e seus produtos derivados não eram movidos para a parte inferior da lista quando essa configuração era ativada.

## v1.2.4

Inventory management 1.2.4 (versão do módulo: `magento/inventory-metapackage = 1.2.4`) é compatível com a versão 2.4.4 e compatível com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) O Commerce agora exibe um valor preciso de quantidade disponível para todos os produtos na exibição da lista de produtos do Administrador. Anteriormente, ele exibia um valor em branco para a quantidade vendável de produtos em estoque com SKUs que continham caracteres especiais. <!--- MC-41936-->

![Problema corrigido](../assets/fix.svg) O desempenho melhorou para ações de carrinho e check-out, como adicionar produtos ao carrinho em implantações com muitas (aproximadamente 10.000) fontes de inventário. <!--- MC-42570-->

![Problema corrigido](../assets/fix.svg) A variável `bin/magento inventory:reservation:list-inconsistencies` O comando agora lida corretamente com pedidos com remessas parciais, mesmo que as reservas sejam perdidas do banco de dados e o cache tenha sido limpo. Anteriormente, quando esse comando era executado com um cache pré-limpo, o Commerce exibia o seguinte erro: `Area code is not set`. <!--- MC-42142-->

![Problema corrigido](../assets/fix.svg) A indexação incremental de produtos secundários de produtos agrupados não faz mais com que outros produtos agrupados sejam indexados incorretamente quando os secundários são compartilhados. <!--- MC-41963-->

![Problema corrigido](../assets/fix.svg) A página de categoria da loja agora exibe a contagem de produtos correta após remover um produto de uma categoria por API. Anteriormente, a contagem de produtos da página de categoria estava incorreta até que a reindexação ocorresse. <!--- MC-42287-->

![Problema corrigido](../assets/fix.svg) Os produtos configuráveis agora podem ser devolvidos ao estoque ao criar um aviso de crédito quando o **[!UICONTROL Manage Stock]** está desabilitada. Anteriormente, o Commerce não exibia a variável **Devolução para estoque** caixa de seleção na página criação do aviso de crédito quando essa opção estava desativada. <!--- MC-42002-->

![Problema corrigido](../assets/fix.svg) O gerenciamento do estoque de Estoque que excede 10.000 itens melhorou. Anteriormente, problemas de desempenho às vezes impediam os comerciantes de editar estoque no Admin antes de iniciar seu site. <!--- MC-42643-->

![Problema corrigido](../assets/fix.svg) A variável **[!UICONTROL User Roles]** A página no Administrador é atualizada para fornecer aos administradores permissões restritas acesso à configuração de métodos de delivery. A variável _Métodos de envio_ a seção foi renomeada para _[!UICONTROL Delivery methods]_, e_[!UICONTROL In-Store Pickup]_ é movido para _[!UICONTROL Delivery methods]_seção. [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não cria mais uma reserva de produto duplicada depois que um aviso de crédito é atualizado pela API. <!--- MC-41757-->

![Problema corrigido](../assets/fix.svg) Alternar do _[!UICONTROL Pick up in Store]_para a guia_[!UICONTROL Shipping]_ no fluxo de trabalho de check-out, a guia não acionará mais um erro de JavaScript quando somente a Entrega de coleta na loja estiver disponível. <!--- MC-42808-->

![Problema corrigido](../assets/fix.svg) A quantidade do produto comercializável e a quantidade do produto em estoque agora estão sincronizadas corretamente. Anteriormente, a compensação da reserva de estoque não era recriada para pedidos cancelados. <!--- MC-42485-->

![Problema corrigido](../assets/fix.svg) O desempenho do validador é otimizado para impedir a adição de nova origem ao produto filho de um produto agrupado com tipo de remessa `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (versão do módulo: `magento/inventory-metapackage = 1.2.3`) é compatível com a versão 2.4.3 e compatível com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) Correção de vários problemas relacionados à visibilidade do produto composto no front-end.

![Problema corrigido](../assets/fix.svg) Desempenho de gerenciamento de página do carrinho aprimorado com a quantidade mínima necessária.

![Problema corrigido](../assets/fix.svg) Várias correções foram direcionadas para resolver problemas com criação de origem, itens esgotados, seleção de fornecedor de estoque, classificação de origens alocadas, entrega na loja e comandos de inventário.

![Problema corrigido](../assets/fix.svg) [!DNL Commerce] O agora é compatível com códigos postais canadenses de três dígitos para entrega na loja. Os códigos de seis dígitos não são suportados devido às limitações definidas pelo `geonames.org`.

![Problema corrigido](../assets/fix.svg) O Administrador agora exibe a quantidade correta de estoque padrão para produtos desativados no **Produtos** e a **Editar produto** página para implantações em várias lojas.

![Problema corrigido](../assets/fix.svg) [!DNL Commerce] O agora atualiza o cache do produto da categoria quando um pacote de produtos retorna ao estoque.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (versão do módulo: `magento/inventory-metapackage = 1.2.2`) é compatível com a versão 2.4.2 e compatível com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) Correção de vários problemas relacionados à visibilidade do produto composto no front-end.

![Problema corrigido](../assets/fix.svg) Desempenho da página do carrinho aprimorado durante a atualização de quantidade em B2B.

![Problema corrigido](../assets/fix.svg) Várias correções direcionadas para resolver problemas com coleta na loja, atualizações em massa e limite de inventário.

![Novo](../assets/new.svg) **Testes funcionais.** Introduziu novos testes funcionais e forneceu correções para testes existentes a fim de torná-los mais estáveis.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (versão do módulo: `magento/inventory-metapackage = 1.2.1`) é compatível com a versão 2.4.1 e compatível com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) Correção de um problema conhecido relacionado ao `inventory_cleanup_reservations` cron e resolveu um problema relacionado à funcionalidade de retirada na loja para pacotes de produtos. Essa atualização também inclui melhorias gerais no cálculo de estoque, suporte a produtos de pacote e funcionalidade de backorder.

![Novo](../assets/new.svg) **Testes funcionais.** Foram introduzidos novos testes funcionais para fornecer cobertura adicional à funcionalidade Seleção na loja.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (versão do módulo: `magento/inventory-metapackage = 1.2.0`) é compatível com a versão 2.4.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e com a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) Várias correções para resolver problemas de atribuição de código-fonte, suporte a recursos de ambiente escalável e compatibilidade com PHP 7.4, MySQL 8 e PHPUNIT 9.

![Novo](../assets/new.svg) **Método de entrega na loja.** Adição de uma opção para que os usuários selecionem uma origem a ser usada como um local de retirada durante o check-out. Consulte [Entrega na loja](../stores-purchase/shipping-in-store-delivery.md) no _Guia de experiência de vendas e compras_.

![Novo](../assets/new.svg) **Suporte de produto de pacote para modo de várias origens.** O Inventory suporta todos os tipos de produtos com várias origens.

![Novo](../assets/new.svg) **Reindexação assíncrona de estoque.** Adição da capacidade de reindexar o estoque de forma assíncrona e melhoria do desempenho de vários cenários críticos.

![Novo](../assets/new.svg) **Interfaces em massa.** Introdução de novas interfaces em massa para verificação de escalabilidade: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Novo](../assets/new.svg) **Maior cobertura de teste.** A nova funcionalidade é abordada com testes automatizados, incluindo cobertura estendida para problemas detectados e corrigidos.

![Problema conhecido](../assets/bug.svg) **Problema conhecido.** A inexistência de uma `object_id` nos metadados de reservas está impedindo a `inventory_cleanup_reservations` o trabalho cron funcione corretamente. Esse problema foi introduzido no [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Solução alternativa:** Execute as seguintes consultas do MySQL para limpar manualmente as reservas:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (versão do módulo: `inventory-composer-metapackage = 1.1.6`) é compatível com a versão 2.3.6 e com a versão 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) Correções para resolver problemas relacionados a backorders, avisos de crédito, grade de relatório de baixo estoque, correções conectadas à ferramenta CLI &quot;resolver inconsistências&quot; e melhorias gerais.

![Novo](../assets/new.svg) **Reindexação assíncrona de estoque.** Adição da capacidade de reindexar o estoque de forma assíncrona e melhoria do desempenho de vários cenários críticos.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (versão do módulo: `inventory-composer-metapackage = 1.1.5`) é compatível com a versão 2.3.5 e com a versão 2.3.4, 2.3.3, 2.3.2, 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Novo](../assets/new.svg) **Atualizar estoque assim que o SKU do produto for alterado.** Introdução de uma nova configuração para alternar para o novo comportamento: &quot;Sincronizar com o catálogo&quot;.

![Novo](../assets/new.svg) **Testes funcionais.** Novos testes funcionais introduzidos para eliminar a lacuna de cobertura de teste. Correção de vários problemas para tornar os testes mais estáveis e confiáveis).

![Problema conhecido](../assets/bug.svg) Correções para evitar venda excessiva de produtos, visibilidade de produtos &quot;esgotados&quot; na loja, várias correções para suporte escalável ao ambiente e melhorias na interface do usuário.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (versão do módulo: `inventory-composer-metapackage = 1.1.4`) é compatível com a versão 2.3.4 e com as versões 2.3.3, 2.3.2, 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido ](../assets/fix.svg)**Maior desempenho.** Introdução da lógica de agrupamento para o comando da CLI de Reservas de Inventário para reduzir o uso de memória e evitar casos em que o processo trava sem nenhuma resposta.

![Novo ](../assets/new.svg)**Maior cobertura de teste.** Introdução de vários novos testes funcionais. Quase todos os cenários de inventário manuais são cobertos por testes automatizados.

![Problema conhecido](../assets/bug.svg) Várias correções destinadas a resolver problemas com avisos de crédito, produtos agrupados e ações de origem e estoque em massa.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (versão do módulo: `inventory-composer-metapackage = 1.1.3`) é compatível com a versão 2.3.3 e com as versões 2.3.2, 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido ](../assets/fix.svg)**Melhor integração com recursos do Adobe Commerce e B2B.** [!DNL Inventory Management] O agora funciona corretamente com os seguintes recursos para sites que usam fontes de inventário e estoques não padrão:

- Fazer pedido por SKU (Adobe Commerce)
- Ordem rápida (B2B)
- Listas de requisições (B2B)

![Novo ](../assets/new.svg)**Maior desempenho.** O desempenho de navegação do catálogo da loja é aprimorado para sites que executam o estoque de inventário padrão e a origem.

![Novo ](../assets/new.svg)**Maior cobertura de teste.** A cobertura de teste funcional e de integração automatizada aumentou significativamente.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (versão do módulo: `inventory-composer-metapackage = 1.1.2`) é compatível com a versão 2.3.2 e com as versões 2.3.1 e 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e Magento Open Source de base de código.

![Problema corrigido](../assets/fix.svg) Adicionado `source_code` à resposta da GET `/V1/shipments` Endpoint REST. <!-- https://github.com/magento/inventory/pull/2142 -->

![Problema corrigido](../assets/fix.svg) Correção da emissão para compensar corretamente as reservas e atualizar as quantidades de produtos após a emissão de um aviso de crédito para uma ordem não entregue. Ao selecionar a opção para <!-- https://github.com/magento/inventory/pull/2179 -->

![Problema corrigido](../assets/fix.svg) Solução do problema para salvar corretamente a quantidade de filhos de produtos configuráveis ao inserir quantidades durante a criação do produto. <!-- https://github.com/magento/inventory/pull/2158 -->

Novos módulos para o [!DNL Inventory Management] 1.1.2 As versões beta incluem:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Novo](../assets/new.svg) **Adição de um ponto de extremidade de transferência de estoque parcial em massa** - Os pontos de extremidade de transferência em massa atuais movem todas as quantidades atribuídas de uma origem para uma origem de destino. O novo `/rest/V1/inventory/bulk-partial-source-transfer` o endpoint permite que os comerciantes transfiram estoque parcial da origem para a origem como uma operação em massa. Para transferir uma quantidade específica de quantidade, insira uma solicitação para o ponto de extremidade com a `sku`, `qty`, `origin_source_code`, e `destination_source_code`. As transferências verificam se a origem está atribuída ao `sku`, existe quantidade suficiente para transferir e assim por diante. Consulte [Ações em massa de estoque](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} na documentação da REST API. <!-- https://github.com/magento/inventory/pull/2117 -->

![Novo](../assets/new.svg) **CLI de reserva adicionada** - Novos comandos que fornecem opções para detectar e resolver inconsistências de reserva. À medida que os pedidos enviam e alteram o status, [!DNL Inventory Management] gera reservas iniciais e atualizações por meio de reservas de remuneração. Esses comandos retornam uma lista de inconsistências detectadas pelo ID do pedido, SKU e ID do estoque e criam reservas para resolver. Consulte a [Referência da CLI](cli.md) para obter mais informações. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Novo](../assets/new.svg) **Melhorias de desempenho para origens e opções de SSA** - A classificação e seleção de origens durante a remessa causou degradação de desempenho em estoques com um grande número de origens. Esta versão oferece melhorias significativas de desempenho para listar e classificar origens disponíveis ao revisar e selecionar opções de SSA em entregas. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Novo](../assets/new.svg) **Adição de suporte do GraphQL para o Inventory management** - Esta versão instala um novo `magento/module-inventory-graph-ql` módulo. O GRAPHQL [Atributos de ProductInterface](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} agora inclui o `only_x_left_in_stock` e `stock_status` atributos para [!DNL Inventory Management] suporte. <!-- https://github.com/magento/inventory/pull/2124 -->

![Novo](../assets/new.svg) **Interface simplificada para fontes atribuídas** - A tabela Fontes atribuídas nas páginas de produto simplificou o conteúdo para facilitar as atualizações e aumentar o desempenho ao exibir muitas fontes. Todas as origens são listadas por nome de origem (passe o mouse sobre para `source_code`).

![Novo](../assets/new.svg) **Exportar serviço de estoque agregado** - Esta versão fornece um novo serviço de ações agregadas por exportação (mantendo reservas no sistema) para oferecer suporte a Sales Channel externos, como anúncios de compras do Amazon, eBay e Google.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (versão do módulo: `inventory-composer-metapackage = 1.1.0`) é compatível e compatível com a versão 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e com a base de código Magento Open Source. [!DNL Inventory Management] O 1.1.1 é lançado apenas como uma atualização de nome de pacote, compatível com a versão 2.3.1 e compatível com a versão 2.3.0 do Adobe Commerce, Adobe Commerce na infraestrutura em nuvem e a base de código Magento Open Source.

![Problema corrigido](../assets/fix.svg) **Adição de suporte para Elasticsearch para modos de uma única fonte e várias fontes** — Agora você pode configurar e usar o Elasticsearch com estoques personalizados. Consulte [Configurar serviço Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} para obter informações sobre a instalação. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Problema corrigido](../assets/fix.svg) Solução de problemas de desempenho com o Estoque padrão para aumentar drasticamente o desempenho com várias operações. As melhorias aumentam o desempenho para o modo de origem única, as páginas Transferir Inventário para Origem, Categoria de vitrine e os cálculos de Quantidade Venável.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Problema corrigido](../assets/fix.svg) Solução de problemas com o status Sem estoque e Transferência de estoque em massa para o Stock de produtos configuráveis e agrupados. Selecionar os produtos principais e executar ações em massa não afeta o status do produto. Se o produto principal estava em estoque, ele permanece em estoque.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Novo](../assets/new.svg) **Algoritmo de prioridade de distância** — O Algoritmo de prioridade de distância é um novo Algoritmo de seleção de origem pronto para uso para recomendações de entrega baseadas em distância. Este algoritmo compara o local do endereço de destino da entrega com os locais de origem para determinar a origem mais próxima para atender às entregas. A distância pode ser determinada pela distância física ou pelo tempo gasto viajando de um local para outro, usando dados de localização geocode importados ou direções do Google (direção de carro, caminhada ou bicicleta).

![Novo](../assets/new.svg) **Lista de quantidades de origem expandida** — comerciantes com um alto número de fontes podem passar o mouse sobre todas as fontes por produto e visualizá-las facilmente por meio da grade de produtos. Cada produto exibe no mínimo cinco fontes e quantidades correspondentes. Ao passar o cursor do mouse sobre as origens, você pode percorrer toda a lista de origens e quantidades atuais.

![Problema conhecido](../assets/bug.svg) Problema conhecido com o Magento Open Source e o Adobe Commerce v2.3.1 - A migração assíncrona de dados entre fontes encontra problemas devido a alterações nas APIs assíncronas com nomes de tópico que refletem nomes de classe e método PHP. Uso de operações síncronas, definição **[!UICONTROL Run asynchronously]** para `No`, é recomendado.
