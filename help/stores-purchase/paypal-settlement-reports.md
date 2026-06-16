---
title: Relatório de liquidação do PayPal
description: Saiba mais sobre o relatório de Liquidação do PayPal como uma ferramenta para gerenciar transações do PayPal.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/c7v5oSsVPmD6r6obfGEoxPiGkMI4KMWAmfJAW0-CCJk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 0%

---

# Relatório de liquidação do PayPal

O relatório Liquidação do PayPal fornece aos comerciantes as informações sobre cada transação que afeta a liquidação de fundos.

>[!NOTE]
>
>Antes de gerar relatórios de liquidação, o administrador da loja deve solicitar que os Serviços Técnicos de Comerciante do PayPal criem uma conta de usuário SFTP, habilitem a geração de relatórios de liquidação e habilitem o SFTP em sua conta comercial do PayPal.

Depois de configurar e ativar os relatórios de liquidação na conta de comerciante do PayPal, o Adobe Commerce e o Magento Open Source começarão a gerar relatórios durante as 24 horas seguintes. A lista de relatórios de liquidação disponíveis pode ser visualizada no Admin.

**_Para exibir relatórios de liquidação:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![Relatórios de Liquidação do PayPal](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Para obter as atualizações mais recentes, clique em **[!UICONTROL Fetch Updates]** no canto superior direito.

   O sistema se conecta ao servidor SFTP do PayPal para buscar os relatórios. Quando o processo estiver concluído, uma mensagem será exibida com o número de relatórios obtidos. O relatório inclui as seguintes informações para cada transação:

   | Coluna de relatório | Descrição |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | Um dos seguintes códigos de referência:<br/>- ID da Ordem<br/>- ID da Transação<br/>- ID da Assinatura |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - O texto inserido pelo comerciante na transação no PayPal.<br/>**[!UICONTROL Transaction Debit or Credit]**- A direção da movimentação de dinheiro do valor bruto.<br/>**[!UICONTROL Fee Debit or Credit]** - A direção do movimento do dinheiro por taxa. |

   {style="table-layout:auto"}
