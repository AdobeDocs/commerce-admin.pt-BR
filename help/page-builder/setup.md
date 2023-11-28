---
title: '[!DNL Page Builder] configuração'
description: Saiba mais sobre [!DNL Page Builder] configuração de recurso no Admin para Adobe Commerce e Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] configuração

Quando ativado na configuração, [!DNL Page Builder] é a ferramenta de criação de conteúdo padrão para Páginas do CMS, Blocos e Blocos dinâmicos. Além disso, a _[!UICONTROL Enable Advanced CMS]_ofertas de botão [!DNL Page Builder] como uma opção para Categorias e Produtos. Você também pode escolher o padrão [layout de página](../content-design/page-layout.md) que você deseja usar para produtos, categorias e páginas do CMS. [!DNL Page Builder] não está disponível para o conteúdo do informativo, que usa o formato WYSIWYG [editor](../content-design/editor.md).

>[!NOTE]
>
>Quando instalado, [!DNL Page Builder] substitui a configuração padrão para o [!UICONTROL Mask for Meta Description] campo de configuração. O valor é alterado de `{{name}} {{description}}` para `{{name}}`.
><br>
>Você pode acessar essa configuração quando acessa [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], expandir [!UICONTROL Catalog]e escolha [!UICONTROL Catalog] por baixo. A variável [!UICONTROL Mask for Meta Description] o campo está no campo [!UICONTROL Product Fields Auto-generation] seção.

>[!NOTE]
>
>Um usuário administrador deve ter [!UICONTROL Content] permissões para seus [escopo da função](../systems/permissions-user-roles.md) para ver [!UICONTROL Edit with Page Builder] e poder usar o Page Builder.

Para obter mais informações sobre as opções de configuração das Ferramentas avançadas de gerenciamento de conteúdo, consulte [_Guia de referência de configuração_](../configuration-reference/general/content-management.md).

## Configurar [!DNL Page Builder]

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** e verificar se **[!UICONTROL Enable Page Builder]** está definida como `Yes`.

   ![Ferramentas de conteúdo avançadas](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Se estiver pronto para configurar [!DNL Google Maps], faça o seguinte:

   - Se necessário, siga as instruções [Obter chave de API][1] e copie e cole suas instruções **[!UICONTROL Google Maps API Key]**.

   - Para alterar o **[!UICONTROL Google Maps Style]**, cole o código JSON gerado pelo [[!DNL Google Maps] Assistente de estilo das APIs][2].

   >[!NOTE]
   >
   >Consulte [Mídia - Mapa](map.md) para obter mais informações sobre como usar o [!DNL Google Maps] no seu [!DNL Page Builder] conteúdo.

1. Para configurar o número de diretrizes na variável [!DNL Page Builder] grade da coluna, faça o seguinte:

   - Para **[!UICONTROL Default Column Grid Size]**, insira o número padrão de colunas que você deseja exibir na grade.

   - Para **[!UICONTROL Maximum Column Grid Size]**, insira o maior número de colunas que você deseja que estejam disponíveis na grade.

   >[!NOTE]
   >
   >Consulte [Layout - Coluna](column.md) para obter mais informações sobre como usar a grade de colunas ao trabalhar com [!DNL Page Builder] conteúdo.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar layouts padrão

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Web]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** e faça o seguinte:

   ![Layouts padrão](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Para obter mais informações sobre as opções de configuração da Web, consulte [_Guia de referência de configuração_](../configuration-reference/general/web.md#default-layouts).

   - Escolha o **[!UICONTROL Default Product Layout]** que você deseja usar nas páginas de produto.

   - Escolha o **[!UICONTROL Default Category Layout]** que você deseja usar para páginas de categoria.

   - Escolha o **[!UICONTROL Default Page Layout]** que você deseja usar para páginas CMS.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Desativar [!DNL Page Builder]

>[!NOTE]
>
>Desativando [!DNL Page Builder] substitui as Ferramentas de conteúdo avançadas pelo WYSIWYG [editor](../content-design/editor.md)e podem causar erros de exibição na loja. Conteúdo criado anteriormente com [!DNL Page Builder] pode não ser editável no Administrador.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** e defina **[!UICONTROL Enable Page Builder]** para `No`.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL Turn Off]**.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, [atualizar](../systems/cache-management.md) qualquer cache inválido.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
