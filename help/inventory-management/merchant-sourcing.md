---
title: Tipos de fornecimento de comerciante
description: Compare os modos de comerciante de origem única e de várias origens para escolher como você atribui origens, estoques e quantidades em [!DNL Inventory Management].
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/-ABDMLnAibksuQGkdEM683g8JwcUSt2DQERC0WJnQiM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%
---
# Tipos de fornecimento de comerciante

O [!DNL Commerce] oferece suporte ao [!DNL Inventory Management] para empresas de todos os tamanhos, incluindo uma única loja com um site para uma rede internacional de sites, lojas, depósitos e entregadores. Todos os comerciantes que usam o Adobe Commerce ou o Magento Open Source se dividem em dois tipos com base no número de locais ou origens na sua empresa.

- Os comerciantes de origem única entregam os produtos de um local. Você é considerado um comerciante/modo de origem única até começar a adicionar fontes e estoques personalizados à sua instalação.

- Mercadores de várias origens entregam produtos de mais de um local, como lojas tradicionais, depósitos, entregadores e centros de distribuição. Depois de adicionar origens personalizadas por local, você se torna automaticamente um comerciante de várias origens.

## Comerciantes de origem única

Os comerciantes de origem única têm um único local que gerencia o estoque disponível e atende aos pedidos. Normalmente, você tem vários sites (ou canais de vendas) vendendo produtos do mesmo catálogo, inventário e local.

Por exemplo, você tem um site ou uma implementação de vários sites com sites dos Estados Unidos, Alemanha, França e Brasil, todos extraindo produtos de um grande depósito. Essa única origem gerencia todas as quantidades de inventário, remessas e devoluções, independentemente de qual canal de vendas recebe a ordem.

Para começar:

- Defina as [configurações globais e de produto](configuration.md) para o inventário da sua loja, conforme necessário.

- Atualize o [Source Padrão](sources-manage.md) com informações sobre seu único local de inventário. Não é necessário criar fontes adicionais.

- Atualize o [Estoque Padrão](stocks-manage.md). Certifique-se de que todos os sites estejam selecionados como canais de vendas. À medida que você adiciona novos sites, o [!DNL Commerce] os adiciona automaticamente ao Estoque Padrão. Não é necessário criar estoques adicionais.

>[!NOTE]
>
>À medida que sua empresa se expande, adicione mais fontes e estoques e atualize sua configuração do [!DNL Inventory Management] para se tornar um comerciante de várias fontes. Consulte [Expandir e Reestruturar o Inventário](expand-restructure.md) para obter todos os detalhes.

## Comerciantes de várias origens

Comerciantes de várias origens têm um site ou uma implementação de vários sites e gerenciam o inventário em estoque e realizam pedidos por meio de vários locais.

Por exemplo, você tem uma implementação de vários sites com sites dos Estados Unidos, Alemanha, França e Brasil. Sua empresa inclui vários depósitos e lojas nesses países e serviços de entrega direta que gerenciam todo o estoque de estoque e atendem a pedidos. Esses locais e sites se tornam fontes e estoques em [!DNL Commerce]. Você pode criar um estoque para as Américas e outro para a Europa, atribuindo sites e fontes com base em localidades e locais. Os clientes que compram cada site só têm acesso a inventários comercializáveis das fontes atribuídas.

Para começar:

- Defina as configurações globais para o inventário da sua loja, conforme necessário.

- Adicione [fontes personalizadas](sources-add.md) para seus locais de estoque: depósitos, lojas, centros de distribuição e entregadores.

- Adicione [estoques personalizados](stocks-add.md) para cada região para mapear seus sites com várias fontes. Reordene as fontes em cada estoque em prioridade de localização, útil ao atender seus pedidos.

- Atribuir origens aos produtos, adicionando quantidades por localização.

- Conclua quaisquer configurações adicionais por produto para limites de quantidade, backorders e assim por diante.
