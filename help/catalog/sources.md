---
title: Configurações do produto - [!UICONTROL Sources]
description: Para um produto, as configurações do [!UICONTROL Sources] fornecem acesso às [!DNL Inventory Management] fontes das quais o produto pode ser distribuído.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
TQID: 'https://experienceleague.adobe.com/7LFF4ufXyKtJwUp4DiNDdnRMhFRsM1tX8Z2TlPt1Kso'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%
---
# Configurações do produto - [!UICONTROL Sources]

A seção _[!UICONTROL Sources]_&#x200B;das configurações do produto lista as fontes das quais o produto pode ser distribuído. É usado para atribuir e desatribuir origens, bem como gerenciar a quantidade e a disponibilidade do produto. Esta seção será exibida somente se houver mais de uma origem definida para o armazenamento. Para obter mais informações sobre fontes, consulte [Gerenciar fontes](../inventory-management/sources-manage.md).

## Atribuir uma origem a um produto

1. Clique em **[!UICONTROL Assign Source]**.

1. Marque a caixa de seleção das fontes necessárias.

1. Clique em **[!UICONTROL Done]**.

1. Selecione **[!UICONTROL Source Item Status]** e insira os valores de **[!UICONTROL Qty]** e **[!UICONTROL Notify Qty]**, conforme necessário.

1. Clique em **[!UICONTROL Save]** para salvar as alterações.

![Exibição das fontes](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Referência do campo

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Name] | O nome exclusivo de uma origem. |
| [!UICONTROL Source Status] | Determina se o produto está ativado ou desativado no catálogo. |
| [!UICONTROL Source Item Status] | Determina a disponibilidade atual do produto. Opções:<br />**[!UICONTROL In Stock]**- Disponibiliza o produto para compra.<br />**[!UICONTROL Out of Stock]** - A menos que os pedidos pendentes sejam ativados, impede que o produto esteja disponível para compra e remove a listagem do catálogo. |
| [!UICONTROL Qty] | Valores de estoque disponível para cada origem. |
| [!UICONTROL Notify Qty] | Um valor para a _Notificar para Quantidade_ para esta origem específica se `Notify Quantity Use Default` não estiver selecionado. |
| [!UICONTROL Notify Qty Use Default] | Indica o uso da configuração padrão para _Notificar para Quantidade_ no inventário avançado do produto ou configuração global na configuração da loja. Para obter mais informações sobre configurações avançadas de inventário para o seu produto, consulte [Configurar opções avançadas do produto](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Para uma origem atribuída, clique em **[!UICONTROL Unassign]** para tornar a origem não disponível para o produto. Para uma origem não atribuída, clique em **[!UICONTROL Assign Sources]** para disponibilizar uma origem para o produto. Para obter mais informações sobre as opções de [!UICONTROL Assign Sources], consulte [Atribuindo origens por produto](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}

