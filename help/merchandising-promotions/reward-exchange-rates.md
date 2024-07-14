---
title: Taxas de câmbio de recompensa
description: Saiba como configurar as taxas de câmbio de premiação que determinam o número de pontos de premiação ganhos.
exl-id: 4850d853-fb86-4f64-bfee-47915ea028e2
feature: Rewards, Promotions/Events, Customers
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Taxas de câmbio de recompensa

{{ee-feature}}

As taxas de câmbio de premiação determinam o número de pontos ganhos com base no valor do pedido e no valor dos pontos ganhos. Diferentes taxas de câmbio podem ser aplicadas a diferentes sites e grupos de clientes. Se várias taxas de câmbio de sites e grupos de clientes diferentes forem aplicadas ao mesmo cliente, as seguintes regras de prioridade serão aplicadas:

## Prioridade de taxa de câmbio

**1**: aplica-se a um site específico e a um grupo de clientes específico.

**2**: aplica-se a todos os sites e a um grupo de clientes específico.

**3**: aplica-se a um site específico e a todos os grupos de clientes.

**4**: aplica-se a todos os sites e grupos de clientes.

Ao converter a moeda em pontos, o número de pontos não pode ser dividido. O restante de qualquer moeda é arredondado para baixo. Por exemplo, se $2,00 converte para dez pontos, os pontos são ganhos em grupos de $2,00. Portanto, um pedido de US$ 7,00 ganharia 30 pontos e os US$ 1,00 restantes seriam arredondados para baixo. A quantia monetária do pedido é definida como a quantia que o comerciante recebe ou o total geral menos os impostos, frete, descontos, crédito de loja e cartões-presente. Os pontos são ganhos no momento em que não há itens não faturados no pedido (todos os itens são pagos ou cancelados). Se um usuário administrador não quiser permitir que os clientes ganhem pontos de recompensa por pedidos cancelados, esses pontos podem ser deduzidos manualmente da página Gerenciar clientes.

## Configurar taxas de câmbio

![Taxas de câmbio de recompensa](./assets/reward-exchange-rates.png){width="700" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Rate]**.

1. Na seção **[!UICONTROL Reward Exchange Rate Information]**, faça o seguinte:

   ![Taxas de câmbio de premiação - informações](./assets/reward-exchange-rate-new.png){width="600" zoomable="yes"}

   - Defina **[!UICONTROL Website]** para os sites nos quais a taxa de câmbio de premiação se aplica.

   - Defina **[!UICONTROL Customer Group]** para os grupos aos quais a taxa de câmbio da premiação se aplica.

   - Defina **[!UICONTROL Direction]** como um dos seguintes:

      - `Points to Currency`
      - `Currency to Points`

   Para qualquer configuração de Direção, o valor é representado na moeda base do site.

1. Insira os valores de **[!UICONTROL Rate]** de acordo com a configuração _[!UICONTROL Direction]_.

   | Direção | Configurações de taxa |
   |---------|-------------|
   | [!UICONTROL Points to Currency] | No primeiro campo _[!UICONTROL Rate]_, insira o número de pontos. No segundo campo_[!UICONTROL Rate]_, insira o valor monetário dos pontos. |
   | [!UICONTROL Currency to Points] | No primeiro campo _[!UICONTROL Rate]_, insira o valor monetário. No segundo campo_[!UICONTROL Rate]_, insira o número de pontos que é representado pelo valor monetário. |

   Ao converter pontos em moeda, o número de pontos não pode ser dividido. Por exemplo, se dez pontos forem convertidos em US$ 2,00, os pontos deverão ser resgatados em grupos de dez. Portanto, 25 pontos seriam resgatados por US$ 4,00, com 5 pontos restantes no saldo do cliente.

   É recomendável configurar uma conversão para `Points to Currency` e `Currency to Points`.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Excluir uma taxa de câmbio de premiação

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Localizar a taxa de câmbio da premiação a ser excluída e abri-la no modo de edição.

1. Na barra de menus, clique em **[!UICONTROL Delete]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

## Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Website] | Os sites nos quais as taxas de recompensa se aplicam. |
| [!UICONTROL Customer Group] | Os grupos de clientes aos quais as taxas de premiação se aplicam. |
| [!UICONTROL Direction] | Determina o tipo de transação definido pela taxa de câmbio. Opções: <br/>**[!UICONTROL Points to Currency]**- Define o número de pontos que podem ser aplicados como crédito ao valor de um pedido. No primeiro campo _[!UICONTROL Rate]_, insira o número de pontos. No segundo campo_[!UICONTROL Rate]_, insira o valor monetário dos pontos.<br/>**[!UICONTROL Currency to Points]** - Define a quantidade de um pedido que pode ganhar pontos do cliente. No primeiro campo _[!UICONTROL Rate]_, insira o valor monetário. No segundo campo_[!UICONTROL Rate]_, insira o número de pontos que é representado pelo valor monetário. |
