---
title: Visualizações da loja
description: Saiba como adicionar e editar uma visualização de loja.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 2%

---

# Visualizações da loja

As exibições da loja geralmente são usadas para torná-la disponível em diferentes localidades. Os compradores podem usar o seletor de idioma no cabeçalho da loja para alterar a exibição da loja.

![Escopo - várias exibições de armazenamento](./assets/scope-multiview.svg){width="550"}

## Adicionar uma exibição de loja

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Todas as lojas](./assets/stores-all.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Create Store View]**.

   ![Criar exibição de loja](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Store]** ao armazenamento pai desta exibição.

1. Insira um **[!UICONTROL Name]** para esta exibição de loja.

   O nome aparece no seletor de idioma no cabeçalho da loja. Por exemplo: `Spanish`.

1. Para **[!UICONTROL Code]**, insira o código que identifica a exibição (em caracteres minúsculos).

   Por exemplo: `spanish`.

1. Para ativar a exibição, defina **[!UICONTROL Status]** para `Enabled`.

1. (Opcional) Insira um **[!UICONTROL Sort Order]** número para determinar a sequência na qual essa exibição é listada com outras exibições.

1. Clique em **[!UICONTROL Save Store View]**.

## Editar uma exibição de loja

Como o nome da exibição aparece no seletor de idioma, talvez você queira alterar o nome da exibição padrão para algo mais descritivo. A variável _Nome_ O campo é simplesmente um rótulo e pode ser facilmente alterado.

Se sua instalação do Adobe Commerce ou Magento Open Source tiver uma configuração multisite ou de várias lojas, não altere o campo Store Code sem verificar se o valor não está referenciado no `index.php` arquivo. Se você não tiver acesso ao servidor para examinar o arquivo, peça ajuda a um desenvolvedor.

| Campo | Valor original | Valor atualizado |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. No _[!UICONTROL Store View]_da grade, clique no nome da exibição que deseja editar.

   Ao editar a exibição padrão, a variável _[!UICONTROL Store]_e_[!UICONTROL Status]_ campos não estão disponíveis.

   ![Exibição de armazenamento - editar exibição padrão](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Atualize os seguintes campos conforme necessário:

   - **[!UICONTROL Store]** (somente exibições não padrão)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (somente se não for usado em `index.php`)
   - **[!UICONTROL Status]** (somente exibições não padrão)
   - **[!UICONTROL Sort Order]**

1. Clique em **[!UICONTROL Save Store View]**.
