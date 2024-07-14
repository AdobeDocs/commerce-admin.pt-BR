---
title: '[!DNL Google Content Experiments]'
description: Saiba como usar o [!DNL Google Content Experiments] para configurar um teste A/B de produtos, categorias ou páginas de conteúdo do Commerce.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

O exemplo a seguir mostra como configurar um teste A/B de produtos, categorias ou páginas de conteúdo usando experimentos de conteúdo do Google Analytics. Recomendamos que você mantenha duas guias do navegador abertas ao trabalhar com as instruções, pois é necessário que você pule de um lado para o outro entre o Administrador do Commerce e sua conta do [!DNL Google Analytics].

>[!NOTE]
>
>[!DNL Google Content Experiments] foi descontinuado e está agendado para substituição por [Google Otimize](https://support.google.com/optimize/answer/7084762?hl=en).

## Etapa 1. Ativar experimentos de conteúdo (Commerce)

1. Faça logon no Admin da sua instalação do Commerce.

1. Siga as instruções para habilitar [Google Analytics](google-analytics.md) com Experimentos de Conteúdo na configuração do Commerce.

   ![Configuração de vendas - API Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Etapa 2. Configurar as variações (Commerce)

Crie várias variações do mesmo produto, categoria ou página.

- Cada variação deve ter uma [chave de URL](../catalog/catalog-urls.md) exclusiva.
- Cada variação deve ter a mesma [exibição de repositório](../getting-started/websites-stores-views.md#scope-settings) selecionada.

Você pode criar até dez variações de cada entidade que deseja testar. Para produtos, use [Salvar e duplicar](../catalog/product-workspace.md) para economizar tempo.

## Etapa 3. Configurar o experimento (Google)

>[!NOTE]
>
>Você deve ter as permissões apropriadas para que a conta do Google crie um experimento.

1. Abra outra guia do navegador e faça logon em sua conta do [Google Analytics][2].

   Se necessário, navegue até **[!UICONTROL Account]** e **[!UICONTROL Property]**.

1. Na barra lateral à esquerda, escolha **[!UICONTROL Admin]** e use um dos seguintes métodos:

   **Método 1:** Escolher uma Exibição Existente

   No cabeçalho da coluna _[!UICONTROL View]_, clique na seta para baixo e escolha a exibição que fornecerá os dados para o experimento.

   **Método 2:** Criar um Novo Modo de Exibição de Relatório

   - No cabeçalho da coluna _Exibir_, clique em **[!UICONTROL Create View]** e faça o seguinte:

      - Identifique o local do experimento como `Website` ou `Mobile app`.

      - Insira um **[!UICONTROL Reporting View Name]** descritivo.

      - Especifique o **[!UICONTROL Reporting Time Zone]**.

   - Quando terminar, clique em **[!UICONTROL Create View]** e, em seguida, clique na seta para trás para retornar à página anterior.

1. No painel esquerdo, em _[!UICONTROL Reports]_, escolha **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Clique em **[!UICONTROL Create experiment]** e faça o seguinte:

   - Especifique a porcentagem de tráfego a ser redirecionada.

   - Especifique o **[!UICONTROL Original Page URL]** e as URLs de cada **[!UICONTROL page variation]** que você deseja testar.

   - Complete as outras opções.

1. Quando o experimento estiver configurado, clique em **[!UICONTROL Manually Insert the Code]** e copie o trecho de código.

## Etapa 4. Colar trecho de código (Commerce)

1. Retorne ao Administrador da instalação do Commerce e abra a versão original do produto, categoria ou página no modo de edição.

1. Expanda a seção **[!UICONTROL View Optimization]** do produto, categoria ou página.

1. Cole o trecho de código copiado do Google Analytics na caixa de texto **[!UICONTROL Experiment Code]**.

   >[!NOTE]
   >
   >Não cole o trecho de código em nenhuma das variações.

   ![Otimização de exibição do produto](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Etapa 5: revise e inicie o experimento (Google)

1. Retorne à sua conta do [Google Analytics][2].

1. Revise as configurações do experimento.

1. Se estiver pronto para começar, clique em **[!UICONTROL Start Experiment]**.

   Caso contrário, clique em **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
