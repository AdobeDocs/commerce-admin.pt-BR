---
title: Zonas e alíquotas de imposto
description: Saiba como definir alíquotas de imposto para cada área geográfica em que você coleta e remete impostos.
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Zonas e alíquotas de imposto

As taxas de imposto geralmente se aplicam a transações que ocorrem dentro de uma área geográfica específica. Use a ferramenta _Taxas e zonas de imposto_ para especificar a alíquota de imposto para cada área geográfica da qual você coleta e envia impostos. Como cada zona e alíquota de imposto tem um identificador exclusivo, é possível ter várias alíquotas de imposto para uma determinada área geográfica (como locais que não cobram impostos de alimentos ou remédios, mas cobram impostos de outros itens).

O imposto da loja é calculado com base no endereço da loja. O imposto real do cliente para uma ordem é calculado depois que o cliente conclui as informações da ordem. Em seguida, o Commerce calcula o imposto de acordo com a configuração de imposto da loja.

![Taxas e zonas de impostos](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## Definir uma nova alíquota de imposto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Tax Rate]**.

   ![Nova Alíquota de Imposto](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. Insira um **[!UICONTROL Tax Identifier]**.

1. Para aplicar a alíquota de imposto a um único CEP, insira o código de **[!UICONTROL Zip/Post Code]**.

   O curinga de asterisco (`*`) pode ser usado para corresponder até dez caracteres no código. Por exemplo, `90*` representa todos os códigos postais de 90.000 a 90.999.

1. Para aplicar a alíquota a uma faixa de CEPs ou códigos postais, faça o seguinte:

   - Marque a caixa de seleção **[!UICONTROL Zip/Post is Range]** e defina o intervalo inserindo o primeiro e o último CEP para **[!UICONTROL Range From]** e **[!UICONTROL Range To]**.

     ![ZIP/Post é um intervalo](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - Escolha o **[!UICONTROL State]** onde a alíquota do imposto se aplica.

   - Escolha o **[!UICONTROL Country]** onde a alíquota do imposto se aplica.

   - Insira o **[!UICONTROL Rate Percent]** que é usado para o cálculo da alíquota do imposto.

1. Se você tiver vários armazenamentos, poderá definir **[!UICONTROL Tax Titles]** para cada exibição de armazenamento.

   >[!NOTE]
   >
   >Deixe este campo vazio se quiser usar o identificador de imposto.

1. Quando terminar, clique em **[!UICONTROL Save Rate]**.

## Editar uma alíquota de imposto existente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Localize a alíquota de imposto na grade _[!UICONTROL Tax Zones and Rates]_e abra o registro no modo de edição.

   Se houver muitas taxas na lista, use os [controles de filtro](../getting-started/admin-grid-controls.md) para encontrar a taxa necessária.

1. Faça as alterações necessárias no **[!UICONTROL Tax Rate Information]**.

1. Atualize o **[!UICONTROL Tax Titles]** conforme necessário.

1. Quando terminar, clique em **[!UICONTROL Save Rate]**.

## Excluir alíquota de imposto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Localize a alíquota do imposto a ser excluída e abra-a no modo de edição.

1. Na barra de menus, clique em **[!UICONTROL Delete Rate]**.

1. Para confirmar a ação, clique em **[!UICONTROL OK]**.
