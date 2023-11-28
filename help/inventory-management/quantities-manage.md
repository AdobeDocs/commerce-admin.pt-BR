---
title: Gerenciar quantidades de estoque
description: Saiba como atribuir origens e quantidades para novos produtos ou alterar produtos existentes.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Gerenciar quantidades de estoque

As informações a seguir detalham como atribuir origens e quantidades para novos produtos ou alterar produtos existentes.

Ao criar produtos, atribua origens e quantidades durante a criação do produto. Consulte [Criar um produto](../catalog/product-create.md) para obter instruções completas. Essas páginas incluem informações de origem única e de várias origens para origens e quantidades por origem.

Ao acessar pela primeira vez um [!DNL Commerce] com [!DNL Inventory Management], todos os produtos e quantidades são atribuídos à Origem padrão. Ao importar novos produtos por meio do arquivo .csv, eles também são atribuídos à Origem padrão.

Comerciantes de uma ou várias origens podem atualizar origens, quantidades de inventário e limites por produto ou em massa.

- Os comerciantes de origem única podem atualizar quantidades de produtos para a Origem Padrão. Essa quantidade é o número total de produtos disponíveis para venda.

- Os comerciantes de várias origens podem atribuir várias origens e quantidades por produto para cada local (depósitos, lojas, entregadores diretos e assim por diante). Recomenda-se adicionar origens antes de definir os valores de inventário do produto.

Ao adicionar origens e quantidades aos seus produtos, é possível exibir as quantidades por meio da Grade de Produtos. Se você tiver um número alto de fontes, passe o mouse sobre _[!UICONTROL Quantity per Source]_para ver a lista completa e rolável de origens com quantidades atuais.

![Quantidades de produto por origem](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Você tem as seguintes opções para atribuir inventário a produtos:

- [Atribuindo origens por produto](sources-assign-per-product.md) - Atribua origens manualmente por produto em seu catálogo.

- [Atribuindo Quantidades por Produto](quantities-assign-per-product.md) - Adicione os valores de estoque disponíveis aos seus produtos por origem. Essas informações são específicas para comerciantes de várias origens.

- [Atribuição e cancelamento de atribuição de origens em massa](bulk-assignment.md) - Atribua origens aos produtos selecionados como uma ação em massa. Use o [Transferir Inventário para Origem](inventory-transfer.md) opção se quiser transferir o inventário e remover a origem.

- [Transferindo Inventário para Origem](inventory-transfer.md) - Transfira em massa todo o inventário de uma origem para uma origem de destino.

- [Importando e Exportando Quantidades](inventory-import-export.md) : use os recursos de importação e exportação para atualizar vários SKUs de produtos com origens e quantidades de estoque.
