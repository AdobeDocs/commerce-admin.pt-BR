---
title: Traduzir uma página de conteúdo
description: Saiba como criar uma versão traduzida de cada página que está disponível na exibição de loja específica.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Traduzir uma página de conteúdo

Se sua loja tiver várias exibições em diferentes [idiomas](../stores-purchase/store-localize.md), e você tiver definido o local de cada exibição para um idioma diferente, o resultado será um site parcialmente traduzido. A próxima etapa é criar uma versão traduzida de cada página disponível na exibição de loja específica. A variável [!UICONTROL Store View] coluna da _[!UICONTROL Manage Pages]_A lista mostra cada exibição que tem uma versão traduzida da página.

Para traduzir uma página de conteúdo, é necessário criar outra página que tenha a mesma Chave de URL da original, mas seja atribuída à exibição de loja específica. Em seguida, atualize a página da exibição específica com o texto traduzido. O exemplo a seguir mostra como criar uma versão traduzida do _Sobre nós_ página para a exibição de loja em espanhol.

## Etapa 1: Copiar a chave de URL da página a ser traduzida

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Na grade, localize a página que será traduzida e aberta no _editar_ modo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Search Engine Optimization]** e copie a **[!UICONTROL URL Key]** para a área de transferência.

1. Para retornar ao _[!UICONTROL Pages]_, clique em **[!UICONTROL Back]**na barra de botões superior.

## Etapa 2: adicionar uma página para o conteúdo traduzido

1. Clique em **[!UICONTROL Add New Page]**.

1. Inserir o traduzido **[!UICONTROL Page Title]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Content]** e preencha o texto traduzido para a página.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Search Engine Optimization]** e faça o seguinte:

   - Cole o **[!UICONTROL URL Key]** que você copiou da página original.

   - Insira o texto traduzido para o **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**, e **[!UICONTROL Meta Description]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Page in Websites]** seção e definir **[!UICONTROL Store View]** para a exibição de loja onde a página deve estar disponível.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Design]** e defina a coluna **[!UICONTROL Layout]** da página.

1. Clique em **[!UICONTROL Save]**.

1. Quando solicitado, atualize qualquer arquivo inválido [caches](../systems/cache-management.md).

## Etapa 3: verificar a tradução

Para verificar a tradução, vá para a loja e use o seletor de idioma para alterar a exibição da loja.

Observe que ainda há alguns elementos na página que devem ser traduzidos, incluindo os links do rodapé da empresa [bloco](block-add.md), o [mensagem de boas-vindas](../getting-started/storefront-branding.md#change-the-welcome-message), e [informações do produto](../stores-purchase/store-localize.md#localize-products).
