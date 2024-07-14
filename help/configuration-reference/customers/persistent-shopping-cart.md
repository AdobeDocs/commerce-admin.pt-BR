---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Revise as configurações na página [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] do Administrador do Commerce.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>Um [Carrinho de Compras Persistente](../../stores-purchase/cart-persistent.md) permite a retenção de itens não comprados que são deixados no carrinho e os salva por um período configurado em _Duração da Persistência_. Os cookies devem ser permitidos no navegador do cliente para usar o carrinho de compras persistente.

## [!UICONTROL General Options]

![Opções gerais](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Site | Determina se a persistência está ativada. |
| [!UICONTROL Persistence Lifetime (seconds)] | Site | Define a duração do cookie persistente em segundos. O valor máximo permitido é de 3153600000 segundos (100 anos). |
| [!UICONTROL Enable "Remember Me"] | Site | Define se a caixa de seleção _Lembre-se de Mim_ aparecerá nas páginas de logon e registro do armazenamento. Opções: <br/>**`Yes`**- Exibe a caixa de seleção _Lembrar-se de Mim_.<br/>**`No`** - Não exibe a caixa de seleção _Lembrar-se de mim_ e o cookie persistente é usado apenas para clientes que já o possuem. |
| [!UICONTROL "Remember Me" Default Value] | Site | Define o estado padrão da caixa de seleção _Lembrar-se de mim_. |
| [!UICONTROL Clear Persistence on Log Out] | Site | Define se o cookie persistente é excluído quando um cliente da loja faz logoff. Independentemente da configuração, se um cliente não fizer logoff, mas o cookie da sessão expirar, o cookie persistente ainda será usado. |
| [!UICONTROL Persist Shopping Cart] | Site | Define se o uso do cookie persistente dará acesso aos dados do carrinho de compras da conta correspondente. Opções: <br/>**`Yes`**- O conteúdo do carrinho de compras é salvo após o término da sessão.<br/>**`No`** - O conteúdo do carrinho de compras não é salvo após o término da sessão. |
| [!UICONTROL Persist Wish List] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (somente Adobe Commerce) determina se o estado das listas de desejos dos clientes é mantido quando a sessão termina. Opções: <br/>**`Yes`**- O conteúdo da lista de desejos é salvo quando a sessão termina.<br/>**`No`** - A lista de desejos não é salva quando a sessão termina. |
| [!UICONTROL Persist Recently Ordered Items] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado dos itens encomendados recentemente é mantido quando a sessão termina. Opções: <br/>**`Yes`**- O estado de Itens Recentemente Solicitados é salvo quando a sessão termina.<br/>**`No`** - O estado dos Itens Recentemente Solicitados não é salvo quando a sessão termina. |
| [!UICONTROL Persist Currently Compared Products] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado dos produtos comparados no momento será mantido quando a sessão terminar. Opções: <br/>**`Yes`**- O estado dos produtos comparados atualmente é salvo quando a sessão termina.<br/>**`No`** - O estado dos produtos atualmente comparados não é salvo quando a sessão termina. |
| [!UICONTROL Persist Comparison History] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado do histórico de comparação é retido quando a sessão termina. Opções: <br/>**`Yes`**- O estado do histórico de comparação é salvo quando a sessão termina.<br/>**`No`** - O estado do histórico de comparação não é salvo quando a sessão termina. |
| [!UICONTROL Persist Recently Viewed Products] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado dos produtos visualizados recentemente será mantido quando a sessão terminar. Opções: <br/>**`Yes`**- O estado dos produtos visualizados recentemente é salvo quando a sessão termina.<br/>**`No`** - O estado dos produtos visualizados recentemente não é salvo quando a sessão termina. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Site | ![Adobe Commerce](../../assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado dos critérios de associação de grupo e segmentação dos clientes é mantido quando a sessão termina. Opções: <br/>**`Yes`**- O estado dos dados de segmentação e associação de grupo do cliente é salvo quando a sessão termina.<br/>**`No`** - O estado dos dados de segmentação e associação de grupo do cliente não é salvo quando a sessão termina. |

{style="table-layout:auto"}
