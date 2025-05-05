---
title: Alterações agendadas para regras de preço de catálogo
description: Saiba como aplicar regras de preço de catálogo conforme agendado como parte de uma campanha e agrupado com outras alterações de conteúdo.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 11f8fcba70491f9dcb6c20d14b406fba4b14cab4
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 0%

---

# Alterações agendadas para regras de preço de catálogo

{{ee-feature}}

A caixa Alterações programadas aparece na parte superior da página quando uma nova regra de preço é salva ou atualizada. As regras de preço de catálogo podem ser aplicadas de acordo com a programação como parte de uma campanha e agrupadas com outras alterações de conteúdo. Você pode criar uma campanha com base em alterações programadas em uma regra de preço ou aplicar as alterações a uma campanha existente.

>[!NOTE]
>
>Os campos [!UICONTROL From] e [!UICONTROL To] foram removidos do Adobe Commerce ![Adobe Commerce](../assets/adobe-logo.svg) e não podem ser modificados diretamente na regra de preço de catálogo. Você deve criar uma atualização agendada para essas ativações.

>[!NOTE]
>
>Todas as atualizações programadas são aplicadas consecutivamente. Isso significa que qualquer entidade pode ter apenas uma atualização agendada em um ponto do tempo. Qualquer atualização agendada é aplicada a todas as exibições de loja dentro de seu período de tempo. Como resultado, uma entidade não pode ter atualizações agendadas diferentes para exibições de loja diferentes ao mesmo tempo. Todos os valores de atributo de entidade em todas as exibições de armazenamento, que não são afetados pela atualização agendada atual, são obtidos dos valores padrão, e não da atualização agendada anterior.

Se houver várias regras de preço em execução na mesma campanha, a configuração de Prioridade da regra de preço determinará qual regra tem prioridade. Para saber mais, consulte [Preparo de conteúdo](../content-design/content-staging.md).

>[!IMPORTANT]
>
>Se uma campanha ativa for criada inicialmente sem uma data de término, a campanha não poderá ser editada posteriormente para incluir uma data de término. Nesse caso, é necessário criar uma campanha duplicada e inserir a data final necessária.

![Regra de preço de catálogo - alterações agendadas](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## Agendar uma atualização para uma regra de preço de catálogo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**Regra de Preço de Catálogo**.

1. Abra a regra no modo de edição.

1. Na caixa **[!UICONTROL Scheduled Changes]**, na parte superior da página, clique em **[!UICONTROL Schedule New Update]**.

1. Com a opção **[!UICONTROL Save as a New Update]** selecionada, faça o seguinte:

   - Para **[!UICONTROL Update Name]**, insira um nome para a atualização da regra.

   - Insira um breve **[!UICONTROL Description]** da atualização, incluindo como ou por que ela é aplicada.

   - Use o _Calendário_ (![Ícone de calendário](../assets/icon-calendar.png)) para escolher o **[!DNL Start Date]** e o **[!UICONTROL End Date]** para que a alteração agendada entre em vigor. Para criar uma alteração aberta, deixe a data final em branco.

   ![Regras de preço de catálogo - novas alterações agendadas](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >A data/hora de início e término é determinada pela data/hora e pelo fuso horário padrão do painel Administração, não pelo fuso horário de um site específico. Considere o fuso horário do site para determinar corretamente as horas de início e término. Crie regras separadas para sites em fusos horários diferentes que precisam ser iniciados e/ou interrompidos em horários locais específicos.

1. Role para baixo até a seção **[!UICONTROL Rule Information]** e altere a regra conforme necessário.

   É possível agendar alterações para qualquer parâmetro de regra, incluindo os sites (escopo)/grupos de clientes da regra, as condições da regra e as ações aplicadas pela regra. Para obter mais informações, consulte [Criando uma Regra de Preço de Catálogo](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >Se você alterar para qualquer um dos parâmetros de informações da regra, verifique se _[!UICONTROL Status]_&#x200B;está definido corretamente. Se você quiser que a alteração resulte em uma regra aplicada ativamente, o status deverá ser `Active`.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A alteração programada é exibida na parte superior da página, com as datas de início e término da campanha.

## Editar uma alteração de regra agendada

1. Na caixa **[!UICONTROL Scheduled Changes]**, na parte superior da página, clique em **[!UICONTROL View/Edit]**.

1. Faça as alterações necessárias na atualização agendada.

   >[!NOTE]
   >
   >Se uma campanha estiver vinculada a mais de uma regra de preço de catálogo, ela só poderá ser editada no [Painel de Preparo de Conteúdo](../content-design/content-staging-dashboard.md).

1. Clique em **[!UICONTROL Save]**.

## Visualizar a alteração de regra agendada

1. Na caixa **[!UICONTROL Scheduled Changes]**, na parte superior da página, clique em **[!UICONTROL Preview]**.

   A Pré-visualização abre uma nova guia do navegador que carrega sua loja com a alteração agendada aplicada. Navegue até um produto afetado pela alteração.

   ![Visualizar Alteração Agendada](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. No canto superior esquerdo da janela Visualizar, clique em **[!UICONTROL Calendar]**.

   Os detalhes do calendário mostram outras campanhas programadas para o mesmo dia. Cada registro na lista é uma atualização de regra separada.

   ![Lista de Atualizações Agendadas para uma Data Específica](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. Para visualizar um dia ou hora diferente, clique no **[!UICONTROL Date & Time]** ícone do calendário ![Calendário](../assets/icon-calendar.png) e faça o seguinte:

   - Escolha uma data e/ou hora diferente.

   - Clique em **[!UICONTROL Preview]**.

1. Para retornar ao calendário, clique em **[!UICONTROL Calendar]** no cabeçalho da página de Visualização.

   Aqui, você pode fazer o seguinte:

   **Compartilhar um Link para a Visualização**

   Para compartilhar um link para a visualização da loja com seus colegas, clique em **[!UICONTROL Share]**. Copie o link para a área de transferência e cole-o no corpo de uma mensagem de email.

   >[!NOTE]
   >
   >É necessário ter uma conta de usuário Administrador para ter uma visualização compartilhada. Se a sua [função tiver acesso](../systems/permissions-user-roles.md) para criar uma conta de usuário Administrador, você deverá criar a conta para um novo usuário antes de compartilhar.

   **Alterar o Escopo da Visualização**

   Para ver as alterações agendadas para diferentes modos de exibição de armazenamento, clique em **[!UICONTROL Scope]** no cabeçalho da página de Visualização. Escolha o modo de exibição de site, loja ou loja que deseja visualizar.

1. Se necessário, retorne ao calendário e clique em **[!UICONTROL View/Edit]** na coluna _[!UICONTROL Action]_&#x200B;para abrir outra atualização agendada.
