---
title: Proteja seu [!DNL Commerce] account
description: Saiba como usar a autenticação de dois fatores para proteger seu [!DNL Commerce] conta.
exl-id: 4847b5cb-a93a-40d0-8c31-c30afa27c0ce
feature: User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 0%

---

# Proteja seu [!DNL Commerce] account

A autenticação de dois fatores (TFA ou 2FA) é uma camada adicional de segurança para proteger melhor seu [!DNL Commerce] acesso não autorizado à conta. Para concluir o processo de logon, o TFA exige uma _segundo fator_ além das credenciais padrão de nome de usuário e senha. Esse segundo fator assume a forma de códigos de verificação temporários gerados continuamente por um aplicativo TFA instalado em seu dispositivo móvel e emparelhado com seu [!DNL Commerce] conta.

Com o TFA ativado, sua conta fica mais segura. Um usuário não autorizado não pode fazer logon, a menos que tenha suas credenciais de nome de usuário e senha (primeiro fator) e um código de verificação válido do aplicativo TFA em seu dispositivo pessoal (segundo fator).

>[!NOTE]
>
>A autenticação de dois fatores que protege o _Admin_ da sua loja tem uma configuração separada. Para saber mais, consulte [Autenticação de dois fatores](../systems/security-two-factor-authentication.md).

## Antes de começar

Para usar o TFA, você deve ter um aplicativo TFA instalado em seu dispositivo pessoal (como smartphone, tablet, computador). Há muitos disponíveis, mas algumas opções populares e gratuitas incluem:

- Autenticador Google (iOS, Android™, BlackBerry®)

- Authy (iOS, Android™)

- Autenticador Microsoft® (iOS, Android™, Windows Phone)

## Habilitar autenticação de dois fatores

1. Faça logon no [[!DNL Commerce] account][1]{:target=&quot;_blank&quot;}.

1. No painel de navegação esquerdo, selecione **[!UICONTROL Account Settings]** e selecione **[!UICONTROL Two-factor Authentication]**.

   ![Ativar TFA](./assets/2fa-enable.png){width="600" zoomable="yes"}

1. Selecionar **[!UICONTROL Enable]** para iniciar o processo de configuração da autenticação de dois fatores.

1. Insira o **[!UICONTROL Verification Code]** enviado para o seu email e selecione **[!UICONTROL Verify Code]** para continuar.

   ![Insira o código de verificação](./assets/2fA-verification-code-prompt.png){width="400"}

1. Abra o aplicativo de autenticação de dois fatores que você baixou e instalou em seu dispositivo pessoal.

1. No [!UICONTROL SETUP TWO-FACTOR AUTHENTICATION] formulário, use o **[!UICONTROL Setup Code]** para adicionar o Adobe Commerce ao seu aplicativo TFA.

   ![Adicionar o Adobe Commerce ao aplicativo TFA](./assets/commerce-account-2fa-setup-app.png){width="400"}

   Você pode adicionar o código digitalizando o código QR usando o aplicativo TFA ou inserindo-o manualmente. Esse código vincula seu aplicativo TFA ao seu [!DNL Commerce] e permite que as permissões gerem o aplicativo TFA para gerar códigos de verificação para acesso seguro à conta.

1. Conclua a configuração.

   - No [!UICONTROL SETUP TWO FACTOR-AUTHENTICATION] insira o código de verificação do aplicativo de autenticação de dois fatores.

   - Selecionar **[!UICONTROL Verify Code]**.

   >[!NOTE]
   >
   >Por questões de segurança, os códigos de verificação em seu aplicativo TFA expiram e regeneram continuamente. **_Sempre_** usar o código exibido no momento.

1. Salve o **[!UICONTROL Recovery Codes]** apresentado num local seguro e acessível.

   ![Códigos de recuperação de armazenamento](./assets/commerce-account-2fa-store-recovery-codes.png){width="400"}

   Se você não puder fornecer um código de verificação ao fazer logon na [!DNL Commerce] , você deve usar um código de recuperação para recuperar o acesso à conta.

   Cada código de recuperação pode ser usado apenas uma vez, mas você pode [gerar](#generate-new-recovery-codes) novos. Os códigos de recuperação fazem distinção entre maiúsculas e minúsculas.

1. Marque a caixa de seleção de confirmação e selecione **[!UICONTROL Submit]** para continuar.

1. Para garantir que você possa recuperar o acesso à sua conta, insira um **[!UICONTROL Recovery Email]**.

   Esse endereço de e-mail será necessário se você não puder gerar um código de verificação a partir do aplicativo de autenticação de dois fatores e não tiver acesso a um código de recuperação pré-gerado não utilizado.

   Uma vez a cada 24 horas, você pode gerar e enviar um código de recuperação temporário para o endereço de e-mail de recuperação designado. Use esse código para recuperar o acesso à conta.

   >[!IMPORTANT]
   >
   >Mantenha o acesso à sua conta de email de recuperação. Caso contrário, você não poderá usar códigos de recuperação temporários enviados para essa conta.

   ![Definir email de recuperação](./assets/commerce-account-2fa-set-recovery-email.png){width="400"}

1. Marque a caixa de seleção de confirmação e selecione **[!UICONTROL Submit]** para concluir o processo de configuração da autenticação de dois fatores.

   - Uma notificação é enviada para o endereço de email associado à [!DNL Commerce] para confirmar se você habilitou com êxito a autenticação de dois fatores.

   - Uma notificação é enviada para sua conta de email de recuperação para confirmar a configuração.

>[!TIP]
>
>Se você perder seu dispositivo pessoal ou obter um novo, você pode [alterar o aplicativo de autenticação de dois fatores](#change-your-two-factor-authentication-application) e gerar novos códigos de recuperação.

## Fazer logon usando um código de verificação

1. Vá para a [!DNL Commerce] [logon da conta][1]{:target=&quot;_blank&quot;}.

1. Digite suas credenciais de nome de usuário e senha e selecione **[!UICONTROL Login]**.

1. Insira o **[!UICONTROL Verification Code]** exibido no aplicativo de autenticação de dois fatores quando solicitado.

   ![Inserir código de verificação](./assets/commerce-account-2fa-login-verification-code.png){width="600"}

1. Selecionar **[!UICONTROL Submit]** para concluir o processo de logon.

## Fazer logon usando um código de recuperação

1. Vá para a [!DNL Commerce] [logon da conta][1]{:target=&quot;_blank&quot;}.

1. Digite suas credenciais de nome de usuário e senha e selecione **[!UICONTROL Login]**.

1. Selecionar **[!UICONTROL Use recovery code]** para ignorar o prompt do código de verificação.

1. Insira um não usado **[!UICONTROL Recovery Code]** quando solicitado.

   ![Inserir código de recuperação](./assets/2fa-recovery-code.png){width="600"}

1. Selecionar **[!UICONTROL Submit]** para concluir o processo de logon.

## Fazer logon usando seu email de recuperação

1. Faça logon no [[!DNL Commerce] account][1]{:target=&quot;_blank&quot;}.

1. Digite suas credenciais de nome de usuário e senha e selecione **[!UICONTROL Login]**.

1. Selecionar **[!UICONTROL Use recovery code]** para ignorar o prompt do código de verificação.

1. Para obter um código de recuperação temporário por email, selecione o **[!UICONTROL recovery email]** link.

   ![Usar email de recuperação](./assets/2fa-recovery-email.png){width="600"}

1. Abra a conta de email de recuperação para obter o código temporário e insira o código nos campos designados.

1. Selecionar **[!UICONTROL Submit]** para concluir o processo de logon.

Depois de usar um código de recuperação temporário para acessar sua conta, [gerar novos códigos de recuperação](#generate-new-recovery-codes) e salve-as para evitar mais problemas de acesso à conta.

## Exibir seus códigos de recuperação

1. Vá para a [!DNL Commerce] [logon da conta][1]{:target=&quot;_blank&quot;}.

1. Digite suas credenciais de nome de usuário e senha e selecione **[!UICONTROL Login]**.

1. Conclua o processo de logon usando um dos métodos de autenticação de dois fatores descritos anteriormente.

1. No painel de navegação esquerdo, selecione **[!UICONTROL Account Settings]** e selecione **[!UICONTROL Two-factor Authentication]**.

   ![Configurações de 2FA](./assets/commerce-account-2fa-manage.png){width="600" zoomable="yes"}

1. Para exibir os códigos de recuperação pré-gerados, selecione **Exibir Códigos de Recuperação**.

1. Insira o **[!UICONTROL Verification Code]** enviado para o seu email e selecione **[!UICONTROL Verify Code]** para continuar.

   ![Inserir código de verificação](./assets/2fA-verification-code-prompt.png){width="400"}

1. Salve o **Códigos de Recuperação** apresentado num local seguro e acessível.

   Se você não puder fornecer um código de verificação para fazer logon na sua [!DNL Commerce] de recuperação é a única maneira de recuperar o acesso à conta.

   Cada código de recuperação é de uso único, mas você sempre pode [gerar](#generate-new-recovery-codes) novos. Os códigos de recuperação fazem distinção entre maiúsculas e minúsculas.

   ![Exibir códigos de recuperação](./assets/2fa-view-recovery.png){width="400"}

1. Marque a caixa de seleção de confirmação e selecione **[!UICONTROL Submit]** para fechar o diálogo.

## Gerar novos códigos de recuperação

1. Vá para a [!DNL Commerce] [logon da conta][1]{:target=&quot;_blank&quot;}.

1. Digite suas credenciais de nome de usuário e senha e selecione **[!UICONTROL Login]**.

1. Conclua o processo de logon usando um dos métodos de autenticação de dois fatores descritos anteriormente.

1. No painel de navegação esquerdo, selecione **[!UICONTROL Account Settings]** e selecione **[!UICONTROL Two-factor Authentication]**.

1. Para gerar novos Códigos de Recuperação pré-gerados, selecione **Gerar Novos Códigos de Recuperação**.

1. Insira o **[!UICONTROL Verification Code]** enviado para o seu email e selecione **[!UICONTROL Verify Code]** para continuar.

1. Salve o **Códigos de Recuperação** apresentado num local seguro e acessível.

   Se você não puder fornecer um código de verificação ao fazer logon na [!DNL Commerce] de recuperação é a única maneira de recuperar o acesso à conta.

   Todos os códigos de recuperação gerados anteriormente agora são renderizados como inválidos e devem ser descartados (somente o conjunto atual de códigos de recuperação gerados é funcional). Os códigos de recuperação fazem distinção entre maiúsculas e minúsculas.

1. Marque a caixa de seleção de confirmação e selecione **[!UICONTROL Submit]** para fechar o diálogo.

## Alterar email de recuperação

1. Vá para a [!DNL Commerce] [logon da conta][1]{:target=&quot;_blank&quot;}.

1. Digite suas credenciais de nome de usuário e senha e selecione **[!UICONTROL Login]**.

1. Conclua o processo de logon usando um dos métodos de autenticação de dois fatores descritos anteriormente.

1. No painel de navegação esquerdo, selecione **[!UICONTROL Account Settings]** e selecione **[!UICONTROL Two-factor Authentication]**.

1. Selecionar **Alterar email de recuperação** para alterar o e-mail de recuperação registrado para sua conta.

1. Insira o **[!UICONTROL Verification Code]** enviado para o seu email e selecione **[!UICONTROL Verify Code]** para continuar.

1. Para ajudar a garantir que você possa recuperar o acesso à sua conta, insira um **E-mail de recuperação**.

   Esse endereço de e-mail será necessário se você não puder gerar um código de verificação a partir do aplicativo de autenticação de dois fatores e não tiver acesso a um código de recuperação pré-gerado não utilizado.

   Uma vez a cada 24 horas, você pode gerar e enviar um código de recuperação temporário para o endereço de e-mail de recuperação designado. Você pode usar esse código para recuperar o acesso à conta.

   >[!IMPORTANT]
   >
   >Mantenha o acesso à sua conta de email de recuperação. Caso contrário, você não poderá usar códigos de recuperação temporários enviados para essa conta.

1. Marque a caixa de seleção de confirmação e selecione **[!UICONTROL Submit]** para fechar o diálogo.

   O sistema envia uma notificação por e-mail para o e-mail de recuperação que você designou para confirmar que um endereço de e-mail específico está no arquivo como seu e-mail de recuperação para receber códigos de recuperação temporários.

## Alterar o aplicativo de autenticação de dois fatores

1. Vá para a [!DNL Commerce] [logon da conta][1]{:target=&quot;_blank&quot;}.

1. Digite suas credenciais de nome de usuário e senha e selecione **[!UICONTROL Login]**.

1. Conclua o processo de logon usando um dos métodos de autenticação de dois fatores descritos anteriormente.

1. No painel de navegação esquerdo, selecione **[!UICONTROL Account Settings]** e selecione **[!UICONTROL Two-factor Authentication]**.

1. Selecionar **Alterar aplicativo TFA** para usar um aplicativo do TFA diferente com sua conta magento.com.

1. Insira o **[!UICONTROL Verification Code]** enviado para o seu email e selecione **[!UICONTROL Verify Code]** para continuar.

1. Abra o aplicativo de autenticação de dois fatores no seu dispositivo pessoal.

1. Insira o **Código de configuração** no aplicativo de autenticação de dois fatores.

   Você pode adicionar o código digitalizando o código QR usando o aplicativo TFA ou inserindo-o manualmente. Esse código vincula seu aplicativo TFA ao seu [!DNL Commerce] e permite que as permissões do aplicativo TFA gerem códigos de verificação para acesso seguro à conta.

   >[!NOTE]
   >
   >Por questões de segurança, os códigos de verificação em seu aplicativo TFA expiram e regeneram continuamente. **_Sempre_** usar o código exibido no momento.

1. Com seu aplicativo TFA agora emparelhado com seu [!DNL Commerce] conta, insira o **[!UICONTROL Verification Code]** exibido no aplicativo TFA e selecione **[!UICONTROL Verify Code]** para continuar.

1. Salve o **Códigos de Recuperação** apresentado num local seguro e acessível.

   Se você não puder fornecer um código de verificação ao fazer logon na [!DNL Commerce] a única maneira de recuperar o acesso à conta é usar um código de recuperação.

   Cada código de recuperação é de uso único, mas você sempre pode [gerar](#generate-new-recovery-codes) novos. Os códigos de recuperação fazem distinção entre maiúsculas e minúsculas. Os códigos de recuperação fazem distinção entre maiúsculas e minúsculas.

1. Marque a caixa de seleção para confirmar e selecionar **[!UICONTROL Submit]** para continuar.

1. Para ajudar a garantir que você possa recuperar o acesso à sua conta, insira um **E-mail de recuperação**.

   Esse endereço de e-mail será necessário se você não puder gerar um código de verificação a partir do aplicativo de autenticação de dois fatores e não tiver acesso a um código de recuperação pré-gerado não utilizado.

   Uma vez a cada 24 horas, você pode gerar e enviar um código de recuperação temporário para o endereço de e-mail de recuperação designado. Use esse código para recuperar o acesso à conta.

   >[!IMPORTANT]
   >
   >Mantenha o acesso à sua conta de email de recuperação. Caso contrário, você não poderá usar códigos de recuperação temporários enviados para essa conta.

1. Marque a caixa de seleção de confirmação e selecione **[!UICONTROL Submit]** para concluir o processo de configuração da autenticação de dois fatores.

   Uma notificação por e-mail é enviada ao e-mail de recuperação que você designou para confirmar que um endereço de e-mail específico está no arquivo como seu e-mail de recuperação para receber um código de recuperação temporário.

## Desabilitar autenticação de dois fatores

>[!IMPORTANT]
>
>Se sua política de segurança organizacional exigir a autenticação multifator em contas do Adobe Commerce, não será possível desabilitar a autenticação de dois fatores.

1. Vá para a [!DNL Commerce] [logon da conta][1]{:target=&quot;_blank&quot;}.

1. Digite suas credenciais de nome de usuário e senha e selecione **[!UICONTROL Login]**.

1. Conclua o processo de logon usando um dos métodos de autenticação de dois fatores descritos anteriormente.

1. No painel de navegação esquerdo, selecione **[!UICONTROL Account Settings]** e selecione **[!UICONTROL Two-factor Authentication]** por baixo.

1. Selecionar **[!UICONTROL Disable]** para iniciar o processo de desativação do TFA.

1. Insira o **[!UICONTROL Verification Code]** enviado para o seu email e selecione **[!UICONTROL Verify Code]** para continuar.

1. Marque a caixa de seleção de confirmação e selecione **[!UICONTROL Submit]** para concluir a desativação da autenticação de dois fatores.

   O sistema envia uma confirmação de email indicando que o TFA foi desativado na [!DNL Commerce] conta.

   ![Desativar TFA](./assets/2fa-disable.png){width="400"}

[1]: https://account.magento.com/customer/account/login
