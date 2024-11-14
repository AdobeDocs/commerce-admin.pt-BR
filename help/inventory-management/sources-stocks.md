---
title: Estoques e fontes
description: Saiba mais sobre as relações entre produtos, fontes e estoques.
exl-id: 01bbbd82-898b-4757-ab40-0d8b89ec59bc
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Estoques e fontes

Gerencie o estoque, independentemente do local do depósito, do tipo de produto ou serviço ou do canal de vendas. Atenda a pedidos e entregue produtos de vários depósitos, lojas tradicionais, centros de distribuição e entrega direta para concluir ordens com foco no inventário balanceado, custos de entrega e muito mais.

Essas descrições incluem produtos, fontes e estoques para uma empresa de bicicletas com vários locais de remessa e sites nos Estados Unidos e na Europa.

## Origens

[Fontes](sources-manage.md) são os locais físicos onde o inventário de produtos é gerenciado e enviado para atendimento de pedidos ou onde os serviços estão disponíveis. Esses locais podem incluir depósitos, lojas tradicionais, centros de distribuição e carregadores. O [!DNL Commerce] usa as quantidades e as quantidades comercializáveis por estoque e gerencia automaticamente os valores de estoque dos produtos e pedidos gerenciados. Se você tiver uma origem, será considerado no modo _fonte única_. Se você tiver várias origens, será considerado no modo _várias origens_.

Uma origem pode ter prioridade no escopo de estoque em um depósito, mas não necessariamente em todos os depósitos, pois a origem pode ser reutilizada em diferentes estoques. O número de estoques e fontes aumenta a complexidade para determinar o melhor depósito ou loja para atender a um pedido. Por exemplo, você pode ter um número limitado de produtos disponíveis em seus locais tradicionais com um inventário extenso em seus depósitos e serviços em locais-chave com disponibilidade limitada.

Neste exemplo, o comerciante tem uma mountain bike disponível para remessa a partir de lojas, armazéns e um drop shipper.

![Exemplo de diagrama de fontes](assets/diagram-sources.png){width="600" zoomable="yes"}

## Estoques

[Ações](stocks-manage.md) representam um inventário agregado virtual de produtos disponíveis para venda em seus canais de vendas (sites). Cada estoque mapeia seus canais de vendas com origens para inventários disponíveis e quantidades comercializáveis. Dependendo da configuração do site, o estoque pode ser atribuído a um ou mais canais e fontes de vendas.

Os Sales Channel representam entidades que vendem seu inventário, incluindo sites, visualizações de lojas, grupos de clientes B2B e assim por diante. Os canais de vendas só podem ser associados a um Estoque. Cada canal de vendas só pode ter um único estoque atribuído a ele, e um único estoque pode ser atribuído a vários sites. Por meio do estoque, você pode modificar a priorização das fontes usadas ao enviar pedidos e pelo [Algoritmo de seleção Source](selection-reservations.md).

Você começa com um Estoque padrão atribuído com o Source padrão e seu site, melhor usado por comerciantes de origem única. Somente o Source padrão pode ser atribuído a esse estoque. Comerciantes de várias origens criam estoques personalizados para fontes e sites personalizados, conforme necessário.

![Diagrama para exemplo de ações para um armazenamento](assets/diagram-stock.png){width="600" zoomable="yes"}

## Quantidades do produto

Quantidade é o número de produtos no inventário ativo que estão disponíveis para compra. A quantidade de produtos aumenta e diminui quando você conclui remessas ou ajusta o inventário. A adição de produtos ao carrinho não afeta essa quantidade. A Quantidade Venável rastreia a disponibilidade do produto para um canal de vendas e também usa esse valor para determinar o estoque disponível para compra. Dependendo do número de origens, você verá e gerenciará a quantidade do produto para uma das seguintes opções:

- **Quantidade** - Para comerciantes de origem única, a coluna e o valor _[!UICONTROL Quantity]_controlam a quantidade de estoque disponível.
- **Quantidade por Source** - Para comerciantes de várias origens, a coluna e os valores _[!UICONTROL Quantity per Source]_controlam o estoque disponível por localização. Se você adicionar várias origens, esse valor substituirá a Quantidade e listará cada origem e quantidade atribuída.

As reservas rastreiam solicitações de estoque para todo o processo de compras — adicionar produtos ao carrinho, concluir o check-out e gerenciar reembolsos. Para estoque e estoque disponíveis, as reservas reservam valores de estoque por ordem por meio do processo de finalização, subtraídos da quantidade vendável. As reservas são convertidas em deduções de quantidade ao faturar e enviar produtos.

A Quantidade Venável calcula o inventário virtual de produtos (ou disponibilidade), usando limites configurados, valores reservados ou vendidos e quantidades por origem. Para cada estoque, [!DNL Commerce] acessa todas as fontes atribuídas e agrega quantidades de produtos associadas. Com esse valor base, ele subtrai todos os valores de reserva e o limite _[!UICONTROL Notify for Quantity Below]_.

![Calculando a quantidade vendável de um estoque](assets/diagram-salable-quantity.png){width="600" zoomable="yes"}

## Configurações de inventário

Cada produto, origem e estoque inclui várias opções para configurar o para sua loja no nível global, de origem, de estoque e de produto. Para obter uma lista completa dessas opções, consulte [Configurando o Inventory management](configuration.md).

Estas são opções importantes a serem compreendidas para [!DNL Inventory Management]:

- **[!UICONTROL Out-of-Stock Threshold]** - Define um valor para subtrair da Quantidade Venável. Se você ativar Backorders, esse valor não será deduzido da Quantidade Venável.
- **[!UICONTROL Backorders]** - Determina se os produtos podem ser vendidos além de um estoque zero, salvando ordens até serem reabastecidas. Quando ordens pendentes estão habilitadas, é recomendável configurar o [!UICONTROL Out-of-Stock Threshold].

>[!NOTE]
>
>O valor de Limite esgotado suporta valores negativos e positivos. Se você habilitar Backorders, defina esse valor como um valor negativo para o número máximo de produtos que podem ter backorder antes que o produto seja realmente considerado indisponível.

## Demonstração do Inventory management

Assista a este vídeo para saber mais sobre fontes e ações da Inventory management:

>[!VIDEO](https://video.tv.adobe.com/v/343748?quality=12&learn=on)
