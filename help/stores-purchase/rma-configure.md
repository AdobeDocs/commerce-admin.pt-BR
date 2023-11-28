---
title: Configurar devoluções
description: Saiba como habilitar devoluções para sua loja e configurar os métodos de envio compatíveis.
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Configurar devoluções

{{ee-feature}}

Quando ativadas, as solicitações de RMA podem ser enviadas pelos clientes da loja. Uma RMA só poderá ser gerada se houver um item na ordem que esteja disponível para devolução. As solicitações para retornar itens individuais são gerenciadas pelo _Ativar RMA_ em cada registro de produto. Por padrão, as configurações são aplicadas ao produto (_[!UICONTROL Use Config Settings]_for selecionada). Se_[!UICONTROL Enable RMA]_ está definida como `No`, o produto não aparece na lista de itens disponíveis para devolução. Se você alterar a variável _Ativar RMA_ se aplica tanto a pedidos novos como a pedidos existentes.

## Habilitar RMAs para sua loja

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL RMA Settings]** seção.

   ![Configurações de RMA](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Enable RMA on Storefront]** para `Yes`.

   Esta configuração determina se os clientes podem criar e visualizar solicitações de RMA na loja. As RMAs podem ser aplicadas a ordens novas e existentes.

1. Definir **[!UICONTROL Enable RMA on Product Level]** para `Yes`.

   Essa configuração determina o comportamento do _Ativar RMA_ atributo para produtos individuais na loja:

   - Quando [!UICONTROL Enable RMA on Product Level] está definida como `Yes`, os clientes da loja podem devolver todos os produtos individuais. Inclui ambas as _[!UICONTROL Enable RMA]_= `Yes` e_[!UICONTROL Enable RMA]_ = `No` valores de atributo de produto.
   - Quando [!UICONTROL Enable RMA on Product Level] está definida como `No`, os clientes da loja podem devolver apenas os produtos com uma _[!UICONTROL Enable RMA]_= `Yes` valor do atributo do produto.

1. Definir **[!UICONTROL Use Store Address]** a um dos seguintes valores:

   - `Yes` - Enviar produtos devolvidos para o endereço da loja.
   - `No` - Digite um endereço alternativo para devoluções de produtos.

   ![Configurações de RMA com endereço alternativo](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.

## Configurar métodos de envio para devoluções

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Delivery Methods]**.

1. Expanda a seção da transportadora que deseja usar para o serviço de devolução, como **[!UICONTROL UPS]**.

   ![Habilitar serviço RMA para operadora](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Enabled for RMA]** para `Yes`.

1. Clique em **[!UICONTROL Save Config]**.

## Alterar RMAs permitidas no nível do produto

Se você habilitar as RMAs para sua loja e seu catálogo contiver alguns produtos que não devem ter permissão para devolução, será possível modificar a configuração no nível do produto,

1. Abra o produto no modo de edição.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Autosettings]** seção.

1. Limpe a **[!UICONTROL Use Config Setting]** , se necessário.

1. Alterne a **[!UICONTROL Enable RMA]** configuração para `No`.

   ![Desativar a RMA para um produto](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save]**.
