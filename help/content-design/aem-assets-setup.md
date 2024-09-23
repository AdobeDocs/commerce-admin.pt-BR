---
title: Configurar a integração do AEM Assets
description: Saiba mais sobre os requisitos e as etapas para configurar a integração entre o Adobe Commerce e o AEM Assets as a Cloud Service.
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Configurar a integração do AEM Assets

Habilite recursos avançados de gerenciamento de ativos configurando o ambiente do AEM Assets e instalando e configurando a integração do AEM Assets com o Commerce.

Quando a integração está ativa, os administradores podem usar o Experience Manager Assets as a Cloud Service como a única fonte da verdade para a criação e o gerenciamento de ativos e como uma ferramenta central de gerenciamento de ativos digitais (DAM) para criar, gerenciar, organizar e distribuir ativos para projetos da Commerce.

## Requisitos

- Adobe Commerce 2.4.5+
   - PHP 8.1, 8.2, 8.3
   - Compositor: 2.x
- O Adobe Experience Manager foi provisionado com o [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/overview)
- O usuário do Adobe Commerce que está configurando a integração deve ter acesso à [Organização IMS](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) onde o projeto do AEM Assets é provisionado.

## Configurar a integração

>[!BEGINSHADEBOX]

**Pré-requisitos**

A configuração da integração do AEM Assets requer acesso administrativo para personalizar a configuração do aplicativo e do ambiente.

- Acesso administrativo ao programa Cloud Manager, onde os ambientes as a Cloud Service do AEM Assets são provisionados.
- Acesso administrativo ao ambiente do Adobe Commerce e capacidade de recuperar ou gerar chaves de API necessárias para autenticação.

>[!ENDSHADEBOX]

A habilitação da integração do Commerce com o Experience Manager Assets é um processo de três etapas:

1. [Configure seu projeto do Experience Manager Assets para gerenciar ativos do Commerce](aem-assets-configure-aem.md).

1. [Instale a extensão Integração do Experience Manager Assets e configure o Adobe Commerce](aem-assets-configure-aem.md).

1. [Habilitar a sincronização de ativos](aem-assets-setup-synchronization.md).
