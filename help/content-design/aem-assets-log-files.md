---
title: Configurar rotação de log
description: Configure a rotação do log para a Integração do AEM Assets para o Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Configurar Experience Manager Assets

A integração do AEM Assets para o Commerce fornece os seguintes arquivos de log na instância do Commerce:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Solicite ao administrador do sistema que verifique a programação de rotação dos arquivos de registro para esses registros, a fim de evitar que eles fiquem muito grandes. Em alguns ambientes, os arquivos de log são girados automaticamente, mas em outros ambientes você deve configurar a rotação de log manualmente. Para obter detalhes, consulte os seguintes tópicos:

- Para instalações locais do Adobe Commerce, peça ao Administrador do Sistema para configurar a [rotação de log](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings).
- Para projetos de infraestrutura em nuvem do Adobe Commerce, consulte [Exibir e gerenciar logs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html).
