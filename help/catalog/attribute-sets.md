---
title: Conjuntos de atributos
description: Saiba como organizar atributos em grupos, que determinam onde eles aparecem no registro do produto.
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/MXe9ockAmhKgFC-ND2CUxqHRAsShfA5Tf8yJsJWy04o
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 0%

---

# Conjuntos de atributos

Uma das primeiras etapas ao criar um produto é escolher o conjunto de atributos usado como modelo para o registro do produto. O conjunto de atributos determina os campos que estão disponíveis durante a entrada de dados e os valores que aparecem para o cliente.

Os atributos são organizados em grupos que determinam onde eles aparecem no registro do produto. Seu armazenamento vem com um conjunto de atributos inicial (chamado _padrão_) que inclui um conjunto de atributos comumente usados. Se você quiser adicionar alguns atributos, poderá adicioná-los a esse conjunto de atributos padrão. Se você vender produtos que exigem tipos específicos de informações, talvez seja melhor criar um conjunto de atributos dedicado que inclua os atributos específicos necessários para o produto.

![Conjuntos de Atributos](./assets/attribute-sets.png){width="700" zoomable="yes"}

## Criar um conjunto de atributos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Clique em **[!UICONTROL Add New Set]**.

   ![Conjunto de atributos - editar nome](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. Insira um **[!UICONTROL Name]** para o conjunto de atributos.

1. Defina **[!UICONTROL Based On]** para um conjunto de atributos existente para ser usado como modelo.

1. Clique em **[!UICONTROL Save]**.

   A próxima página exibe o seguinte:

   - A coluna da esquerda mostra o nome do conjunto de atributos. O nome é para referência interna e pode ser alterado conforme necessário.
   - O centro da página lista a seleção atual de grupos de atributos.
   - A coluna direita lista a seleção de atributos que não estão designados ao conjunto de atributos no momento.

1. Para adicionar um atributo ao conjunto, arraste o atributo da lista **[!UICONTROL Unassigned Attributes]** para a pasta apropriada na coluna **[!UICONTROL Groups]**. Para remover um atributo do conjunto, arraste-o para a lista **[!UICONTROL Unassigned Attributes]**.

   >[!NOTE]
   >
   >Os atributos do sistema são marcados com um ponto e não podem ser removidos da lista _[!UICONTROL Groups]_. No entanto, eles podem ser arrastados para outro grupo no conjunto de atributos.

1. Quando terminar, clique em **[!UICONTROL Save]**.

![Conjunto de atributos - editar](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## Criar um grupo de atributos

1. Na coluna _[!UICONTROL Groups]_do conjunto de atributos, clique em **[!UICONTROL Add New]**.

1. Insira um **[!UICONTROL Name]** para o novo grupo e clique em **[!UICONTROL OK]**.

1. Siga um destes procedimentos:

   - Arraste **[!UICONTROL Unassigned Attributes]** para o novo grupo.
   - Arraste os atributos de qualquer outro grupo para o novo grupo.
   - Arraste atributos desnecessários para **[!UICONTROL Unassigned Attributes]**.

   O novo grupo se torna uma seção de atributos em qualquer produto baseado no conjunto de atributos.

## Excluir um conjunto de atributos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Selecione o conjunto de atributos na lista e abra no modo de edição.

1. Clique em **[!UICONTROL Delete]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

