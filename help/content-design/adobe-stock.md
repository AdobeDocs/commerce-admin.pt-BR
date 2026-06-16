---
title: Integração do Adobe Stock
description: Integre o Adobe Stock com sua instância  [!DNL Commerce]  para acessar inúmeros ativos de mídia para uso em sua loja.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/VwiTbOAj5V8s7OWtkq5hfoP4LcvNLPR9QaKStaCdArs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c32adafa-ed01-4b31-997e-2413013911b0id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 427
ht-degree: 0%

---

# Integração do Adobe Stock

Para obter acesso a inúmeros ativos de mídia para uso em sua loja, integre o [Adobe Stock](https://stock.adobe.com) ao [!UICONTROL Commerce].

![Resultados da Pesquisa do Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

O serviço Adobe Stock fornece às empresas acesso a milhões de fotos, vetores, ilustrações, vídeos, modelos e ativos 3D de alta qualidade, com curadoria e isentos de royalties, para todos os seus projetos criativos. Os usuários do [!DNL Commerce] podem rapidamente encontrar, visualizar e licenciar os ativos da Adobe Stock. Os usuários também podem salvá-los no [armazenamento de mídia](./media-storage.md), tudo sem sair do espaço de trabalho de Administrador.

## Pré-requisitos

Essa integração exige:

- Uma conta do [Adobe Developer](https://developer.adobe.com/console/home)
- Adobe Commerce ou Magento Open Source, 2.3.4 ou posterior

O licenciamento de imagens do Adobe Stock exige:

- Uma [conta do Adobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html)
- Um plano pago [Adobe Stock](https://stock.adobe.com) associado à conta

## Integrar o [!DNL Commerce] e o Adobe Stock

A configuração da integração do Adobe Stock para o Adobe Commerce é um processo de duas etapas:

1. [Crie uma integração adobe.developer](#create-an-adobe-developer-integration) para gerar uma Chave de API
1. [Configurar a integração do Adobe Stock no Commerce Admin](#configure-the-adobe-stock-integration)

### Criar uma integração do Adobe Developer

1. Navegue até [Adobe Developer Console](https://developer.adobe.com/console/home).

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

   Usando o exemplo do URI de redirecionamento padrão anterior, o padrão seria `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`

1. Clique em **[!UICONTROL Next]**.

1. Revise os escopos disponíveis e clique em **[!UICONTROL Save configured API]**.

1. Na página a seguir, copie o **[!UICONTROL Client ID]** (Chave de API) e o **[!UICONTROL Client secret]**.

   Essas informações são usadas nas etapas da próxima seção.

### Configurar a integração do Adobe Stock

Para definir a configuração do sistema no Administrador [!DNL Commerce], use a _Chave da API_ e o _Segredo do cliente_ gerados na [seção anterior](#create-an-adobeio-integration).

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** e faça o seguinte:

   - Defina **[!UICONTROL Enabled Adobe Stock]** como `Yes`.

   - Insira seu **[!UICONTROL API Key (Client ID)]**.

   - Insira seu **[!UICONTROL Client Secret]**.

   - Clique em **[!UICONTROL Test Connection]** para validar suas chaves.

   ![Configuração avançada - Integração com o Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Conceda alguns segundos à validação. Se suas credenciais forem válidas, você deverá ver uma _Conexão bem-sucedida!_ verde mensagem.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
