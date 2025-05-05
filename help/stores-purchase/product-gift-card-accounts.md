---
title: Contas de cartão-presente
description: Saiba mais sobre contas de cartão-presente e como definir as configurações padrão para o gerenciamento de pool de códigos.
exl-id: f8caff04-38fd-4195-ab11-77dae900976d
feature: Products, Gift, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 0%

---

# Contas de cartão-presente

Uma conta de cartão-presente é criada automaticamente para cada cartão-presente comprado. O valor do vale-presente pode então ser aplicado para a compra de um produto em sua loja. Você também pode criar contas de cartão-presente do Administrador como uma promoção ou serviço para clientes. O número da conta do cartão-presente corresponde ao código do cartão-presente.

![Contas de Vale-presente](./assets/marketing-gift-card-accounts-grid.png){width="700" zoomable="yes"}

## Configurar contas de cartão-presente

A configuração de cartão-presente estabelece as configurações padrão para todos os cartões-presente para a exibição de loja e gerencia o conjunto de códigos. O conjunto de códigos é um conjunto de códigos de cartão-presente exclusivos em um formato específico. Os códigos do grupo são usados sempre que uma conta de cartão-presente é criada. É responsabilidade do administrador da loja garantir que haja códigos suficientes disponíveis para vendas de cartão-presente. Certifique-se de gerar um conjunto de códigos antes de oferecer cartões-presente para venda. Por padrão, o Adobe Commerce gera 1.000 códigos. Um novo grupo de códigos não é gerado até que não haja mais códigos disponíveis no grupo atual.

### Etapa 1: configurar notificações por email

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Gift Cards]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Gift Card Email Settings]_&#x200B;e faça o seguinte:

   - Defina **[!UICONTROL Gift Card Notification Email Sender]** para a identidade da loja que aparece como remetente de notificações de cartão-presente.

   - Defina **[!UICONTROL Gift Card Notification Email Template]** para o modelo usado para a notificação.

   ![Configurações de email de cartão-presente](../configuration-reference/sales/assets/gift-cards-gift-card-email-settings.png){width="600" zoomable="yes"}

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Email Sent from Gift Card Account Management]_&#x200B;e faça o seguinte:

   - Defina **[!UICONTROL Gift Card Email Sender]** para que a identidade da loja apareça como o remetente dos cartões-presente.

   - Defina **[!UICONTROL Gift Card Template]** com o modelo que deseja usar para o cartão-presente.

Consulte [Armazenar endereços de email](../configuration-reference/general/store-email-addresses.md) para obter campos e opções de configuração específicos.

### Etapa 2: concluir as configurações gerais

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Gift Card General Settings]_.

1. Para permitir que o cliente troque o valor do cartão por dinheiro, defina **[!UICONTROL Redeemable]** como `Yes`.

1. Para **[!UICONTROL Lifetime (days)]**, insira o número de dias antes do cartão expirar.

   Se não houver data de expiração, deixe o campo em branco.

   >[!NOTE]
   >
   >Dependendo da sua localização, pode ser ilegal que cartões-presente expirem. Verifique suas leis locais antes de definir uma vida útil para seus cartões-presente.

1. Para dar aos clientes a opção de inserir uma mensagem para acompanhar o cartão-presente, defina **[!UICONTROL Allow Gift Message]** como `Yes` e insira o número de caracteres disponíveis para a mensagem para **[!UICONTROL Gift Message Maximum Length]**.

1. Defina **[!UICONTROL Generate Gift Card Account when Orders Item is]** como um dos seguintes:

   - `Ordered` - A conta do cartão-presente é criada quando o pedido é feito.
   - `Invoiced` - A conta do cartão-presente é criada depois que o pagamento é capturado e o pedido é faturado.

   ![Configurações Gerais do Cartão-Presente](../configuration-reference/sales/assets/gift-cards-gift-card-general-settings.png){width="600" zoomable="yes"}

### Etapa 3: estabelecer o conjunto de códigos de cartão-presente

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Gift Card Account General Settings]_&#x200B;e faça o seguinte:

   ![Configurações Gerais da Conta de Cartão-Presente](../configuration-reference/sales/assets/gift-cards-gift-card-account-general-settings.png){width="600" zoomable="yes"}

   - Para personalizar o código, conclua o seguinte de acordo com sua preferência:

      - Comprimento do código
      - Formato do código
      - Prefixo do código
      - Sufixo do código
      - Traço a cada X caracteres

   - Para determinar o número de códigos a serem gerados, insira o **[!UICONTROL New Pool Size]**.

   - Para especificar quando você recebe uma notificação para reabastecer o pool de códigos, insira o **[!UICONTROL Low Code Pool Threshold]**.

1. Antes de gerar o pool de códigos, clique em **[!UICONTROL Save Config]**.

1. Clique em **[!UICONTROL Generate]**.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Revisar uma conta existente de cartão-presente

1. Para localizar o número da conta de cartão-presente de uma ordem atual, faça o seguinte:

   - Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

   - Localize a ordem na lista e clique em **[!UICONTROL View]** na coluna _[!UICONTROL Action]_.

   - Role até a seção _[!UICONTROL Items Ordered]_.

   O número está na coluna _[!UICONTROL Product]_, em **[!UICONTROL Gift Card Accounts]**.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. Localize a conta de cartão-presente na grade e abra-a no modo de edição.

   O código do cartão-presente aparece na parte superior da seção _Informações_.

   ![Informações da Conta do Cartão-presente](./assets/gift-card-account-information.png){width="600" zoomable="yes"}

## Criar uma conta de cartão-presente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. No canto superior direito, clique em **[!UICONTROL Add Gift Card Account]**.

1. Na seção _[!UICONTROL Information]_, defina **[!UICONTROL Active]**&#x200B;como `Yes` e faça o seguinte:

   - Para tornar o saldo do cartão resgatável no check-out ou transferido para o crédito da loja do cliente, defina **[!UICONTROL Redeemable]** como `Yes`.

   - Escolha o **[!UICONTROL Website]** onde a conta do cartão-presente pode ser usada.

   - Insira o **[!UICONTROL Balance]** inicial no cartão-presente.

   - _(Opcional)_ Para definir um **[!UICONTROL Expiration Date]** para o cartão-presente, selecione a data no ![ícone de Calendário](../assets/icon-calendar.png) do calendário.

     Se deixado em branco, a conta do cartão-presente não expirará.

     ![Nova Conta](./assets/gift-card-account-add-new.png){width="600" zoomable="yes"}

1. No painel esquerdo, escolha **[!UICONTROL Send Gift Card]** e faça o seguinte:

   - Digite o endereço **[!UICONTROL Recipient Email]**.

   - Insira o **[!UICONTROL Recipient Name]**.

   - Defina **[!UICONTROL Send Email from the Following Store View]** para a exibição de armazenamento que aparece como remetente da notificação de cartão-presente.

   ![Enviar Configurações De Cartão-Presente](./assets/marketing-gift-card-accounts-new-send.png){width="600" zoomable="yes"}

1. Siga um destes procedimentos para salvar a nova conta:

   - Se você não estiver pronto para enviar o cartão-presente, clique em **[!UICONTROL Save]**.

   - Para salvar as alterações e enviar o cartão-presente por email para o destinatário, clique em **Salvar e Enviar Email**.

## Exibir histórico de conta de cartão-presente

1. Vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. Abra o cartão-presente no modo de edição.

1. O **[!UICONTROL History]** do cartão-presente é exibido.

   ![Histórico do Cartão-Presente](./assets/gift-card-history.png){width="600" zoomable="yes"}

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL ID] | Um número de ação exclusivo com cartão-presente. |
| [!UICONTROL Date] | Data da ação. |
| [!UICONTROL Action] | Determina todas as ações possíveis com um cartão-presente. Opções: `Created` / `Updated` / `Sent` / `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance Change] | Exibe o valor pelo qual o saldo do cartão-presente foi alterado. |
| [!UICONTROL Balance] | Indica o saldo disponível. |
| [!UICONTROL More Information] | Exibe informações sobre quem alterou o saldo do cartão-presente. |

{style="table-layout:auto"}

## Excluir uma conta de cartão-presente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. Selecione a conta de cartão-presente a ser excluída e abra-a no modo de edição.

1. Na barra de menus, clique em **[!UICONTROL Delete]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

## Descrições da coluna

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL ID] | Um identificador numérico exclusivo que é atribuído à conta de cartão-presente. |
| [!UICONTROL Code] | O código que deve ser inserido para aplicar um cartão-presente. |
| [!UICONTROL Website] | Indica os sites nos quais a conta de cartão-presente está disponível. |
| [!UICONTROL Created] | Data de criação. |
| [!UICONTROL End] | Data de expiração do cartão-presente, se programada. |
| [!UICONTROL Active] | Determina se o cartão-presente está ativo. |
| [!UICONTROL Status] | Determina se o cartão-presente é resgatado na conta do cliente ou se está disponível. Opções: `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance] | Indica o saldo disponível. |

{style="table-layout:auto"}
