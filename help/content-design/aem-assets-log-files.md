---
title: Configurar rotação de log
description: Configure a rotação do log para a Integração do AEM Assets para o Commerce.
feature: CMS, Media, Integration
source-git-commit: 9e1f80d24eed078b5b28ae2d102c3f3df457081d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Configurar Experience Manager Assets

A integração do AEM Assets para o Commerce fornece os seguintes arquivos de log:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Solicite ao administrador do sistema que verifique a programação de rotação dos arquivos de registro para esses registros, a fim de evitar que eles fiquem muito grandes. Em alguns ambientes, os arquivos de log são girados automaticamente, mas em outros ambientes você deve configurar a rotação de log manualmente. Para obter detalhes, consulte os seguintes tópicos:

- Para instalações locais do Adobe Commerce, peça ao Administrador do Sistema para configurar a [rotação de log](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings).
- Para projetos de infraestrutura em nuvem do Adobe Commerce, consulte [Exibir e gerenciar logs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html).


