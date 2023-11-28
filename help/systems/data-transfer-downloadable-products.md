---
title: Importar produtos baixáveis
description: Veja um exemplo de importação de dados do produto para um produto baixável.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Importar produtos baixáveis

O fluxo de importação de produtos baixáveis é o mesmo de [Produtos do pacote](data-transfer-bundle-products.md) ou [Produtos configuráveis](data-transfer-configurable-products.md). A diferença é que um produto para download tem [links para download](../catalog/product-create-downloadable.md) e [amostras para download](../catalog/product-create-downloadable.md) com suas imagens.

O diretório raiz padrão para links e exemplos baixáveis é `<Magento-root-folder>/pub/media/import`. Se o módulo de armazenamento remoto estiver habilitado, o diretório raiz padrão para links para download e exemplos será o `<remote-storage-root-folder>/media/import` diretório.

O arquivo CSV tem colunas separadas para `downloadable_links` e `downloadable_samples`.

- **Imagens de links baixáveis** — No exemplo a seguir, imagens de links baixáveis (`red.jpg` e `black.jpg`) estão no `<Magento-root-folder>/pub/media/import/test` pasta. Se o armazenamento remoto estiver ativado, essas imagens estarão na `<remote-storage-root-folder>/media/import/test` pasta.

  ![Exemplo de dados - produto baixável com links baixáveis](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Imagens de amostra baixáveis** — No exemplo a seguir, a imagem de amostra disponível para download (`white.jpg`) está no `<Magento-root-folder>/pub/media/import/test` pasta. Se o armazenamento remoto estiver ativado, essa imagem estará no estado `<remote-storage-root-folder>/media/import/test` pasta.

  ![Exemplo de dados - produto baixável com amostras baixáveis](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Para obter mais informações sobre como ativar e gerenciar o módulo de armazenamento remoto, consulte [Configurar armazenamento remoto](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) no _Guia de configuração_.
