---
title: Espaço de trabalho do produto
description: Saiba mais sobre as configurações e os controles disponíveis no espaço de trabalho do produto.
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
TQID: https://experienceleague.adobe.com/O9e0Z-bHxbokLZd4RbT1puWWAGWnF7SDqvGcc4Bteco
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9958c3ea938ea5ef743f4b347d11e4f833ee1483
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 0%

---

# Espaço de trabalho do produto

O espaço de trabalho do produto é basicamente o mesmo para todos os tipos de produto, embora a seleção de campos mude dependendo do conjunto de atributos usado. Os atributos do produto estão na parte superior do formulário, seguidos por seções expansíveis de informações do produto. Quando um novo produto é salvo pela primeira vez, o seletor _[!UICONTROL Store View]_aparece no canto superior esquerdo do formulário.

>[!NOTE]
>
>As atualizações de enriquecimento do catálogo aplicadas aparecem no nome do produto na parte superior do formulário e na seção **[!UICONTROL Content]**. Para obter mais informações, consulte [Enriquecimento do catálogo](catalog-enrichment.md).

![Espaço de trabalho do produto](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## Configuração de [!UICONTROL Enable Product]

O status online do produto é indicado pelo switch na parte superior do formulário. Para alterar o status online, defina a opção **[!UICONTROL Enable Product]** como `Yes` ou `No`.

| Controle | Descrição |
|-------- | ----------- |
| ![Alternar sim](../assets/toggle-yes.png) | Indica que o produto está online. |
| ![Alternar nº](../assets/toggle-no.png) | Indica que o produto está offline. |

{style="table-layout:auto"}

## Conjunto de atributos

O nome do [conjunto de atributos](attribute-sets.md) aparece no canto superior esquerdo e determina os campos que aparecem no registro do produto. Para escolher um conjunto de atributos diferente, clique na seta para baixo ao lado do nome do conjunto de atributos default.

![Conjunto de atributos](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Expandir/recolher

Para expandir ou recolher uma seção, clique no ícone expandir ![Seletor de expansão](../assets/icon-display-expand.png) ou recolher ![Seletor recolher](../assets/icon-display-collapse.png).

## Menu [!UICONTROL Save]

O menu _[!UICONTROL Save]_inclui várias opções que permitem salvar e continuar, salvar e criar um produto, salvar e duplicar o produto ou salvar e fechar.

![Salvar menu](./assets/product-save-menu.png){width="600" zoomable="yes"}

| Comando | Descrição |
|--- |--- |
| [!UICONTROL Save] | Salve o produto atual e continue trabalhando. |
| [!UICONTROL Save & New] | Salve e feche o produto atual e inicie um novo produto com base no mesmo tipo de produto e modelo. |
| [!UICONTROL Save & Duplicate] | Salvar e fechar o produto atual e abrir uma nova cópia duplicada. |
| [!UICONTROL Save & Close] | Salvar o produto atual e retornar ao espaço de trabalho _[!UICONTROL Products]_. |

{style="table-layout:auto"}

## Valores de campo padrão

Para economizar tempo ao criar produtos, o valor padrão de vários campos de produto faz referência a valores de outro campo. Você pode aceitar o valor padrão ou inserir outro. Os seguintes campos geraram automaticamente valores padrão:

| Campo | Padrão |
|----- |------- |
| [!UICONTROL SKU] | Com base no nome do produto. |
| [!UICONTROL Meta Title] | Com base no nome do produto. |
| [!UICONTROL Meta Keywords] | Com base no nome do produto. |
| [!UICONTROL Meta Description] | Com base no nome e na descrição do produto. |

{style="table-layout:auto"}

Os espaços reservados que representam o valor de outro campo são colocados entre chaves duplas. Qualquer código de atributo incluído no produto [conjunto de atributos](attribute-sets.md) pode ser usado como um espaço reservado.

![Geração automática de campos de produto](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

Para obter uma lista detalhada dessas configurações, consulte [Geração automática de campos de produto](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) na _Referência de configuração_.

### Editar o valor do espaço reservado

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Product Fields Auto-Generation]** e faça as alterações necessárias nos valores de espaço reservado.

   Por exemplo, se houver uma palavra-chave específica que você deseja incluir para cada produto ou uma frase que você deseja incluir em cada meta descrição, insira o valor diretamente no campo apropriado.

   >[!NOTE]
   >
   >Se desejar manter os valores de espaço reservado existentes, preserve as chaves duplas que delimitam cada tag de marcação.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Espaços reservados comuns

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`

