---
title: Operações
description: Diretrizes para migrar para uma oferta pronta para HIPAA e usar o ambiente de preparo secundário para solução de problemas.
source-git-commit: 999d3126ae368000fc2c58c315473739012f3934
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# Operações

Use estas diretrizes para saber mais sobre como migrar para a oferta pronta para HIPAA do Adobe Commerce e usar o ambiente `staging_for_support` para solução de problemas.

## Migração

Os clientes que migrarem de uma oferta Commerce que não seja HIPAA para uma oferta pronta para HIPAA devem seguir as seguintes diretrizes:

1. **Excluir dataspaces existentes**: antes da migração, todos os dataspaces existentes devem ser excluídos para impedir a combinação de dados confidenciais e não confidenciais na camada SaaS do Adobe Commerce. Crie um tíquete de suporte para excluir seus espaços de dados.
1. **Configurar novo ambiente**: a configuração do [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas) na nova instância do Commerce HIPAA só deve ser configurada após a exclusão dos dataspaces. O novo ambiente SaaS HIPAA só deve ser usado após a exclusão dos espaços de dados antigos. A configuração do Commerce Services Connector aciona automaticamente a criação de novos espaços de dados SaaS.
1. **Estratégia de migração**: a exclusão dos espaços de dados SaaS é um processo irreversível e exclui todos os seus dados de catálogo e configurações relacionadas. Uma estratégia de migração deve estar em vigor se você quiser levar adiante qualquer um dos dados ou configurações antigos. Essa estratégia é de responsabilidade do comerciante. Um tíquete de suporte para excluir os espaços de dados existentes deve ser criado somente após a realização do backup de dados de migração (se aplicável).

>[!NOTE]
>Para excluir espaços de dados existentes, os clientes devem criar um tíquete de Suporte da Adobe Commerce intitulado &quot;Migração HIPAA: excluir espaços de dados SaaS&quot;, fornecer seu `MAGEID` e fornecer as IDs do projeto SaaS que precisam ser excluídas.

## Solução de problemas com o suporte da Adobe Commerce

A oferta pronta para HIPAA da Adobe Commerce vem com um ambiente `staging_for_support` adicional para ser usado pela equipe de suporte da Adobe Commerce para fins de solução de problemas.

Os clientes devem garantir que o ambiente `staging_for_support`:

- Não contém dados confidenciais, como, mas não se limitando a, informações de saúde protegidas (PHI).
- Não deve ser usado para atividades de produção.
- Não deve receber um nome diferente de `staging_for_support` para evitar confusão.
- É mantido atualizado com o código e a configuração do ambiente de produção para garantir que a solução de problemas seja executada em um ambiente o mais próximo possível da produção.

## Serviços da Commerce

- **Serviços Commerce não prontos para HIPAA** — os clientes não devem usar serviços Adobe Commerce, como Live Search, Product Recommendations, Payment Services, Sales Channel ou Commerce Intelligence, porque eles não estão prontos para HIPAA. Os clientes só devem usar os [serviços prontos para HIPAA](overview.md).

- **Conexão de Dados** — Somente o Coletor de Back-Office na [Conexão de Dados](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) está pronto para HIPAA. Os clientes não devem enviar PHI para serviços de conexão de dados prontos que não sejam da HIPAA, como eventos de vitrine e Audience Activation. Os clientes devem garantir que a coleta de dados da loja esteja desativada.

- **Serviço de Catálogo** — por design, o [Serviço de Catálogo](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/overview) não processa PHI, portanto, está fora do escopo para a auditoria de preparação e conformidade HIPAA. Os clientes são responsáveis por garantir que usem esse serviço com base em sua própria avaliação de casos de uso e em consulta com o departamento jurídico. Os clientes também não devem usar o Serviço de catálogo por meio do serviço federado para evitar o risco de transmitir PHI para serviços prontos que não sejam da HIPAA.

- **Exportação de dados SaaS**—O serviço [Exportação de dados SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) deve ser configurado para enviar dados somente para componentes prontos para HIPAA na Adobe Commerce.
