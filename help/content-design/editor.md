---
title: Editor WYSIWYG
description: Saiba como usar o editor e trabalhar com conteúdo em uma visualização do _What You See Is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%
---
# Editor WYSIWYG

O editor oferece a capacidade de inserir e formatar o conteúdo durante o trabalho em uma exibição do _What You See Is What You Get_ (WYSIWYG). Se preferir trabalhar diretamente com o código HTML subjacente, é possível alterar os modos facilmente. O editor pode ser usado para criar conteúdo para [páginas](pages.md), [blocos](blocks.md) e [descrições de produtos](../catalog/product-content.md). Ao trabalhar nos detalhes do produto, acesse o editor clicando em **[!UICONTROL Show / Hide Editor]**.

![Barra de ferramentas do editor](./assets/editor-toolbar.png){width="700" zoomable="yes"}

Os tópicos a seguir fornecem informações detalhadas sobre o uso do editor:

- [Inserção de um link](editor-insert-link.md)
- [Inserção de uma imagem](editor-insert-image.md)
- [Inserir um widget](editor-widget.md)
- [Inserção de uma variável](editor-insert-variable.md)

## Configurar o editor

O editor do WYSIWYG é ativado por padrão e pode ser usado para editar conteúdo em páginas e blocos do CMS e em produtos e categorias. Na configuração, você pode ativar ou desativar o editor e optar por usar URLs estáticos, em vez de [dinâmicos](../catalog/catalog-urls.md#dynamic-url), para conteúdo de mídia nas descrições de produto e categoria.

![Opções do WYSIWYG](../configuration-reference/general/assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

>[!NOTE]
>
>O TinyMCE foi substituído pelo Hugerte como editor padrão do WYSIWYG no Magento 2.4.6 e versões posteriores.

Para obter uma descrição detalhada de todas as opções do WYSIWYG, consulte [Gerenciamento de Conteúdo](../configuration-reference/general/content-management.md) na _Referência de Configuração_.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Defina **[!UICONTROL Enable WYSIWYG Editor]** de acordo com sua preferência.

   O editor é ativado por padrão.

1. Defina **[!UICONTROL Static URLs for Media Content in WYSIWYG]** de acordo com sua preferência para todo o [conteúdo de mídia](../catalog/catalog-urls.md#static-url) inserido com o editor do WYSIWYG.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
