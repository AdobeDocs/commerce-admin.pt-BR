---
title: Configurações do produto - [!UICONTROL Product Reviews]
description: Para um produto, as configurações de [!UICONTROL Product Reviews] fornecem acesso às revisões enviadas para o produto e editam o status das revisões pendentes.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/GdeAB8bT8WjR9vSGjuD-h5I3O6vYNxyaaUQYAjjy8ME
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
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
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Configurações do produto - [!UICONTROL Product Reviews]

A seção _[!UICONTROL Product Reviews]_&#x200B;lista todas as análises que os clientes enviaram sobre o produto. Esta seção é exibida com as outras informações do produto somente depois que um novo produto é salvo pela primeira vez. Para obter mais informações, consulte [Avaliações do Produto](../merchandising-promotions/product-reviews.md).

![Avaliações do Produto](./assets/product-review.png){width="600" zoomable="yes"}

## Referência do campo

| Campo | Descrição |
|--- |--- |
| [!UICONTROL ID] | ID numérica exclusiva gerada para a entrada de revisão do produto |
| [!UICONTROL Created] | Data de publicação da revisão |
| [!UICONTROL Status] | Status da revisão (`Pending`, `Approved` ou `Not Approved`) |
| [!UICONTROL Title] | Revisar título |
| [!UICONTROL Nickname] | O apelido do usuário que deixou a revisão |
| [!UICONTROL Review] | Análise do cliente sobre o produto atual |
| [!UICONTROL Visibility] | Visibilidade em revisões da loja |
| [!UICONTROL Type] | Tipo de usuário que deixou a revisão (`Guest` ou `Customer`) |
| [!UICONTROL Product] | Nome do produto revisado |
| [!UICONTROL SKU] | A Unidade de Manutenção de Estoque exclusiva atribuída ao produto |
| [!UICONTROL Action] | Abre o produto no modo de edição |

{style="table-layout:auto"}

## Avaliações moderadas de um produto específico

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Localize o produto e abra-o no modo de edição.

1. Role até a seção _[!UICONTROL Product Reviews]_.

1. Clique em **[!UICONTROL Edit]** para uma análise de produto com status `Pending` para exibir e editar os detalhes.

1. Definir status para revisão:

   - Para aprovar uma revisão pendente, selecione `Approved`.
   - Para rejeitar uma revisão, selecione `Not Approved`.
   - Você pode alterar o status da revisão para `Pending` a qualquer momento.

1. Quando terminar, clique em **[!UICONTROL Save Review]**.

Revisões com os status `Pending` e `Not Approved` não são exibidas na loja.

