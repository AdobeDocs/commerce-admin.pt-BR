---
title: Preços avançados
description: Saiba mais sobre os controles avançados de preços disponíveis no Adobe Commerce.
exl-id: 0f353341-1b6b-4093-bba9-4a1b88323f8a
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Preços avançados

O Adobe Commerce e o Magento Open Source suportam várias opções de preço que podem ser usadas em promoções ou para atender aos requisitos mínimos de preço anunciados do fabricante. As alterações nos preços do produto podem ser feitas de acordo com a programação ou pela regra de preço aplicada no nível do produto ou no carrinho de compras.

Gerencie os preços de seus produtos com preços avançados para oferecer aos clientes melhores taxas que incentivam os consumidores a gastar mais, direcionar o tráfego para o seu site e limpar o estoque antigo.

As configurações de _[!UICONTROL Advanced Pricing]_&#x200B;definem as condições necessárias para preços especiais disponíveis para um grupo de clientes ou catálogo compartilhado específico. Os preços avançados podem ser aplicados a produtos simples, virtuais, para download e de pacotes. Para aplicar preços com desconto a outros tipos de produtos, use uma [regra de preço de catálogo](../merchandising-promotions/price-rules-catalog.md). Para obter mais informações, consulte [Escopo de Preço](catalog-price-scope.md).

Os dados de preços avançados são sincronizados com as páginas do produto. Por exemplo, se você atualizar uma quantidade de preço da camada, o sistema atualizará o valor na página do produto.

![Adobe Commerce B2B](../assets/b2b.svg) (Disponível somente com o [Adobe Commerce B2B](./b2b/../introduction.md)) Se você estiver usando catálogos compartilhados, os dados de preço avançado serão sincronizados com as páginas de produto e os catálogos compartilhados. Por exemplo, se você atualizar uma quantidade de preço da camada, o sistema atualizará o valor no catálogo compartilhado e na página do produto. Qualquer preço personalizado indicado no catálogo compartilhado tem prioridade sobre o preço do grupo de clientes. Consulte também [Definir preços e estrutura de catálogo compartilhado](https://experienceleague.adobe.com/docs/commerce-admin/b2b/shared-catalogs/define/catalog-shared-pricing-structure.html) no _Guia B2B do Adobe Commerce_.

![Preços Avançados](./assets/product-pricing-advanced-link.png){width="600" zoomable="yes"}

## Acessar as opções de preço avançadas

1. Abra o produto no modo de edição.

1. Em **[!UICONTROL Price]**, clique em **[!UICONTROL Advanced Pricing]**.

1. Siga as instruções para o tipo de preço avançado necessário.

   - [Preço de Grupo](product-price-group.md)

   - [Preço especial](product-price-special.md)

   - [Preço da camada](product-price-tier.md)

   - [Preço Mínimo Anunciado](product-price-minimum-advertised.md)

## Referência da página

### [!UICONTROL Special Price]

Para oferecer um preço com desconto durante um período de tempo especificado ou campanha programada, informe o preço especial. Quando um preço especial está disponível, o preço de varejo é riscado e o preço especial aparece abaixo em texto grande e em negrito.

#### [!UICONTROL Special Price From] datas

{{ce-feature}}

| Campo | Descrição |
| ---- | ----------- |
| [!UICONTROL From] | Define a primeira data em que o preço especial estará disponível. Você pode inserir a data ou selecioná-la no calendário. |
| [!UICONTROL To] | Define a última data em que o preço especial estará disponível. Você pode inserir a data ou selecioná-la no calendário. |

{style="table-layout:auto"}

### [!UICONTROL Cost]

Informe o custo real do item.

### [!UICONTROL Customer Group Price]

![Preços Avançados](./assets/product-pricing-advanced-group-price.png){width="600" zoomable="yes"}

Configura preços promocionais e de camada para grupos de clientes específicos.

| Item | Descrição |
| ---- | ----------- |
| [!UICONTROL Website] | Identifica o site onde a regra de preço de grupo se aplica. Essa opção será exibida somente se a instalação tiver vários sites. |
| [!UICONTROL Customer Group] | (Obrigatório) Identifica o grupo de clientes que se qualifica para receber o preço com desconto. Quando um valor em um campo de grupo ou catálogo é alterado, a linha de preço personalizada correspondente à configuração anterior é excluída do catálogo compartilhado. <br/>**[!UICONTROL ALL GROUPS]**- Aplica a regra a todos os grupos de clientes.<br/>**[!UICONTROL NOT LOGGED IN]** - Aplica os convidados e clientes da regra que não estão conectados às suas contas. |
| [!UICONTROL Quantity] | Especifica a quantidade necessária para receber um preço de camada. |
| [!UICONTROL Price] | (Obrigatório) Especifica um preço de produto fixo ou com desconto para membros do grupo de clientes, dentro do site específico. Opções: <br/>**[!UICONTROL Fixed]**- (Padrão) O preço com desconto é inserido como um valor decimal fixo. Por exemplo, insira `9.99` como o preço com desconto.<br/>**[!UICONTROL Discount]** - O preço com desconto é inserido como uma porcentagem (%) do preço base do produto. Por exemplo, insira `10` para um desconto de 10%. |
| ![Ícone de lixeira](../assets/icon-delete-trashcan-solid.png) | Exclui a regra atual. |
| **[!UICONTROL Add]** | Insere outra linha para uma nova regra. |

{style="table-layout:auto"}

### [!UICONTROL Catalog and Tier Price]

Configura preços promocionais e de camada para catálogos compartilhados e grupos de clientes específicos.

{{b2b-feature}}

![Advanced Pricing para lojas B2B com catálogos compartilhados](./assets/product-pricing-advanced.png){width="600" zoomable="yes"}

| Item | Descrição |
|----|-----------|
| [!UICONTROL Website] | Identifica o site onde a regra de preço de grupo se aplica. Essa opção será exibida somente se a instalação tiver vários sites. <br>**_Importante:_**&#x200B;Portanto, selecione_Site _na configuração [Escopo do Preço de Catálogo](catalog-price-scope.md); caso contrário, os preços avançados definidos serão exibidos para&#x200B;**todos &#x200B;** sites. |
| [!UICONTROL Group or Catalog] | (Obrigatório) Identifica o grupo de clientes ou catálogo compartilhado que se qualifica para receber o preço com desconto. Quando um valor em um campo de grupo ou catálogo é alterado, a linha de preço personalizada correspondente à configuração anterior é excluída do catálogo compartilhado. <br/>**[!UICONTROL ALL GROUPS]**- Aplica a regra a todos os grupos de clientes. O valor não é aplicado ao catálogo compartilhado e as alterações nos dados de preços avançados não são sincronizadas com o catálogo compartilhado.<br/>**[!UICONTROL NOT LOGGED IN]** - Aplica os convidados e clientes da regra que não estão conectados às suas contas.<br/>**[!UICONTROL Shared Catalogs]**- Aplica a regra a um catálogo compartilhado específico. |
| Quantidade | Especifica a quantidade necessária para receber um preço de camada. |
| [!UICONTROL Price] | (Obrigatório) Especifica um preço de produto fixo ou com desconto para membros do grupo de clientes, dentro do site específico. Opções: <br/>**[!UICONTROL Fixed]**- (Padrão) O preço com desconto é inserido como um valor decimal fixo. Por exemplo, insira `9.99` como o preço com desconto.<br/>**[!UICONTROL Discount]** - O preço com desconto é inserido como uma porcentagem (%) do preço base do produto. Por exemplo, insira `10` para um desconto de 10%. |
| ![Ícone de lixeira](../assets/icon-delete-trashcan-solid.png) | Exclui a regra atual. |
| **[!UICONTROL Add]** | Insere outra linha para uma nova regra. |

{style="table-layout:auto"}

### [!UICONTROL Minimum Advertised Price]

O preço mínimo anunciado (MAP) do produto.

### [!UICONTROL Display Actual Price]

Determina onde o preço real do produto é visível para o cliente.

| Item | Descrição |
|----|-----------|
| [!UICONTROL Use Config] | Usa a definição de configuração atual para a exibição de preço. |
| [!UICONTROL On Gesture] | Exibe o preço real do produto em um pop-up, em resposta ao _Clique para preço_ ou _O que é isso?Link_. |
| [!UICONTROL In Cart] | Exibe o preço real do produto no carrinho de compras. |
| [!UICONTROL Before Order Confirmation] | Exibe o preço real do produto no final do processo de finalização, antes do envio do pedido. |

{style="table-layout:auto"}
