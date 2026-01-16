---
title: Google reCAPTCHA V3 e V2
description: Saiba como configurar o Google reCAPTCHA para acesso de Administrador e várias ações de vitrine iniciadas por clientes registrados.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 80b2ecc9fddd7a20d6824182f41f0d19f6d51003
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 0%

---

# Google reCAPTCHA V3 e V2

O [Google reCAPTCHA](https://developers.google.com/recaptcha) garante que um ser humano, em vez de um computador (ou &quot;bot&quot;), esteja interagindo com o seu site. Ao contrário do Adobe Commerce padrão e do Magento Open Source [CAPTCHA](security-captcha.md), o Google reCAPTCHA fornece segurança aprimorada com uma seleção de diferentes opções e métodos de exibição. Informações adicionais sobre o tráfego do site estão disponíveis no painel da conta do Google reCAPTCHA.

O Google reCAPTCHA é configurado separadamente para o Administrador e a loja.

- Para o Administrador, o Google reCAPTCHA pode ser usado na página [Entrar](../getting-started/admin-signin.md) e quando um usuário solicitar uma redefinição de senha. Se o Commerce padrão [CAPTCHA](security-captcha.md) também estiver habilitado, o Google reCAPTCHA poderá ser usado ao mesmo tempo sem nenhum problema.

- Para a loja, o Google reCAPTCHA pode ser usado para entrar em uma [conta de cliente](../customers/customer-sign-in.md), enviar uma mensagem da página [Fale Conosco](../getting-started/store-details.md#contact-us-form) e em várias outras localizações de loja.

  ![Google reCAPTCHA - logon do cliente](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

O Google reCAPTCHA pode ser implementado de várias maneiras:

- _reCAPTCHA v3 Invisible_ — Usa um algoritmo para classificar interações de usuário e determina a probabilidade de o usuário ser humano com base em uma pontuação.

- _reCAPTCHA v2 Invisible_ — Executa verificação em segundo plano sem interação com o usuário. Os usuários e clientes são verificados automaticamente, mas pode ser necessário selecionar imagens específicas para concluir um desafio.

- _reCAPTCHA v2 (&quot;Não sou um robô&quot;)_ — Valida solicitações com a caixa de seleção _&quot;Não sou um robô&quot;_.

>[!IMPORTANT]
>
>Antes de configurar o Google reCAPTCHA, verifique se o arquivo `PHP.ini` inclui a seguinte configuração: `allow_url_fopen = 1`. Isso pode exigir ajuda do desenvolvedor. Consulte [Configurações PHP Necessárias](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html){:target="_blank"} no Guia de Instalação.

## Etapa 1: gerar chaves reCAPTCHA do Google

O Google reCAPTCHA requer um par de chaves de API para ser habilitado. Você pode obter essas chaves gratuitamente no site reCAPTCHA. Antes de gerar as chaves, você deve saber o tipo de reCAPTCHA que deseja usar.

1. Abra a página do Google reCAPTCHA e faça logon em sua conta.

1. Para **[!UICONTROL Label]**, insira um nome para identificar as chaves para referência interna.

   Você precisa de um conjunto de chaves para cada tipo de reCAPTCHA usado na instalação do Adobe Commerce ou do Magento Open Source. Por exemplo: `Commerce Invisible`

1. Para **[!UICONTROL reCAPTCHA type]**, escolha o método que deseja usar.

   - _reCAPTCHA v3 Invisível_
   - _reCAPTCHA v2 Invisível_
   - _reCAPTCHA v2 (&quot;Não sou um robô&quot;)_

1. Para **[!UICONTROL Domain]**, insira o domínio do seu armazenamento. Por exemplo: mystore.com

   Se você tiver várias lojas com domínios diferentes, insira cada domínio em uma linha separada.

   - Adicione o domínio de armazenamento e quaisquer subdomínios.
   - Você pode adicionar `localhost`, outros domínios de VM locais e domínios de preparo conforme necessário para testes.

1. Marque a caixa de seleção para **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (Opcional) Marque a caixa de seleção **[!UICONTROL Send alerts to owners]** para enviar uma notificação se o Google detectar problemas ou tráfego suspeito.

1. Clique em **[!UICONTROL Submit]** para concluir o registro e receber chaves.

   >[!IMPORTANT]
   >
   >Nem todas as chaves são aplicáveis a todos os tipos de reCAPTCHA, e aplicá-las incorretamente pode levar a um comportamento inesperado. Por exemplo, chaves reCAPTCHA do Google geradas para reCAPTCHA v2 &quot;Não sou um robô&quot; não funcionam com o _reCAPTCHA v2 Invisible_ e podem bloquear a funcionalidade em que o reCAPTCHA está habilitado.

## Etapa 2: configurar o Google reCAPTCHA para o administrador

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

1. Faça logon em sua conta de administrador.

1. Na barra lateral Admin, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No canto superior direito, defina **[!UICONTROL Store View]** como `Default Config`.

1. No painel esquerdo, expanda **[!UICONTROL Security]** e clique em **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Desmarque a caixa de seleção **[!UICONTROL Use system value]** para cada campo que você deseja configurar.

1. Para usar _[!DNL reCAPTCHA v2 ("I am not a robot")]_, expanda a seção **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**e faça o seguinte:

   - Para **[!UICONTROL Google API Website Key]**, insira a chave do site que foi criada para esse tipo de reCAPTCHA quando você registrou sua conta do Google reCAPTCHA.

   - Para **[!UICONTROL Google API Secret Key]**, insira a chave secreta associada à sua conta do Google reCAPTCHA.

   - Para **[!UICONTROL Size]**, escolha o tamanho da caixa do Google reCAPTCHA que você deseja exibir. Opções: `Normal (default)` / `Compact`

   - Para **[!UICONTROL Theme]**, escolha o tema que deseja usar para estilizar a caixa reCAPTCHA do Google. Opções: `Light Theme (default)` / `Dark Theme`

   - Para **[!UICONTROL Language Code]**, insira o código de dois caracteres para especificar o [idioma usado para texto e mensagens do Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - &quot;Não sou um robô&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. Para usar _[!DNL reCAPTCHA v2 Invisible]_, expanda a seção **[!UICONTROL reCAPTCHA v2 Invisible]**e faça o seguinte:

   - Para **[!UICONTROL Google API Website Key]**, insira a chave do site que foi criada para esse tipo de reCAPTCHA quando você registrou sua conta do Google reCAPTCHA.

   - Para **[!UICONTROL Google API Secret Key]**, insira a chave secreta associada à sua conta do Google reCAPTCHA.

   - Para **[!UICONTROL Invisible Badge Position]**, escolha a posição do selo a ser usado em cada página. Opções: `Inline` / `Bottom Right` / `Bottom Left`

   - Para **[!UICONTROL Theme]**, escolha o tema a ser usado para estilizar a caixa do reCAPTCHA do Google. Opções: `Light Theme (default)` / `Dark Theme`

   - Para **[!UICONTROL Language Code]**, insira um código de dois caracteres que especifique o [idioma usado para texto e mensagens do Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 Invisível](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. Para usar _[!DNL reCAPTCHA v3 Invisible]_, expanda a seção **[!UICONTROL reCAPTCHA v3 Invisible]**e faça o seguinte:

   - Para **[!UICONTROL Google API Website Key]**, insira a chave do site que foi criada para esse tipo de reCAPTCHA quando você registrou sua conta do Google reCAPTCHA.

   - Para **[!UICONTROL Google API Secret Key]**, insira a chave secreta associada à sua conta do Google reCAPTCHA.

   - Insira o **[!UICONTROL Minimum Score Threshold]** para identificar quando uma interação do usuário é sinalizada como um risco potencial; onde 1.0 é uma interação típica do usuário e 0.0 provavelmente é um bot. Padrão: `0.5`

   - Para **[!UICONTROL Invisible Badge Position]**, escolha a posição a ser usada em cada página. Opções: `Inline` / `Bottom Right` / `Bottom Left`

   - Para **[!UICONTROL Theme]**, escolha o tema a ser usado para estilizar a caixa do reCAPTCHA do Google. Opções: `Light Theme (default)` / `Dark Theme`

   - Para **[!UICONTROL Language Code]**, insira um código de dois caracteres que especifique o [idioma usado para texto e mensagens do Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 Invisível](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Expanda **[!UICONTROL reCAPTCHA Validation Failure Messages]** e insira as mensagens que aparecem no Administrador se a validação falhar ou não puder ser concluída.

   ![Mensagens de falha do reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Expanda a seção **[!UICONTROL Admin Panel]** e configure o seguinte conforme necessário:

   - Defina **[!UICONTROL Enable for Login]** como o tipo reCAPTCHA que você deseja usar para a página de Entrada do Administrador.

   - Defina **[!UICONTROL Enable for Forgot Password]** com o tipo reCAPTCHA que você deseja usar para solicitações de redefinição de senha.

   ![Opções de administrador do reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Etapa 3: configurar o Google reCAPTCHA para a loja

1. No painel esquerdo, em _[!UICONTROL Security]_, escolha **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Complete a seção para cada tipo de reCAPTCHA que deseja usar na loja.

   Consulte as informações em _Etapa 2: Configurar o Google reCAPTCHA para o Administrador_ para obter detalhes sobre as opções para cada tipo de reCAPTCHA.

1. Expanda **[!UICONTROL reCAPTCHA Validation Failure Messages]** e insira as mensagens que aparecem na loja se a validação falhar ou não puder ser concluída.

1. Expanda a seção **[!UICONTROL Storefront]**.

   >[!NOTE]
   >
   >Desmarque a caixa de seleção **[!UICONTROL Use system value]** para cada campo que você deseja configurar.

1. Defina cada campo de localização da loja com o tipo de reCAPTCHA que você configurou para usar.

   {{recaptcha-forms-list}}

   ![Configuração de opções de vitrine eletrônica](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Etapa 4: salvar a configuração

1. Quando as configurações estiverem concluídas, clique em **[!UICONTROL Save Config]**.

1. Na mensagem na parte superior do espaço de trabalho, clique em **[!UICONTROL Cache Management]** e atualize cada cache inválido.
