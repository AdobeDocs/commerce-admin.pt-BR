---
title: '[!UICONTROL My Quote Templates]'
description: Saiba mais sobre a experiência do cliente para modelos de cotação, que está disponível no painel de conta da loja.
feature: B2B, Companies, Quotes
exl-id: 3d95a44e-b874-442b-af96-0dc6b589d0f7
source-git-commit: 71b9326aa5a8c3d7656b3c0f166cf25291b2abba
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# [!UICONTROL My Quote Templates]

Se as cotações estiverem habilitadas, a seção _[!UICONTROL My Quotes Template]_do painel da conta do cliente listará todos os modelos de cotações associados à conta do cliente. Dependendo das permissões, somente os compradores que fazem compras em nome de uma empresa podem solicitar um modelo de cotação e negociar preços e condições de cotação para pedidos recorrentes.

![Meus Modelos de Cotação](./assets/account-dashboard-quote-templates-list.png){width="700" zoomable="yes"}

A lista de modelos de cotação organiza os modelos por status.

- **[!UICONTROL Active Quote Templates]** lista os modelos que foram negociados e aprovados para uso. As informações incluem cota mínima total e ordens feitas se essas opções tiverem sido configuradas durante o processo de negociação. Os compradores podem gerar uma cotação vinculada a partir do modelo para submeter uma ordem com base nas condições da cotação.

- **[!UICONTROL In Review]** lista modelos no processo de negociação mostrando o status atual e fornecendo um link para abrir o modelo.

- **[!UICONTROL Inactive]** lista modelos que expiraram, foram cancelados ou não são mais válidos porque um comprador esgotou o número permitido de ordens confirmadas.

Para o comprador, a página *[!UICONTROL My Quotes Templates]* é o ponto focal para toda a comunicação entre comprador e vendedor durante o processo de negociação.

Um comprador que aceita as condições negociadas oferecidas pelo vendedor pode aceitar o modelo e, em seguida, usá-lo para gerar cotações vinculadas pré-aprovadas que podem ser usadas para fazer pedidos.

- Ações relacionadas ao gerenciamento do modelo de cotação:

   - Cancelar um modelo
   - Enviar ao vendedor para revisão
   - Aceitar o modelo de cotação
   - Alterar a data de expiração do modelo de cotação
   - Adicionar um endereço de entrega

- Ações para atualizar detalhes do modelo de cota durante o processo de negociação:

   - Revisar preços e atualizações de itens.
   - Se os limites de quantidade tiverem sido configurados no modelo de cotação, ajuste os valores mínimo e máximo.
   - Rastreie o processo de negociação das seções [!UICONTROL Comments] e [!UICONTROL History].
   - Para modelos que ainda estão sendo revisados, o comprador pode modificar o modelo de cota removendo itens.
   - Comunique-se e negocie com o vendedor adicionando notas no nível de item de linha e cotação.

  Depois de fazer alterações, o comprador retorna o modelo ao vendedor para revisão.

- Ações gerais durante a negociação:

   - Enviar modelo de cotação ao vendedor para revisão
   - Aceitar o modelo de cotação
   - Cancelar para encerrar a negociação e fechar a cotação

O exemplo a seguir mostra um modelo de cotação que foi atualizado pelo comprador e enviado de volta ao vendedor para revisão.

![Exibição do comprador do modelo de cotação](./assets/account-dashboard-my-quote-template-detailed.png){width="700" zoomable="yes"}

Os modelos com o status `Submitted` são bloqueados até que o vendedor revise e atualize o modelo e retorne-o ao comprador.

## Criar um modelo de cotação

O comprador pode iniciar o processo de negociação do modelo de cota usando um dos seguintes métodos:

- Crie um modelo a partir de uma cotação existente clicando na ação **[!UICONTROL Create quote template]**.

- Envie uma solicitação de cotação da loja e adicione comentários solicitando ao representante de vendas que crie um modelo de cotação a partir da solicitação de cotação.

## Exibir um modelo de cotação

1. O comprador faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL My Quote Templates]**.

1. Localiza o modelo de citação na lista e clica em **[!UICONTROL View]** na coluna _[!UICONTROL Action]_.

## Adicionar um endereço de entrega

O comprador não pode aceitar um modelo de cotação até que ele tenha um endereço de entrega.

1. O comprador faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL My Quote Templates]**.

1. Seleciona o modelo de cotação desejado.

1. Na seção **[!UICONTROL Shipping Information]**, clique em **[!UICONTROL Add New Address]**.

1. Preenche detalhes do novo endereço.

1. Cliques **[!UICONTROL Save Address]**.

Depois que o comprador adiciona o endereço, ele envia o modelo de volta ao vendedor para revisão. O vendedor fornece as opções de envio e entrega. Essas atualizações podem afetar o preço da cotação negociada. As opções de envio são bloqueadas no check-out.

## Gerar uma cotação vinculada

Depois que o comprador aceitar um modelo de cotação, ele poderá usá-lo para gerar cotações vinculadas e pré-aprovadas do *[!UICONTROL My Quote Templates dashboard]* ou do modelo de cotação usando a ação **[!UICONTROL Generate a quote]**.

A cotação vinculada inclui uma notificação indicando que está aprovada e pronta para check-out. Ele também fornece um link para o modelo de cotação nas informações do cabeçalho.

![Aspas vinculadas geradas a partir de um modelo de cotação](./assets/quote-templates-linked-quote.png){width="700" zoomable="yes"}

Se o modelo de cotação foi configurado com um limite de pedido, a contagem é incrementada quando a cotação vinculada é gerada.

Os compradores podem concluir as seguintes ações a partir de uma cota vinculada:

- Se a cota estiver configurada com limites de quantidade, ajuste a quantidade da ordem para os itens de linha.
- Prossiga para o check-out para enviar um pedido.
- Excluir ou imprimir a cotação.
- Abrir o modelo de cotação usado para gerar a cotação.

## Cancelar um modelo de cotação

Na página de modelo de citação, clique em **[!UICONTROL Cancel Quote Template]**.

O modelo de cotação é cancelado, e o status da cotação muda para `Closed`. A cotação fechada permanece na lista de *[!UICONTROL Inactive]* cotações e permanece na grade _[!UICONTROL Quote Templates]_do Administrador.
