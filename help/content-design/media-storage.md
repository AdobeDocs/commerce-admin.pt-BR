---
title: Armazenamento de mídia
description: Saiba como o armazenamento de mídia ajuda a organizar e obter acesso aos arquivos de mídia do Commerce armazenados no servidor.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Armazenamento de mídia

O armazenamento de mídia ajuda você a organizar e obter acesso aos arquivos de mídia armazenados no servidor. O caminho para o local dos arquivos é determinado pela configuração da [URL base](../stores-purchase/store-urls.md). Os arquivos no armazenamento de mídia podem ser acessados do editor ao trabalhar em páginas e blocos estáticos. Normalmente, o armazenamento de mídia reside no sistema de arquivos no mesmo servidor que os arquivos de programa do [!DNL Commerce].

Como alternativa, os arquivos de mídia podem ser gerenciados em um [banco de dados](media-storage-database.md) ou em um servidor separado ou em uma [rede de entrega de conteúdo](media-storage-content-delivery-network.md). A vantagem de usar armazenamento alternativo é que ele minimiza o esforço necessário para sincronizar a mídia. O desempenho da sincronização é especialmente afetado quando várias instâncias do sistema são implantadas em servidores diferentes que precisam de acesso às mesmas imagens, arquivos CSS e outros arquivos de mídia.

O editor pode ser configurado para usar URLs de mídia estática ou [dinâmica](../catalog/catalog-urls.md#configure-catalog-media-url-format) para conteúdo de catálogo na categoria ou descrição do produto.

![[!DNL Commerce] Armazenamento de mídia](./assets/media-storage.png){width="650" zoomable="yes"}

## Adicionar arquivos ao armazenamento de mídia

As duas primeiras etapas são iguais se você estiver inserindo uma imagem.

1. Na barra de ferramentas do [editor](editor.md), clique no ícone _Inserir Imagem_.

   ![Ícone Inserir imagem](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Esta ação abre a caixa de diálogo _[!UICONTROL Insert/edit image]_.

1. Depois de _[!UICONTROL Source]_, clique no ícone_ Pesquisar _(![Ícone Pesquisar](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Na árvore de diretórios à esquerda, siga um destes procedimentos:

   - Navegue até a pasta onde deseja salvar a imagem carregada.

   - Navegue até o local onde deseja criar uma pasta e clique em **Criar Pasta**.

     Para adicionar uma pasta, digite o nome da pasta e clique em **[!UICONTROL OK]**.

1. Para adicionar um ou mais arquivos ao Armazenamento de Mídia, você pode carregar os arquivos do seu sistema ou usar a [Integração do Adobe Stock](adobe-stock.md):

   Para carregar arquivos do seu sistema, clique em **[!UICONTROL Choose Files]** e faça o seguinte:

   - No diretório do computador local, navegue até o local das imagens.

   - Selecione cada imagem a ser carregada.

   - Clique em **[!UICONTROL Open]**.

   Para usar ativos do Adobe Stock usando a [integração](adobe-stock.md):

   - Clique em **[!UICONTROL Search Adobe Stock]**.

   - Adicione uma imagem de visualização ou licenciada do Adobe Stock (consulte [Uso de imagens do Adobe Stock](adobe-stock-manage.md)).

As imagens são carregadas na pasta de Armazenamento de mídia atual no servidor.

![[!DNL Commerce] Armazenamento de mídia](./assets/media-storage.png){width="650" zoomable="yes"}

## Inserir uma imagem do armazenamento de mídia

Abra a página ou o bloco a ser editado. Em seguida, use um dos métodos a seguir para inserir uma imagem do armazenamento de mídia:

### Método 1: modo WYSIWYG

1. Na barra de ferramentas do [editor](editor.md), clique no ícone _Inserir Imagem_.

1. Depois de _[!UICONTROL Source]_, clique no ícone_ Pesquisar _(![Ícone Pesquisar](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Selecionando o ícone de pesquisa](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Na árvore de diretórios à esquerda, navegue até a pasta onde a imagem está armazenada.

1. Selecione o bloco da imagem e clique em **[!UICONTROL Add Selected]**.

### Método 2: modo HTML

1. Posicione o cursor no código onde a tag `<img>` deve ser inserida.

1. Clique em **[!UICONTROL Insert Image]**.

   ![Inserir Imagem (Modo HTML)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
