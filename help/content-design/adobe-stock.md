---
title: Integração do Adobe Stock
description: Integrar o Adobe Stock com o seu [!DNL Commerce] para acessar inúmeros ativos de mídia para uso em sua loja.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 6666073a48741cb494f408a61401f46fc20cedc4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Integração do Adobe Stock

Para obter acesso a inúmeros ativos de mídia para uso em sua loja, integre [Adobe Stock][adobe-stock] com [!UICONTROL Commerce].

![Resultados de pesquisa do Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

O serviço Adobe Stock fornece às empresas acesso a milhões de fotos, vetores, ilustrações, vídeos, modelos e ativos 3D de alta qualidade, com curadoria e isentos de royalties, para todos os seus projetos criativos. [!DNL Commerce] Os usuários do podem encontrar, visualizar e licenciar rapidamente os ativos do Adobe Stock. Os usuários também podem salvá-los na [armazenamento de mídia][media-storage], tudo sem sair do espaço de trabalho de Administração.

## Pré-requisitos

Essa integração exige:

- Um [Adobe Developer][dev-console] account
- Adobe Commerce ou Magento Open Source, 2.3.4 ou posterior

O licenciamento de imagens do Adobe Stock exige:

- Um [conta Adobe][adobe-signin]
- Um pagamento [Adobe Stock][adobe-stock] plano associado à conta

## Integrar [!DNL Commerce] e ADOBE STOCK

A configuração da integração do Adobe Stock para o Adobe Commerce é um processo de duas etapas:

1. [Criar uma integração adobe.developer](#create-an-adobe-developer-integration) para gerar uma chave de API
1. [Configurar a integração do Adobe Stock no Administrador de comércio](#configure-the-adobe-stock-integration)

### Criar uma integração do Adobe Developer

1. Navegue até a [Console do Adobe Developer][dev-console].

1. Em _[!UICONTROL Quick Start]_, clique em **[!UICONTROL Create new project]**.

1. No _[!UICONTROL Project overview]_clique em **[!UICONTROL Add API]**.

1. Selecionar **[!UICONTROL Adobe Stock]** na lista de integrações e clique em **[!UICONTROL Next]**.

1. Selecione o OAuth 2.0 **[!UICONTROL Web App]**.

1. Especifique a **[!UICONTROL redirect URI]**.

   O URI de redirecionamento padrão está no formulário `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, como `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, em que:

   - `${HOST}` é seu [!DNL Commerce] nome de domínio totalmente qualificado (por exemplo, `https://store.myshop.com`).
   - `${ADMIN_URI}` é seu [!DNL Commerce] URI do administrador (como `admin_hgkq1l`), que pode ser recuperado executando `magento info:adminuri`.

1. Especifique a **[!UICONTROL Redirect URI pattern]**, que é o mesmo que o URI de redirecionamento com duas diferenças:

   - Qualquer ponto (`.`) deve ser evitada com duas barras invertidas (`\\`).
   - Adicionar `.*` até o fim do padrão.

   Usando o exemplo do URI de redirecionamento padrão anterior, seria `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Clique em **[!UICONTROL Next]**.

1. Revise os escopos disponíveis e clique em **[!UICONTROL Save configured API]**.

1. Na página seguinte, copie o **[!UICONTROL Client ID]** (Chave de API) e **[!UICONTROL Client secret]**.

   Essas informações são usadas nas etapas da próxima seção.

### Configurar a integração do Adobe Stock

Para definir a configuração do sistema no seu [!DNL Commerce] Administrador, use o _Chave de API_ e _Client secret_ gerado no [seção anterior][create-integration].

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** e faça o seguinte:

   - Definir **[!UICONTROL Enabled Adobe Stock]** para `Yes`.

   - Insira seu **[!UICONTROL API Key (Client ID)]**.

   - Insira seu **[!UICONTROL Client Secret]**.

   - Clique em **[!UICONTROL Test Connection]** para validar suas chaves.

   ![Configuração avançada - Integração com o Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Conceda alguns segundos à validação. Se suas credenciais forem válidas, você deverá ver uma _Conexão bem sucedida!_ mensagem.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
