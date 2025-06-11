---
title: Temas
description: Saiba mais sobre  [!DNL Commerce]  temas, que incluem arquivos de layout, arquivos de modelo, arquivos de tradução e capas que definem a aparência da sua loja.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Temas

Um tema é uma coleção de arquivos que determina a apresentação visual da loja. Quando você instala o [!DNL Commerce] pela primeira vez, os elementos de design do armazenamento são baseados no tema _Padrão_. Além do tema padrão inicial que acompanha a instalação do [!DNL Commerce], há uma grande variedade de temas disponíveis que você pode usar _como está_ ou modificar conforme suas necessidades.

Um tema responsivo ajusta o layout da página para se ajustar à porta de exibição do dispositivo. O tema de amostra _Luma_ tem um layout flexível e responsivo que pode ser visualizado no desktop, tablet ou dispositivo móvel.

[!DNL Commerce] temas incluem arquivos de layout, arquivos de modelo, arquivos de tradução e capas. Uma capa é uma coleção de arquivos CSS, imagens e JavaScript compatíveis que, juntos, criam a apresentação visual e as interações que os clientes experimentam quando visitam a loja. Temas e capas podem ser modificados e personalizados por um desenvolvedor ou profissional de design que entende o design de temas do Commerce e tem acesso ao seu servidor. Para saber mais, consulte o [_Guia do Desenvolvedor de Front-end_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Tema Luma](./assets/design-responsive.png){width="600" zoomable="yes"}

## O tema padrão

O tema responsivo `Magento Blank` renderiza a exibição da sua vitrine eletrônica para diferentes dispositivos e incorpora as práticas recomendadas para dispositivos móveis, de desktop e de tabela. Alguns temas são projetados para uso somente com dispositivos específicos. Quando o [!DNL Commerce] detecta uma ID de navegador ou agente de usuário específico, ele usa o tema configurado para o navegador específico. A sequência de pesquisa também pode incluir expressões regulares compatíveis com Perl (PCRE).

![Temas](./assets/themes.png){width="700" zoomable="yes"}

### Filtrar a grade de temas

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Clique em **[!UICONTROL Filters]**.

1. Insira um intervalo de ID, nome de tema (ou título), caminho da pasta ou tema principal.

1. Clique em **[!UICONTROL Apply Filters]** para atualizar a lista de temas.

## Exibir as configurações de tema atuais

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Na lista de temas instalados, localize o tema que deseja examinar e clique na linha para exibir as configurações.

1. Para exibir uma página de exemplo, clique em **[!UICONTROL Theme Preview Image]**.

![Tema de visualização](./assets/theme-settings.png){width="600" zoomable="yes"}

## Aplicar um tema padrão

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de armazenamento que você deseja configurar e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Em _[!UICONTROL Default Theme]_, defina **[!UICONTROL Applied Theme]**como aquele que deseja usar para a exibição atual.

   ![Tema Aplicado](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.

## Adicionar uma regra de agente do usuário

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Em _[!UICONTROL Design Rule]_, clique em **[!UICONTROL Add New User Agent Rule]**.

   ![Regra de Design](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Search String]**, insira a ID de navegador do dispositivo específico.

   As cadeias de caracteres de pesquisa são correspondidas na ordem em que são inseridas. Por exemplo, para o Firefox, digite:

   `/^mozilla/i`

1. Para inserir dispositivos adicionais, repita o processo.

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.
