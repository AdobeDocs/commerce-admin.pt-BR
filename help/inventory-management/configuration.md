---
title: "Configurar [!DNL Inventory Management]"
description: Saiba mais sobre a configuração do [!DNL Inventory Management] opções que determinam a disponibilidade de origem, os produtos da loja e a entrega do pedido.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# Configurar [!DNL Inventory Management]

A variável [!DNL Inventory Management] O módulo suporta as definições de configuração de inventário no nível do produto e global e também fornece definições adicionais que afetam a disponibilidade da origem, os produtos da loja e a entrega do pedido. As configurações se aplicam a:

- O catálogo inteiro: Ir para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Em seguida, expanda **[!UICONTROL Catalog]**no painel esquerdo e selecione **[!UICONTROL Inventory]**.

- Produtos específicos: Vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. Abra o produto no modo de edição e clique em **[!UICONTROL Advanced Inventory]** no _[!UICONTROL Sources]_seção.

Seu catálogo pode ser configurado para exibir dados de inventário em sua vitrine, gerenciar carrinhos de compras ativos e muito mais. Exibir a disponibilidade de cada item como _Em estoque_ ou _Sem estoque_ e o estoque disponível quando o estoque estiver baixo.

O limite de indisponibilidade indica quando um produto deve ser reordenado, subtrai da Quantidade Venável de um estoque e pode ser definido para suportar backorders ativados ou desativados. Permitir backorders para sua loja, definindo uma quantidade máxima de ordens para todos os produtos ou produtos específicos.

Outra maneira de usar o limite de disponibilidade de estoque é gerenciar produtos que estejam em alta demanda. Se você quiser capturar novos clientes, em vez de vender para compradores de alta quantidade, poderá definir uma quantidade máxima para impedir que um único comprador obtenha todo o inventário.

![Exemplo de Em estoque, Somente 1 restante](assets/storefront-stock-options-1-left.png)

## Opções de configuração

[!DNL Commerce] lojas e produtos oferecem suporte às seguintes configurações para gerenciamento de produtos, inventário, notificações e muito mais. [!DNL Commerce] O fornece definições de configuração adicionais para ações em massa e o algoritmo de Prioridade de distância.

| Opção | Descrição |
|--|--|
| [!UICONTROL Manage Stock] | Habilita [!DNL Commerce] para gerenciar todo o inventário. Definir se o controle de estoque é usado para este produto ou todos os produtos em [!DNL Commerce]. Exibe mais opções quando configurado como `Yes`. |
| [!UICONTROL Only X left Threshold] | Define uma quantidade a ser notificada quando um valor específico ficar disponível para compra. Esse valor é rastreado no nível do estoque. |
| [!UICONTROL Out-of-Stock Threshold] | Seu Estoque de Segurança, Quantidade para acionar uma notificação de Ausência de Estoque e reduzir o risco de falta de estoque. Esse valor afeta ordens pendentes. Opções:<br />**[!UICONTROL No Backorders]**: não aceita pedidos pendentes quando o produto estiver indisponível.<br />**[!UICONTROL Allow Qty Below 0]**: aceita backorders quando a quantidade cai abaixo de zero.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: aceita backorders quando a quantidade cai abaixo de zero, mas notifica os clientes que os pedidos ainda podem ser feitos.<br /><br />**[!UICONTROL Backorders disabled]**: É recomendado inserir um valor positivo acima de 0, como 5 ou 25. <br/>**[!UICONTROL Backorders enabled]**: Informe um limite negativo para a quantidade máxima de backorders permitidos, como -5 ou -25. Um valor de 0 atua como estoque infinito. Um valor positivo é ignorado e tratado como 0. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Define a quantidade mínima do produto que pode ser comprado em um único pedido. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Define a quantidade máxima do produto que pode ser comprado em um único pedido. |
| [!UICONTROL Qty Uses Decimals] | Permite valores decimais para a quantidade de um produto, em vez de números inteiros. Essa configuração é útil para produtos vendidos por peso, volume ou comprimento. Especificado no nível de Origem, calculado no nível de Estoque com base nas Origens atribuídas. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Determina se as peças de um produto podem ser enviadas separadamente. Essa opção estará visível quando **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Indica se Backorders são permitidos. Especificado no nível de Origem, calculado no nível de Estoque com base nas Origens atribuídas. Se ativado para permitir backorders, definindo um valor negativo para o Limite de Indisponibilidade (consulte [Configurando Backorders](backorders.md)) é recomendada. Opções:<br />**[!UICONTROL No Backorders]**: não aceita pedidos pendentes quando o produto estiver indisponível.<br />**[!UICONTROL Allow Qty Below 0]**: aceita backorders quando a quantidade cai abaixo de zero.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: aceita backorders quando a quantidade cai abaixo de zero, mas notifica os clientes que os pedidos ainda podem ser feitos. |
| [!UICONTROL Notify for Quantity Below] | Define a quantidade que aciona uma notificação de Quantidade Abaixo, aviso de baixo estoque. Esse valor é deduzido da Quantidade Venável, não da Quantidade do inventário. |
| [!UICONTROL Enable Qty Increments] | Determina se o produto pode ser vendido em incrementos de quantidade. Se habilitado, insira a quantidade de produtos que devem ser comprados em uma etapa incremental. Os incrementos definem quantos itens de produto devem ser comprados como um único produto e como um filho de produtos configuráveis, agrupados e agrupados. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] não usa esse valor. Quando você conclui uma devolução ou um aviso de crédito, a quantidade do produto é automaticamente retornada à quantidade de origem afetada. Consulte [Configuração das opções de produto](product-options.md). |

## Retorno e herança da configuração

As configurações substituem ou se aplicam ao seguinte caminho de herança: Produto _[!UICONTROL Sources]_a seção substitui o produto_[!UICONTROL Advanced Options]_ substitui global _[!UICONTROL Inventory]_configuração de armazenamento.

Quando [!DNL Commerce] O verifica as configurações personalizadas a serem aplicadas; segue esta ordem:

1. Verifica as configurações personalizadas no nível do Produto na _[!UICONTROL Sources]_seção. Algumas configurações estão disponíveis.

1. Verifica o produto _[!UICONTROL Advanced Inventory]_configurações.

1. Se `Use Config Settings` for selecionada para as configurações do produto, ela verificará um valor do campo _Inventário_ página de configuração da loja.

Por exemplo, você pode configurar ordens pendentes de forma diferente na loja com uma configuração semelhante à seguinte:

- _Globalmente:_ Habilitar ordens pendentes para o armazenamento, definir o Limite de Indisponibilidade como `-50`

- _Produto:_ Desative os pedidos pendentes de um produto específico, defina o Limite de indisponibilidade como `10`
