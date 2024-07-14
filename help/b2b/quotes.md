---
title: Cotações Negociáveis
description: Saiba mais sobre os fluxos de trabalho de cotação e como você pode fornecer esse serviço para as contas da sua empresa.
exl-id: c278818b-fa5a-4e7a-8ca2-c4b757da4f05
feature: B2B, Quotes
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Cotações Negociáveis

Compradores e vendedores usam Cotações para gerenciar o processo de negociação de itens de adição de uma ordem, atualização de quantidades, solicitação e aplicação de descontos, etc., até chegarem a um acordo. O processo de negociação de cota pode ser iniciado por um comprador autorizado da empresa ou por um representante de vendas da empresa.

As cotações podem ser iniciadas por um comprador autorizado da empresa ou um representante de vendas. Depois que a cota é criada, o processo de negociação começa quando o comprador ou vendedor submete a cota para revisão. A grade _Quotes_, que lista cada cotação recebida e mantém um histórico da comunicação entre comprador e vendedor. Use os [controles do local de trabalho](../getting-started/admin-workspace.md) padrão para filtrar a lista, alterar o layout da coluna, salvar exibições e exportar dados.

- Na loja, os compradores enviam a cotação como uma [solicitação para negociar](quote-price-negotiation.md) o preço do carrinho de compras. Ao criar a solicitação de cota, um comprador pode salvar a cota como uma preliminar ou submetê-la diretamente ao vendedor.

- No Administrador, os representantes de vendas podem criar cotações em nome do comprador da empresa. Ao criar a cota, um vendedor pode salvá-la como uma preliminar ou submetê-la diretamente ao comprador para iniciar o processo de negociação.

Durante o processo de negociação, a cota só pode ser atualizada pela pessoa que revisa e propõe os termos para negociação adicional.

## Pré-requisitos

As cotas negociáveis estarão disponíveis somente se o Adobe Commerce tiver as seguintes definições de configuração:

- [A extensão B2B do Adobe Commerce está instalada](install.md)
- [Recursos B2B configurados](enable-basic-features.md)
   - Habilitar contas da empresa
   - Ativar cotação B2B

## Fluxo de trabalho de cotação

As cotações podem ser iniciadas pelo comprador ou pelo vendedor.

**Etapa 1: Criação da cotação**

- **O comprador solicita uma cotação** - O comprador [solicita uma cotação](quote-request.md) do carrinho de compras. A solicitação aparece na lista _Minhas Cotações_ no painel de conta do comprador e a notificação por email é enviada ao representante de vendas atribuído à conta da empresa. No Administrador, a solicitação aparece na grade _Aspas_, com o status `New`. Uma solicitação de cotação pode ser modificada pelo comprador até que seja aberta pelo vendedor.

  ![Cotas](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}


- **Representante de vendas** — Um Representante de Vendas pode [criar uma cotação](sales-rep-initiates-quote.md) do Administrador em nome de um comprador específico da empresa. O Representante de Vendas deve atualizar a cota para adicionar produtos e outras informações, como descontos e notas ao comprador. A Representação de Vendas pode salvar a cotação como um `draft` ou enviá-la ao comprador para iniciar a negociação. No estado de rascunho, a cotação é visível somente para o vendedor. Depois que a cotação é enviada, o status é `Submitted`. Ele não pode ser modificado pelo vendedor até que o comprador o envie de volta.

  ![Vendedor que inicia uma cotação de comprador a partir da grade Cotações no Administrador](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}


**Etapa 2: revisão e negociação da cotação**

**O vendedor exibe a solicitação e envia a resposta** - No Administrador, o vendedor exibe a solicitação de cotação. O status da cotação muda para `Pending`, e o comprador não pode fazer nenhuma alteração. O [vendedor responde](quote-price-negotiation.md) oferecendo preços com desconto para os produtos na cotação, insere um comentário e envia a cotação de volta ao comprador. O comprador e o representante de vendas são notificados por e-mail de que o vendedor respondeu.

**O comprador visualiza a cotação do vendedor e envia a resposta** - O comprador clica no link na notificação por email para abrir a cotação ou abre a cotação na página _Minhas Cotações_ do painel de conta. O comprador pode deixar notas ao vendedor no nível do item de linha ou da cota e remover itens.

O comprador e o vendedor podem continuar o processo de negociação até que um acordo seja alcançado ou o vendedor recuse a cotação. Se o comprador fizer alterações na cotação, como adicionar ou remover produtos ou alterar quantidades de produtos, a cotação deverá ser devolvida ao vendedor para revisão.

**Etapa 4: O comprador aceita a cotação** - O comprador aceita o preço proposto e continua a finalizar a compra. Descontos adicionais não podem ser adicionados à cotação negociada.

## Recursos da função B2B para cotações de armazenamento

As opções de configuração para cotações são controladas usando os [recursos de função](../systems/permissions-user-roles.md#role-resources). Esses recursos de função devem ser definidos para a função de usuário Administrador atribuída ao administrador de armazenamento.

Para conceder acesso às funções de cotação no Administrador, vá para **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, selecione a função e navegue até [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] na árvore_ Recursos de Função _.

## Aplicar uma ação

No Admin, os Administradores e Vendedores B2B podem gerenciar cotações da Grade de Cotações usando o menu [!UICONTROL Actions].

![Cotas](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

1. Na primeira coluna da grade, marque a caixa de seleção de cada registro ao qual deseja aplicar a ação.

1. Em **[!UICONTROL Actions]**, selecione a ação a ser aplicada.

### Exibir uma cotação

1. Na coluna **[!UICONTROL Actions]** de um registro, clique em **[!UICONTROL View]**.

1. Para responder à solicitação do cliente, siga as instruções e inicie o processo [negociação de preço](quote-price-negotiation.md).

### Exibir atividade de cotação

Exibir a linha do tempo da negociação, a comunicação e outras atividades de cotação do [!UICONTROL Comments] e do [!UICONTROL History Log]—as informações incluem alterações de status, atualizações de informações de cliente e de remessa, atualizações de itens e preços e outras informações importantes.

1. Abra uma cotação.

1. Exiba os comentários e o histórico da negociação de cotações rolando até **[!UICONTROL Negotiation]** e selecionando **[!UICONTROL Comments]** e **[!UICONTROL History Log]**.

   ![Exibir Histórico](./assets/quote-view-history.png){width="400"}

1. O histórico também é rastreado no nível do item de linha.

   ![Exibir Histórico do Item de Linha](./assets/quote-view-line-item-history.png){width="400"}


### Recusar uma solicitação de cotação

Somente solicitações de cotação com status `Open` podem ser recusadas.

1. Selecione cada solicitação de cotação em aberto que você deseja recusar.

1. Defina o controle _[!UICONTROL Actions]_como `Declined`.

1. Quando solicitado, insira o motivo da recusa da cotação e clique em **[!UICONTROL Confirm]**.

   ![Recusar Cotação?](./assets/quote-decline-confirm.png){width="400"}


## Descrições da coluna

| Coluna | Descrição |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Para selecionar as aspas que estarão sujeitas a uma ação, marque a caixa de seleção ou use o controle de seleção no cabeçalho da coluna. Opções: Selecionar Tudo / Desmarcar Tudo |
| [!UICONTROL ID] | Um identificador numérico exclusivo que é atribuído quando uma solicitação de cotação é enviada do carrinho de compras de um comprador. Ao visualizar o detalhe da cotação, a ID aparece na parte superior da página, em vez do nome da cotação. |
| [!UICONTROL Name] | O nome atribuído a uma solicitação de cotação pelo comprador. |
| [!UICONTROL Created Date] | A data e a hora em que o comprador submeteu pela primeira vez a solicitação de uma cotação. |
| [!UICONTROL Company] | O nome da empresa em nome da qual um comprador envia uma solicitação de cotação. |
| [!UICONTROL Submitted By] | O nome e sobrenome do comprador da empresa que envia uma solicitação de cotação. |
| [!UICONTROL Last Updated] | A data e hora da última comunicação entre comprador e vendedor em relação à cotação. |
| [!UICONTROL Sales Rep] | O nome e sobrenome do representante de vendas que gerencia a conta do comprador. |
| [!UICONTROL Quote Total (Base)] | O preço total dos produtos a serem comprados com base na cotação original. O valor total aparece na moeda base do site e na moeda da loja. |
| [!UICONTROL Quote Total (Negotiated)] | O preço total dos produtos a serem comprados com base na cotação negociada. Esse total é calculado automaticamente pelo sistema e inclui qualquer item de linha ou descontos no nível da cotação aplicados pelo vendedor. O valor total aparece na moeda base do site e na moeda da loja. |
| [!UICONTROL Status] | Indica o estado atual de uma solicitação de cotação. O status de uma cotação só pode ser alterado por ação por parte do comprador ou do vendedor. Consulte também as configurações de Status da [conta do comprador](account-dashboard-my-quotes.md).<ul><li>**[!UICONTROL New]** - O comprador enviou uma solicitação de cotação, mas ela não foi visualizada pelo vendedor. A solicitação pode ser atualizada pelo comprador até que seja aberta pelo vendedor.</li><li>**[!UICONTROL Draft]** - O vendedor cria uma cotação de rascunho para um comprador. A cotação não é visível para o comprador até que o vendedor adicione os detalhes da oferta (itens, quantidade, desconto e assim por diante) e envie a cotação para o comprador.</li> <li>**[!UICONTROL Open]** - O vendedor abriu a solicitação e está em processo de revisá-la e preparar uma resposta. </li><li>**[!UICONTROL Submitted]** - O vendedor enviou uma resposta ao comprador. O registro de cota não pode ser editado durante o processo de negociação.</li><li>**[!UICONTROL Client Reviewed]** - O comprador visualizou a resposta do vendedor e está preparando uma resposta.</li><li>**[!UICONTROL Updated]** - O comprador enviou uma resposta, mas ela não foi visualizada pelo vendedor.</li><li>**[!UICONTROL Ordered]** - O comprador enviou a ordem com base na cotação negociada.</li><li>**[!UICONTROL Closed]** - O comprador cancelou a solicitação de cotação.</li><li>**[!UICONTROL Declined]** - O vendedor recusou a solicitação de cotação. Qualquer preço personalizado é removido da cotação e o registro é bloqueado para novas edições.</li><li>**[!UICONTROL Expired]** - O comprador não respondeu à resposta do vendedor dentro do período de tempo designado e a cotação não é mais válida.</li></ul> |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Abre a solicitação de cotação e mantém um registro da negociação entre comprador e vendedor. |

{style="table-layout:auto"}

## Barra de botões

| Botão | Descrição |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Send] | Envia a cotação atualizada como uma resposta à consulta do comprador. Esse botão será desativado se o vendedor estiver aguardando uma resposta do comprador. |
| [!UICONTROL Back] | Retorna à página _Cotações_ sem salvar as alterações. |
| [!UICONTROL Create Copy] | [!BADGE 1.5.0-beta capabilities]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Disponível somente para participantes do programa Beta&quot;} Crie uma nova cotação a partir da cotação atual copiando-a e renomeando-a. Quando as novas aspas são abertas, o nome padrão é `<original quote name> (copy)`. Altere o nome editando o valor no campo [!UICONTROL Name] e salvando a cotação como rascunho. |
| [!UICONTROL Print] | Envia a cotação para uma impressora ou a salva como um arquivo PDF. |
| [!UICONTROL Create a copy] | Cria uma cópia da cotação denominada `<original quote name> (copy)` e a abre. Renomeie e atualize a nova cotação conforme necessário antes de salvá-la como rascunho ou enviá-la ao comprador. |
| [!UICONTROL Save as Draft] | Salva quaisquer alterações feitas na cotação, mas não a envia de volta ao comprador. |
| [!UICONTROL Decline] | Rejeita o pedido de negociação de preços, quer no inquérito inicial, quer durante as negociações em curso. Quando uma cotação é recusada, o vendedor deve adicionar um comentário para explicar a decisão. Quando uma cotação é recusada, todos os preços negociados são redefinidos para os valores originais. Esse botão é desativado enquanto o vendedor aguarda uma resposta do comprador. |

{style="table-layout:auto"}

## Exemplo de citação

A figura a seguir mostra um exemplo da visualização detalhada da cotação no Administrador com algumas configurações definidas.

![Exemplo de citação](./assets/quote-full.png){width="700" zoomable="yes"}


>[!NOTE]
>
>[!BADGE 1.5.0-recursos beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponível somente para participantes do programa Beta"}
