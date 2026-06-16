---
title: Painel de preparo de conteúdo
description: Use o painel de preparo de conteúdo para acessar uma visão geral de todas as campanhas ativas e futuras.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/Hwrb3dYdJlggWN-Z-nUKxVBhsejFMZR-yWIgRzfJifQ
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# Painel de preparo de conteúdo

{{ee-feature}}

O Painel [!UICONTROL Content Staging] fornece uma visão geral de todas as campanhas ativas e futuras. O formato do painel pode ser alterado de uma grade para uma linha do tempo. Também é possível usar filtros para localizar campanhas, personalizar o layout da coluna e salvar diferentes exibições da grade. Para obter mais informações sobre os controles do espaço de trabalho, consulte [Espaço de trabalho de administrador](../getting-started/admin-workspace.md).

![Painel de preparo na exibição de grade](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## Exibir o painel de preparo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Para alterar o formato do painel, defina o controle **[!UICONTROL View As]** como `list`, `Grid` ou `Timeline`.

   ![Modo de exibição de Linha do Tempo](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   Quando a linha do tempo é exibida, o controle deslizante no canto inferior direito pode ser usado para ajustar a exibição de uma a quatro semanas. Cada coluna representa um dia.

1. Se a linha do tempo for exibida, arraste o controle deslizante até a posição `4w` na extremidade direita para exibir um período de tempo mais longo.

   ![Exibição de quatro semanas](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. Para exibir informações gerais sobre a campanha, clique em qualquer item na página.

   - Para abrir a campanha, clique em **[!UICONTROL View/Edit]**.

   - Para ver a aparência da campanha para os clientes da loja naquele dia, clique em **[!UICONTROL Preview]**.

   ![Informações da campanha](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## Descrições da coluna do painel de preparação

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Status] | Status da campanha. `Active` ou `Upcoming`. |
| [!UICONTROL Update Name] | O nome da campanha. |
| [!UICONTROL Includes] | Define quantos objetos são incluídos na campanha. |
| [!UICONTROL Start Time] | A data em que a campanha começa. |
| [!UICONTROL End Time] | A data em que a campanha termina. |
| [!UICONTROL Description] | Descrição adicional de cada campanha. |
| [!UICONTROL Action] | As ações que podem ser aplicadas a um registro individual incluem:<br/>**[!UICONTROL View/Edit]**- Abre a campanha no modo de edição.<br/>**[!UICONTROL Preview]** - Exibe a campanha no modo de visualização. |

{style="table-layout:auto"}

## Editar uma campanha

Os objetos de campanha existentes podem ser editados no painel de preparo, exceto para campanhas de regra de preço que não têm datas de término.

>[!NOTE]
>
>Se uma campanha ativa for criada inicialmente sem uma data de término, a campanha não poderá ser editada posteriormente para incluir uma data de término. Nesse caso, é necessário criar uma campanha duplicada e inserir a data final necessária.

![Detalhes da campanha](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

A campanha neste exemplo inclui duas categorias e três produtos individuais.

Siga as etapas abaixo para editar qualquer um dos objetos nesta campanha.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Encontre a campanha na lista ou linha do tempo exibida e abra-a para acessar os detalhes:

   - Para exibir uma lista, clique em **[!UICONTROL Select]** e depois em **[!UICONTROL View/Edit]** na coluna _[!UICONTROL Action]_.
   - Para exibir uma linha do tempo, clique uma vez para exibir o resumo e clique em **[!UICONTROL View/Edit]**.

1. Atualize qualquer uma das configurações na seção _[!UICONTROL General]_, conforme necessário.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) qualquer seção que contenha um item a ser editado.

   ![Atualizando os produtos atribuídos de um item de campanha](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save]**.
