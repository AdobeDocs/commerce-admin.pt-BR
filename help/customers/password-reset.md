---
title: Redefinir senhas do cliente
description: Os clientes geralmente redefinem suas senhas da loja, mas um administrador de loja pode iniciar uma redefinição de senha ou uma entrada forçada do Administrador.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Redefinir senhas do cliente

Os clientes geralmente redefinem suas senhas na loja clicando em _[!UICONTROL Forgot Your Password?]_. No entanto, o administrador de armazenamento pode iniciar uma redefinição de senha ou um logon forçado pelo Administrador.

| Função | Descrição |
| --- | --- |
| Redefinir senha | Um email de redefinição de senha é enviado diretamente para a conta de email do cliente. O administrador da loja não pode obter acesso à senha do cliente. |
| Forçar Entrada | Revoga os tokens de acesso OAuth associados à conta do cliente. Isso pode ser usado somente com contas de clientes que receberam tokens OAuth, como parte de uma API da Web [integração](../systems/integrations.md). Para saber mais, consulte [Autenticação baseada em OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) na documentação do desenvolvedor. <br/><br/>As contas de clientes padrão criadas na loja ou no Administrador não têm tokens OAuth. |

{style="table-layout:auto"}

## Redefinir uma senha da loja

1. Na página de logon, o cliente clica em **[!UICONTROL Forgot Your Password?]**.

1. Quando solicitado, insere o **[!UICONTROL Email Address]** que está associado à sua conta e clica em **[!UICONTROL Reset My Password]**.

   ![Esqueceu sua senha](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Se o endereço de email inserido corresponder ao que está associado à conta, o cliente receberá um email de Confirmação de redefinição de senha com um link para redefinir sua senha.

1. Quando o email chegar, o cliente clicar no _redefinir senha_ e insere seus **[!UICONTROL New Password]** quando solicitado.

1. Insira-o novamente para confirmar e clicar em **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >A nova senha deve ter seis ou mais caracteres sem espaços. Ao receberem a confirmação de que a senha foi atualizada, eles poderão usar a nova senha para entrar em suas contas. Por padrão, a variável _redefinir senha_ O link é válido por 24 horas.

## Redefinir uma senha do Administrador

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Localize a conta do cliente na grade e clique em **[!UICONTROL Edit]** no _Ação_ coluna.

1. No conjunto de opções na parte superior da página, clique em **[!UICONTROL Reset Password]**.

   O número de solicitações de redefinição de senha permitidas em uma hora é definido no [configuração](../configuration-reference/customers/customer-configuration.md) tópico.

## Revogar tokens OAuth de um cliente

>[!IMPORTANT]
>
>Não prossiga, a menos que você tenha um entendimento completo da Autenticação de API.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Localize a conta do cliente na grade e clique em **[!UICONTROL Edit]** no _Ação_ coluna.

1. No conjunto de opções na parte superior da página, clique em **[!UICONTROL Force Sign In]**.

1. Quando for solicitada a confirmação, clique em **OK**.
