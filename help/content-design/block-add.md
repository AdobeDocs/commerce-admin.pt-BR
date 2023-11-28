---
title: Adicionar blocos de conteúdo
description: Crie blocos personalizados de conteúdo que você pode reutilizar em qualquer página ou em outro bloco.
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Adicionar blocos de conteúdo

Blocos personalizados de conteúdo podem ser criados e, em seguida, adicionados a qualquer página, grupo de páginas ou até mesmo a outro bloco. Por exemplo, você pode colocar um controle deslizante de imagem em um bloco e, em seguida, colocar o bloco na página inicial. O espaço de trabalho Blocos usa o mesmo [controles básicos](pages-workspace.md) como o _Páginas_ espaço de trabalho para ajudá-lo a encontrar blocos disponíveis e executar a manutenção de rotina. Quando o bloco for concluído, você poderá usar o [Widget](widget-static-block.md) para colocá-la em páginas específicas da loja.

![A página Blocos exibe uma grade de blocos existentes](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## Criar um bloco

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. No canto superior direito, clique em **Adicionar novo bloco**.

   ![A página Novo bloco exibe opções e um espaço de conteúdo](./assets/block-detail.png){width="500" zoomable="yes"}

1. Se quiser alterar o status de habilitação padrão do novo bloco, defina **Habilitar Bloco** para `No`.

1. Atribuir um **Título do bloco** para referência interna.

1. Atribuir um único **Identificador** para o bloco.

   Use todos os caracteres em minúsculas com sublinhados em vez de espaços.

1. Selecionar cada **[!UICONTROL Store View]** onde você deseja que o bloco esteja disponível.

1. Adicione o conteúdo do bloco usando o conjunto de ferramentas de conteúdo exibido:

   - Se [Page Builder](../page-builder/introduction.md) estiver ativado, selecione **[!UICONTROL Edit with Page Builder]** para usar as ferramentas do Page Builder no conteúdo [espaço de trabalho](../page-builder/workspace.md).

     ![Espaço de trabalho do Page Builder](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Para obter informações sobre como adicionar blocos com o Page Builder, consulte [Tutorial 2: blocos](../page-builder/2-blocks.md).

   - Use o [editor](editor.md) para formatar texto, criar links e adicionar tabelas, imagens, vídeo e áudio.

     Se preferir trabalhar com o código HTML, clique em **Mostrar / Ocultar editor**.

     ![Editor de bloco (oculto)](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. Quando terminar, clique no botão **[!UICONTROL Save]** seta e escolha **[!UICONTROL Save & Close]**.

   O novo bloco aparece na parte inferior da lista na grade Blocos.

1. Use o [Widget](widget-static-block.md) ferramenta para colocar o bloco concluído em uma página específica na loja.

## Excluir um bloco

Há duas maneiras de remover um bloco personalizado. Você pode removê-lo do _Blocos_ ou na página editar bloco.

### Método 1: remover um bloco da grade Blocos

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Localize os blocos usando filtros acima da grade e marque a caixa de seleção de um ou mais blocos a serem excluídos.
1. No canto superior esquerdo da lista, defina **[!UICONTROL Actions]** para `Delete`.
1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

### Método 2: remover um bloco da página de edição

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Localize o bloco a ser excluído.
1. No _Ações_ para o bloco, clique em **[!UICONTROL Select]** e escolha **[!UICONTROL Edit]**.
1. Na barra de menus, clique em **[!UICONTROL Delete Block]**.
1. Para confirmar a ação, clique em **[!UICONTROL OK]**.

## Menu Salvar

| Comando | Descrição |
|----------|----------- |
| [!UICONTROL Save] | Salve o bloco atual e continue trabalhando. |
| [!UICONTROL Save & Duplicate] | Salvar e fechar o bloco atual e abrir uma nova cópia duplicada. |
| [!UICONTROL Save & Close] | Salve e feche o bloco atual e retorne à grade Blocos. |

{style="table-layout:auto"}

## Adicionar uma lightbox ou controle deslizante

- É fácil adicionar um [controle deslizante](../page-builder/slider.md) para sua loja com [[!DNL Page Builder]](../page-builder/introduction.md). O controle deslizante pode ser definido para ser reproduzido automaticamente ou controlado manualmente com botões de navegação.

  ![Controle deslizante do Page Builder](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  Há também uma grande variedade de lightboxes de imagem baseadas em jQuery disponíveis em [[!DNL Commerce Marketplace]][1], e alguns são de graça.

- Também é possível baixar uma extensão do [!DNL Commerce Marketplace]. Para obter ajuda adicional, consulte a documentação fornecida pelo desenvolvedor da extensão.

[1]: https://marketplace.magento.com/extensions.html?q=lightbox
