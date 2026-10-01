---
title: Gerenciar configuração de exibição do catálogo
description: Saiba como revisar as exibições de catálogo do Adobe Commerce Optimizer criadas para catálogos compartilhados B2B e atribuir as chaves de acesso restrito que os protegem.
feature: B2B, Companies, Catalog Management
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: f9f21f675d5c608547db790f33d1aa9be90a36eb
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%
---
# Gerenciar configuração de exibição de catálogo

Com a extensão [!DNL Adobe Commerce Optimizer Connector for B2B] instalada, a página Exibições de Catálogo lista as [!DNL Adobe Commerce Optimizer] [projeções de exibição de catálogo](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"} criadas para o catálogo compartilhado personalizado.  Uma _projeção_ é a exibição de catálogo criada quando o conector sincroniza os dados de catálogo compartilhado com [!DNL Adobe Commerce Optimizer]. O conector cria uma projeção separada para cada exibição de loja no catálogo compartilhado, de modo que um catálogo compartilhado pode ter várias exibições de catálogo. Nas experiências da loja, essas exibições de catálogo são acessíveis somente para empresas atribuídas ao catálogo compartilhado associado.

Por exemplo, suponha que a Acme Industrial esteja atribuída a um catálogo compartilhado, EU Business, que pertence ao site da UE. Esse site tem duas visualizações de loja:

- `English (UK)`

- `German (Germany)`

O conector projeta o catálogo compartilhado em duas [!DNL Adobe Commerce Optimizer] exibições de catálogo:

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

A empresa tem exibições de catálogo em inglês e alemão, mas apenas uma atribuição de catálogo compartilhado. Cada exibição de armazenamento exibe dados de sua exibição de catálogo correspondente.

Ambas as exibições de catálogo podem compartilhar o mesmo catálogo de preços quando usam o mesmo site e escopo de precificação de grupo de clientes.

## Autenticação de visualização de catálogo

O conector protege as exibições de catálogo com chaves de acesso restritas. A Adobe Commerce usa a chave privada para assinar um token de acesso para um comprador autorizado. Antes de retornar os dados do catálogo protegido, [!DNL Adobe Commerce Optimizer] valida o token com a chave pública correspondente associada à exibição do catálogo solicitada.

Para configurar a duração do token ou desabilitar a emissão de token, consulte [Serviços > Exibição do Catálogo ACO](/help/configuration-reference/services/aco-catalog-view.md).

Você pode revisar essas exibições de catálogo e gerenciar suas chaves atribuídas a partir da guia _[!UICONTROL Catalog Views]_&#x200B;do catálogo compartilhado ou da seção&#x200B;_[!UICONTROL Catalog Views]_ da empresa associada - ambas listam as mesmas exibições de catálogo e atribuições de chave atuais. Consulte [Editar chaves de acesso restrito](#edit-restricted-access-keys) para obter o caminho de navegação exato de cada local.

Para monitorar a sincronização de dados do catálogo compartilhado com [!DNL Adobe Commerce Optimizer], consulte [Monitoramento do status de sincronização da exibição do catálogo](/help/systems/catalog-view-sync-status.md).

## Referência de exibições de catálogo

{{$include /help/_includes/catalog-views-reference-table.md}}

## Editar chaves de acesso restrito

{{$include /help/_includes/edit-restricted-access-keys.md}}

Para obter detalhes adicionais, consulte [Gerenciar chaves de acesso restrito](/help/systems/restricted-access-keys.md).

>[!MORELIKETHIS]
>
> - [Projeção de catálogo compartilhado B2B](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}
> - [Serviços > Exibição do catálogo de ACO](/help/configuration-reference/services/aco-catalog-view.md)
> - [Monitoramento do Status de Sincronização da Exibição de Catálogo](/help/systems/catalog-view-sync-status.md)
> - [Gerenciar seus catálogos compartilhados](catalog-shared-manage.md)
> - [Gerenciar contas da empresa](account-company-manage.md)
