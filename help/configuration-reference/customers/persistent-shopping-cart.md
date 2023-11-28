---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Revise as configurações no [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] página do Administrador do Commerce.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>A [Carrinho de compras persistente](../../stores-purchase/cart-persistent.md) permite a retenção de itens não comprados que são deixados no carrinho e os salva por um período configurado em _Duração da persistência_. Os cookies devem ser permitidos no navegador do cliente para usar o carrinho de compras persistente.

## [!UICONTROL General Options]

![Opções gerais](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Site | Determina se a persistência está ativada. |
| [!UICONTROL Persistence Lifetime (seconds)] | Site | Define a duração do cookie persistente em segundos. O valor máximo permitido é de 3153600000 segundos (100 anos). |
| [!UICONTROL Enable "Remember Me"] | Site | Define se a variável _Lembrar-me_ aparece nas páginas de logon e registro da loja. Opções: <br/>**`Yes`**- Exibe o _Lembrar-me_ caixa de seleção<br/>**`No`** - Não exibe a variável _Lembrar-me_ e o cookie persistente será usado somente para os clientes que já o tiverem. |
| [!UICONTROL "Remember Me" Default Value] | Site | Define o estado padrão para o _Lembrar-me_ caixa de seleção |
| [!UICONTROL Clear Persistence on Log Out] | Site | Define se o cookie persistente é excluído quando um cliente da loja faz logoff. Independentemente da configuração, se um cliente não fizer logoff, mas o cookie da sessão expirar, o cookie persistente ainda será usado. |
| [!UICONTROL Persist Shopping Cart] | Site | Define se o uso do cookie persistente dará acesso aos dados do carrinho de compras da conta correspondente. Opções: <br/>**`Yes`**- O conteúdo do carrinho de compras é salvo após o término da sessão.<br/>**`No`** - O conteúdo do carrinho de compras não é salvo após o término da sessão. |
| [!UICONTROL Persist Wish List] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Determina se o estado das listas de desejos do cliente é mantido quando a sessão termina. Opções: <br/>**`Yes`**- O conteúdo da lista de desejos é salvo quando a sessão termina.<br/>**`No`** - A lista de desejos não é salva quando a sessão termina. |
| [!UICONTROL Persist Recently Ordered Items] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Determina se o estado dos itens encomendados recentemente é mantido quando a sessão termina. Opções: <br/>**`Yes`**- O estado dos Itens solicitados recentemente é salvo quando a sessão termina.<br/>**`No`** - O estado dos Itens solicitados recentemente não é salvo quando a sessão termina. |
| [!UICONTROL Persist Currently Compared Products] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Determina se o estado dos produtos comparados atualmente é retido quando a sessão termina. Opções: <br/>**`Yes`**- O estado dos produtos comparados é salvo quando a sessão termina.<br/>**`No`** - O estado dos produtos comparados atualmente não é salvo quando a sessão termina. |
| [!UICONTROL Persist Comparison History] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Determina se o estado do histórico de comparação é retido quando a sessão termina. Opções: <br/>**`Yes`**- O estado do histórico de comparação é salvo quando a sessão termina.<br/>**`No`** - O estado do histórico de comparação não é salvo quando a sessão termina. |
| [!UICONTROL Persist Recently Viewed Products] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Determina se o estado dos produtos visualizados recentemente é mantido quando a sessão termina. Opções: <br/>**`Yes`**- O estado dos produtos visualizados recentemente é salvo quando a sessão termina.<br/>**`No`** - O estado dos produtos visualizados recentemente não é salvo quando a sessão termina. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (Somente no Adobe Commerce) Determina se o estado dos critérios de associação e segmentação de grupo dos clientes é mantido quando a sessão termina. Opções: <br/>**`Yes`**- O estado dos dados de associação de grupo e segmentação do cliente é salvo quando a sessão termina.<br/>**`No`** - O estado da associação de grupo do cliente e os dados de segmentação não são salvos quando a sessão termina. |

{:style=&quot;table-layout:auto&quot;}
