---
title: Adicionar uma origem de inventário
description: Saiba como criar uma origem para um local, como um depósito, uma loja física, um centro de distribuição ou um entregador.
exl-id: 1bff9986-8722-4fb5-ac83-41de82325f7b
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Adicionar uma origem

Gerencie o inventário e o atendimento de pedidos de vários locais com origens personalizadas. Crie uma origem para cada local, como depósitos, lojas tradicionais, centros de distribuição e entregadores. Atribuir origens e atualizar quantidades por produto

Se estiver editando a Origem padrão, você poderá editar todas as configurações, exceto o nome e o código. Recomenda-se que os comerciantes de origem única adicionem informações correspondentes à sua localização.

## Adicionar uma origem de inventário

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Clique em **[!UICONTROL Add New Source]**.

   ![Gerenciar fontes](assets/inventory-sources.png)

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL General]** e faça o seguinte:

   - Para identificar a origem do inventário, informe uma **[!UICONTROL Name]**.

   - Insira um único **[!UICONTROL Code]**.

     O código oferece suporte a letras maiúsculas e minúsculas, números, traços e sublinhados. O código é um identificador exclusivo usado ao atribuir para dados de estoque e importação/exportação.

   - Se esta origem de inventário estiver pronta para uso, defina **[!UICONTROL Is Enabled]** para `Yes`.

   - Insira um resumo **[!UICONTROL Description]** para obter este local para referência rápida ou detalhes adicionais.

   - Para **[!UICONTROL Latitude]** e **[!UICONTROL Longitude]**, insira as coordenadas do GPS (Global Positioning System) da localização da instalação.

     Para encontrar as coordenadas do GPS com [Google Maps][1], digite o endereço na caixa de pesquisa. Clique com o botão direito do mouse no marcador no mapa e escolha **[!UICONTROL What's here?]**. As coordenadas do GPS aparecem na caixa de detalhes abaixo do endereço da rua.

     ![Opções gerais de origem](assets/inventory-source-general.png)

   - Se esta origem de estoque for um local de retirada, defina **[!UICONTROL Use as Pickup Location]** para `Yes`.

     A Origem Padrão não pode ser usada como um local de retirada para ordens de retirada na loja.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Contact Info]** e faça o seguinte:

   - Para **[!UICONTROL Contact Name]**, digite o nome completo do contato principal no local.

   - Insira um **[!UICONTROL Email]** endereço para entrar em contato com a localização.

   - Para **[!UICONTROL Phone]**, insira o código de área e o número de telefone.

   - Para **[!UICONTROL Fax]**, digite o código de área e o número de telefone do fax, se disponível.

     ![Informações de contato](assets/inventory-source-contact-info.png)

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Address Data]** e faça o seguinte:

   - Escolha o **[!UICONTROL Country]**.

   - Para **[!UICONTROL State/Province]**, insira a abreviação padrão do estado ou província.

   - Insira o **[!UICONTROL City]**.

   - Insira o físico **[!UICONTROL Street]** endereço.

   - Para **[!UICONTROL Postcode]**, digite o CEP ou código postal.

     ![Dados do endereço](assets/inventory-source-address.png)

1. Se você definir a origem como um local de retirada na etapa anterior, expanda ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Pickup Location]** e forneça informações descritivas sobre a localização:

   - Insira o **[!UICONTROL Frontend Name]** do local de retirada.

   - Insira um **[!UICONTROL Frontend Description]** do local de retirada. Use essa caixa de texto para exibir horas de armazenamento, o local relativo a outros pontos de referência ou outras informações úteis que ajudam o cliente a selecionar o local de retirada correto.

     ![Local de retirada](assets/inventory-pickup-location.png)

   Para obter mais informações sobre como configurar notificações por email ao usar uma origem como um local de coleta, consulte [Emails de vendas](../configuration-reference/sales/sales-emails.md) no _Guia de referência de configuração_.

1. Para salvar seu trabalho, siga um destes procedimentos:

   - Para salvar seu trabalho e continuar editando, clique em **[!UICONTROL Save & Continue]**.

   - Para salvar seu trabalho e retornar à página Gerenciar fontes, clique na seta para baixo (![Seta de menu](../assets/icon-menu-down-arrow-red.png)) e escolha **[!UICONTROL Save & Close]**.

   - Para salvar seu trabalho no registro de origem atual e informar uma nova origem, escolha **[!UICONTROL Save & New]**.

## Barra de botões

| Botão | Descrição |
|--|--|
| [!UICONTROL Back] | Retorna à página Gerenciar fontes. |
| [!UICONTROL Reset] | Restaura todos os campos no formulário aos seus valores no momento do último salvamento. |
| [!UICONTROL Save & Continue] | Salva todas as alterações e mantém o formulário aberto para edição adicional. Clique na seta para baixo para ver opções adicionais:<br/>**[!UICONTROL Save & Close]**- Salva as alterações no registro atual, fecha o formulário e retorna à página Gerenciar fontes.<br/>**[!UICONTROL Save & New]** - Salva alterações, fecha o registro atual e abre um novo formulário em branco. |

## Descrições dos campos

| Campo | Descrição |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | (Obrigatório) Um nome exclusivo que identifica a origem do inventário para os usuários administradores. |
| [!UICONTROL Code] | (Obrigatório) Um código alfanumérico exclusivo que é usado pelo sistema para identificar a origem do inventário. Insira o código em caracteres maiúsculos ou minúsculos e/ou números, sem espaços. Se necessário, um hífen ou sublinhado pode ser usado em vez de um espaço. O código não pode ser editado após a criação da fonte. É uma ID exclusiva usada ao atribuir origens a estoques e exportar e/ou importar dados do produto. |
| [!UICONTROL Is Enabled] | Determina se a origem do estoque está disponível para uso. Opções: Sim / Não |
| [!UICONTROL Description] | Uma breve descrição do local de origem do inventário. Inclua detalhes úteis para seus usuários administradores. |
| [!UICONTROL Latitude] | Especifica a coordenada de latitude da fonte de inventário para GPS. Insira o valor como um número, precedido por um sinal de mais ou menos, conforme necessário. O símbolo de grau e as letras não são permitidos. Por exemplo: Latitude 32.7555 |
| [!UICONTROL Longitude] | Especifica a coordenada de longitude da fonte de inventário para GPS. Insira o valor como um número, precedido por um sinal de mais ou menos, conforme necessário. O símbolo de grau e as letras não são permitidos. Por exemplo: `-97.3308` |
| **[!UICONTROL Contact Info]** | |
| [!UICONTROL Contact Name] | O nome do contato principal no local de origem do estoque. |
| [!UICONTROL Email] | O email do contato principal. |
| [!UICONTROL Phone] | O código de área e o número de telefone do contato principal, usando o formato de sua preferência. Por exemplo: `(123) 456-7890` ou `123-456-7890` |
| [!UICONTROL Fax] | O código de área e o número de fax do contato principal. |
| **[!UICONTROL Address Data]** | |
| [!UICONTROL Country] | (Obrigatório) O país onde a origem do inventário está localizada. |
| [!UICONTROL State/Province] | O estado ou província onde a origem do inventário está localizada. |
| [!UICONTROL City] | A cidade onde a origem do inventário está localizada. |
| [!UICONTROL Street] | O endereço da origem do estoque. |
| [!UICONTROL Postcode] | (Obrigatório) O CEP ou código postal da origem do estoque. |
| **[!UICONTROL Pickup Location]** | |
| [!UICONTROL Frontend Name] | O nome do local de retirada da origem que é exibido na loja. |
| [!UICONTROL Frontend Description] | A descrição do local de retirada da origem que é exibida na loja. Ele pode conter imagens anexadas. |

[1]: https://www.google.com/maps
