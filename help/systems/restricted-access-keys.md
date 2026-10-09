---
title: Gerenciar chaves de acesso restrito no Commerce
description: Crie, atribua e exclua as chaves de acesso restrito que protegem exibições de catálogo compartilhado B2B sincronizadas com o Adobe Commerce Optimizer.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
last-update: 2026-10-01
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: 601e4abe-d9bf-58de-a779-32ed6794dcbe
    internal-label: Data Import/Export
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%
---

# Gerenciar chaves de acesso restrito

Use a página Chaves de Acesso Restrito para gerenciar chaves de acesso para exibições de catálogo privado criadas pelo [!DNL Adobe Commerce Optimizer Connector for B2B]. O conector sincroniza as configurações do catálogo compartilhado B2B do Adobe Commerce para o Adobe Commerce Optimizer.

>[!NOTE]
>
>Para chaves criadas manualmente usadas para gerenciar catálogos privados em cenários não B2B, como portais de parceiros, gerencie chaves de [[!DNL Adobe Commerce Optimizer Studio]](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"}.

## Público e disponibilidade {#audience}

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente ao Adobe Commerce na infraestrutura em nuvem e a projetos locais."}

A página [!UICONTROL Restricted Access Keys] está disponível para o Adobe Commerce na Infraestrutura em Nuvem e comerciantes locais que usam catálogos compartilhados B2B com o [!DNL Adobe Commerce Optimizer Connector for B2B]. O conector instala e ativa a página automaticamente.

Quando uma visualização de catálogo é criada pela primeira vez para um catálogo compartilhado, o conector gera e atribui automaticamente uma chave. Use esta página para exibir essa chave e para criar, atribuir ou excluir chaves adicionais.

## Acessar a página Chaves de Acesso Restrito {#access-restricted-access-keys-page}

Na área Administrador, navegue até **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**.

![Chaves de acesso restrito listando chaves e suas exibições de catálogo atribuídas](assets/restricted-access-keys.png){width="600" zoomable="yes"}

Esta página lista todas as chaves independentemente de estarem atribuídas a uma exibição de catálogo. Para atribuir uma chave a uma exibição de catálogo específica, use a ação [!UICONTROL Edit Restricted Access Keys] nessa exibição de catálogo. Consulte [Atribuir chaves a uma exibição de catálogo](#assign-keys-to-a-catalog-view).

## Resumo das Chaves de Acesso Restrito {#restricted-access-keys-summary}

A grade contém uma chave por linha.

| Campo | Descrição |
| --- | --- |
| **ID da Chave** | O identificador de chave exclusivo. |
| **Título** | Um rótulo fornecido para identificar a chave. |
| **Exibições de Catálogo Atribuídas** | As exibições de catálogo às quais esta chave está atribuída. |
| **Expira Em** | A data de expiração da chave. |
| **Ações** | Ações no nível da linha. Consulte [Gerenciar chaves](#manage-keys). |

## Gerenciar chaves {#manage-keys}

- **[!UICONTROL Create Key]** — Gera um novo par de chaves não atribuído. O Commerce gera o par de chaves e armazena a chave privada. A chave pública não é registrada com [!DNL Adobe Commerce Optimizer] até que você atribua a chave a uma exibição de catálogo.
- **[!UICONTROL View Public Key]** — Abre uma exibição somente leitura da chave pública da chave, para que você possa copiá-la para registrar novamente ou sincronizar novamente a chave, se necessário. A chave privada nunca é exibida.
- **[!UICONTROL Delete]**—Remove a chave e revoga seu registro remoto em [!DNL Adobe Commerce Optimizer]. Os tokens de vitrine já emitidos com esta chave permanecem válidos até que expirem. Essa ação não pode ser desfeita.

>[!NOTE]
>
>Uma chave expirada só pode ser excluída. Não é possível atribuir ou cancelar a atribuição de uma chave expirada.

## Criar uma chave

Na página [!UICONTROL Restricted Access Keys], crie uma chave selecionando **[!UICONTROL Create Key]**.

O Commerce gera um novo par de chaves e armazena a chave privada. A tabela Chaves de acesso restrito é atualizada com uma nova entrada de chave que mostra a ID de chave exclusiva. Use este [!UICONTROL Key ID] quando atribuir a chave a uma exibição de catálogo.

A chave pública não é registrada com [!DNL Adobe Commerce Optimizer] até que você atribua a chave a uma exibição de catálogo. Após o registro, a entrada da tabela Chaves de acesso restrito é atualizada para mostrar a atribuição do catálogo e a data de expiração.

## Atribuir ou remover chaves de acesso restrito {#assign-keys-to-a-catalog-view}

{{$include /help/_includes/edit-restricted-access-keys.md}}

## Seleção e rotação de chaves {#key-selection-and-rotation}

Quando mais de uma chave é atribuída a uma exibição de catálogo, o [!DNL Adobe Commerce] usa automaticamente a chave atribuída não expirada com a data de expiração mais recente para assinar tokens.

>[!IMPORTANT]
>
>A rotação de chaves automática ainda não está disponível. As chaves assumem como padrão um longo período de expiração. Para girar uma chave manualmente, crie uma nova chave e atribua-a à exibição de catálogo junto com a existente. Depois de confirmar que a nova chave está sendo usada, exclua a chave antiga.

Para alterar o período de expiração padrão aplicado às chaves recém-criadas, vá para **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Restricted Access Keys]** > **[!UICONTROL Provisioning]** > **[!UICONTROL Default key lifetime (days)]**. Consulte [Serviços > Chaves de acesso restrito ACO](../configuration-reference/services/aco-restricted-access-keys.md).

## Limitações conhecidas {#known-limitations}

- Não há indicador de status ou ativo na grade [!UICONTROL Restricted Access Keys] principal.

  Você pode ver o status do link na página [!UICONTROL Edit Restricted Access Keys]. Use a lista suspensa para exibir as chaves disponíveis e seus status. Se uma chave for atribuída a uma exibição de catálogo, ela será vinculada. Se não for atribuído, não terá status. Você pode atribuir essas chaves à exibição de catálogo que está editando.

  Na página [!UICONTROL Catalog View Sync Status], você pode ver chaves vinculadas a uma exibição de catálogo a partir da página de detalhes da exibição de catálogo (ação **[!UICONTROL View details]**). A página de detalhes também mostra o histórico principal, incluindo quando ele foi atribuído ou desatribuído de uma exibição de catálogo.

- A rotação de chaves automática ainda não está disponível.

>[!MORELIKETHIS]
>
> - [Gerenciar configuração de exibição de catálogo](/help/b2b/catalog-views-manage.md) — Atribua essas chaves do catálogo compartilhado ou da conta da empresa
> - [Monitoramento do Status de Sincronização da Exibição de Catálogo](catalog-view-sync-status.md) — Monitore e reconcilie as exibições de catálogo protegidas por essas chaves
> - [Serviços > Chaves de acesso restrito ACO](../configuration-reference/services/aco-restricted-access-keys.md) — Configurar o período de expiração de chave padrão
> - [Serviços > Exibição do Catálogo ACO](../configuration-reference/services/aco-catalog-view.md) — Configure o tempo de vida do token de acesso de vitrine e habilite ou desabilite a emissão
> - [Gerenciar chaves de acesso restrito](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"} no *Guia do Conector do Adobe Commerce Optimizer* — Saiba como essas chaves se encaixam na sincronização do catálogo compartilhado B2B
> - [Chaves de acesso restrito](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} no *Guia do Adobe Commerce Optimizer* — o fluxo de chaves manual baseado no ACO Studio para casos de uso não B2B
