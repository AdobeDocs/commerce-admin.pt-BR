---
title: Categorias ocultas
description: Saiba como usar categorias ocultas para fins internos ou para vincular a uma categoria que não está incluída no menu de navegação.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Categorias ocultas

Há muitas maneiras de usar categorias ocultas. Talvez você queira criar níveis de categoria adicionais para suas próprias finalidades internas, mas mostrar apenas as categorias de nível superior para os clientes. Ou talvez você queira vincular a uma categoria que não está incluída no menu de navegação.

## Criar categorias ocultas

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Na árvore de categorias, selecione a categoria que deseja ocultar e faça o seguinte:

   - Definir **[!UICONTROL Is Active]** para `Yes`.
   - Definir **[!UICONTROL Include in Menu]** para `No`.

1. No **[!UICONTROL Display Settings]** seção, definir **[!UICONTROL Anchor]** para `No`.

   ![Categoria oculta](./assets/hidden-categories.png){width="600" zoomable="yes"}

   A categoria oculta está ativa, mas não aparece no menu superior nem na navegação em camadas.

1. Complete as configurações a seguir para cada subcategoria oculta para criar subcategorias:

   >[!NOTE]
   >
   >Embora a categoria esteja oculta, você pode criar subcategorias abaixo dela e ativá-las.

   - Definir **[!UICONTROL Enable Category]** para `Yes`.
   - No **[!UICONTROL Display Settings]** seção, definir **[!UICONTROL Anchor]** para `Yes`.

   Como categorias ativas, agora é possível vinculá-las a partir de outros locais na loja, mas elas não aparecem no menu.

1. Quando terminar, clique em **[!UICONTROL Save]**.
