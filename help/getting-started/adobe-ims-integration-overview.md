---
title: Visão geral da integração do Adobe Identity Management Service (IMS)
description: Apresenta a integração opcional do logon de administrador do Adobe Commerce com o Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Visão geral da integração do Adobe Identity Management Service (IMS)

{{ee-feature}}

Os usuários administradores do Adobe Commerce que têm uma conta Adobe agora podem usar o Adobe ID para fazer logon no Adobe Commerce. O Adobe Identity Management Service (IMS) é um recurso de gerenciamento de identidades baseado em OAuth 2.0 da Adobe que oferece suporte à autenticação. Adobe Integrar a autenticação do Administrador do Commerce ao fluxo de trabalho de autenticação IMS do Produto comercial pode simplificar o processo de autenticação para usuários que trabalham com outros produtos Adobe. Essa integração é opcional e é ativada com base na instância. Somente os workflows de usuário administrador são afetados quando essa integração é habilitada. 

Os módulos necessários para a integração do IMS do administrador do Commerce estão incluídos no  `adobe-ims-metapackage`, que vem com as versões principais do Adobe Commerce.

Para implementar essa integração, consulte [Configurar a integração do administrador do Commerce com o IMS](./adobe-ims-config.md).

## Alterações nos fluxos de trabalho e na interface do administrador após a integração com o IMS

Quando essa integração é habilitada, os usuários administradores do Commerce experimentam alterações no logon de administrador do Commerce padrão e no fluxo de trabalho de autenticação, à medida que executam tarefas de rotina no Administrador que exigem reautenticação, como a criação de um usuário administrador. A imposição da autenticação de dois fatores (2FA) no nível da organização de Adobe é necessária para a ativação do módulo. O logon padrão de Administrador e 2FA são desativados e a variável _[!UICONTROL Sign In with Adobe ID]_O botão substitui o formulário padrão de Logon de administrador. As autorizações ainda são gerenciadas do Administrador.

## Como a integração do administrador com o IMS afeta as senhas do Commerce

As implantações do Commerce que foram integradas ao Adobe IMS exigem uma conta do Adobe ID com acesso à organização do Adobe IMS configurada para o aplicativo do Commerce durante o processo de habilitação do IMS.  Quando a integração IMS está habilitada, os usuários administradores se autenticam por meio da página de logon de Adobe usando suas credenciais de Adobe. As senhas do Commerce e os nomes de usuário dos usuários administradores não são mais usados para autenticação, desde que a integração do Adobe IMS esteja habilitada.

Se a integração IMS estiver desativada, os usuários administradores deverão se autenticar novamente por meio do Adobe Commerce usando seu nome de usuário e senha do Commerce. Os usuários administradores devem salvar suas credenciais de Administrador do Commerce (nome de usuário e senha) e credenciais do 2FA antes de habilitar essa integração.

Determinados componentes de back-end envolvidos na autenticação do usuário ainda exigem uma senha não nula. Para atender a esse requisito, o Commerce cria senhas aleatórias para usuários administradores recém-criados na `admin_user` tabela.

As contas de usuário e permissões de função para o aplicativo Commerce ainda são gerenciadas pelo administrador do Commerce.


## Geração de token da API da Web com credenciais IMS

As APIs de administrador do Commerce são afetadas quando a autenticação de administrador com o Adobe IMS é ativada em uma instância do Commerce. Os usuários administradores não podem mais usar as credenciais emitidas pela instância do Commerce. Essas são as credenciais necessárias para fazer logon no Administrador e obter tokens de acesso que os serviços podem usar para fazer solicitações às APIs REST e SOAP do Administrador.

Após habilitar a integração do Adobe IMS, os usuários administradores devem usar [Tokens OAuth do Adobe IMS](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) para endpoints de API do Adobe Commerce que exigem autenticação. As soluções do cliente obtêm os tokens dinamicamente para uso da API da Web. Esse mecanismo de autenticação é ativado para áreas REST e SOAP da API da Web como parte da configuração dessa integração.

Consulte [Autenticação baseada em token](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) para obter uma visão geral de como as APIs da Web usam tokens de acesso do Commerce, incluindo tokens de acesso IMS.

## Gerenciamento de sessão de comércio e tokens de acesso do Adobe IMS

Os tokens de acesso mantêm as credenciais do usuário e as informações da sessão de logon. Depois que um usuário é autenticado e uma sessão é iniciada, essas duas variáveis são adicionadas à sessão do usuário:

`token_last_check_time`. Identifica a hora atual e é usada pelo `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` plug-in.

`adobe_access_token` — Identifica o `ACCESS_TOKEN` valor recebido durante a autorização.

A variável `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` O plug-in verifica se `token_last_check_time` foi atualizado há 10 minutos. Se a variável `token_last_check_time` foi verificado há dez minutos, o fluxo de trabalho de autenticação faz uma chamada de API ao IMS para validar o token de acesso e a sessão continua. Se o token de acesso for válido, a variável `token_last_check_time` é atualizado para a hora atual. Se o token não for válido, a sessão será encerrada.

## Arquivos importantes

`adminAdobeIms` - Fornece uma implementação do login de Administrador com base no `AdobeImsApi` módulo.

`admin_adobe_ims_webapi` - Mantém um registro de todos os tokens de acesso validados. Quando um token é validado ou invalidado, um registro de seu status é preservado nesta tabela.

`adobeIms` - Implementa toda a lógica de negócios relacionada à integração com o Adobe IMS (preservada para evitar incompatibilidades com versões anteriores).

`adobeImsApi` - Declara as interfaces que oferecem suporte à integração com o Adobe IMS.

`adminadobe-ims.log` - Arquivo de log de erros.

## Habilitar a integração

O metappackage do Adobe IMS é instalado com o Adobe Commerce 2.4.5 e superior, mas deve ser configurado para uso. Estende o `AdobeIms` módulo de suporte ao módulo que habilita a lógica de autenticação (`AdminAdobeIms`).

Para obter mais informações sobre como habilitar a integração, consulte [Configurar a integração do administrador do Commerce com o Adobe IMS](./adobe-ims-config.md).
