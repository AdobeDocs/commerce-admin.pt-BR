---
title: Configurar cotações
description: Saiba mais sobre a configuração da cotação, que controla o valor mínimo necessário do pedido para solicitações de cotação, o tempo de vida da cotação e os anexos de arquivo.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
TQID: https://experienceleague.adobe.com/RenH7-cnfF8qVEqFQc7IPMVsIp0alug5OgvYlr5piTM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# Configurar cotações

Se as cotações estiverem habilitadas nos [recursos B2B](enable-basic-features.md) gerais, você poderá configurar o suporte para cotações no Administrador. A configuração da cotação determina o valor mínimo exigido do pedido para solicitações de cotação, o tempo de vida da cotação e os formatos de arquivo compatíveis para arquivos anexados.

>[!NOTE]
>
>As opções de configuração de cotas e a capacidade de usar funções de negociação de cotas são controladas usando os [recursos de função](../systems/permissions-user-roles.md#role-resources). Esses recursos de função devem ser selecionados para a função de usuário Administrador atribuída à conta de usuário Administrador. Para conceder acesso às funções de cotação no Administrador, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, selecione a função e navegue até [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] na árvore_ Recursos de Função _.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Quotes]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL General]** e faça o seguinte:

   ![Configuração de cotações de venda - geral](./assets/quotes-general.png){width="700" zoomable="yes"}

   Consulte [Quotes](../configuration-reference/sales/quotes.md) na _Referência de Configuração_ para obter uma lista completa das opções de recursos de Cotas e suas funções.

   - Insira o **[!UICONTROL Minimum Amount]** no carrinho de compras que deve ser atendido antes do envio de uma solicitação de cotação.

   - Para **[!UICONTROL Minimum Amount Message]**, insira a mensagem que você deseja exibir quando o total do carrinho de compras não atingir a quantidade mínima necessária.

   - Para **[!UICONTROL Default Expiration Period]**, insira o número de **[!UICONTROL days]**, **[!UICONTROL weeks]** ou **[!UICONTROL months]** que uma aspa deve permanecer válida.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Attached files]** e faça o seguinte:

   - Para **[!UICONTROL File formats for upload]**, insira o sufixo de cada tipo de arquivo que você aceita para arquivos anexados a aspas.

     Insira cada sufixo de arquivo em minúsculas e separado por vírgula.

     Por padrão, os seguintes formatos têm suporte: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` e `jpeg`

   - Para **[!UICONTROL Maximum file size]**, insira o tamanho máximo de um arquivo anexado em megabytes.

     O valor inserido pode ser substituído pela configuração do servidor.

     ![Configuração de cotações de venda - arquivos anexados](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
