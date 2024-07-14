---
title: Grupos de clientes
description: Use grupos de clientes para determinar quais descontos estão disponíveis para clientes atribuídos a um grupo e a classe de imposto associada ao grupo.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: c2fd228311a4b990be9c1409d2cdd2b5677fe2af
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Grupos de clientes

Os grupos de clientes determinam quais descontos estão disponíveis e a classe de imposto associada ao grupo. Os grupos de clientes padrão são `General`, `Not Logged In` e `Wholesale`.

![Grupos de Clientes](assets/customer-groups.png){width="700" zoomable="yes"}

## Filtrar a lista [!UICONTROL Customer Groups]

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Clique em **[!UICONTROL Filters]**.

1. Informe os critérios para grupos de pesquisa, incluindo uma faixa de IDs, grupo ou classe de imposto.

   ![Opções de Filtragem](assets/groups-filters.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Apply Filters]**.

## Criar um grupo de clientes

>[!NOTE]
>
>Os usuários administradores que não têm acesso a todos os sites (aos quais foi atribuída uma função com um [!UICONTROL Role Scope] &#39;Personalizado&#39;) não podem criar, modificar ou excluir grupos de clientes.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Clique em **[!UICONTROL Add New Customer Group]**.

1. Para [!DNL **Group Name]**, insira um nome exclusivo com menos de 32 caracteres para identificar o grupo.

1. Selecione o **[!UICONTROL Tax Class]** que se aplica ao grupo.

   ![Informações do Grupo](assets/group-information.png){width="600" zoomable="yes"}

1. Selecione o **[!UICONTROL Excluded Website(s)]** que deseja excluir do grupo.

   >[!IMPORTANT]
   >
   >A exclusão de sites pode diminuir o tempo de indexação do preço do produto e da regra de catálogo, pois os sites excluídos não são indexados. Quando um grupo de clientes é salvo com uma exclusão de site adicionada, o preço do produto, a regra de catálogo e os índices de pesquisa de catálogo são invalidados. Se você tiver muitos produtos, sites e grupos de clientes, é recomendável pausar o processo de reindexação até excluir sites dos grupos de clientes.

   Nenhum site é excluído por padrão. Para selecionar vários valores, mantenha pressionada a tecla _Ctrl_ (PC) ou a tecla _Command_ (Mac) e clique em cada opção.

1. Quando terminar, clique em **[!UICONTROL Save Customer Group]**.

## Editar um grupo de clientes

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Abra o registro no modo de edição.

1. Faça as alterações necessárias.

1. Quando terminar, clique em **[!UICONTROL Save Customer Group]**.

## Atribuir um cliente a um grupo diferente

>[!NOTE]
>
>Depois de alterar o grupo de empresas, um usuário da empresa deve fazer logoff e logon na Loja para ver os novos preços no catálogo.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Localize o cliente na lista e marque a caixa de seleção na primeira coluna.

1. Defina o controle **Ações** como `Assign a Customer Group` e escolha o grupo no menu.

   ![Atribuir um Grupo de Clientes](assets/group-assign.png){width="600" zoomable="yes"}

1. Quando for solicitada a confirmação, clique em **OK**.

## Associar um grupo de clientes com descontos específicos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _Promoções_ > **[!UICONTROL Cart Price Rules]**.

1. Selecione a regra de preço do carrinho na qual você deseja associar um grupo ao desconto aplicado ou [criar uma regra de preço](../merchandising-promotions/price-rules-catalog.md).

1. Selecione os grupos de clientes aos quais a regra se aplica.

   ![Grupo de Clientes para Descontos Específicos](assets/group-discount.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save]**.

>[!NOTE]
>
> Você também pode usar a Precificação antecipada para aplicar descontos de produto a grupos de clientes. Consulte [Preços avançados](../catalog/product-price-group.md).

## Excluir um grupo de clientes

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Abra o registro no modo de edição.

1. Na barra de botões, clique em **[!UICONTROL Delete Customer Group]**.

1. Quando for solicitada a confirmação, clique em **OK**.

## Demonstração de grupos de clientes

Saiba mais sobre como criar grupos de clientes assistindo a esta demonstração:

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
