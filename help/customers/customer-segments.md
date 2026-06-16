---
title: Segmentos de clientes
description: Os segmentos de clientes permitem exibir dinamicamente conteúdo e promoções para clientes específicos.
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
TQID: https://experienceleague.adobe.com/K10qvsYlYebR6fJG8-QNI5qrqwjE-Sn-kSxzfiuoXdo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 0%

---

# Segmentos de clientes

Os segmentos de clientes permitem exibir dinamicamente conteúdo e promoções para clientes específicos, com base em várias propriedades. Alguns exemplos são endereço do cliente, histórico de pedidos e conteúdo do carrinho de compras. Você pode otimizar iniciativas de marketing com base em segmentos direcionados com regras de preço de carrinho de compras. Você também pode gerar relatórios e exportar a lista de clientes direcionados. Como as informações de segmento do cliente são constantemente atualizadas, os clientes podem se tornar associados e desassociados de um segmento à medida que fazem compras em sua loja.

Para entender melhor a diferença entre [grupos de clientes](../customers/customer-groups.md) e segmentos de clientes, observe onde eles são usados:

|  | Segmento do cliente | Grupo de clientes |
|--- |--- |--- |
| Regra de preço de catálogo |  | ✔️ |
| Regra de preço do carrinho | ✔️ | ✔️ |
| Nível de preço |  | ✔️ |
| Regra de produto relacionada | ✔️ |  |
| Bloqueio dinâmico | ✔️ |  |
| Taxas de câmbio de recompensa |  | ✔️ |
| Permissões de categoria |  | ✔️ |
| Convites |  | ✔️ |

{style="table-layout:auto"}

## Atributos de segmento de clientes

Os atributos de segmento dos clientes são definidos de maneira semelhante às regras de preço do carrinho de compras e do catálogo. Para que um atributo seja usado em uma condição de segmento de cliente, a _[!UICONTROL Use in Customer Segment]_[propriedade](attribute-properties.md#) deve ser definida como `Yes`. As condições do segmento do cliente podem incorporar os seguintes tipos de atributos:

| Atributo | Descrição |
|---|---|
| `Customer Address Fields` | Você pode definir qualquer um dos campos de endereço, como cidade ou país. Qualquer endereço no catálogo de endereços de um cliente pode corresponder a essas condições para que o cliente faça a correspondência. Ou você pode especificar que somente os endereços padrão de faturamento ou de envio possam ser usados para corresponder a um cliente. Os atributos de endereço do cliente estão disponíveis somente para clientes que estão conectados às suas contas. |
| `Customer Information Fields` | É possível definir diversas informações do cliente, incluindo Grupo de clientes, nome, email, status de assinatura do boletim informativo e Saldo de crédito da loja. As informações do cliente estão disponíveis somente para clientes que estão conectados às suas contas. |
| `Cart Fields` | As propriedades do carrinho podem ser baseadas na quantidade (itens de linha ou quantidade total) ou no valor (como total geral, imposto e cartão-presente) do conteúdo do carrinho. |
| `Products` | É possível referenciar produtos que estão atualmente no carrinho de compras ou na lista de desejos, ou que foram visualizados ou solicitados anteriormente. Você também pode definir um intervalo de datas no qual ele ocorreu. Os produtos são definidos usando atributos de produto. |
| `Order Fields` | As características de pedidos de pedidos anteriores podem ser definidas com base no endereço de faturamento/entrega do pedido, no valor ou quantidade total (ou média) dos pedidos ou no número total de pedidos. Você também pode definir um intervalo de datas para quando ele ocorreu e o status do pedido dos pedidos que correspondem a essas condições. Disponível somente para clientes que estão conectados. As condições definidas para compradores que não estão conectados param de funcionar quando eles fazem logon. |

{style="table-layout:auto"}

Consulte [Criar e excluir segmentos de clientes](../customers/customer-segment-create.md) para obter mais informações sobre como definir segmentos de clientes.

## eBooks

- **Segmentação de clientes** — Obtenha o [eBook](https://business.adobe.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html) para saber como aumentar os lucros e a satisfação geral do cliente.
- **Táticas de segmentação** — Use o [eBook](https://business.adobe.com/resources/3-segmentation-tactics-ignite-conversion.html) para melhorar o direcionamento de suas mensagens e promoções e criar conversas significativas com seus clientes.
