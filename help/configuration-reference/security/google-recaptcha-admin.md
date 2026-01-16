---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel]'
description: Revise as configurações na página [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel] do Administrador do Commerce.
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 6fe5ffb6f529f95e32bb12a55ae16100f4d1bbbb
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Antes de configurar o Google reCAPTCHA, verifique se o arquivo `PHP.ini` inclui a seguinte configuração: `allow_url_fopen = 1`. Isso pode exigir ajuda do desenvolvedor. Consulte [Configurações PHP Necessárias](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) no _Guia de Instalação_.

{{config}}

Para obter mais informações sobre como alterar essas configurações, consulte o [Google reCAPTCHA](../../systems/security-google-recaptcha.md) no _Guia de Sistemas de Administração_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;Não sou um robô&quot;)](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | A chave do site que é criada ao registrar sua conta do Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | A chave secreta associada à sua conta do Google reCAPTCHA. |
| [!UICONTROL Size] | Global | O tamanho da caixa do Google reCAPTCHA que aparece durante o logon. Opções: `Normal` (padrão) / `Compact` |
| [!UICONTROL Theme] | Global | Determina o estilo da caixa do reCAPTCHA do Google. Opções: `Light Theme` (padrão) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | Um [código de dois caracteres](https://developers.google.com/recaptcha/docs/language) que especifica o idioma usado para texto e mensagens do Google reCAPTCHA. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Invisível](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | A chave do site que é criada ao registrar sua conta do Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | A chave secreta associada à sua conta do Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Global | A posição do selo reCAPTCHA invisível em cada página. Opções: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Determina o estilo da caixa do reCAPTCHA do Google. Opções: `Light Theme` (padrão) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | Um [código de dois caracteres](https://developers.google.com/recaptcha/docs/language) que especifica o idioma usado para texto e mensagens do Google reCAPTCHA. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 Invisível](./assets/recaptcha-admin-v3-invisible.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | A chave do site que é criada ao registrar sua conta do Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | A chave secreta associada à sua conta do Google reCAPTCHA. |
| [!UICONTROL Minimum Score Threshold] | Global | A pontuação mínima que identifica uma interação do usuário como um risco potencial, onde 1,0 é uma interação típica do usuário e 0,0 provavelmente é um bot. Padrão: `0.5` |
| [!UICONTROL Invisible Badge Position] | Global | A posição do selo reCAPTCHA invisível em cada página. Opções: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Determina o estilo da caixa do reCAPTCHA do Google. Opções: `Light Theme` (padrão) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | Um [código de dois caracteres](https://developers.google.com/recaptcha/docs/language) que especifica o idioma usado para texto e mensagens do Google reCAPTCHA. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Mensagens de falha](./assets/recaptcha-admin-failure-messages.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Global | A mensagem que é exibida no Admin se a verificação falhar. Texto padrão: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Global | A mensagem que é exibida no Admin se o reCAPTCHA não retornar um resultado de verificação. Texto padrão: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Admin Panel]

![Painel de administração](./assets/recaptcha-admin-panel.png)<!-- zoom -->

>[!NOTE]
>
>O tipo do reCAPTCHA escolhido deve corresponder ao tipo associado à chave de API da sua conta do Google reCAPTCHA.

>[!WARNING]
>
>Ao usar o reCAPTCHA versão 3, um usuário genuíno com baixa pontuação não pode continuar. Para a versão 2, um usuário genuíno com uma pontuação baixa recebe um desafio. Considere cuidadosamente se os usuários originais com uma pontuação baixa devem ter a oportunidade de resolver um desafio (versão 2) ou ser bloqueados (versão 3).

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--|--|--|
| [!UICONTROL Enable for Login] | Global | Determina o tipo de reCAPTCHA habilitado para o [Logon de administrador](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html). Opções:<br/>**`No`**- (padrão) Não valida o logon de Administrador.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Exige que o usuário marque a caixa de seleção _Não sou um robô_.<br />**`Invisible reCAPTCHA v2`**- Valida o comportamento do usuário em segundo plano sem exigir interações com base na pontuação.<br/>**`Invisible reCAPTCHA v3`** - (Recomendado) Valida o comportamento do usuário em segundo plano com base na pontuação de interação. |
| [!UICONTROL Enable for Forgot Password] | Global | Determina o tipo de reCAPTCHA habilitado para solicitar uma [redefinição de senha de administrador](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html#reset-your-password). Opções:<br/>**`No`**- (padrão) Não valida a solicitação de redefinição de senha.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Exige que o usuário marque a caixa de seleção _Não sou um robô_.<br />**`Invisible reCAPTCHA v2`**- Valida o comportamento do usuário em segundo plano sem exigir interações com base na pontuação.<br/>**`Invisible reCaptcha v3`** - (Recomendado) Valida o comportamento do usuário em segundo plano com base na pontuação de interação. |

{style="table-layout:auto"}
