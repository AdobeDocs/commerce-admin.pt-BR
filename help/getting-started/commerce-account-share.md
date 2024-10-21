---
title: Compartilhar uma conta  [!DNL Commerce]
description: Saiba como conceder acesso limitado à sua conta [!DNL Commerce] para outros [!DNL Commerce] titulares da conta.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 8f8cb141c79b8b5a57363faf7ec5c8f2e75bb473
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# Compartilhar uma conta do [!DNL Commerce]

Sua conta do [!DNL Commerce] contém informações que você pode disponibilizar para funcionários confiáveis e provedores de serviços que ajudam a gerenciar seu site. Como titular primário da conta, você tem autoridade para conceder acesso limitado a outros [!DNL Commerce] titulares da conta. O acesso compartilhado pode ser revogado, mas não pode ser transferido de um usuário para outro.

A equipe de suporte do [!DNL Commerce] não tem acesso à conta e não pode configurar o acesso compartilhado para você. Somente o titular primário da conta com as permissões apropriadas pode configurar o acesso compartilhado. Quando você compartilha o acesso à conta, todas as informações confidenciais, como seu histórico de cobrança ou informações de cartão de crédito, permanecem protegidas e nunca ficam disponíveis para outros usuários.

>[!NOTE]
>
>Todas as ações tomadas por usuários com acesso compartilhado são de exclusiva responsabilidade do titular principal da conta. O Adobe não é responsável por nenhuma ação tomada pelos usuários que têm acesso compartilhado à sua conta.

![Configurações de acesso compartilhado](./assets/shared-access.png){width="600" zoomable="yes"}

## Configurar uma conta compartilhada

1. Antes de começar, obtenha as seguintes informações da conta [!DNL Commerce] do **novo favorecido de acesso compartilhado**:

   - O usuário já deve ter se registrado em uma conta em account.adobe.com e estar conectado por meio de account.magento.com.
   - O `MAGE ID/Account ID (MAG00XXXXXXX)` é exibido no canto superior esquerdo da guia _[!UICONTROL Magento]_, logo acima do link **Logoff**.
   - O endereço `Email` associado à conta.

1. Faça logon em sua [[!DNL Commerce] conta](commerce-account-create.md).

1. No painel de navegação esquerdo, clique em **[!UICONTROL Shared Access]**.

1. Clique em **[!UICONTROL Add New User]**.

   ![Adicionar um novo usuário](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. Em [!UICONTROL _New User Information]_, faça o seguinte:

   - Insira o **[!UICONTROL Account ID]** da conta [!DNL Commerce] do novo usuário.
   - Digite o endereço **[!UICONTROL Email]** que está associado à conta [!DNL Commerce] do novo usuário.

   ![Informações sobre o novo usuário](./assets/shared-new-user.png){width="600"}

1. Em _[!UICONTROL Shared Information]_, faça o seguinte:

   - Para identificar a conta compartilhada, insira um **[!UICONTROL Share Name]**. Esse nome serve para referência interna e é visível apenas para você e para a pessoa com quem você compartilha sua conta.

     Uma prática recomendada é usar o nome da sua Organização como [!UICONTROL Share Name]. Não use um nome que comece com `CLOUD SHARED ACCESS FROM MAG XYX`.
   - Para compartilhar suas informações pessoais de contato com o novo usuário, digite **[!UICONTROL Your Email]** e **[!UICONTROL Your Phone]**.

1. Em _[!UICONTROL Grant Account Permissions]_, marque a caixa de seleção de cada produto e serviço do [!DNL Commerce] que você deseja compartilhar.

   ![Conceder as permissões da conta](./assets/shared-permissions.png){width="600"}

1. Clique em **[!UICONTROL Create Shared Access]**.

   As novas informações do usuário aparecem na seção _[!UICONTROL Manage Permissions]_da página Acesso Compartilhado, e um convite por email com instruções para acessar a conta compartilhada é enviado ao novo usuário.

   ![Gerenciar permissões para acesso compartilhado](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Não é necessário compartilhar o acesso ao _[!UICONTROL Security Tool]_. Qualquer usuário com uma ID de MAGE pode configurar a Ferramenta de Verificação de Segurança com sua própria conta. Eles só precisam dos privilégios necessários para fazer alterações no site e verificar a propriedade do domínio usando um dos [métodos necessários](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)).

## Acessar uma conta compartilhada

As instruções a seguir são escritas da perspectiva de um usuário compartilhado que recebe um convite para uma conta compartilhada.

1. Ao receber um convite para uma conta compartilhada, siga as instruções no email para fazer logon em sua própria conta do [!DNL Commerce].

   O painel de navegação esquerdo de sua conta tem uma nova guia _[!UICONTROL Shared with me]_. O controle_[!UICONTROL Switch Accounts]_ no canto superior direito tem opções para `My Account` e o nome da conta compartilhada.

   ![Compartilhado(s) comigo](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   Se você não vir o controle _[!UICONTROL Switch Accounts]_, contate o titular primário da conta e confirme se inseriu as [informações da conta](#set-up-a-shared-account) corretas.


1. Para obter acesso à conta compartilhada, defina **[!UICONTROL Switch Accounts]** como o nome da conta compartilhada.

   ![Alternar para a conta compartilhada](./assets/shared-switch.png){width="600" zoomable="yes"}

   A conta compartilhada exibe uma mensagem de boas-vindas e informações de contato. O painel de navegação esquerdo inclui apenas os itens que você tem permissão para usar.

1. Para conectar a conta compartilhada ao Centro de Ajuda, clique em **[!UICONTROL Support]** no painel de navegação esquerdo da conta compartilhada.

   ![Suporte](./assets/shared-support.png){width="600" zoomable="yes"}

   Você pode usar a [Central de Ajuda do Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) da conta compartilhada para procurar artigos e informações de solução de problemas, encontrar patches para problemas conhecidos e criar tíquetes de suporte.

   >[!NOTE]
   >
   >Depois de receber acesso compartilhado, o usuário deve fazer logon em sua [[!DNL Commerce] conta](https://account.magento.com/customer/account/login), navegar até o _Acesso Compartilhado_ e clicar na guia **[!UICONTROL Support]**. Esta ação é necessária somente na primeira vez para garantir que a [Base de Dados de Conhecimento de Suporte da Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) seja configurada corretamente por meio da chamada `SSO`.

1. Para retornar à sua própria conta, clique em **Voltar** nos controles do navegador e defina **[!UICONTROL Switch Accounts]** como `My Account`.

## Revogar acesso compartilhado

1. Faça logon em sua conta da Commerce.

1. No painel de navegação esquerdo, clique em **[!UICONTROL Shared Access]**.

1. Localize a conta a ser revogada em _[!UICONTROL Managing Users & Permissions]_e clique em **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > Se **[!UICONTROL Delete]** não for exibido, verifique se **[!UICONTROL Share Name]** começa com `Cloud Shared Access from MAG XYZ`. Você não pode excluir contas com esse [padrão de nomenclatura](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).
   > 
   > Em caso positivo, peça ao proprietário da conta para modificar a conta de Acesso Compartilhado para limpar as permissões da conta. Após essa atualização, o usuário não poderá acessar nenhum recurso da conta.
   >
   > Além disso, remova os usuários do projeto para que eles não recebam mais notificações por email: [Os membros antigos da equipe recebem emails de notificação da nuvem do Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)


1. Quando for solicitada a confirmação, clique em **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Não é possível excluir usuários com o Nome de Compartilhamento do _Acesso Compartilhado na Nuvem da MAG[XYZ]_ nesta interface. Consulte [Como excluir usuários que receberam acesso compartilhado por meio de um projeto na nuvem?](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).
