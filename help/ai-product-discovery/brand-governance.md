---
title: Criar regras de marca de enriquecimento de catálogo
description: Saiba como criar e gerenciar regras de governança de marca para o Enriquecimento do catálogo, definir requisitos de cópia de produto e aplicar regras aos trabalhos de Enriquecimento do catálogo.
role: Admin, User, Leader
source-git-commit: 9d7a4f4e98fe2d2d51261d96a2e072c28925babd
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%
---
# Criar regras de marca de Enriquecimento de Catálogo

As regras de governança de marca e governança de marca estão disponíveis somente para o Enriquecimento do catálogo. Não se aplicam ao enriquecimento em PDP. Essas regras definem requisitos para nomes de produtos e descrições gerados por [!DNL Commerce Catalog Agent]. Edite ou configure uma Regra padrão para seus padrões de marca padrão e, em seguida, crie regras personalizadas para campanhas específicas, categorias de produtos ou submarcas. Selecione uma regra ao criar um trabalho de [Enriquecimento do catálogo](catalog-enrichment.md).

## Governança de marca aberta

1. No Admin, vá para **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**.
1. Abra a guia **[!UICONTROL Brand Governance]**.

A guia **Controle de Marca** contém a Regra Padrão e todas as regras personalizadas que você criou. Você pode pesquisar por regras ou filtrar a tabela de regras.

Para cada linha, você verá o **Nome da regra**, **Campos**, **Tom**, **Última modificação** e **Status**. A Regra Padrão está marcada **[!UICONTROL Default]**.

A área **[!UICONTROL Needs your attention]** destaca as regras que precisam ser trabalhadas, como rascunhos que precisam ser configurados ou regras com conflitos. Revise os detalhes da regra e use a ação disponível, como **[!UICONTROL Finish setup]** ou **[!UICONTROL Fix conflict]**.

## Entender os tipos de regras

O Enriquecimento de catálogo oferece suporte a uma regra padrão e a regras personalizadas.

### Regra padrão

Cada instância [!DNL Adobe Commerce] tem exatamente uma Regra Padrão. [!DNL Adobe Commerce] cria esta regra com campos vazios. Seu nome está fixo como **[!UICONTROL Global]**. É possível editar a regra, mas não excluí-la.

O [!DNL Adobe Commerce] aplica a Regra Padrão por padrão ao criar um trabalho de Enriquecimento de Catálogo sem selecionar uma regra personalizada. A Regra padrão fornece a governança de linha de base para o Enriquecimento de catálogo.

### Regras personalizadas

É possível criar qualquer número de regras personalizadas para uma campanha, categoria de produto ou submarca. Uma regra personalizada não é aplicada automaticamente. Selecione-a ao criar um trabalho de Enriquecimento de catálogo.

Uma regra personalizada não herda valores da Regra padrão. Ao criar uma regra personalizada, você pode copiar os valores atuais da Regra padrão como um ponto de partida único. Alterações posteriores na Regra padrão não atualizam a regra personalizada.

Use a Regra padrão para padrões que devem se aplicar quando um usuário não selecionar uma regra personalizada. Crie uma regra personalizada para uma campanha ou categoria com requisitos diferentes. Adicione quaisquer Requisitos globais que a regra personalizada também precise, pois as regras personalizadas não herdam Valores globais.

## Criar uma regra personalizada

Nesta seção, você aprenderá a criar uma regra de governança de marca.

![Criar regra de governança de marca](./assets/brand-gov-create-rule.png)

1. Na guia **Controle de Marca**, clique em **[!UICONTROL Create Rule]**.
1. Escolha como iniciar a regra:
   - **[!UICONTROL Blank]**: Defina você mesmo todos os valores.
   - **[!UICONTROL Copy Global enrichment]**: comece com os valores de Regra Padrão atuais como uma cópia única.
   - **[!UICONTROL Draft with AI]**: (**Em breve**) descreva a voz da sua marca para obter os valores de regras sugeridos.
1. Digite um **Nome da regra** que identifique sua finalidade, como campanha, categoria ou submarca.
1. Em **Campos a serem aprimorados**, configure os requisitos do nome e da descrição do produto.

   Configure os nomes e as descrições dos produtos separadamente. Cada campo tem seus próprios requisitos de switch e governança habilitados.

1. Definir **Comprimento do nome do produto**.

   Defina o intervalo de comprimento mínimo e máximo de um nome de produto enriquecido. Por exemplo, uma regra pode exigir no mínimo 20 caracteres e no máximo 200 caracteres.

1. Defina a opção **Capitalização**:

   - **[!UICONTROL Sentence case]**: `Waterproof hiking boots`
   - **[!UICONTROL Title Case]**: `Waterproof Hiking Boots`
   - **[!UICONTROL As written]**: Preserve a capitalização do texto de origem.

1. Descreva o **Tom da marca**. Consulte [definir tom da marca](#set-brand-tone) para obter orientação.
1. Definir as frases necessárias e excluídas

   Adicione uma frase **[!UICONTROL Must include]**.
   Adicione uma frase **[!UICONTROL Never use]**.

1. Clique em **[!UICONTROL Save as draft]** para concluir mais tarde ou clique em **[!UICONTROL Publish rule]** para tornar a regra disponível para seleção ao criar uma regra de enriquecimento de catálogo. Clique **[!UICONTROL Cancel]** para sair sem salvar.

1. Agora você pode aplicar a regra a um trabalho de [Enriquecimento do catálogo](catalog-enrichment.md).

### Definir o tom da marca

Digite orientação no campo **[!UICONTROL Brand tone]** multilinha para descrever a voz e o estilo do nome enriquecido.

Estes são alguns exemplos do tom que você pode usar para a **Descrição**:

- **B2B industrial**: `Write for the operator and the buyer. Open with what the unit does and where it fits in the kitchen, then throughput, utility requirements, footprint, and certifications. Plain, technical language. Mention cleaning and maintenance, because total cost of ownership drives the decision. No lifestyle language.`
- **Moda de luxo**: `Quiet confidence. Lead with craftsmanship and provenance (atelier, tannery, technique), then how the piece wears and ages. Short, measured sentences. Sensory detail is fine. Never compare to other brands or mention price or value.`
- **Eletrônicos de consumo**: `Clear and benefit-led. Turn every spec into what it does for the user. Scannable short paragraphs or bullets. Put compatibility and what's in the box up front. Don't make performance claims without a source, and don't use comparative claims like "fastest"`
- **Comida e mercearia especializados**: `Warm and appetizing, but honest. Describe taste, texture, and aroma in concrete terms, then origin and how it's made, then serving ideas. Plain, friendly language. Put allergens and dietary attributes in a consistent closing line. Don't make health claims.`
- **Móveis residenciais**: `Inviting and practical. Open with how the piece is used, then dimensions, materials, and care. Help the shopper picture it in their space without overselling. Always mention assembly, delivery, and weight, since those drive returns.`
