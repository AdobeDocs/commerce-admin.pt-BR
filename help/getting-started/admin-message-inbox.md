---
title: Caixa de entrada de mensagens do administrador
description: Saiba mais sobre a caixa de entrada de mensagens do administrador, que fornece mensagens importantes e úteis do Adobe e do sistema  [!DNL Commerce] .
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
TQID: https://experienceleague.adobe.com/3RgVAR8efVGsjazQsH8-3Ohfw1h8SDuqLyCDzMYAAng
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 393
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
