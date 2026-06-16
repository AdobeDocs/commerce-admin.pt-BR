---
title: Detecção de recursos do navegador
description: Saiba como configurar a detecção de recursos do navegador e exibir um aviso se as configurações do navegador do cliente precisarem ser alteradas.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/zPxdplYIYblw6-tsDvxEmvKfAx-2M6opb6qjX7YL1I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 0%

---

# Detecção de recursos do navegador

Como a maioria dos sites e aplicativos na Internet, o Adobe Commerce e o Magento Open Source exigem que o navegador do visitante permita o uso de cookies e do JavaScript para operações completas. No entanto, ocasionalmente, o navegador de um usuário é definido com a configuração de privacidade mais alta que impede cookies e o JavaScript. Sua loja pode ser configurada para testar os recursos do navegador de cada visitante e exibir um aviso se as configurações precisarem ser alteradas.

- Se as configurações de privacidade do navegador não permitirem cookies, você poderá configurar o sistema para redirecioná-los automaticamente para a página [Habilitar Cookies](../content-design/pages.md#enable-cookies), que explica como fazer as configurações recomendadas com a maioria dos navegadores.
- Se as configurações de privacidade do navegador não permitirem o JavaScript, você poderá configurar o sistema para exibir a seguinte mensagem acima do cabeçalho de cada página.

Para obter informações técnicas, consulte [Navegadores suportados](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) no _Guia de Instalação_.

## Configurar a detecção de recursos do navegador

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel à esquerda, abaixo de _[!UICONTROL General]_, escolha **[!UICONTROL Web]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Browser Capabilities Detection]** e faça o seguinte:

   - Para exibir instruções que expliquem como configurar o navegador para permitir cookies, defina **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** como `Yes`.

   - Para exibir um banner acima do cabeçalho quando o JavaScript estiver desabilitado no navegador do usuário, defina **[!UICONTROL Show Notice if JavaScript is Disabled]** como `Yes`.

   - Para exibir um banner acima do cabeçalho quando o Armazenamento local estiver desabilitado no navegador do usuário, defina **[!UICONTROL Show Notice if Local Storage is Disabled]** como `Yes`.

   ![Configuração geral - Detecção de recursos do navegador da Web](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
