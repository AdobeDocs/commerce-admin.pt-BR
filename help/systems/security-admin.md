---
title: Configurar a segurança do administrador
description: Saiba como configurar a segurança para o Administrador da loja.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Configurar a segurança do administrador

Recomendamos que você adote uma abordagem multifacetada para proteger a segurança de sua loja. Você pode começar usando um [URL de administração personalizada](../stores-purchase/store-urls.md#use-a-custom-admin-url) isso não é fácil de adivinhar, ao invés do óbvio &quot;Administrador&quot; ou &quot;Back-end&quot;. Por padrão, as senhas usadas para [fazer logon](../getting-started/admin-signin.md) para o Administrador deve ter sete ou mais caracteres e incluir letras e números. Como um [prática recomendada](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html), use somente senhas de Administrador fortes que incluam uma combinação de letras, números e símbolos. O Adobe Commerce e o Magento Open Source não permitem a reutilização das quatro últimas senhas atribuídas à conta.

A configuração de segurança do Administrador oferece a capacidade de:

- Adicionar uma chave secreta aos URLs
- Exigir senhas para diferenciar maiúsculas de minúsculas
- Limitar a duração das sessões de Administrador
- Limitar a duração das senhas
- Limitar o número de tentativas de logon que podem ser feitas antes que a conta de usuário administrador seja [bloqueado](permissions-users-all.md#locked-users).

Para aumentar a segurança, você pode configurar o comprimento da inatividade do teclado antes que a sessão atual expire e exigir que o nome de usuário e a senha diferenciem maiúsculas de minúsculas.

Além das configurações de segurança nesta seção, [autenticação de dois fatores](security-two-factor-authentication.md) (2FA) é necessário para verificar a identidade dos usuários com uma senha única gerada por um aplicativo ou dispositivo. Você será solicitado a configurar o 2FA na primeira vez que fizer logon no Admin. Para maior segurança, o logon de Administrador também pode ser configurado para exigir uma [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Lojas que foram habilitadas [!DNL Adobe Identity Management Services] (IMS) têm o Adobe Commerce nativo e o Magento Open Source 2FA desabilitado. Os usuários administradores que estão conectados à instância do Commerce com suas credenciais de Adobe não precisam se autenticar novamente para muitas tarefas de administrador. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [[!DNL Adobe Identity Management Service] Visão geral da integração do (IMS)](../getting-started/adobe-ims-integration-overview.md).

Para obter informações técnicas, consulte [Visão geral de segurança](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;} na documentação do desenvolvedor.

![Segurança do administrador](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Configurar a segurança do administrador

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL Advanced]_, escolha **[!UICONTROL Admin]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Security]** seção.

1. Para impedir que usuários Administradores façam logon na mesma conta em dispositivos diferentes, defina **[!UICONTROL Admin Account Sharing]** para `No`.

1. Para determinar o método usado para gerenciar solicitações de redefinição de senha, defina **[!UICONTROL Password Reset Protection Type]** a um dos seguintes:

   - `By IP and Email` — A senha pode ser redefinida on-line depois que uma resposta recebida da notificação é enviada ao endereço de e-mail associado à conta de administrador.
   - `By IP` — A senha pode ser redefinida on-line sem confirmação adicional.
   - `By Email` — A senha pode ser redefinida somente respondendo por e-mail à notificação enviada para o endereço de e-mail associado à conta de Administrador.
   - `None` — A senha pode ser redefinida somente pelo administrador de armazenamento.

1. Definir opções de segurança de logon:

   - Para **[!UICONTROL Recovery Link Expiration Period (hours)]**, digite o número de horas que um link de recuperação de senha permanece válido.

   - Para determinar o número máximo de solicitações de senha que podem ser enviadas por hora, digite o número de **[!UICONTROL Max Number of Password Reset Requests]**.

   - Para **[!UICONTROL Min Time Between Password Reset Requests]**, insira o número mínimo de minutos entre as solicitações de redefinição de senha.

   - Para anexar uma chave secreta ao URL do Administrador como precaução contra explorações, defina **[!UICONTROL Add Secret Key to URLs]** para `Yes`. Essa configuração é ativada por padrão.

   - Para exigir que o uso de caracteres maiúsculos e minúsculos em qualquer credencial de logon inserida corresponda ao que está armazenado no sistema, defina **[!UICONTROL Login is Case Sensitive]** para `Yes`.

   - Para determinar a duração de uma sessão de Administrador antes que ela expire, insira a duração da sessão em segundos para **[!UICONTROL Admin Session Lifetime (seconds)]** campo. O valor deve ser de 60 segundos ou superior.

   - Para **[!UICONTROL Maximum Login Failures to Lockout Account]**, digite o número de vezes que um usuário pode tentar fazer logon no Administrador antes que a conta seja bloqueada. Por padrão, são permitidas seis tentativas. Deixe o campo vazio para tentativas de logon ilimitadas.

   - Para **[!UICONTROL Lockout Time (minutes)]**, digite o número de minutos em que uma conta de administrador é bloqueada quando o número máximo de tentativas é atingido.

1. Definir opções de senha:

   - Para limitar o tempo de vida de senhas de Administrador, digite o número de dias que uma senha é válida **[!UICONTROL Password Lifetime (days)]**. Por tempo de vida ilimitado, deixe o campo em branco.

   - Definir **[!UICONTROL Password Change]** a um dos seguintes:

      - `Forced` — Exige que os usuários administradores alterem suas senhas após a configuração da conta.
      - `Recommended` — Recomenda que os usuários administradores alterem suas senhas após a configuração da conta.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Requisitos de senha do administrador

Por padrão, a senha do administrador deve ter sete ou mais caracteres e incluir letras e números.
