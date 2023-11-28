---
title: Programas de recompensa e fidelidade
description: Saiba mais sobre o sistema de pontos de recompensa que você pode usar para impulsionar o engajamento do cliente e promover a fidelidade do cliente.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 0%

---

# Programas de recompensa e fidelidade

{{ee-feature}}

A variável _pontos de premiação_ no Adobe Commerce oferece a capacidade de implementar programas exclusivos que impulsionam o engajamento do cliente e promovem a fidelidade do cliente. Os pontos podem ser concedidos para uma grande variedade de atividades de transação e cliente, e a configuração pode ser definida para controlar a alocação, o saldo e a expiração de pontos. Os clientes podem resgatar pontos em compras com base na taxa de conversão estabelecida entre os pontos de premiação e a moeda.

## Regras de preço do carrinho de compras

Os pontos podem ser recompensados aos clientes com base em um [regra do carrinho de compras](price-rules-cart.md). Elas podem ser recompensadas como a única ação da regra de preço ou juntamente com um desconto.

## Saldo do cliente

Os saldos de pontos de premiação podem ser gerenciados por usuários administradores por cliente. Se ativado na loja, os clientes também podem visualizar os detalhes do saldo de pontos.

## Resgatar pontos

>[!NOTE]
>
>[Taxas de câmbio de recompensa](reward-exchange-rates.md) A configuração do é necessária para o resgate de pontos de recompensa por clientes e usuários administradores durante o check-out.

Os pontos podem ser resgatados por usuários administradores e clientes (se ativados) durante o check-out. Na seção Método de Pagamento, uma caixa de seleção Usar meus Pontos de Recompensa aparece acima dos métodos de pagamento ativados. Os pontos e a taxa de câmbio monetários disponíveis estão incluídos. Se o saldo disponível for maior que o total geral do pedido, nenhum método de pagamento adicional será necessário. O número de pontos de premiação aplicado ao pedido é exibido com os totais do pedido, subtraídos do total geral, de modo semelhante a cartões de crédito ou presentes de uma loja. Se os pontos de recompensa forem usados junto com o crédito da loja ou um cartão-presente, os pontos de recompensa serão deduzidos primeiro. O cartão de crédito ou de presente da loja será deduzido se o total do pedido for maior que o número resgatável de pontos de premiação.

>[!NOTE]
>
>Os pontos de recompensa não são recomendados para uso com compras de COD, pois o recebimento do pagamento não pode ser confirmado até que o pedido seja faturado.

## Reembolso para pontos de premiação

Os pedidos feitos com pontos de recompensa podem ser reembolsados até o valor resgatado na ordem. No [_Novo Aviso de Crédito_ página](../stores-purchase/credit-memo-create.md), o número de pontos a serem aplicados ao saldo do cliente pode ser inserido. Por padrão, o campo contém o número completo de pontos que foram usados na ordem.

## Habilitar operações de ponto de premiação para seu armazenamento

A configuração de Pontos de recompensa determina como os pontos de recompensa são apresentados na loja e define os parâmetros operacionais básicos.

![Configuração dos clientes — pontos de premiação](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Etapa 1. Configurar os pontos de premiação

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Reward Points]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Reward Points]** e faça o seguinte:

   - Para ativar pontos de premiação, defina **[!UICONTROL Enable Reward Points Functionality]** para `Yes`.

   - Para permitir que os clientes ganhem seus próprios pontos de recompensa, defina **[!UICONTROL Enable Reward Points Functionality on Storefront]** para `Yes`.

   - Para permitir que os clientes vejam um histórico detalhado de suas recompensas, defina **[!UICONTROL Customers May See Reward Point History]** para `Yes`.

1. Para **[!UICONTROL Reward Points Balance Redemption Threshold]**, insira o número de pontos que devem ser acumulados antes de serem resgatados (em branco para não haver um mínimo).

1. Para **[!UICONTROL Cap Reward Points Balance At]**, insira o número máximo de pontos que um cliente pode acumular (em branco para sem limite).

1. Para **[!UICONTROL Reward Points Expire in (days)]**, insira o número de dias antes de os pontos de premiação expirarem (em branco se não houver expiração).

1. Definir **[!UICONTROL Reward Points Expiry Calculation]** a um dos seguintes:

   - `Static` - Determina o tempo de vida restante dos pontos de premiação com base no número de dias definidos na configuração. Se o limite de expiração na configuração for alterado, a data de expiração dos pontos existentes não será alterada.

   - `Dynamic` - Calcula o número restante de dias sempre que o saldo de pontos de premiação aumenta. Se o limite de expiração na configuração for alterado, a expiração de todos os pontos existentes será atualizada adequadamente.

1. Se quiser reembolsar pontos de premiação disponíveis automaticamente, defina **[!UICONTROL Refund Reward Points Automatically]** para `Yes`.

1. Se quiser deduzir pontos de premiação automaticamente, defina **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** para `Yes`.

1. Definir **[!UICONTROL Landing Page]** para a página de conteúdo que explica seu programa de pontos de premiação.

   Atualize a página padrão Pontos de recompensa com suas próprias informações.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Etapa 2. Configurar pontos ganhos para atividades do cliente

Nesta etapa, o número de pontos de premiação que podem ser obtidos para várias atividades de clientes é especificado. Quando os clientes concluírem uma ação que tenha pontos atribuídos, uma mensagem será exibida indicando quantos pontos eles ganharam.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Actions for Acquiring Reward Points by Customer]** seção.

   ![Configuração dos clientes — ações para obter pontos de premiação por cliente](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Para exibir uma mensagem no carrinho de compras que inclua os pontos de recompensa ganhos para a compra e o saldo atual do ponto de recompensa do cliente, defina **[!UICONTROL Purchase]** para `Yes`.

   >[!NOTE]
   >
   >Ganhar pontos de recompensa por seus _primeiro_ pedido, o cliente deve estar registrado _antes_ a transação é capturada pelo método de pagamento. A maioria dos métodos de pagamento poderia ser configurada para capturar transações _automaticamente_ quando o pedido é feito, mas _antes_ o registro da conta do cliente foi concluído.

1. Para **[!UICONTROL Registration]**, insira o número de pontos ganhos ao abrir uma conta de cliente.

1. Para **[!UICONTROL Newsletter Signup]**, insira o número de pontos ganhos por clientes registrados que assinam um boletim informativo.

1. Para **[!UICONTROL Converting Invitation to Customer]**, insira o número de pontos ganhos por um cliente que envia um convite e o recipient abre uma conta de cliente.

   É possível limitar o número de conversões de convites que podem ser usadas para ganhar pontos para o cliente que envia o convite (em branco para sem limite). Para fazer isso, insira um número no campo **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** campo.

1. Para **[!UICONTROL Converting Invitation to Order]**, insira o número de pontos ganhos por um cliente que envia um convite ao recipient que faz um pedido e faz o seguinte:

   - Para **Limite de Quantidade de Conversões de Convite para Ordem**, insira o número de pontos ganhos pelo cliente que envia o convite quando o recipient faz um pedido inicial (em branco para sem limite).

   - Para **[!UICONTROL Invitation Conversion to Order Reward]**, selecione o `Each` opção para ganhar pontos por cada pedido feito pelo recipient ou selecione a `First` opção para ganhar pontos somente no primeiro pedido feito pelo recipient.

1. Para **[!UICONTROL Review Submission]**, insira o número de pontos ganhos por um cliente que envia uma revisão aprovada para publicação.

1. Em seguida, para limitar o número de análises que podem ser usadas para ganhar pontos por cliente, insira o número nas **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** (em branco para sem limite).

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Etapa 3. Concluir as configurações de notificação por email

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Email Notification Settings]** seção.

   ![Configuração dos clientes: notificações por email de pontos de premiação](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Email Sender]** ao contato da loja que aparece como remetente de atualizações de saldo e notificações de expiração.

1. Se quiser assinar clientes por padrão para ser notificado sobre atualizações de saldo e datas de expiração futuras, defina **[!UICONTROL Subscribe Customers by Default]** para `Yes`.

1. Definir **[!UICONTROL Balance Update Email]** ao modelo usado para a notificação que é enviada aos clientes sempre que seu saldo de ponto é atualizado.

1. Definir **[!UICONTROL Reward Points Expiry Warning Email]** ao modelo usado para a notificação enviada aos clientes quando o limite de expiração de um lote de pontos é atingido.

1. Para **[!UICONTROL Expiry Warning Before (days)]**, insira o número de dias antes do vencimento do ponto em que a notificação é enviada.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Atualizar o saldo de pontos de premiação

O saldo de pontos de premiação pode ser atualizado no Administrador.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Localize o cliente na grade e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Em _Informações do cliente_, escolha o **[!UICONTROL Reward Points]** seção.

1. Insira o número de **[!UICONTROL Update Points]**:

   - Para atualizar o valor de pontos de premiação, insira o número para aumentar o saldo total de pontos.
   - Para subtrair o valor de pontos de premiação, insira o número negativo que deseja reduzir o saldo total de pontos.

1. Enter **[!UICONTROL Comments]** de pontos de compensação, se necessário.

   ![Saldo de pontos de premiação](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Como opção, inscreva o cliente em _Notificações de pontos de recompensa_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Clique em **[!UICONTROL Save Customer]**.

Todas as ações relacionadas a pontos de premiação são exibidas no _[!UICONTROL Reward Points History]_em sua conta na loja.

## Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Balance] | Saldo atual de pontos de premiação do cliente |
| [!UICONTROL Amount Balance] | O valor do saldo de caixa atual |
| [!UICONTROL Points] | O número de pontos adicionados ou subtraídos |
| [!UICONTROL Amount] | Valor em dinheiro adicionado ou subtraído |
| [!UICONTROL Rate] | A variável [premiar taxa de câmbio](reward-exchange-rates.md) |
| [!UICONTROL Website] | Site ao qual o histórico de pontos de premiação é atribuído |
| [!UICONTROL Reason] | Motivos para a atribuição de pontos:<br>**[!UICONTROL Making purchases]**— Toda vez que o cliente faz uma compra, ele pode ganhar pontos.<br>**[!UICONTROL Registering on the site]** - Acumulado no registro (uma vez).<br>**[!UICONTROL Subscribing to a newsletter]**- Acumulado pela primeira vez na assinatura (uma vez).<br>**[!UICONTROL Sending Invitations]** — Ganhe pontos convidando seus amigos para ingressar no site.<br>**[!UICONTROL Converting Invitations to Customer]**— Ganhe pontos para cada convite que eles enviam, os principais amigos que se registram no site.<br>**[!UICONTROL Converting Invitations to Order]** — Ganhe pontos por cada venda resultante de um convite enviado.<br>**[!UICONTROL Review Submission]**— ganhe pontos ao enviar análises de produtos. |
| [!UICONTROL Created] | Atualização de data e hora dos pontos de premiação |
| [!UICONTROL Expired] | Número de pontos de premiação expirados |
| [!UICONTROL Comment] | Comentários ao adicionar ou subtrair pontos |

{style="table-layout:auto"}

## Solução de problemas de recursos

Para obter ajuda com a solução de problemas de pontos de premiação, consulte os seguintes artigos da Base de conhecimento de suporte do Commerce:

- [Pontos de fidelidade em ordens parciais](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31295-magento-patch-loyalty-points-on-partial-orders.html)
- [Erro 404 - remoção de pontos de recompensa na finalização de remessa múltipla](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
