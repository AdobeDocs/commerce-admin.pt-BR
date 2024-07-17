---
title: Configurar Experience Manager Assets
description: Adicione os metadados de ativos necessários para habilitar a Integração do AEM Assets para o Commerce a fim de sincronizar ativos entre projetos do Adobe Commerce e do Experience Manager Assets.
feature: CMS, Media, Integration
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Configurar Experience Manager Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Para gerenciar ativos de mídia para sua loja usando a integração do AEM Assets para o Commerce, seu projeto do AEM Assets exige a adição de determinados metadados para garantir que você possa pesquisar e gerenciar facilmente os ativos do Commerce. Esses metadados também facilitam a sincronização de ativos entre o Adobe Commerce e o Experience Manager Assets. Após definir os campos de metadados, o mapeamento inicial desses campos ocorre automaticamente na primeira vez que um ativo do Commerce é compartilhado com o Experience Manager Assets.

Para a integração, você configura dois tipos de metadados:

- O **[perfil de metadados](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles)** permite aplicar metadados padrão a ativos em uma pasta. Todos os ativos na pasta herdam os metadados padrão configurados no perfil.

- O **[esquema de metadados](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)** define o layout da página de propriedades e o conjunto de campos que podem ser usados como propriedades de metadados em um ativo AEM.

## Configurar metadados

Para a integração inicial, adicione os seguintes metadados do Commerce a um perfil de metadados do AEM Assets e a um esquema de metadados.

| Tipo de campo | Rótulo | Propriedade | Valor padrão |
|------ | ------- | ---------- | ------------- |
| Texto | **Ele existe no Adobe Commerce?** | `./jcr:content/metadata/commerce:isCommerce` | sim |
| Texto multivalor | **SKUs** | `./jcr:content/metadata/commerce:skus` | nenhum |
| Texto multivalor | **Posições** | `./jcr:content/metadata/commerce:positions` | nenhum |
| Texto multivalor | **Funções** | `./jcr:content/metadata/commerce:roles` | nenhum |


### Adicionar campos do Commerce a um perfil de metadados

1. No espaço de trabalho do Adobe Experience Manager, acesse o espaço de trabalho de administração de conteúdo do autor para o AEM Assets clicando no ícone Adobe Experience Manager.

   ![criação no AEM Assets](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Abra as Ferramentas do administrador selecionando o ícone de martelo.

   ![Administrador do AEM para gerenciar perfis de metadados](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Abra a página de configuração do perfil clicando em **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** um perfil de metadados para a integração com o Commerce.

   ![Administrador do AEM adiciona perfis de metadados ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Adicione uma guia para metadados do Commerce.

   1. À esquerda, clique em **[!UICONTROL Settings]**.

   1. Clique em **[!UICONTROL +]** na seção da guia e especifique o **[!UICONTROL Tab Name]**, `Commerce`.

1. Adicione os [campos de metadados](#configure-metadata) ao formulário.

   ![Administrador do autor do AEM adiciona campos de metadados ao perfil](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Salve a atualização.

1. Aplique o perfil de metadados `Commerce integration` à pasta em que os ativos do Commerce estão armazenados.

   1. Na página [!UICONTROL  Metadata Profiles], selecione o perfil de integração do Commerce.

   1. No menu de ações, selecione **[!UICONTROL Apply Metadata Profiles to Folder(s)]**.

   1. Selecione a pasta que contém os ativos do Commerce.

      Crie uma pasta do Commerce se ela não existir.

   1. Clique em **[!UICONTROL Apply]**.

### Adicionar campos do Commerce a um formulário de esquema de metadados

1. No painel de administração Conteúdo de Autor do AEM para Assets, abra **[!UICONTROL Metadata Schemas]** ([!UICONTROL Manage metadata schema forms]).

   ![Esquema de metadados de atualização do Administrador do AEM](./assets/aem-assets-manage-metadata-schema.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create]** um esquema de metadados para o Commerce.

   ![Esquema de metadados de atualização do Administrador do AEM](./assets/aem-assets-create-metadata-schema.png){width="600" zoomable="yes"}

1. No [!UICONTROL Metadata Schema Form], crie os campos `Does Commerce exist?` e `Commerce mappings` e mapeie as propriedades.

1. Clique em **[!UICONTROL Save]**.


## Publish e um ativo

Depois de configurar os metadados de AEM e o perfil de esquema para ativos do Commerce, crie o primeiro ativo do Commerce para mapear os campos de metadados do Commerce.

1. No Experience Manager, vá para [!UICONTROL Assets > Files], selecione a pasta **Commerce**.

1. Carregue uma imagem para um projeto do Commerce arrastando o arquivo para a pasta ou clicando em **[!UICONTROL Add Assets]**.

1. Verifique a configuração de metadados: **isCommerce** está definida como `true` e se a propriedade `commerce:skus` está definida como SKU para o produto Commerce associado à imagem.

1. Aprove o ativo.


## Adicionar um ativo à pasta do Commerce

Crie pelo menos um ativo na pasta AEM Assets Commerce que tenha os atributos de metadados do Commerce atribuídos.

Esse ativo é necessário para configurar a sincronização entre a instância do Commerce e o AEM Assets.

## Mapear metadados para ativos

Os metadados são mapeados quando um ativo do Commerce é publicado pela primeira vez.  do Commerce pela primeira vez. Os ativos de mídia que têm os campos incorporados ou personalizados são mapeados automaticamente para os campos especificados na primeira vez que um ativo é enviado ao Experience Manager Assets.

Antes de começar o mapeamento de ativos, conclua as seguintes tarefas:

- [Instalar e configurar a Integração do AEM Assets para o Commerce](aem-assets-configure-commerce.md)
- [Ativar a sincronização de ativos para transferir ativos entre o ambiente do projeto do Adobe Commerce e o ambiente do projeto do AEM Assets](aem-assets-setup-synchronization.md)
