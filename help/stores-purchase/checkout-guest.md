---
title: Check-out de convidado
description: Saiba como habilitar recursos de check-out de convidado em sua loja.
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
source-git-commit: 347321ec5b0722f06240780136cb29816aab559f
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Check-out de convidado

Sua loja pode ser configurada para exigir que os compradores abram uma conta antes de fazer uma compra. A configuração padrão permite que os convidados façam compras, com uma opção para se registrarem em uma conta depois de concluírem o processo de finalização.

![O armazenamento Luma exibe Fazer Check-out como Convidado](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_Para desabilitar check-out de convidado:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Checkout]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Checkout Options]**.

   ![Opções de check-out expandidas na página de configuração](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Opções de Check-out](../configuration-reference/sales/checkout.md#checkout-options) no _Guia de Referência de Configuração_.

1. Se a configuração for para um modo de exibição de repositório específico, [escolha o modo de exibição de repositório](../configuration-reference/scope-change.md#set-the-scope) ao qual a configuração se aplica.

   Quando solicitado, clique em **[!UICONTROL OK]** para continuar.

1. Defina **[!UICONTROL Allow Guest Checkout]** como `No`.

   Se necessário, desmarque a caixa de seleção **[!UICONTROL Use system value]** para habilitar alterações nessa configuração.

1. Clique em **[!UICONTROL Save Config]**.

## Permitir acesso de pedido de convidado para emails registrados

[!BADGE Somente SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplicável somente a projetos do Adobe Commerce as a Cloud Service (infraestrutura SaaS gerenciada pela Adobe)."}

Uma configuração opcional no nível da loja, que é desativada por padrão, permite que os compradores convidados rastreiem seus pedidos feitos usando um endereço de email que corresponda a uma conta de cliente registrada.

Quando ativado, os pedidos de check-out de convidado feitos com um email registrado permanecem acessíveis e também aparecem no histórico de pedidos do cliente.

Para habilitar este recurso, navegue até **Lojas** > Configurações > **Configuração** > Vendas > **Vendas** > **Check-out de Convidado** e defina a configuração **Permitir Acesso de Pedido de Convidado para Emails Registrados** como `Yes`.
