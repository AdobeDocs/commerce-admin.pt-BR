---
title: Configurações do produto - [!UICONTROL Gift Options]
description: Para um produto, as configurações de [!UICONTROL Gift Options] determinam se uma mensagem de presente pode ser incluída ou se as opções de invólucro do presente estão disponíveis durante o check-out.
exl-id: 21597e38-60f5-45e5-8d99-955d088c5c48
feature: Catalog Management, Products, Gift
TQID: 'https://experienceleague.adobe.com/MIzb2vY-DiVqODkNFmgX3tFLejQFZMtOETUDPoHrt-Y'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 4fc0a729-4349-5307-bd06-1b4bfbaf5d0c
    internal-label: Gift
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%
---
# Configurações do produto - [!UICONTROL Gift Options]

Na seção _[!UICONTROL Gift Options]_, é possível definir opções de mensagem de presente e invólucro de presente no check-out no nível do produto. Para substituir a configuração padrão, desmarque a caixa de seleção **[!UICONTROL Use Config Settings]**.

![Opções de presente](./assets/product-gift-options-ee.png){width="600" zoomable="yes"}

## Definir opções de presente para um único produto

1. Abra o produto no modo de edição.

1. Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Gift Options]_e faça o seguinte:

   - Para substituir a configuração padrão, desmarque a caixa de seleção **[!UICONTROL Use Config Settings]**.

   - Defina **[!UICONTROL Allow Gift Message]** conforme necessário para o produto.

   - ![Adobe Commerce](../assets/adobe-logo.svg) ([Adobe Commerce](../landing/home.md#product-editions) somente) Defina **[!UICONTROL Allow Gift Wrapping]** conforme necessário para o produto.

   - ![Adobe Commerce](../assets/adobe-logo.svg) ([Adobe Commerce](../landing/home.md#product-editions) somente) Se aplicável, insira o **[!UICONTROL Price for Gift Wrapping]**.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Habilitar mensagens de presente para sua loja

Por padrão, o Commerce permite que os clientes adicionem uma mensagem de presente personalizada a seus pedidos e produtos durante o processo de finalização.

Você pode fornecer este recurso aos clientes habilitando a _mensagem de presente_ para sua loja:

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales]** abaixo de.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** na página.

1. Para **[!UICONTROL Allow Gift Messages on Order Level]**, selecione `Yes` para habilitar uma única mensagem de presente para todo o pedido.

1. Para **[!UICONTROL Allow Gift Messages for Order Items]**, selecione `Yes` para habilitar a adição de mensagens de presente separadamente a itens individuais no carrinho de compras do cliente.

1. Clique em **[!UICONTROL Save Config]**.

Com essa configuração, os clientes podem adicionar uma mensagem de presente à página do carrinho de loja, conforme mostrado no exemplo a seguir:

![Mensagem de presente](./assets/gift-message.png){width="600" zoomable="yes"}
