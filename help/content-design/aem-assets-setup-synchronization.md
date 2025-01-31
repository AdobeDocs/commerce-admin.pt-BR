---
title: Habilitar sincronização de ativos
description: Saiba como conectar seus projetos do Adobe Commerce e do Experience Manager Assets para habilitar a sincronização de ativos entre esses dois sistemas.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e9b3ede8945de0a6ed0cdb02e5675d736764d3e4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Habilitar sincronização de ativos

Durante o processo de ativação, registre a ID do locatário do projeto usando a ID do programa e do ambiente do ambiente de criação do AEM. Essas IDs identificam o projeto do AEM Assets ao qual você está se conectando e fornecem as credenciais para permitir a comunicação entre os ambientes do Commerce e do AEM Assets.

Depois de identificar o projeto de ativos AEM, você seleciona a regra de correspondência para sincronizar ativos entre o Adobe Commerce e o AEM Assets.

- **[!UICONTROL Match by product SKU]** — Regra padrão que corresponde ao SKU nos metadados do ativo com o [SKU do produto Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku) para garantir que os ativos estejam associados aos produtos corretos.

- **[!UICONTROL Custom match]** — Regra de correspondência para cenários mais complexos ou requisitos de negócios específicos que exigem lógica de correspondência personalizada. A implementação da correspondência personalizada requer o desenvolvimento de código personalizado no Adobe Developer App Builder para definir como os ativos são correspondidos aos produtos. Mais detalhes em breve...

Para integração inicial, use a regra padrão *Corresponder por SKU de produto*.

## Pré-requisitos

- [Configurar o AEM Experience Manager Assets para gerenciar ativos da Commerce](#aem-assets-configure-aem)

- [Instale e configure a Integração do AEM Assets para o Commerce](#aem-assets-configure-commerce.md) para adicionar a extensão e gerar as credenciais e conexões necessárias para usar a extensão.

- Crie um tíquete de suporte para solicitar a ativação da integração do AEM Assets. Você deve fornecer o **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** e **[!UICONTROL IMS Org ID]**.

  >[!TIP]
  >
  > (Opcional) Forneça o **[!UICONTROL Asset Selector IMS Client ID]**, se disponível.

## Configurar a conexão

1. Obtenha o [Ambiente de Criação do AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) e a ID do ambiente.

   1. Abra o console AEM Sites e selecione **[!UICONTROL Assets]**.

   1. Copie e salve as IDs de projeto e ambiente da URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. No Administrador do Commerce, abra a configuração da Integração do AEM Assets.

   1. Vá para **[!UICONTROL Store]** > Configuração > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![A Integração do AEM Assets habilita a integração](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Entre no ambiente AEM Assets **[!UICONTROL Program ID]** e **[!UICONTROL Environment ID]**.

1. Digite o **[!UICONTROL Asset Selector IMS Client ID]**, se disponível.

   A [ID do IMS](../getting-started/adobe-ims-config.md) é exigida por [[!UICONTROL Assets Selector]](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/overview-asset-selector), que seleciona imagens para categorias e/ou [!DNL Page Builder].

1. Selecione o [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) para solicitações de autenticação entre o Commerce e o serviço de correspondência de ativos.

1. Permitir que o Commerce aceite atualizações de entrada do AEM Assets definindo **[!UICONTROL Integration enabled]** como `Yes`.

   Depois de habilitar a integração, configure a regra de correspondência de ativos.

   ![Selecionar regra de correspondência de ativos da Integração do AEM Assets](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Defina a regra de correspondência para a sincronização de ativos.

   1. Selecione **[!UICONTROL Match by product SKU]**.

   1. Adicione o [nome do campo de metadados do AEM Assets](aem-assets-configure-aem.md#configure-metadata) definido para SKUs de produtos Commerce no campo **[!UICONTROL Match by product SKU attribute name]**, `commerce:skus` por exemplo.

   ![Selecionar regra de correspondência de ativos da Integração do AEM Assets](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Selecione **[!UICONTROL Save Config]** para aplicar atualizações e iniciar a sincronização de ativos
