---
title: Importação de imagem do produto
description: Saiba como importar imagens de produtos usando o caminho e o nome de arquivo de cada imagem.
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# Importação de imagem do produto

Várias imagens de produtos de cada tipo podem ser importadas para o Adobe Commerce e o Magento Open Source e associadas a um produto específico. O caminho e o nome de arquivo de cada imagem de produto são inseridos no arquivo CSV, e os arquivos de imagem a serem importados são carregados no caminho correspondente no servidor do Commerce ou no servidor externo.

O Commerce cria sua própria estrutura de diretórios para imagens de produtos, organizada alfabeticamente. Ao exportar dados do produto com imagens existentes para um arquivo CSV, você pode ver o caminho em ordem alfabética antes do nome de arquivo de cada imagem. No entanto, ao importar novas imagens, não é necessário especificar um caminho, pois o Commerce gerencia a estrutura de diretórios automaticamente. Mas certifique-se de inserir o caminho relativo para o diretório de importação antes do nome do arquivo de cada imagem a ser importada.

Para carregar imagens, você deve ter credenciais de logon e permissões corretas para acessar a pasta do Commerce no servidor. Com as credenciais corretas, você pode usar qualquer utilitário SFTP para fazer upload dos arquivos do seu computador desktop para o servidor.

Antes de tentar importar muitas imagens, revise as etapas no método de importação que deseja usar e execute o processo com alguns produtos. Depois de entender como funciona, você se sentirá confiante ao importar grandes quantidades de imagens.

>[!IMPORTANT]
>
>É recomendável usar um programa compatível com a codificação UTF-8 para editar arquivos CSV, como o Notepad++. O Microsoft® Excel insere caracteres adicionais no cabeçalho da coluna do arquivo CSV, o que pode impedir que os dados sejam importados novamente para o Commerce.

## Método 1: importar imagens do servidor local

1. No servidor do Commerce, carregue os arquivos de imagem para a pasta `var/import/images` ou uma subpasta, como `var/import/images/product_images`. Esta é a pasta raiz padrão para importar imagens de produtos.

   ```
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Começando com a versão Adobe Commerce e Magento Open Source `2.3.2`, o caminho especificado nos concatenados **[!UICONTROL Images File Directory]** para importação no diretório base de imagens - `<Magento-root-folder>/var/import/images`. Para versões anteriores do Adobe Commerce e do Magento Open Source, é possível usar uma pasta diferente no servidor do Commerce, desde que o caminho para a pasta seja especificado durante o processo de importação.

1. Nos dados CSV, insira o nome de cada arquivo de imagem a ser importado na linha correta, por `sku`, e na coluna correta, de acordo com o tipo de imagem (`base_image`, `small_image`, `thumbnail_image` ou `additional_images`).

   >[!NOTE]
   >
   >Para imagens na pasta de importação padrão (`var/import/images`), não inclua o caminho antes do nome do arquivo nos dados CSV.

   O arquivo CSV deve incluir somente a coluna `sku` e as colunas de imagem relacionadas.

   ![Exemplo - Importação de dados de imagem CSV](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Siga as instruções para [importar](data-import.md) os dados.

1. Após selecionar o arquivo a ser importado, insira o caminho relativo após **[!UICONTROL Images File Directory]**.

   ```
   var/import/images
   ```

   ![Diretório do arquivo de imagens de importação de dados](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >Deixe _[!UICONTROL Images File Directory]_&#x200B;em branco para usar o diretório `<Magento-root-folder>/var/import/images`. A partir do Adobe Commerce e do Magento Open Source versão 2.3.2, este é o diretório base de imagens de importação padrão.

   Se estiver importando várias imagens para uma única `sku`, insira as imagens em uma coluna chamada `additional_images` (adicione a coluna caso ainda não tenha sido adicionada), separadas por vírgulas. Exemplo: `image02.jpg,image03.jpg`

## Método 2: importar imagens do servidor externo

1. Faça upload das imagens a serem importadas para a pasta designada no servidor externo.

1. Nos dados do CSV, insira a URL completa para cada arquivo de imagem na coluna correta por tipo de imagem (`base_image`, `small_image`, `thumbnail_image` ou `additional_images`).

   ```
   https://example.com/images/image.jpg
   ```

1. Siga as instruções para [importar](data-import.md) os dados.

## Método 3: importar imagens com armazenamento remoto

1. No módulo de Armazenamento remoto, carregue os arquivos de imagem na pasta `var/import/images` ou em uma subpasta, como `var/import/images/product_images`. Esta é a pasta raiz padrão para importar imagens de produtos.

   ```bash
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Começando com a versão Adobe Commerce e Magento Open Source `2.3.2`, o caminho especificado nos _[!UICONTROL Images File Directory]_&#x200B;concatenados para importação no diretório base de imagens: `<remote-storage-root-folder>/var/import/images`. Para versões anteriores do Adobe Commerce e do Magento Open Source, é possível usar uma pasta diferente no servidor do Commerce, desde que o caminho para a pasta seja especificado durante o processo de importação.

1. Nos dados CSV, insira o nome de cada arquivo de imagem a ser importado na linha correta, por `sku`, e na coluna correta, de acordo com o tipo de imagem (`base_image`, `small_image`, `thumbnail_image` ou `additional_images`).

   >[!NOTE]
   >
   >Para imagens na pasta de importação padrão (`var/import/images`), não inclua o caminho antes do nome do arquivo nos dados CSV.

   O arquivo CSV deve incluir somente a coluna `sku` e as colunas de imagem relacionadas.

   ![Exemplo - Importação de dados de imagem CSV](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Siga as instruções para [importar](data-import.md) os dados.

1. Após selecionar o arquivo a ser importado, insira o caminho relativo após **[!UICONTROL Images File Directory]**.

   ```
   var/import/images/product_images
   ```

   >[!TIP]
   >
   >Deixe o _[!UICONTROL Images File Directory]_&#x200B;em branco para usar o diretório `<Magento-root-folder>/var/import/images`. A partir do Adobe Commerce e do Magento Open Source versão 2.3.2, este é o diretório base de imagens de importação padrão.

   Se estiver importando várias imagens para uma única `sku`, insira as imagens em uma coluna chamada `additional_images` (adicione a coluna caso ainda não tenha sido adicionada), separadas por vírgulas: `image02.jpg,image03.jpg`

Para obter mais informações sobre como habilitar e gerenciar o módulo de Armazenamento remoto, consulte [Configurar armazenamento remoto](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) no _Guia de configuração_.

>[!NOTE]
>
>A importação de imagens de produtos não inicia o redimensionamento da imagem. As imagens do produto são redimensionadas no front-end por `pub/get.php`. Verifique se o `pub/get.php` está funcionando corretamente; caso contrário, as imagens podem não ser redimensionadas.
