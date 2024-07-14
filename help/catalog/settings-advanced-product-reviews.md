---
title: Configurações do produto - [!UICONTROL Product Reviews]
description: Para um produto, as configurações de [!UICONTROL Product Reviews] fornecem acesso às revisões enviadas para o produto e editam o status das revisões pendentes.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Configurações do produto - [!UICONTROL Product Reviews]

A seção _[!UICONTROL Product Reviews]_lista todas as análises que os clientes enviaram sobre o produto. Esta seção é exibida com as outras informações do produto somente depois que um novo produto é salvo pela primeira vez. Para obter mais informações, consulte [Avaliações do Produto](../merchandising-promotions/product-reviews.md).

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
