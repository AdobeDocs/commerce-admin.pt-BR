---
title: Traduzir uma página de conteúdo
description: Saiba como criar uma versão traduzida de cada página que está disponível na exibição de loja específica.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Traduzir uma página de conteúdo

Se o armazenamento tiver várias exibições em diferentes [idiomas](../stores-purchase/store-localize.md) e você tiver definido a localidade de cada exibição para um idioma diferente, o resultado será um site parcialmente traduzido. A próxima etapa é criar uma versão traduzida de cada página disponível na exibição de loja específica. A coluna [!UICONTROL Store View] da lista _[!UICONTROL Manage Pages]_&#x200B;mostra cada exibição que tem uma versão traduzida da página.

Para traduzir uma página de conteúdo, é necessário criar outra página que tenha a mesma Chave de URL da original, mas seja atribuída à exibição de loja específica. Em seguida, atualize a página da exibição específica com o texto traduzido. O exemplo a seguir mostra como criar uma versão traduzida da página _Sobre nós_ para a exibição de loja em espanhol.

## Etapa 1: Copiar a chave de URL da página a ser traduzida

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Na grade, localize a página a ser traduzida e aberta no modo _editar_.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]** e copie o **[!UICONTROL URL Key]** para a área de transferência.

1. Para retornar à grade _[!UICONTROL Pages]_, clique em **[!UICONTROL Back]**&#x200B;na barra de botões superior.

## Etapa 2: adicionar uma página para o conteúdo traduzido

1. Clique em **[!UICONTROL Add New Page]**.

1. Inserir o **[!UICONTROL Page Title]** traduzido.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Content]** e conclua o texto traduzido para a página.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Search Engine Optimization]** e faça o seguinte:

   - Cole o **[!UICONTROL URL Key]** que você copiou da página original.

   - Insira o texto traduzido para **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]** e **[!UICONTROL Meta Description]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Page in Websites]** e defina **[!UICONTROL Store View]** para o modo de exibição de repositório onde a página estará disponível.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Design]** e defina a coluna **[!UICONTROL Layout]** da página.

1. Clique em **[!UICONTROL Save]**.

1. Quando solicitado, atualize todos os [caches](../systems/cache-management.md) inválidos.

## Etapa 3: verificar a tradução

Para verificar a tradução, vá para a loja e use o seletor de idioma para alterar a exibição da loja.

Observe que ainda há alguns elementos na página que devem ser traduzidos, incluindo os links de rodapé da empresa [bloco](block-add.md), a [mensagem de boas-vindas](../getting-started/storefront-branding.md#change-the-welcome-message) e as [informações sobre o produto](../stores-purchase/store-localize.md#localize-products).
