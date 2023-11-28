---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Quotes]'
description: Revise as configurações no [!UICONTROL Sales] &gt; [!UICONTROL Quotes] página do Administrador do Commerce.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Com a instalação e a habilitação do B2B para Adobe Commerce, a experiência de compra pode ser personalizada com recursos específicos da empresa. O B2B para Adobe Commerce é uma solução integrada que oferece suporte aos modelos B2B e B2C. Para obter mais informações sobre os recursos B2B, consulte a [Guia do usuário B2B para Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://docs.magento.com/user-guide/sales/quotes.html) -->

## [!UICONTROL General]

![Geral](./assets/quotes-general.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Site | O valor mínimo do subtotal do carrinho de compras, após quaisquer descontos, que é necessário antes que um cliente possa enviar uma solicitação de cotação. Valor padrão: `0` |
| [!UICONTROL Minimum Amount Message] | Exibição da loja | A mensagem que aparece no carrinho de compras quando um cliente tenta enviar uma solicitação de cotação, mas o valor mínimo necessário não é atendido. |
| [!UICONTROL Default Expiration Period] | Site | Determina a duração padrão de um [citação](../../b2b/quote-price-negotiation.md) como período de tempo a partir da data em que a solicitação de cotação é enviada. Opções: `Days` / `Weeks` / `Months` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Attached Files]

![Arquivos Anexados](./assets/quotes-attached-files.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Global | Determina os formatos de arquivo que podem ser anexados a aspas. Valores padrão suportados: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, e `jpeg` |
| [!UICONTROL Maximum file size] | Global | Determina o tamanho máximo de um arquivo anexado a uma aspa. Esta configuração pode ser substituída pela configuração do servidor. |

{:style=&quot;table-layout:auto&quot;}
