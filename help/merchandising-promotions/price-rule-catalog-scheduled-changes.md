---
title: Alterações agendadas para regras de preço de catálogo
description: Saiba como aplicar regras de preço de catálogo conforme agendado como parte de uma campanha e agrupado com outras alterações de conteúdo.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Alterações agendadas para regras de preço de catálogo

{{ee-feature}}

A caixa Alterações programadas aparece na parte superior da página quando uma nova regra de preço é salva ou atualizada. As regras de preço de catálogo podem ser aplicadas de acordo com a programação como parte de uma campanha e agrupadas com outras alterações de conteúdo. Você pode criar uma campanha com base em alterações programadas em uma regra de preço ou aplicar as alterações a uma campanha existente.

>[!NOTE]
>
>Todas as atualizações programadas são aplicadas consecutivamente. Isso significa que qualquer entidade pode ter apenas uma atualização agendada em um ponto do tempo. Qualquer atualização agendada é aplicada a todas as exibições de loja dentro de seu período de tempo. Como resultado, uma entidade não pode ter atualizações agendadas diferentes para exibições de loja diferentes ao mesmo tempo. Todos os valores de atributo de entidade em todas as exibições de armazenamento, que não são afetados pela atualização agendada atual, são obtidos dos valores padrão, e não da atualização agendada anterior.

Se houver várias regras de preço em execução na mesma campanha, a configuração de Prioridade da regra de preço determinará qual regra tem prioridade. Para saber mais, consulte [Preparo de conteúdo](../content-design/content-staging.md).

>[!IMPORTANT]
>
>Se uma campanha que inclui uma regra de preço for criada inicialmente sem uma data final, a campanha não poderá ser editada posteriormente para incluir uma data final. É recomendável adicionar uma data de término ao criar a campanha ou criar uma versão duplicada da campanha existente e adicionar a data de término à duplicação, conforme necessário.

![Regra de preço de catálogo - alterações agendadas](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## Agendar uma atualização para uma regra de preço de catálogo

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**Regra de preço de catálogo**.

1. Abra a regra no modo de edição.

1. No **[!UICONTROL Scheduled Changes]** na parte superior da página, clique em **[!UICONTROL Schedule New Update]**.

1. Com o **[!UICONTROL Save as a New Update]** selecionada, faça o seguinte:

   - Para **[!UICONTROL Update Name]**, digite um nome para a atualização da regra.

   - Insira um resumo **[!UICONTROL Description]** da atualização, incluindo como ou por que ela é aplicada.

   - Use o _Calendário_ (![Ícone de calendário](../assets/icon-calendar.png)) para escolher o **[!DNL Start Date]** e **[!UICONTROL End Date]** para que a alteração programada entre em vigor. Para criar uma alteração aberta, deixe a data final em branco.

   ![Regras de preço de catálogo - novas alterações agendadas](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >A data/hora de início e término é determinada pela data/hora e pelo fuso horário padrão do painel Administração, não pelo fuso horário de um site específico. Considere o fuso horário do site para determinar corretamente as horas de início e término. Crie regras separadas para sites em fusos horários diferentes que precisam ser iniciados e/ou interrompidos em horários locais específicos.

1. Role para baixo até **[!UICONTROL Rule Information]** e altere a regra conforme necessário.

   É possível agendar alterações para qualquer parâmetro de regra, incluindo os sites (escopo)/grupos de clientes da regra, as condições da regra e as ações aplicadas pela regra. Para obter mais informações, consulte [Criando uma Regra de Preço de Catálogo](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >Se você alterar para qualquer um dos parâmetros de informações da regra, verifique se _[!UICONTROL Status]_está definido corretamente. Se desejar que a alteração resulte em uma regra aplicada ativamente, o status deverá ser`Active`.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A alteração programada é exibida na parte superior da página, com as datas de início e término da campanha.

## Editar uma alteração de regra agendada

1. No **[!UICONTROL Scheduled Changes]** na parte superior da página, clique em **[!UICONTROL View/Edit]**.

1. Faça as alterações necessárias na atualização agendada.

1. Clique em **[!UICONTROL Save]**.

## Visualizar a alteração de regra agendada

1. No **[!UICONTROL Scheduled Changes]** na parte superior da página, clique em **[!UICONTROL Preview]**.

   A Pré-visualização abre uma nova guia do navegador que carrega sua loja com a alteração agendada aplicada. Navegue até um produto afetado pela alteração.

   ![Visualizar Alteração Agendada](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. No canto superior esquerdo da janela Visualizar, clique em **[!UICONTROL Calendar]**.

   Os detalhes do calendário mostram outras campanhas programadas para o mesmo dia. Cada registro na lista é uma atualização de regra separada.

   ![Lista de atualizações agendadas para uma data específica](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. Para visualizar um dia ou hora diferente, clique no link **[!UICONTROL Date & Time]** calendário ![Ícone de calendário](../assets/icon-calendar.png) e faça o seguinte:

   - Escolha uma data e/ou hora diferente.

   - Clique em **[!UICONTROL Preview]**.

1. Para retornar ao calendário, clique em **[!UICONTROL Calendar]** no cabeçalho da página Visualizar.

   Aqui, você pode fazer o seguinte:

   **Compartilhar um link para a visualização**

   Para compartilhar um link para a visualização da loja com seus colegas, clique em **[!UICONTROL Share]**. Copie o link para a área de transferência e cole-o no corpo de uma mensagem de email.

   >[!NOTE]
   >
   >É necessário ter uma conta de usuário Administrador para ter uma visualização compartilhada. Se o seu [tem acesso](../systems/permissions-user-roles.md) para criar uma conta de usuário Admin, você deve criar a conta para um novo usuário antes de compartilhar.

   **Alterar o Escopo da Visualização**

   Para ver as alterações agendadas para diferentes modos de exibição de loja, clique em **[!UICONTROL Scope]** no cabeçalho da página Visualizar. Escolha o modo de exibição de site, loja ou loja que deseja visualizar.

1. Se necessário, retorne ao calendário e clique em **[!UICONTROL View/Edit]** no _[!UICONTROL Action]_para abrir outra atualização agendada.
