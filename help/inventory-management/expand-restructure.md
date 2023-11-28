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

À medida que sua empresa cresce e muda, [!DNL Inventory Management] O atende às suas necessidades. Você pode expandir para um comerciante de várias origens ou reduzir para um comerciante de uma única origem com facilidade.

## Expandir para várias origens

Os comerciantes de origem única podem adicionar novas lojas, depósitos, drop shippers e muito mais. Expandir requer apenas algumas adições e atualizações de estoque para expandir para multi-sourcing:

1. Adicionar [fontes personalizadas](sources-add.md) para cada novo local.

   Você usa somente a Origem padrão para produtos do Pacote.

1. Adicionar [estoques personalizados](stocks-add.md) conforme necessário para suas novas fontes.

   Por exemplo, talvez você queira criar estoques por site, país, localidade ou outro método. Você pode atribuir origens aos seus estoques personalizados. Você usa somente o Estoque padrão para produtos do pacote.

1. Atualizar [atribuições e quantidades de origem](quantities-manage.md) para seus produtos.

   Você também pode usar a variável [Ferramenta Ações em massa](bulk-assignment.md) e [Importação-Exportação](inventory-import-export.md) para adicionar rapidamente fontes e dados de produtos.

## Reestruturação para uma única origem

Para comerciantes de várias origens que desejam reduzir as vendas on-line a um local para entrega, modifique as origens, o estoque e as quantidades a serem atualizados:

1. Desativar [fontes personalizadas](sources-disable.md).

1. Transfira o estoque do produto para a Origem Padrão.

   Recomenda-se o uso de ações em massa. Consulte [Transferindo Inventário para Origem](inventory-transfer.md).

1. Atribuir todos os sites à [Estoque padrão](stocks-manage.md).
