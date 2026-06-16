---
title: Cenários de mensagem de estoque
description: Saiba mais sobre a combinação de definições de configuração que controlam as mensagens de disponibilidade de estoque nas páginas de produtos e nas listas de produtos nas páginas de catálogo.
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/9kPHtr75C7PkM9vD-2-AeG8JnAfKAao0GKEH9MhkBbU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 1%

---

# Cenários de mensagem de estoque

Você pode usar uma combinação de definições de configuração para controlar as mensagens de disponibilidade de estoque nas páginas de produtos e nas listagens de produtos nas páginas de catálogo.

![Produto agrupado com a mensagem &quot;Em falta&quot;](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## Mensagens de estoque de página do produto

Há várias variações de mensagens disponíveis para a página do produto, dependendo da combinação das configurações Gerenciar estoque e Disponibilidade do estoque.

### Exemplo 1: mostrar mensagem de disponibilidade

#### Cenário 1

Essa combinação de configurações faz com que a mensagem de disponibilidade apareça na página do produto, de acordo com a disponibilidade de estoque de cada produto.

| Opções de estoque | Configuração | Mensagem |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### Cenário 2

Quando o estoque não é gerenciado para um produto, essa combinação de configurações pode ser usada para exibir a mensagem de disponibilidade na página do produto.

| Opções de estoque | Configuração | Mensagem |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### Exemplo 2: ocultar mensagem de disponibilidade

#### Cenário 1

Essa combinação de configurações e definições de produto impede que a mensagem de disponibilidade apareça na página do produto.

| Opções de estoque | Configuração | Mensagem |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | Nenhum |
|  | `Out of Stock` | Nenhum |

#### Cenário 2

Quando o estoque não é gerenciado para um produto, essa combinação de configurações e definições do produto impede que a mensagem de disponibilidade apareça na página do produto.

| Opções de estoque | Configuração | Mensagem |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | Nenhum |

## Mensagens de estoque de página de catálogo

As seguintes opções de exibição são possíveis para a categoria e as listas de resultados da pesquisa, dependendo da disponibilidade do produto e das definições de configuração.

![Mensagem de Indisponibilidade na Página de Categoria](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

### Exemplo 1: mostrar produto com a mensagem &quot;Produto esgotado&quot;

Essa combinação de definições de configuração inclui produtos indisponíveis na categoria e nas listas de resultados de pesquisa, e exibe uma mensagem de &quot;indisponível&quot;.

| Opções de estoque | Configuração | Mensagem |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | Nenhum |

### Exemplo 2: mostrar produto sem mensagem &quot;esgotado&quot;

Essa combinação de definições de configuração inclui produtos indisponíveis na categoria e nas listas de resultados de pesquisa, mas não exibe uma mensagem.

| Opções de estoque | Configuração | Mensagem |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | Nenhum |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### Exemplo 3: ocultar o produto até que ele esteja novamente em estoque

Essa configuração omite totalmente os produtos indisponíveis da categoria e das listas de resultados de pesquisa até que estejam de volta ao estoque.

| Opções de estoque | Configuração | Mensagem |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | Nenhum |
