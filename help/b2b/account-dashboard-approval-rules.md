---
title: Regras de aprovação de ordem de compra
description: Saiba mais sobre as regras de aprovação de ordem de compra e como os administradores da empresa podem defini-las na loja.
exl-id: e8d8bbc9-41cf-4024-85cc-92f0b0ce32d6
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Regras de aprovação de ordem de compra

A maioria das empresas exige aprovação de pedidos para pedidos de compra. Ao adicionar regras de aprovação para a conta da empresa, é possível controlar quem pode criar ordens de compra e quanto pode gastar. Por exemplo:

* Qualquer OC menor que o valor X é automaticamente aprovada.
* OCs acima do valor X, mas menor que Q, devem ser aprovadas por Y.
* Qualquer OC acima do valor X deve ser aprovada por Y e Z.
* Uma OC criada por qualquer pessoa no nível da Director ou superior é automaticamente aprovada.

Dependendo da função e das permissões da empresa, os usuários podem criar, editar, excluir ou exibir regras de aprovação.

>[!IMPORTANT]
>
>A configuração da regra de aprovação requer uma configuração [estrutura da empresa](account-company-structure.md) para especificar a aprovação do gerente do cliente comprador.

## Métodos de pagamento

Os fluxos de aprovação de ordem de compra oferecem suporte aos métodos de pagamento online e offline. Todos os métodos de pagamento off-line padrão são suportados para aprovações de ordens de compra. Para pagamentos on-line, os seguintes métodos são compatíveis:

* PayPal Express
* pagamentos Braintree


## Configuração da regra de aprovação

Com o necessário [permissões para suas funções](account-company-roles-permissions.md), os clientes B2B podem configurar regras de aprovação para aplicar as políticas da empresa clicando em **[!UICONTROL Approval Rules]** no painel esquerdo para a conta do cliente.

![Regras de aprovação da empresa](./assets/approval-rules.png){width="700" zoomable="yes"}

Para criar uma regra de aprovação, um cliente conclui as seguintes etapas:

1. Cliques **[!UICONTROL Add New Rule]** para criar uma regra.

1. Se necessário, altera a regra de **[!UICONTROL Enabled]** para **[!UICONTROL Disabled]**.

   A regra é ativada como o padrão, mas um cliente pode criar a regra usando uma configuração desativada e depois ativá-la quando estiver pronto para aplicá-la.

1. Para **[!UICONTROL Rule name]**, insere um nome curto, mas descritivo, para a Regra, como `Orders less than $100`.

   Rule names must be unique.

1. Para **[!UICONTROL Description]**, insere uma explicação mais longa da regra.

1. Para **[!UICONTROL Applies to]**, escolhe uma ou mais funções de empresa usadas para aplicar a regra.

1. Escolhe o **[!UICONTROL Rule Type]** e define a regra.

   As seções a seguir fornecem uma explicação detalhada e um exemplo para cada tipo de regra.

   ![Criação de uma nova regra de aprovação](./assets/approval-rules-create.png){width="700" zoomable="yes"}

1. Para **[!UICONTROL Requires approval from]**, escolhe um ou mais aprovadores necessários de acordo com o tipo de aprovação.

   >[!NOTE]
   >
   >* Ao atribuir uma função como aprovador, verifique se há pelo menos um usuário nessa função.
   >* Se houver dois ou mais usuários com a mesma função de aprovador, o criador da ordem de compra não poderá aprová-la. Nesse caso, a aprovação manual é exigida por qualquer outro usuário com essa função de aprovador. No entanto, se `Auto-approve POs created within this role` estiver definida na caixa [Permissões de função](account-company-roles-permissions.md), a ordem de compra é aprovada automaticamente.
   >* Se houver apenas um usuário com a função de aprovador e esse usuário for o criador, a ordem de compra será sempre aprovada automaticamente - o `Auto-approve POs created within this role` configuração de permissão é ignorada.

1. Clique em **[!UICONTROL Save]**.

### [!UICONTROL Order Total]

Esse tipo de regra é usado para exigir uma aprovação de OC com base no total do pedido, incluindo o imposto.

1. Escolhe um **[!UICONTROL Order Total amount]** opção:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. Seleciona o tipo de moeda e insere o valor.

![Regra de aprovação total do pedido](./assets/approval-rules-order-total.png){width="600" zoomable="yes"}

### [!UICONTROL Shipping Cost]

Esse tipo de regra é usado para exigir uma aprovação de OC com base no custo de envio, que muitas empresas exigem.

1. Define o **[!UICONTROL Shipping cost value]**:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. Define a quantidade de remessa desejada.

![Regra de Aprovação de Custo de Remessa](./assets/approval-rules-shipping-cost.png){width="600" zoomable="yes"}

### [!UICONTROL Number of SKUs]

Esse tipo de regra é usado para exigir uma aprovação de OC com base no número de SKUs ou produtos exclusivos no pedido. Ele controla o número de tipos de item distintos, não o número de itens sendo solicitados. Por exemplo, uma OC pode incluir:

* Duas camisas brancas grandes
* Três camisas brancas médias

Este exemplo especifica cinco itens, mas duas SKUs distintas.

1. Define o **[!UICONTROL Number of SKUs]** valor:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. Define a quantidade de SKUs.

![Número de regras de aprovação de SKUs](./assets/approval-rules-number-skus.png){width="600" zoomable="yes"}

## Editar regras de aprovação

Para modificar uma regra de aprovação existente, um cliente pode concluir as seguintes etapas:

1. Na barra lateral da conta, o cliente seleciona **[!UICONTROL Approval Rules]**.

1. Localiza a entrada da regra de aprovação a ser editada.

1. Cliques **[!UICONTROL Edit]**.

1. Faz todas as alterações e cliques necessários **[!UICONTROL Save]**.

## Excluir regras de aprovação

Para remover uma regra de aprovação existente, um cliente pode concluir as seguintes etapas:

1. Na barra lateral da conta, o seleciona **[!UICONTROL Approval Rules]**.

1. Localiza a entrada de regra de aprovação a ser excluída.

1. Cliques **[!UICONTROL Delete]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

## Demonstração de aprovações de ordem de compra

Assista a este vídeo para saber mais sobre aprovações de ordens de compra:

>[!VIDEO](https://video.tv.adobe.com/v/344450?quality=12)
