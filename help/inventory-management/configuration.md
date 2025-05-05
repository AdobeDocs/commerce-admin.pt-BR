---
title: Configurar [!DNL Inventory Management]
description: Saiba mais sobre a configuração de  [!DNL Inventory Management]  opções que determinam a disponibilidade de origem, os produtos da loja e a remessa do pedido.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# Configurar [!DNL Inventory Management]

O módulo [!DNL Inventory Management] oferece suporte às definições de configuração de inventário no nível do produto e global e também fornece definições adicionais que afetam a disponibilidade da origem, os produtos da loja e a remessa do pedido. As configurações se aplicam a:

- O catálogo inteiro: Vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Em seguida, expanda **[!UICONTROL Catalog]**&#x200B;no painel esquerdo e selecione **[!UICONTROL Inventory]**.

- Produtos específicos: Vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. Em seguida, abra o produto no modo de edição e clique em **[!UICONTROL Advanced Inventory]** na seção _[!UICONTROL Sources]_.

Seu catálogo pode ser configurado para exibir dados de inventário em sua vitrine, gerenciar carrinhos de compras ativos e muito mais. Exiba a disponibilidade de cada item como _Em Estoque_ ou _Sem Estoque_ e o estoque disponível quando o estoque estiver baixo.

O limite de indisponibilidade indica quando um produto deve ser reordenado, subtrai da Quantidade Venável de um estoque e pode ser definido para suportar backorders ativados ou desativados. Permitir backorders para sua loja, definindo uma quantidade máxima de ordens para todos os produtos ou produtos específicos.

Outra maneira de usar o limite de disponibilidade de estoque é gerenciar produtos que estejam em alta demanda. Se você quiser capturar novos clientes, em vez de vender para compradores de alta quantidade, poderá definir uma quantidade máxima para impedir que um único comprador obtenha todo o inventário.

![Exemplo de Em Estoque, Somente 1 Restante](assets/storefront-stock-options-1-left.png)

## Opções de configuração

As lojas e os produtos do [!DNL Commerce] oferecem suporte às seguintes configurações para gerenciamento de produtos, inventário, notificações e muito mais. [!DNL Commerce] fornece definições de configuração adicionais para ações em massa e o algoritmo de Prioridade de Distância.

| Opção | Descrição |
|--|--|
| [!UICONTROL Manage Stock] | Habilita [!DNL Commerce] para gerenciar todo o estoque. Defina se o controle de estoque é usado para este produto ou todos os produtos em [!DNL Commerce]. Exibe mais opções quando definido como `Yes`. |
| [!UICONTROL Only X left Threshold] | Define uma quantidade a ser notificada quando um valor específico ficar disponível para compra. Esse valor é rastreado no nível do estoque. |
| [!UICONTROL Out-of-Stock Threshold] | Seu Estoque de Segurança, Quantidade para acionar uma notificação de Ausência de Estoque e reduzir o risco de falta de estoque. Esse valor afeta ordens pendentes. Opções:<br />**[!UICONTROL No Backorders]**: não aceita pedidos pendentes quando o produto está esgotado.<br />**[!UICONTROL Allow Qty Below 0]**: aceita ordens pendentes quando a quantidade cai abaixo de zero.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: aceita ordens pendentes quando a quantidade cai abaixo de zero, mas notifica os clientes que as ordens ainda podem ser feitas.<br /><br />**[!UICONTROL Backorders disabled]**: é recomendável inserir um valor positivo acima de 0, como 5 ou 25. <br/>**[!UICONTROL Backorders enabled]**: insira um limite negativo para a quantidade máxima de ordens pendentes permitidas, como -5 ou -25. Um valor de 0 atua como estoque infinito. Um valor positivo é ignorado e tratado como 0. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Define a quantidade mínima do produto que pode ser comprado em um único pedido. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Define a quantidade máxima do produto que pode ser comprado em um único pedido. |
| [!UICONTROL Qty Uses Decimals] | Permite valores decimais para a quantidade de um produto, em vez de números inteiros. Essa configuração é útil para produtos vendidos por peso, volume ou comprimento. Especificado no nível do Source, calculado no nível do Estoque com base nas Fontes atribuídas. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Determina se as peças de um produto podem ser enviadas separadamente. Esta opção fica visível quando **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Indica se Backorders são permitidos. Especificado no nível do Source, calculado no nível do Estoque com base nas Fontes atribuídas. Se habilitado para permitir backorders, é recomendado definir um valor negativo para o Limite de Falta de Estoque (consulte [Configurando Backorders](backorders.md)). Opções:<br />**[!UICONTROL No Backorders]**: não aceita pedidos pendentes quando o produto está esgotado.<br />**[!UICONTROL Allow Qty Below 0]**: aceita ordens pendentes quando a quantidade cai abaixo de zero.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: aceita ordens pendentes quando a quantidade cai abaixo de zero, mas notifica os clientes que as ordens ainda podem ser feitas. |
| [!UICONTROL Notify for Quantity Below] | Define a quantidade que aciona uma notificação de Quantidade Abaixo, aviso de baixo estoque. Esse valor é deduzido da Quantidade Venável, não da Quantidade do inventário. |
| [!UICONTROL Enable Qty Increments] | Determina se o produto pode ser vendido em incrementos de quantidade. Se habilitado, insira a quantidade de produtos que devem ser comprados em uma etapa incremental. Os incrementos definem quantos itens de produto devem ser comprados como um único produto e como um filho de produtos configuráveis, agrupados e agrupados. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] não usa este valor. Quando você conclui uma devolução ou um aviso de crédito, a quantidade do produto é automaticamente retornada à quantidade de origem afetada. Consulte [Configurando Opções de Produto](product-options.md). |

## Retorno e herança da configuração

As configurações substituem ou se aplicam ao seguinte caminho de herança: a seção do produto _[!UICONTROL Sources]_&#x200B;substitui a configuração de armazenamento global&#x200B;_[!UICONTROL Inventory]_ do produto _[!UICONTROL Advanced Options]_.

Quando o [!DNL Commerce] procura configurações personalizadas a serem aplicadas, ele segue esta ordem:

1. Procura configurações personalizadas no nível do Produto na seção _[!UICONTROL Sources]_. Algumas configurações estão disponíveis.

1. Verifica as configurações do Produto _[!UICONTROL Advanced Inventory]_.

1. Se `Use Config Settings` for selecionado para as configurações do produto, ele verificará um valor da página de configuração de loja do _Inventário_ global.

Por exemplo, você pode configurar ordens pendentes de forma diferente na loja com uma configuração semelhante à seguinte:

- _Globalmente:_ Habilitar ordens pendentes para o armazenamento, definir o Limite de Indisponibilidade como `-50`

- _Produto:_ Desabilitar ordens pendentes para um produto específico, definir Limite de Produto Indisponível como `10`
