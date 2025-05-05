---
title: Alertas de produto
description: Saiba mais sobre alertas de produtos e como usá-los para notificar os clientes sobre status das ações e alterações de preço dos produtos.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Alertas de produto

Os clientes podem assinar dois tipos de alertas por email - alertas de alteração de preço e alertas no estoque. Para cada tipo de alerta, você pode determinar se os clientes podem se inscrever, selecionar o modelo de email usado e identificar o remetente do email.

![Inscrever-se para obter um alerta de produto](assets/product-alert-setting.png){width="600" zoomable="yes"}

## Alertas de alteração de preço

Quando os alertas de alteração de preço estiverem habilitados, um link _Notifique-me quando o preço cair_ será exibido em cada página do produto. Os clientes podem clicar no link para assinar alertas relacionados ao produto. Os convidados serão solicitados a abrir uma conta em sua loja. Sempre que o preço muda ou o produto fica especial, todos que assinaram o alerta recebem um alerta por email.

## Alertas no estoque

O alerta no estoque cria um link chamado _Notifique-me quando este produto estiver no estoque_ para cada produto indisponível. Os clientes podem clicar no link para assinar o alerta. Quando o produto estiver de volta ao estoque, os clientes receberão uma notificação por email informando que o produto está disponível. Os produtos com alertas têm uma guia _Alertas de Produtos_ no painel Informações do Produto, que lista os clientes que assinaram um alerta.

![Lista de assinaturas de produtos e alertas de preços](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## Configurar alertas do produto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Clique para expandir a seção _[!UICONTROL Product Alerts]_&#x200B;e faça o seguinte:

   ![Alertas de Produtos](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - Para oferecer alertas de alteração de preço aos seus clientes, defina **[!UICONTROL Allow Alert When Product Price Changes]** como `Yes`.

   - Defina **[!UICONTROL Price Alert Email Template]** com o modelo que deseja usar para as notificações de alerta de preço.

   - Para oferecer alertas quando produtos indisponíveis forem disponibilizados novamente, defina **[!UICONTROL Allow Alert When Product Comes Back in Stock]** como `Yes`.

     >[!NOTE]
     >
     >A mensagem _Notificar quando este produto estiver em estoque_ é exibida somente quando **[!UICONTROL Display Out of Stock Products]** estiver definido como `Yes` (na Configuração em [!UICONTROL Catalog] > [!UICONTROL Inventory]).

   - Defina **[!UICONTROL Stock Alert Email Template]** com o modelo que deseja usar para alertas de estoque de produtos.

   - Defina **[!UICONTROL Alert Email Sender]** como o [contato da loja](../getting-started/store-details.md#store-email-addresses){target="_blank"} que você deseja que apareça como remetente do alerta de email. Saiba mais sobre [armazenar endereços de email](../configuration-reference/general/store-email-addresses.md){target="_blank"} no guia do usuário principal.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar modelos de email de alertas do produto

Em seguida, configure, adicione ou modifique o template de email para seu alerta de preço. Talvez você queira editar as configurações de alerta de preço após criar modelos adicionais.

Para obter informações mais detalhadas sobre o uso de mensagens de email, consulte [Modelos de Mensagem](../systems/email-template-custom.md#message-templates) no _Guia de Sistemas de Administração_.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Clique em **[!UICONTROL Add New Template]**.

1. Em _Carregar modelo padrão_, escolha o **[!UICONTROL Template]** que deseja personalizar.

   Você pode escolher o modelo de alerta incluído com o seu tema. Ou você pode selecionar os modelos `Price Alert` ou `Stock Alert` em _[!UICONTROL Magento_PriceAlert]_.

1. Clique em **[!UICONTROL Load Template]**.

1. Insira um **[!UICONTROL Template Name]**.

   Você pode selecionar este nome na configuração _Alertas de Preço_.

1. Leia o conteúdo existente e faça as alterações necessárias para o seguinte:

   | Campo | Descrição |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | Esse texto é exibido na linha de assunto de um email. |
   | [!UICONTROL Template Content] | Esse texto é exibido no conteúdo completo do email enviado. |

1. Para adicionar informações geradas dos dados [!DNL Commerce], use a opção **[!UICONTROL Insert Variable]** para usar uma lista de variáveis disponíveis.

1. Clique em **[!UICONTROL Save Template]**.

## Configurações de execução de alerta do produto

Essas configurações permitem que você selecione com que frequência o [!DNL Commerce] verifica se há alterações que exigem o envio de alertas. Você também pode selecionar o recipient, remetente e modelo para emails enviados se o envio de alertas falhar.

![Configurações de Execução do Alerta do Produto](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Product Alerts Run Settings]**.

1. Para determinar com que frequência os alertas de produto são enviados, defina **[!UICONTROL Frequency]** como uma das seguintes opções:

   - `Daily`
   - `Weekly`
   - `Monthly`

1. Para determinar a hora do dia em que os alertas do produto são enviados, defina **[!UICONTROL Start Time]** como hora, minuto e segundo.

   >[!NOTE]
   >
   >Os alertas de produtos são enviados pelo consumidor &quot;product_alert&quot;.

1. Para **[!UICONTROL Error Email Recipient]**, insira o email da pessoa a ser contatada se ocorrer um erro.

1. Para **[!UICONTROL Error Email Sender]**, selecione a identidade de armazenamento que aparece como remetente da notificação de erro.

1. Defina **[!UICONTROL Error Email Template]** para o modelo de email transacional a ser usado para a notificação de erro.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
