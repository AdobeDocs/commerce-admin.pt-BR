---
title: Usar um widget para posicionar um bloco
description: Saiba como usar um widget de bloco estático para colocar um conteúdo existente em quase qualquer lugar da loja.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Usar um widget para posicionar um bloco

A variável _Bloco estático do CMS_ [widget](widgets.md) oferece a capacidade de colocar um dispositivo existente [bloco de conteúdo](blocks.md) praticamente em qualquer lugar da loja.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Etapa 1: Escolher o tipo de widget

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]**.

1. No _Configurações_ seção, definir **[!UICONTROL Type]** para `CMS Static Block` e clique em **[!UICONTROL Continue]**.

1. Verifique se **[!UICONTROL Design Theme]** for definido com o tema atual e clique em **[!UICONTROL Continue]**.

   ![Configurações do widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. No _[!UICONTROL Storefront Properties]_faça o seguinte:

   - Para **[!UICONTROL Widget Title]**, insira um título descritivo para o widget.

     Este título é visível somente no _Admin_.

   - Para **[!UICONTROL Assign to Store Views]**, selecione as exibições de loja onde o widget está visível.

     Você pode selecionar uma visualização de loja específica, ou `All Store Views`. Para selecionar várias exibições, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

   - (Opcional) Para **[!UICONTROL Sort Order]**, insira um número para determinar a ordem em que esse item aparece com outros na mesma parte da página. (`0` = primeiro, `1` = segundo, `3` = terceiro e assim por diante.)

     ![Propriedades da vitrine](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Etapa 2: completar as atualizações de layout do widget

1. No _[!UICONTROL Layout Updates]_clique em **[!UICONTROL Add Layout Update]**.

1. Definir **[!UICONTROL Display On]** à categoria, ao produto ou à página em que deseja que o bloco seja exibido.

1. Para colocar o bloco em uma página específica, faça o seguinte:

   - Escolha o **[!UICONTROL Page]** onde deseja que o bloco apareça.

   - Escolha o **[!UICONTROL Block Reference]** que identifica o local onde o bloco é exibido na página.

   - Aceite a configuração padrão para **[!UICONTROL Template]**, que está definida como `CMS Static Block Default Template`.

     ![Atualizações de layout](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Opções de atualização de layout

| Campo | Descrição |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | Exibe o widget na página de categoria de âncora.<br/>**[!UICONTROL Categories]**- Categorias em que a âncora é exibida. Opções: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Defina o contêiner na parte do layout da página em que deseja exibir o widget.<br/>**[!UICONTROL Template]**- Determina o tema do layout. |
| [!UICONTROL Non-Anchor Categories] | Exibe o widget na página de categoria sem âncora.<br/>**[!UICONTROL Categories]**- Categorias em que a âncora é exibida. Opções: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Defina o contêiner na parte do layout da página em que deseja exibir o widget.<br/>**[!UICONTROL Template]**- Determina o tema do layout. |
| **_[!UICONTROL Products]_** |  |
| Todos os tipos de produto | Exibe o widget em um tipo específico de página de produto ou em todas as páginas de produto. <br/>**[!UICONTROL Products]**- Produtos para os quais o widget é exibido. Opções: `All` /` Specific Products`<br/>**[!UICONTROL Container]** - Defina o contêiner na parte do layout da página em que deseja exibir o widget.<br/>**[!UICONTROL Template]**- Determina o tema do layout. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | Exibe o widget em todas as páginas. <br/>**[!UICONTROL Container]**- Defina o contêiner na parte do layout da página em que deseja exibir o widget.<br/>**[!UICONTROL Template]** - Determina o tema do layout. |
| [!UICONTROL Specified Page] | Exibe o widget em uma página específica. Opções:<br/>**[!UICONTROL Page]**- Páginas para as quais o widget é exibido.<br/>**[!UICONTROL Container]** - Defina o contêiner na parte do layout da página em que deseja exibir o widget.<br/>**Modelo** - Determina o tema do layout. |
| [!UICONTROL Page Layouts] | Exibe o widget em páginas com um determinado layout. <br/>**[!UICONTROL Page]**- Páginas para as quais o widget é exibido.<br/>**[!UICONTROL Container]** - Defina o contêiner na parte do layout da página em que deseja exibir o widget.<br/>**[!UICONTROL Template]**- Determina o tema do layout. |

{style="table-layout:auto"}

## Etapa 3: Colocar o bloco

1. No painel esquerdo, selecione **[!UICONTROL Widget Options]**.

1. Clique em **[!UICONTROL Select Block…]** e escolha o bloco que deseja colocar na lista.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   O aplicativo agora aparece na lista.

1. Quando solicitado, siga as instruções na parte superior da página para atualizar o índice e o cache da página.

1. Volte para a loja para verificar se o bloco aparece no local correto.

   Para mover o bloco, você pode reabrir o widget ou tentar uma página ou referência de bloco diferente.
