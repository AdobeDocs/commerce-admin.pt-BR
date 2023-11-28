---
title: Preparo de conteúdo
description: O armazenamento temporário de conteúdo oferece à sua equipe de negócios a capacidade de criar, visualizar e agendar facilmente uma grande variedade de atualizações de conteúdo para sua loja diretamente do administrador.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Preparo de conteúdo

{{ee-feature}}

O armazenamento temporário de conteúdo oferece à sua equipe de negócios a capacidade de criar, visualizar e agendar facilmente uma grande variedade de atualizações de conteúdo para sua loja diretamente do _Admin_. Por exemplo, em vez de pensar em termos de uma página estática, considere uma página como uma coleção de diferentes elementos que podem ser transformados _em_ ou _desligado_ com base em um agendamento. Você pode usar o preparo de conteúdo para criar uma página que muda automaticamente durante o ano em um agendamento.

O termo _campaign_ refere-se ao registro de uma alteração agendada ou a uma coleção de alterações gerenciadas no Painel de Preparo. As alterações podem ser visualizadas em um calendário ou linha do tempo. Os termos _alteração agendada_ e _atualização programada_ são intercambiáveis e se referem a uma única alteração.

Quando você agenda uma alteração de conteúdo por um período específico, o conteúdo é revertido para a versão anterior quando a alteração agendada expira. Você pode criar várias versões do mesmo conteúdo de linha de base a ser usado para atualizações futuras. Você também pode voltar atrás na linha do tempo para visualizar versões anteriores do conteúdo. Para salvar uma versão de rascunho, basta atribuir uma data na linha do tempo que está tão distante no futuro que ela nunca entra em produção.

## Campanhas e objetos de preparo de conteúdo

Quando uma nova atualização programada é criada para qualquer um dos seguintes objetos, uma campanha correspondente é criada como um espaço reservado e a variável _[!UICONTROL Scheduled Changes]_aparecerá na parte superior da página. A campanha de espaço reservado tem uma data inicial, mas não uma data final. Você pode agendar atualizações no conteúdo como parte de uma campanha, bem como pré-visualizar e compartilhar as alterações por data, hora ou exibição de loja. Depois que uma nova campanha é criada para um objeto, você pode atribuí-la como uma atualização programada para outros objetos.

- [Produtos](../catalog/product-scheduled-changes.md)
- [Categorias](../catalog/category-scheduled-changes.md)
- [Regras de preço de catálogo](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Regras de preço do carrinho](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [Páginas CMS](pages-workspace.md#scheduled-changes)
- [Blocos CMS](blocks.md)

## Fluxo de trabalho de preparo de conteúdo

1. **Criar o conteúdo da linha de base**

   A linha de base é o conteúdo de um ativo sem uma campanha e inclui tudo abaixo de _[!UICONTROL Scheduled Changes]_na parte superior da página. O conteúdo da linha de base é sempre usado, a menos que haja uma campanha ativa com alterações programadas para esse local na linha do tempo.

1. **Criar a primeira campanha**

   Crie sua primeira campanha com as datas de início e término conforme necessário. Para tornar a campanha aberta, deixe a data final em branco. Quando a primeira campanha terminar, o conteúdo original da linha de base será restaurado.

   >[!NOTE]
   >
   >A data de início e a data de término da campanha devem ser definidas usando o **_padrão_** Fuso horário do administrador, que é convertido do fuso horário local de cada site. Considere um exemplo em que você tem vários sites em fusos horários diferentes, mas deseja iniciar uma campanha com base em um fuso horário dos EUA. Nesse caso, você deve agendar uma atualização separada para cada fuso horário local e definir **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** no fuso horário convertido de cada site local para o fuso horário padrão do Administrador.

1. **Adicionar uma segunda campanha**

   Crie a segunda campanha, com as datas de início e término conforme necessário. A segunda campanha pode ser atribuída a um período totalmente diferente. Ao criar várias campanhas para o mesmo ativo, as campanhas não podem se sobrepor. Você pode criar quantas campanhas forem necessárias.

   >[!NOTE]
   >
   >Todas as atualizações programadas são aplicadas consecutivamente, o que significa que qualquer entidade pode ter apenas uma atualização programada de cada vez. Qualquer atualização agendada é aplicada a todas as exibições de loja dentro de seu período de tempo. Como resultado, uma entidade não pode ter uma atualização agendada diferente para diferentes exibições de loja ao mesmo tempo. Todos os valores de atributo de entidade em todas as exibições de armazenamento, que não são afetados pela atualização agendada atual, são obtidos dos valores padrão, e não da atualização agendada anterior.

1. **Restaurar o conteúdo da linha de base**

   Se todas as campanhas tiverem datas de término, o conteúdo da linha de base será restaurado sempre que todas as campanhas ativas terminarem.

>[!NOTE]
>
>Enquanto uma atualização por preparo está ativa para uma entidade, editar a entidade está editando a atualização de preparo ativa atual. Isso não afeta o conteúdo de linha de base, que é restaurado quando a atualização de preparo termina.

## [!UICONTROL Content Staging] painel

A variável [!UICONTROL Content Staging] [painel](content-staging-dashboard.md) oferece visibilidade de todas as alterações e atualizações planejadas do site. Qualquer dia, intervalo de datas ou período de uma campanha pode ser visualizado e compartilhado com outras pessoas.

![Painel de preparo](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Demonstração do preparo de conteúdo

Para saber mais sobre o preparo de conteúdo, assista a este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12)

## Solução de problemas de recursos

Para obter ajuda com a solução de problemas de preparo de conteúdo, consulte o seguinte [!DNL Commerce] Artigos da Base de conhecimento de suporte:

- [Erro 404 em todas as páginas devido ao problema de preparo de conteúdo](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [Atualizações programadas do armazenamento temporário de conteúdo não são exibidas com o cache obsoleto do Fastly](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [Posso programar atualizações de Armazenamento temporário de conteúdo para preços em um catálogo compartilhado?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
