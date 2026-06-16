---
title: Categorias - Configurações de conteúdo
description: Saiba mais sobre como usar as configurações de [!UICONTROL Content] para definir qualquer conteúdo adicional que apareça na página de categoria.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/PKCKw4i-EDB10X3AU-daMiyVMT96naqRLF8vrVBp24s
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 450
ht-degree: 0%

---

# Categorias - Configurações de conteúdo

As configurações de _[!UICONTROL Content]_&#x200B;determinam se algum conteúdo adicional aparece na página de categoria. Além da lista de produtos da categoria, a página pode incluir uma imagem, uma descrição e um bloco do CMS. Você pode usar as ferramentas de conteúdo [[!DNL Page Builder]](../page-builder/introduction.md) para definir a descrição da categoria.

## Adicionar a descrição da categoria em [!DNL Page Builder]

1. Abra a categoria no modo de edição.

1. Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) na seção **[!UICONTROL Content]**.

   ![Conteúdo da categoria](./assets/category-content.png){width="600" zoomable="yes"}

1. Na parte superior direita da área **[!UICONTROL Description]**, clique em **[!UICONTROL Edit with Page Builder]**.

1. Use as ferramentas de conteúdo do [[!DNL Page Builder]](../page-builder/introduction.md) para [editar qualquer texto existente](../page-builder/text.md) e adicionar outro conteúdo (se necessário).

## Visualização de [!DNL Page Builder]

Quando você expande a seção _Conteúdo_ para uma categoria existente onde há conteúdo criado com [!DNL Page Builder], ela exibe uma pré-visualização do conteúdo **[!UICONTROL Description]** como ele apareceria na página de categoria. Clicar na área de conteúdo abre o espaço de trabalho [!DNL Page Builder], onde você pode fazer as atualizações necessárias.

![Visualização da descrição](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Essa pré-visualização de conteúdo é ativada para os formulários de produto e categoria por padrão. Se o desempenho for afetado pelo carregamento da visualização, você poderá desabilitar a visualização nas configurações de [Gerenciamento de conteúdo](../configuration-reference/general/content-management.md#advanced-content-tools).

## Adicionar a descrição da categoria no editor

Digite somente caracteres ASCII simples na caixa de texto. Ao colar texto de um processador de texto, salve-o primeiro como um arquivo .TXT simples para remover os caracteres de controle invisíveis.

Para obter mais informações, consulte [editor do WYSIWYG](../content-design/editor.md).

1. Abra a categoria no modo de edição.

1. Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) na seção **[!UICONTROL Content]**.

   ![Conteúdo da categoria](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Insira a categoria **[!UICONTROL Description]** e use a [barra de ferramentas do editor](../content-design/editor.md) para formatar conforme necessário.

   Você pode arrastar o canto inferior direito para alterar a altura da caixa de texto.

## Adicionar um bloco CMS à página de categoria

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Na árvore de categorias, selecione a categoria que deseja editar.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Content]**.

1. Para **[!UICONTROL Add the CMS block]**, selecione um bloco que deseja adicionar.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Display Settings]**.

1. Defina o **[!UICONTROL Display Mode]** como um dos seguintes:

   - `Static block only`
   - `Static block and products`

1. Quando terminar, clique em **[!UICONTROL Save]** e revise a exibição de bloco na loja (requer atualização do cache).

## Referência de configurações de conteúdo

| Configuração | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Category Image] | Exibição da loja | Especifica uma imagem para a parte superior da página de categoria. Métodos: <br/><br/>**[!UICONTROL Upload]**- Carrega um arquivo de imagem do computador local para a galeria e o usa como a imagem da categoria.<br/><br/>**[!UICONTROL Select from Gallery]** - Solicita que você escolha uma imagem existente na galeria. <br/><br/>![Ícone de câmera do Page Builder](../assets/icon-camera.png) - Arraste um arquivo de imagem para o bloco da câmera ou navegue até a imagem e selecione-a no sistema de arquivos local. |
| [!UICONTROL Description] | Exibição da loja | Especifica uma descrição que aparece na página da categoria. <br/><br/>**[!UICONTROL Edit with Page Builder]**- Abre o [[!DNL Page Builder] espaço de trabalho](../page-builder/workspace.md), onde você pode editar a descrição.<br/><br/>**[!UICONTROL Show / Hide Editor]** - Alterna a exibição entre o editor WYSIWYG e os modos HTML. |
| [!UICONTROL Add CMS Block] | Exibição da loja | Adiciona um [bloco do CMS](../content-design/blocks.md) existente à página de categoria. |

{style="table-layout:auto"}
