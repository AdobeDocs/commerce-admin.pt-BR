---
title: Preparo de conteúdo
description: O armazenamento temporário de conteúdo oferece à sua equipe de negócios a capacidade de criar, visualizar e agendar facilmente uma grande variedade de atualizações de conteúdo para sua loja diretamente do administrador.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# Preparo de conteúdo

{{ee-feature}}

O preparo de conteúdo oferece à sua equipe de negócios a capacidade de criar, visualizar e agendar facilmente uma grande variedade de atualizações de conteúdo para sua loja diretamente do _Administrador_. Por exemplo, em vez de pensar em termos de uma página estática, considere uma página como uma coleção de diferentes elementos que podem ser ativados _em_ ou _desativados_ com base em um agendamento. Você pode usar o preparo de conteúdo para criar uma página que muda automaticamente durante o ano em um agendamento.

O termo _campanha_ se refere ao registro de uma alteração agendada ou a uma coleção de alterações gerenciadas no Painel de Preparo. As alterações podem ser visualizadas em um calendário ou linha do tempo. Os termos _alteração agendada_ e _atualização agendada_ são intercambiáveis e se referem a uma única alteração.

Quando você agenda uma alteração de conteúdo por um período específico, o conteúdo é revertido para a versão anterior quando a alteração agendada expira. Você pode criar várias versões do mesmo conteúdo de linha de base a ser usado para atualizações futuras. Você também pode voltar atrás na linha do tempo para visualizar versões anteriores do conteúdo. Para salvar uma versão de rascunho, basta atribuir uma data na linha do tempo que está tão distante no futuro que ela nunca entra em produção.

## Campanhas e objetos de preparo de conteúdo

Os campos relacionados à Data inicial e à Data final foram removidos do Adobe Commerce e não podem ser modificados diretamente na regra de preço do carrinho, na regra de preço do catálogo, no produto, na categoria e na página do CMS. Você deve criar uma atualização agendada para essas ativações.

Todas as atualizações programadas são aplicadas consecutivamente, o que significa que qualquer entidade pode ter apenas uma atualização programada de cada vez. Qualquer atualização agendada é aplicada a todas as exibições de loja dentro de seu período de tempo. Como resultado, uma entidade não pode ter uma atualização agendada diferente para diferentes exibições de loja ao mesmo tempo. Todos os valores de atributo de entidade em todas as exibições de armazenamento, que não são afetados pela atualização agendada atual, são obtidos dos valores padrão, e não da atualização agendada anterior.

Quando uma nova atualização agendada é criada para qualquer um dos seguintes objetos, uma campanha correspondente é criada como um espaço reservado e a caixa _[!UICONTROL Scheduled Changes]_&#x200B;é exibida na parte superior da página. A campanha de espaço reservado tem uma data inicial, mas não uma data final. Você pode agendar atualizações no conteúdo como parte de uma campanha, bem como pré-visualizar e compartilhar as alterações por data, hora ou exibição de loja. Depois que uma nova campanha é criada para um objeto, você pode atribuí-la como uma atualização programada para outros objetos.

- [Produtos](../catalog/product-scheduled-changes.md)
- [Categorias](../catalog/category-scheduled-changes.md)
- [Regras de preço de catálogo](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Regras de preço do carrinho](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [Páginas do CMS](pages-workspace.md#scheduled-changes)
- [Blocos do CMS](blocks.md)

## Fluxo de trabalho de preparo de conteúdo

1. **Criar o conteúdo da linha de base**

   A linha de base é o conteúdo de um ativo sem uma campanha e inclui tudo abaixo da seção _[!UICONTROL Scheduled Changes]_&#x200B;na parte superior da página. O conteúdo da linha de base é sempre usado, a menos que haja uma campanha ativa com alterações programadas para esse local na linha do tempo.

1. **Criar a primeira campanha**

   Crie sua primeira campanha com as datas de início e término conforme necessário. Para tornar a campanha aberta, deixe a data final em branco. Quando a primeira campanha terminar, o conteúdo original da linha de base será restaurado.

   A data de início e a data de término da campanha devem ser definidas usando o fuso horário padrão **_1&rbrace; do administrador, que é convertido do fuso horário local de cada site._** Considere um exemplo em que você tem vários sites em fusos horários diferentes, mas deseja iniciar uma campanha com base em um fuso horário dos EUA. Nesse caso, você deve agendar uma atualização separada para cada fuso horário local e definir **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** como convertidos de cada fuso horário de site local para o fuso horário padrão do Administrador.

1. **Adicionar uma segunda campanha**

   Crie a segunda campanha, com as datas de início e término conforme necessário. A segunda campanha pode ser atribuída a um período totalmente diferente. Ao criar várias campanhas para o mesmo ativo, as campanhas não podem se sobrepor. Você pode criar quantas campanhas forem necessárias.

   Vários ativos podem ser atribuídos a uma campanha existente que ainda não foi iniciada. Por exemplo, dois preços de produtos diferentes podem ser atualizados no escopo da mesma campanha com uma data de início futura.

   >[!NOTE]
   >
   >Se uma campanha estiver vinculada a mais de uma entidade, ela só poderá ser editada no [Painel de preparação de conteúdo](content-staging-dashboard.md).

1. **Restaurar o conteúdo da linha de base**

   Se todas as campanhas tiverem datas de término, o conteúdo da linha de base será restaurado sempre que todas as campanhas ativas terminarem.

   >[!NOTE]
   >
   >Se uma campanha ativa for criada inicialmente sem uma data de término, a campanha não poderá ser editada posteriormente para incluir uma data de término. Nesse caso, é necessário criar uma campanha duplicada e inserir a data final necessária.

>[!NOTE]
>
>Enquanto uma atualização por preparo está ativa para uma entidade, editar a entidade está editando a atualização de preparo ativa atual. Isso não afeta o conteúdo de linha de base, que é restaurado quando a atualização de preparo termina.

## Painel [!UICONTROL Content Staging]

O [!UICONTROL Content Staging] [painel](content-staging-dashboard.md) oferece visibilidade de todas as alterações e atualizações de site planejadas. Qualquer dia, intervalo de datas ou período de uma campanha pode ser visualizado e compartilhado com outras pessoas.

![Painel de preparo](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Demonstração do preparo de conteúdo

Para saber mais sobre o preparo de conteúdo, assista a este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3412505?quality=12&learn=on&captions=por_br)

## Solução de problemas de recursos

Para obter ajuda com a solução de problemas de preparo de conteúdo, consulte os seguintes artigos da Base de Dados de Conhecimento de Suporte do [!DNL Commerce]:

- [Erro 404 em todas as páginas devido ao problema de preparo de conteúdo](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html?lang=pt-BR)
- [Atualizações agendadas de preparo de conteúdo não exibidas com o cache obsoleto do Fastly](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html?lang=pt-BR)
- [Posso agendar atualizações de Armazenamento Temporário de Conteúdo para preços em um catálogo compartilhado?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html?lang=pt-BR)
