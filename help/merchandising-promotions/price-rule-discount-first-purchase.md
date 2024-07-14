---
title: Exemplo de regra de preço do carrinho - desconto com a primeira compra
description: Analise um exemplo de uso de uma regra de preço de carrinho para oferecer um desconto a clientes pela primeira vez.
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Exemplo de regra de preço do carrinho - desconto com a primeira compra

{{ee-feature}}

As regras de preço do carrinho podem ser usadas para oferecer automaticamente um desconto aos clientes na primeira compra, sem a necessidade de um cupom.

Para oferecer um desconto direcionado para clientes pela primeira vez, é possível:

- Crie um segmento de cliente definido como _compradores sem pedidos_ e
- Crie uma regra de preço do carrinho que segmente o novo segmento de cliente.

>[!NOTE]
>
>Certifique-se de que o recurso Segmentos do cliente esteja ativado. Consulte [Criar um segmento de cliente](../customers/customer-segment-create.md).

## Etapa 1. Criar um segmento de cliente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. No canto superior direito, clique em **[!UICONTROL Add Segment]**.

1. Defina o **[!UICONTROL General Properties]**.

   - Insira um **[!UICONTROL Segment Name]** para identificar o segmento do cliente (Exemplo: _Primeiro cliente_).

   - Para **[!UICONTROL Assigned to Website]**, selecione o site onde o segmento de cliente pode ser usado.

   - Para **[!UICONTROL Status]**, selecione `Active`.

   - Para **[!UICONTROL Apply to]**, selecione `Visitors and Registered Customers`.

   - Quando terminar, clique em **[!UICONTROL Save and Continue Edit]**.

     Opções adicionais ficam disponíveis no painel à esquerda.

   ![Propriedades do segmento do cliente](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. Defina o **[!UICONTROL Conditions]**.

   Neste exemplo, a condição é direcionada a clientes para os quais _o Número Total de Pedidos é menor que 1_ e é Verdadeiro.

   - No painel à esquerda, escolha **[!UICONTROL Conditions]**.

     A condição padrão começa com &quot;Se TODAS essas condições forem VERDADEIRAS:&quot;

   - Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) e selecione `Number of Orders`.

   - Clique em **[!UICONTROL is]** e selecione `less than`.

   - Clique em **...** e digite `1` no campo.

   - Clique na marca de seleção verde ( ![Marca de seleção verde](../assets/icon-checkmark-green-circle.png) ) para salvar a configuração de condição.

   ![Condição de segmento de cliente](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save]**.

O segmento de cliente é criado e exibido na grade _[!UICONTROL Customer Segments]_.

>[!TIP]
>
>Anote a ID do segmento. Você usa esse número de ID para criar a regra de preço do carrinho.

## Etapa 2. Criar a regra de preço do carrinho

1. Na barra lateral _Admin_, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Rule]**.

   A seção **[!UICONTROL Rule Information]** é exibida por padrão, com seções expansíveis para **[!UICONTROL Conditions]** e **[!UICONTROL Conditions]**.

1. Defina o **[!UICONTROL Rule Information]**.

   - Complete os campos **[!UICONTROL Rule Name]** e **[!UICONTROL Description]**. Esses campos são somente para sua referência interna.

   - Para **[!UICONTROL Websites]**, selecione o site onde a regra deve estar disponível.

   - Para **[!UICONTROL Customer Groups]**, selecione o grupo de clientes ao qual essa regra se aplica.

     Para selecionar vários grupos, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

     >[!NOTE]
     >
     >As opções nesta lista dependem dos grupos de clientes criados e gerenciados em **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

   - Para **[!UICONTROL Coupon]**, selecione `No Coupon`.

   - Para **[!UICONTROL Uses per Customer]**, digite `1`.

   - Para **[!UICONTROL Priority]**, insira um número para estabelecer a prioridade desta regra em relação a outras regras.

     >[!NOTE]
     >
     >A configuração Prioridade é importante quando o mesmo produto de catálogo atende às condições definidas para mais de uma regra de preço. A regra com a configuração de Prioridade mais alta se torna ativa para o cliente. A prioridade mais alta é 1. Neste exemplo, inserir `1` significa que esta regra é aplicada antes de qualquer outra regra de preço. Este valor é usado pela configuração **[!UICONTROL Discard Subsequent Rules]** na seção **[!UICONTROL Action]**.

   - Quando terminar, clique em **[!UICONTROL Save and Continue Edit]**.

     Opções adicionais ficam disponíveis no painel à esquerda.

   ![Informações sobre a regra de preço do carrinho](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. Defina o **[!UICONTROL Conditions]**.

   - Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png) na seção **[!UICONTROL Conditions]**.

     A regra padrão começa, &quot;Se TODAS essas condições forem TRUE:&quot;.

   - Clique em _Adicionar_ (![Ícone Adicionar](../assets/icon-add-green-circle.png)) e selecione `Customer Segment`.

     O campo de qualificador é padronizado como `matches`.

   - Clique em **...** e digite a ID de segmento do cliente que deseja direcionar.

     Neste exemplo, a ID do segmento criado na Etapa 1 é `2`.

     >[!NOTE]
     >
     >Se você não souber a ID do segmento, clique no ícone do seletor ( ![ícone de Lista](../assets/icon-list-chooser.png) ) para exibir a lista Segmento de cliente. Você pode inserir manualmente a ID no campo ou marcar a caixa de seleção do segmento desejado para preencher automaticamente o campo.

   - Clique na marca de seleção verde ( ![Marca de seleção verde](../assets/icon-checkmark-green-circle.png) ) para salvar a configuração de condição.

   - Quando terminar, clique em **[!UICONTROL Save and Continue Edit]**.

     Essa linha da regra se aplica a todos os clientes que correspondem à ID de segmento de cliente 2.

   ![Condição de segmento de cliente](./assets/customer-segment-matches.png){width="400"}

1. Role para baixo e expanda ![Seletor de expansão](../assets/icon-display-expand.png)a seção **[!UICONTROL Conditions]** e defina as ações para a regra.

   Nesta seção, você define o tipo de desconto e o valor/quantia do desconto que deseja aplicar aos clientes pela primeira vez. Este exemplo define um desconto de 10% para todos os clientes que atenderem à condição definida. Para obter informações sobre outras opções disponíveis, consulte [Criando uma Regra de Preço do Carrinho](price-rules-cart-create.md).

   - Para **[!UICONTROL Apply]**, selecione Porcentagem de desconto no preço do produto.

   - Para **[!UICONTROL Discount Amount]**, digite `10`.

   - Para aplicar esta regra de preço somente a valores de produtos, defina **[!UICONTROL Apply to Shipping Amount]** como `No`.

   - Para impedir que o sistema aplique várias regras de preço ao mesmo produto, defina **[!UICONTROL Discard Subsequent Rules]** como `Yes`.

   - Quando terminar, clique em **[!UICONTROL Save]**.

   ![Ações de regra de preço do carrinho](./assets/actions-first-time.png){width="600" zoomable="yes"}

Normalmente, a nova regra fica disponível em uma hora. Teste a regra para garantir que ela funcione conforme definido.

## Etapa 3: salvar e testar a regra

{{new-price-rule}}

1. Quando a regra estiver concluída, clique em **[!UICONTROL Save Rule]**.

1. Teste a regra para verificar se ela funciona corretamente.
