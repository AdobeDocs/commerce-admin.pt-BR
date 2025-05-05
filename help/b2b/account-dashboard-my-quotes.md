---
title: '[!UICONTROL My Quotes]'
description: Saiba mais sobre a experiência do cliente para cotações, que está disponível no painel de conta.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 6cf53c7caf37c24be473afecfba829595c14cb8c
workflow-type: tm+mt
source-wordcount: '1220'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Se as cotações estiverem habilitadas, a seção _[!UICONTROL My Quotes]_&#x200B;do painel da conta do cliente listará todas as cotações enviadas pelo cliente. Dependendo das permissões, somente os compradores que fazem compras em nome de uma empresa podem enviar solicitações para negociar o preço de uma compra.

![Minhas Cotações](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

O comprador inicia o processo [enviando uma solicitação](quote-request.md) de cotação do carrinho de compras. O email é trocado entre o comprador e o vendedor durante o [processo de negociação](quote-price-negotiation.md). Para o comprador, a página [!UICONTROL My Quotes] é o ponto focal para toda a comunicação entre comprador e vendedor durante o processo de negociação. Um comprador que aceita o preço negociado oferecido pelo vendedor pode prosseguir diretamente para a página de check-out a partir da cotação. Descontos adicionais não podem ser adicionados à cotação negociada.

Ao negociar uma cota, um comprador tem várias opções para gerenciar a cota ou atualizar os detalhes da cota.

* Ações relacionadas ao gerenciamento da cotação:

   * Criar uma cópia da cotação
   * Fechar a cotação
   * Excluir a cotação
   * Renomear a cotação
   * Imprimir a cotação
   * Criar um modelo

* Ações para atualizar detalhes da cotação:

   * Revisar preços e atualizações de itens
   * Rastrear o processo de negociação das seções [!UICONTROL Comments] e [!UICONTROL History]
   * Modificar a cotação para remover itens
   * Comunicar e negociar com o vendedor adicionando notas no nível do item de linha e da cotação
   * Adicionar um endereço de entrega
   * Mover itens de linha para uma lista de requisições
   * Converter a cotação em um pedido se os termos forem aceitáveis

* Ações gerais durante a negociação:

   * Enviar cotação ao vendedor para revisão
   * Prosseguir para o check-out

O exemplo a seguir mostra uma cotação que foi atualizada pelo comprador e enviada de volta ao vendedor para revisão.


![Exibição da cotação pelo comprador](./assets/account-dashboard-my-quote-detailed.png){width="700" zoomable="yes"}

Cotações com o status `Updated` são bloqueadas até que o vendedor retorne a cotação.

## Mostrar aspas

Com as [permissões necessárias para sua função](account-company-roles-permissions.md), os compradores associados a uma conta da empresa podem ver as cotações solicitadas pelos [usuários subordinados](account-company-structure.md). Os administradores da empresa podem visualizar todas as cotações da conta da empresa.

1. O comprador faz logon em sua conta na loja.

1. Clica em **[!UICONTROL My Quotes]** na navegação à esquerda.

1. Para ver todas as cotações criadas, clique no link **[!UICONTROL Show My Quotes]** (exibido apenas para o administrador da empresa ou conta com usuários subordinados).

1. Para ver todas as cotações de todos os usuários da empresa, clique em **[!UICONTROL Show All Quotes]**.

## Exibir uma cotação

1. O comprador faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL My Quotes]**.

1. Localiza a aspa na lista e clica em **[!UICONTROL View]** na coluna _[!UICONTROL Action]_.

## Copiar uma cotação

1. O comprador faz logon na conta da empresa na loja.

1. No painel esquerdo, escolhe **[!UICONTROL My Quotes]**.

1. Localize e acesse a cotação desejada na lista e clique em **[!UICONTROL Create Copy]** na cotação original.

## Criar modelo

1. O comprador faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL My Quote Templates]**.

1. Localiza a aspa na lista **[!UICONTROL My Quotes]** e clica em **[!UICONTROL Create Quote Template]** na coluna _[!UICONTROL Action]_.

## Mover itens de linha de uma cotação para uma lista de requisições

1. O comprador faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL My Quotes]**.

1. Localize e acesse a cotação desejada na lista.

1. Selecione os itens de linha.

1. Clique em **[!UICONTROL Move to Requisition list]** na lista suspensa _[!UICONTROL Actions]_.

1. Selecione uma lista de requisições existente para mover os itens selecionados.

1. Clique em **[!UICONTROL Move item]**.

Consulte [Adicionar produtos a uma lista de requisições](requisition-lists.md) para saber mais sobre este processo.

>[!NOTE]
>
> Você não pode criar uma nova lista de requisições ao mover itens. Os itens só podem ser movidos para uma lista de requisições existente.

## Mover itens de linha para uma nova cotação

1. O comprador faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL My Quotes]**.

1. Localize e acesse a cotação desejada na lista.

1. Selecione os itens de linha.

1. Clique em **[!UICONTROL Move item to new quote]** na lista suspensa _[!UICONTROL Actions]_.

1. Nomeie a nova cotação na modal.

1. Selecione **[!UICONTROL Move to quote]** para mover o item selecionado para a nova cotação.

>[!NOTE]
>
> Ao selecionar vários itens, o modal é exibido como **[!UICONTROL Move selected items to new quote]**.

## Adição de um endereço de entrega

1. O comprador faz logon em sua conta.

1. No painel esquerdo, escolhe **[!UICONTROL My Quotes]**.

1. Seleciona a cotação desejada.

1. Na seção **[!UICONTROL Shipping Information]**, clique em **[!UICONTROL Add New Address]**.

1. Preenche detalhes do novo endereço.

1. Cliques **[!UICONTROL Save Address]**.

Quando o comprador adiciona o endereço, o vendedor fornece as opções de envio e entrega. Essas atualizações podem afetar o preço da cotação negociada. As opções de envio são bloqueadas no check-out.

## Imprimir uma cotação

1. Na cotação aberta à direita da seção _[!UICONTROL Items Quoted]_, o comprador clica em **[!UICONTROL Print]**.

1. Verifica o **[!UICONTROL Destination]** como uma impressora ou PDF.

1. Cliques **[!UICONTROL Print]**.

## Cancelar uma solicitação de orçamento

1. Na aspa aberta logo acima da seção Itens entre Aspas, clique em **[!UICONTROL Close quote]**.

   A solicitação foi cancelada e o status da cotação muda para `Closed`. A cotação fechada permanece na lista de cotações e permanece listada na grade _[!UICONTROL Quotes]_&#x200B;do Administrador.

1. Para remover a cotação cancelada da lista de cotações, clique em **[!UICONTROL Delete]**.

1. Quando for solicitada a confirmação, clique em **[!UICONTROL OK]**.

   A cotação fechada é removida da lista de cotações. No entanto, ela permanece listada na grade _[!UICONTROL Quotes]_&#x200B;no Administrador, com o status `Closed`.

## Ações da Cotação

| Ação | Descrição |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Renomear | Alterar o nome da cotação |
| Criar cópia | Um comprador pode criar uma cotação a partir da cotação atual copiando-a e renomeando-a. |
| Fechar cotação | Depois que um comprador fecha uma cotação, ela não pode ser reaberta. Se necessário, o comprador pode recriá-lo usando a ação [!UICONTROL Create Copy]. Esta opção não estará disponível se o status da cotação for `Draft`. |
| Criar modelo | Criar um modelo de cotação com base na cotação atual. Os modelos de cota otimizam a negociação de cota permitindo que compradores e vendedores concordem sobre os termos do contrato e da precificação que podem ser aplicados a várias cotas.  Mediante acordo, o comprador pode gerar uma cota vinculada e pré-aprovada a partir do modelo para ordens subsequentes, em vez de reiniciar o processo de solicitação de cotação (SDC). |
| Excluir cotação | Quando um comprador exclui uma cotação, ela é removida do sistema e não está mais disponível. |
| Imprimir | Abre um formulário de impressão para salvar a cotação como um PDF, arquivo ou imprimi-la em uma impressora configurada. |

## Descrições da coluna

| Coluna | Descrição |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | O nome atribuído à solicitação de cotação pelo comprador. |
| [!UICONTROL Created] | A data em que a solicitação de cotação foi enviada pela primeira vez. |
| [!UICONTROL Created By] | O nome e sobrenome do comprador que submeteu a solicitação de cotação. |
| [!UICONTROL Status] | Indica o status da cotação. O status de uma cotação só pode ser alterado por ação por parte do comprador ou do vendedor. <br/>**[!UICONTROL Submitted]**- A solicitação de cotação do comprador ainda não foi aberta pelo vendedor. Enquanto estiver nesse estado, o comprador ainda poderá modificar a solicitação de uma cotação. Ações disponíveis: `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - O vendedor abriu a solicitação e está em processo de analisá-la e preparar uma resposta. Ações disponíveis: `View` / `Close` <br/>**[!UICONTROL Updated]**- O vendedor enviou uma resposta ao comprador e o botão _[!UICONTROL Proceed to Checkout]_&#x200B;está habilitado. Enquanto estiver nesse estado, o comprador poderá continuar modificando a cotação. Ações disponíveis: `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- O comprador ainda está atualizando a cotação e o botão&#x200B;_[!UICONTROL Proceed to Checkout]_ está desabilitado. Ações disponíveis: `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- O comprador enviou um pedido com base na cotação negociada. A cotação está bloqueada e não pode ser editada. Ação disponível: Exibição<br/>**[!UICONTROL Closed]** - O comprador finalizou a negociação e cancela a cotação. A cotação está bloqueada e não pode ser editada pelo comprador ou vendedor. Ações disponíveis: `View` / `Delete` <br/>**[!UICONTROL Declined]**- O vendedor recusou a solicitação de cotação ou fez uma alteração proposta durante o processo de negociação. Uma cotação pode ser recusada em qualquer estágio do workflow. Qualquer preço personalizado é removido da cotação. O comprador pode continuar editando a cota e ressubmetê-la, ou fazer a compra com preços de catálogo padrão. Ações disponíveis: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - O tempo de vida da cotação expirou. Os preços propostos são redefinidos. O comprador pode concluir a compra com base nos preços de catálogo padrão ou iniciar outra rodada de negociações. Ações disponíveis: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
