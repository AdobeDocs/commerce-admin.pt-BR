---
title: Visão geral do catálogo compartilhado
description: Saiba mais sobre os catálogos compartilhados fornecidos pelo Adobe Commerce B2B e como você pode usá-los para manter catálogos fechados com preços personalizados para diferentes contas da empresa.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Visão geral do catálogo compartilhado

O Adobe Commerce B2B oferece a capacidade de manter fechado _compartilhado_ catálogos com preços personalizados para diferentes empresas. Além do padrão, _principal_, catálogo de produtos, fornece ao cliente acesso a dois tipos de catálogos compartilhados com estruturas de preços diferentes.

Se a variável [Recurso Catálogo compartilhado](enable-basic-features.md) estiver ativado na configuração, o catálogo principal original permanecerá visível do Administrador, mas somente o catálogo público compartilhado padrão (geral) ficará visível na loja. Além disso, é possível criar catálogos personalizados que estejam visíveis somente para membros de [empresa](account-companies.md) contas.

Para o `Default (General)` catálogo compartilhado público, você deve atribuir produtos para exibir o catálogo na loja. Por padrão, está vazio e não contém nenhum produto.

>[!NOTE]
>
>**[Versão 1.3.0 B2B](release-notes.md#b2b-v130) e posterior** — Ao criar um catálogo compartilhado, cada [permissão de categoria](../catalog/category-permissions.md) para o catálogo estiver definido como _[!UICONTROL Allow for the Display Product Prices]_e_[!UICONTROL Add to Cart]_ para grupos de clientes aos quais esse acesso é atribuído nas configurações de permissão do catálogo. Anteriormente, essas configurações eram definidas automaticamente como `Deny` mesmo quando as permissões do catálogo estavam definidas como `Allow`.

>[!IMPORTANT]
>
>Todos os existentes [configurações de permissão de grupo](../configuration-reference/catalog/catalog.md#category-permissions) são ignorados por **_all_** categorias no catálogo quando a variável **_[!UICONTROL Shared Catalog]_** recurso está habilitado. [!UICONTROL Shared Catalog] controla totalmente todas as permissões de categoria no catálogo quando ele é habilitado.

A variável _[!UICONTROL Shared Catalogs]_fornece acesso às ferramentas usadas para gerenciar seus catálogos compartilhados. A página é semelhante ao padrão [Espaço de trabalho do administrador](../getting-started/admin-workspace.md), com filtros e controles de ação. A grade lista todos os catálogos compartilhados, incluindo o catálogo público compartilhado padrão e todos os catálogos personalizados que você configurou.

![Catálogos compartilhados](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Acesse o [!UICONTROL Shared Catalogs] página

No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Controles de ações

A variável [controles de ações](../getting-started/admin-actions-control.md) no canto superior esquerdo pode ser usado com o controle de ações em massa para excluir catálogos compartilhados selecionados que não são mais necessários. Na grade, a variável _[!UICONTROL Actions]_A coluna contém a seleção completa de ferramentas para gerenciar seus catálogos compartilhados.

![Ações de catálogo compartilhado](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| Controle | Descrição |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | Determina a seleção de produto e o preço personalizado disponíveis no catálogo compartilhado. |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | Determina quais empresas podem acessar um catálogo compartilhado. |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | Determina as informações detalhadas do catálogo, incluindo nome, tipo de catálogo, classe de imposto do cliente e descrição. |
| [!UICONTROL Delete] | Exclui os catálogos compartilhados selecionados. |

{style="table-layout:auto"}

## Descrições da coluna

| Cabeçalho | Descrição |
|--- |--- |
| [!UICONTROL Select] | Seleciona registros de catálogo compartilhado para aplicar uma ação. O controle no cabeçalho pode ser usado para selecionar todos ou desmarcar todos os registros de catálogo compartilhados na grade. Para selecionar um catálogo compartilhado individual, marque a caixa de seleção. |
| [!UICONTROL ID] | Um identificador numérico exclusivo atribuído em sequência quando o catálogo é criado. |
| [!UICONTROL Name] | O nome do catálogo compartilhado. Por padrão, o catálogo compartilhado padrão (Geral) está disponível. |
| [!UICONTROL Type] | Identifica o tipo de catálogo compartilhado como: <br/>**[!UICONTROL Public]**- O catálogo público compartilhado padrão é criado automaticamente quando o Adobe Commerce B2B é instalado. É atribuído inicialmente ao `General` e `Not Logged In` grupos de clientes, e é visível para convidados e clientes individuais conectados que não estão associados a uma empresa. O sistema oferece suporte a apenas um catálogo público compartilhado por vez.<br/>**[!UICONTROL Custom]** - Um catálogo compartilhado personalizado contém preços que são visíveis apenas para associados conectados das contas atribuídas da empresa. Você pode criar quantos catálogos compartilhados personalizados forem necessários. |
| [!UICONTROL Customer Tax Class] | A classe de imposto atribuída ao grupo de clientes correspondente. Essa coluna não aparece na grade padrão, mas pode ser adicionada alterando o layout da coluna. |
| [!UICONTROL Created At] | A data e a hora em que o catálogo compartilhado foi criado. |
| [!UICONTROL Created By] | O nome e o sobrenome do administrador de armazenamento que criou o catálogo compartilhado. |
| [!UICONTROL Action] | Lista as ações que serão aplicadas aos catálogos selecionados. Opções: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
