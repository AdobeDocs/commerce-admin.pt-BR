---
title: Configurar a integração do AEM Assets para o Commerce
description: Saiba como instalar e configurar o ambiente do Experience Manager Assets para gerenciar ativos do Commerce na sua loja.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/loyCmoFINQvC-13BGzAUKmcF7gY6T2e6mV-lK-SnVxo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 42029ed6d13cd4203c4a5d8300297315aac1abf5
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 3%

---

# Configurar a integração do AEM Assets para o Commerce

A definição da integração do Adobe Experience Manager Assets para o Commerce requer acesso administrativo para personalizar a configuração do aplicativo e do ambiente.

- Acesso administrativo ao programa do Cloud Manager em que os ambientes do AEM Assets as a Cloud Service são provisionados.

- Acesso administrativo ao ambiente do Adobe Commerce e a capacidade de recuperar ou gerar as chaves de API necessárias para autenticação.

## Requisitos para usar a integração

Para aproveitar essa integração, as empresas devem atender aos seguintes requisitos:

- Licenças ativas para Adobe Commerce, Adobe Experience Manager Assets e [AEM Dynamic Media](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

- O Adobe Experience Manager foi provisionado com o [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/overview)

- O usuário do Adobe Commerce que está configurando a integração deve ter acesso à [Organização IMS](https://experienceleague.adobe.com/pt-br/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) onde o projeto do AEM Assets é provisionado.

## Principais benefícios

- **Sem Custo Adicional**—Esta integração é fornecida gratuitamente para comerciantes que atendem aos requisitos de licenciamento.

- **Solução oficial da Adobe**—Desenvolvida, mantida e totalmente suportada pela Adobe, garantindo estabilidade e alinhamento com futuros aprimoramentos da plataforma.

- **Modelo de suporte gerenciado da Adobe**—A Adobe cuida da assistência e da solução de problemas, proporcionando tranquilidade e agilizando a resolução de problemas.

## Próximas etapas

A habilitação da integração do Commerce com o Experience Manager Assets é um processo de três etapas:

1. [Instalar pacote do AEM Assets](aem-assets-configure-aem.md).
1. [Instalar pacotes do Adobe Commerce](aem-assets-configure-aem.md).
1. [Configurar o ativo de integração](aem-assets-setup-synchronization.md).
