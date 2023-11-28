---
title: Armazenamento de mídia
description: Saiba como o armazenamento de mídia ajuda você a organizar e obter acesso aos arquivos de mídia do Commerce armazenados no servidor.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
source-git-commit: 7dae6b6d387c796c5ff472293c6590fabaa83e85
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Armazenamento de mídia

O armazenamento de mídia ajuda você a organizar e obter acesso aos arquivos de mídia armazenados no servidor. O caminho para o local dos arquivos é determinado pelo parâmetro [URL base](../stores-purchase/store-urls.md) configuração. Os arquivos no armazenamento de mídia podem ser acessados do editor ao trabalhar em páginas e blocos estáticos. Normalmente, o armazenamento de mídia reside no sistema de arquivos no mesmo servidor que o [!DNL Commerce] arquivos de programa.

Como alternativa, os arquivos de mídia podem ser gerenciados em um [banco de dados](media-storage-database.md), ou em um servidor separado ou [rede de entrega de conteúdo](media-storage-content-delivery-network.md). A vantagem de usar armazenamento alternativo é que ele minimiza o esforço necessário para sincronizar a mídia. O desempenho da sincronização é especialmente afetado quando várias instâncias do sistema são implantadas em servidores diferentes que precisam de acesso às mesmas imagens, arquivos CSS e outros arquivos de mídia.

O editor pode ser configurado para usar estático ou [URLs de mídia dinâmica](../catalog/catalog-urls.md#configure-catalog-media-url-format) para conteúdo de catálogo em descrições de categoria ou produto.

![[!DNL Commerce] Armazenamento de mídia](./assets/media-storage.png){width="650" zoomable="yes"}

## Adicionar arquivos ao armazenamento de mídia

As duas primeiras etapas são iguais se você estiver inserindo uma imagem.

1. No [editor](editor.md) barra de ferramentas, clique no link _Inserir imagem_ ícone.

   ![Ícone Inserir imagem](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Essa ação abre a variável _[!UICONTROL Insert/edit image]_diálogo.

1. Depois _[!UICONTROL Source]_, clique no link_ Pesquisar _ícone (![Ícone de pesquisa](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Na árvore de diretórios à esquerda, siga um destes procedimentos:

   - Navegue até a pasta onde deseja salvar a imagem carregada.

   - Navegue até o local onde deseja criar uma pasta e clique em **Criar pasta**.

     Para adicionar uma pasta, digite o nome da pasta e clique em **[!UICONTROL OK]**.

1. Para adicionar um ou mais arquivos ao Armazenamento de mídia, você pode fazer upload dos arquivos do seu sistema ou usar o [Integração do Adobe Stock](adobe-stock.md):

   Para carregar arquivos do seu sistema, clique em **[!UICONTROL Choose Files]** e faça o seguinte:

   - No diretório do computador local, navegue até o local das imagens.

   - Selecione cada imagem a ser carregada.

   - Clique em **[!UICONTROL Open]**.

   Para usar ativos do Adobe Stock usando o [integração](adobe-stock.md):

   - Clique em **[!UICONTROL Search Adobe Stock]**.

   - Adicione uma imagem de visualização ou licenciada do Adobe Stock (consulte [Uso de imagens do Adobe Stock](adobe-stock-manage.md)).

As imagens são carregadas na pasta de Armazenamento de mídia atual no servidor.

![[!DNL Commerce] Armazenamento de mídia](./assets/media-storage.png){width="650" zoomable="yes"}

## Inserir uma imagem do armazenamento de mídia

Abra a página ou o bloco a ser editado. Em seguida, use um dos métodos a seguir para inserir uma imagem do armazenamento de mídia:

### Método 1: modo WYSIWYG

1. No [editor](editor.md) barra de ferramentas, clique no link _Inserir imagem_ ícone.

1. Depois _[!UICONTROL Source]_, clique no link_ Pesquisar _ícone (![Ícone de pesquisa](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Selecionar o ícone de pesquisa](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Na árvore de diretórios à esquerda, navegue até a pasta onde a imagem está armazenada.

1. Selecione o bloco da imagem e clique em **[!UICONTROL Add Selected]**.

### Método 2: modo HTML

1. Posicione o cursor no código onde a variável `<img>` tag será inserida.

1. Clique em **[!UICONTROL Insert Image]**.

   ![Inserir imagem (modo HTML)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
