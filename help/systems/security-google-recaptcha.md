---
title: Google reCAPTCHA
description: Saiba como configurar o Google reCAPTCHA para acesso de Administrador e várias ações de vitrine iniciadas por clientes registrados.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) A garante que um ser humano, em vez de um computador (ou &quot;bot&quot;), esteja interagindo com seu site. Ao contrário do padrão Adobe Commerce e Magento Open Source [CAPTCHA](security-captcha.md), o Google reCAPTCHA oferece segurança aprimorada com uma seleção de diferentes opções e métodos de exibição. Informações adicionais sobre o tráfego do site estão disponíveis no painel da conta do Google reCAPTCHA.

O Google reCAPTCHA é configurado separadamente para o Administrador e a loja.

- Para o Administrador, o Google reCAPTCHA pode ser usado no [Conectar](../getting-started/admin-signin.md) e quando um usuário solicitar uma redefinição de senha. Se o Commerce padrão [CAPTCHA](security-captcha.md) também estiver ativado, o Google reCAPTCHA pode ser usado ao mesmo tempo, sem problemas.

- Na loja, o Google reCAPTCHA pode ser usado para fazer logon em uma [conta do cliente](../customers/customer-sign-in.md), envie uma mensagem do [Entre em contato](../getting-started/store-details.md#contact-us-form) página e em vários outros locais de loja.

  ![Google reCAPTCHA - logon do cliente](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

O Google reCAPTCHA pode ser implementado de várias maneiras:

- _reCAPTCHA v3 Invisível_ — Usa um algoritmo para classificar as interações do usuário e determina a probabilidade de o usuário ser humano com base em uma pontuação.

- _reCAPTCHA v2 Invisível_ — Executa verificação em segundo plano sem interação com o usuário. Os usuários e clientes são verificados automaticamente, mas pode ser necessário selecionar imagens específicas para concluir um desafio.

- _reCAPTCHA v2 (&quot;Não sou um robô&quot;)_ — Valida solicitações com o _&quot;Eu não sou um robô&quot;_ caixa de seleção

>[!IMPORTANT]
>
>Antes que o Google reCAPTCHA possa ser configurado, verifique se `PHP.ini` O arquivo inclui a seguinte configuração: `allow_url_fopen = 1`. Isso pode exigir ajuda do desenvolvedor. Consulte [Configurações de PHP necessárias](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html){:target=&quot;_blank&quot;} no Guia de instalação.

## Etapa 1: gerar chaves reCAPTCHA do Google

O Google reCAPTCHA requer um par de chaves de API para ser habilitado. Você pode obter essas chaves gratuitamente no site reCAPTCHA. Antes de gerar as chaves, você deve saber o tipo de reCAPTCHA que deseja usar.

1. Abra a página do Google reCAPTCHA e faça logon em sua conta.

1. Para **[!UICONTROL Label]**, digite um nome para identificar as chaves para referência interna.

   Você precisa de um conjunto de chaves para cada tipo de reCAPTCHA usado na instalação do Adobe Commerce ou Magento Open Source. Por exemplo: `Commerce Invisible`

1. Para **[!UICONTROL reCAPTCHA type]**, escolha o método que deseja usar.

   - _reCAPTCHA v3 Invisível_
   - _reCAPTCHA v2 Invisível_
   - _reCAPTCHA v2 (&quot;Não sou um robô&quot;)_

1. Para **[!UICONTROL Domain]**, insira o domínio da loja. Por exemplo: mystore.com

   Se você tiver várias lojas com domínios diferentes, insira cada domínio em uma linha separada.

   - Adicione o domínio de armazenamento e quaisquer subdomínios.
   - Você pode adicionar `localhost`, outros domínios de VM local e domínios de preparo, conforme necessário para testes.

1. Marque a caixa de seleção para **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (Opcional) Selecione a **[!UICONTROL Send alerts to owners]** caixa de seleção para enviar notificação se o Google detectar problemas ou tráfego suspeito.

1. Clique em **[!UICONTROL Submit]** para concluir o registro e receber chaves.

   >[!IMPORTANT]
   >
   >Nem todas as chaves são aplicáveis a todos os tipos de reCAPTCHA, e aplicá-las incorretamente pode levar a um comportamento inesperado. Por exemplo, as chaves reCAPTCHA do Google geradas para reCAPTCHA v2 &quot;Não sou um robô&quot; não funcionam com o _reCAPTCHA v2 Invisível_ e poderia bloquear a funcionalidade em que o reCAPTCHA está habilitado.

## Etapa 2: configurar o Google reCAPTCHA para o administrador

1. Faça logon em sua conta de administrador.

1. Na barra lateral Admin, acesse **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No canto superior direito, defina **[!UICONTROL Store View]** para `Default Config`.

1. No painel esquerdo, expanda **[!UICONTROL Security]** e clique em **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Limpe a **[!UICONTROL Use system value]** para cada campo que você deseja configurar.

1. Para usar _[!DNL reCAPTCHA v2 ("I am not a robot")]_, expanda a **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**e faça o seguinte:

   - Para **[!UICONTROL Google API Website Key]**, insira a chave do site criada para esse tipo de reCAPTCHA quando você registrou sua conta do Google reCAPTCHA.

   - Para **[!UICONTROL Google API Secret Key]**, insira a chave secreta associada à conta do Google reCAPTCHA.

   - Para **[!UICONTROL Size]**, escolha o tamanho da caixa do Google reCAPTCHA que você deseja exibir. Opções: `Normal (default)` / `Compact`

   - Para **[!UICONTROL Theme]**, escolha o tema que deseja usar para criar o estilo da caixa do reCAPTCHA do Google. Opções: `Light Theme (default)` / `Dark Theme`

   - Para **[!UICONTROL Language Code]**, insira o código de dois caracteres para especificar o [idioma usado para mensagens e texto do Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - &quot;Não sou um robô&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. Para usar _[!DNL reCAPTCHA v2 Invisible]_, expanda a **[!UICONTROL reCAPTCHA v2 Invisible]**e faça o seguinte:

   - Para **[!UICONTROL Google API Website Key]**, insira a chave do site criada para esse tipo de reCAPTCHA quando você registrou sua conta do Google reCAPTCHA.

   - Para **[!UICONTROL Google API Secret Key]**, insira a chave secreta associada à conta do Google reCAPTCHA.

   - Para **[!UICONTROL Invisible Badge Position]**, escolha a posição do selo a ser usado em cada página. Opções: `Inline` / `Bottom Right` / `Bottom Left`

   - Para **[!UICONTROL Theme]**, escolha o tema a ser usado para criar o estilo da caixa do Google reCAPTCHA. Opções: `Light Theme (default)` / `Dark Theme`

   - Para **[!UICONTROL Language Code]**, insira um código de dois caracteres que especifique o [idioma usado para mensagens e texto do Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 Invisível](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. Para usar _[!DNL reCAPTCHA v3 Invisible]_, expanda a **[!UICONTROL reCAPTCHA v3 Invisible]**e faça o seguinte:

   - Para **[!UICONTROL Google API Website Key]**, insira a chave do site criada para esse tipo de reCAPTCHA quando você registrou sua conta do Google reCAPTCHA.

   - Para **[!UICONTROL Google API Secret Key]**, insira a chave secreta associada à conta do Google reCAPTCHA.

   - Insira o **[!UICONTROL Minimum Score Threshold]** para identificar quando uma interação do usuário é sinalizada como um risco potencial; onde 1.0 é uma interação típica do usuário e 0.0 é provavelmente um bot. Padrão: `0.5`

   - Para **[!UICONTROL Invisible Badge Position]**, escolha a posição a ser usada em cada página. Opções: `Inline` / `Bottom Right` / `Bottom Left`

   - Para **[!UICONTROL Theme]**, escolha o tema a ser usado para criar o estilo da caixa do Google reCAPTCHA. Opções: `Light Theme (default)` / `Dark Theme`

   - Para **[!UICONTROL Language Code]**, insira um código de dois caracteres que especifique o [idioma usado para mensagens e texto do Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 Invisível](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Expandir **[!UICONTROL reCAPTCHA Validation Failure Messages]** e insira as mensagens que aparecem no Admin se a validação falhar ou não puder ser concluída.

   ![Mensagens de falha do reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Expanda a **[!UICONTROL Admin Panel]** e configure o seguinte conforme necessário:

   - Definir **[!UICONTROL Enable for Login]** ao tipo reCAPTCHA que você deseja usar para a página Logon de administração.

   - Definir **[!UICONTROL Enable for Forgot Password]** ao tipo reCAPTCHA que você deseja usar para solicitações de redefinição de senha.

   ![Opções de administração do reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Etapa 3: configurar o Google reCAPTCHA para a loja

1. No painel esquerdo, em _[!UICONTROL Security]_, escolha **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Complete a seção para cada tipo de reCAPTCHA que deseja usar na loja.

   Consulte as informações em _Etapa 2: configurar o Google reCAPTCHA para o administrador_ para obter detalhes sobre as opções para cada tipo de reCAPTCHA.

1. Expandir **[!UICONTROL reCAPTCHA Validation Failure Messages]** e insira as mensagens que aparecem na loja se a validação falhar ou não puder ser concluída.

1. Expanda a **[!UICONTROL Storefront]** seção.

   >[!NOTE]
   >
   >Limpe a **[!UICONTROL Use system value]** para cada campo que você deseja configurar.

1. Defina cada campo de localização da loja com o tipo de reCAPTCHA que você configurou para usar.

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg) (Disponível somente com o Adobe Commerce B2B)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![Configuração de opções da vitrine eletrônica](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Etapa 4: salvar a configuração

1. Quando as configurações estiverem concluídas, clique em **[!UICONTROL Save Config]**.

1. Na mensagem localizada na parte superior do espaço de trabalho, clique em **[!UICONTROL Cache Management]** e atualizar cada cache inválido.
