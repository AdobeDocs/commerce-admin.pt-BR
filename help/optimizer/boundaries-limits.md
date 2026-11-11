---
title: Limites e limites dos serviços de merchandising
description: Saiba mais sobre limites de licença e limites do sistema do Adobe Commerce Optimizer. Planeje a capacidade, rastreie o uso e evite a latência e a limitação quando exceder os limites.
role: Admin, Developer
hide: true
badgeSaas: label="Somente SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplicável a instâncias do Adobe Commerce as a Cloud Service provisionadas apenas com CCDM (infraestrutura SaaS gerenciada pela Adobe)."
autotag-review: '2026-11-02T18:48:38.168Z'
TQID: 'https://experienceleague.adobe.com/KoRp--G2sMvv-Hr7KiHriZrFmtEm0BhGoGWVQQK-ofE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
source-git-commit: 71df9ad673f2e7dff802e4b26d8e169c42d9c063
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 1%
---

# Limites e limites dos Serviços de merchandising com o modelo de dados de catálogo combinável (CCDM)

Os Serviços de merchandising da Adobe Commerce com CCDM aplicam limites de licença e limites de sistema que definem quanta capacidade seu projeto pode usar:

- **Limites de licença**—Com base na sua capacidade adquirida; pode ser expandido adquirindo pacotes adicionais.
- **Limites do sistema**—Limites fixos que protegem os recursos do sistema e garantem desempenho confiável para todos os usuários.

Sua utilização deve permanecer dentro desses limites. Excedê-los pode causar maior latência e limitação de solicitação.

## Solicitar capacidade adicional

Os limites de licença podem ser aumentados adquirindo os pacotes de licença descritos na seção [Limites de licença e limites do sistema](#license-limits-and-system-boundaries) ou negociando o licenciamento personalizado para casos de uso exclusivos. Entre em contato com seu representante de conta da Adobe para discutir suas necessidades.

Em caso de dúvidas sobre os limites do sistema, contate o [Suporte da Adobe](https://experienceleague.adobe.com/home?lang=en#support).

## Evitar problemas de desempenho

Siga estas práticas recomendadas para ficar dentro dos limites e evitar problemas operacionais:

- **Revise seus limites**—Entenda seus [limites de capacidade](#license-limits-and-system-boundaries) antes de iniciar novas vitrines ou campanhas.
- **Rastrear seu uso**—Use painéis de métricas internos ou logs de CDN.

## Limites da licença e limites do sistema

As tabelas a seguir resumem os limites de licença e os limites do sistema por área de recurso e incluem informações sobre a adição de mais licenças para expandir a capacidade, quando aplicável.


### Catálogo

| **Recurso** | **Descrição** | **Alocação base** | **Expansível?** |
| --- | --- | --- | --- |
| Taxa de assimilação do produto | A quantidade de produtos criados ou atualizados | 1K atualizações por minuto<p>No máximo 100 mil atualizações por dia</p> | Sim<p>Adicionar um pacote de licenças:</p><ul><li>5 mil atualizações por minuto<br>No máximo 500 mil atualizações por dia</li> <li>10.000 atualizações por minuto<br>No máximo 1 milhão de atualizações por dia</li></ul><p>A capacidade máxima para assimilação de dados é de 1 milhão de atualizações por dia.</p> |
| Tamanho do conteúdo do produto | A quantidade máxima de dados permitida ao criar, atualizar ou assimilar informações do produto usando a API | 200 KB | Não |
| Variações do catálogo | O número de visualizações de um catálogo que estão disponíveis para os usuários da loja,<p>que são contados como (*Número de Exibições do Catálogo × Número de Catálogos de Preços*)</p> | 100 variações | Sim<p>Adicionar pacote de licenças de 100 variações de catálogo</p> |
| Produtos em uma única origem de catálogo | SKUs compatíveis no catálogo | 250 mil SKUs | Sim<p>Adicionar pacote de licença do 100K SKU</p> |
| Variantes por produto | O número de variantes de produtos (tamanho, combinações de cores) permitidas por produto | 10 K | Não |
| Origens do catálogo | O número de contextos de dados de catálogo (por exemplo, localidades ou fontes de dados como PIMs e ERPs) | 50 | Não |

{style="table-layout:auto"}

### Catálogos de preços

| **Recurso** | **Descrição** | **Alocação base** | **Expansível?** |
| --- | --- | --- | --- |
| Catálogos de preços | O número de catálogos de preços permitidos por instância | Com base no número de [Variações de catálogo](#catalog) | Sim<br>Aumentar variações de catálogo |
| Descontos por registro de preço | O número de descontos que podem ser aplicados a um preço de produto em um único catálogo de preços | 10 | Não |

{style="table-layout:auto"}

### Exibições e políticas do catálogo

| **Recurso** | **Descrição** | **Alocação base** | **Expansível?** |
| --- | --- | --- | --- |
| Exibições de catálogo | Número de subconjuntos configuráveis do catálogo principal | Com base no número de [Variações de catálogo](#catalog) | Sim<br>Aumentar variações de catálogo |
| Políticas por exibição de catálogo | Número de filtros de dados permitidos | 10 | Não |
| Valores de atributo em uma política | Número de características do produto que podem ser configuradas para filtragem | 100 | Não |
| [Atribuição de chave de acesso restrito](setup/private-catalog-view.md) | Número de chaves de acesso restrito que podem ser atribuídas a uma única exibição de catálogo | 3 | Não |
| Tamanho da chave RSA (chaves de acesso restrito) | Fortaleza de chave mínima e máxima aceita para uma chave de acesso restrito | 2048 bits mínimo, 8192 bits máximo | Não |
| Chaves de acesso restrito | Atraso na propagação de revogação de chave | Até 5 minutos, devido ao armazenamento em cache. Os tokens assinados por uma chave removida são negados assim que o atraso decorre. | Não se aplica |

{style="table-layout:auto"}

### Loja do catálogo

A alocação básica para os recursos de vitrine de catálogo é determinada com base no nível GMV (valor de mercadoria bruta). A tabela indica a alocação mínima para cada recurso.

| **Recurso** | **Descrição** | **Alocação base** | **Expansível?** |
| --- | --- | --- | --- |
| Taxa de recuperação do catálogo | Número de vezes por mês que uma API de catálogo é chamada por um sistema (vitrine, sistema de transações, ERP ou outro) para recuperar dados do catálogo | Com base no nível de GMV<p>Alocação mínima: 10 milhões/mês</p> | Sim<p>Adicionar 1 milhão de solicitações por mês a pacotes de licenças</p> |
| Solicitações de conteúdo | Solicitações à loja para exibições de página do HTML ou chamadas de API JSON. Contado como 1 exibição de página ou 5 chamadas de API. | Com base no nível de GMV<p>Alocação mínima: 2 milhões/mês</p> | Sim<p>Adicionar um pacote de licença mensal</p> |
| Variações da GenAI da loja | Permissão para a geração de conteúdo baseado em texto | Com base no nível de GMV<p>Alocação mínima: 1 mil variações por mês</p> | Sim<p>Adquirir créditos de IA geradores separadamente</p> |

{style="table-layout:auto"}

>[!NOTE]
>
>A geração de imagem requer uma licença [!DNL Adobe Firefly] provisionada para a mesma organização IMS que [!DNL Adobe Commerce Optimizer].


### Descoberta de produto

Os limites a seguir se aplicam à pesquisa de produtos da loja, à listagem e à configuração de merchandising.

| **Recurso** | **Descrição** | **Alocação base** | **Expansível?** |
| --- | --- | --- | --- |
| Recuperação de produto | Máximo de SKUs por solicitação do GraphQL [!DNL Catalog Service] ao buscar dados do produto com `products`, `productSearch`, `refineProduct` e `variants`. Dividir solicitações maiores em várias chamadas. | 100 | Não |
| Atributos filtráveis | O número de características do produto (como cor, tamanho, marca ou material) que podem ser ativadas para a navegação em camadas e aspectos | 200 | Não |
| Atributos pesquisáveis | O número de características do produto que podem ser indexadas para pesquisa no catálogo | 200 | Não |
| Atributos classificáveis | O número de características do produto disponíveis como opções de classificação em páginas de pesquisa e categoria. | 50 | Não |
| Profundidade da paginação de pesquisa | Máximo de produtos acessível por meio de paginação de pesquisa (por exemplo, página 100 × 100 produtos/página) | 10 K | Não |
| Facetas | O número de atributos de produto filtráveis (como Marca, Cor, Tamanho, Preço) que podem ser configurados para ajudar os compradores a refinar os resultados da pesquisa e procurar categorias | 100<p>Deve ser um atributo filtrável</p> | Não |
| Opções por faceta | O número de valores de atributo de produto filtráveis que os compradores podem selecionar em uma faceta (por exemplo, &quot;Vermelho&quot;, &quot;Azul&quot; para Cor; &quot;Pequeno&quot;, &quot;Medium&quot; para Tamanho) | 100 | Sim<p>Pode aumentar por meio de solicitação de suporte</p> |

{style="table-layout:auto"}

### Recommendations

Os recursos a seguir estão disponíveis para recomendações de produtos. Alguns recursos disponíveis em outros produtos da Adobe Commerce não têm suporte no [!DNL Adobe Commerce Optimizer].

| **Recurso** | **Descrição** | **Alocação base** | **Expansível?** |
| --- | --- | --- | --- |
| Unidades de recomendação ativas | Número de componentes de recomendação ativos na sua loja (como &quot;Clientes também visualizados&quot; ou &quot;Você também pode gostar&quot;) | 50 | Não |
| Inclusões/exclusões de categoria ou atributo | Filtrar produtos para um conjunto específico que esteja qualificado para recomendações | Não suportado | — |

{style="table-layout:auto"}
