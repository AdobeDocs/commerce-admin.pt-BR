---
title: '[!DNL Google Content Experiments]'
description: Saiba como usar o [!DNL Google Content Experiments] para configurar um teste A/B de produtos, categorias ou páginas de conteúdo do Commerce.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

O exemplo a seguir mostra como configurar um teste A/B de produtos, categorias ou páginas de conteúdo usando experimentos de conteúdo do Google Analytics. Recomendamos que você mantenha duas guias do navegador abertas ao trabalhar com as instruções, pois é necessário alternar entre o Administrador do Commerce e o [!DNL Google Analytics] conta.

>[!NOTE]
>
>[!DNL Google Content Experiments] foi descontinuado e está agendado para substituição por [Otimização do Google](https://support.google.com/optimize/answer/7084762?hl=en).

## Etapa 1. Habilitar experimentos de conteúdo (Commerce)

1. Faça logon no Administrador da instalação do Commerce.

1. Siga as instruções para habilitar [Google Analytics](google-analytics.md) com experimentos de conteúdo na configuração Comércio.

   ![Configuração de vendas - API do Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Etapa 2. Configurar as variações (Comércio)

Crie várias variações do mesmo produto, categoria ou página.

- Cada variação deve ter um único [Chave do URL](../catalog/catalog-urls.md).
- Cada variação deve ter o mesmo [exibição de loja](../getting-started/websites-stores-views.md#scope-settings) selecionado.

Você pode criar até dez variações de cada entidade que deseja testar. Para produtos, use [Salvar e duplicar](../catalog/product-workspace.md) para economizar tempo.

## Etapa 3. Configurar o experimento (Google)

>[!NOTE]
>
>Você deve ter as permissões apropriadas para que a conta do Google crie um experimento.

1. Abra outra guia do navegador e faça logon na [Google Analytics][2] conta.

   Se necessário, navegue até o **[!UICONTROL Account]** e **[!UICONTROL Property]**.

1. Na barra lateral à esquerda, escolha **[!UICONTROL Admin]** e use um dos seguintes métodos:

   **Método 1:** Escolher uma visualização existente

   No cabeçalho do _[!UICONTROL View]_clique na seta para baixo e escolha a visualização que fornecerá os dados para o experimento.

   **Método 2:** Criar um Novo Modo de Exibição de Relatório

   - No cabeçalho do _Exibir_ clique em **[!UICONTROL Create View]** e faça o seguinte:

      - Identifique o local do experimento como `Website` ou `Mobile app`.

      - Insira um descritivo **[!UICONTROL Reporting View Name]**.

      - Especifique a **[!UICONTROL Reporting Time Zone]**.

   - Quando terminar, clique em **[!UICONTROL Create View]** e, em seguida, clique na seta para trás para retornar à página anterior.

1. No painel esquerdo, em _[!UICONTROL Reports]_, escolha **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Clique em **[!UICONTROL Create experiment]** e faça o seguinte:

   - Especifique a porcentagem de tráfego a ser redirecionada.

   - Especifique a **[!UICONTROL Original Page URL]** e os URLs de cada **[!UICONTROL page variation]** que você deseja testar.

   - Complete as outras opções.

1. Quando o experimento estiver configurado, clique em **[!UICONTROL Manually Insert the Code]** e copie o trecho de código.

## Etapa 4. Colar trecho de código (Commerce)

1. Retorne ao administrador da instalação do Commerce e abra a versão original do produto, categoria ou página no modo de edição.

1. Expanda a **[!UICONTROL View Optimization]** para o produto, categoria ou página.

1. Cole o trecho de código que você copiou do Google Analytics na **[!UICONTROL Experiment Code]** texto.

   >[!NOTE]
   >
   >Não cole o trecho de código em nenhuma das variações.

   ![Otimização da visualização do produto](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Etapa 5: revise e inicie o experimento (Google)

1. Retorne ao [Google Analytics][2] conta.

1. Revise as configurações do experimento.

1. Se estiver pronto para começar, clique em **[!UICONTROL Start Experiment]**.

   Caso contrário, clique **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
