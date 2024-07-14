---
title: Modelos de endereço do cliente
description: Saiba como personalizar os modelos de endereço do cliente.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Modelos de endereço do cliente

{{ee-feature}}

Você pode modificar o modelo que controla o formato de endereços de entrega e faturamento do cliente que aparecem em NFFs impressas, remessas e reembolsos, bem como no livro de endereços da conta do cliente. Se quiser incluir informações adicionais, crie [atributos personalizados](attribute-properties.md) associados à conta do cliente e ao [endereço](address-attributes.md) e incorpore-os ao modelo.

## Exemplo 1: formato curto

Para o modelo de endereço [!UICONTROL Text One Line]:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## Exemplo 2: formato longo

Para modelos de endereço [!UICONTROL Text], [!UICONTROL HTML] e [!UICONTROL PDF]:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![Modelos de endereço do cliente](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## Alterar a ordem dos campos de endereço

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel lateral esquerdo, expanda **[!UICONTROL Customers]** e selecione **[!UICONTROL Customer Configuration]**.

1. Clique para expandir a seção **[!UICONTROL Address Templates]**.

   A seção inclui um conjunto separado de instruções de formatação para cada um dos itens a seguir:

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. Edite cada template conforme necessário, usando os exemplos de referência.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
