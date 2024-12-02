---
title: Atualizações de [!DNL Commerce]
description: Saiba como as atualizações do Adobe Commerce e do Magento Open Source afetam o catálogo e as  [!DNL Inventory Management]  configurações.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 392d8550741fe6fca3ea1301575c9ebb5e2483bd
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Atualizações de [!DNL Commerce]

Se você usou inventário de origem única em uma versão anterior, essas informações fornecem detalhes sobre novos recursos e alterações em suas configurações existentes de catálogo e inventário.

O [!DNL Inventory Management] for Adobe Commerce e Magento Open Source inclui recursos, melhorias e suporte ao desenvolvedor que aprimoram e atualizam todo o gerenciamento do estoque de produtos e adicionam novos recursos. Todos os recursos estão disponíveis prontos para uso, incluindo o Algoritmo de seleção da Source e Finalização simultânea para corresponder as quantidades da ordem às origens e ao atendimento da ordem. Dependendo dos sites, lojas e tipo de comerciante, você pode criar estoque e origens adicionais, atribuir valores de inventário e muito mais. Para obter informações completas, consulte [Inventory management](introduction.md).

Ao instalar o Magento Open Source 2.4.x ou o Adobe Commerce 2.4.x, ocorrem as seguintes alterações iniciais:

- Habilitar o [Inventory management](enable.md) no nível de loja global ou de produto. A opção Gerenciar Estoque habilita ou desabilita o rastreamento de quantidades de inventário, cálculos de quantidades de vendas agregadas e gerenciamento de reservas para rastrear compras até fatura e remessa. Você pode desativar essa opção para usar um ERP e outros serviços de terceiros para gerenciar estoque, pedidos e remessas. Para obter informações adicionais, consulte [!DNL Inventory Management] Módulos abaixo.

- Um [Source Padrão](sources-manage.md) e [Estoque Padrão](stocks-manage.md) são adicionados ao sistema. Não desative ou remova esses padrões. O [!DNL Commerce] atribui produtos existentes e recém-importados a esses padrões.

  >[!IMPORTANT]
  >
  >O uso do Estoque padrão e do Source padrão é altamente desencorajado porque fazem parte do módulo `CatalogInventory`, que foi descontinuado. Em vez disso, é recomendável criar e usar estoques e fontes personalizados.

   - Os estoques fornecem uma Quantidade Venável virtual agregada com reservas para rastrear carrinhos de compras e pedidos, garantindo check-out simultâneo.

   - Todos os produtos existentes no catálogo são atribuídos ao Source padrão. Até que você adicione novas origens, a interface do produto não será alterada. Se você entregar produtos apenas de um local, não haverá outras diferenças para origens. Você pode criar [fontes](sources-add.md) e [atribuir quantidades](quantities-manage.md) personalizadas por local de remessa.

   - Você pode configurar uma origem como um Local de Retirada e [atribuir quantidades](quantities-manage.md) para essa origem.

   - Seu site atribui ao Estoque padrão. Você pode criar [estoques](stocks-add.md) personalizados para conectar canais de vendas (sites) e fontes (locais).

- As [opções de configuração](configuration.md) adicionais são adicionadas aos seus produtos e à loja global. Algumas opções de configurações existentes recebem opções e comportamentos atualizados:

   - Notificar para Quantidade Abaixo envia notificações e deduções da Quantidade Venável.

   - O Limite esgotado suporta valores positivos, zero e negativos. Com Backorders ativados, os valores positivos são ignorados, considerados zero (ou infinitos).

   - As ordens pendentes suportam valores zero (infinitos) e negativos. Quando ativado, a opção Notificar para Quantidade Abaixo não deduz da Quantidade Vendível.

- Novas Reservas rastreiam vendas potenciais, convertendo em deduções de quantidade quando a ordem é enviada. Você nunca acessa ou cria reservas diretamente. [!DNL Commerce] cria e gerencia reservas nos bastidores por meio de pedidos, remessas e avisos de crédito.

- [Pedidos e remessas](shipments.md) inclui novos recursos para recomendar remessas usando o Algoritmo de Seleção do Source e oferece suporte a remessas parciais de várias fontes para atender a um pedido.

- Os novos [recursos de importação/exportação](inventory-import-export.md) permitem adicionar origens em massa, atualizar quantidades de estoque e definir o status de estoque (entrada/saída) para todas as SKUs do catálogo. Esses recursos permitem modificar para uma origem, uma origem selecionada ou todas as origens.

- Novas opções em massa por meio da página Grade de produtos oferecem suporte a [atribuição e desatribuição de fontes](bulk-assignment.md) e [transferência de estoque para a origem](inventory-transfer.md).

- [!DNL Inventory Management] dá suporte a catálogos B2B. Atualmente, todos os produtos B2B devem ser atribuídos ao Source padrão e ao Estoque padrão.

## [!DNL Commerce Order Management] e [!DNL Inventory Management]

O [Commerce Order Management (MCOM)][1] não é compatível com o [!DNL Inventory Management]. Quando instalados, os módulos MCOM fornecem todos os recursos de gerenciamento de estoque para [!DNL Commerce], incluindo gerenciamento de uma ou várias origens, estoques, reservas e muito mais. Os módulos [!DNL Inventory Management] são desabilitados por padrão.

O MCOM oferece amplos recursos e serviços para gerenciamento avançado de pedidos omnicanal, inventário global e multi-sourcing, distribuição de armazenamento para depósito e atendimento centralizado ao cliente. Para obter uma lista completa de recursos, consulte a [lista de Recursos do MCOM][2].

O [!DNL Inventory Management] estende os recursos existentes do [!DNL Commerce] com opções adicionais para rastrear pedidos em andamento, estoque disponível, estoque disponível para um estoque e APIs para desenvolvimento de extensão.

## [!DNL Inventory Management] módulos

Talvez você queira desabilitar [!DNL Inventory Management] módulos para:

- Acelere o upgrade dos comerciantes que estão atualmente no Adobe Commerce ou no Magento Open Source 2.0/2.1/2.2/2.3 e migre para a versão 2.4.x.

- Use módulos de inventário e gerenciamento de pedidos personalizados ou de terceiros.

- Use [!DNL Order Management System] para gerenciamento de estoque. O conector atual não dá suporte a interfaces [!DNL Inventory Management]. Para os comerciantes do OMS que estão atualizando para o Adobe Commerce 2.4.0, eles devem desativar esses módulos.

Para obter detalhes completos, consulte [Instalar e atualizar](install-update.md).

[1]: https://commerce-docs.github.io/oms-documentation-archive/
[2]: https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/
