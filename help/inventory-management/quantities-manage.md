---
title: Gerenciar quantidades de estoque
description: Saiba como atribuir origens e quantidades para novos produtos ou alterar produtos existentes.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/ykiHTLnzZGtJrRdp2wZvlL7YLbEb7iAiYlcbY8K7IX8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 325
ht-degree: 0%

---

# Gerenciar quantidades de estoque

As informações a seguir detalham como atribuir origens e quantidades para novos produtos ou alterar produtos existentes.

Ao criar produtos, atribua origens e quantidades durante a criação do produto. Consulte [Criar um produto](../catalog/product-create.md) para obter instruções completas. Essas páginas incluem informações de origem única e de várias origens para origens e quantidades por origem.

Ao acessar pela primeira vez um [!DNL Commerce] atualizado com [!DNL Inventory Management], todos os produtos e quantidades são atribuídos ao Source Padrão. Ao importar novos produtos por meio do arquivo .csv, eles também são atribuídos ao Source padrão.

Comerciantes de uma ou várias origens podem atualizar origens, quantidades de inventário e limites por produto ou em massa.

- Os comerciantes de origem única podem atualizar quantidades de produtos para o Source Padrão. Essa quantidade é o número total de produtos disponíveis para venda.

- Os comerciantes de várias origens podem atribuir várias origens e quantidades por produto para cada local (depósitos, lojas, entregadores diretos e assim por diante). Recomenda-se adicionar origens antes de definir os valores de inventário do produto.

Ao adicionar origens e quantidades aos seus produtos, é possível exibir as quantidades por meio da Grade de Produtos. Se você tiver um número alto de origens, passe o mouse sobre _[!UICONTROL Quantity per Source]_&#x200B;para ver a lista completa e rolável de origens com quantidades atuais.

![Quantidades de produto por origem](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Você tem as seguintes opções para atribuir inventário a produtos:

- [Atribuindo origens por produto](sources-assign-per-product.md) - Atribua origens manualmente por produto no catálogo.

- [Atribuindo Quantidades por Produto](quantities-assign-per-product.md) - Adicione os valores de estoque disponíveis aos seus produtos por origem. Essas informações são específicas para comerciantes de várias origens.

- [Atribuição e cancelamento de atribuições em massa de origens](bulk-assignment.md) - Atribua origens a produtos selecionados como uma ação em massa. Use a opção [Transferir inventário para o Source](inventory-transfer.md) se desejar transferir o inventário e remover a origem.

- [Transferindo o Estoque para o Source](inventory-transfer.md) - Transfira em massa todo o estoque de uma origem para uma origem de destino.

- [Importando e Exportando Quantidades](inventory-import-export.md) - Use recursos de importação e exportação para atualizar várias SKUs de produtos com origens e quantidades de estoque.
