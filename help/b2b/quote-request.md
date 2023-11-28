---
title: Solicitação de cotação
description: Saiba como os clientes associados a uma conta de empresa podem enviar uma solicitação de cotação.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: 21361104fa06425df0b44d5c7ae204ef4d9e21ac
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Solicitação de cotação

Se as cotas estiverem ativadas na variável [Configuração de recursos de vendas](configure-quotes.md), um comprador autorizado de uma empresa pode iniciar o processo de negociação de preços solicitando uma cotação do carrinho de compras. Se um comprador não estiver pronto para submeter uma cota para negociação, ele poderá salvá-la como uma preliminar.

>[!NOTE]
>
>Uma solicitação de cotação não pode incluir códigos de desconto ou cartões-presente.

## Experiência de solicitação de cotação do cliente

1. O cliente faz logon na conta de usuário como comprador com [permissão](account-company-roles-permissions.md) para solicitar uma cotação.

1. Adiciona os produtos que eles desejam incluir na cotação ao carrinho de compras.

1. Seleciona **[!UICONTROL Request a Quote]**.

   ![Solicitando uma cotação do carrinho de compras](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. No **[!UICONTROL Add your comment]** insira uma breve nota que descreva a solicitação.

1. Insere um **[!UICONTROL Quote Name]**.

   ![Inserção dos comentários e do nome da cotação](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Se necessário, anexa um documento ou imagem de suporte à cotação:

   - Seleciona **[!UICONTROL Attach file]**.
   - Escolhe o arquivo do sistema.

   Por padrão, uma variável [arquivo anexado](configure-quotes.md) pode ter até 2 MB, em qualquer um dos seguintes formatos de arquivo: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG ou JPEG, PNG.

1. Cria e processa a cotação:

   - Envia a cotação para o vendedor ao selecionar **[!UICONTROL Request a Quote]**.
   - [!BADGE Recurso 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponível somente para participantes do programa Beta"}**[!UICONTROL Save as Draft]**.

     Se o comprador salvar a cota como uma preliminar, ela estará disponível na [!UICONTROL My Quotes] in `Draft` estado. Não estará visível para o Vendedor até que o Comprador abra a cotação preliminar e a submeta.
