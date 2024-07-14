---
title: Configurar etiquetas de remessa
description: Saiba como configurar a loja para gerar etiquetas de remessa.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Configurar etiquetas de remessa

As configurações a seguir devem ser feitas no nível do produto e na configuração de cada operadora usada para imprimir etiquetas. Para imprimir etiquetas, todas as operadoras exigem que você abra uma conta. Em seguida, conclua a configuração na loja para cada operadora que planeja usar.

## Requisitos da operadora

| [!UICONTROL Carrier] | Requisitos |
|-------|--------|
| [USPS](usps.md) | Exige uma conta USPS. A partir de 23 de fevereiro de 2018, a USPS exige que todas as etiquetas de envio incluam a postagem. |
| [UPS](ups.md) | Exige uma conta UPS. As etiquetas de remessa estão disponíveis apenas para remessas originárias dos EUA. Credenciais específicas são necessárias para lojas fora dos EUA. |
| [FedEx](fedex.md) | Exige uma conta FedEx. Para lojas fora dos EUA, as etiquetas de remessa são suportadas apenas para remessas internacionais. A FedEx não permite remessas domésticas originárias de fora dos EUA |
| [DHL](dhl.md) | Requer uma conta DHL. As etiquetas de remessa só têm suporte para remessas originárias dos EUA. |

{style="table-layout:auto"}

## Etapa 1: verifique o país de fabricação

O país de fabricação é necessário para todos os produtos que são enviados internacionalmente pelo USPS e pela FedEx. Se você tiver muitos produtos que precisam ser atualizados, é possível [importar](../systems/data-import.md) as atualizações ou usar a grade do Inventário para atualizar vários registros.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Atualize o registro de etiqueta de remessa usando um dos métodos a seguir.

### Método 1: atualizar um único registro

1. Na grade, localize o produto a ser atualizado e abra-o no modo de edição.

1. Atualize o **País de Fabricação** conforme necessário.

   ![País de fabricação](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Save]**.

### Método 2: atualizar vários registros

1. Na grade, marque a caixa de seleção de cada produto a ser atualizado.

   Por exemplo, todos os produtos que são fabricados na China.

1. Defina o controle **[!UICONTROL Actions]** como `Update Attributes` e clique em **[!UICONTROL Submit]**.

1. No formulário _Atualizar atributos_, localize o campo **País de Fabricação** e marque a caixa de seleção **Alterar**.

1. Escolha o país.

1. Clique em **[!UICONTROL Save]**.

## Etapa 2 Verificar as informações da loja

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Shipping Settings]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Origin]** e verifique se os seguintes campos estão completos:

   - **[!UICONTROL Street Address]** - O endereço do local de onde as remessas são enviadas. Por exemplo, o local da sua empresa ou depósito. Este campo é obrigatório para etiquetas de remessa.
   - **[!UICONTROL Street Address Line 2]** - Quaisquer informações adicionais de endereço, como andar ou entrada. É recomendado usar este campo.

   ![Origem](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Na seção _Vendas_ do painel esquerdo, escolha **[!UICONTROL Delivery Methods]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL USPS]** e verifique se os seguintes campos estão completos:

   - **[!UICONTROL Secure Gateway URL]** - O sistema insere automaticamente a URL do gateway.
   - **[!UICONTROL Password]** - A senha é fornecida pelo USPS e fornece acesso ao sistema por meio dos Serviços da Web.
   - **Comprimento, Largura, Altura, Girth** - As dimensões padrão do pacote. Para que esses campos apareçam, defina **[!UICONTROL Size]** como `Large`.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **FedEx** e verifique se os seguintes campos estão completos:

   - Número do Medidor
   - Chave
   - Senha

   Essas informações são fornecidas pela operadora e são necessárias para obter acesso ao sistema por meio dos Serviços da Web.

1. No painel esquerdo, expanda **[!UICONTROL General]** e escolha **[!UICONTROL General]** abaixo de.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Store Information]** e verifique se os seguintes campos estão completos:

   - **[!UICONTROL Store Name]** - O nome do armazenamento ou exibição de armazenamento.
   - **[!UICONTROL Store Contact Telephone]** - O número de telefone do contato principal da loja ou exibição de loja.
   - **[!UICONTROL Country]** - O país onde a loja está baseada.
   - **[!UICONTROL VAT Number]** - Se aplicável, o número do Imposto sobre Valor Agregado da sua loja. (Não obrigatório para lojas com sede nos EUA)
   - **[!UICONTROL Store Contact Address]** - O endereço do contato principal do armazenamento ou exibição de armazenamento.

1. Se você tiver vários armazenamentos e as informações de contato forem diferentes do padrão, defina **[!UICONTROL Store View]** para cada um e verifique se as informações estão completas.

   Se as informações estiverem ausentes, um erro será exibido quando você tentar imprimir as etiquetas.

   ![Armazenar Informações](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.
