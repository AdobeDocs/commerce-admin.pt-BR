---
title: Categorias ocultas
description: Saiba como usar categorias ocultas para fins internos ou para vincular a uma categoria que não está incluída no menu de navegação.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/vXJFiYxeTBcRQxdc4XGrPEPKuBAcqr-mnuUlh1WIskM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 0%

---

# Categorias ocultas

Há muitas maneiras de usar categorias ocultas. Talvez você queira criar níveis de categoria adicionais para suas próprias finalidades internas, mas mostrar apenas as categorias de nível superior para os clientes. Ou talvez você queira vincular a uma categoria que não está incluída no menu de navegação.

## Criar categorias ocultas

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Na árvore de categorias, selecione a categoria que deseja ocultar e faça o seguinte:

   - Defina **[!UICONTROL Is Active]** como `Yes`.
   - Defina **[!UICONTROL Include in Menu]** como `No`.

1. Na seção **[!UICONTROL Display Settings]**, defina **[!UICONTROL Anchor]** como `No`.

   ![Categoria oculta](./assets/hidden-categories.png){width="600" zoomable="yes"}

   A categoria oculta está ativa, mas não aparece no menu superior nem na navegação em camadas.

1. Complete as configurações a seguir para cada subcategoria oculta para criar subcategorias:

   >[!NOTE]
   >
   >Embora a categoria esteja oculta, você pode criar subcategorias abaixo dela e ativá-las.

   - Defina **[!UICONTROL Enable Category]** como `Yes`.
   - Na seção **[!UICONTROL Display Settings]**, defina **[!UICONTROL Anchor]** como `Yes`.

   Como categorias ativas, agora é possível vinculá-las a partir de outros locais na loja, mas elas não aparecem no menu.

1. Quando terminar, clique em **[!UICONTROL Save]**.
