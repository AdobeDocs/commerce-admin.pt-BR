---
title: Visão geral da integração do Adobe Identity Management Service (IMS)
description: Apresenta a integração opcional do logon de administrador do Adobe Commerce com o Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Visão geral da integração do Adobe Identity Management Service (IMS)

{{ee-feature}}

Os usuários administradores do Adobe Commerce que têm uma conta Adobe agora podem usar o Adobe ID para fazer logon no Adobe Commerce. O Adobe Identity Management Service (IMS) é um recurso de gerenciamento de identidades baseado em OAuth 2.0 da Adobe que oferece suporte à autenticação. Integrar a autenticação do Commerce Admin no fluxo de trabalho de autenticação IMS do Adobe Product pode simplificar o processo de autenticação para usuários que trabalham com outros produtos Adobe. Essa integração é opcional e é ativada com base na instância. Somente os workflows de usuário administrador são afetados quando essa integração é habilitada. 

Os módulos necessários para a integração do IMS do Commerce Admin estão empacotados em `adobe-ims-metapackage`, que vem com as versões principais do Adobe Commerce.

Para implementar essa integração, consulte [Configurar a Integração do Administrador do Commerce com o IMS](./adobe-ims-config.md).

## Alterações nos fluxos de trabalho e na interface do administrador após a integração com o IMS

Quando essa integração é habilitada, os usuários administradores do Commerce experimentam alterações no logon e no fluxo de trabalho de autenticação padrão do administrador do Commerce ao realizar tarefas de rotina no administrador que exigem reautenticação, como criar um usuário administrador. A imposição da autenticação de dois fatores (2FA) no nível da organização de Adobe é necessária para a ativação do módulo. O logon de Administrador padrão e 2FA estão desabilitados, e o botão _[!UICONTROL Sign In with Adobe ID]_substitui o formulário de logon de Administrador padrão. As autorizações ainda são gerenciadas do Administrador.

## Como a integração do administrador com o IMS afeta as senhas do Commerce

As implantações do Commerce que foram integradas ao Adobe IMS exigem uma conta da Adobe ID com acesso à organização do Adobe IMS configurada para o aplicativo do Commerce durante o processo de ativação do IMS.  Quando a integração IMS está habilitada, os usuários administradores se autenticam por meio da página de logon de Adobe usando suas credenciais de Adobe. As senhas e os nomes de usuário do Commerce para usuários administradores não são mais usados para autenticação, desde que a integração do Adobe IMS esteja habilitada.

Se a integração IMS estiver desativada, os usuários administradores deverão se autenticar novamente por meio do Adobe Commerce usando seu nome de usuário e senha da Commerce. Os usuários administradores devem salvar suas credenciais de administrador do Commerce (nome de usuário e senha) e credenciais do 2FA antes de habilitar essa integração.

Determinados componentes de back-end envolvidos na autenticação do usuário ainda exigem uma senha não nula. Para atender a esse requisito, o Commerce cria senhas aleatórias para novos usuários administradores na tabela `admin_user`.

As contas de usuário e as permissões de função para o aplicativo Commerce ainda são gerenciadas no Administrador do Commerce.


## Geração de token da API da Web com credenciais IMS

As APIs de administrador do Commerce são afetadas quando a autenticação Admin com o Adobe IMS é ativada em uma instância do Commerce. Os usuários administradores não podem mais usar as credenciais emitidas pela instância do Commerce. Essas são as credenciais necessárias para fazer logon no Administrador e obter tokens de acesso que os serviços do podem usar para fazer solicitações às APIs REST e SOAP do Administrador.

Depois que a integração do Adobe IMS for habilitada, os usuários administradores deverão usar [tokens OAuth do Adobe IMS](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) para os pontos de extremidade da API do Adobe Commerce que exigem autenticação. As soluções do cliente obtêm os tokens dinamicamente para uso da API da Web. Esse mecanismo de autenticação é ativado para áreas REST e SOAP da API da Web como parte da configuração dessa integração.

Consulte [Autenticação baseada em token](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) para obter uma visão geral de como as APIs da Web usam tokens de acesso do Commerce, incluindo tokens de acesso IMS.

## Gerenciamento de sessão do Commerce e tokens de acesso do Adobe IMS

Os tokens de acesso mantêm as credenciais do usuário e as informações da sessão de logon. Depois que um usuário é autenticado e uma sessão é iniciada, essas duas variáveis são adicionadas à sessão do usuário:

`token_last_check_time`. Identifica a hora atual e é usada pelo plug-in `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`.

`adobe_access_token` — Identifica o valor `ACCESS_TOKEN` recebido durante a autorização.

O plug-in `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` verifica se o `token_last_check_time` foi atualizado há 10 minutos. Se `token_last_check_time` foi verificado há dez minutos, o fluxo de trabalho de autenticação faz uma chamada de API ao IMS para validar o token de acesso e a sessão continua. Se o token de acesso for válido, o valor `token_last_check_time` será atualizado para a hora atual. Se o token não for válido, a sessão será encerrada.

## Arquivos importantes

`adminAdobeIms` - Fornece uma implementação do logon de Administrador com base no módulo `AdobeImsApi`.

`admin_adobe_ims_webapi` - Mantém um registro de todos os tokens de acesso validados. Quando um token é validado ou invalidado, um registro de seu status é preservado nesta tabela.

`adobeIms` - Implementa toda a lógica de negócios relacionada à integração com o Adobe IMS (preservada para evitar incompatibilidades anteriores).

`adobeImsApi` - Declara as interfaces que oferecem suporte à integração com o Adobe IMS.

`adminadobe-ims.log` - Arquivo de log de erros.

## Habilitar a integração

O metappackage do Adobe IMS é instalado com o Adobe Commerce 2.4.5 e superior, mas deve ser configurado para uso. Ele estende o módulo `AdobeIms` para oferecer suporte ao módulo que habilita a lógica de autenticação (`AdminAdobeIms`).

Para obter mais informações sobre como habilitar a integração, consulte [Configurar a Integração de Administrador do Commerce com o Adobe IMS](./adobe-ims-config.md).
