---
title: '[!DNL Commerce] upgrades'
description: Saiba como as atualizações do Adobe Commerce e do Magento Open Source afetam o catálogo e [!DNL Inventory Management] configurações.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Commerce] atualizações

Se você usou inventário de origem única em uma versão anterior, essas informações fornecem detalhes sobre novos recursos e alterações em suas configurações existentes de catálogo e inventário.

[!DNL Inventory Management] O para Adobe Commerce e Magento Open Source inclui recursos, melhorias e suporte ao desenvolvedor que aprimoram e atualizam todo o gerenciamento do estoque de produtos e adicionam novos recursos. Todos os recursos estão disponíveis prontamente, incluindo o Algoritmo de Seleção de Origem e Finalização Concorrente para corresponder quantidades da ordem às origens e ao atendimento da ordem. Dependendo dos sites, lojas e tipo de comerciante, você pode criar estoque e origens adicionais, atribuir valores de inventário e muito mais. Para obter informações completas, consulte [Inventory management](introduction.md).

Ao instalar o Magento Open Source 2.4.x ou o Adobe Commerce 2.4.x, ocorrem as seguintes alterações iniciais:

- [Inventory management](enable.md) habilita no nível de loja global ou de produto. A opção Gerenciar Estoque habilita ou desabilita o rastreamento de quantidades de inventário, cálculos de quantidades de vendas agregadas e gerenciamento de reservas para rastrear compras até fatura e remessa. Você pode desativar essa opção para usar um ERP e outros serviços de terceiros para gerenciar estoque, pedidos e remessas. Para obter informações adicionais, consulte [!DNL Inventory Management] Módulos abaixo.

- A [Origem padrão](sources-manage.md) e [Estoque padrão](stocks-manage.md) adicionar ao sistema. Não desative ou remova esses padrões. [!DNL Commerce] atribui a esses padrões os produtos existentes e recém-importados.

  >[!IMPORTANT]
  >
  >O uso do Estoque padrão e da Origem padrão é altamente desencorajado porque fazem parte do `CatalogInventory` módulo, que agora está obsoleto. Em vez disso, é recomendável criar e usar estoques e fontes personalizados.

   - Os estoques fornecem uma Quantidade Venável virtual agregada com reservas para rastrear carrinhos de compras e pedidos, garantindo check-out simultâneo.

   - Todos os produtos existentes no catálogo atribuem à Origem padrão. Até que você adicione novas origens, a interface do produto não será alterada. Se você entregar produtos apenas de um local, não haverá outras diferenças para origens. Você pode criar relatórios [origens](sources-add.md) e [atribuir quantidades](quantities-manage.md) por local de entrega.

   - Você pode configurar uma origem como um Local de retirada e [atribuir quantidades](quantities-manage.md) para essa fonte.

   - Seu site atribui ao Estoque padrão. Você pode criar relatórios [estoques](stocks-add.md) para conectar canais de vendas (sites) e fontes (locais).

- Adicional [opções de configuração](configuration.md) adicione aos seus produtos e à loja global. Algumas opções de configurações existentes recebem opções e comportamentos atualizados:

   - Notificar para Quantidade Abaixo envia notificações e deduções da Quantidade Venável.

   - O Limite esgotado suporta valores positivos, zero e negativos. Com Backorders ativados, os valores positivos são ignorados, considerados zero (ou infinitos).

   - As ordens pendentes suportam valores zero (infinitos) e negativos. Quando ativado, a opção Notificar para Quantidade Abaixo não deduz da Quantidade Vendível.

- Novas Reservas rastreiam vendas potenciais, convertendo em deduções de quantidade quando a ordem é enviada. Você nunca acessa ou cria reservas diretamente. [!DNL Commerce] cria e gerencia reservas nos bastidores por meio de pedidos, remessas e avisos de crédito.

- [Pedidos e remessas](shipments.md) inclua novos recursos para recomendar entregas usando o Algoritmo de Seleção de Origem e suporte a entregas parciais de várias origens para preencher uma ordem.

- Novo [recursos de importação/exportação](inventory-import-export.md) permite adicionar origens em massa, atualizar quantidades de inventário e definir status de estoque (entrada/saída) para todos os SKUs no catálogo. Esses recursos permitem modificar para uma origem, uma origem selecionada ou todas as origens.

- Novas opções em massa por meio da página Grade de produtos suportam em massa [atribuindo e desatribuindo origens](bulk-assignment.md), e [transferindo inventário para origem](inventory-transfer.md).

- [!DNL Inventory Management] O suporta catálogos B2B. Atualmente, todos os produtos B2B devem ser atribuídos à Origem padrão e ao Estoque padrão.

## [!DNL Commerce Order Management] e [!DNL Inventory Management]

[Gerenciamento de pedidos de comércio (MCOM)][1] não é compatível com o [!DNL Inventory Management]. Quando instalados, os módulos MCOM fornecem todos os recursos de gerenciamento de inventário para [!DNL Commerce], incluindo gerenciamento de origem única e múltipla, estoques, reservas e muito mais. A variável [!DNL Inventory Management] Os módulos do são desativados por padrão.

O MCOM oferece amplos recursos e serviços para gerenciamento avançado de pedidos omnicanal, inventário global e multi-sourcing, distribuição de armazenamento para depósito e atendimento centralizado ao cliente. Para obter uma lista completa de recursos, consulte [Lista de recursos do MCOM][2].

[!DNL Inventory Management] estende o existente [!DNL Commerce] recursos com opções adicionais para rastrear pedidos em andamento, inventário em estoque, inventário disponível para um estoque e APIs para desenvolvimento de extensão.

## [!DNL Inventory Management] módulos

Talvez você queira desativar [!DNL Inventory Management] módulos para:

- Acelere o upgrade dos comerciantes que estão atualmente no Adobe Commerce ou no Magento Open Source 2.0/2.1/2.2/2.3 e migre para a versão 2.4.x.

- Use módulos de inventário e gerenciamento de pedidos personalizados ou de terceiros.

- Uso [!DNL Order Management System] para gerenciamento de estoque. O conector atual não dá suporte a [!DNL Inventory Management] interfaces. Para os comerciantes do OMS que estão atualizando para o Adobe Commerce 2.4.0, eles devem desativar esses módulos.

Para obter detalhes completos, consulte [Instalar e atualizar](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/
