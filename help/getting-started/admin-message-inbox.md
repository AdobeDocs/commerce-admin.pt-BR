---
title: Caixa de entrada de mensagens do administrador
description: Saiba mais sobre a caixa de entrada de mensagens do administrador, que fornece mensagens importantes e úteis do Adobe e do sistema  [!DNL Commerce] .
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Caixa de entrada de mensagens do administrador

Sua loja recebe mensagens do Adobe regularmente. As mensagens são classificadas por importância e podem se referir a atualizações do sistema, patches, novas versões, manutenção programada ou eventos futuros. O ícone de sino no cabeçalho indica o número de mensagens não lidas na sua caixa de entrada.

![Administrador - mensagens de entrada](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

A página _[!UICONTROL Notifications]_&#x200B;lista todas as mensagens classificadas por data. Os comandos&#x200B;_[!UICONTROL Action]_ podem ser usados para marcar mensagens individuais como lidas, exibir informações mais detalhadas ou remover a mensagem da caixa de entrada.

A configuração determina com que frequência a caixa de entrada é atualizada e como as mensagens são entregues. Se o administrador da loja tiver um URL seguro, as notificações deverão ser entregues por HTTPS.

## Exibir novas mensagens de entrada

1. Clique no ícone **[!UICONTROL Notification]** no cabeçalho e leia o resumo.

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

   - Clique no ícone **[!UICONTROL Notification]** no cabeçalho. Se houver uma ou mais novas mensagens exibidas, clique em **[!UICONTROL See All]**.

   - Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. Na coluna **[!UICONTROL Action]**, siga um destes procedimentos:

   - Para obter mais informações, clique em **[!UICONTROL Read Details]** para abrir a página vinculada em uma nova janela.

   - Para manter a mensagem em sua caixa de entrada, clique em **[!UICONTROL Mark As Read]**.

     ![Administrador - Marcar notificações selecionadas como lidas](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - Para excluir a mensagem, clique em **[!UICONTROL Remove]**.

1. Para aplicar uma ação a várias mensagens, siga um destes procedimentos:

   - Marque a caixa de seleção na primeira coluna para cada mensagem a ser gerenciada.
   - Para selecionar várias mensagens, defina o controle **[!UICONTROL Mass Actions]** conforme necessário.

1. Defina o controle **[!UICONTROL Actions]** como um dos seguintes:

   - `Mark as Read`
   - `Remove`

1. Clique em **[!UICONTROL Submit]** para concluir o processo.

## Configurar notificações

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel de navegação esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png)a seção **[!UICONTROL Notifications]**.

   ![Configuração de notificações](./assets/system-notifications.png){width="600"}

1. Se o Administrador do armazenamento executar por uma [URL segura](../stores-purchase/store-urls.md), defina **[!UICONTROL Use HTTPS to Get Feed]** como `Yes`.

1. Defina **[!UICONTROL Update Frequency]** para determinar com que frequência sua caixa de entrada é atualizada.

   O intervalo pode ser de uma a 24 horas.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

Para obter mais informações sobre as opções de configuração do [!UICONTROL System], consulte o [_Guia de Referência de Configuração_](../configuration-reference/advanced/system.md).
