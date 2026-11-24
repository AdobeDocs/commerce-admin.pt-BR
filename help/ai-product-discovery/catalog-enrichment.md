---
title: Enriquecimento do catálogo
description: Use o Enriquecimento do catálogo do [!DNL Adobe Commerce] para revisar a cópia de produto sugerida pela IA, criar trabalhos de enriquecimento e implantar atualizações aprovadas para descoberta de LLM e AI.
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
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
source-git-commit: b2a1abb72839717a7249e9a34b13266b8e384189
workflow-type: tm+mt
source-wordcount: '1976'
ht-degree: 0%
---
# Enriquecimento do catálogo

O enriquecimento do catálogo é um recurso nativo do [!DNL Adobe Commerce] que ajuda a melhorar os nomes de produtos e as descrições longas, para que seu catálogo seja representado com mais precisão quando os compradores usarem LLMs e assistentes de IA para pesquisa e descoberta de produtos.

## Como funciona {#how-it-works}

O catálogo de produtos do [!DNL Adobe Commerce] é o sistema de registro de dados de produtos: nomes, descrições, atributos, preços e estoque. [!DNL Adobe Commerce] conecta dados do catálogo ao vivo a experiências do Adobe AI. A partir daí, o Catalog Agent pode identificar lacunas em nomes de produtos e descrições longas, propor melhorias e gravar alterações aprovadas no Commerce para que você possa analisá-las no Commerce Admin.

Com o enriquecimento do catálogo, você pode:

- Identifique lacunas e inconsistências nos nomes de produtos e descrições longas que afetam como os LLMs interpretam seus produtos.
- Revise as melhorias sugeridas com o contexto de suporte, incluindo justificações e comparações antes e depois.
- Aplique atualizações aprovadas diretamente ao catálogo do Commerce para que o Administrador, a loja e outros canais que leem esses campos permaneçam alinhados.

Como os nomes dos produtos e as descrições longas ficam no Commerce, a melhoria da cópia uma vez pode beneficiar cada canal que consome esses dados do produto. O benefício depende de como e quando seus sistemas são atualizados.

| Direção | Finalidade |
| --- | --- |
| Catálogo do Commerce -> análise | Os sinais de tráfego de catálogo e agente descobrem oportunidades de sugestões de enriquecimento. |
| Enriquecimento -> Catálogo do Commerce | Depois de aprovar uma atualização, as alterações no nome e na descrição do produto são salvas no catálogo do Commerce para que o administrador e a loja reflitam os valores otimizados. |

### Acessar enriquecimento do catálogo

Antes de começar, revise os [pré-requisitos de Descoberta de Produto de IA](prerequisites.md) específicos da implantação. Após concluir a configuração da sua plataforma Commerce, vá para **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** no Administrador.

![Painel de enriquecimento do catálogo](assets/catalog-enrich-dashboard.png){zoomable="yes"}

O espaço de trabalho de Enriquecimento de Catálogo inclui as guias **[!UICONTROL Optimizations]**, **[!UICONTROL Brand governance]** e **[!UICONTROL Settings]**.

- Use a guia **[!UICONTROL Optimizations]** para analisar sinais de descoberta baseados em tráfego de agente e gerenciar trabalhos de enriquecimento.
- Use a guia **[!UICONTROL Brand Governance]** para [definir requisitos](brand-governance.md) para nomes e descrições de produtos gerados por [!DNL Commerce Catalog Agent].
- Use a guia **[!UICONTROL Settings]** para [conectar sua instância do Commerce](settings.md) à Descoberta de Produto de IA.

A extensão compartilhada também permite o enriquecimento da PDP, que tem um fluxo de trabalho separado para expor fatos de produtos estruturados aos agentes de IA. Consulte [enriquecimento da página de detalhes do produto](pdp-enrichment.md).

## Dois caminhos de enriquecimentos de catálogo

Há dois caminhos para receber enriquecimentos de catálogo:

- **Tráfego de agente** - Esse tipo de enriquecimento inicia automaticamente entre 24 e 48 horas após a configuração da instância do Commerce e exibe os resultados na guia **Otimizações**.
- **Gerenciador de enriquecimento** - Os comerciantes configuram esses enriquecimentos quando clicam no botão **[!UICONTROL Create enrichment]** e selecionam manualmente as SKUs a serem enriquecidas. Saiba mais sobre o [gerenciador de enriquecimento](#create-an-enrichment-job).

### Revisar e aplicar enriquecimento do catálogo {#review-and-apply}

Depois que o enriquecimento do catálogo for habilitado e configurado, use a guia **[!UICONTROL Optimizations]** para revisar os insights de tráfego de pesquisa e agilidade e gerenciar trabalhos de enriquecimento.

### Revisar o tráfego agêntico mensal

Cada auditoria mensal de tráfego agencial identifica SKUs de alto tráfego e disponibiliza um lote recomendado. Otimizações para revisão são geradas automaticamente para as SKUs de tráfego agêntico alto. Essas otimizações são geradas automaticamente com base em sua regra de governança &quot;Padrão&quot;. Os cartões mensais mostram a contagem de produtos, as visitas dos agentes de IA e o status do trabalho. O tráfego de agente e os lotes autoselecionados usam o mesmo fluxo de trabalho de seleção, confirmação, execução, revisão e implantação de regra.

### Revisar tarefas que precisam de atenção

A seção **[!UICONTROL Needs your attention]** destaca os trabalhos que precisam de ação, incluindo os trabalhos concluídos prontos para revisão. Abra um trabalho concluído para revisar as alterações de produto propostas antes da implantação.

### Localizar trabalhos

A tabela **[!UICONTROL All jobs]** lista cada ID de trabalho, nome, origem, contagem de SKUs, regra usada, hora de início e status. As origens identificam se um lote foi selecionado automaticamente ou recomendado do tráfego agêntico. Rastrear status de processamento como **[!UICONTROL Queued]**, **[!UICONTROL Running]**, **[!UICONTROL Completed]** ou **[!UICONTROL Failed]**. No espaço de trabalho de Otimizações, esses trabalhos também podem aparecer como **[!UICONTROL Generating]** enquanto são executados, **[!UICONTROL Ready to review]** quando a geração está concluída e **[!UICONTROL Deployed]** após a implantação das alterações aprovadas. Você pode executar vários trabalhos simultaneamente. Tente novamente um trabalho com falha com **[!UICONTROL Retry]**.

### Criar um trabalho de enriquecimento

**Para criar um enriquecimento de catálogo:**

![Criar Enriquecimento de Catálogo](./assets/create-cat-enrich.png){zoomable="yes"}

1. Em **[!UICONTROL Optimizations]**, clique em **[!UICONTROL Create enrichment]**.
1. Insira um **Nome do enriquecimento**, como &quot;Black Friday 2026&quot;.
1. Selecione a **Categoria**, como &quot;Café&quot;.
1. Selecione o **Conjunto de atributos**, como &quot;Acessórios&quot;.
1. Selecione o **Tipo de produto**, como &quot;Produto simples&quot;.
1. Selecione o **intervalo de preços**.
1. Clique em **[!UICONTROL Apply filters]**.

   Você pode visualizar os produtos que correspondem aos seus critérios de enriquecimento e clicar em **Personalizar** para definir ainda mais o escopo dos produtos que deseja enriquecer.

1. Clique em **[!DNL Next]** e visualize a [regra de governança](brand-governance.md) que está sendo aplicada ao seu enriquecimento.
1. Clique em **[!DNL Next]** para confirmar os produtos específicos que deseja enriquecer.
1. Clique em **[!DNL Run enrichment]**.

   O job de enriquecimento é executado e exibido na tabela Otimizações. Quando terminar a execução, você poderá [Revisar e Implantar](#review-deploy-catalog) as otimizações.

### Revisar e implantar um trabalho de enriquecimento {#review-deploy-catalog}

Abra um trabalho de enriquecimento.

![Lista de URLs de Enriquecimento de Catálogo](./assets/catalog-enrich-urls.png){zoomable="yes"}

A tabela **URLs com sugestões** lista todos os produtos com oportunidades de enriquecimento. Para cada produto, você pode:

- **Expanda a linha** para exibir a Análise de IA e o enriquecimento proposto.
- **Edite** o nome ou a descrição do produto proposto antes de aplicar, para alinhar-se à voz da sua marca e às diretrizes de comercialização.
- **Implante a Otimização** para os produtos que deseja enriquecer e publique-a diretamente no catálogo do Adobe Commerce.
- **Marcar como Corrigido** depois que o enriquecimento tiver sido revisado e aplicado.
- **Ignore** sugestões que não são relevantes para sua estratégia de catálogo.

As sugestões são organizadas em três modos de exibição: **Sugestões Atuais**, **Sugestões Fixas** e **Sugestões Ignoradas**. Depois que um enriquecimento é aplicado, ele é movido para Sugestões Fixas com um status de **Aplicado** e uma ação **Exibir no Catálogo** para verificar a atualização no Adobe Commerce. Os enriquecimentos aplicados podem ser revertidos a qualquer momento, restaurando o nome e a descrição originais do produto.

## Verificar enriquecimento no Admin {#verify-in-admin}

**Para verificar o enriquecimento do catálogo aplicado:**

1. Vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]** no Administrador do Commerce.
1. Use filtros e o seletor **[!UICONTROL Store View]** conforme necessário (por exemplo, **[!UICONTROL Default Store View]**).
1. Procure o SKU.
1. Abra o produto no modo de edição.

   O formulário do produto mostra o nome e/ou a descrição do produto enriquecido.

   ![Nome de Produto Enriquecido](./assets/enriched-product-name.png){zoomable="yes"}

1. Opcional: selecione **[!UICONTROL Override Catalog Agent provided Product Name]** se quiser manter um nome inserido manualmente.

   As substituições manuais afetam como as sugestões permanecem sincronizadas com o catálogo. Para obter mais informações, consulte [Substituição manual no Admin](#manual-override-in-the-admin).

1. Expanda a seção **[!UICONTROL Content]** e localize o campo de descrição.

   A descrição enriquecida é exibida quando você aplica alterações de descrição.

   ![Enriquecer Descrição Do Produto](./assets/enrich-product-description.png){zoomable="yes"}

1. Opcional: selecione **[!UICONTROL Override Catalog Agent provided Description]** se quiser manter uma descrição inserida manualmente.

As substituições manuais afetam como as sugestões permanecem sincronizadas com o catálogo. Para obter mais informações, consulte [Substituição manual no Admin](#manual-override-in-the-admin).

## Verificar enriquecimento na loja {#verify-storefront}

**Para verificar o enriquecimento na loja:**

1. Procure o SKU na sua loja.
1. Abra a página do produto.
1. Confirme se o nome e a descrição do produto correspondem ao que você aprovou.

   Pode levar algum tempo até que os enriquecimentos apareçam em sua loja.

1. Confirme se as regiões que mostram a descrição longa correspondem ao que você aprovou.
1. Opcional: Confirme os canais downstream que consomem os mesmos atributos de catálogo, quando relevante para a implantação.

## Substituições, assimilação e sugestões desatualizadas {#overrides-ingestion}

Depois que o enriquecimento do catálogo atualiza o nome ou a descrição de um produto, outros sistemas de assimilação podem alterar os mesmos campos. Os exemplos incluem chamadas de API REST, importações de CSV e feeds PIM.

### Valor original assimilado novamente {#original-value-reingested}

Se um processo externo gravar o nome ou a descrição original (o valor que existia antes do enriquecimento ser aplicado), a Commerce continuará a honrar o valor enriquecido para esse campo de acordo com as regras de enriquecimento do catálogo. A sugestão não pode ser revertida automaticamente com base apenas nessa assimilação.

### Novo valor assimilado novamente {#new-value-reingested}

Se o processo externo enviar um novo valor que não seja uma repetição do texto de pré-enriquecimento, o Commerce respeitará o novo valor de catálogo. Por exemplo, uma renomeação de &quot;Sapatos vermelhos&quot; para &quot;Sapatos vermelhos icônicos&quot; substitui o valor enriquecido. A sugestão de enriquecimento relacionada é normalmente marcada como *Desatualizada* porque o catálogo em tempo real não corresponde mais ao contexto de sugestão.

### Substituição manual no administrador {#manual-override-in-the-admin}

Se você editar manualmente o nome ou a descrição do produto no [!DNL Adobe Commerce] Administrador:

- O valor Admin vence como o sistema de registro para essa alteração manual.
- A sugestão de enriquecimento está marcada como *Desatualizada*.
- O fluxo de trabalho de sugestão volta ao estado original desse item para que você possa criar uma nova linha de base ou aceitar uma nova sugestão se a análise for executada novamente.

Essas regras ajudam você a saber se o enriquecimento do catálogo, os feeds de assimilação ou as edições de administrador são autoritativos quando vários canais tocam a mesma SKU.

## Limites e considerações {#limits}

- O enriquecimento aplica-se apenas a nomes de produtos e descrições longas. Isso não altera o layout da página de detalhes do produto, widgets ou outro conteúdo da loja no nível da página.
- Catálogos grandes e contagens altas de URL podem afetar a rapidez com que a análise é concluída e quantas sugestões são exibidas de uma só vez.
- Sugestões significativas presumem que os bots relevantes para o LLM possam acessar os URLs de produto importantes para você. As regras de robôs, a autenticação, o bloqueio geográfico e a personalização pesada podem reduzir a cobertura.

## Práticas recomendadas {#best-practices}

- Documente a propriedade do sistema para o nome e a descrição do produto, de modo que as tarefas do PIM ou do feed não entrem em conflito involuntariamente com o enriquecimento do catálogo.
- Coordene com as equipes de SEO e marca antes de aplicar títulos ou descrições em massa.
- Sincronizar novamente ou analisar novamente após importações de catálogo principal para que as sugestões reflitam o estado atual do catálogo.

## Exemplos

Os exemplos a seguir mostram como o enriquecimento do catálogo transforma atributos técnicos brutos em uma cópia de produto narrativa, focada no comprador, que os LLMs podem usar para responder a perguntas de compras.

### Exemplo: produto de café com atributos técnicos

Um catálogo da coffee retailer armazena apenas as especificações técnicas de um produto de grãos de café torrado médio: variedade de grãos, região de origem, método de processamento, nível de torrefação e faixa de altitude. Esses campos descrevem o produto, mas não comunicam seu valor a um comprador. Portanto, um assistente de IA tem pouco a trabalhar ao responder uma pergunta como &quot;que café tem um sabor suave e pouco ácido?&quot;

O enriquecimento do catálogo lê os atributos técnicos e os motivos por meio de como eles interagem para inferir características relevantes para o consumidor:

| Atributo técnico | Característica inferida | Raciocínio |
| --- | --- | --- |
| Honey Process, Medium Roast | Baixa acidez | A mucilagem do fruto deixada no feijão durante o processamento do mel suprime a acidez, e o meio assado decompõe os compostos ácidos residuais. |
| Honey Process, Arabica, Medium Roast | Sabor a avelã | Os açúcares de frutos da mucilagem combinam-se com as notas naturais de nozes da Arabica, amplificadas em média torrefação. |
| Processo do Mel, Arábica | Sensação bucal rica e cremosa | Óleos absorvidos da mucilagem durante a secagem adicionam viscosidade e corpo. |
| Processo de mel, Altitude 900-1200m | Conotações de caramelo | Feijão mais denso, de alta altitude, desenvolve açúcares mais complexos, aprofundados pelo processamento do mel. |

O enriquecimento do catálogo aplica essas características inferidas à cópia do produto:

- **Antes**: &quot;Medium Roast Coffee Beans - Arabica, Brasil Minas Gerais, Honey Process, 900-1200m&quot;
- **Depois**: &quot;Feijão arábica cultivado entre 900 e 1.200 metros em Minas Gerais, mel processado e meio torrado, desenvolvem uma sensação bucal naturalmente doce e cremosa, com caractere de avelã distinto, tons caramelo e baixa acidez. Um café especial consistente e acessível, melhor experiente através do derramamento.&quot;

O nome e a descrição atualizados são salvos diretamente no catálogo do Commerce, de modo que a vitrine, os feeds LLM e outros canais que leem esses campos refletem a mesma cópia enriquecida.

### Exemplo: configuração de mobília modular

Uma retailer de mobília vende um sofá de seção modular onde a descrição do produto lista apenas os códigos de configuração e o nome da malha, por exemplo, `6 Standard Seats + 6 Standard Sides in Sapphire Navy Corded Velvet`. Essa abreviação é compreensível para um cliente recorrente, mas fornece ao assistente de IA pouco contexto sobre como o produto funciona ou o que o torna durável ou confortável.

O enriquecimento do catálogo expande os atributos de configuração e malha em uma descrição narrativa que explica o que cada componente faz e por que ele é importante para um comprador:

- **Antes**: &quot;6 assentos padrão + 6 lados padrão em veludo com cabo da marinha de safira&quot;
- **Depois**: &quot;Esta configuração inclui 6 Conjuntos de Inserções de Assento Padrão e 6 Inserções Laterais Padrão que funcionam alternadamente como braços ou costas, formando os blocos de construção modulares do seu layout. Cada assento possui espuma padrão com três camadas de alta densidade projetadas para preservar a sustentação e resistir à abrasão. A cobertura de veludo com cabo da Marinha de Safira é tão durável quanto luxuosa, apresentando fios texturizados que criam um brilho sutil e uma sensação macia e macia. As capas são costuradas à mão para uma aparência precisa e personalizada e são laváveis e substituíveis por máquinas, para que sua seção possa evoluir com o seu espaço.&quot;

Como a descrição enriquecida é gravada de volta no catálogo do Commerce, ela está disponível para bots de IA que rastream a página de detalhes do produto, bem como para qualquer canal ou feed downstream que consome os dados de catálogo do produto, sem alterar o layout ou o design que os compradores veem na página.
