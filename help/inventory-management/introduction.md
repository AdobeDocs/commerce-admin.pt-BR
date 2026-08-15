---
title: Introdução a  [!DNL Inventory Management]
description: Saiba como usar o [!DNL Inventory Management] for [!DNL Commerce] para gerenciar o estoque entre fontes e estoques, calcular quantidades comercializáveis, rastrear reservas e dar suporte ao atendimento de pedidos. Use o Admin para definir as configurações e gerar relatórios, além da interface de linha de comando para fazer alterações em segundo plano e na configuração.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-git-commit: 125a49f740639bce0ced8063074ca43d627c0eac
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 0%

---

# Introdução ao [!DNL Inventory Management]

O [!DNL Inventory Management] for [!DNL Commerce] ajuda os comerciantes a gerenciar o estoque em um ou mais sites e locais de produtos físicos ou virtuais. Ele fornece ferramentas na interface de linha de comando e administração para configurar o inventário, rastrear quantidades disponíveis e agregadas, proteger o inventário durante a finalização da compra e oferecer suporte ao atendimento de pedidos. Você pode usar [!DNL Inventory Management] para uma única origem ou uma rede de várias origens que inclui depósitos, lojas, locais de retirada, entregadores e outros locais de preenchimento.

## Maneiras de usar [!DNL Inventory Management]

- **Administrador:** Defina as opções de inventário e gere relatórios de inventário.
- **Interface de linha de comando:** Execute comandos de instalação e aplique alterações de inventário em segundo plano.
- **Escopo de configuração:** Defina as configurações de inventário globalmente, por origem ou por produto.

## Principais recursos

[!DNL Inventory Management] recursos incluem:

- Configurações diferentes para comerciantes cujo inventário se origina de uma única origem ou de várias origens
- Estoques para rastrear quantidades comercializáveis agregadas entre fontes atribuídas
- Proteção de check-out simultâneo
- Algoritmos de correspondência de entregas que oferecem suporte a recomendações de atendimento com base na distância ou na prioridade

>[!NOTE]
>
>Esses recursos foram desenvolvidos como parte do projeto [Inventory management](https://github.com/magento/inventory) (antigo MSI) por meio do programa de Engenharia da Comunidade.<br/>
>
>O módulo [!DNL Inventory Management] é instalado com Magento Open Source e Adobe Commerce, com todos os recursos habilitados por padrão. Para obter informações sobre as alterações incluídas nos lançamentos do módulo, consulte as [Notas de versão](release-notes.md).

## Terminologia básica

É importante entender os seguintes termos ao trabalhar com o [!DNL Inventory Management]:

[!UICONTROL Sources] representa locais físicos que armazenam e enviam produtos disponíveis. Consulte [Estoques e fontes](sources-stocks.md) para ver exemplos e diagramas. (Qualquer local pode ser designado como uma origem para produtos virtuais.)

[!UICONTROL Stocks] mapeie um canal de vendas (atualmente limitado a sites) para locais de origem e estoque disponível. Um estoque pode ser mapeado para vários canais de vendas, mas um canal de vendas pode ser atribuído a apenas um estoque.

[!UICONTROL Aggregate Salable Quantity] é o inventário virtual total que pode ser vendido através de um canal de vendas. A quantidade é calculada em todas as fontes atribuídas a um estoque.

[!UICONTROL Reservations] rastreie as deduções da quantidade vendável à medida que os clientes adicionam produtos aos carrinhos e concluem o check-out. Quando uma ordem é entregue, a reserva compensa e deduz as quantias entregues das quantidades de inventário de origem específicas.
