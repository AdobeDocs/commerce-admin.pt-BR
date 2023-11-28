---
title: Gerenciar assinantes do informativo
description: Saiba como gerenciar os assinantes do boletim informativo usando uma lista simples de assinaturas ativas.
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Gerenciar assinantes do informativo

Como prática recomendada, você deve gerenciar a lista de assinaturas regularmente e processar todas as solicitações para cancelar a inscrição. Em algumas jurisdições, é exigido por lei que os pedidos de cancelamento de subscrição sejam processados em um período específico.

É possível gerenciar facilmente os assinantes usando uma lista simples de assinaturas ativas. Quando um cliente envia uma solicitação de cancelamento de inscrição, você pode simplesmente aplicar uma _Cancelar inscrição_ para uma ou mais assinaturas selecionadas.

Em configurações de site único com várias exibições de loja, uma assinatura de conta de cliente pode ser associada a uma exibição de loja específica.

Em configurações de várias lojas e vários sites com um [escopo da conta do cliente](../customers/customer-account-scope.md), uma conta de cliente pode assinar boletins informativos para vários sites/lojas. Nesse caso, talvez você queira editar a conta do cliente para gerenciar um grupo de assinaturas ou cancelar uma assinatura para um site/loja específico para atender a uma solicitação.

Se quiser usar um serviço de terceiros para enviar informativos, é possível exportar a lista de assinaturas como um arquivo CSV ou XML.

## Gerenciar assinaturas de um cliente

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Localize o cliente na grade e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Clique em **[!UICONTROL Newsletter]** no painel esquerdo.

1. Modifique as assinaturas do cliente de acordo com a configuração do site/loja.

   Para uma configuração de um único site/loja, basta selecionar ou limpar a variável **[!UICONTROL Subscribed to Newsletter]** caixa de seleção

   ![Caixa de seleção de subscrição de boletim informativo de cliente de loja única](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   Para uma configuração de um único site/várias lojas, você pode selecionar ou limpar a variável **[!UICONTROL Subscribed to Newsletter]** caixa de seleção e definir **[!UICONTROL Subscribed on Store View]** para a exibição de armazenamento correta da assinatura.

   ![Caixa de seleção de subscrição de boletim informativo de cliente de várias lojas e seletor de visualização de loja](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   Para uma configuração de vários sites/várias lojas com um escopo de conta de cliente global, a página exibe o status de assinatura de todos os sites. Você pode selecionar ou limpar a variável **[!UICONTROL Subscribed]** e/ou alterar o **[!UICONTROL Store View]** para a assinatura.

   ![Caixas de seleção de subscrição de boletim informativo de cliente de vários sites e seletores de visualização de loja](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. Clique em **[!UICONTROL Save Customer]**.

## Cancelar uma assinatura na lista de assinantes

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   Para uma configuração de vários sites, em que alguns clientes têm assinaturas para mais de um site, cada assinatura é exibida como um item de linha na grade.

1. Localize o assinante na grade e marque a caixa de seleção na primeira coluna.

   >[!NOTE]
   >
   >Para um cancelamento de subscrição em massa, marque a caixa de seleção de cada assinante que deseja cancelar.

1. Defina o _[!UICONTROL Action]_controle para **[!UICONTROL Unsubscribe]**e clique em **[!UICONTROL Submit]**.

   ![Cancelar assinatura do informativo](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   O status do registro muda para `Unsubscribed`.

## Exportar a lista de assinantes

1. No _[!UICONTROL Newsletter Subscribers]_usar os controles de filtro para incluir somente registros com uma_ Status _de `Subscribed` e para a visualização apropriada do site, loja ou loja.

1. Defina o **[!UICONTROL Export to]** controle para uma das seguintes opções:

   - `CSV`
   - `XML`

1. Clique em **[!UICONTROL Export]** e procure o prompt na parte inferior da tela e salve o arquivo.

   ![Exportar assinantes do informativo](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## Deletar um assinante da lista de assinantes

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. Localize o assinante na grade e marque a caixa de seleção na primeira coluna.

1. Defina o _[!UICONTROL Action]_controle para **[!UICONTROL Delete]**e clique em **[!UICONTROL Submit]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.
