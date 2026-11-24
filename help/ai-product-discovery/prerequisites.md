---
title: Pré-requisitos da descoberta de produtos de IA
description: Revise os requisitos para o enriquecimento do catálogo e do PDP e instale a extensão de enriquecimento compartilhado no Adobe Commerce na infraestrutura em nuvem ou no local.
role: Admin, Developer
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%
---
# Pré-requisitos

Antes de usar o enriquecimento do Catálogo ou do PDP, confirme os requisitos que se aplicam a cada implantação e conclua a configuração da sua plataforma Commerce.

## Requisitos para todas as implantações {#all-deployments}

| Requisito | Aplicável a | Detalhes |
| --- | --- | --- |
| Otimizar na Edge | Enriquecimento de PDP | Obrigatório. Otimizar na Edge fornece os dados do produto enriquecidos aos agentes de IA. Consulte o [guia Otimizar na Edge](https://experienceleague.adobe.com/pt-br/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). |
| Encaminhamento de log | Ambos os workflows | Opcional. Habilita recomendações de enriquecimento com base no tráfego de agente. Sem ele, ainda é possível selecionar produtos ou páginas de produtos manualmente. Consulte o [guia de encaminhamento de logs](https://experienceleague.adobe.com/pt-br/docs/brand-visibility/using/log-forwarding/log-forwarding-overview). |
| Loja rastreável | Enriquecimento do catálogo | Obrigatório para recomendações baseadas em rastreo. Os bots orientados por LLM e de agente devem ser capazes de acessar as páginas do produto. |
| [!DNL Adobe Admin Console] acesso | Enriquecimento do catálogo | Obrigatório. Durante a configuração, o [!DNL Adobe Commerce] verifica se sua organização assinou o GenAI Rider ou se recusou a usar os serviços de IA subjacentes. |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
TBD (SME): Confirm whether the Admin Console and GenAI rider check also applies to PDP enrichment.
-->

## Configurar a plataforma do Commerce {#set-up}

>[!BEGINTABS]

>[!TAB Commerce na infraestrutura na nuvem ou no local]

Para [!DNL Adobe Commerce] na infraestrutura em nuvem ou no local, instale a extensão de enriquecimento compartilhado, que habilita o enriquecimento do Catálogo e o enriquecimento de PDP.

**Antes de começar:**

- [!DNL Adobe Commerce] 2.4.7 ou posterior no PHP 8.3 ou posterior. Consulte as [notas de versão](release-notes.md).
- Uma organização [!DNL Adobe IMS]. Se sua organização não tiver uma, consulte a [visão geral da integração do Adobe IMS](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview). O enriquecimento do catálogo usa o token de acesso IMS do usuário administrador conectado. Fazer logon com apenas um nome de usuário e senha do Commerce não fornece esse token.
- Acesso via linha de comando ao servidor de aplicativos do Commerce e permissão para baixar pacotes de `repo.magento.com`.

**Instalar e verificar:**

1. Se nem [!DNL Live Search] nem [!DNL Product Recommendations] estiver habilitado, adicione [!DNL Catalog Service] do diretório do projeto do Commerce:

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   O [!DNL Catalog Service] é instalado automaticamente com o [!DNL Live Search] e o [!DNL Product Recommendations]. Ignore esta etapa se algum dos serviços estiver habilitado.

1. Se ainda não estiver configurado para outro serviço Commerce, configure o [Commerce Services Connector](https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/integration-services/saas) com chaves de API e um Espaço de Dados SaaS.

1. Adicionar a extensão de enriquecimento compartilhada:

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Implante as alterações:

   - **Infraestrutura na nuvem:** confirme e envie as alterações para `composer.json` e `composer.lock`.
   - **Local:** atualize o aplicativo e limpe o cache:

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. No Administrador, vá para **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]** e confirme se o Commerce exporta dados de catálogo.

   O número de registros de produtos enviados com êxito deve corresponder aos registros de origem, sem falha ou aguardando envio. Para registros com falha, analise os detalhes do erro, resolva o problema e agende uma ressincronização para os registros afetados.

1. Vá para **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]** e confirme se os dados de catálogo esperados estão disponíveis em [!DNL Catalog Service].

Para obter detalhes sobre o status e solucionar problemas, consulte [Monitorar o status do feed de dados](/help/systems/data-feed-sync-status.md#monitor-data-feed-status).

>[!TAB Adobe Commerce as a Cloud Service]

Para [!DNL Adobe Commerce as a Cloud Service], a instalação do [!DNL Catalog Service], o enriquecimento do catálogo e o enriquecimento de PDP são manipulados para você durante o provisionamento da conta.

Conclua os [requisitos para todas as implantações](#all-deployments) que se aplicam aos fluxos de trabalho que você planeja usar.

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## Próxima etapa {#next-step}

[Defina as configurações de enriquecimento](settings.md) para conectar sua instância do Commerce à Descoberta de Produto de IA.
