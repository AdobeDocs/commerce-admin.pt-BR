---
title: Temas
description: Saiba mais sobre [!DNL Commerce] temas, que incluem arquivos de layout, arquivos de modelo, arquivos de tradução e capas que definem a aparência da loja.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Temas

Um tema é uma coleção de arquivos que determina a apresentação visual da loja. Quando você instala o pela primeira vez [!DNL Commerce], os elementos de design do armazenamento se baseiam no _Padrão_ tema. Além do tema padrão inicial que vem com o seu [!DNL Commerce] instalação, há uma grande variedade de temas disponíveis que você pode usar _como está_ ou modifique conforme suas necessidades.

Um tema responsivo ajusta o layout da página para se ajustar à porta de exibição do dispositivo. A amostra _Luma_ o tema tem um layout flexível e responsivo que pode ser visualizado no desktop, tablet ou dispositivo móvel.

[!DNL Commerce] os temas incluem arquivos de layout, arquivos de modelo, arquivos de tradução e capas. Uma capa é uma coleção de arquivos CSS, imagens e JavaScript compatíveis que, juntos, criam a apresentação visual e as interações que os clientes experimentam quando visitam a loja. Temas e capas podem ser modificados e personalizados por um desenvolvedor ou profissional de design que entende o design de temas do Commerce e tem acesso ao seu servidor. Para saber mais, consulte a [_Guia do desenvolvedor de front-end_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Tema Luma](./assets/design-responsive.png){width="600" zoomable="yes"}

## O tema padrão

A variável `Magento Blank` o tema responsivo renderiza a exibição da loja para diferentes dispositivos e incorpora as práticas recomendadas para desktop, tabela e dispositivos móveis. Alguns temas são projetados para uso somente com dispositivos específicos. Quando [!DNL Commerce] O detecta uma ID de navegador específica, ou agente do usuário, e usa o tema configurado para o navegador específico. A sequência de pesquisa também pode incluir expressões regulares compatíveis com Perl (PCRE).

![Temas](./assets/themes.png){width="700" zoomable="yes"}

### Filtrar a grade de temas

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Clique em **[!UICONTROL Filters]**.

1. Insira um intervalo de ID, nome de tema (ou título), caminho da pasta ou tema principal.

1. Clique em **[!UICONTROL Apply Filters]** para atualizar a lista de temas.

## Exibir as configurações de tema atuais

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Na lista de temas instalados, localize o tema que deseja examinar e clique na linha para exibir as configurações.

1. Para exibir uma página de exemplo, clique no link **[!UICONTROL Theme Preview Image]**.

![Visualizar tema](./assets/theme-settings.png){width="600" zoomable="yes"}

## Aplicar um tema padrão

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de loja que deseja configurar e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Em _[!UICONTROL Default Theme]_, definir **[!UICONTROL Applied Theme]**para aquele que você deseja usar na exibição atual.

   ![Tema aplicado](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.

## Adicionar uma regra de agente do usuário

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Em _[!UICONTROL Design Rule]_, clique em **[!UICONTROL Add New User Agent Rule]**.

   ![Regra de design](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Search String]**, digite a ID do navegador do dispositivo específico.

   As cadeias de caracteres de pesquisa são correspondidas na ordem em que são inseridas. Por exemplo, para o Firefox, digite:

   `/^mozilla/i`

1. Para inserir dispositivos adicionais, repita o processo.

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.
