---
title: Expandir e reestruturar estoque
description: Saiba como expandir para um comerciante de várias origens ou reduzir para um comerciante de única origem.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Expandir e reestruturar estoque

À medida que sua empresa cresce e muda, o [!DNL Inventory Management] atende às suas necessidades. Você pode expandir para um comerciante de várias origens ou reduzir para um comerciante de uma única origem com facilidade.

## Expandir para várias origens

Os comerciantes de origem única podem adicionar novas lojas, depósitos, drop shippers e muito mais. Expandir requer apenas algumas adições e atualizações de estoque para expandir para multi-sourcing:

1. Adicione [fontes personalizadas](sources-add.md) para cada novo local.

   Você só usa o Source padrão para produtos do pacote.

1. Adicione [estoques personalizados](stocks-add.md) conforme necessário para suas novas fontes.

   Por exemplo, talvez você queira criar estoques por site, país, localidade ou outro método. Você pode atribuir origens aos seus estoques personalizados. Você usa somente o Estoque padrão para produtos do pacote.

1. Atualize [atribuições de origem e quantidades](quantities-manage.md) para seus produtos.

   Você também pode usar a [Ferramenta de Ações em Massa](bulk-assignment.md) e o recurso [Importar-Exportar](inventory-import-export.md) para adicionar rapidamente fontes e dados de produtos.

## Reestruturação para uma única origem

Para comerciantes de várias origens que desejam reduzir as vendas on-line a um local para entrega, modifique as origens, o estoque e as quantidades a serem atualizados:

1. Desabilitar [fontes personalizadas](sources-disable.md).

1. Transfira o inventário do produto para o Source padrão.

   Recomenda-se o uso de ações em massa. Consulte [Transferindo inventário para o Source](inventory-transfer.md).

1. Atribuir todos os sites ao [Estoque Padrão](stocks-manage.md).
