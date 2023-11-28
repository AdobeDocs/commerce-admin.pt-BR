---
title: Gerenciar ordens e remessas do estoque
description: Saiba mais sobre os [!DNL Inventory Management] recursos e opções para gerenciar quantidades de inventário por meio do processo de entrega.
exl-id: cc4ca518-d98c-48f3-9051-6fb3c6fae9fe
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 0%

---

# Gerenciar pedidos e remessas

[!DNL Inventory Management] inclui recursos e opções adicionais para gerenciar quantidades de inventário por meio do processo de entrega. À medida que você revisa e preenche entregas, cancela ordens e emite avisos de crédito, as quantidades do produto comercializável e em estoque são atualizadas automaticamente.

Essas informações incluem informações específicas para [!DNL Inventory Management]. Para obter informações adicionais, consulte a seção [Pedidos](../stores-purchase/orders.md){target="_blank"} tópico no _Guia de experiência de vendas e compras_.

## Pedidos

[!DNL Commerce] O oferece suporte a pedidos únicos e pedidos com vários endereços prontos para uso, sem configurações adicionais. À medida que os clientes ou a equipe inserem pedidos, [!DNL Inventory Management] rastreia o inventário usando reservas em relação à quantidade vendável, deduzindo da quantidade em estoque os produtos faturados e entregues.

### Pedidos de vários endereços

Para pedidos com vários endereços, uma série de pedidos únicos é gerada — um para cada endereço de destino inserido. Durante o checkout, os clientes selecionam cada conjunto de produtos associados por endereço durante o checkout, que é gerado como pedidos únicos de acordo com o endereço de destino. Cada pedido inclui os produtos associados por endereço.

[!DNL Commerce] gerencia o estoque para esses pedidos de vários endereços exatamente como pedidos únicos. Permite recomendações ou sobreposições do Algoritmo de seleção de origem durante a entrega, entregas parciais, cancelamento de pedidos e reembolso com atualizações de estoque.

![Vários endereços no check-out](assets/inventory-multi-ship.png){width="350" zoomable="yes"}

### Reembolsos

Ao inserir um [memorando de crédito](../stores-purchase/credit-memo-create.md){target="_blank"} para emitir um reembolso, é possível retornar a quantidade do produto para a fonte deduzida. As informações da ordem incluem a origem do estoque que entregou o produto. É recomendável premiar a quantidade do produto devolvido por meio de um aviso de crédito ao receber o produto devolvido.

![Itens para Reembolso com Devolução ao Estoque Selecionado](assets/credit-memo-items-to-refund.png)
{width="350" zoomable="yes"}

### Cancelar ordens não entregues

Se uma ordem não tiver sido entregue e for cancelada (total ou parcialmente), [!DNL Inventory Management] retorna automaticamente o estoque do produto à quantidade vendável. Até a fatura e a remessa, os produtos comprados são reservados contra a quantidade vendável, não deduzidos da quantidade real. No ponto de faturamento e entrega da ordem, o sistema converte a reserva em uma dedução de inventário.

Nos bastidores, [!DNL Inventory Management] insere automaticamente uma reserva de remuneração removendo a retenção na quantidade do produto. A quantidade retorna para a quantidade vendida virtual agregada.

## Entregas

Com [!DNL Inventory Management] ativado, você pode enviar entregas parciais ou completas de uma ou mais origens para preencher ordens. Você controla o inventário de saída para cada ordem, definindo as quantias a serem deduzidas, enviando uma ou mais entregas e distribuindo em estoque e backorders, à medida que o inventário estiver disponível. Para cada item de linha na ordem, insira uma quantia a ser deduzida da quantidade de origem. Gere uma entrega por origem à medida que tiver estoque de estoque, até que toda a ordem seja atendida.

### Remessas parciais

Para comerciantes de várias origens, [!DNL Commerce] gera uma entrega para cada origem selecionada. O workflow geral permite selecionar uma origem, definir a quantidade de produtos a ser deduzida para atender à ordem e prosseguir para a entrega. Quando terminar, crie entregas adicionais para cada origem até que você tenha preenchido a ordem.

Os comerciantes de origem única também podem enviar entregas parciais para suportar backorders ou balancear o inventário à medida que as ordens chegam para itens populares.

### Recommendations e algoritmo de seleção de origem

A variável [Algoritmo de seleção de origem](selection-reservations.md) (SSA) fornece recomendações para entregas parciais e completas. Você pode acessar os Algoritmos de Seleção de Origem ao criar NFFs de entrega para uma ordem. Na página Entrega, execute o algoritmo Prioridade de Origem ou Prioridade de Distância a qualquer momento para determinar as melhores opções para vincular quantidades solicitadas e origens disponíveis. O sistema oferece suporte à entrega de uma ordem completa a partir de uma origem e à divisão da ordem em várias entregas parciais em várias origens. Você pode acessar essas opções para preenchimento imediato e entregas escalonadas para enviar quantias menores ao longo do tempo.

Para concluir e entregar um pedido, ele deve ter concluído o pagamento e ser faturado. Atualmente, você pode executar novamente o SSA para recomendações e entregar a partir de uma ou mais origens ou sobrepor as recomendações do SSA com origens e quantidades definidas manualmente para preencher a entrega.

- É recomendável executar novamente o SSA para revisar as recomendações para cada entrega.

- Se quiser alterar as seleções, você poderá sobrepor com deduções manuais de origem.

### Remessas e reservas

À medida que as entregas são geradas, as reservas de produtos são liberadas e a quantidade do produto é deduzida. A quantidade disponível por estoque é atualizada com base nos detalhes da remessa. Por exemplo, se você enviar entregas para dez produtos de duas origens, as quantidades dessas origens deduzirão 10 cada. A Quantidade Venável é atualizada automaticamente para estoques associados, fornecendo aos clientes e à equipe as quantidades de produto mais recentes. E as reservas são completamente limpas, não contando mais com a Quantidade Venável.
