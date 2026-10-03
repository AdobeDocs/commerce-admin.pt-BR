---
title: Monitoramento do Status de Sincronização da Exibição de Catálogo
description: Monitore a integridade da projeção do catálogo compartilhado B2B e reconcilie exibições de catálogo, políticas, catálogos de preços e chaves de acesso para o Conector do Adobe Commerce Optimizer.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
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
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 0%
---

# Monitoramento do status de sincronização da exibição de catálogo

Use a página Status da Sincronização da View de Catálogo para monitorar a sincronização e solucionar problemas de views de catálogo projetadas no Adobe Commerce Optimizer. Para cada catálogo compartilhado personalizado, o [!DNL Adobe Commerce Optimizer Connector for B2B] cria uma exibição de catálogo para cada exibição de loja no escopo do site do catálogo compartilhado. Cada exibição de catálogo é configurada com uma política de classificação, seu catálogo de preços vinculado e a chave pública usada para validar tokens de acesso restrito. O Adobe Commerce retém os metadados de exibição de catálogo correspondentes, incluindo a chave privada e a ID de catálogo de preços padrão.

>[!NOTE]
>
>Para acompanhar o status de sincronização dos feeds de dados de catálogo, use a página [[!UICONTROL Data Feed Sync Status]](data-feed-sync-status.md).

## Público e disponibilidade {#audience}

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente ao Adobe Commerce na infraestrutura em nuvem e a projetos locais."}

A página [!UICONTROL Catalog View Sync Status] está disponível para o Adobe Commerce na Infraestrutura em Nuvem e comerciantes locais que usam catálogos compartilhados B2B com a integração [!DNL Adobe Commerce Optimizer Connector for B2B]. A página é instalada e ativada automaticamente quando a extensão do conector é instalada.

## Acessar a página Exibir Status da Sincronização do Catálogo {#access-catalog-view-sync-status-page}

Na área Administrador, navegue até **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Catalog View Sync Status]**.

![Página Status da Sincronização da Exibição de Catálogo listando exibições de catálogo com sua integridade de sincronização](assets/catalog-view-sync-status.png){width="600" zoomable="yes"}

A página tem três guias:

- **[!UICONTROL Catalog Views]** — Exibições de catálogo criadas pelo conector, com integridade de sincronização para cada um. Consulte [Resumo do Status de Sincronização da Exibição de Catálogo](#catalog-view-sync-status-summary).
- **[!UICONTROL Orphaned in ACO]** — Entidades que existem em [!DNL Adobe Commerce Optimizer] sem nenhuma origem [!DNL Adobe Commerce] correspondente. Consulte [Órfão na guia ACO](#orphaned-in-aco-tab).
- **[!UICONTROL Deleted]** — Um registro de projeções de exibição de catálogo foi removido porque seu catálogo compartilhado foi excluído. Consulte [Guia Excluída](#deleted-tab).

## Resumo do Status de Sincronização da Exibição de Catálogo {#catalog-view-sync-status-summary}

Os cartões de resumo na parte superior da página mostram o número de exibições de catálogo em cada estado de integridade, além de uma contagem de chaves de acesso restritas que expiram em 30 dias:

| Cartão | Descrição |
| --- | --- |
| **Íntegro** | Exibições de catálogo sem desvio detectado. |
| **Degradado** | Visualizações do catálogo com descompasso reparável. |
| **Falha** | Exibições de catálogo que nunca foram criadas ou que foram excluídas diretamente em [!DNL Adobe Commerce Optimizer]. |
| **Chaves ≤ 30D** | Chaves de acesso restrito expirando em 30 dias. |

A grade lista uma linha por exibição de catálogo:

| Campo | Descrição |
| --- | --- |
| **Exibição de catálogo** | O identificador da exibição de catálogo projetada para [!DNL Adobe Commerce Optimizer]. |
| **Source** | O catálogo compartilhado do qual a exibição do catálogo foi projetada. Selecione o link para abrir o catálogo compartilhado em Admin. |
| **Exibir Repositório** | A exibição de loja que a exibição de catálogo representa. |
| **Empresas** | O número de empresas atualmente vinculadas a esta exibição de catálogo. |
| **Status** | A integridade geral da sincronização da exibição do catálogo. Consulte [Valores de status de sincronização](#sync-status-values). |
| **Política** | Se a política de classificação atribuída a esta exibição de catálogo corresponde à sua configuração do [!DNL Adobe Commerce]. |
| **Catálogo de Preços** | Se o catálogo de preços atribuído a esta exibição de catálogo corresponde à sua configuração do [!DNL Adobe Commerce]. |
| **Chave de Acesso** | Se uma chave de acesso restrito está vinculada a esta exibição de catálogo. |
| **Chave Expira** | A data de expiração da chave de acesso restrito da visualização do catálogo e o número de dias restantes. |
| **Deriva** | O tipo de desvio detectado, se houver. |
| **Última reconciliação** | Quando o processo de reconciliação verificou esta exibição de catálogo pela última vez. |
| **Ação** | **[!UICONTROL View details]** abre a página de detalhes Exibir Status de Sincronização da Exibição de Catálogo para exibir o status atual, a deriva, as chaves de acesso e os eventos recentes. **[!UICONTROL Open in ACO admin]** abre a página de detalhes de exibição do catálogo no [!DNL Adobe Commerce Optimizer] Studio. **[!UICONTROL Copy ID]** copia a ID de exibição do catálogo para referência. Consulte [Reconciliar e corrigir problemas](#reconcile-and-repair-drift). |

## Sincronizar valores de status {#sync-status-values}

| Status | Significado |
| --- | --- |
| **Íntegro** | Nenhum desvio detectado. A exibição do catálogo, a política, o catálogo de preços e as chaves correspondem à configuração do [!DNL Adobe Commerce]. |
| **Degradado** | O desvio foi detectado e pode ser reparado — por exemplo, uma política ou catálogo de preços foi alterado diretamente em [!DNL Adobe Commerce Optimizer]. |
| **Falha** | A exibição do catálogo nunca foi criada ou foi excluída diretamente em [!DNL Adobe Commerce Optimizer]. |
| **Pendente** | A exibição do catálogo ainda não foi reconciliada ou está aguardando sua primeira projeção. |
| **Retirando** | O catálogo compartilhado foi excluído em [!DNL Adobe Commerce], e a exibição do catálogo está dentro de seu período de carência de exclusão. |
| **Excluído** | A projeção de exibição do catálogo foi removida após seu período de carência. Ele será mantido como um registro na guia [!UICONTROL Deleted] por 90 dias. |
| **Órfão** | A exibição ou chave do catálogo existe em [!DNL Adobe Commerce Optimizer], mas não tem uma origem [!DNL Adobe Commerce] correspondente. Consulte [Órfão na guia ACO](#orphaned-in-aco-tab). |

### Configurar o período de carência de exclusão {#configure-the-deletion-grace-period}

O período de carência de exclusão especifica a janela de retenção de dados para exibições de catálogo e dados associados após a exclusão do catálogo compartilhado associado. O valor padrão é 7 dias.
Depois que a janela expira, todos os dados são removidos.

#### Alterar a configuração de retenção de dados

1. Abra o [!DNL Adobe Commerce] Administrador.

1. No menu **[!UICONTROL Stores]**, selecione **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Catalog View Sync]** > **[!UICONTROL Deletion]** > **[!UICONTROL Deletion Grace Period (days)]**.

1. Atualize o valor **[!UICONTROL Deletion Grace Period (days)]** conforme necessário.

   Para remover uma projeção ACO de exibição de catálogo imediatamente após excluir um catálogo compartilhado, defina esse valor como `0`.

1. Selecione **[!UICONTROL Save Config]**.

Para obter detalhes, consulte [Serviços > Sincronização de Exibição do Catálogo ACO](../configuration-reference/services/aco-catalog-view-sync.md) para todas as configurações disponíveis de sincronização e reconciliação de desvio.

## Reconciliar e reparar diferenças de configuração {#reconcile-and-repair-drift}

[!DNL Adobe Commerce] é a fonte autoritativa para a projeção do catálogo compartilhado B2B. A reconciliação compara a configuração do [!DNL Adobe Commerce] com o [!DNL Adobe Commerce Optimizer] e relata ou repara quaisquer diferenças.

>[!IMPORTANT]
>
>As alterações feitas diretamente em [!DNL Adobe Commerce Optimizer] em uma exibição de catálogo gerenciada por conector, política, catálogo de preços ou chave não são a principal fonte da verdade. A reconciliação os relata como diferenças de configuração e, ao reparar, os reverte para corresponder a [!DNL Adobe Commerce]. Faça alterações na configuração em [!DNL Adobe Commerce], não em [!DNL Adobe Commerce Optimizer]. O reparo não remove as políticas adicionadas manualmente junto com a política gerenciada por conector.

Use os botões de nível de página para reconciliar:

- **[!UICONTROL Reconcile]** — Verifica diferenças de configuração e atualiza o status de sincronização sem fazer alterações em [!DNL Adobe Commerce Optimizer].

- **[!UICONTROL Reconcile & Repair]** — Verifica as diferenças de configuração e restaura automaticamente a configuração esperada para quaisquer diferenças reparáveis.

  Selecionar **[!UICONTROL Reconcile & Repair]** envia uma solicitação de reconciliação assíncrona e retorna antes da execução do reparo. Uma mensagem de confirmação informa que o status é atualizado em breve, mas a página não é recarregada automaticamente. Aguarde a conclusão do processamento e atualize a grade para verificar o resultado.

Use o menu **[!UICONTROL Action]** em uma linha para:

- **[!UICONTROL View details]** — Abra a página Detalhes do Status de Sincronização de Exibição de Catálogo para exibir o status atual, a deriva, as chaves de acesso e os eventos recentes.
- **[!UICONTROL Open in ACO admin]** — Abra a página de detalhes da exibição do catálogo no [!DNL Adobe Commerce Optimizer] Studio.
- **[!UICONTROL Copy ID]** — Copie a ID de exibição do catálogo para referência.

## Órfão na guia ACO {#orphaned-in-aco-tab}

A guia **[!UICONTROL Orphaned in ACO]** lista exibições de catálogo e chaves de acesso restritas que existem em [!DNL Adobe Commerce Optimizer], mas não têm origem [!DNL Adobe Commerce] correspondente. Por exemplo, entidades criadas manualmente no [!DNL Adobe Commerce Optimizer] Studio em vez do conector. Essas entidades não podem aparecer na grade principal porque não há nenhum registro [!DNL Adobe Commerce] que corresponda a elas.

![Órfão na guia ACO listando entidades sem origem Adobe Commerce](assets/catalog-view-sync-orphan.png){width="600" zoomable="yes"}

| Campo | Descrição |
| --- | --- |
| **Tipo** | A categoria da entidade órfã: [!UICONTROL Catalog View] ou [!UICONTROL Access Key]. |
| **ID DO ACO** | O identificador da entidade em [!DNL Adobe Commerce Optimizer]. |
| **Detalhe** | Contexto adicional sobre a entidade, como sua política. |
| **Primeira visualização** | Quando a reconciliação detectou esta entidade pela primeira vez. |
| **Ação** | Selecione **[!UICONTROL Copy ID]** para copiar o identificador de entidade. Use a ID copiada para localizar e remover a entidade das exibições do catálogo do [!DNL Adobe Commerce Optimizer] Studio. |

>[!NOTE]
>
>Essa guia é somente para relatório. A reconciliação nunca exclui entidades órfãs. Remova-os diretamente no [!DNL Adobe Commerce Optimizer] Studio se eles não forem mais necessários.

## Guia Excluída {#deleted-tab}

A guia **[!UICONTROL Deleted]** lista projeções de exibição de catálogo que foram removidas porque seu catálogo compartilhado foi excluído em [!DNL Adobe Commerce]. Como o catálogo compartilhado e sua visualização de catálogo não existem mais, essas linhas não são vinculadas em nenhum lugar. Eles são mantidos apenas como um registro do que foi removido.

![Projeções de exibição de catálogo da listagem de guias excluídas removidas após a exclusão de seu catálogo compartilhado](assets/catalog-view-sync-deleted.png){width="600" zoomable="yes"}

| Campo | Descrição |
| --- | --- |
| **Exibição de catálogo** | O identificador da exibição de catálogo removida. |
| **Source** | O catálogo compartilhado que foi excluído. |
| **Exibir Repositório** | A exibição de loja representada pela exibição de catálogo. |
| **Excluído Às** | Quando a projeção foi removida. |

As linhas nesta guia são limpas automaticamente após 90 dias.

## Limitações conhecidas

- Não há um indicador visual no [!DNL Adobe Commerce Optimizer] Studio que diferencie as exibições de catálogo gerenciadas por conector das criadas manualmente. Use esta página, não a interface do usuário do Studio [!DNL Adobe Commerce Optimizer], para determinar o que o conector gerencia.
- A coluna **[!UICONTROL ACO ID]** da guia **[!UICONTROL Orphaned in ACO]** identifica uma exibição de catálogo, uma política ou uma chave de acesso, não um identificador exclusivo. A nomeação da coluna está sujeita a alterações.

>[!MORELIKETHIS]
>
> - [Gerenciar configuração de exibição de catálogo](/help/b2b/catalog-views-manage.md) — Revise as exibições de catálogo do catálogo compartilhado ou da conta da empresa
> - [Status de sincronização do feed de dados](data-feed-sync-status.md)
> - [Serviços > Sincronização de Exibição do Catálogo ACO](../configuration-reference/services/aco-catalog-view-sync.md) — Configure os períodos de cortesia de exclusão e criação e o reconciliador de descompasso
> - [Gerenciamento de Chaves de Acesso Restrito](restricted-access-keys.md) — Gerencie as chaves cuja expiração esta página supera
> - [Monitorar sincronização de exibição de catálogo para catálogos compartilhados B2B](https://experienceleague.adobe.com/pt-br/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/catalog-view-sync-status) no *Guia do Adobe Commerce Optimizer Connector*
> - [Exibições de catálogo privado](https://experienceleague.adobe.com/pt-br/docs/commerce/optimizer/setup/private-catalog-view)
> - [Chaves de acesso restrito](https://experienceleague.adobe.com/pt-br/docs/commerce/optimizer/setup/restricted-access-keys)
