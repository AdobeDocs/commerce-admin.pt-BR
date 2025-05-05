---
title: Criar um catálogo compartilhado
description: Saiba mais sobre como criar catálogos compartilhados e duplicar catálogos compartilhados existentes.
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Criar um catálogo compartilhado

Quando um [catálogo compartilhado](catalog-shared.md) é criado, o sistema cria automaticamente um [grupo de clientes](account-company-customer-group.md) com o mesmo nome. Por exemplo, se você criar um catálogo compartilhado chamado _Catálogo ABC_, o sistema também criará um grupo de clientes _Catálogo ABC_ correspondente. Atribuir uma empresa ao catálogo personalizado compartilhado é basicamente o mesmo que atribuí-la a um grupo de clientes.

Um novo catálogo compartilhado não inclui produtos, preços personalizados ou associações de empresas. Um catálogo público, que é o catálogo compartilhado padrão criado quando os catálogos compartilhados são ativados, é automaticamente atribuído aos convidados e aos clientes que não estão associados a uma empresa.

![Catálogos compartilhados](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

Os seguintes aspectos de um catálogo compartilhado devem ser configurados antes de ser usado:

- Escopo do catálogo
- Seleção do produto
- Preços personalizados
- Atribuições da empresa

## Escopo de preço

Se você tiver uma instalação multissite, certifique-se de configurar o escopo de preço antes de criar seus catálogos compartilhados. O [escopo de preço](../catalog/catalog-price-scope.md) pode ser definido como `Global` ou `Website`. No entanto, ele só pode ser definido no início do processo de configuração. O seletor de sites aparece durante a etapa 2 da [configuração do catálogo compartilhado](catalog-shared-pricing-structure.md).

![Seletor de sites](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **Catálogo** e escolha **Catálogo** abaixo de.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **Preço**.

1. Definir **Escopo do Preço de Catálogo** para `Website`.

   ![Escopo do Preço de Catálogo](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.

## Etapa 1: criar o catálogo compartilhado

Há duas maneiras de criar um catálogo compartilhado. Você pode criar um catálogo compartilhado de qualquer tipo ou duplicar um catálogo compartilhado existente. Um novo catálogo compartilhado não inclui nenhum produto e ainda não está atribuído a uma empresa.

### Método 1: adicionar um novo catálogo compartilhado

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. No canto superior direito, clique em **[!UICONTROL Add Shared Catalog]** e faça o seguinte:

   - Digite um **[!UICONTROL Name]** para o catálogo compartilhado.

     O nome atribuído é usado em todo o painel de administração e cliente, se aplicável, para fazer referência ao catálogo compartilhado. Ele também se torna o nome do grupo de clientes correspondente.

   - Selecione **[!UICONTROL Type]** : `Custom` ou `Public`.

   - Escolha o **[!UICONTROL Customer Tax Class]** apropriado que se aplica às compras feitas do catálogo compartilhado.

     Para obter mais informações sobre configuração e definição da classe de imposto, consulte [Classes de imposto](../stores-purchase/tax-class.md).

     O exemplo a seguir mostra um novo catálogo personalizado para um cliente grossista específico.

     ![Novo catálogo compartilhado](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - Inserir **[!UICONTROL Description]**

1. Quando terminar, clique em **[!UICONTROL Save]**.

   O novo catálogo aparece na grade _[!UICONTROL Shared Catalogs]_.

### Método 2: duplicar um catálogo compartilhado existente

Um catálogo personalizado duplicado retém o modelo de preço e a estrutura do original, mas não as associações de empresa. Um grupo de clientes correspondente também é criado com o mesmo nome do catálogo duplicado. Por padrão, um catálogo duplicado é denominado _Duplicate of_ do catálogo original.

Se um catálogo compartilhado público for duplicado, o tipo de catálogo duplicado será alterado para `custom`.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para o catálogo compartilhado na grade que você deseja duplicar, vá para a coluna **[!UICONTROL Action]** e selecione **[!UICONTROL General Settings]**.

1. Nas opções na parte superior da página, clique em **[!UICONTROL Duplicate]**.

   ![Duplicar Catálogo Compartilhado](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. Atualize os seguintes campos para o novo catálogo:

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A duplicata aparece na grade _[!UICONTROL Shared Catalogs]_, com uma ID exclusiva.

## Etapa 2: concluir a configuração

Depois de criar um novo catálogo compartilhado, ele deve ser configurado com a seleção de produto apropriada, [atribuições de empresa](catalog-shared-assign-companies.md) e [permissões de categoria](../catalog/category-permissions.md). Para continuar, consulte [Definir preço e estrutura](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[Versão 1.3.0](release-notes.md#b2b-v130) e posterior** do B2B — Quando você cria um catálogo compartilhado, cada [permissão de categoria](../catalog/category-permissions.md) para o catálogo é definida como _[!UICONTROL Allow for the Display Product Prices]_&#x200B;e_[!UICONTROL Add to Cart]_ para grupos de clientes aos quais é atribuído esse acesso nas configurações de permissão do catálogo. Anteriormente, essas configurações eram automaticamente definidas como `Deny`, mesmo quando as permissões do catálogo eram definidas como `Allow`.

## Demonstração do catálogo compartilhado

Para ver uma demonstração do gerenciamento de catálogo compartilhado, assista a este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/344446?quality=12&learn=on)

## Referência de página do catálogo compartilhado

### Barra de botões

| Botão | Descrição |
|--- |--- |
| [!UICONTROL Back] | Retorna à página Catálogos compartilhados sem salvar o novo catálogo compartilhado. |
| [!UICONTROL Reset] | Limpa o formulário de qualquer alteração não salva e restaura as informações detalhadas do catálogo original. |
| [!UICONTROL Save and Continue Edit] | Salva todas as alterações e mantém o formulário aberto no modo de edição. |
| [!UICONTROL Save] | Salva alterações, fecha o formulário e retorna à página Catálogos compartilhados. |

{style="table-layout:auto"}

### Detalhes do catálogo

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Name] | Identifica o catálogo compartilhado em todo o Administrador e nas contas de cliente em que ele está disponível. O nome do catálogo deve ser descritivo e não deve ter mais de 32 caracteres. Você não pode ter dois catálogos compartilhados com o mesmo nome. Máximo de caracteres: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifica um catálogo com preços personalizados que está disponível somente para as empresas específicas às quais ele está atribuído.<br/>**[!UICONTROL Public]**- Identifica o catálogo compartilhado que está disponível para todos os visitantes convidados e clientes conectados que não estão associados a uma empresa. Um catálogo compartilhado público padrão é criado quando [!DNL Adobe Commerce B2B] é instalado, mas deve ser configurado por um administrador de armazenamento. Somente um catálogo público compartilhado pode existir por vez. |
| [!UICONTROL Customer Tax Class] | Determina a classe de imposto usada para compras feitas do catálogo. As opções incluem todas as classes de imposto disponíveis. |
| [!UICONTROL Description] | Uma breve explicação de como o catálogo deve ser usado. |

{style="table-layout:auto"}

### Colunas de grade

| Campo | Descrição |
|--- |--- |
| [!UICONTROL ID] | Um identificador numérico exclusivo atribuído à entidade de catálogo compartilhado. |
| [!UICONTROL Name] | O nome do catálogo compartilhado. |
| [!UICONTROL Type] | Indica o tipo de catálogo compartilhado. Pode ser `Public` ou `Custom`. |
| [!UICONTROL Created At] | A data em que o catálogo compartilhado foi criado no sistema. |
| [!UICONTROL Created By] | O nome do usuário administrador que criou um catálogo compartilhado. |
| [!UICONTROL Action] | A lista de ações. Opções: `Set Pricing and Structure`, `Assign Companies`, `General Settings`, `Delete`. |

{style="table-layout:auto"}
