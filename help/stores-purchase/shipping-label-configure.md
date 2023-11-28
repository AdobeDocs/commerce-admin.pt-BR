---
title: Configurar etiquetas de remessa
description: Saiba como configurar a loja para gerar etiquetas de remessa.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '595'
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

O país de fabricação é necessário para todos os produtos que são enviados internacionalmente pelo USPS e pela FedEx. Se você tiver muitos produtos que devem ser atualizados, é possível [importar](../systems/data-import.md) as atualizações ou use a grade Inventário para atualizar vários registros.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Atualize o registro de etiqueta de remessa usando um dos métodos a seguir.

### Método 1: atualizar um único registro

1. Na grade, localize o produto a ser atualizado e abra-o no modo de edição.

1. Atualize o **País de fabricação** conforme necessário.

   ![País de fabricação](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Clique em **[!UICONTROL Save]**.

### Método 2: atualizar vários registros

1. Na grade, marque a caixa de seleção de cada produto a ser atualizado.

   Por exemplo, todos os produtos que são fabricados na China.

1. Defina o **[!UICONTROL Actions]** controle para `Update Attributes` e clique em **[!UICONTROL Submit]**.

1. No _Atualizar atributos_ formulário, localize o **País de fabricação** e selecione o **Alterar** caixa de seleção

1. Escolha o país.

1. Clique em **[!UICONTROL Save]**.

## Etapa 2 Verificar as informações da loja

{{beta2-updates}}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Shipping Settings]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Origin]** e verifique se os seguintes campos estão completos:

   - **[!UICONTROL Street Address]** - O endereço do local de onde as remessas são enviadas. Por exemplo, o local da sua empresa ou depósito. Este campo é obrigatório para etiquetas de remessa.
   - **[!UICONTROL Street Address Line 2]** - Quaisquer informações adicionais sobre o endereço, como andar ou entrada. É recomendado usar este campo.

   ![Origem](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. No _Vendas_ no painel esquerdo, escolha **[!UICONTROL Delivery Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL USPS]** e verifique se os seguintes campos estão completos:

   - **[!UICONTROL Secure Gateway URL]** - O sistema insere automaticamente o URL do gateway.
   - **[!UICONTROL Password]** - A senha é fornecida pelo USPS e fornece acesso ao sistema por meio dos Serviços da Web.
   - **Comprimento, Largura, Altura, Girth** - As dimensões padrão do pacote. Para que esses campos apareçam, defina **[!UICONTROL Size]** para `Large`.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **FedEx** e verifique se os seguintes campos estão completos:

   - Número do Medidor
   - Chave
   - Senha

   Essas informações são fornecidas pela operadora e são necessárias para obter acesso ao sistema por meio dos Serviços da Web.

1. No painel esquerdo, expanda **[!UICONTROL General]** e escolha **[!UICONTROL General]** por baixo.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Store Information]** e verifique se os seguintes campos estão completos:

   - **[!UICONTROL Store Name]** - O nome da loja ou exibição de loja.
   - **[!UICONTROL Store Contact Telephone]** - O número de telefone do contato principal da loja ou exibição de loja.
   - **[!UICONTROL Country]** - O país onde sua loja está baseada.
   - **[!UICONTROL VAT Number]** - Se aplicável, o número de Imposto sobre o Valor Agregado da loja. (Não obrigatório para lojas com sede nos EUA)
   - **[!UICONTROL Store Contact Address]** - O endereço do contato principal da exibição de loja ou loja.

1. Se você tiver vários armazenamentos e as informações de contato forem diferentes do padrão, defina **[!UICONTROL Store View]** para cada e verifique se as informações estão completas.

   Se as informações estiverem ausentes, um erro será exibido quando você tentar imprimir as etiquetas.

   ![Armazenar informações](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Config]**.
