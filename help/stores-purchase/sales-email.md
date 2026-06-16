---
title: Emails de vendas
description: Saiba como configurar emails de vendas para oferecer suporte a comunicações com clientes sobre seus pedidos.
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
TQID: https://experienceleague.adobe.com/M9-GhmO0XeRC9sgZmQXpv759NN-5cM92Bd8ZxxM96yg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 0%

---

# Emails de vendas

Várias mensagens de email são acionadas pelos eventos relacionados a um pedido e a configuração é semelhante. Identifique o contato da loja que aparece como remetente da mensagem, o modelo de email a ser usado e qualquer outra pessoa que deva receber uma cópia da mensagem. Emails de vendas podem ser enviados quando acionados por um evento ou por um intervalo predeterminado.

![Configuração de vendas - emails de vendas](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## Etapa 1. Atualizar os modelos de email

Atualize o modelo [cabeçalho de email](../systems/email-template-custom.md#header-template) para que ele reflita sua marca e os outros modelos de email conforme necessário. Para obter uma lista completa de modelos, consulte [Modelos de email](../systems/email-templates.md).

## Etapa 2. Escolha o tipo de transmissão

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Sales Emails]**.

1. Se necessário, expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL General Settings]**.

   ![Configuração de vendas - configurações gerais do email de vendas](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Por padrão, o Envio assíncrono está configurado para `Disable`. Para alterar a configuração do sistema, desmarque a caixa de seleção **[!UICONTROL Use system value]** e defina **[!UICONTROL Asynchronous sending]** como uma das seguintes opções:

   - `Disable` - Envia email de vendas quando acionado por um evento.
   - `Enable` - Envia emails de vendas em intervalos regulares predeterminados.

   O Suporte da Adobe Commerce recomenda ativar o envio assíncrono para melhorar o desempenho do posicionamento de pedidos. Consulte [Práticas recomendadas de configuração para processamento de pedidos](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) na Base de Dados de Conhecimento de Suporte da Adobe Commerce.

## Etapa 3. Preencha os detalhes de cada mensagem de email de vendas

1. Se necessário, expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Order]**.

   ![Configuração de vendas - ordem de emails de vendas](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Verifique se **[!UICONTROL Enabled]** está definido como `Yes` (padrão).

1. Defina **[!UICONTROL New Order Confirmation Email]** para o contato de armazenamento que aparece como remetente da mensagem.

1. Defina **[!UICONTROL New Order Confirmation Template]** com o modelo que é usado para o email enviado a clientes registrados.

1. Defina **[!UICONTROL New Order Confirmation Template for Guest]** com o modelo usado para o email enviado aos convidados que não têm uma conta na sua loja.

1. Para **[!UICONTROL Send Order Email Copy To]**, insira o endereço de email de qualquer pessoa que receberá uma cópia do novo email do pedido.

   Se estiver enviando uma cópia para vários destinatários, separe cada endereço com uma vírgula.

1. Defina **[!UICONTROL Send Order Email Copy Method]** como um dos seguintes:

   - `Bcc` - Envia uma _cópia de cortesia oculta_ ao incluir o destinatário no cabeçalho do mesmo email enviado ao cliente. O destinatário CCO não está visível para o cliente.
   - `Separate Email` - Envia a cópia como um email separado.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Order Comments]** e repita essas etapas.

   ![Configuração de vendas - Comentários de pedidos de emails de vendas](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. Conclua a configuração dos tipos de email de vendas restantes:

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

   Quando solicitado, clique no link [Gerenciamento de Cache](../systems/cache-management.md) na mensagem na parte superior do espaço de trabalho e limpe todos os caches inválidos.
