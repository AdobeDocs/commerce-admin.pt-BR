---
title: '[!UICONTROL Sales] > [!UICONTROL Quotes]'
description: Revise as configurações na página [!UICONTROL Sales] > [!UICONTROL Quotes] do Administrador do Commerce.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Com a instalação e a habilitação do Adobe Commerce B2B, a experiência de compra pode ser personalizada com recursos específicos da empresa. O Adobe Commerce B2B é uma solução integrada que oferece suporte aos modelos B2B e B2C. Para obter mais informações sobre os recursos B2B, consulte o [Guia do Usuário B2B do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![Geral](./assets/quotes-general.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Site | O valor mínimo do subtotal do carrinho de compras, após quaisquer descontos, que é necessário antes que um cliente possa enviar uma solicitação de cotação. Valor padrão: `0` |
| [!UICONTROL Minimum Amount Message] | Exibição da loja | A mensagem que aparece no carrinho de compras quando um cliente tenta enviar uma solicitação de cotação, mas o valor mínimo necessário não é atendido. |
| [!UICONTROL Default Expiration Period] | Site | Determina o tempo de vida padrão de uma [aspa](../../b2b/quote-price-negotiation.md) como período de tempo a partir da data em que a solicitação de aspas é enviada. Opções: `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![Arquivos anexados](./assets/quotes-attached-files.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Global | Determina os formatos de arquivo que podem ser anexados a aspas. Valores padrão com suporte: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` e `jpeg` |
| [!UICONTROL Maximum file size] | Global | Determina o tamanho máximo de um arquivo anexado a uma aspa. Esta configuração pode ser substituída pela configuração do servidor. |

{style="table-layout:auto"}
