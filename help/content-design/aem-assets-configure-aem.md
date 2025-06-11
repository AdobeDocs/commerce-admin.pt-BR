---
title: Instalar pacote do AEM Assets para o Commerce
description: Adicione os metadados de ativos necessários para habilitar a Integração do AEM Assets para o Commerce a fim de sincronizar ativos entre projetos do Adobe Commerce e do Experience Manager Assets.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Instalar o pacote do AEM Assets

A Adobe fornece um modelo de projeto, `commerce-assets`, para adicionar namespace Commerce e recursos de esquema de metadados à configuração do ambiente Experience Manager Assets as a Cloud Service. Implante esse modelo no seu ambiente como um pacote Maven. Em seguida, configure os metadados do Commerce no ambiente de criação do AEM Assets para concluir a configuração.

O modelo adiciona os seguintes recursos ao ambiente de criação do AEM Assets.

- Um [namespace personalizado](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json), `Commerce` para identificar propriedades relacionadas ao Commerce.

- Um tipo de metadados personalizado `commerce:isCommerce` com o rótulo `Eligible for Commerce` para marcar ativos da Commerce associados a um projeto do Adobe Commerce.

- Um tipo de metadados personalizado `commerce:productmetadata` e um componente correspondente da interface do usuário para adicionar uma propriedade *[!UICONTROL Product Data]*. Os Dados do produto incluem as propriedades de metadados para associar um ativo do Commerce às SKUs do produto e para especificar os atributos da imagem `role` e `position` para o ativo.

  ![Controle de IU de Dados de Produto Personalizado](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- Um formulário de esquema de metadados com uma guia Commerce que inclui os campos `Eligible for Commerce?` e `Product Data` para marcar ativos do Commerce. O formulário também fornece opções para mostrar ou ocultar os campos `roles` e `order` (posição) da interface do usuário do AEM Assets.

  ![Guia Commerce para o formulário de esquema de metadados do AEM Assets](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- Um [ativo de Commerce marcado e aprovado](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg` de amostra para oferecer suporte à sincronização de ativos inicial. Somente ativos aprovados do Commerce podem ser sincronizados do AEM Assets para o Adobe Commerce.

>[!NOTE]
>Para obter informações adicionais sobre o modelo de projeto do AEM `commerce-assets`, consulte o [Leiame](https://github.com/ankumalh/assets-commerce).

Você precisa dos seguintes recursos e permissões para usar este projeto do AEM para atualizar a configuração do ambiente:

- [Acesso ao Programa e aos ambientes do AEM Assets Cloud Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo) com as funções de Gerente de Programa e de Implantação.

- Um [ambiente de desenvolvimento local do AEM](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) e familiaridade com o processo de desenvolvimento local do AEM.

- Entenda a [estrutura do projeto do AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) e como implantar pacotes de conteúdo personalizados usando o Cloud Manager.

## Instalar o pacote `commerce-assets`

1. No Cloud Manager, crie ambientes de produção e de preparo para seu projeto do AEM Assets, se necessário.

1. Configurar um pipeline de implantação, se necessário.

1. No GitHub, baixe o código do modelo do [projeto Commerce-Assets AEM](https://github.com/ankumalh/assets-commerce).

1. A partir do seu [ambiente de desenvolvimento local do AEM](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview), instale o código personalizado na sua configuração de ambiente do AEM Assets como um pacote Maven ou copiando manualmente o código na configuração de projeto existente.

1. Confirme as alterações e envie a ramificação de desenvolvimento local para o repositório Git do Cloud Manager.

1. No Cloud Manager, [implante seu código para atualizar o ambiente do AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager).

## Configurar um perfil de metadados

No ambiente de criação do AEM Assets, defina valores padrão para os metadados de ativos do Commerce criando um perfil de metadados. Em seguida, aplique o novo perfil às pastas do AEM Asset para usar automaticamente esses padrões. Essa configuração simplifica o processamento de ativos, reduzindo as etapas manuais.

Ao configurar o perfil de metadados, é necessário configurar apenas os seguintes componentes:

- Adicione uma guia Commerce. Essa guia ativa as configurações específicas do Commerce adicionadas pelo modelo
- Adicione o campo `Eligible for Commerce` à guia Commerce.

O componente da interface de dados do produto é adicionado automaticamente com base no modelo.

### Configurar o perfil de metadados

1. Faça logon no ambiente de criação do Adobe Experience Manager.

1. No espaço de trabalho do Adobe Experience Manager, acesse o espaço de trabalho Administração de conteúdo do autor para o AEM Assets clicando no ícone Adobe Experience Manager.

   ![criação no AEM Assets](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Abra as Ferramentas do administrador selecionando o ícone de martelo.

   ![Administrador do AEM Author Admin para gerenciar perfis de metadados](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Abra a página de configuração do perfil clicando em **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** um perfil de metadados para a integração com o Commerce.

   ![Administrador do AEM Author Admin adicionou perfis de metadados ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Adicione uma guia para metadados do Commerce.

   1. À esquerda, clique em **[!UICONTROL Settings]**.

   1. Clique em **[!UICONTROL +]** na seção da guia e especifique o **[!UICONTROL Tab Name]**, `Commerce`.

1. Adicione o campo `Eligible for Commerce` ao formulário.

   ![Administrador do AEM Author adiciona campos de metadados ao perfil](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

   - Clique em **[!UICONTROL Build form]**.

   - Arraste o campo `Single Line text` para o formulário.

   - Adicione o texto `Eligible for Commerce` para o rótulo clicando em **[!UICONTROL Field Label]**.

   - Na guia Configurações, adicione o texto do rótulo a **Rótulo do Campo**.

   - Defina o texto do espaço reservado como `yes`.

   - No campo **[!UICONTROL Map to Property]**, copie e cole o seguinte valor

     ```terminal
     ./jcr:content/metadata/commerce:isCommerce
     ```

1. Opcional. Para sincronizar automaticamente ativos aprovados do Commerce à medida que forem carregados no ambiente AEM Assets, defina o valor padrão do campo _[!UICONTROL Review Status]_na guia `Basic` como `approved`.

1. Salve a atualização.

#### Aplicar o perfil de metadados à pasta de origem dos ativos do Commerce

1. Na página [!UICONTROL  Metadata Profiles], selecione o perfil de integração do Commerce.

1. No menu de ações, selecione **[!UICONTROL Apply Metadata Profiles to Folders]**.

1. Selecione a pasta que contém os ativos do Commerce.

   Crie uma pasta do Commerce se ela não existir.

1. Clique em **[!UICONTROL Apply]**.

## Próxima etapa

[Instalar pacotes do Adobe Commerce](aem-assets-configure-commerce.md)
