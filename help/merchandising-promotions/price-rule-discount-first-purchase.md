---
title: Exemplo de regra de preço do carrinho - desconto com a primeira compra
description: Analise um exemplo de uso de uma regra de preço de carrinho para oferecer um desconto a clientes pela primeira vez.
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Exemplo de regra de preço do carrinho - desconto com a primeira compra

{{ee-feature}}

As regras de preço do carrinho podem ser usadas para oferecer automaticamente um desconto aos clientes na primeira compra, sem a necessidade de um cupom.

Para oferecer um desconto direcionado para clientes pela primeira vez, é possível:

- Crie um segmento de cliente definido como _compradores sem pedidos_ e depois
- Crie uma regra de preço do carrinho que segmente o novo segmento de cliente.

>[!NOTE]
>
>Certifique-se de que o recurso Segmentos do cliente esteja ativado. Consulte [Criar um segmento de cliente](../customers/customer-segment-create.md).

## Etapa 1. Criar um segmento de cliente

1. No _Admin_ barra lateral, vá para **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. No canto superior direito, clique em **[!UICONTROL Add Segment]**.

1. Defina o **[!UICONTROL General Properties]**.

   - Insira um **[!UICONTROL Segment Name]** para identificar o segmento do cliente (Exemplo: _Cliente de primeira vez_).

   - Para **[!UICONTROL Assigned to Website]**, selecione o site onde o segmento do cliente pode ser usado.

   - Para **[!UICONTROL Status]**, selecione `Active`.

   - Para **[!UICONTROL Apply to]**, selecione `Visitors and Registered Customers`.

   - Quando terminar, clique em **[!UICONTROL Save and Continue Edit]**.

     Opções adicionais ficam disponíveis no painel à esquerda.

   ![Propriedades do segmento do cliente](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. Defina o **[!UICONTROL Conditions]**.

   Neste exemplo, a condição destina-se a clientes para os quais _O número total de pedidos é inferior a 1_ é True.

   - No painel à esquerda, escolha **[!UICONTROL Conditions]**.

     A condição padrão começa com &quot;Se TODAS essas condições forem VERDADEIRAS:&quot;

   - Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) e selecione `Number of Orders`.

   - Clique em **[!UICONTROL is]** e selecione `less than`.

   - Clique em **..** e insira `1` no campo.

   - Clique na marca de seleção verde ( ![Marca de seleção verde](../assets/icon-checkmark-green-circle.png) ) para salvar a configuração de condição.

   ![Condição de segmento do cliente](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save]**.

O segmento do cliente é criado e exibido no _[!UICONTROL Customer Segments]_grade.

>[!TIP]
>
>Anote a ID do segmento. Você usa esse número de ID para criar a regra de preço do carrinho.

## Etapa 2. Criar a regra de preço do carrinho

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Rule]**.

   A variável **[!UICONTROL Rule Information]** é exibida por padrão, com seções expansíveis para **[!UICONTROL Conditions]** e **[!UICONTROL Conditions]**.

1. Defina o **[!UICONTROL Rule Information]**.

   - Conclua o **[!UICONTROL Rule Name]** e **[!UICONTROL Description]** campos. Esses campos são somente para sua referência interna.

   - Para **[!UICONTROL Websites]**, selecione o site onde a regra deve estar disponível.

   - Para **[!UICONTROL Customer Groups]**, selecione o grupo de clientes ao qual essa regra se aplica.

     Para selecionar vários grupos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

     >[!NOTE]
     >
     >As opções nessa lista dependem dos grupos de clientes criados e gerenciados no **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

   - Para **[!UICONTROL Coupon]**, selecione `No Coupon`.

   - Para **[!UICONTROL Uses per Customer]**, insira `1`.

   - Para **[!UICONTROL Priority]**, digite um número para estabelecer a prioridade desta regra em relação a outras regras.

     >[!NOTE]
     >
     >A configuração Prioridade é importante quando o mesmo produto de catálogo atende às condições definidas para mais de uma regra de preço. A regra com a configuração de Prioridade mais alta se torna ativa para o cliente. A prioridade mais alta é 1. Para este exemplo, inserir `1` significa que essa regra é aplicada antes de qualquer outra regra de preço. Esse valor é usado pelo **[!UICONTROL Discard Subsequent Rules]** configuração no **[!UICONTROL Action]** seção.

   - Quando terminar, clique em **[!UICONTROL Save and Continue Edit]**.

     Opções adicionais ficam disponíveis no painel à esquerda.

   ![Informações de regra de preço do carrinho](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. Defina o **[!UICONTROL Conditions]**.

   - Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Conditions]** seção.

     A regra padrão começa, &quot;Se TODAS essas condições forem TRUE:&quot;.

   - Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) e selecione `Customer Segment`.

     O campo de qualificador é padronizado como `matches`.

   - Clique em **..** e informe a ID de segmento do segmento do cliente que deseja direcionar.

     Neste exemplo, a ID do segmento para o novo segmento criado na Etapa 1 é `2`.

     >[!NOTE]
     >
     >Se você não souber a ID do segmento, clique no ícone do seletor ( ![Ícone de Lista](../assets/icon-list-chooser.png) ) para exibir a lista de Segmentos do cliente. Você pode inserir manualmente a ID no campo ou marcar a caixa de seleção do segmento desejado para preencher automaticamente o campo.

   - Clique na marca de seleção verde ( ![Marca de seleção verde](../assets/icon-checkmark-green-circle.png) ) para salvar a configuração de condição.

   - Quando terminar, clique em **[!UICONTROL Save and Continue Edit]**.

     Essa linha da regra se aplica a todos os clientes que correspondem à ID de segmento de cliente 2.

   ![Condição de segmento do cliente](./assets/customer-segment-matches.png){width="400"}

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png)o **[!UICONTROL Conditions]** e defina as ações da regra.

   Nesta seção, você define o tipo de desconto e o valor/quantia do desconto que deseja aplicar aos clientes pela primeira vez. Este exemplo define um desconto de 10% para todos os clientes que atenderem à condição definida. Para obter informações sobre outras opções disponíveis, consulte [Criando uma Regra de Preço do Carrinho](price-rules-cart-create.md).

   - Para **[!UICONTROL Apply]**, selecione Percentual de desconto do preço do produto.

   - Para **[!UICONTROL Discount Amount]**, insira `10`.

   - Para aplicar esta regra de preço somente aos valores do produto, defina **[!UICONTROL Apply to Shipping Amount]** para `No`.

   - Para impedir que o sistema aplique várias regras de preço ao mesmo produto, defina **[!UICONTROL Discard Subsequent Rules]** para `Yes`.

   - Quando terminar, clique em **[!UICONTROL Save]**.

   ![Ações de regra de preço do carrinho](./assets/actions-first-time.png){width="600" zoomable="yes"}

Normalmente, a nova regra fica disponível em uma hora. Teste a regra para garantir que ela funcione conforme definido.

## Etapa 3: salvar e testar a regra

{{new-price-rule}}

1. Quando a regra for concluída, clique em **[!UICONTROL Save Rule]**.

1. Teste a regra para verificar se ela funciona corretamente.
