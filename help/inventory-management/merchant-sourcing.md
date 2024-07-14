---
title: Tipos de fornecimento de comerciante
description: Saiba mais sobre os dois tipos de seleção de fornecedor com base no número de locais, ou origens, em sua empresa.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Tipos de fornecimento de comerciante

O [!DNL Commerce] oferece suporte ao [!DNL Inventory Management] para empresas de todos os tamanhos, incluindo uma única loja com um site para uma rede internacional de sites, lojas, depósitos e entregadores. Todos os comerciantes que usam Adobe Commerce ou Magento Open Source se dividem em dois tipos com base no número de locais, ou origens, em sua empresa.

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
