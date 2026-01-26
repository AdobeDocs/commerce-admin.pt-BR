---
title: Configuração de [!DNL Page Builder]
description: Saiba mais sobre a configuração de recursos do  [!DNL Page Builder]  no Admin para Adobe Commerce e Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Configuração de [!DNL Page Builder]

Quando habilitada na configuração, [!DNL Page Builder] é a ferramenta de criação de conteúdo padrão para Páginas, Blocos e Blocos Dinâmicos do CMS. Além disso, o botão _[!UICONTROL Enable Advanced CMS]_&#x200B;oferece [!DNL Page Builder] como uma opção para Categorias e Produtos. Você também pode escolher o [layout de página](../content-design/page-layout.md) padrão que deseja usar para produtos, categorias e páginas do CMS. [!DNL Page Builder] não está disponível para o conteúdo do informativo, que usa o [editor](../content-design/editor.md) do WYSIWYG.

>[!NOTE]
>
>Quando instalado, [!DNL Page Builder] substitui a configuração padrão para o campo de configuração [!UICONTROL Mask for Meta Description]. Valor alterado de `{{name}} {{description}}` para `{{name}}`.
><br>
>Você pode acessar esta configuração quando for até [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], expandir [!UICONTROL Catalog] e escolher [!UICONTROL Catalog] abaixo. O campo [!UICONTROL Mask for Meta Description] está na seção [!UICONTROL Product Fields Auto-generation].

>[!NOTE]
>
>Um usuário administrador deve ter [!UICONTROL Content] permissões para seu [escopo de função](../systems/permissions-user-roles.md) para ver os botões [!UICONTROL Edit with Page Builder] e poder usar o Page Builder.

Para obter mais informações sobre as opções de configuração das Ferramentas Avançadas de Gerenciamento de Conteúdo, consulte o [_Guia de Referência de Configuração_](../configuration-reference/general/content-management.md).

## Configurar [!DNL Page Builder]

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** e verifique se **[!UICONTROL Enable Page Builder]** está definido como `Yes`.

   ![Ferramentas avançadas de conteúdo](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Se você estiver pronto para configurar o [!DNL Google Maps], faça o seguinte:

   - Se necessário, siga as instruções de [Obter Chave de API](https://developers.google.com/maps/documentation/javascript/get-api-key) e copie cole seu **[!UICONTROL Google Maps API Key]**.

   - Para alterar o **[!UICONTROL Google Maps Style]**, cole o código JSON gerado pelo [[!DNL Google Maps] Assistente de Estilos de APIs](https://mapstyle.withgoogle.com/).

   >[!NOTE]
   >
   >Consulte [Mídia - Mapa](map.md) para obter mais informações sobre como usar o [!DNL Google Maps] no seu conteúdo [!DNL Page Builder].

1. Para configurar o número de diretrizes na grade da coluna [!DNL Page Builder], faça o seguinte:

   - Para **[!UICONTROL Default Column Grid Size]**, insira o número padrão de colunas que você deseja exibir na grade.

   - Para **[!UICONTROL Maximum Column Grid Size]**, insira o maior número de colunas que você deseja que estejam disponíveis na grade.

   >[!NOTE]
   >
   >Consulte [Layout - Coluna](column.md) para obter mais informações sobre como usar a grade da coluna ao trabalhar com o conteúdo [!DNL Page Builder].

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar layouts padrão

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Web]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** e faça o seguinte:

   ![Layouts padrão](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Para obter mais informações sobre as opções de configuração da Web, consulte o [_Guia de Referência de Configuração_](../configuration-reference/general/web.md#default-layouts).

   - Escolha o **[!UICONTROL Default Product Layout]** que deseja usar nas páginas de produto.

   - Escolha a **[!UICONTROL Default Category Layout]** que deseja usar para páginas de categoria.

   - Escolha o **[!UICONTROL Default Page Layout]** que deseja usar para páginas do CMS.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Desabilitar [!DNL Page Builder]

>[!NOTE]
>
>Desabilitar [!DNL Page Builder] substitui as Ferramentas de Conteúdo Avançado pelo [editor](../content-design/editor.md) do WYSIWYG e pode causar erros de exibição na loja. O conteúdo criado anteriormente com [!DNL Page Builder] pode não ser editável pelo Administrador.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** e definir **[!UICONTROL Enable Page Builder]** como `No`.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL Turn Off]**.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, [atualize](../systems/cache-management.md) qualquer cache inválido.
