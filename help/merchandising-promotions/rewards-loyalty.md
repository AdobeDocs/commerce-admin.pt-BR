---
title: Programas de recompensa e fidelidade
description: Saiba mais sobre o sistema de pontos de recompensa que você pode usar para impulsionar o engajamento do cliente e promover a fidelidade do cliente.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: b0e9087016f7a6ce682e84feb931f7ad870e6420
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 0%

---

# Programas de recompensa e fidelidade

{{ee-feature}}

O sistema de _pontos de premiação_ do Adobe Commerce oferece a capacidade de implementar programas exclusivos que impulsionam o engajamento do cliente e promovem a fidelidade do cliente. Os pontos podem ser concedidos para uma grande variedade de atividades de transação e cliente, e a configuração pode ser definida para controlar a alocação, o saldo e a expiração de pontos. Os clientes podem resgatar pontos em compras com base na taxa de conversão estabelecida entre os pontos de premiação e a moeda.

## Regras de preço do carrinho de compras

Os pontos podem ser recompensados aos clientes com base em uma [regra de carrinho de compras](price-rules-cart.md). Elas podem ser recompensadas como a única ação da regra de preço ou juntamente com um desconto.

## Saldo do cliente

Os saldos de pontos de premiação podem ser gerenciados por usuários administradores por cliente. Se ativado na loja, os clientes também podem visualizar os detalhes do saldo de pontos.

## Resgatar pontos

>[!NOTE]
>
>A configuração [Taxas de Câmbio de Recompensa](reward-exchange-rates.md) é necessária para o resgate de pontos de recompensa por clientes e usuários administradores durante o check-out.

Os pontos podem ser resgatados por usuários administradores e clientes (se ativados) durante o check-out. Na seção Método de Pagamento, uma caixa de seleção Usar meus Pontos de Recompensa aparece acima dos métodos de pagamento ativados. Os pontos e a taxa de câmbio monetários disponíveis estão incluídos. Se o saldo disponível for maior que o total geral do pedido, nenhum método de pagamento adicional será necessário. O número de pontos de premiação aplicado ao pedido é exibido com os totais do pedido, subtraídos do total geral, de modo semelhante a cartões de crédito ou presentes de uma loja. Se os pontos de recompensa forem usados junto com o crédito da loja ou um cartão-presente, os pontos de recompensa serão deduzidos primeiro. O cartão de crédito ou de presente da loja será deduzido se o total do pedido for maior que o número resgatável de pontos de premiação.

>[!NOTE]
>
>Os pontos de recompensa e o crédito de armazenamento não reduzem a base tributável do pedido. O imposto é calculado sobre o subtotal antes da aplicação desses descontos. Os pontos ou crédito só reduzem o valor final que o cliente paga.

>[!NOTE]
>
>Os pontos de recompensa não são recomendados para uso com compras de COD, pois o recebimento do pagamento não pode ser confirmado até que o pedido seja faturado.

## Reembolso para pontos de premiação

Os pedidos feitos com pontos de recompensa podem ser reembolsados até o valor resgatado na ordem. Na página [_Novo Aviso de Crédito_](../stores-purchase/credit-memo-create.md), o número de pontos a serem aplicados ao saldo do cliente pode ser inserido. Por padrão, o campo contém o número completo de pontos que foram usados na ordem.

## Habilitar operações de ponto de premiação para seu armazenamento

A configuração de Pontos de recompensa determina como os pontos de recompensa são apresentados na loja e define os parâmetros operacionais básicos.

![Configuração de clientes - pontos de premiação](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Etapa 1. Configurar os pontos de premiação

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Reward Points]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Reward Points]** e faça o seguinte:

   - Para ativar pontos de premiação, defina **[!UICONTROL Enable Reward Points Functionality]** como `Yes`.

   - Para permitir que os clientes ganhem seus próprios pontos de premiação, defina **[!UICONTROL Enable Reward Points Functionality on Storefront]** como `Yes`.

   - Para permitir que os clientes vejam um histórico detalhado de suas recompensas, defina **[!UICONTROL Customers May See Reward Point History]** como `Yes`.

1. Para **[!UICONTROL Reward Points Balance Redemption Threshold]**, insira o número de pontos que devem ser acumulados antes de serem resgatados (em branco para não haver um mínimo).

1. Para **[!UICONTROL Cap Reward Points Balance At]**, insira o número máximo de pontos que um cliente pode acumular (em branco para sem limite).

1. Para **[!UICONTROL Reward Points Expire in (days)]**, insira o número de dias antes dos pontos de premiação expirarem (em branco para sem expiração).

1. Defina **[!UICONTROL Reward Points Expiry Calculation]** como um dos seguintes:

   - `Static` - Determina a duração restante dos pontos de premiação com base no número de dias definido na configuração. Se o limite de expiração na configuração for alterado, a data de expiração dos pontos existentes não será alterada.

   - `Dynamic` - Calcula o número restante de dias sempre que o saldo de pontos de premiação aumenta. Se o limite de expiração na configuração for alterado, a expiração de todos os pontos existentes será atualizada adequadamente.

1. Se quiser reembolsar automaticamente os pontos de premiação disponíveis, defina **[!UICONTROL Refund Reward Points Automatically]** como `Yes`.

1. Para anular pontos de premiação ganhos através de compras quando a ordem que obteve os pontos for total ou parcialmente reembolsada, defina **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** como `Yes`.

   >[!NOTE]
   >
   >Somente os pontos ganhos com o pedido que está sendo reembolsado são afetados.

1. Defina **[!UICONTROL Landing Page]** para a página de conteúdo que explica seu programa de pontos de premiação.

   Atualize a página padrão Pontos de recompensa com suas próprias informações.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Etapa 2. Configurar pontos ganhos para atividades do cliente

Nesta etapa, o número de pontos de premiação que podem ser obtidos para várias atividades de clientes é especificado. Quando os clientes concluírem uma ação que tenha pontos atribuídos, uma mensagem será exibida indicando quantos pontos eles ganharam.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Actions for Acquiring Reward Points by Customer]**.

   ![Configuração dos clientes - ações para adquirir pontos de premiação por cliente](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Para permitir que pontos de premiação sejam ganhos para as compras baseadas nas [Taxas de Câmbio de Recompensa](reward-exchange-rates.md) configuradas, defina **[!UICONTROL Purchase]** como `Yes`.

   >[!NOTE]
   >
   >Para ganhar pontos de premiação pelo seu pedido _first_, o cliente deve ser registrado _antes_ de a transação ser capturada pelo método de pagamento. A maioria dos métodos de pagamento poderia ser configurada para capturar transações _automaticamente_ quando o pedido é feito, mas _antes_ o registro da conta do cliente foi concluído.

1. Para **[!UICONTROL Registration]**, insira o número de pontos obtidos para abrir uma conta de cliente.

1. Para **[!UICONTROL Newsletter Signup]**, insira o número de pontos obtidos por clientes registrados que assinam um boletim informativo.

1. Para **[!UICONTROL Converting Invitation to Customer]**, insira o número de pontos ganhos por um cliente que envia um convite e o destinatário abre uma conta de cliente.

   É possível limitar o número de conversões de convites que podem ser usadas para ganhar pontos para o cliente que envia o convite (em branco para sem limite). Para fazer isso, insira um número no campo **[!UICONTROL Invitation to Customer Conversions Quantity Limit]**.

1. Para **[!UICONTROL Converting Invitation to Order]**, insira o número de pontos obtidos por um cliente que envia um convite ao destinatário que faz um pedido e faz o seguinte:

   - Para o **Limite de Quantidade de Conversões de Convite para Pedido**, insira o número de pontos ganhos pelo cliente que envia o convite quando o destinatário faz um pedido inicial (em branco para sem limite).

   - Para **[!UICONTROL Invitation Conversion to Order Reward]**, selecione a opção `Each` para ganhar pontos para cada pedido feito pelo destinatário, ou selecione a opção `First` para ganhar pontos somente para o primeiro pedido feito pelo destinatário.

1. Para **[!UICONTROL Review Submission]**, insira o número de pontos obtidos por um cliente que envia uma revisão aprovada para publicação.

1. Em seguida, para limitar o número de análises que podem ser usadas para ganhar pontos por cliente, insira o número no campo **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** (em branco para sem limite).

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Etapa 3. Concluir as configurações de notificação por email

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Email Notification Settings]**.

   ![Configuração de clientes - notificações por email de pontos de premiação](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Email Sender]** para o contato de armazenamento que aparece como remetente de atualizações de saldo e notificações de expiração.

1. Se quiser assinar clientes por padrão para ser notificado sobre atualizações de saldo e datas de vencimento futuras, defina **[!UICONTROL Subscribe Customers by Default]** como `Yes`.

1. Defina **[!UICONTROL Balance Update Email]** para o modelo usado para a notificação que é enviada aos clientes sempre que o saldo de pontos for atualizado.

1. Defina **[!UICONTROL Reward Points Expiry Warning Email]** com o modelo usado para a notificação que é enviada aos clientes quando o limite de expiração de um lote de pontos é atingido.

1. Para **[!UICONTROL Expiry Warning Before (days)]**, insira o número de dias antes do vencimento dos pontos em que a notificação é enviada.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Atualizar o saldo de pontos de premiação

O saldo de pontos de premiação pode ser atualizado no Administrador.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Encontre o cliente na grade e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Em _Informações do Cliente_, escolha a seção **[!UICONTROL Reward Points]**.

1. Digite o número de **[!UICONTROL Update Points]**:

   - Para atualizar o valor de pontos de premiação, insira o número para aumentar o saldo total de pontos.
   - Para subtrair o valor de pontos de premiação, insira o número negativo que deseja reduzir o saldo total de pontos.

1. Insira **[!UICONTROL Comments]** relacionado ao ajuste de pontos de premiação, se necessário.

   ![Saldo de pontos de premiação](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Opcionalmente, inscreva o cliente nas _Notificações de Pontos de Recompensa_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Clique em **[!UICONTROL Save Customer]**.

Todas as ações relacionadas a pontos de premiação são exibidas no bloco _[!UICONTROL Reward Points History]_do cliente em sua conta na loja.

## Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Balance] | Saldo atual de pontos de premiação do cliente |
| [!UICONTROL Amount Balance] | O valor do saldo de caixa atual |
| [!UICONTROL Points] | O número de pontos adicionados ou subtraídos |
| [!UICONTROL Amount] | Valor em dinheiro adicionado ou subtraído |
| [!UICONTROL Rate] | A [taxa de câmbio de recompensa](reward-exchange-rates.md) |
| [!UICONTROL Website] | Site ao qual o histórico de pontos de premiação é atribuído |
| [!UICONTROL Reason] | Motivos para atribuir pontos:<br>**[!UICONTROL Making purchases]**— Toda vez que o cliente faz uma compra, ele pode ganhar pontos.<br>**[!UICONTROL Registering on the site]** - Acumulado no registro (uma vez).<br>**[!UICONTROL Subscribing to a newsletter]**- Acumulado na primeira assinatura (uma vez).<br>**[!UICONTROL Sending Invitations]** — Ganhe pontos convidando seus amigos para ingressar no site.<br>**[!UICONTROL Converting Invitations to Customer]**— Ganhe pontos para cada convite que eles enviarem, fazendo com que os principais amigos se registrem no site.<br>**[!UICONTROL Converting Invitations to Order]** — Ganhe pontos em cada venda resultante de um convite enviado.<br>**[!UICONTROL Review Submission]**— Ganhe pontos ao enviar análises de produtos. |
| [!UICONTROL Created] | Atualização de data e hora dos pontos de premiação |
| [!UICONTROL Expired] | Número de pontos de premiação expirados |
| [!UICONTROL Comment] | Comentários ao adicionar ou subtrair pontos |

{style="table-layout:auto"}

