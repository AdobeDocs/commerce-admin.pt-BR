---
title: Desative a integração do administrador do Commerce com o Adobe ID
description: Siga este procedimento opcional para desabilitar a integração do Adobe Commerce Admin com o Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Desative a integração do administrador do Commerce com o Adobe ID

{{ee-feature}}

Os comerciantes que integraram sua instância do Commerce ao fluxo de trabalho de autenticação do Adobe IMS podem precisar desativar essa integração opcional.

As implantações do Commerce são revertidas para o fluxo de trabalho de autenticação do Commerce padrão e para as políticas de senha depois que a integração IMS é desativada. Somente os workflows de usuário administrador são afetados quando essa integração é habilitada ou desabilitada.

Consulte [Sua conta de administrador](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=pt-BR) para obter uma visão geral do logon de administrador da Commerce.

## Etapa 1: desabilitar a integração

Não é possível desabilitar essa integração do Administrador. Para desativar a integração do Adobe IMS com o Commerce e retornar a autenticação do Commerce ao seu estado padrão, desative a integração na interface de linha de comando.

Para desativar a integração:

```bash
bin/magento admin:adobe-ims:disable
```

O Adobe Commerce exibe a seguinte mensagem após o sucesso:

```
Admin Adobe IMS integration is disabled.
```

## Etapa 2: criar ou recuperar a senha do Commerce

Depois de desabilitar a integração, os usuários administradores devem usar uma senha do Commerce para fazer logon no Administrador.

* Os usuários administradores do Commerce que lembram de sua senha do Commerce pré-existente (ou seja, uma senha do Commerce criada antes da integração do IMS) podem usá-la para fazer logon no Administrador.

* Os usuários administradores do Commerce que não têm uma senha do Commerce pré-existente ou que a esqueceram devem criar uma nova senha. Para criar uma nova senha, os usuários administradores podem usar o recurso [!UICONTROL Forgot your password?] na página de logon do Commerce para criar uma nova senha. Consulte [Redefinir senhas do cliente](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html?lang=pt-BR). O Commerce não aceitará um campo de senha vazio.

## Depois de desabilitar a integração

O fluxo de trabalho padrão de autenticação do Commerce é retomado depois que a integração do IMS é desativada e os usuários administradores são solicitados novamente a fornecer sua senha.

A desabilitação da integração IMS exclui as credenciais inseridas quando a integração foi habilitada (`Organization ID`, `Client ID` e `Client Secret` valores) dos arquivos de configuração do Commerce.
