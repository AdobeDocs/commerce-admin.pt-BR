---
title: Configurar cotações
description: Saiba mais sobre a configuração da cotação, que controla o valor mínimo necessário do pedido para solicitações de cotação, o tempo de vida da cotação e os anexos de arquivo.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Configurar cotações

Se as cotas estiverem ativadas no modo [Recursos B2B](enable-basic-features.md), é possível configurar o suporte a cotações no Administrador. A configuração da cotação determina o valor mínimo exigido do pedido para solicitações de cotação, o tempo de vida da cotação e os formatos de arquivo compatíveis para arquivos anexados.

>[!NOTE]
>
>As opções de configuração de cota e a capacidade de usar funções de negociação de cota são controladas usando o [recursos da função](../systems/permissions-user-roles.md#role-resources). Esses recursos de função devem ser selecionados para a função de usuário Administrador atribuída à conta de usuário Administrador. Para conceder acesso a funções de cotação no Administrador, acesse **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, selecione a função e navegue até [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] no_ Recursos da função _árvore.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Quotes]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL General]** e faça o seguinte:

   ![Configuração de cotações de venda - geral](./assets/quotes-general.png){width="700" zoomable="yes"}

   Consulte [Aspas](../configuration-reference/sales/quotes.md) no _Referência de configuração_ para obter uma lista completa das opções de recursos de Cotações e suas funções.

   - Insira o **[!UICONTROL Minimum Amount]** no carrinho de compras que deve ser atendida antes de uma solicitação de cotação ser enviada.

   - Para **[!UICONTROL Minimum Amount Message]**, insira a mensagem que deseja exibir quando o total do carrinho de compras não atingir o valor mínimo necessário.

   - Para **[!UICONTROL Default Expiration Period]**, insira o número de **[!UICONTROL days]**, **[!UICONTROL weeks]** ou **[!UICONTROL months]** que uma cotação deve permanecer válida.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Attached files]** e faça o seguinte:

   - Para **[!UICONTROL File formats for upload]**, insira o sufixo de cada tipo de arquivo que você aceita para arquivos anexados a aspas.

     Insira cada sufixo de arquivo em minúsculas e separado por vírgula.

     Por padrão, os seguintes formatos são compatíveis: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, e `jpeg`

   - Para **[!UICONTROL Maximum file size]**, insira o tamanho máximo de um arquivo anexado em megabytes.

     O valor inserido pode ser substituído pela configuração do servidor.

     ![Configuração de cotações de venda - arquivos anexados](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
