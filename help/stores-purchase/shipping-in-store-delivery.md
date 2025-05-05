---
title: Entrega na loja
description: Saiba como configurar uma opção de entrega na loja.
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Entrega na loja

Com o método de entrega na loja, o cliente pode selecionar uma origem a ser usada como um local de retirada durante a finalização da compra.

![Método de Entrega na Loja no Check-out](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

Durante o check-out na loja:

1. O cliente clica em **[!UICONTROL Pick In Store]** ou seleciona o método de envio _[!UICONTROL In-Store Pickup Delivery]_.
1. A guia de check-out _[!UICONTROL Pick In Store]_&#x200B;é aberta.

Quando o cliente tiver um endereço ou tiver preenchido anteriormente o formulário de endereço de entrega antes de alternar para a guia _[!UICONTROL Pick In Store]_:

- A origem mais próxima do endereço do cliente dentro do raio configurado é automaticamente pré-selecionada como uma loja de retirada.
- Quando o cliente clicar em **[!UICONTROL Select Other]**, o formulário de pesquisa _[!UICONTROL Select Store]_&#x200B;será aberto. Somente os armazenamentos dentro da distância configurada (raio) do armazenamento pré-selecionado são exibidos na lista. Todos os armazenamentos na lista são classificados pela distância até o armazenamento pré-selecionado.
- Quando o cliente informa um código postal ou o nome da cidade no campo de pesquisa, somente as lojas dentro da distância configurada (raio) para o local pesquisado são exibidas na lista. Todos os armazenamentos na lista são classificados pela distância até o local pesquisado.
- Quando o cliente apaga o código postal ou o nome da cidade do campo de pesquisa, todas as lojas de retirada atribuídas aos produtos no carrinho de compras são mostradas ao cliente. Todos os armazenamentos na lista são classificados em ordem crescente dos códigos-fonte, sem qualquer limitação de distância (raio).

Se o cliente não tiver um endereço ou não tiver preenchido o formulário de endereço de entrega antes de alternar para a guia _[!UICONTROL Pick In Store]_:

- A página exibe a mensagem _Não foi possível pré-selecionar o local da retirada com base nas informações disponíveis_.
- Quando o cliente clicar em **[!UICONTROL Select Store]**, o formulário de pesquisa _[!UICONTROL Select Store]_&#x200B;será aberto.
- Todas as lojas de retirada atribuídas aos produtos no carrinho de compras são exibidas em ordem crescente dos códigos-fonte, sem qualquer limitação de distância (raio).
- Quando o cliente informa um código postal ou o nome da cidade no campo de pesquisa, somente as lojas dentro da distância configurada (raio) para o local pesquisado são exibidas na lista. Todos os armazenamentos na lista são classificados pela distância até o local pesquisado.

## Antes da configuração

- Verifique se você tem um estoque e uma origem não padrão. Para obter mais informações sobre como configurar uma origem como um local de retirada, consulte [Adicionar uma origem](../inventory-management/sources-add.md).
- Verifique se você configurou um Algoritmo de Prioridade de Distância. Para obter mais informações, consulte [Configurar o Algoritmo de Prioridade de Distância](../inventory-management/distance-priority-algorithm.md).
- Verifique se você [baixou e importou](../inventory-management/cli.md#import-geocodes) todos os geocódigos necessários para o cálculo offline.
- Verifique se você definiu as configurações de [Cálculo de Destino de Imposto Padrão](../configuration-reference/sales/tax.md#default-tax-destination-calculation).

>[!IMPORTANT]
>
>**Na loja, os resultados da pesquisa são filtrados por distância (raio) para mostrar resultados relevantes:**<br><br>
>Se o cliente tiver um endereço de entrega, o local base para calcular a distância (raio) será obtido do endereço de entrega.<br><br>
>Se o cliente não tiver um endereço de entrega, o local base para calcular a distância será obtido das configurações de [Cálculo de Destino de Imposto Padrão](../configuration-reference/sales/tax.md#default-tax-destination-calculation). Essas configurações são definidas por exibição de loja e você deve definir as configurações de Cálculo de Destino de Imposto Padrão para garantir que a pesquisa de loja de retirada funcione corretamente.

## Configurar entrega na loja

Primeiro, verifique se o delivery na loja está ativado.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Delivery Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL In-Store Delivery]**.

   ![Entrega na loja](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Enabled]** como `Yes`.

   >[!NOTE]
   >
   >Se necessário, desmarque a caixa de seleção **[!UICONTROL Use system value]** para alterar o padrão de qualquer campo.

1. Insira o **[!UICONTROL Method Name]** que descreve o método de cálculo usado para produzir uma estimativa de remessa.

   O nome do método aparece ao lado da taxa estimada calculada no carrinho de compras.

1. Insira a **[!UICONTROL Title]** que você deseja exibir para a seção _Entrega na Loja_ durante o check-out.

   O título padrão é `In-Store Pickup Delivery`.

1. Para cobrar dos clientes o serviço de coleta na loja, insira a taxa no campo **[!UICONTROL Price]**.

1. Insira o **[!UICONTROL Search Radius]** em quilômetros para a pesquisa de local de retirada de loja no check-out de vitrine.

1. Para **[!UICONTROL Displayed Error Message]**, insira a mensagem que aparece se a entrega na loja ficar indisponível.

   A mensagem padrão é `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Clique em **[!UICONTROL Save Config]**.
