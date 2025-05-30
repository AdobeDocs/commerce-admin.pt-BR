---
title: Configurar a segurança do administrador
description: Saiba como configurar a segurança para o Administrador da loja.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Configurar a segurança do administrador

Recomendamos que você adote uma abordagem multifacetada para proteger a segurança de sua loja. Você pode começar usando uma [URL de administrador personalizada](../stores-purchase/store-urls.md#use-a-custom-admin-url) que não é fácil de adivinhar, em vez da óbvia &quot;Admin&quot; ou &quot;Infraestrutura&quot;. Por padrão, as senhas usadas para [fazer logon](../getting-started/admin-signin.md) no Administrador devem ter sete ou mais caracteres e incluir letras e números. Como uma [prática recomendada](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=pt-BR), use somente senhas de Administrador fortes que incluam uma combinação de letras, números e símbolos. A Adobe Commerce e a Magento Open Source não permitem a reutilização das quatro últimas senhas atribuídas à conta.

A configuração de segurança do Administrador oferece a capacidade de:

- Adicionar uma chave secreta aos URLs
- Exigir senhas para diferenciar maiúsculas de minúsculas
- Limitar a duração das sessões de Administrador
- Limitar a duração das senhas
- Limite o número de tentativas de logon que podem ser feitas antes que a conta de usuário Administrador seja [bloqueada](permissions-users-all.md#locked-users).

Para aumentar a segurança, você pode configurar o comprimento da inatividade do teclado antes que a sessão atual expire e exigir que o nome de usuário e a senha diferenciem maiúsculas de minúsculas.

Além das configurações de segurança desta seção, a [autenticação de dois fatores](security-two-factor-authentication.md) (2FA) é necessária para verificar a identidade dos usuários com uma senha de uso único gerada por um aplicativo ou dispositivo. Você será solicitado a configurar o 2FA na primeira vez que fizer logon no Admin. Para maior segurança, o logon de Administrador também pode ser configurado para exigir um [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Os armazenamentos que habilitaram a autenticação [!DNL Adobe Identity Management Services] (IMS) têm o Adobe Commerce nativo e o Magento Open Source 2FA desabilitados. Os usuários administradores que estão conectados à instância do Commerce com suas credenciais do Adobe não precisam se autenticar novamente para muitas tarefas administrativas. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [[!DNL Adobe Identity Management Service] (IMS) Visão geral da integração](../getting-started/adobe-ims-integration-overview.md).

Para obter informações técnicas, consulte [Visão geral sobre segurança](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"} na documentação do desenvolvedor.

![Segurança do administrador](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Configurar a segurança do administrador

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL Advanced]_, escolha **[!UICONTROL Admin]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Security]**.

1. Para impedir que usuários Administradores façam logon na mesma conta em diferentes dispositivos, defina **[!UICONTROL Admin Account Sharing]** como `No`.

1. Para determinar o método usado para gerenciar solicitações de redefinição de senha, defina **[!UICONTROL Password Reset Protection Type]** como um dos seguintes:

   - `By IP and Email` — A senha pode ser redefinida online depois que uma resposta recebida da notificação é enviada para o endereço de email associado à conta de Administrador.
   - `By IP` — A senha pode ser redefinida online sem confirmação adicional.
   - `By Email` — A senha só pode ser redefinida respondendo por email à notificação enviada para o endereço de email associado à conta de Administrador.
   - `None` — A senha pode ser redefinida somente pelo administrador de armazenamento.

1. Definir opções de segurança de logon:

   - Para **[!UICONTROL Recovery Link Expiration Period (hours)]**, insira o número de horas que um link de recuperação de senha permanece válido.

   - Para determinar o número máximo de solicitações de senha que podem ser enviadas por hora, digite o número para **[!UICONTROL Max Number of Password Reset Requests]**.

   - Para **[!UICONTROL Min Time Between Password Reset Requests]**, insira o número mínimo de minutos que devem decorrer entre as solicitações de redefinição de senha.

   - Para anexar uma chave secreta à URL do Administrador como precaução contra explorações, defina **[!UICONTROL Add Secret Key to URLs]** como `Yes`. Essa configuração é ativada por padrão.

   - Para exigir que o uso de caracteres maiúsculos e minúsculos em qualquer credencial de logon inserida corresponda ao que está armazenado no sistema, defina **[!UICONTROL Login is Case Sensitive]** como `Yes`.

   - Para determinar a duração de uma sessão de Administrador antes que ela expire, insira a duração da sessão em segundos para o campo **[!UICONTROL Admin Session Lifetime (seconds)]**. O valor deve ser de 60 segundos ou superior.

   - Para **[!UICONTROL Maximum Login Failures to Lockout Account]**, insira o número de vezes que um usuário pode tentar fazer logon no Administrador antes que a conta seja bloqueada. Por padrão, são permitidas seis tentativas. Deixe o campo vazio para tentativas de logon ilimitadas.

   - Para **[!UICONTROL Lockout Time (minutes)]**, insira o número de minutos durante os quais uma conta de Administrador é bloqueada quando o número máximo de tentativas é atingido.

1. Definir opções de senha:

   - Para limitar o tempo de vida de senhas de Administrador, digite o número de dias que uma senha é válida por **[!UICONTROL Password Lifetime (days)]**. Por tempo de vida ilimitado, deixe o campo em branco.

   - Defina **[!UICONTROL Password Change]** como um dos seguintes:

      - `Forced` — Requer que os usuários Administradores alterem suas senhas após a configuração da conta.
      - `Recommended` — Recomenda que os usuários administradores alterem suas senhas após a configuração da conta.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Requisitos de senha do administrador

Por padrão, a senha do administrador deve ter sete ou mais caracteres e incluir letras e números.
