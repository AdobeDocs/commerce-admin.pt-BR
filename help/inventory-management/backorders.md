---
title: "Configurar [!DNL Inventory Management] ordens pendentes"
description: Saiba como configurar pedidos pendentes para dar suporte à venda de produtos indisponíveis.
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Configurar ordens pendentes do [!DNL Inventory Management]

Os backorders permitem que sua loja continue vendendo produtos depois que a quantidade atingir zero ou ficar efetivamente fora do estoque. Quando uma ordem de cliente é um backorder, os fundos são autorizados e capturados imediatamente, o status de processamento da ordem não é alterado e a entrega permanece em espera até que o estoque esteja disponível.

Dependendo da loja e das vendas, talvez você queira ativar ou desativar backorders nos seguintes níveis:

- **[!UICONTROL Global]** - Todos os produtos no seu catálogo no nível do site

- **[!UICONTROL Product]** - Produtos específicos que substituem configurações de site, origem e estoque

## Entender as configurações de ordem pendente

É altamente recomendável que você defina limites e configurações específicos para melhor suportar backorders.

### Limite de indisponibilidade

Use um valor negativo para esse limite para definir a quantidade máxima de produtos que podem ter backorder antes que o produto seja realmente considerado indisponível. Esse valor é adicionado à quantidade vendável. O valor definido no nível do produto substitui qualquer valor definido no nível global.

A fórmula para a Quantidade Venável é `(Quantity - (Out-of-Stock Threshold))`.

Veja um exemplo a seguir:

- Quantidade: 25
- Notificação para Quantidade Abaixo: 10
- Somente X limite esquerdo: 5
- Limite de Fora do Estoque: -50

A Quantidade Venável deste produto é `75 (25 - (-50))`.

![Exemplo de Quantidade Venável antes de ordens pendentes habilitadas](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![Exemplo de Quantidade Venável após ordens pendentes habilitadas](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

Quando os clientes compram os 25 produtos disponíveis, os novos pedidos são inseridos como ordens pendentes. Como a Quantidade Comercializável do produto é reduzida para 5 (70 itens foram vendidos), a página _Produto_ exibe uma mensagem `Only 5 left` na loja. Quando a Quantidade de Vendas atinge `0`, o produto é exibido como `Out of Stock` na loja.

>[!NOTE]
>
>Quando um cliente faz um pedido usando _[!UICONTROL backorder qty]_, [!DNL Inventory Management] subtrai automaticamente a quantidade da quantidade vendável. Se uma ordem não for entregue e for cancelada, a quantidade retornará para a quantidade vendida virtual agregada. A **_quantidade da ordem cancelada não está atribuída a nenhuma das origens_**, mas é retornada ao número total de produtos disponíveis para venda (_[!UICONTROL Salable Quantity]_ coluna na grade de produtos).

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### Status do estoque

Os produtos devem ser definidos com o status `In Stock` ao habilitar ordens pendentes. Você pode definir este valor na página _Produto_. Para comerciantes de várias origens, você deve ter pelo menos uma origem marcada como `In Stock`. Acesse e defina o status por meio da página _Produto_ e da grade _Fontes_ atribuída.

## Configurar backorders globalmente

Essas etapas permitem backorders para todos os produtos no nível do site.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Defina **[!UICONTROL Store View]** como `Default Config`.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Inventory]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**.

1. Para **[!UICONTROL Backorders]**, desmarque a caixa de seleção **[!UICONTROL Use system value]** e selecione uma opção:

   | Opção | Descrição |
   | -- | -- |
   | `No Backorders` | Para não aceitar pedidos pendentes quando o produto estiver indisponível. |
   | `Allow Qty Below 0` | Para aceitar backorders quando a quantidade cair abaixo de zero. |
   | `Allow Qty Below 0 and Notify Customer` | Para aceitar backorders quando a quantidade cair abaixo de zero e notificar o cliente que o pedido ainda pode ser feito. |

1. Para **[!UICONTROL Out-of-Stock Threshold]**, desmarque a caixa de seleção **[!UICONTROL Use system value]** e insira um valor diferente.

   | Valor | Descrição |
   | -- | -- |
   | Valor positivo | Com Ordens pendentes desativadas, informe um valor positivo. |
   | Zero | Com Backorders habilitado, inserir `0` permite backorders infinitos. |
   | Valor negativo | Com Backorders ativados, é recomendável inserir um valor negativo. O valor é adicionado à Quantidade Venável. Por exemplo, insira `-50` para permitir pedidos até esse valor. |

1. Clique em **[!UICONTROL Save Config]**.

## Configurar backorders para um produto

As configurações de nível de produto substituem as configurações globais. Talvez você queira configurar backorders no nível do produto para substituir as configurações no nível da loja global ou da origem. Por exemplo, sua loja pode suportar pedidos pendentes globalmente. Com as configurações do produto, é possível desativar pedidos pendentes ou alterar o limite de indisponibilidade sem afetar outros produtos e origens.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra um produto no modo **[!UICONTROL Edit]** e role a página até a área _[!UICONTROL Sources]_.

   Para produtos configurados sem o [!DNL Inventory Management], a guia não é exibida. O botão `Advanced Inventory` é exibido sob o campo _[!UICONTROL Quantity]_.

1. Clique em **[!UICONTROL Advanced Inventory]**.

   Essa ação exibe uma página de configurações específicas do produto. Qualquer configuração listada como `global` exibe a configuração global atual para o armazenamento.

1. Para **[!UICONTROL Backorders]**, desmarque a caixa de seleção **[!UICONTROL Use Config Setting]** e selecione uma opção:

   | Opção | Descrição |
   | -- | -- |
   | `No Backorders` | Para não aceitar pedidos pendentes quando o produto estiver indisponível. |
   | `Allow Qty Below 0` | Para aceitar backorders quando a quantidade cair abaixo de zero. |
   | `Allow Qty Below 0 and Notify Customer` | Para aceitar backorders quando a quantidade cair abaixo de zero e para notificar o cliente que o pedido ainda pode ser feito. |

1. Para **[!UICONTROL Out-of-Stock Threshold]**, desmarque a caixa de seleção **[!UICONTROL Use Config Setting]** e insira um valor:

   | Valor | Descrição |
   | -- | -- |
   | Valor positivo | Com Ordens pendentes desativadas, informe um valor positivo. |
   | Zero | Com Backorders habilitado, inserir `0` permite backorders infinitos. |
   | Valor negativo | Com Backorders ativados, é recomendável inserir um valor negativo. O valor é adicionado à Quantidade Venável. Por exemplo, insira `-50` para permitir pedidos até esse valor. |

   ![Inventário Avançado configurado para Backorders](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Done]** e depois em **[!UICONTROL Save]**.
