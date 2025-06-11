---
title: Inserir uma imagem no editor
description: O editor do WYSIWYG oferece uma maneira fácil de inserir uma imagem do armazenamento de mídia, vincular a uma imagem que reside em outro servidor ou usar os ativos do Adobe Stock.
exl-id: 591830c9-6dba-4738-a6e7-cf5f93b3c319
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Inserir uma imagem no editor

No editor, é possível inserir uma imagem usando três tipos de origem:

- Adicione uma imagem que foi carregada para o [armazenamento de mídia](media-storage.md)
- Link para uma imagem que reside em outro servidor
- Use a integração do Adobe Stock para pesquisar e usar os ativos do Adobe Stock

![Armazenamento de mídia](./assets/media-storage.png){width="650" zoomable="yes"}

1. Abra uma página, um bloco ou um bloco dinâmico no modo de edição.

1. Vá para a seção _[!UICONTROL Content]_e clique em qualquer elemento compatível com o editor.

1. Posicione o cursor onde deseja que a imagem apareça.

1. Na barra de ferramentas do editor, clique no ícone _Inserir imagem_.

   ![Ícone Inserir imagem](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Esta ação abre a caixa de diálogo _[!UICONTROL Insert/edit image]_.

1. Para o **Source**, clique no ícone _Pesquisar_ e use o método que corresponda ao local do ativo de imagem que você deseja usar:

   ![Selecionando o ícone de pesquisa](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

   - **Carregar uma nova imagem**: use este método para carregar um novo arquivo de imagem.

      - Selecione a pasta na árvore onde deseja adicionar o novo arquivo de imagem.

      - Clique em **[!UICONTROL Choose Files]**.

      - Localize e escolha o arquivo de imagem.

      - Clique na miniatura do novo arquivo e clique em **[!UICONTROL Add Selected]**.

   - **Selecionar um ativo existente**: use este método para selecionar um ativo de imagem existente do armazenamento de mídia/galeria.

      - Use a árvore para navegar até a imagem.

      - Clique na miniatura e em **[!UICONTROL Add Selected]**.

   - **Pesquise e selecione uma imagem do Adobe Stock**: use este método para localizar uma imagem do Adobe Stock.

     >[!NOTE]
     >
     >Este método requer uma [integração com o Adobe Stock](adobe-stock.md) configurada para o Administrador.

      - Clique em **[!UICONTROL Search Adobe Stock]** e procure uma imagem.

      - Salve a imagem de visualização ou licenciada na galeria.

        Consulte [Usando Imagens do Adobe Stock](adobe-stock-manage.md) para obter mais informações sobre como trabalhar com ativos do [Adobe Stock](https://stock.adobe.com).

      - Selecione a miniatura do ativo na galeria e clique em **[!UICONTROL Add Selected]**.

1. Para **[!UICONTROL Image Description]**, insira uma breve descrição da imagem.

1. Insira a largura e a altura **[!UICONTROL Dimensions]**, em pixels, para renderizar a imagem na página.

   Mantenha a caixa de seleção **[!UICONTROL Constrain proportions]** marcada para manter automaticamente a taxa de proporção da imagem.

1. Clique em **[!UICONTROL Insert]** para concluir o processo.
