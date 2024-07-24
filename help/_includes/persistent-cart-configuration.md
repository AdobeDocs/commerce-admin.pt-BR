---
title: Referência de configuração do carrinho de compras persistente
description: Conteúdo reutilizável para a referência de configuração do carrinho de compras persistente.
source-git-commit: d23cb0d63409e533cf950d8d14514d9f9157fd05
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![Opções gerais](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Campo | [Escopo](/help/getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | Site | Determina se o recurso de persistência está ativado. |
| [!UICONTROL Persistence Lifetime (seconds)] | Site | Define a duração do cookie persistente em segundos. O valor máximo permitido é 34560000 segundos (400 dias). Esta é uma limitação da vida útil máxima recomendada do cookie. |
| [!UICONTROL Enable "Remember Me"] | Site | Define se a caixa de seleção _Lembre-se de Mim_ será exibida nas páginas de logon e registro do armazenamento. Opções: <br/>**`Yes`**- Exibe a caixa de seleção _Lembrar-se de Mim_.<br/>**`No`** - Não exibe a caixa de seleção _Lembrar-se de mim_ e o cookie persistente é usado apenas para clientes que já o possuem. |
| [!UICONTROL "Remember Me" Default Value] | Site | Define o estado padrão da caixa de seleção _Lembrar-se de mim_. |
| [!UICONTROL Clear Persistence on Log Out] | Site | Define se o cookie persistente é excluído quando um cliente da loja faz logoff. Independentemente de como essa opção esteja configurada, se um cliente não fizer logoff, mas o cookie da sessão expirar, o cookie persistente ainda será usado. |
| [!UICONTROL Persist Shopping Cart] | Site | Define se o uso do cookie persistente dará acesso aos dados do carrinho de compras da conta correspondente. Opções: <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Wish List] | Site | ![Adobe Commerce](/help/assets/adobe-logo.svg) (somente Adobe Commerce) determina se o estado das listas de desejos dos clientes é mantido quando a sessão termina. Opções: <br/>**`Yes`**- O conteúdo da lista de desejos é salvo quando a sessão termina.<br/>**`No`** - A lista de desejos não é salva quando a sessão termina. |
| [!UICONTROL Persist Recently Ordered Items] | Site | ![Adobe Commerce](/help/assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado dos itens encomendados recentemente é salvo quando a sessão termina. Opções: <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Currently Compared Products] | Site | ![Adobe Commerce](/help/assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado dos produtos comparados atualmente é mantido quando a sessão termina. Opções: <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Comparison History] | Site | ![Adobe Commerce](/help/assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado do histórico de comparação é retido quando a sessão termina. Opções: <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Recently Viewed Products] | Site | ![Adobe Commerce](/help/assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado dos produtos visualizados recentemente será mantido quando a sessão terminar. Opções: <br/>**`Yes`**ou **`No`**. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Site | ![Adobe Commerce](/help/assets/adobe-logo.svg) (somente Adobe Commerce) Determina se o estado dos critérios de associação de grupo e segmentação dos clientes é mantido quando a sessão termina. Opções: <br/>**`Yes`**- O estado dos dados de segmentação e associação de grupo do cliente é salvo quando a sessão termina.<br/>**`No`** - O estado dos dados de segmentação e associação de grupo do cliente não é salvo quando a sessão termina. |

{style="table-layout:auto"}
