---
title: Configurar a integração do administrador do Commerce com a ID
description: Siga este procedimento opcional para integrar logons de conta de usuário administrador do Adobe Commerce com o Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 20b2560ce2b8071c740907292544519f8b1c3ddf
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 1%

---

# Configurar a integração do administrador do Commerce com o Adobe ID

{{ee-feature}}

Essa integração oferece suporte a comerciantes do Commerce com usuários Administradores que têm um Adobe ID e que desejam simplificar o logon nos produtos Adobe Commerce e Adobe Business. É opcional e é ativado com base na instância. Somente os workflows de usuário Admin são afetados quando habilitados. 

>[!IMPORTANT]
>
>Os usuários administradores devem salvar suas credenciais de Administrador do Commerce (nome de usuário e senha) e credenciais do 2FA antes de habilitar essa integração. Essas credenciais são necessárias se a integração do IMS estiver desativada.

## Pré-requisitos

* Adobe Commerce 2.4.5 ou posterior
* Uma conta Adobe.com com acesso ao [Adobe Admin Console](https://adminconsole.adobe.com/).

O administrador que configura essa integração precisa das seguintes credenciais durante a ativação do módulo:

* ID da organização (obtida de [Adobe Admin Console](https://adminconsole.adobe.com/)), que deve ter pelo menos 24 caracteres. O usuário autenticado deve pertencer a esta organização IMS. Para obter informações sobre como encontrar a ID da organização, consulte [Organizações no Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA deve ser aplicado no nível da Organização no Adobe Admin Console para ativar o módulo. Marcar [Configurações de autenticação](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* ID do cliente
* Client secret
* A ID do cliente e o segredo do cliente estão disponíveis após recuperar as chaves de API da [Console do Adobe Developer](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Os usuários administradores do Commerce devem criar uma conta com uma Adobe ID para fazer logon.

## Etapas gerais

* Obter a ID da organização do Adobe do [Adobe Admin Console](https://adminconsole.adobe.com/)
* Gere um novo projeto, chaves de API do IMS e secreta a partir da [Console do Adobe Developer](https://developer.adobe.com/)
* Ativar o `AdminAdobeIms` módulo
* Configure os usuários do Adobe Commerce na Adobe Admin Console.

Uma integração bem-sucedida requer que todos os usuários do Adobe Commerce tenham contas de usuário administrador com o mesmo nome e endereço de email principal. Se não existir uma conta de usuário Admin correspondente, um usuário com as permissões necessárias (normalmente atribuído com a função de Administrador) deverá fazer isso manualmente [criar a conta de usuário Admin](../systems/permissions-users-all.md#create-a-user) com o mesmo nome e email.

## Configurar a integração

Depois que as etapas a seguir forem concluídas por um administrador ou desenvolvedor com acesso ao sistema, a variável _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_é exibido na página de logon de administrador do Commerce para todos os usuários administradores.

### Etapa 1: obter a ID da organização do Adobe

A associação em pelo menos uma organização IMS é necessária para habilitar esse recurso. Se você tiver uma Adobe ID, pertencerá a pelo menos uma organização Adobe por padrão. Faça logon no [Adobe Admin Console](https://adminconsole.adobe.com/) para recuperar a ID da organização.

### Etapa 2: gerar um novo projeto, chaves de API IMS e segredo

Para criar projetos para uma organização, a conta de Administrador do Adobe da organização deve ter a função de administrador do sistema ou desenvolvedor. Consulte a [Guia do Developer Console](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Efetue logon no [Console do Adobe Developer](https://developer.adobe.com/).
1. Vá para a **[!UICONTROL Projects]** (adobe.io/projects) e clique em **[!UICONTROL Create a new project]**.
1. Clique em **[!UICONTROL Add API]** na página Projeto recém-criada.
1. Selecionar **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Selecionar **[!UICONTROL Oauth 2.0 Web]**.
1. Especifique a **[!UICONTROL Redirect URI]**: `https://<hostname>/`
1. Especifique a **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/.*`

   Evite qualquer ponto no nome do host precedendo os pontos por `\\`. Adicionar um curinga ao final do URL é compatível com a chave secreta de administrador do Adobe Commerce.

1. Clique em **[!UICONTROL Save configured API]**.
1. Copie o [!UICONTROL Client ID] e [!UICONTROL Client Secret] chaves do projeto criado.

### Etapa 3: Ativar o módulo AdminAdobeIms

A variável `AdminAdobeIms` O módulo é responsável pela integração do Adobe Commerce/Adobe IMS. Depois de configurar o novo projeto e copiar a ID da organização, a ID do cliente e o segredo do cliente, você pode ativar a `AdminAdobeIms` módulo.

Enter `bin/magento admin:adobe-ims:enable`. Você será solicitado a informar os parâmetros a seguir. Use os valores gerados durante a criação do projeto.

* ID da organização
* ID do cliente
* Client secret
* 2FA habilitado

O Adobe Commerce exibe uma mensagem que indica se a ativação foi bem-sucedida ou falhou.

Após ativar esse recurso com êxito, é possível fazer a transição de outras contas de usuário do Adobe Commerce para contas do Adobe IMS. Os usuários do Adobe Commerce devem pertencer à organização de Adobe configurada para fazer logon usando uma Adobe ID.

### Etapa 4: configurar usuários do Adobe Commerce na Adobe Admin Console

Após ativar esse recurso com êxito, é possível fazer a transição de outras contas de usuário do Adobe Commerce para contas do Adobe IMS. Os usuários do Adobe Commerce devem pertencer a pelo menos uma organização Adobe para fazer logon usando uma Adobe ID.

1. No [Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html), navegue até **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. Clique em **[!UICONTROL Add User]**.

1. Insira o endereço de email do usuário.

   Se aplicável, o Tipo de ID recomendado será preenchido automaticamente. É possível alterar essa configuração para uma das IDs de produto na lista, que se baseia no plano de compra da sua organização.

   Você pode adicionar até dez usuários de uma vez. Para adicionar mais, repita as etapas anteriores depois de salvar as alterações.

1. Clique em **[!UICONTROL Save]**.

O usuário é adicionado e exibido no [!UICONTROL Users] lista.
