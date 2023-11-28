---
title: Criar um catálogo compartilhado
description: Saiba mais sobre como criar catálogos compartilhados e duplicar catálogos compartilhados existentes.
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Criar um catálogo compartilhado

Quando um [catálogo compartilhado](catalog-shared.md) for criada, o sistema criará automaticamente uma [grupo de clientes](account-company-customer-group.md) pelo mesmo nome. Por exemplo, se você criar um catálogo compartilhado chamado _Catálogo ABC_, o sistema também cria um correspondente _Catálogo ABC_ grupo de clientes. Atribuir uma empresa ao catálogo personalizado compartilhado é basicamente o mesmo que atribuí-la a um grupo de clientes.

Um novo catálogo compartilhado não inclui produtos, preços personalizados ou associações de empresas. Um catálogo público, que é o catálogo compartilhado padrão criado quando os catálogos compartilhados são ativados, é automaticamente atribuído aos convidados e aos clientes que não estão associados a uma empresa.

![Catálogos compartilhados](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

Os seguintes aspectos de um catálogo compartilhado devem ser configurados antes de ser usado:

- Escopo do catálogo
- Seleção do produto
- Preços personalizados
- Atribuições da empresa

## Escopo de preço

Se você tiver uma instalação multissite, certifique-se de configurar o escopo de preço antes de criar seus catálogos compartilhados. A variável [escopo de preço](../catalog/catalog-price-scope.md) pode ser definido como `Global` ou `Website`. No entanto, ele só pode ser definido no início do processo de configuração. O seletor de sites aparece durante a etapa 2 do [configuração do catálogo compartilhado](catalog-shared-pricing-structure.md).

![Seletor de sites](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **Catálogo** e escolha **Catálogo** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **Preço** seção.

1. Definir **Escopo do Preço de Catálogo** para `Website`.

   ![Escopo do Preço de Catálogo](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.

## Etapa 1: criar o catálogo compartilhado

Há duas maneiras de criar um catálogo compartilhado. Você pode criar um catálogo compartilhado de qualquer tipo ou duplicar um catálogo compartilhado existente. Um novo catálogo compartilhado não inclui nenhum produto e ainda não está atribuído a uma empresa.

### Método 1: adicionar um novo catálogo compartilhado

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. No canto superior direito, clique em **[!UICONTROL Add Shared Catalog]** e faça o seguinte:

   - Insira um **[!UICONTROL Name]** para o catálogo compartilhado.

     O nome atribuído é usado em todo o painel de administração e cliente, se aplicável, para fazer referência ao catálogo compartilhado. Ele também se torna o nome do grupo de clientes correspondente.

   - Selecionar **[!UICONTROL Type]** : `Custom` ou `Public`.

   - Escolha o **[!UICONTROL Customer Tax Class]** que se aplica às compras feitas no catálogo compartilhado.

     Para obter mais informações sobre configuração e definição de classe de imposto, consulte [Classes de imposto](../stores-purchase/tax-class.md).

     O exemplo a seguir mostra um novo catálogo personalizado para um cliente grossista específico.

     ![Novo catálogo compartilhado](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - Enter **[!UICONTROL Description]**

1. Quando terminar, clique em **[!UICONTROL Save]**.

   O novo catálogo aparece na variável _[!UICONTROL Shared Catalogs]_grade.

### Método 2: duplicar um catálogo compartilhado existente

Um catálogo personalizado duplicado retém o modelo de preço e a estrutura do original, mas não as associações de empresa. Um grupo de clientes correspondente também é criado com o mesmo nome do catálogo duplicado. Por padrão, um catálogo duplicado é nomeado como _Duplicar de_ o catálogo original.

Se um catálogo compartilhado público for duplicado, o tipo de catálogo duplicado será alterado para `custom`.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para o catálogo compartilhado na grade que você deseja duplicar, vá para a **[!UICONTROL Action]** e selecione **[!UICONTROL General Settings]**.

1. Nas opções na parte superior da página, clique em **[!UICONTROL Duplicate]**.

   ![Duplicar catálogo compartilhado](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. Atualize os seguintes campos para o novo catálogo:

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A duplicata aparece na caixa _[!UICONTROL Shared Catalogs]_grade, com um identificador exclusivo.

## Etapa 2: concluir a configuração

Depois de criar um novo catálogo compartilhado, ele deve ser configurado com a seleção de produto apropriada, [atribuições da empresa](catalog-shared-assign-companies.md), e [permissões de categoria](../catalog/category-permissions.md). Para continuar, consulte [Definir preços e estrutura](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[Versão 1.3.0 B2B](release-notes.md#b2b-v130) e posterior** — Ao criar um catálogo compartilhado, cada [permissão de categoria](../catalog/category-permissions.md) para o catálogo estiver definido como _[!UICONTROL Allow for the Display Product Prices]_e_[!UICONTROL Add to Cart]_ para grupos de clientes aos quais esse acesso é atribuído nas configurações de permissão do catálogo. Anteriormente, essas configurações eram definidas automaticamente como `Deny` mesmo quando as permissões do catálogo estavam definidas como `Allow`.

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
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifica um catálogo com preços personalizados que está disponível somente para as empresas específicas às quais ele está atribuído.<br/>**[!UICONTROL Public]**- Identifica o catálogo compartilhado que está disponível para todos os visitantes convidados e para clientes conectados que não estão associados a uma empresa. Um catálogo público compartilhado padrão é criado quando [!DNL B2B for Adobe Commerce] está instalado, mas deve ser configurado por um administrador de armazenamento. Somente um catálogo público compartilhado pode existir por vez. |
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
