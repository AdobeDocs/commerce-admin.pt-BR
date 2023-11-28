---
title: Caixa de entrada de mensagens do administrador
description: Saiba mais sobre a caixa de entrada de mensagens do administrador, que fornece mensagens importantes e úteis do Adobe e do [!DNL Commerce] sistema.
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Caixa de entrada de mensagens do administrador

Sua loja recebe mensagens do Adobe regularmente. As mensagens são classificadas por importância e podem se referir a atualizações do sistema, patches, novas versões, manutenção programada ou eventos futuros. O ícone de sino no cabeçalho indica o número de mensagens não lidas na sua caixa de entrada.

![Administrador - mensagens de entrada](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

A variável _[!UICONTROL Notifications]_A página lista todas as mensagens classificadas por data. A variável_[!UICONTROL Action]_ os comandos podem ser usados para marcar mensagens individuais como lidas, exibir informações mais detalhadas ou remover a mensagem da caixa de entrada.

A configuração determina com que frequência a caixa de entrada é atualizada e como as mensagens são entregues. Se o administrador da loja tiver um URL seguro, as notificações deverão ser entregues por HTTPS.

## Exibir novas mensagens de entrada

1. Clique em **[!UICONTROL Notification]** no cabeçalho e leia o resumo.

1. Siga um destes procedimentos:

   - Se necessário, clique na mensagem para exibir o texto completo.
   - Para excluir a mensagem, clique no ícone excluir à direita da mensagem.
   - Para exibir a lista completa de Notificações, clique em **[!UICONTROL See All]**.

## Resolver uma mensagem crítica

Para receber uma mensagem de importância crítica, execute um dos procedimentos a seguir:

- Clique em **[!UICONTROL Read Details]**.
- Para descartar a caixa de alerta, mas manter a mensagem ativa, clique em **[!UICONTROL Close]**.

## Administrar as notificações

1. Siga um destes procedimentos para abrir a página Notificações:

   - Clique em **[!UICONTROL Notification]** no cabeçalho. Se uma ou mais mensagens novas forem exibidas, clique em **[!UICONTROL See All]**.

   - No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. No **[!UICONTROL Action]** , siga um destes procedimentos:

   - Para obter mais informações, clique em **[!UICONTROL Read Details]** para abrir a página vinculada em uma nova janela.

   - Para manter a mensagem em sua caixa de entrada, clique em **[!UICONTROL Mark As Read]**.

     ![Administrador - Marcar notificações selecionadas como lidas](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - Para excluir a mensagem, clique em **[!UICONTROL Remove]**.

1. Para aplicar uma ação a várias mensagens, siga um destes procedimentos:

   - Marque a caixa de seleção na primeira coluna para cada mensagem a ser gerenciada.
   - Para selecionar várias mensagens, defina a variável **[!UICONTROL Mass Actions]** controle conforme necessário.

1. Defina o **[!UICONTROL Actions]** controle para uma das seguintes opções:

   - `Mark as Read`
   - `Remove`

1. Clique em **[!UICONTROL Submit]** para concluir o processo.

## Configurar notificações

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel de navegação esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png)o **[!UICONTROL Notifications]** seção.

   ![Configuração de notificações](./assets/system-notifications.png){width="600"}

1. Se o administrador da loja executar em um [URL seguro](../stores-purchase/store-urls.md), definir **[!UICONTROL Use HTTPS to Get Feed]** para `Yes`.

1. Definir **[!UICONTROL Update Frequency]** para determinar com que frequência sua caixa de entrada é atualizada.

   O intervalo pode ser de uma a 24 horas.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

Para obter mais informações sobre o [!UICONTROL System] opções de configuração, consulte a seção [_Guia de referência de configuração_](../configuration-reference/advanced/system.md).
