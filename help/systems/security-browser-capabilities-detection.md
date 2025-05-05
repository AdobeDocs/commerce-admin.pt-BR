---
title: Detecção de recursos do navegador
description: Saiba como configurar a detecção de recursos do navegador e exibir um aviso se as configurações do navegador do cliente precisarem ser alteradas.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Detecção de recursos do navegador

Como a maioria dos sites e aplicativos na Internet, o Adobe Commerce e o Magento Open Source exigem que o navegador do visitante permita cookies e JavaScript para operações completas. No entanto, ocasionalmente, o navegador de um usuário é definido com a configuração de privacidade mais alta que impede cookies e o JavaScript. Sua loja pode ser configurada para testar os recursos do navegador de cada visitante e exibir um aviso se as configurações precisarem ser alteradas.

- Se as configurações de privacidade do navegador não permitirem cookies, você poderá configurar o sistema para redirecioná-los automaticamente para a página [Habilitar Cookies](../content-design/pages.md#enable-cookies), que explica como fazer as configurações recomendadas com a maioria dos navegadores.
- Se as configurações de privacidade do navegador não permitirem o JavaScript, você poderá configurar o sistema para exibir a seguinte mensagem acima do cabeçalho de cada página.

Para obter informações técnicas, consulte [Navegadores suportados](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=pt-BR#supported-browsers) no _Guia de Instalação_.

## Configurar a detecção de recursos do navegador

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel à esquerda, abaixo de _[!UICONTROL General]_, escolha **[!UICONTROL Web]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Browser Capabilities Detection]** e faça o seguinte:

   - Para exibir instruções que expliquem como configurar o navegador para permitir cookies, defina **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** como `Yes`.

   - Para exibir um banner acima do cabeçalho quando o JavaScript estiver desabilitado no navegador do usuário, defina **[!UICONTROL Show Notice if JavaScript is Disabled]** como `Yes`.

   - Para exibir um banner acima do cabeçalho quando o Armazenamento local estiver desabilitado no navegador do usuário, defina **[!UICONTROL Show Notice if Local Storage is Disabled]** como `Yes`.

   ![Configuração geral - Detecção de recursos do navegador da Web](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
