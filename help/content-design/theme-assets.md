---
title: Ativos de tema
description: Saiba como gerenciar ativos de tema, como CSS, fontes, imagens e arquivos JavaScript.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/8dH6Wuc49gsiL1rIFW-CqJmuqYNqawwearfbgq73Mug
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 0%

---

# Ativos de tema

Os _arquivos estáticos_ são a coleção de ativos, como CSS, fontes, imagens e JavaScript, usada por um tema. O local dos arquivos estáticos está especificado na configuração da [URL Base](../stores-purchase/store-urls.md). Você pode adicionar uma assinatura digital ao URL de cada arquivo estático para permitir que os navegadores detectem quando uma versão mais recente estiver disponível. A versão mais recente do arquivo é usada se a assinatura for diferente do que está armazenado no cache do navegador.

Para uma instalação padrão, os ativos associados a um tema são organizados na pasta `web` no seguinte local abaixo da raiz [!DNL Commerce].

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Adicionar uma assinatura digital a URLs de arquivo estático

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL Developer]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Static Files Settings]**.

   ![Configurações de Arquivos Estáticos](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Defina **[!UICONTROL Sign Static Files]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

| Tipo de arquivo | Descrição |
|--- |--- |
| CSS | Controla o estilo visual associado à capa. Exemplo de local no servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| Fontes | Forneça as fontes disponíveis para serem usadas pelo tema. Local no servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| Imagens | Forneça os ativos gráficos usados pelo tema, incluindo botões, texturas de plano de fundo e assim por diante. Exemplo de local no servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | Rotinas JavaScript específicas por tema e funções chamáveis. Exemplo de local no servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## Mesclar arquivos CSS

Como parte de um esforço para otimizar seu site e reduzir o tempo de carregamento de página, você pode reduzir o número de arquivos CSS separados mesclando-os em um único arquivo condensado. Se você abrir um arquivo CSS mesclado, verá um fluxo contínuo de texto, com quebras de linha removidas. Não é possível editar o arquivo mesclado, portanto, é melhor aguardar até que você saia do modo de desenvolvimento e não faça mais alterações frequentes no CSS.

>[!NOTE]
>
>Os arquivos CSS só podem ser mesclados do painel _Admin_ no [modo de desenvolvedor](../systems/developer-tools.md#operation-modes).

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, **[!UICONTROL Advanced]** e escolha **[!UICONTROL Developer]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL CSS Settings]**.

   ![Configurações de CSS](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Para obter descrições detalhadas sobre essas opções de configuração, consulte [Configurações de CSS](../configuration-reference/advanced/developer.md#css-settings) na _Referência de Configuração_.

1. Defina **[!UICONTROL Merge CSS Files]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Mesclar arquivos do JavaScript

Vários arquivos JavaScript podem ser mesclados em um único arquivo condensado para reduzir o tempo de carregamento da página. Se você abrir um arquivo JavaScript mesclado, verá um fluxo contínuo de texto, com quebras de linha removidas. Se você tiver concluído o processo de desenvolvimento e o código não contiver erros, considere mesclar os arquivos.

>[!NOTE]
>
>Os arquivos do JavaScript podem ser mesclados do painel _Admin_ somente quando estiverem trabalhando no [Modo de Desenvolvedor](../systems/developer-tools.md#operation-modes).

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, **[!UICONTROL Advanced]** e escolha **[!UICONTROL Developer]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL JavaScript Settings]**.

   ![Configurações do JavaScript](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Para obter descrições detalhadas sobre essas opções de configuração, consulte [Configurações do JavaScript](../configuration-reference/advanced/developer.md#javascript-settings) na _Referência de Configuração_.

1. Defina **[!UICONTROL Merge JavaScript Files]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
