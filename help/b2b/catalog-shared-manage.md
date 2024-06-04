---
title: Gerenciar seus catálogos compartilhados
description: Saiba mais sobre as informações e as ferramentas disponíveis na página Catálogos compartilhados.
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Gerenciar seus catálogos compartilhados

A variável _[!UICONTROL Shared Catalogs]_fornece acesso às ferramentas necessárias para gerenciar seus catálogos compartilhados. A página é semelhante ao espaço de trabalho padrão de Administração, com filtros e controles de ação. A grade lista todos os catálogos compartilhados, incluindo o catálogo público compartilhado padrão e todos os catálogos personalizados que você configurou.

## Atualizar a seleção de produtos

A seleção de produtos em qualquer catálogo compartilhado pode ser facilmente atualizada no _[!UICONTROL Action]_coluna da grade de catálogos compartilhados. As alterações feitas estão visíveis para os membros de qualquer conta da empresa associada. O processo é basicamente o mesmo que escolher produtos para um novo [estrutura do catálogo](catalog-shared-pricing-structure.md), exceto que o escopo da configuração não pode ser alterado.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para o catálogo compartilhado na grade, vá para a **[!UICONTROL Action]** e selecione **[!UICONTROL Set Pricing and Structure]**.

   ![Grade de catálogo compartilhada e menu de ação](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Siga as instruções em [Etapa 2: Escolher produtos](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   Você pode ignorar o primeiro item, pois o escopo de um catálogo compartilhado não pode ser alterado após ser salvo pela primeira vez.

Se estiver trabalhando com um produto específico, a variável _[!UICONTROL Products In Shared Catalog]_listar cada catálogo compartilhado em que o produto está disponível. Para saber mais, consulte [Adicionar produtos a um catálogo compartilhado](catalog-shared-product-add.md).

![Produto em catálogos compartilhados](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Atualizar preços personalizados

Os preços personalizados de produtos em qualquer catálogo compartilhado podem ser facilmente atualizados na coluna Ação da grade Catálogos compartilhados. As alterações feitas estão visíveis na loja para membros da empresa associada ou grupo de clientes. O processo é basicamente o mesmo que definir preços personalizados para um novo [catálogo compartilhado](catalog-shared-pricing-structure.md), exceto que o escopo da configuração não pode ser alterado.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para o catálogo compartilhado na grade que você deseja atualizar, vá para a **[!UICONTROL Action]** e selecione **[!UICONTROL Set Pricing and Structure]**.

1. No _[!UICONTROL Catalog Structure]_clique em **[!UICONTROL Configure]**e siga um destes procedimentos:

   - No indicador de progresso, na parte superior da página, clique em **[!UICONTROL Pricing]**.
   - No canto superior direito, clique em **[!UICONTROL Next]**.

1. Siga as instruções em [Etapa 3: Definir preços personalizados](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Atualizar permissões de categoria

[Permissões de categoria](../catalog/category-permissions.md) são automaticamente definidos como `Allow` para produtos adicionados da árvore de categorias a um catálogo compartilhado. Posteriormente, você pode ajustar as permissões ou criar regras adicionais, conforme necessário.

>[!NOTE]
>
>**[Versão 1.3.0 B2B](release-notes.md#b2b-v130) e posterior** — Ao criar um catálogo compartilhado, cada [permissão de categoria](../catalog/category-permissions.md) para o catálogo estiver definido como `Allow` para o _[!UICONTROL Display Product Prices]_e_[!UICONTROL Add to Cart]_ para grupos de clientes aos quais esse acesso é atribuído nas configurações de permissão do catálogo. Anteriormente, essas configurações eram definidas automaticamente como `Deny` mesmo quando as permissões do catálogo estavam definidas como `Allow`.

>[!IMPORTANT]
>
>Todos os existentes [configurações de permissão de grupo](../configuration-reference/catalog/catalog.md#category-permissions) são ignorados por **_all_** categorias no catálogo quando a variável **_[!UICONTROL Shared Catalog]_** recurso está habilitado. [!UICONTROL Shared Catalog] controla totalmente todas as permissões de categoria no catálogo quando ele é habilitado.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Na árvore de categorias, selecione a categoria dos produtos que deseja atualizar.

   Para incluir todos os produtos, selecione a categoria de nível superior na árvore.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Category Permissions]** seção.

1. Clique em **[!UICONTROL New Permission]** e faça o seguinte:

   ![Nova permissão](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Escolha o **[!UICONTROL Customer Group]** que corresponde ao catálogo compartilhado e altere as configurações de permissão conforme necessário.

     ![Regra de permissões de categoria](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Para criar uma regra de permissões para outro grupo de clientes, clique em **[!UICONTROL New Permissions]** e repita o processo.

   - Para excluir uma regra de permissão, clique no link _Excluir_ ![Lixeira](../assets/icon-delete-trashcan-solid.png) ícone.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Atualizar os detalhes do catálogo

As informações detalhadas de qualquer catálogo compartilhado podem ser facilmente atualizadas na coluna Ação da grade Catálogos compartilhados. As alterações feitas são refletidas em qualquer conta da empresa associada.

![Configurações gerais](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para o catálogo compartilhado que você deseja atualizar, vá para a **[!UICONTROL Action]** e selecione **[!UICONTROL General Settings]**.

   ![Detalhes do catálogo](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Atualize as informações detalhadas do catálogo conforme necessário.

   - Alterar o nome de um catálogo compartilhado também altera o nome do grupo de clientes correspondente.
   - Alteração do tipo de catálogo de `Custom` para `Public` converte o catálogo público existente em um catálogo personalizado. Todas as empresas associadas ao catálogo público original são reatribuídas à substituição. Um catálogo público não pode ser convertido em um catálogo personalizado.

1. Quando terminar, clique em **[!UICONTROL Save]**.

## Referência de página do catálogo compartilhado

### Barra de botões

| Botão | Descrição |
|--- |--- |
| [!UICONTROL Back] | Retorna à página Catálogos compartilhados sem salvar o novo catálogo compartilhado. |
| [!UICONTROL Delete] | Exclui o catálogo e reatribui qualquer empresa associada e seus membros ao catálogo público compartilhado. |
| [!UICONTROL Reset] | Limpa o formulário de qualquer alteração não salva e restaura as informações detalhadas do catálogo original. |
| [!UICONTROL Duplicate] | Cria um [cópia duplicada do catálogo](catalog-shared-create.md). Para um catálogo personalizado, o modelo de precificação e a estrutura do original, mas sem as associações de empresa. Se um catálogo compartilhado público for duplicado, o tipo de catálogo duplicado será alterado para `custom`. Um grupo de clientes correspondente também é criado com o mesmo nome do catálogo duplicado. Por padrão, um catálogo duplicado é nomeado como _Duplicar de_ o catálogo original. |
| [!UICONTROL Save and Continue Edit] | Salva todas as alterações e mantém o formulário aberto no modo de edição. |
| [!UICONTROL Save] | Salva alterações, fecha o formulário e retorna à página Catálogos compartilhados. |

{style="table-layout:auto"}

### Detalhes do catálogo

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Name] | Identifica o catálogo compartilhado em todo o Administrador e nas contas de cliente em que ele está disponível. O nome do catálogo deve ser descritivo e não deve ter mais de 32 caracteres. Você não pode ter dois catálogos compartilhados com o mesmo nome. Máximo de caracteres: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifica um catálogo com preços personalizados que está disponível somente para as empresas específicas às quais ele está atribuído.<br/>**[!UICONTROL Public]**- Identifica o catálogo compartilhado que está disponível para todos os visitantes convidados e para clientes conectados que não estão associados a uma empresa. Um catálogo público compartilhado &quot;padrão&quot; é criado quando o Adobe Commerce B2B é instalado, mas deve ser configurado pelo administrador. Somente um catálogo público compartilhado pode existir por vez. |
| [!UICONTROL Customer Tax Class] | Determina a classe de imposto usada para compras feitas do catálogo. As opções incluem todas as classes de imposto disponíveis. |
| [!UICONTROL Description] | Uma breve explicação de como o catálogo deve ser usado. |

{style="table-layout:auto"}
