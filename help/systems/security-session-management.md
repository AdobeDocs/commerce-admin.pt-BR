---
title: Gerenciamento de sessão
description: Saiba como configurar o gerenciamento de sessão para proteger o Administrador e a loja.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Gerenciamento de sessão

[O gerenciamento de sessão](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) é uma prática recomendada de anti-negação de serviço (DoS) para segurança de API. Uma sessão representa o tempo que um visitante gasta no site e não está relacionada ao tempo em que os usuários administradores ou clientes estão conectados às suas contas.

Uma sessão é uma sequência de transações de resposta e solicitação HTTP de rede associadas ao mesmo usuário. É uma maneira de associar um cliente (Admin) aos seus dados quando ele acessa o servidor. As sessões são usadas para estabelecer variáveis, como direitos de acesso e configurações de localização, que se aplicam a todas as interações que um usuário tem com um aplicativo web durante a sessão.

## Tamanho da sessão

Use as seguintes configurações para limitar o tamanho máximo da sessão para usuários Administradores e visitantes da loja:

- **[!UICONTROL Max Session Size in Admin]** — Limita o tamanho máximo das sessões em bytes. Use `0` para desabilitar.
- **[!UICONTROL Max Session Size in Storefront]** — Limita o tamanho máximo das sessões em bytes. Use `0` para desabilitar.

>[!TIP]
>
>Ambas as configurações são medidas em bytes e o padrão é `256000` bytes (ou 256 KB).

**_Para configurar o tamanho máximo da sessão:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Security]** para acessar as configurações da sessão.

   ![Configurações da sessão](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Insira os novos tamanhos da sessão em bytes.

   >[!WARNING]
   >
   >Definir o valor como muito baixo pode causar problemas. Se você definir uma das opções abaixo do padrão de 256.000 bytes, verá uma mensagem de aviso. Se você clicar em **[!UICONTROL No]**, o sistema alterará o valor para `256000`.

1. Clique em **[!UICONTROL Save Config]**.

### Sessões de administrador

Se você exceder o tamanho máximo de sessão, uma mensagem de erro será exibida e o sistema registrará a restrição de tamanho de sessão no diretório `var/log`.

Se você perder o acesso ao Administrador depois de definir o tamanho da sessão como muito baixo, use a CLI para redefinir a configuração:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Sessões de vitrine eletrônica

Se você exceder o tamanho máximo de sessão, nenhum erro será exibido, mas o sistema registrará a restrição de tamanho de sessão no diretório `var/log`.

## Validação de sessão

O Adobe Commerce e o Magento Open Source permitem validar variáveis de sessão como uma medida de proteção contra possíveis ataques de fixação de sessão ou tentativas de envenenar ou sequestrar sessões de usuário. As Configurações de validação de sessão determinam como as variáveis de sessão são validadas durante cada visita de armazenamento e se a ID da sessão é incluída no URL do armazenamento.

Para obter informações técnicas, consulte [Usar Redis para armazenamento de sessão](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) no _Guia de Configuração_.

![Configuração geral - Validação de sessão da Web](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

A validação verifica se os visitantes são quem dizem ser comparando o valor nas variáveis de validação com os dados da sessão armazenados nos dados `$_SESSION` para o usuário. A validação falhará se as informações não forem transmitidas conforme esperado e a variável correspondente estiver vazia. Dependendo das configurações de validação da sessão, se uma variável de sessão falhar no processo de validação, a sessão do cliente será encerrada imediatamente.

Ativar todas as variáveis de validação pode ajudar a evitar ataques, mas também pode afetar o desempenho do servidor. Por padrão, toda validação de variável de sessão é desativada. Recomendamos que você experimente as configurações para encontrar a melhor combinação para sua instalação do Adobe Commerce ou Magento Open Source. A ativação de todas as variáveis de validação pode ser desnecessariamente restritiva e pode impedir o acesso a clientes que têm conexões com a Internet que passam por um servidor proxy ou são originários de um firewall. Para saber mais sobre as variáveis de sessão e seu uso, consulte a documentação de administração do sistema Linux®.

**_Para configurar a validação da sessão:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda _[!UICONTROL General]_e escolha **[!UICONTROL Web]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Session Validation Settings]**.

1. Defina cada uma das opções de configuração:

   - **[!UICONTROL Validate REMOTE_ADDR]** — Defina como `Yes` para verificar se o endereço IP de uma solicitação corresponde ao que está armazenado na variável `$_SESSION`.

   - **[!UICONTROL Validate HTTP_VIA]** — Defina como `Yes` para verificar se o endereço de proxy de uma solicitação recebida corresponde ao que está armazenado na variável `$_SESSION`.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — Defina como `Yes` para verificar se o endereço encaminhado-para de uma solicitação corresponde ao que está armazenado na variável `$_SESSION`.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — Defina como `Yes` para verificar se o navegador ou dispositivo usado para acessar o armazenamento durante uma sessão corresponde ao que está armazenado na variável `$_SESSION`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Tempo de vida da sessão do administrador

Como medida de segurança, o _Administrador_ está inicialmente definido como tempo limite após 900 segundos (15 minutos) de inatividade do teclado. Você pode ajustar o tempo de vida da sessão para ajustá-lo ao seu estilo de trabalho.

**_Para ajustar a duração da sessão do Administrador:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Role para baixo e expanda **[!UICONTROL Advanced]** no painel lateral esquerdo.

1. Clique em **[!UICONTROL Admin]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Security]_.

1. Por **[!UICONTROL Admin Session Lifetime (seconds)]**, insira o número de segundos durante os quais uma sessão permanece ativa antes do tempo limite.

   ![Configuração avançada - Configurações de segurança do administrador](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.## Tempo de vida da sessão do administrador

Como medida de segurança, o _Administrador_ está inicialmente definido como tempo limite após 900 segundos (15 minutos) de inatividade do teclado. Você pode ajustar o tempo de vida da sessão para ajustá-lo ao seu estilo de trabalho.

**_Para ajustar a duração da sessão do Administrador:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Role para baixo e expanda **[!UICONTROL Advanced]** no painel lateral esquerdo.

1. Clique em **[!UICONTROL Admin]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção _Segurança_.

1. Por **[!UICONTROL Admin Session Lifetime (seconds)]**, insira o número de segundos durante os quais uma sessão permanece ativa antes do tempo limite.

   ![Configuração avançada - Configurações de segurança do administrador](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
