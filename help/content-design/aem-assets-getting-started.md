---
title: Configurar a integração do AEM Assets para o Commerce
description: Saiba como instalar e configurar o ambiente do Experience Manager Assets para gerenciar ativos do Commerce na sua loja.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
source-git-commit: 934473c5124002b3b0b1bee2da47afff468406dc
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Configurar a integração do AEM Assets para o Commerce

A definição da integração do Adobe Experience Manager Assets para o Commerce requer acesso administrativo para personalizar a configuração do aplicativo e do ambiente.

- Acesso administrativo ao programa do Cloud Manager em que os ambientes do AEM Assets as a Cloud Service são provisionados.

- Acesso administrativo ao ambiente do Adobe Commerce e a capacidade de recuperar ou gerar as chaves de API necessárias para autenticação.

## Requisitos para usar a integração

Para aproveitar essa integração, as empresas devem atender aos seguintes requisitos:

- Licenças ativas para Adobe Commerce, Adobe Experience Manager Assets e [AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

   - PHP 8.1, 8.2, 8.3
   - Compositor: 2.x

- O Adobe Experience Manager foi provisionado com o [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/overview)

- O usuário do Adobe Commerce que está configurando a integração deve ter acesso à [Organização IMS](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) onde o projeto do AEM Assets é provisionado.

## Principais benefícios

- **Sem Custo Adicional**—Esta integração é fornecida gratuitamente para comerciantes que atendem aos requisitos de licenciamento.

- **Solução oficial da Adobe**—Desenvolvida, mantida e totalmente suportada pela Adobe, garantindo estabilidade e alinhamento com futuros aprimoramentos da plataforma.

- **Modelo de suporte gerenciado da Adobe**—A Adobe cuida da assistência e da solução de problemas, proporcionando tranquilidade e agilizando a resolução de problemas.

## Próximas etapas

A habilitação da integração do Commerce com o Experience Manager Assets é um processo de três etapas:

1. [Configure seu projeto do Adobe Experience Manager Assets para gerenciar ativos do Adobe Commerce](aem-assets-configure-aem.md).

1. [Instale a integração do Adobe Experience Manager Assets para a extensão do Commerce e configure o Adobe Commerce](aem-assets-configure-aem.md).

1. [Habilitar a sincronização de ativos](aem-assets-setup-synchronization.md).
