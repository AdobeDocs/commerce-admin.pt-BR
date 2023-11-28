---
title: Introdução ao Inventory management
description: Saiba como usar o [!DNL Inventory Management] recursos para gerenciar o estoque em vários locais, de modo que seus [!DNL Commerce] o armazenamento reflete com precisão o estoque físico.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Introdução ao Inventory management

[!DNL Inventory Management] para [!DNL Commerce] O fornece as ferramentas para gerenciar o inventário de produtos. Comerciantes com uma única loja para vários depósitos, lojas, locais de retirada, entregadores diretos e muito mais podem usar esses recursos para manter quantidades para vendas e controlar entregas para ordens completas. Você pode rastrear as quantidades de seu inventário, fornecer quantidades precisas de estoque comercializável aos clientes para todos os seus sites e entregar de acordo com as recomendações com base na distância ou na prioridade. Você também pode definir as configurações de produto de sua preferência globalmente (para todas as lojas e produtos), por origem e por produto. Esses recursos crescem com a sua empresa, permitindo que você trabalhe a partir de um único warehouse ou de uma rede de envio complexa com algumas configurações adicionais.

[!DNL Inventory Management] os recursos incluem:

- Configurações diferentes para comerciantes cujo inventário se origina de uma única origem e de várias origens
- Estoques para rastrear quantidades agregadas disponíveis por meio de fontes atribuídas
- Proteção de check-out simultâneo
- Algoritmos de correspondência de entregas

>[!NOTE]
>
>Esses recursos foram desenvolvidos como parte da [Inventory management](https://github.com/magento/inventory) (anteriormente MSI) através do programa comunitário de engenharia.<br/>
>
>A variável [!DNL Inventory Management] O módulo é instalado com o Magento Open Source e o Adobe Commerce, com todos os recursos ativados por padrão. Para obter informações sobre as alterações incluídas nas versões dos módulos, consulte a [Notas de versão](release-notes.md).

## Terminologia básica

É importante entender os termos a seguir ao trabalhar com o [!DNL Inventory Management]:

[!UICONTROL **Origens**] representam locais físicos que armazenam e enviam produtos disponíveis. Esses locais podem incluir depósitos, lojas tradicionais, centros de distribuição e carregadores. (Qualquer local pode ser designado como uma origem para produtos virtuais.)

[!UICONTROL **Estoques**] mapear um canal de vendas (atualmente limitado a sites) para locais de origem e estoque disponível. Um estoque pode ser mapeado para vários canais de vendas, mas um canal de vendas pode ser atribuído a apenas um estoque.

[!UICONTROL **Quantidade Agregável**] é o inventário virtual total que pode ser vendido por meio de um canal de vendas. A quantidade é calculada em todas as fontes atribuídas a um estoque.

[!UICONTROL **Reservas**] rastreie as deduções da quantidade vendável à medida que os clientes adicionam produtos aos carrinhos e concluem o check-out. Quando uma ordem é entregue, a reserva compensa e deduz as quantias entregues das quantidades de inventário de origem específicas.
