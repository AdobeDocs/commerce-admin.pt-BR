---
title: Enriquecimento do catálogo
description: Use o recurso de enriquecimento do catálogo nativo no Adobe Commerce para revisar e aplicar as melhorias sugeridas pela IA aos nomes de produtos e descrições longas para descoberta assistida por LLM e IA.
role: Admin, User, Leader
recommendations: noCatalog
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a5d9ef32b56d3f422e7af6352002ed5827fc185c
workflow-type: tm+mt
source-wordcount: 2182
ht-degree: 0%

---

# Enriquecimento do catálogo

O enriquecimento do catálogo é um recurso nativo do [!DNL Adobe Commerce] que ajuda a melhorar os nomes de produtos e as descrições longas, para que seu catálogo seja representado com mais precisão quando os compradores usarem LLMs e assistentes de IA para pesquisa e descoberta de produtos.

>[!NOTE]
>
>O enriquecimento do catálogo é viabilizado por [!DNL Commerce Catalog Agent] e [!DNL Adobe LLM Optimizer] nos bastidores. O enriquecimento é usado como parte do fluxo de trabalho do catálogo do Commerce. Você não gerencia uma integração do LLM Optimizer separada para aplicar atualizações de nome e descrição aprovadas. Para um monitoramento e otimização mais amplos do LLM fora do Commerce, consulte a [documentação do produto do LLM Optimizer](https://experienceleague.adobe.com/en/docs/llm-optimizer/using/home).

## Como funciona {#how-it-works}

O catálogo de produtos do [!DNL Adobe Commerce] é o sistema de registro de dados de produtos: nomes, descrições, atributos, preços e estoque. [!DNL Adobe Commerce] O MCP da loja (Model Context Protocol) conecta dados de catálogo em tempo real às experiências do Adobe AI. A partir daí, o Catalog Agent pode identificar lacunas em nomes de produtos e descrições longas, propor melhorias e gravar alterações aprovadas no Commerce para que você possa analisá-las no Commerce Admin.

Com o enriquecimento do catálogo, você pode:

- Identifique lacunas e inconsistências nos nomes de produtos e descrições longas que afetam como os LLMs interpretam seus produtos.
- Revise as melhorias sugeridas com o contexto de suporte, incluindo justificações e comparações antes e depois.
- Aplique atualizações aprovadas diretamente ao catálogo do Commerce para que o Administrador, a loja e outros canais que leem esses campos permaneçam alinhados.

Como os nomes dos produtos e as descrições longas ficam no Commerce, a melhoria da cópia uma vez pode beneficiar cada canal que consome esses dados do produto. O benefício depende de como e quando seus sistemas são atualizados.

| Direção | Finalidade |
| --- | --- |
| Catálogo do Commerce -> análise | Sugestões de enriquecimento de feed de sinais de catálogo e URL. |
| Enriquecimento -> Catálogo do Commerce | Depois de aprovar uma atualização, as alterações no nome e na descrição do produto são salvas no catálogo do Commerce para que o administrador e a loja reflitam os valores otimizados. |

## Quem é este {#who-this-is-for}

- Profissionais de marketing digital e comerciantes que desejam que os dados do produto sejam precisos e consistentes em respostas orientadas por LLM.
- Profissionais de marketing digital e comerciantes que precisam de uma maneira controlada para melhorar a cópia do catálogo em escala.
- Administradores do Commerce que são proprietários de integridade de catálogo, processos administrativos e integrações (API, CSV, PIM) que alimentam atributos de produto.

## Pré-requisitos {#prerequisites}

Os seguintes pré-requisitos se aplicam quando você tem acesso ao enriquecimento do catálogo.

- Sua loja pode ser rastreada por bots orientados a LLM e de agente, nos quais a cobertura do rastreo é necessária para sugestões com reconhecimento de catálogo.
- Os serviços Commerce necessários e a conectividade de catálogo estão ativados e íntegros. Consulte [Habilitar enriquecimento do catálogo](#enable-catalog-enrichment) para saber mais.
- [IMS configurado](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations).
- Você tem acesso ao [Adobe Admin Console](https://helpx.adobe.com/business/enterprise/plan-your-deployment/basic-concepts/admin-console.html).
- Sua organização assinou o GenAI Rider, ou recusou explicitamente, os serviços de IA subjacentes.

>[!NOTE]
>
>Como parte da configuração, a Commerce verifica se sua organização assinou o GenAI Rider que cobre os serviços de IA por trás do enriquecimento de catálogo. Se você ainda não tiver assinado o piloto ou optado por não participar, será solicitado que assine ou atualize o piloto antes de poder usar o enriquecimento do catálogo.

## Ativar enriquecimento do catálogo {#enable-catalog-enrichment}

Trabalhe com o administrador do Commerce ou parceiro de implementação para garantir o seguinte antes de revisar ou aplicar sugestões:

### Instalar extensões de enriquecimento do catálogo e serviços de catálogo

1. Instale a extensão de enriquecimento do catálogo na instância do Commerce executando o seguinte comando:

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Se você ainda não tiver instalado os Serviços de catálogo, [faça isso](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/installation#install-the-catalog-service-extension).

   **[!UICONTROL Catalog enrichment]** agora está disponível na sua instância do Commerce.

### Acessar enriquecimento do catálogo

Após instalar as extensões de enriquecimento do catálogo e serviços de catálogo, o recurso de enriquecimento do catálogo estará disponível no Administrador em **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Enrichment]**.

![Enriquecimento do catálogo](./assets/catalog-enrichment-menu.png)

### Configurar enriquecimento do catálogo

Configure o enriquecimento do catálogo na guia **[!UICONTROL Settings]** para que o [!DNL Commerce Catalog Agent] possa se conectar ao seu ambiente [!DNL Adobe Commerce] e sugerir a superfície no Administrador do Commerce.

1. No Admin, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Enrichment]**.
1. Na lista **[!UICONTROL Scope]** na parte superior da página, selecione o modo de exibição de loja que deseja configurar ou deixe **[!UICONTROL All Store Views]** para gerenciar as configurações entre os modos de exibição de loja.
1. Abra a guia **[!UICONTROL Settings]**.
1. Em **[!UICONTROL Commerce Configuration]**, expanda o painel de exibição de loja rotulado com sua URL.

   Forneça os detalhes do ambiente [!DNL Adobe Commerce] para habilitar o Serviço de Catálogo do LLM Optimizer e os fluxos de trabalho de auditoria.

   ![Configuração do Commerce na guia Configurações de Enriquecimento do Catálogo](./assets/catalog-enrichment-commerce-config.png)

1. Insira os detalhes da conexão necessários para a exibição da loja.

   - **[!UICONTROL Store View URL]**: URL correspondente à exibição de armazenamento (por exemplo, `https://brand.example.com/fr/`).
   - **[!UICONTROL Environment ID]**: Identificador exclusivo do ambiente [!DNL Adobe Commerce] que a conexão acessa.
   - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]** e **[!UICONTROL Store View Code]**: Códigos de exibição de site, loja e loja do site da Commerce. Esses valores devem corresponder aos códigos no Administrador do Commerce.
   - **[!UICONTROL Host Name]**: Nome do host da sua instância [!DNL Adobe Commerce].

1. Clique em **[!UICONTROL Save]**.

Depois de salvar, aguarde a conclusão de qualquer trabalho de sincronização ou validação inicial antes de depender dos resultados do catálogo ou da auditoria para essa exibição de armazenamento. Pode levar até 24 horas para que as sugestões de produtos sejam exibidas na página **[!UICONTROL Catalog Enrichment]**.

Para remover uma configuração de exibição de repositório, expanda essa entrada e clique em **[!UICONTROL Delete]**.

#### Descrições dos campos {#commerce-connection-fields}

Os campos obrigatórios estão marcados com um asterisco (*) no formulário **[!UICONTROL Commerce Configuration]**.

| Campo | Obrigatório | Descrição |
| --- | --- | --- |
| Armazenar URL de exibição | Sim | URL correspondente à exibição de armazenamento (por exemplo, `https://brand.example.com/fr/`). |
| ID do ambiente | Sim | Identificador exclusivo do ambiente [!DNL Adobe Commerce] que a conexão acessa. |
| Código do site | Sim | Código do site da Commerce. |
| Armazenar código | Sim | Código de armazenamento do site da Commerce. |
| Código de exibição da loja | Sim | Exibição de loja do site da Commerce. |
| Nome do host | Sim | Nome do host da instância [!DNL Adobe Commerce]. |

### Revisar e aplicar enriquecimento do catálogo {#review-and-apply}

Após habilitar e configurar o enriquecimento do catálogo, as sugestões de produtos são exibidas na guia **[!UICONTROL Agentic Opportunities]**. Aqui, você pode revisar sugestões e aplicar atualizações aprovadas a nomes de produtos e descrições longas no catálogo do Commerce.

O enriquecimento do catálogo usa as seguintes exibições de fluxo de trabalho:

- **[!UICONTROL Current Suggestions]**: itens novos ou ativos para revisão.
- **[!UICONTROL Fixed Suggestions]**: itens que você já aplicou ou resolveu.
- **[!UICONTROL Ignored Suggestions]**: itens que você excluiu intencionalmente da ação.

![Enriquecimento do catálogo](./assets/agentic-opportunities.png)

### Implantar sugestões aprovadas {#review-deploy-catalog}

Para implantar sugestões aprovadas:

1. Selecione **[!UICONTROL Current Suggestions]**.
1. Clique no controle de expansão da linha URL ou SKU para mostrar o nome do produto proposto e as atualizações da descrição do produto.
1. Revise a sugestão e confirme se ela corresponde à sua estratégia de merchandising e SEO.

Você pode editar uma sugestão antes de implantá-la ou movê-la para **[!UICONTROL Ignored Suggestions]** se ela não corresponder à sua estratégia.

1. Selecione a linha do URL ou SKU a ser atualizado.
1. Clique em **[!UICONTROL Deploy optimizations]** e confirme.

Alterações de nome e descrição aprovadas são salvas no catálogo [!DNL Adobe Commerce] como outras atualizações de produto.

>[!IMPORTANT]
>
>Trate cada atualização aplicada como uma alteração no catálogo de produção. Use suas práticas normais de controle de alterações, preparo e controle de qualidade. Aplique as atualizações somente depois que as partes interessadas em merchandising e SEO concordarem com a cópia final.

Depois de aplicar uma atualização, as sugestões serão movidas para **[!UICONTROL Fixed Suggestions]** com o status **Marcado como Fixo**.

## Verificar enriquecimento no Admin {#verify-in-admin}

**Para verificar o enriquecimento do catálogo aplicado:**

1. Vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]** no Administrador do Commerce.
1. Use filtros e o seletor **[!UICONTROL Store View]** conforme necessário (por exemplo, **[!UICONTROL Default Store View]**).
1. Procure o SKU.
1. Abra o produto no modo de edição.

   O formulário do produto mostra o nome e/ou a descrição do produto enriquecido.

   ![Nome de Produto Enriquecido](./assets/enriched-product-name.png)

1. Opcional: selecione **[!UICONTROL Override Catalog Agent provided Product Name]** se quiser manter um nome inserido manualmente.

   As substituições manuais afetam como as sugestões permanecem sincronizadas com o catálogo. Para obter mais informações, consulte [Substituição manual no Admin](#manual-override-in-the-admin).

1. Expanda a seção **[!UICONTROL Content]** e localize o campo de descrição.

   A descrição enriquecida é exibida quando você aplica as alterações de descrição.

   ![Enriquecer Descrição Do Produto](./assets/enrich-product-description.png)

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

- O enriquecimento aplica-se apenas a nomes de produtos e descrições longas. Isso não altera o layout PDP, widgets ou outro conteúdo de vitrine no nível da página.
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
