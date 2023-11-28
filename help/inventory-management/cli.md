---
title: '[!DNL Inventory Management] Referência da CLI'
description: Saiba mais sobre os comandos fornecidos pelo [!DNL Inventory Management] módulo para gerenciar dados de inventário e definições de configuração.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!DNL Inventory Management] Referência da CLI

[!DNL Inventory Management] O fornece comandos para gerenciar dados de inventário e definições de configuração.

Esses comandos incluem:

- Verificando e resolvendo inconsistências de reserva que afetam a quantidade vendável
- Adicionar geocódigos para o algoritmo de Prioridade de Distância

## Resolver inconsistências de reservas

As reservas colocam uma retenção de quantidade vendável para SKUs de produto por estoque. Ao entregar, adicionar produtos, cancelar ou reembolsar uma ordem, as reservas de compensação são informadas para colocar ou limpar essas retenções.

[!DNL Inventory Management] O fornece dois comandos para verificar e resolver inconsistências de reserva:

- [`inventário:reservation:list-inconsistencies`](#list-inconsistencies-command)
- [`inventário:reservation:create-compensations`](#create-compensations-command)

### Causas de inconsistências de reserva

[!DNL Inventory Management] gera reservas para eventos importantes:

- Colocação de pedido (reserva inicial)
- Remessa de pedido (reserva de remuneração)
- Ordem de reembolso ou emissão de um aviso de crédito (reserva de compensação)
- Cancelamento de pedido (reserva de compensação)

As inconsistências de reserva podem ocorrer quando:

- [!DNL Inventory Management] perde a reserva inicial e insere muitas compensações de reserva (supercompensando e levando a valores inconsistentes)
- [!DNL Inventory Management] O coloca corretamente a reserva inicial, mas perde as reservas compensatórias.

Você pode revisar e verificar reservas manualmente na `inventory_reservation` tabela.

As seguintes configurações e eventos podem causar inconsistências de reserva:

- **Atualizar para 2.3.x com pedidos que não estão em um estado final (Concluído, Cancelado ou Fechado).** [!DNL Inventory Management] cria reservas compensatórias para essas ordens, mas não insere ou tem a reserva inicial que deduz da quantidade vendável. Recomenda-se o uso desses comandos após o upgrade para Adobe Commerce ou Magento Open Source v2.3.x de 2.1.x ou 2.2.x. Se você tiver ordens pendentes, os comandos atualizarão corretamente a quantidade e as reservas para vendas e atendimento de ordens.
- **Você não gerencia o estoque e depois altera essa configuração.** Você pode começar a usar o 2.3.x com **[!UICONTROL Manage Stock]** definir como `No` na configuração. [!DNL Commerce] não faz reservas em eventos de colocação e entrega de ordem. Se você ativar posteriormente a variável **[!UICONTROL Manage Stock]** e alguns pedidos forem criados, a Qtd. Venável será corrompida com a reserva de compensação quando você manipular e atender a esse pedido.
- **Você reatribui o Stock de um Site enquanto os pedidos são enviados para esse site**. A reserva inicial é inserida para o estoque inicial e toda a reserva de compensação é inserida para o novo estoque.
- **O total de todas as reservas pode não resolver para `0`.** Todas as reservas no escopo de um pedido em um estado final (Concluído, Cancelado, Fechado) devem ser resolvidas para `0`, limpando todas as retenções de quantidade vendável.

### Comando Listar inconsistências

A variável `list-inconsistencies` detecta e lista todas as inconsistências de reserva. Use as opções de comando para verificar apenas pedidos concluídos ou incompletos, ou todos.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Opções de comando:

- `-c`, `--complete-orders` - Retorna inconsistências para pedidos concluídos. Reservas incorretas ainda podem estar em espera para ordens concluídas.
- `-i`, `--incomplete-orders` - Retorna inconsistências para pedidos incompletos (parcialmente remetidos, não remetidos). Reservas incorretas podem reter uma quantidade suficiente ou insuficiente para as ordens.
- `-b`, `--bunch-size` - Define quantos pedidos devem ser carregados de uma vez.
- `-r`, `--raw` - Produção bruta.

Respostas usando `-r` retornar em `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` formato:

- A ID do pedido indica o escopo da inconsistência.
- O SKU indica o produto com a inconsistência.
- Quantidade define o valor a ser inserido para a compensação da reserva.
- A ID do estoque define o escopo para o estoque, que usa as reservas para calcular a quantidade vendável.

Exemplos:

```terminal
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```terminal
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Se nenhum problema for encontrado, essa mensagem retornará: Nenhuma inconsistência de ordem foi encontrada.

### Comando Criar compensações

A variável `create-compensations` cria reservas de remuneração. Dependendo da emissão, novas reservas são criadas para colocar ou liberar uma retenção na quantidade vendável.

Para criar reservas, forneça compensações usando o formato `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` como `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Opção de comando:

- `-r`, `--raw` - Retorna saída bruta.

Se o formato da solicitação estiver incorreto, a seguinte mensagem será exibida:

```terminal
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

À medida que o comando cria reservas, ele exibe mensagens indicando as atualizações por SKU, pedido e estoque.

```terminal
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Se o SKU de uma entrada de compensação incluir espaços, coloque o SKU entre aspas.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Detectar inconsistências e criar compensações

Você pode detectar inconsistências e criar compensações imediatamente usando uma barra vertical para executar as `list-inconsistencies` e `create-compensations`. Use o `-r` opção de comando para gerar e enviar os dados brutos para o `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Exemplo de resposta:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```terminal
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Após a conclusão das atualizações, execute o comando list para verificar:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```terminal
No order inconsistencies were found.
```

Também é possível canalizar os comandos para detectar inconsistências e criar compensações somente para incompletos (`-i`) ou completa (`-c`) pedidos.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importar geocódigos

[!DNL Inventory Management] fornece a [Algoritmo Prioridade de distância](distance-priority-algorithm.md), que ajuda a determinar a melhor opção para enviar um pedido completo ou parcial. O algoritmo usa informações de GPS ou geocódigos para calcular a distância entre a origem (um depósito ou outro local físico) de cada item em um pedido e o endereço de entrega. Com base nesses resultados, o algoritmo recomenda qual origem deve ser usada para entregar cada item na ordem.

O comerciante seleciona o provedor dos dados de GPS ou geocode necessários para calcular as distâncias:

- **GOOGLE MAP** usos [Plataforma Google Maps](https://mapsplatform.google.com/) serviços para calcular a distância e a hora entre o endereço de destino da entrega e os locais de origem. Essa opção requer um plano de faturamento da Google e pode gerar cobranças por meio do Google.

- **Cálculo offline** calcula a distância usando dados baixados de [geonames.org](https://www.geonames.org/) e importado para o Commerce com um comando. Essa opção é gratuita.

Para importar geocódigos para cálculo off-line:

Digite o seguinte comando com uma lista separada por espaços de [Códigos de país ISO-3166 alpha2](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Por exemplo:

```bash
bin/magento inventory-geonames:import us ca gb de
```

O sistema baixa e importa os dados de geocodes para o banco de dados e, em seguida, exibe a mensagem  `Importing <country code>: OK`.
