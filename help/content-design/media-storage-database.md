---
title: Usar um banco de dados de mídia
description: Saiba como usar um banco de dados de mídia para armazenar seus  [!DNL Commerce] arquivos de mídia.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Usar um banco de dados de mídia

>[!IMPORTANT]
>
>O método de armazenamento de mídia de banco de dados está obsoleto a partir do Adobe Commerce e do Magento Open Source 2.4.3.

Por padrão, todas as imagens, arquivos CSS compilados e arquivos JavaScript compilados da instância [!DNL Commerce] são armazenados no sistema de arquivos no servidor Web. Você pode optar por armazenar esses arquivos em um banco de dados em um servidor de banco de dados. Uma vantagem dessa abordagem é a opção de sincronização automática e sincronização reversa entre o sistema de arquivos do servidor Web e o banco de dados. Você pode usar o banco de dados padrão para armazenar mídia ou criar uma. Para poder usar um banco de dados recém-criado como armazenamento de mídia, você deve adicionar informações sobre ele e suas credenciais de acesso ao arquivo `env.php`.

## Fluxo de trabalho do banco de dados

1. **Mídia de solicitações do navegador** - Uma página da loja é aberta no navegador do cliente e o navegador solicita a mídia especificada na HTML.

1. **O sistema procura mídia no sistema de arquivos** - O sistema procura a mídia no sistema de arquivos e, se for encontrada, a transmite para o navegador.

1. **O sistema localiza a mídia no banco de dados** - Se a mídia não for encontrada no sistema de arquivos, uma solicitação para a mídia será enviada para o banco de dados especificado na configuração.

1. **O sistema localiza a mídia no banco de dados** - Um script PHP transfere os arquivos do banco de dados para o sistema de arquivos e envia para o navegador do cliente. A solicitação do navegador para mídia aciona o script para ser executado da seguinte maneira:

   - Se o servidor Web [regravações](../merchandising-promotions/url-rewrite.md) estiver habilitado para [!DNL Commerce] e suportado pelo servidor, o script PHP somente será executado quando a mídia solicitada não for encontrada no sistema de arquivos.
   - Se as regravações do servidor Web estiverem desabilitadas para [!DNL Commerce] ou não forem suportadas pelo servidor, o script PHP executará mesmo assim, mesmo se a mídia necessária estiver disponível no sistema de arquivos.

## Usar um banco de dados para armazenamento de mídia

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL System]**.

1. No canto superior esquerdo, defina **[!UICONTROL Store View]** como `Default Config` para aplicar a configuração no nível global.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Storage Configuration for Media]** e faça o seguinte:

   ![Configuração avançada - configuração de armazenamento para mídia](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Defina **[!UICONTROL Media Storage]** como `Database`.

   - Defina **[!UICONTROL Select Media Database]** para o banco de dados que você deseja usar.

   - Para transferir a mídia existente para o banco de dados recém-selecionado, clique em **[!UICONTROL Synchronize]**.

   - Insira o **[!UICONTROL Environment Update Time]** em segundos.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
