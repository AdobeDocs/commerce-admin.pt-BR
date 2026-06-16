---
title: Solicitação de cotação
description: Saiba como os clientes associados a uma conta de empresa podem enviar uma solicitação de cotação.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
TQID: https://experienceleague.adobe.com/lRPDBgKHCTklbiZ1QWsvXD--n86T-IySJDu9nv-umsU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 0%

---

# Solicitação de cotação

Se as cotações estiverem habilitadas na [Configuração dos recursos de vendas](configure-quotes.md), um comprador autorizado de uma empresa poderá iniciar o processo de negociação de preços solicitando uma cota do carrinho de compras. Se um comprador não estiver pronto para submeter uma cota para negociação, ele poderá salvá-la como uma preliminar.

>[!NOTE]
>
>Uma solicitação de cotação não pode incluir códigos de desconto ou cartões-presente.

## Experiência de solicitação de cotação do cliente

1. O cliente faz logon em sua conta de usuário como comprador com [permissão](account-company-roles-permissions.md) para solicitar uma cotação.

1. Adiciona os produtos a serem incluídos na cotação ao carrinho.

   >[!TIP]
   > 
   >Os clientes podem adicionar uma lista de SKUs de produtos ao carrinho mais rapidamente usando o [Pedido rápido](quick-order.md).

1. Seleciona **[!UICONTROL Request a Quote]**.

   ![Solicitando uma cotação do carrinho de compras](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. Na caixa **[!UICONTROL Add your comment]**, o cliente insere uma breve observação para descrever a solicitação.

1. Insere um **[!UICONTROL Quote Name]**.

   ![Inserindo comentários e o nome da citação](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Se necessário, anexa um documento ou imagem de suporte à cotação:

   - Seleciona **[!UICONTROL Attach file]**.
   - Escolhe o arquivo do sistema.

   Por padrão, um [arquivo anexado](configure-quotes.md) pode ter até 2 MB, em qualquer um dos seguintes formatos de arquivo: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG ou JPEG, PNG.

1. Cria e processa a cotação:

   - Envia a cotação para o Vendedor selecionando **[!UICONTROL Request a Quote]**.
   - Salva a cotação como rascunho selecionando **[!UICONTROL Save as Draft]**.

     Se o comprador salvar a cotação como um rascunho, ela estará disponível em [!UICONTROL My Quotes] no estado `Draft`. Cotações de rascunho não estão visíveis para o Vendedor até que o Comprador as envie para revisão.
