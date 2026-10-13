---
source-git-commit: bb5da9eea16601303b62ccc06327c6a832062c49
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%
---
# Problemas corrigidos do Adobe Commerce B2B (v1.5.4-alpha1)

## B2B v1.5.4-alpha1

*13 de outubro de 2026*

Foram corrigidos 23 problemas no código Adobe Commerce B2B 1.5.4-alpha1. Um subconjunto dos problemas corrigidos incluídos nesta versão está descrito abaixo.

### Interface do administrador

#### [B2B] Quantidades de produtos do pacote não preservadas após Atualizar Preços em cotações de back-end

Correção de um problema em que a quantidade de um item de pacote em uma cotação negociável de administrador revertia para seu valor anterior após editar a quantidade na grade após uma alteração de configuração por meio da caixa de diálogo Configurar.

_ACP2E-5005_

### B2B

#### A página Detalhes da Cotação [B2B] (loja e Administrador) perde as informações de item/produto quando o produto relacionado é excluído do catálogo

Correção do problema em que os produtos não vendáveis desaparecem das cotações negociáveis finalizadas

_ACP2E-4680_

#### A quantidade de produto do pacote não foi atualizada corretamente após o envio da cotação do back-end

Correção do problema em que as quantidades de opções de produtos agrupados não eram atualizadas ao reconfigurar uma cotação negociável no painel de administração. Anteriormente, as alterações feitas nas quantidades de opção do pacote por meio do botão Configurar eram silenciosamente descartadas.

_ACP2E-4801_

#### A grade de Empresas Administrativas da [NUVEM] [B2B] causa alta CPU do MySQL — consulta company_type / COUNT correlacionada

Correção do problema em que a grade Empresas de administração (Clientes → Empresas) causava alto uso do MySQL CPU e sessões de banco de dados de longa duração. Anteriormente, determinar o Tipo de empresa (Pai/Filho/Empresa) para cada linha exigia uma subconsulta correlacionada à tabela company_relation que era acionada uma vez por linha de empresa, tornando as consultas de listagem e contagem total O(N²) em escala; a correção substitui isso por um único JOIN pré-agregado que é executado uma vez, independentemente do tamanho do conjunto de dados.

_ACP2E-4846_

#### Pagamento na Conta (B2B) - O botão Editar Pedido está ausente para Pedidos pendentes enquanto estiver visível para CQO

O botão Editar pedido agora está disponível para pedidos feitos com Pagamento por conta. Anteriormente, não era possível editar um pedido feito com Pagamento em conta enquanto o pedido estava pendente

_ACP2E-4877_

#### Tempo limite do PHP salvando empresa B2B com superusuário multiempresa

Salvar uma empresa B2B ou carregar a página de superusuário da empresa no administrador não excede mais o tempo máximo de execução do PHP quando o superusuário da empresa é atribuído a um número muito grande de empresas.

_ACP2E-4967_

#### Cotações negociáveis [NO LOCAL] não atualizadas conforme esperado

Correção do problema em que as cotações negociáveis não eram atualizadas quando um produto presente em uma cotação negociável ativa era excluído.

_ACP2E-5001_

#### Cheques adicionais voláteis &quot;Pagamento por conta&quot;

Correção do problema em que o Pagamento por conta, um método de pagamento destinado exclusivamente a membros da empresa B2B, podia ser selecionado por clientes individuais (B2C) durante a finalização da compra. Anteriormente, esses clientes podiam incorretamente continuar com o Pagamento por conta em vez de receber o erro &quot;método de pagamento não disponível&quot;.

_ACP2E-5013_

#### A ação salvar do assistente de catálogo compartilhado apaga a estrutura de preços de um catálogo compartilhado

Correção de um problema quando a ação salvar do assistente de catálogo compartilhado apaga a estrutura de preços de um salvamento de catálogo compartilhado

_ACP2E-5015_

#### GraphQL customer.role retorna &quot;Erro interno de servidor&quot; para clientes B2C sem empresa

Correção do problema em que a consulta do cliente { role {...} } por meio do GraphQL retornava um &quot;Erro de servidor interno&quot; para clientes B2C não atribuídos a nenhuma empresa. Anteriormente, esta consulta disparava um erro de tipo do PHP porque uma ID de empresa nula era passada para um método com uma dica de tipo inteiro estrita.

_ACP2E-5017_

#### [B2B] O desconto de item de produto de pacote não é aplicado quando as quantidades de opção são atualizadas em Cotações de back-end

Correção do problema em que um desconto no nível do item aplicado a um produto Dynamic Price Bundle no back-end do administrador de Cotações não era refletido no Subtotal ou Subtotal (Excl. Tax) quando as quantidades de opção do pacote foram atualizadas por meio da caixa de diálogo Configurar. Anteriormente, o desconto aparecia na coluna de desconto, mas não reduzia o subtotal cotado.

_ACP2E-5034_

#### Recarregamentos de seção de requisição em cada navegação de página

Correção do problema em que a seção de requisição acionava um recarregamento desnecessário do AJAX em cada navegação de página de produto e categoria. Anteriormente, a seção era recarregada em cada carregamento de página para qualquer cliente com dados da lista de requisições não vazios, mesmo quando nenhuma alteração tinha sido feita.

_ACP2E-5037_

#### [B2B] Erro quando o endereço da empresa não contém dados de região

Correção de um problema em que as páginas Perfil da empresa e Editar cliente administrador exibiam um erro quando um endereço da empresa tinha uma região adicionada ao seu país depois que o endereço era salvo sem uma região. Agora, o endereço retorna corretamente ao texto da região armazenada, em vez de causar um erro.

_ACP2E-5092_

#### Atualização da empresa no administrador com localidade fora do inglês redefine o limite de crédito

Correção de um problema em que a edição dos detalhes de uma empresa B2B poderia redefinir involuntariamente o Limite de crédito configurado para 0 quando a localidade do administrador diferia da localidade padrão. O Limite de crédito agora é preservado corretamente, a menos que seja explicitamente modificado.

_ACP2E-5127_

#### O administrador restrito ao site da [NUVEM] não pode excluir os clientes quando a user_id colide com uma entity_id de cliente inacessível

Anteriormente, quando um administrador restrito a sites tentava excluir um cliente, o plug-in de verificação de permissão do sistema comparava a ID de usuário do próprio administrador com a
IDs de entidade do cliente para aplicar restrições de hierarquia da empresa, sem verificar se o usuário em exercício era realmente um cliente; se a ID de usuário do administrador aconteceu
para coincidir com a ID de entidade de um cliente não relacionado em um site que o administrador não pôde acessar, o plug-in tentou carregar esse registro de cliente inacessível
e a exclusão falhou com um erro &quot;mais permissões são necessárias&quot;, mesmo que o administrador tenha direitos válidos para o cliente que está sendo excluído. Isso foi resolvido
ao adicionar uma condição para que a comparação de ID do cliente só seja executada quando o usuário em exercício for realmente um cliente, o que significa que as exclusões iniciadas pelo administrador agora ignoram totalmente essa verificação — os administradores restritos podem excluir novamente os clientes em seus sites atribuídos sem serem bloqueados por registros de clientes não relacionados e inacessíveis

_ACP2E-5146_

#### O pedido B2B mostra o Nome da empresa incorreto nas Ordens de venda do administrador

Correção de um problema em que um nome de empresa incorreto era exibido para ordens de compra B2B em Ordens de venda de administração quando um usuário era atribuído a várias empresas.
O nome da empresa agora é exibido corretamente com base na empresa associada ao pedido.

_B2B-4656_

### B2B, carrinho e finalização

#### [NO PREM] [B2B] O carregador de Pedido Rápido congela ao tentar carregar um arquivo binário que termina com a extensão .CSV

Correção do problema em que o carregador de arquivo de Pedido rápido aceitava qualquer arquivo renomeado com uma extensão .csv, incluindo binários. Anteriormente, nenhuma validação de tipo MIME ou conteúdo era executada, portanto, arquivos não CSV (por exemplo, executáveis) podiam ser carregados e processados como se fossem listas SKU/QTY válidas.

_ACP2E-5212_

### B2B, GraphQL

#### Imprecisão da Contagem Total de GQL da Lista de Requisições

Correção do problema quando a consulta do GraphQL requisition_lists retornava um valor total_count incorreto, que refletia apenas o número de itens na página atual, em vez do número total de entidades de lista de requisições correspondentes aos critérios de consulta.

_ACP2E-4799_

### B2B, Ordem

#### Ajuda para limpar tabelas de cotações de mais de 59 milhões (sales_clean_quotes não pode ser executado)

Correção do problema em que o trabalho cron `sales_clean_quotes` expirava em instâncias com tabelas de aspas grandes. Anteriormente, a consulta de limpeza selecionava todas as colunas da tabela `negotiable_quote` desnecessariamente, fazendo com que o MySQL executasse uma classificação de arquivos completa em milhões de linhas; e cada aspas era excluída individualmente através da camada de modelo PHP, aumentando o custo de desempenho.

_ACP2E-4891 - [Contribuição de código do GitHub](https://github.com/magento/magento2/commit/b63925d9)_

### B2B, desempenho

#### [NUVEM] Acompanhamento de ACSD-70033: bloqueio na tabela magento_catalogpermissions_index_product. continuação

Anteriormente, a reindexação de permissões de catálogo com o Catálogo compartilhado ativado poderia resultar em um erro de deadlock, causando a falha da reindexação. Agora, a reindexação é concluída com sucesso mesmo quando vários processos do indexador são executados simultaneamente.

_ACP2E-4844_

### Conteúdo

#### As páginas do CMS criadas para sites diferentes estão exibindo páginas incorretas no front-end

Anteriormente, em configurações de vários sites, em que a chave de cache da página de destino de Restrição de site não tinha escopo por site, fazendo com que a página incorreta do CMS fosse distribuída na loja do site secundário. A chave de cache em WebsiteRestriction/Controller/Index/Stub.php agora inclui corretamente a ID do site atual resolvida por meio do gerenciador de loja.

_ACP2E-4593_

### Estrutura

#### [B2B] Ordens de compra não convertidas automaticamente em ordem de venda com AtiveMQ

Correção de um problema em que os consumidores iniciados pelo cron não processavam mensagens quando o AtiveMQ era usado com o protocolo STOMP. Como resultado, as ordens de compra aprovadas automaticamente não eram convertidas em ordens de venda. O processamento de mensagens para filas STOMP agora é mais confiável e consistente com as implementações de fila DB e AMQP.

_ACP2E-4349 - [Contribuição de código do GitHub](https://github.com/magento/magento2/commit/08b91f1a) - [Contribuição de código do GitHub](https://github.com/magento/inventory/commit/239464da)_

### Instalar e administrar

#### Correção de códigos de subdivisão ISO desatualizados da [Cloud]

Atualização dos códigos de região para 13 países para corresponder ao padrão ISO 3166-2. Anteriormente, alguns códigos de região não correspondiam ao padrão, o que poderia causar problemas com integrações de terceiros e conformidade internacional. Novas regiões adicionadas para Bélgica, Colômbia, Espanha, França, Itália e Letônia. Códigos de região atualizados para Áustria, Colômbia, Costa Rica, Alemanha, Estônia, Espanha, Finlândia, França, Índia, Islândia e Letônia.

_ACP2E-4495 - [Contribuição de código do GitHub](https://github.com/magento/magento2/commit/9b6a8bd9)_
