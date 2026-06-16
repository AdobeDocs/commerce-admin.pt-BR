---
title: Expandir e reestruturar estoque
description: Saiba como expandir para um comerciante de várias origens ou reduzir para um comerciante de única origem.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/w4TV-BQrg0RzlHn4DVSdHFPD2M5CF11wA7I5OyA7jsY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 219
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
