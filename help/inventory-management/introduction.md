---
title: Introdução ao Inventory management
description: Saiba como usar  [!DNL Inventory Management]  recursos para gerenciar estoque em vários locais para que seu  [!DNL Commerce] armazenamento reflita com precisão o estoque físico.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 364
ht-degree: 0%

---

# Introdução ao Inventory management

O [!DNL Inventory Management] for [!DNL Commerce] fornece as ferramentas para gerenciar o inventário de produtos. Comerciantes com uma única loja para vários depósitos, lojas, locais de retirada, entregadores diretos e muito mais podem usar esses recursos para manter quantidades para vendas e controlar entregas para ordens completas. Você pode rastrear as quantidades de seu inventário, fornecer quantidades precisas de estoque comercializável aos clientes para todos os seus sites e entregar de acordo com as recomendações com base na distância ou na prioridade. Você também pode definir as configurações de produto de sua preferência globalmente (para todas as lojas e produtos), por origem e por produto. Esses recursos crescem com a sua empresa, permitindo que você trabalhe a partir de um único warehouse ou de uma rede de envio complexa com algumas configurações adicionais.

[!DNL Inventory Management] recursos incluem:

- Configurações diferentes para comerciantes cujo inventário se origina de uma única origem e de várias origens
- Estoques para rastrear quantidades agregadas disponíveis por meio de fontes atribuídas
- Proteção de check-out simultâneo
- Algoritmos de correspondência de entregas

>[!NOTE]
>
>Esses recursos foram desenvolvidos como parte do projeto [Inventory management](https://github.com/magento/inventory) (antigo MSI) por meio do programa de Engenharia da Comunidade.<br/>
>
>O módulo [!DNL Inventory Management] é instalado com Magento Open Source e Adobe Commerce, com todos os recursos habilitados por padrão. Para obter informações sobre as alterações incluídas nos lançamentos do módulo, consulte as [Notas de versão](release-notes.md).

## Terminologia básica

É importante entender os seguintes termos ao trabalhar com o [!DNL Inventory Management]:

[!UICONTROL **Fontes**] representam locais físicos que armazenam e enviam produtos disponíveis. Esses locais podem incluir depósitos, lojas tradicionais, centros de distribuição e carregadores. (Qualquer local pode ser designado como uma origem para produtos virtuais.)

[!UICONTROL **Estoques**] mapear um canal de vendas (atualmente limitado a sites) para locais de origem e estoque disponível. Um estoque pode ser mapeado para vários canais de vendas, mas um canal de vendas pode ser atribuído a apenas um estoque.

[!UICONTROL **Quantidade de Venda Agregada**] é o estoque virtual total que pode ser vendido por meio de um canal de vendas. A quantidade é calculada em todas as fontes atribuídas a um estoque.

[!UICONTROL **As reservas**] rastreiam as deduções da quantidade comercializável à medida que os clientes adicionam produtos aos carrinhos e concluem o check-out. Quando uma ordem é entregue, a reserva compensa e deduz as quantias entregues das quantidades de inventário de origem específicas.
