---
title: Integração do Adobe Stock
description: Integre o Adobe Stock com sua instância  [!DNL Commerce]  para acessar inúmeros ativos de mídia para uso em sua loja.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 6666073a48741cb494f408a61401f46fc20cedc4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Integração do Adobe Stock

Para obter acesso a inúmeros ativos de mídia para uso em sua loja, integre o [Adobe Stock][adobe-stock] ao [!UICONTROL Commerce].

![Resultados da Pesquisa do Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

O serviço Adobe Stock fornece às empresas acesso a milhões de fotos, vetores, ilustrações, vídeos, modelos e ativos 3D de alta qualidade, com curadoria e isentos de royalties, para todos os seus projetos criativos. Os usuários do [!DNL Commerce] podem rapidamente encontrar, visualizar e licenciar os ativos da Adobe Stock. Os usuários também podem salvá-los no [armazenamento de mídia][media-storage], tudo sem sair do espaço de trabalho de Administrador.

## Pré-requisitos

Essa integração exige:

- Uma conta do [Adobe Developer][dev-console]
- Adobe Commerce ou Magento Open Source, 2.3.4 ou posterior

O licenciamento de imagens do Adobe Stock exige:

- Uma conta [Adobe][adobe-signin]
- Um plano pago [Adobe Stock][adobe-stock] associado à conta

## Integrar o [!DNL Commerce] e o Adobe Stock

A configuração da integração do Adobe Stock para o Adobe Commerce é um processo de duas etapas:

1. [Crie uma integração adobe.developer](#create-an-adobe-developer-integration) para gerar uma Chave de API
1. [Configurar a integração do Adobe Stock no Commerce Admin](#configure-the-adobe-stock-integration)

### Criar uma integração do Adobe Developer

1. Navegue até [Adobe Developer Console][dev-console].

1. Em _[!UICONTROL Quick Start]_, clique em **[!UICONTROL Create new project]**.

1. No bloco _[!UICONTROL Project overview]_, clique em **[!UICONTROL Add API]**.

1. Selecione **[!UICONTROL Adobe Stock]** na lista de integrações e clique em **[!UICONTROL Next]**.

1. Selecione o OAuth 2.0 **[!UICONTROL Web App]**.

1. Especifique o **[!UICONTROL redirect URI]**.

   O URI de redirecionamento padrão está no formato `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, como `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, onde:

   - `${HOST}` é seu nome de domínio [!DNL Commerce] totalmente qualificado (por exemplo, `https://store.myshop.com`).
   - `${ADMIN_URI}` é o URI do Administrador [!DNL Commerce] (como `admin_hgkq1l`), que pode ser recuperado executando `magento info:adminuri`.

1. Especifique o **[!UICONTROL Redirect URI pattern]**, que é o mesmo que o URI de redirecionamento com duas diferenças:

   - Todos os pontos (`.`) devem ser evitados com duas barras invertidas (`\\`).
   - Adicionar `.*` ao final do padrão.

   Usando o exemplo do URI de redirecionamento padrão anterior, ele seria `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Clique em **[!UICONTROL Next]**.

1. Revise os escopos disponíveis e clique em **[!UICONTROL Save configured API]**.

1. Na página a seguir, copie o **[!UICONTROL Client ID]** (Chave de API) e o **[!UICONTROL Client secret]**.

   Essas informações são usadas nas etapas da próxima seção.

### Configurar a integração do Adobe Stock

Para definir a configuração do sistema no Administrador [!DNL Commerce], use a _Chave da API_ e o _Segredo do cliente_ gerados na [seção anterior][create-integration].

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** e faça o seguinte:

   - Defina **[!UICONTROL Enabled Adobe Stock]** como `Yes`.

   - Insira seu **[!UICONTROL API Key (Client ID)]**.

   - Insira seu **[!UICONTROL Client Secret]**.

   - Clique em **[!UICONTROL Test Connection]** para validar suas chaves.

   ![Configuração avançada - Integração com o Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Conceda alguns segundos à validação. Se suas credenciais forem válidas, você deverá ver uma _Conexão bem-sucedida!_ mensagem.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
