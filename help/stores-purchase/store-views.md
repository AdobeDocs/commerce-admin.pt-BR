---
title: Visualizações da loja
description: Saiba como adicionar e editar uma visualização de loja.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Visualizações da loja

As exibições da loja geralmente são usadas para torná-la disponível em diferentes localidades. Os compradores podem usar o seletor de idioma no cabeçalho da loja para alterar a exibição da loja.

![Escopo - várias exibições de armazenamento](./assets/scope-multiview.svg){width="550"}

## Adicionar uma exibição de loja

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Todas as lojas](./assets/stores-all.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Create Store View]**.

   ![Criar exibição de armazenamento](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Store]** para o armazenamento pai desta exibição.

1. Insira um **[!UICONTROL Name]** para este modo de exibição de loja.

   O nome aparece no seletor de idioma no cabeçalho da loja. Por exemplo: `Spanish`.

1. Para **[!UICONTROL Code]**, insira o código que identifica a exibição (em caracteres minúsculos).

   Por exemplo: `spanish`.

1. Para ativar a exibição, defina **[!UICONTROL Status]** como `Enabled`.

1. (Opcional) Insira um número **[!UICONTROL Sort Order]** para determinar a sequência na qual esta exibição está listada com outras exibições.

1. Clique em **[!UICONTROL Save Store View]**.

## Editar uma exibição de loja

Como o nome da exibição aparece no seletor de idioma, talvez você queira alterar o nome da exibição padrão para algo mais descritivo. O campo _Nome_ é simplesmente um rótulo e pode ser facilmente alterado.

Se sua instalação do Adobe Commerce ou Magento Open Source tiver uma configuração multissite ou multiloja, não altere o campo Código de armazenamento sem verificar se o valor não é referenciado no arquivo `index.php`. Se você não tiver acesso ao servidor para examinar o arquivo, peça ajuda a um desenvolvedor.

| Campo | Valor original | Valor atualizado |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Na coluna _[!UICONTROL Store View]_&#x200B;da grade, clique no nome da exibição que deseja editar.

   Ao editar o modo de exibição padrão, os campos _[!UICONTROL Store]_&#x200B;e_[!UICONTROL Status]_ não estão disponíveis.

   ![Modo de exibição de armazenamento - editar modo de exibição padrão](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Atualize os seguintes campos conforme necessário:

   - **[!UICONTROL Store]** (apenas modos de exibição não padrão)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (somente se não for usado em `index.php`)
   - **[!UICONTROL Status]** (apenas modos de exibição não padrão)
   - **[!UICONTROL Sort Order]**

1. Clique em **[!UICONTROL Save Store View]**.
