---
title: Casos de uso e fluxos de trabalho do modelo de cotação
description: Crie um modelo de cota a partir de uma cota existente para simplificar a negociação de cota para ordens repetitivas.
feature: B2B, Quotes
source-git-commit: 3000d9abab467a86e37c7eca6e7db16b39c763ab
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# Fluxos de trabalho e caso de uso de modelos de cotação

O recurso Modelo de Cota permite que compradores e vendedores simplifiquem o processo de cota criando modelos de cota reutilizáveis e personalizáveis.

- **Cotações Personalizáveis** — Os compradores podem gerar cotações vinculadas a partir de um modelo pré-aprovado, permitindo a personalização dentro de parâmetros especificados, como quantidades e seleções de itens de linha.
- **Limites de Pedidos**—Os vendedores podem definir compromissos de pedidos mínimos e máximos, garantindo que os compradores adiram aos volumes de compras acordados.
- **Datas de Expiração** — Os modelos podem ter períodos de validade, garantindo que os termos sejam aplicáveis somente dentro de um período especificado.
- **Descontos e Preços**- Os vendedores podem usar os mesmos recursos de item de linha, nível de cota e desconto de preço de remessa disponíveis com cotas para definir descontos para ordens recorrentes, simplificando o processo de negociação.
- **Rastreamento e Relatórios** — O sistema rastreia o número de cotações vinculadas geradas a partir do modelo e conclui com êxito os pedidos para fornecer insights sobre o cumprimento das cotas de pedidos acordadas.

## Caso de uso

Um comprador de uma empresa pode usar um modelo de cota para solicitar um conjunto específico de produtos durante um período. O comprador configura as seguintes opções de modelo de cotação para tornar o processo de cotação mais eficiente, consistente e alinhado aos acordos de compra estratégicos.

- Limite de ordem para especificar o número mínimo e máximo de ordens qualificadas para precificação negociada. Isso pode ser usado para aplicar e rastrear cotas de pedido especificadas em contratos.

- Limites de quantidade (quantidades mínimas/máximas) O modelo especifica um limite de quantidade para definir a quantidade mínima e máxima que pode ser comprada para cada ordem, garantindo que o vendedor possa gerenciar efetivamente os níveis de estoque e, ao mesmo tempo, fornecendo ao comprador a flexibilidade para ajustar as quantidades conforme necessário.

## Fluxo de trabalho do modelo de cotação

Os modelos de cota podem ser iniciados pelo comprador ou pelo vendedor.

**Etapa 1: Criação do modelo de cotação (Novo)**

- **O comprador cria o modelo de cotação**

  Ao revisar um modelo de cota existente, o comprador decide que a empresa precisa enviar várias ordens durante o próximo ano e deseja solicitar descontos adicionais com base nos negócios repetidos. Eles criam um modelo de citação usando a ação *[!UICONTROL Create quote template]* na citação. Em seguida, eles iniciam a negociação enviando o novo modelo ao vendedor para revisão.

  Os compradores também podem criar um modelo de cotação diretamente da página *[!UICONTROL My Quote Templates]** na loja.

- **Representante de vendas** — Um Representante de Vendas pode criar um modelo de cotação do Administrador em nome de um comprador específico da empresa. O Representante de Vendas pode criar o modelo de cotação no Administrador a partir de uma cotação existente ou da grade [!UICONTROL Quote Templates] e salvá-lo como `draft` ou enviá-lo ao comprador para iniciar a negociação. No estado de rascunho, a cotação é visível somente para o vendedor. Depois que a cotação é enviada, o status é `Submitted`. Ele não pode ser modificado pelo vendedor até que o comprador o envie de volta.

  ![Vendedor que inicia uma cotação de comprador a partir da grade Cotações no Administrador](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

**Etapa 2: revisão e negociação da cotação (revisão)**

Revisar ou negociar um modelo de cota pode incluir alterar quantidades, remover itens, adicionar comentários de item de linha, aplicar descontos de item de linha ou de cota (vendedor) e adicionar um endereço de entrega (comprador).

- **O vendedor exibe a solicitação e envia a resposta** - No Administrador, o vendedor exibe o modelo de cotação da grade *[!UICONTROL Quote Templates]** ou o abre a partir do link na notificação por email. Na loja, o status da cotação muda para `Pending`, e o comprador não pode fazer nenhuma alteração. Seguindo o mesmo processo para [negociação de cota](quote-price-negotiation.md), o vendedor responde oferecendo descontos de preço e ajustando quantidades e itens conforme necessário, insere um comentário e envia a cota de volta ao comprador. O comprador e o representante de vendas são notificados por e-mail de que o vendedor respondeu.

- **O comprador visualiza o modelo de cotação do vendedor e envia a resposta** - O comprador clica no link da notificação por email para abrir o modelo de cotação ou abre a cotação da página _Meus Modelos de Cotação_ do painel de conta. O comprador pode deixar notas ao vendedor no nível do item de linha ou da cota, alterar quantidades e remover itens.

O comprador e o vendedor continuam o processo de negociação até que um acordo seja alcançado ou o vendedor recuse o modelo de cota. Se o comprador fizer alterações na cotação, como adicionar ou remover produtos ou alterar quantidades de produtos, a cotação deverá ser devolvida ao vendedor para revisão.

- **O comprador adiciona um endereço de entrega** - O comprador deverá adicionar um endereço de entrega ao modelo de cotação se não tiver um. Depois que o comprador adicionar o endereço, o vendedor poderá fornecer opções de envio e entrega. Os métodos de envio mostrados dependem da configuração da Storefront.

Se o comprador adicionar um endereço de entrega, o acordo de negociação deverá ser revisado e o vendedor poderá continuar o processo de negociação até que um acordo seja alcançado ou o vendedor recuse o modelo de cota.

**Etapa 3: o comprador aceita o modelo de cotação**

O comprador aceita as condições negociadas no modelo. Depois que o modelo de cota for aceito, o comprador poderá usá-lo para gerar cotas vinculadas e pré-aprovadas que possam ser usadas para submeter ordens sem exigir negociação adicional.

As opções de envio são bloqueadas no check-out.

### Exibir um modelo de cotação

1. Na coluna **[!UICONTROL Actions]** de um registro, clique em **[!UICONTROL View]**.

1. Para responder à solicitação do cliente, siga as instruções e inicie o mesmo processo de [negociação de preço](quote-price-negotiation.md) usado para negociar cotações.

### Exibir atividade de modelo de cotação

Exibir a linha do tempo da negociação, a comunicação e outras atividades de cotação do [!UICONTROL Comments] e do [!UICONTROL History Log]—as informações incluem alterações de status, atualizações de informações de cliente e de remessa, atualizações de itens e preços e outras informações importantes.

1. Abra um modelo de cotação.

1. Exiba os comentários e o histórico da negociação de cotações rolando até **[!UICONTROL Negotiation]** e selecionando **[!UICONTROL Comments]** e **[!UICONTROL History Log]**.

   ![Exibir Histórico](./assets/quote-view-history.png){width="400"}

1. O histórico também é rastreado no nível do item de linha.

   ![Exibir Histórico do Item de Linha](./assets/quote-view-line-item-history.png){width="400"}


### Recusar um modelo de cotação

Somente modelos de cotação com status `In Review` podem ser recusados.

1. Na grade *[!UICONTROL Quote Templates]*, abra o modelo de cotação que deseja recusar.

1. No modelo de citação, clique em **[!UICONTROL Decline]**.

1. Quando solicitado, insira o motivo da recusa da cotação e clique em **[!UICONTROL Confirm]**.
