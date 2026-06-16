---
title: Importar produtos baixáveis
description: Veja um exemplo de importação de dados do produto para um produto baixável.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/a62y8GDLpN0PHxlm8EYHHMsHfzzkjB4mSNa-BV78Ra8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Importar produtos baixáveis

O fluxo de importação de produtos baixáveis é o mesmo de [Produtos do Pacote](data-transfer-bundle-products.md) ou [Produtos Configuráveis](data-transfer-configurable-products.md). A diferença é que um produto baixável tem [links baixáveis](../catalog/product-create-downloadable.md) e [amostras baixáveis](../catalog/product-create-downloadable.md) com suas imagens.

O diretório raiz padrão para links e exemplos baixáveis é `<Magento-root-folder>/pub/media/import`. Se o módulo de armazenamento remoto estiver habilitado, o diretório raiz padrão para links e exemplos baixáveis será o diretório `<remote-storage-root-folder>/media/import`.

O arquivo CSV tem colunas separadas para `downloadable_links` e `downloadable_samples`.

- **Imagens de links baixáveis** — No exemplo a seguir, as imagens de links baixáveis (`red.jpg` e `black.jpg`) estão na pasta `<Magento-root-folder>/pub/media/import/test`. Se o armazenamento remoto estiver habilitado, essas imagens estarão na pasta `<remote-storage-root-folder>/media/import/test`.

  ![Dados de exemplo - produto baixável com links baixáveis](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Imagens de exemplo baixáveis** — No exemplo a seguir, a imagem de exemplo baixável (`white.jpg`) está na pasta `<Magento-root-folder>/pub/media/import/test`. Se o armazenamento remoto estiver habilitado, esta imagem estará na pasta `<remote-storage-root-folder>/media/import/test`.

  ![Exemplo de dados - produto baixável com amostras baixáveis](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Para obter mais informações sobre como habilitar e gerenciar o módulo de armazenamento remoto, consulte [Configurar armazenamento remoto](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) no _Guia de configuração_.
