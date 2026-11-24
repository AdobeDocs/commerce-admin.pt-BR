---
title: Enriquecimento da página de detalhes do produto
description: Use o Enriquecimento da Página de Detalhes do Produto [!DNL Adobe Commerce] para revisar a cópia do produto sugerida pela IA, criar trabalhos de enriquecimento e implantar atualizações aprovadas para descoberta de LLM e AI.
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%
---

# Enriquecimento da página de detalhes do produto

O enriquecimento da página de detalhes do produto (PDP) maximiza o rastreabilidade para LLMs em cada PDP com dados estruturados do produto sem fazer alterações na experiência visível humana. Esse recurso é lido no catálogo de produtos para criar uma carga de dados estruturada para cada PDP que possa ser facilmente lida e analisada pelos LLMs.

## Como funciona {#how-it-works}

Seu catálogo do Adobe Commerce contém informações do produto, como atributos, variantes, categorias, preços e disponibilidade. Em um trabalho de enriquecimento PDP, selecione as páginas de produto e os grupos de fatos de catálogo a serem disponibilizados aos agentes de IA. As informações são organizadas para agentes sem alterar a experiência da loja.

Com o enriquecimento de PDP é possível:

- Escolha produtos ativados específicos que tenham páginas de produto ativas.
- Revise um resumo das páginas e dos fatos selecionados antes de salvar ou executar o job.
- Visualize as informações do produto incluídas no enriquecimento.

| Direção | Finalidade |
| --- | --- |
| catálogo Commerce -> trabalho de enriquecimento | Selecione as páginas de produto ativas e os fatos do catálogo a serem incluídos. |
| Trabalho de enriquecimento -> Agentes de IA | Disponibilize as informações existentes e selecionadas do produto em um formulário estruturado. A vitrine visível humana não muda. |

## Acessar enriquecimento de PDP

Antes de começar, revise os [pré-requisitos de Descoberta de Produto de IA](prerequisites.md) específicos da implantação. Após concluir a configuração da sua plataforma Commerce, abra o **[!UICONTROL AI Product Discovery]** no Administrador e selecione **[!UICONTROL Product Details Page Enrichment]**.

## Dois caminhos de enriquecimentos PDP

Há dois caminhos para receber enriquecimentos de PDP:

- **Tráfego de agente** - Esse tipo de enriquecimento inicia automaticamente entre 24 e 48 horas após a configuração da instância do Commerce e exibe os resultados na guia **Otimizações**.
- **Gerenciador de Enriquecimento** - Esses enriquecimentos são configurados pelo comerciante quando clicam no botão **[!UICONTROL Create enrichment]** e selecionam manualmente as SKUs a serem enriquecidas. Saiba mais sobre o [gerenciador de enriquecimento](#create-an-enrichment-job).

## Revisar atividade de enriquecimento de PDP

A página de enriquecimento do PDP é aberta na guia **[!UICONTROL Optimizations]**. Use o painel para revisar a cobertura de enriquecimento, a atividade do job e os jobs que precisam de atenção. Use a guia **[!UICONTROL Settings]** para [vincular](settings.md) sua instância do Commerce à Descoberta de Produto de IA.

### Encontrar tarefas que precisam de atenção

A seção **[!UICONTROL Needs your attention]** destaca os trabalhos que exigem ação. Um cartão pode mostrar o nome do trabalho, como os produtos foram selecionados, o número de páginas do produto, o status do trabalho e o progresso. Use a ação disponível em um cartão para continuar o trabalho.

### Pesquisar todos os trabalhos

Use a tabela para pesquisar e rastrear jobs. Pesquisar por detalhes do trabalho ou filtrar por status, incluindo **[!UICONTROL Generating]**, **[!UICONTROL Ready to review]**, **[!UICONTROL Deployed]**, **[!UICONTROL Queued]** ou **[!UICONTROL Failed]**. A tabela lista a ID, o nome, a origem, a contagem de páginas de produtos, a data inicial, o status e as ações disponíveis de cada tarefa.

## Criar um trabalho de enriquecimento

Nesta seção, você aprenderá a criar um enriquecimento da página de detalhes do produto.

![Criar Enriquecimento de PDP](./assets/create-cat-enrich.png)

1. Em **[!UICONTROL Optimizations]**, clique em **[!UICONTROL Create enrichment]**.
1. Insira um **Nome do enriquecimento**, como &quot;Black Friday 2026&quot;.
1. Selecione a **Categoria**, como &quot;Café&quot;.
1. Selecione o **Conjunto de atributos**, como &quot;Acessórios&quot;.
1. Selecione o **Tipo de produto**, como &quot;Produto simples&quot;.
1. Selecione o **intervalo de preços**.
1. Clique em **[!UICONTROL Apply filters]**.

   Você pode visualizar os produtos que correspondem aos seus critérios de enriquecimento e clicar em **Personalizar** para definir ainda mais o escopo dos produtos que deseja enriquecer.

1. Clique em **[!DNL Next]** para confirmar os produtos específicos que deseja enriquecer.
1. Clique em **[!DNL Run enrichment]**.

   O trabalho de enriquecimento é executado e exibido na tabela **Otimizações**. Quando terminar a execução, você poderá [Revisar e Implantar](#review-and-deploy-an-enrichment-job) as otimizações.

### Revisar um trabalho de enriquecimento {#review-and-deploy-an-enrichment-job}

Abra um trabalho de enriquecimento.

![Lista de URLs de Enriquecimento de PDP](./assets/pdp-enrich-urls.png)

A tabela **URLs com sugestões** lista todos os produtos com oportunidades de enriquecimento. Para cada produto, você pode:

- **Expanda a linha** para exibir a Análise de IA e o enriquecimento proposto.
- **Edite** o nome ou a descrição do produto proposto antes de aplicar, para alinhar-se à voz da sua marca e às diretrizes de comercialização.
- **Implante a Otimização** para os produtos que deseja enriquecer e publique-a diretamente na sua loja da Adobe Commerce.
- **Marcar como Corrigido** depois que o enriquecimento tiver sido revisado e aplicado.
- **Ignore** sugestões que não são relevantes para sua estratégia de catálogo.

As sugestões são organizadas em três modos de exibição: **Sugestões Atuais**, **Sugestões Fixas** e **Sugestões Ignoradas**. Depois que um enriquecimento for aplicado, ele será movido para **Sugestões Fixas** com o status **Aplicado**. Os enriquecimentos aplicados podem ser revertidos a qualquer momento.

### Implantar a otimização

Depois de revisar as sugestões e selecionar as páginas de produto a serem otimizadas, clique em **Implantar otimizações** para publicar o enriquecimento usando Otimizar no Edge. Uma caixa de diálogo de confirmação **Implantar no Edge** mostra as URLs do produto selecionado, o tipo de otimização e o enriquecimento sendo aplicado. Após a implantação, uma tela de confirmação confirma quais páginas de produto foram otimizadas com êxito.

A otimização é entregue exclusivamente aos agentes de usuário de IA por meio da [Otimizar na Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). Visitantes humanos continuam a ver sua experiência de loja existente exatamente como antes, sem alterações no design PDP, desempenho da página ou experiência da marca.

## Limites e considerações {#limits}

- Somente produtos habilitados com uma página de produto em tempo real podem ser selecionados.
- O enriquecimento organiza fatos já presentes no catálogo; ele não adiciona novas informações do produto.
- O fluxo de trabalho de enriquecimento do PDP não altera a loja.
- Os trabalhos de enriquecimento de PDP e os trabalhos de Enriquecimento de Catálogo têm finalidades e fluxos de trabalho diferentes.
- A otimização PDP usa [Otimizar em Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn).

## Práticas recomendadas {#best-practices}

- Use nomes de trabalho claros que identifiquem o grupo de produtos ou a campanha.
- Pré-visualize os fatos incluídos no trabalho e confirme se são precisos e apropriados para os agentes de IA.
- Verifique se os produtos já foram enriquecidos antes de decidir ignorá-los ou substituí-los.
- Coordene a sincronização do catálogo e a propriedade de fatos do produto com as equipes responsáveis por esses registros.

## Exemplo: enriquecer um produto com variantes e especificações

Uma página de produto geralmente contém mais informações de catálogo do que os agentes de IA podem ler. Por exemplo, um comerciante vende uma bota de caminhada à prova d&#39;água. As opções de tamanho, largura e cor ficam em um seletor de variante carregado com o JavaScript. Materiais, impermeabilização e instruções de cuidados ficam na guia Detalhes recolhida e o guia de ajuste abre em um pop-up. Um comprador pode abrir tudo isso, mas um rastreador de IA que lê a página à medida que é carregada pela primeira vez pode ver apenas o nome do produto, o preço e uma breve descrição.

Quando o trabalho de enriquecimento é executado neste produto, ele coleta todos os dados do catálogo do produto, incluindo seus atributos e todas as variantes, e os compila em um formato estruturado que os agentes de IA podem ler. Um assistente de IA pode responder perguntas como &quot;Esta inicialização está disponível em um amplo ajuste no tamanho 11?&quot; ou &quot;É totalmente à prova d&#39;água?&quot; dos dados de catálogo do próprio comerciante.

O trabalho de enriquecimento usa apenas as informações que já existem no catálogo. Isso não cria novos fatos do produto e não altera a página do produto que os compradores veem.
