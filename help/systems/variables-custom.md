---
title: Adicionar variáveis personalizadas
description: Saiba como criar variáveis personalizadas e inseri-las em páginas, blocos e conteúdo do produto.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: https://experienceleague.adobe.com/zhgemfdr2g5sanaFuiF9l20figj9ZD-3codE97WWWg8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 344
ht-degree: 1%

---

# Adicionar variáveis personalizadas

Para atender às necessidades específicas da sua empresa, você pode criar variáveis personalizadas e inseri-las em [páginas](../content-design/pages.md), [blocos](../content-design/blocks.md) e [modelos de email](email-templates.md). A lista de variáveis permitidas que aparece ao clicar no botão _Inserir Variável_ inclui [predefinidas](variables-predefined.md) e variáveis personalizadas. A lista de variáveis disponíveis para um template de email específico é determinada pelos dados associados ao template. Consulte a [Referência de variáveis](variables-reference.md) para obter uma lista de modelos de email usados com frequência e suas variáveis associadas.

![Variáveis personalizadas](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Somente variáveis predefinidas ou personalizadas permitidas podem ser usadas em modelos de email e boletim informativo.

## Etapa 1: criar uma variável personalizada

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. Clique em **[!UICONTROL Add New Variable]**.

1. Digite um identificador para **[!UICONTROL Variable Code]**, usando todos os caracteres minúsculos sem espaços.

   Se necessário, você pode usar um caractere de sublinhado ou hífen para representar um espaço. Por exemplo: `my_custom_variable`

1. Digite um **[!UICONTROL Variable Name]**, que é usado para referência interna. Por exemplo: `My Custom Variable`

1. Para inserir o valor associado à variável, siga um destes procedimentos:

   - Para **[!UICONTROL Variable HTML Value]**, insira o valor da variável formatado com marcas HTML simples. Por exemplo:

     `<b>This formatted content appears in place of the variable.</b>`

   - Para **[!UICONTROL Variable Plain Value]**, insira o valor da variável como texto sem formatação. Por exemplo:

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >Se precisar de mais espaço, arraste o canto inferior direito da caixa de texto.

   ![Nova variável personalizada](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Etapa 2: insira a variável personalizada no conteúdo

Use [!DNL Page Builder] para inserir uma variável personalizada.

1. Abra a página, o bloco, a categoria ou o produto em que deseja adicionar a variável ao conteúdo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Content]**.

1. Clique em **[!UICONTROL Edit with Page Builder]**.

1. No painel esquerdo, clique em **[!UICONTROL Elements]** e siga um destes procedimentos:

   - Clique em uma área de texto existente na qual deseja inserir a variável.

   - Arraste um novo objeto **[!UICONTROL Text]** para o estágio.

1. Na extremidade direita da barra de ferramentas do editor, clique em ( ![Inserir variável](./assets/editor-btn-insert-variable.png) ) para inserir uma variável.

   Estágio e painel ![[!DNL Page Builder]](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. Na lista, selecione a variável personalizada que deseja inserir e clique em **[!UICONTROL Insert Variable]**.

   ![Nova variável personalizada](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   O identificador da variável aparece como um espaço reservado no editor.

   Estágio ![[!DNL Page Builder] - espaço reservado para variável](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.
