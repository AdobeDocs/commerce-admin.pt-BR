---
title: Configurar a integração do administrador do Commerce com a ID
description: Siga este procedimento opcional para integrar logons de conta de usuário administrador do Adobe Commerce com o Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: c909d68cb2d99e9eb3d1e3adb8fc9b7c245812d2
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 0%

---

# Configurar a integração do administrador do Commerce com o Adobe ID

{{ee-feature}}

Essa integração oferece suporte aos comerciantes do Commerce com usuários administradores que têm uma Adobe ID e que desejam simplificar o logon nos produtos Adobe Commerce e Adobe Business. É opcional e é ativado com base na instância. Somente os workflows de usuário Admin são afetados quando habilitados. 

>[!IMPORTANT]
>
>Os usuários administradores devem salvar suas credenciais de administrador do Commerce (nome de usuário e senha) e credenciais do 2FA antes de habilitar essa integração. Essas credenciais são necessárias se a integração do IMS estiver desativada.

## Pré-requisitos

* Adobe Commerce 2.4.5 ou posterior
* Uma conta Adobe.com com acesso ao [Adobe Admin Console](https://adminconsole.adobe.com/).

  >[!NOTE]
  >
  >Se você não tiver acesso ao Admin Console do Adobe Commerce, envie uma solicitação para que sua equipe de conta provisione o acesso.

O administrador que configura essa integração precisa das seguintes credenciais durante a ativação do módulo:

* ID da organização (obtida de [Adobe Admin Console](https://adminconsole.adobe.com/)), que deve ter pelo menos 24 caracteres. O usuário autenticado deve pertencer a esta organização IMS. Para obter informações sobre como encontrar sua ID da organização, consulte [Organizações na Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA deve ser aplicado no nível da Organização no Adobe Admin Console para ativar o módulo. Verificar [Configurações de autenticação](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* ID do cliente
* Client secret
* A ID do cliente e o segredo do cliente estão disponíveis após recuperar chaves de API da [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials).

Os usuários administradores do Commerce devem criar uma conta com uma Adobe ID para fazer logon.

## Etapas gerais

* Obter a ID da Organização da Adobe da [Adobe Admin Console](https://adminconsole.adobe.com/)
* Gere um novo projeto, chaves de API IMS e segredo da [Adobe Developer Console](https://developer.adobe.com/)
* Configurar usuários do Adobe Commerce na Adobe Admin Console
* Habilite o módulo `AdminAdobeIms`.

Uma integração bem-sucedida requer que todos os usuários do Adobe Commerce tenham contas de usuário administrador com o mesmo nome e endereço de email principal. Se não existir uma conta de usuário Admin correspondente, um usuário com as permissões necessárias (normalmente com a função de Administrador atribuída) deverá [criar manualmente a conta de usuário Admin](../systems/permissions-users-all.md#create-a-user) com o mesmo nome e email.

## Configurar a integração

Depois que as etapas a seguir forem concluídas por um administrador ou desenvolvedor com acesso ao sistema, o botão _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_será exibido na página de logon do Commerce Admin para todos os usuários administradores.

### Etapa 1: obter a ID da organização da Adobe

A associação em pelo menos uma organização IMS é necessária para habilitar esse recurso. Se você tiver uma Adobe ID, pertencerá a pelo menos uma organização da Adobe por padrão. Faça logon no [Adobe Admin Console](https://adminconsole.adobe.com/) para recuperar a ID da organização.

### Etapa 2: gerar um novo projeto, chaves de API IMS e segredo

Para criar projetos para uma organização, a conta de administrador do Adobe da organização deve ter a função de administrador do sistema ou desenvolvedor. Consulte o [Guia do Developer Console](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Faça logon no [Adobe Developer Console](https://developer.adobe.com/).
1. Vá para a guia **[!UICONTROL Projects]** (adobe.io/projects) e clique em **[!UICONTROL Create a new project]**.
1. Clique em **[!UICONTROL Add API]** na página recém-criada do projeto.
1. Selecione **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Selecione **[!UICONTROL Oauth 2.0 Web]**.
1. Especifique o **[!UICONTROL Redirect URI]**: `https://<commerce_base_url>/`
1. Especifique o **[!UICONTROL Redirect URI pattern]**: `https://<commerce_base_url>/.*`

   Evite qualquer ponto no nome do host precedendo os pontos com `\\`. Adicionar um curinga ao final do URL é compatível com a chave secreta de administrador do Adobe Commerce.

1. Clique em **[!UICONTROL Save configured API]**.
1. Copie as chaves [!UICONTROL Client ID] e [!UICONTROL Client Secret] do projeto criado.

### Etapa 3: configurar usuários do Adobe Commerce na Adobe Admin Console

Antes de habilitar a integração, verifique se cada conta de usuário de administrador do Adobe Commerce tem uma conta do Adobe IMS correspondente. Os usuários da Adobe Commerce devem pertencer a uma organização específica da Adobe para fazer logon usando uma Adobe ID.

>[!TIP]
>
>Você pode criar várias contas de usuário fazendo upload das informações do usuário de um arquivo CSV. Consulte [Gerenciar vários usuários](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. No [Adobe Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html), navegue até **[!UICONTROL Users]** > **[!UICONTROL Users]**.

1. Clique em **[!UICONTROL Add User]**.

1. Insira o endereço de email do usuário.

   Se aplicável, o Tipo de ID recomendado será preenchido automaticamente. É possível alterar essa configuração para uma das IDs de produto na lista, que se baseia no plano de compra da sua organização.

   Você pode adicionar até dez usuários de uma vez. Para adicionar mais, repita as etapas anteriores depois de salvar as alterações.

1. Clique em **[!UICONTROL Save]**.

O usuário é adicionado e exibido na lista [!UICONTROL Users].

### Etapa 4: Ativar o módulo AdminAdobeIms

O módulo `AdminAdobeIms` é responsável pela integração do Adobe Commerce/Adobe IMS. Depois de configurar o novo projeto e copiar a ID da organização, a ID do cliente e o segredo do cliente, você pode habilitar o módulo `AdminAdobeIms`.

Digite `bin/magento admin:adobe-ims:enable`. Você será solicitado a informar os parâmetros a seguir. Use os valores gerados durante a criação do projeto.

* ID da organização
* ID do cliente
* Client secret
* 2FA habilitado

O Adobe Commerce exibe uma mensagem que indica se a ativação foi bem-sucedida ou falhou.

Após ativar esse recurso com êxito, é possível fazer a transição de outras contas de usuário do Adobe Commerce para contas do Adobe IMS. Os usuários do Adobe Commerce devem pertencer à organização configurada do Adobe para fazer logon usando uma Adobe ID.

## Identidade e logon único

Para obter informações sobre opções de configuração de identidade, incluindo Adobe ID, Enterprise ID e Federated ID, e instruções para configurar o Logon Único (SSO) para acesso seguro a aplicativos Adobe, consulte [Configurar identidade e logon único](https://helpx.adobe.com/enterprise/using/set-up-identity.html) na documentação do *Enterprise Admin Console*.
