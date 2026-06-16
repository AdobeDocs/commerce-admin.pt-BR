---
title: As ferramentas e o espaço de trabalho do administrador
description: Saiba mais sobre o espaço de trabalho de Administração, que fornece acesso a todas as ferramentas, dados e conteúdo usados para executar sua loja.
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
TQID: https://experienceleague.adobe.com/RGT21TI5joLEYx3fiOErU5ZoIrXsq0nqZpnI8c40hz4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 528
ht-degree: 0%

---

# As ferramentas e o espaço de trabalho do administrador

O espaço de trabalho de Administrador fornece acesso a todas as ferramentas, dados e conteúdo usados para executar sua loja. A página de inicialização padrão pode ser definida na configuração. Muitas páginas de Administrador têm uma grade que lista os dados da seção, com um conjunto de ferramentas para pesquisar, classificar, filtrar, selecionar e aplicar ações. Por padrão, o [Painel](admin-dashboard.md) é a página de inicialização do Administrador. No entanto, você pode escolher qualquer outra página para aparecer como a página de inicialização ao fazer logon. Você pode clicar no logotipo na barra lateral Admin para retornar à página de inicialização do Admin.

![Administrador - espaço de trabalho](./assets/admin-workspace.png){zoomable="yes"}

## Controles do Workspace

| Controle | Descrição |
|--- |--- |
| [!UICONTROL Global Search] | O ícone de pesquisa na parte superior direita pode ser usado para localizar qualquer valor no banco de dados, incluindo registros de produto, cliente e pedido. |
| [!UICONTROL Grid Search] | A caixa de pesquisa acima da grade pode ser usada para filtrar rapidamente a exibição da grade com base nas palavras-chave encontradas nos registros. |
| [!UICONTROL Sort] | O cabeçalho de cada coluna pode ser usado para classificar a lista em ordem crescente ou decrescente. |
| [!UICONTROL Filters] | Define um conjunto de parâmetros de pesquisa que determina os registros que aparecem na grade. Além disso, os filtros no cabeçalho de algumas colunas podem ser usados para limitar a lista a valores específicos. Alguns filtros têm opções adicionais que podem ser selecionadas em uma caixa de listagem. |
| [!UICONTROL Default View] | Determina o layout de coluna padrão da grade. |
| [!UICONTROL Columns] | Determina a seleção de [colunas](admin-grid-controls.md) e sua ordem na grade. O layout da coluna pode ser alterado e salvo como uma _exibição_. Por padrão, apenas algumas colunas são incluídas na grade. |
| [!UICONTROL Paginate] | Os controles de paginação são usados para exibir as páginas adicionais de resultados. |
| [!UICONTROL Actions] | O controle Actions aplica uma operação a todos os registros selecionados. |
| [!UICONTROL Select] | O controle Select é usado para selecionar vários registros que devem ser o destino da ação. Opções: `Select All` / `Deselect All` |

{style="table-layout:auto"}

## Pesquisa no Workspace

Para localizar qualquer registro no banco de dados, use o ícone de lupa no cabeçalho do _Administrador_. Os resultados podem incluir clientes, produtos, pedidos ou qualquer atributo relacionado. Por exemplo, se você informar um nome de cliente, os resultados poderão incluir o registro do cliente e quaisquer ordens associadas ao nome.

![Ferramenta de pesquisa do administrador](./assets/admin-search.png){width="700" zoomable="yes"}

1. No cabeçalho, clique no ícone _Pesquisar_ (![lupa](../assets/icon-magnify-search.png)) para abrir a caixa de pesquisa.

1. Siga um destes procedimentos:

   - Para localizar uma correspondência aproximada, insira as primeiras letras do que deseja localizar.
   - Para localizar uma correspondência exata, digite a palavra ou várias palavras que deseja localizar.

1. Nos resultados da pesquisa exibidos, clique em qualquer item para abrir o registro.

## Alterar a página de inicialização do administrador

O [painel](admin-workspace.md#the-dashboard) é a página de inicialização padrão do Administrador, embora você possa configurar uma página de inicialização diferente.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel de navegação esquerdo, em **[!UICONTROL Advanced]**, escolha **[!UICONTROL Admin]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Startup Page]**.

   ![Configuração avançada - Configuração da página de inicialização do administrador](./assets/admin-startup-page.png){width="600"}

1. Defina **[!UICONTROL Startup Page]** na página que você deseja que apareça primeiro depois de fazer logon como Administrador.

   Para obter uma lista detalhada de todas as opções de Administrador, consulte [Administrador](../configuration-reference/advanced/admin.md) na _Referência de configuração_.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
