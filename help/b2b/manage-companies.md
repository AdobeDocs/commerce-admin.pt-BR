---
title: Gerenciamento da Empresa
description: Simplifique a administração e o gerenciamento de organizações B2B com modelos operacionais complexos.
feature: B2B, Companies, Storefront
role: Admin
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
TQID: https://experienceleague.adobe.com/po8afDr-Q2XR9pkbzJDdX-9tDvf6FsLVHnP-YzGYrDI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 778
ht-degree: 0%

---

# Gerenciamento da empresa

O gerenciamento de empresas no Adobe Commerce fornece ferramentas abrangentes para administradores organizarem, configurarem e supervisionarem relações comerciais B2B. Esse recurso é essencial para empresas que trabalham com vários clientes corporativos, subsidiárias ou estruturas organizacionais complexas.

O gerenciamento da empresa permite que você:

* **Organizar Relações Comerciais**—Crie e gerencie contas individuais da empresa para seus clientes B2B
* **Criar Hierarquias Organizacionais** — Estrutura de relações pai-filho que espelham organizações comerciais reais
* **Centralizar Administração** — Gerencie várias empresas e suas configurações a partir de uma única interface administrativa
* **Simplifique as operações**—Aplique configurações e políticas consistentes entre empresas relacionadas
* **Suporte a Estruturas Complexas** — Gerencie subsidiárias, franquias, negócios de vários locais e divisões corporativas

Os usuários administradores podem criar uma hierarquia de empresa para refletir uma organização B2B, atribuindo empresas a uma empresa principal designada. Essa atribuição permite que o administrador da empresa principal exiba e gerencie empresas na organização.

Inicie as tarefas de gerenciamento da empresa na exibição *[!UICONTROL Companies]*. No Administrador, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Grade Gerenciar Empresas B2B](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Pré-requisitos

Antes de gerenciar empresas, verifique se:

* Os recursos B2B são ativados na instalação do Adobe Commerce
* Você tem acesso administrativo com permissões de gerenciamento da empresa
* As contas da empresa estão configuradas corretamente com as informações de negócios necessárias
* As funções e permissões do usuário são definidas para administradores e usuários da empresa

## Casos de uso

O gerenciamento da empresa é ideal para:

* **Empresas com vários locais** com compras centralizadas, mas com necessidades específicas de cada local
* **Operações de franquia** que exigem supervisão corporativa e autonomia local
* **Subsidiárias corporativas** com políticas compartilhadas, mas operações independentes
* **Grandes empresas** com várias divisões ou unidades de negócios
* **Redes de distribuição** com revendedores, revendedores ou parceiros de canal

## Noções Básicas sobre a Hierarquia da Empresa e os Tipos de Empresa

A hierarquia da empresa estrutura os relacionamentos comerciais organizando várias empresas em uma única empresa principal. Esse recurso reflete as estruturas organizacionais reais, permitindo o gerenciamento centralizado e preservando as identidades individuais da empresa.

### Tipos de empresa

A coluna *[!UICONTROL Company Type]* na grade Empresas mostra como cada empresa se encaixa na sua organização B2B:

* **Pai** — hub central com uma ou mais empresas atribuídas
   * Controla várias empresas filhas, mas não pode ser atribuído a outro pai
   * **Caso de uso**—Matriz corporativa, principal organização de franquias ou empresa controladora

* **Filho** — Empresa atribuída a uma organização pai
   * Opera sob governança principal e pode herdar configurações
   * Só pode pertencer a um pai por vez
   * **Caso de uso**—Escritórios subsidiários, franquias ou divisões regionais

* **Empresa**—Empresa individual independente
   * Opera independentemente sem relações de hierarquia
   * Pode converter em pai (atribuindo empresas) ou filho (atribuindo ao pai)
   * **Caso de uso** — clientes empresariais individuais ou clientes independentes

### Conversão de tipos de empresas

* **Única Empresa → Pai** — Atribua outras empresas a ela
* **Única Empresa → Filho**—Atribua-o a uma empresa pai existente
* **Filho → Único** — Cancela a atribuição da empresa filho de seu pai
* **Pai → Filho** — Não é possível sem primeiro remover todas as empresas atribuídas

### Gerenciar hierarquias da empresa

Ao editar empresas em uma hierarquia, expanda *[!UICONTROL Company Hierarchy]* para exibir todas as empresas relacionadas. Um sinalizador `Current` indica a empresa que está sendo editada.

![Grade de Hierarquia da Empresa B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

Para obter instruções detalhadas, consulte [Gerenciar a Hierarquia da Empresa](manage-company-hierarchy.md).

## Tarefas de gerenciamento da empresa

Ao gerenciar empresas na grade da empresa, os administradores podem executar as seguintes tarefas na grade *[!UICONTROL Company Hierarchy]*:

* **Exibir e gerenciar relações de empresa**
   * **Exibir Empresas Associadas** — Veja todas as empresas vinculadas a uma organização principal em uma exibição centralizada
   * **Monitorar Status da Empresa** — Rastreie empresas ativas, pendentes e inativas na hierarquia
   * **Acessar Detalhes da Empresa**—Navegue diretamente para páginas de configuração da empresa individual

* **Criar e modificar hierarquias**
   * **Atribuir empresas** — Adicione empresas existentes a uma organização principal na página de detalhes da empresa
   * **Criar relações pai-filho** — Estruturar empresas para refletir relações comerciais reais
   * **Reorganizar estruturas**—Mova empresas entre diferentes organizações pai à medida que as necessidades comerciais mudam

* **Gerenciamento de configuração em massa**
   * **Aplicar configurações entre empresas**—Atualizar configurações avançadas para várias empresas simultaneamente usando o controle [!UICONTROL Actions] na grade Empresa
   * **Padronizar configurações**—Garanta políticas consistentes entre organizações relacionadas
   * **Substituir configurações individuais** — Envia as configurações da empresa pai para as empresas filho selecionadas

* **Ações administrativas**
   * **Remover relações de empresa**—Use a ação *[!UICONTROL Unassign from parent]* para dissolver as relações organizacionais
   * **Gerenciar acesso à empresa** — Controla quais administradores podem exibir e modificar relacionamentos entre empresas
   * **Monitorar alterações de hierarquia** — Rastrear modificações nas estruturas organizacionais

## Práticas recomendadas

Ao gerenciar empresas, considere as seguintes práticas recomendadas:

* **Construindo hierarquias de empresa**—Ao gerenciar estruturas complexas de empresa, planeje sua hierarquia para corresponder a relações de negócios reais, mantendo estruturas simples para evitar confusão do usuário. Documente todos os relacionamentos entre empresas e suas conexões comerciais para referência futura.

* **Gerenciamento de configuração**—Teste as alterações de configuração em empresas individuais antes de aplicá-las a hierarquias inteiras e sempre documente as configurações atuais antes de fazer alterações em massa. Comunicar antecipadamente as alterações planejadas aos administradores da empresa afetados.

* **Segurança** — Limite as permissões de gerenciamento da empresa somente a administradores confiáveis, faça revisões regulares das relações da empresa e das permissões de acesso e monitore todas as alterações de hierarquia para fins de auditoria.

>[!MORELIKETHIS]
>
>* [Criar uma conta de empresa](account-company-create.md)
>* [Gerenciar hierarquias da empresa](manage-company-hierarchy.md)
>* [Funções e permissões da empresa](account-company-roles-permissions.md)
>* [Gerenciamento de crédito da empresa](credit-company.md)
>* [Habilitar recursos B2B](enable-basic-features.md)
