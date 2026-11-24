---
title: Descoberta de produto de IA
description: Saiba como o enriquecimento do catálogo e o enriquecimento de PDP do [!DNL Adobe Commerce] solucionam as lacunas em dados de produtos estruturados e em cópias focadas no comprador para descoberta de produtos de IA.
role: Admin, User, Leader
source-git-commit: f2cf82dad7ec3c86a3b9a0a5635556ac2e77dd05
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%
---
# Descoberta de produto de IA

A descoberta de produtos é a forma como os compradores encontram e avaliam os produtos que atendem às suas necessidades. Em ferramentas de IA de conversação, como o [!DNL ChatGPT] e o [!DNL Gemini], os compradores podem descrever o que desejam na linguagem do dia a dia e usar respostas geradas por IA para explorar e comparar produtos. A utilidade dessas respostas depende, em parte, do fato de os agentes de IA poderem aceder e interpretar dados relevantes do produto.

## Quem é este guia {#who-this-guide-is-for}

- Profissionais de marketing digital e comerciantes que desejam que os dados do produto sejam precisos e úteis na descoberta de produtos assistidos por IA.
- Merchandisers que precisam de uma maneira controlada para enriquecer produtos selecionados ou preparar uma cópia para uma campanha.
- Administradores do [!DNL Adobe Commerce] responsáveis por dados de catálogo, serviços e acesso de Administrador.

## Por que a descoberta de produtos é importante

Os compradores geralmente descrevem uma necessidade, uso ou preferência em vez de procurar um nome de produto ou atributo técnico exato. Para corresponder essas solicitações aos produtos relevantes, os agentes de IA precisam de informações sobre os produtos estruturadas e relevantes para os compradores.

Quando os registros de produtos estão incompletos, inconsistentes ou focados apenas em especificações técnicas, os agentes podem ter dificuldade em entender quais produtos se encaixam na intenção de um comprador. Os compradores podem perder produtos relevantes, e os comerciantes podem precisar gastar tempo corrigindo e enriquecendo conteúdo de catálogo manualmente.

Além disso, consultas a compradores sem marca criam novas oportunidades para a descoberta de produtos. Quando os compradores descrevem suas necessidades sem especificar uma marca, as superfícies de IA mostram produtos relevantes entre marcas concorrentes com base no desempenho desses produtos em relação à intenção do comprador. Para os comerciantes, isso cria uma oportunidade de alcançar novos clientes que podem não estar familiarizados com sua marca, expandindo a visibilidade do produto além do reconhecimento da marca existente.

No entanto, existem alguns desafios na descoberta de produtos em superfícies de IA, como lacunas no catálogo que podem limitar a descoberta de produtos assistidos por IA.

O [!DNL Adobe Commerce] resolve esses problemas de lacuna do catálogo fornecendo dois fluxos de trabalho complementares de enriquecimento: enriquecimento da página de detalhes do produto e enriquecimento do catálogo. Esses dois enriquecimentos melhoram a maneira como os agentes de IA acessam, entendem e combinam produtos à intenção do comprador. Eles podem ser acessados no menu _Admin_ > **Descoberta de Produto de IA**.

## Os fatos do produto são difíceis de acessar e interpretar

As informações do produto geralmente são distribuídas entre atributos, variantes, opções, categorias e outros campos de catálogo. Embora essas informações possam estar disponíveis para os compradores na loja, elas nem sempre são acessíveis ou facilmente interpretadas pelos rastreadores de IA. Os detalhes do produto apresentados por meio de conteúdo renderizado dinamicamente, componentes dependentes de JavaScript, assistentes de compras interativos, pop-ups ou páginas vinculadas podem ser difíceis de serem recuperados pelos rastreadores.

Mesmo quando essas informações estão acessíveis, elas podem não ser estruturadas de uma maneira que os agentes de IA possam interpretar de maneira confiável. Como resultado, os agentes de IA podem não ter uma compreensão completa dos recursos, opções disponíveis e capacidades de um produto, limitando sua capacidade de corresponder com precisão os produtos às necessidades do comprador.

### Disponibilizar fatos estruturados com o Enriquecimento da página de detalhes do produto

O Enriquecimento de PDP cria uma carga útil de dados estruturados contendo informações relevantes do produto, incluindo atributos, variantes, opções, marcadores de recursos, relacionamentos de categorias, preços e disponibilidade. Isso fornece aos agentes de IA uma compreensão mais completa e estruturada dos recursos e das configurações disponíveis de um produto.

Com a tecnologia [Otimize at Edge](#prerequisites), as informações enriquecidas do produto ficam diretamente acessíveis aos rastreadores de IA, sem exigir alterações na loja visível por humanos. Os comerciantes podem melhorar o modo como as informações do produto são apresentadas aos agentes de IA sem modificar os layouts da loja, introduzir novos componentes voltados para o consumidor ou exigir o desenvolvimento de vitrines personalizadas.

Consulte [enriquecimento da página de detalhes do produto](pdp-enrichment.md).

## O catálogo de produtos não reflete a intenção do comprador

Os compradores descrevem cada vez mais suas necessidades, problemas e casos de uso pretendidos em linguagem natural, em vez de procurar nomes de produtos específicos ou especificações técnicas. No entanto, os nomes e as descrições dos produtos geralmente se concentram em atributos técnicos, sem comunicar claramente os benefícios, os casos de uso ou os problemas reais que um produto soluciona.

Isso cria uma lacuna entre a maneira como os compradores expressam suas necessidades e como os produtos são descritos no catálogo. Sem um conteúdo de produto claro e centrado no comprador, os agentes de IA podem ter dificuldades para interpretar o valor de um produto e a relevância para a intenção do comprador, possivelmente ignorando produtos adequados em favor de alternativas cujas descrições se alinhem mais claramente às necessidades do comprador.

### Otimizar o conteúdo do catálogo de produtos com a intenção do comprador usando o Enriquecimento de catálogo

O Enriquecimento do catálogo transforma os atributos técnicos do produto e as informações existentes do catálogo em nomes e descrições de produtos com foco no comprador que comunicam claramente os benefícios, os recursos e os casos de uso reais de um produto. Os nomes e as descrições dos produtos estão entre as fontes mais influentes de informações que as superfícies de IA usam para entender os recursos do produto e determinar sua relevância para a intenção do comprador.

Conectando as especificações técnicas do produto às necessidades e aos problemas que os compradores descrevem em linguagem natural, o Enriquecimento do catálogo ajuda os agentes de IA a entender melhor o valor de um produto, reduzir a ambiguidade na interpretação de seus recursos e corresponder com mais precisão os produtos relevantes à intenção do comprador.

Os comerciantes podem revisar e aprovar melhorias sugeridas antes de aplicá-las diretamente ao catálogo de produtos do Adobe Commerce. Isso garante que as lojas e os canais de vendas alimentados pelo catálogo possam comunicar consistentemente as mesmas informações enriquecidas e de valor do produto aos compradores em todos os pontos de contato.

Consulte [Enriquecimento do catálogo](catalog-enrichment.md).

#### Regras de governança da marca

As regras de governança da marca permitem definir requisitos de cópia do produto para o enriquecimento do catálogo, incluindo comprimento, frases, tom e capitalização. Essas regras se aplicam apenas ao enriquecimento do catálogo, não ao enriquecimento de PDP.

Consulte [Criar regras de marca de Enriquecimento de Catálogo](brand-governance.md).
