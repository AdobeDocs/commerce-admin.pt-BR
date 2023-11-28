---
title: Gerenciar fontes de inventário
description: Saiba mais sobre as origens e como elas definem os locais físicos onde o inventário de produtos é gerenciado e enviado para o atendimento de pedidos ou onde os serviços estão disponíveis.
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Gerenciar fontes

As origens são os locais físicos onde o inventário de produtos é gerenciado e entregue para atendimento de pedidos ou onde os serviços estão disponíveis. Esses locais podem incluir depósitos, lojas tradicionais, centros de distribuição, locais de coleta e entregadores. Você aloca quantidades de inventário para essas origens e [!DNL Commerce] O agrega automaticamente o total de produtos comercializáveis para seus estoques. Para grandes empresas, adicione várias fontes para todos os seus locais: em diferentes localizações geográficas por país e continente, localizações em uma cidade, com base no tipo de inventário, até mesmo com base em serviços.

É recomendável fornecer localizações geográficas físicas específicas ao criar uma origem. Isso permite que o _Algoritmo de prioridade de distância_ para comparar o local do endereço de destino da entrega com os locais de origem disponíveis para determinar a origem mais próxima para atender às entregas. Você pode usar o Google Maps ou cálculos offline, que usam geocódigos. Para obter mais informações sobre este _Algoritmo de prioridade de distância_, consulte [Configurar Algoritmo de Prioridade de Distância](distance-priority-algorithm.md).

Comece com um _Origem padrão_ que você pode atualizar, mas não desativar. Essa origem é usada por comerciantes de origem única e para migração de produtos. Você sempre precisa de uma origem padrão.

- **Informações do local** - Cada fonte inclui o nome, país, endereço físico do local e um ponto de contato.
- **Ativando recursos** - Você pode ativar e desativar origens conforme necessário. Ative uma origem somente se ela aceitar e atender pedidos e backorders.
- **Inventário Disponível** - Atribuir e atualizar quantidades de estoque para cada origem por meio da página do produto. As quantidades de inventário são calculadas, fornecidas e reservadas por meio do mapeamento de origem e estoque.

O diagrama a seguir ajuda a ilustrar as Origens de um comerciante da Loja de Bicicletas que vende uma mountain bike, disponível para estoques e acessível pela SSA para remessas.

![Exemplo de diagrama de fontes](assets/diagram-sources.png){width="600" zoomable="yes"}

Todos os armazenamentos começam com uma Origem padrão que deve permanecer ativada:

- Todos os novos produtos importados para o [!DNL Commerce] exigir uma origem e um estoque, atribuídos automaticamente para acesso imediato a [!DNL Inventory Management].
- Os comerciantes de origem única usam a Origem Padrão como seu ponto único de localização de inventário e entregas.

## Editar fontes

Você pode atualizar o nome, o endereço, a localização no GPS e as informações do ponto de contato. O código-fonte é um valor protegido, atuando como uma ID exclusiva que associa a fonte às quantidades e estoques do seu produto.

Se estiver editando a Origem padrão, você poderá editar todas as configurações, exceto o nome e o código. Recomenda-se que os comerciantes de origem única adicionem informações correspondentes à sua localização.

A variável _[!UICONTROL Manage Sources]_A página lista todos os locais de inventário e instalações de preenchimento disponíveis. Você pode adicionar novas origens de inventário e editar locais existentes.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Para adicionar um local de inventário, consulte [Adicionar uma nova fonte](sources-add.md).

1. Localizar a origem do estoque e abri-la em _Editar_ modo.

1. Atualize as informações e salve as alterações.

   ![Gerenciar fontes](assets/inventory-sources.png){width="600" zoomable="yes"}

## Barra de botões

| Botão | Descrição |
|--|--|
| [!UICONTROL Add New Source] | Abre o formulário Nova Origem que é usado para inserir uma nova origem de estoque, instalação de preenchimento ou local. |

## Gerenciar descrições de colunas de origens

| Coluna | Descrição |
|--|--|
| [!UICONTROL Code] | Um código alfanumérico exclusivo que é usado pelo sistema para identificar a origem do inventário. |
| [!UICONTROL Name] | Um nome exclusivo que identifica a origem do inventário para usuários administradores. |
| [!UICONTROL Is Enabled] | Indica se a origem do inventário está ativa e disponível para uso. |
| [!UICONTROL Pickup Location] | Indica se a origem está ativa como uma localização de retirada para [entrega na loja](../stores-purchase/shipping-in-store-delivery.md). |
| [!UICONTROL Action] | Clicando **[!UICONTROL Edit]** abre o registro de origem do estoque no modo de edição. |

## Outras colunas

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Latitude] | Especifica a coordenada de latitude da fonte de inventário para GPS. Insira o valor como um número, precedido por um sinal de mais ou menos, conforme necessário. O símbolo de grau e as letras não são permitidos. Por exemplo: `32.7555` |
| [!UICONTROL State/Province] | O estado ou província onde a origem está localizada. |
| [!UICONTROL Postcode] | O CEP da origem. |
| [!UICONTROL Email] | O email do contato principal. |
| [!UICONTROL Longitude] | Especifica a coordenada de longitude da fonte de inventário para GPS. Insira o valor como um número, precedido por um sinal de mais ou menos, conforme necessário. O símbolo de grau e as letras não são permitidos. Por exemplo: Longitude -97.3308 |
| [!UICONTROL City] | A cidade onde a fonte está localizada. |
| [!UICONTROL Phone] | O número de telefone do contato principal. |
| [!UICONTROL Country] | O país onde a origem está localizada. |
| [!UICONTROL Street] | O endereço da origem. |
| [!UICONTROL Fax] | O código de área e o número de fax do contato principal. |
