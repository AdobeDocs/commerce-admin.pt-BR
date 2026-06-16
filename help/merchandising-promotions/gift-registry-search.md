---
title: Adicionar pesquisa de registro de presente
description: Saiba como colocar uma caixa de pesquisa de registro de presente para ajudar a armazenar visitantes que compram produtos de registros de clientes.
exl-id: 8c5558d6-3641-4769-987e-8b217603d9fc
feature: Gift, Storefront, Search
TQID: https://experienceleague.adobe.com/YlSi1XDNBNDc4EUdmEuPI-8gxAhHhWbxUY2ge-2AEV0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 437
ht-degree: 0%

---

# Adicionar pesquisa de registro de presente

{{ee-feature}}

A ferramenta [Widget](../content-design/widgets.md) pode ser usada para colocar uma caixa de pesquisa do Registro de presente em qualquer lugar da sua loja. Você pode especificar as opções de pesquisa que estarão disponíveis para os clientes, como nome, endereço de email e ID de registro do presente. Quando o cliente clica no botão Pesquisar, os resultados são exibidos na página Pesquisar no Registro de presentes. Se a pesquisa não retornar resultados, o cliente poderá tentar novamente com outros parâmetros.

![Exemplo de vitrine - pesquisa do registro de presentes](./assets/storefront-gift-registry-search.png){width="700" zoomable="yes"}

## Configurar pesquisa de registro de presente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]**.

1. Escolha a guia **[!UICONTROL Settings]** e faça o seguinte:

   - Defina **[!UICONTROL Type]** como `Gift Registry Search`.

   - Defina **[!UICONTROL Design Theme]** com o tema usado pelo armazenamento.

   - Clique em **[!UICONTROL Continue]**.

   ![Registro de presentes - configurações de pesquisa](./assets/widget-gift-registry-search-settings.png){width="700" zoomable="yes"}

1. Na seção _[!UICONTROL Storefront Properties]_, faça o seguinte:

   - Insira um **[!UICONTROL Widget Title]** para referência interna.

   - Defina **[!UICONTROL Assign to Store Views]** para as exibições de loja onde a Pesquisa do Registro de Presentes deverá estar disponível.

   - Defina **[!UICONTROL Sort Order]** para determinar a ordem em que o bloco de Pesquisa do Registro de Presentes aparece quando há outros blocos atribuídos ao mesmo local na página.

   ![Registro de presentes - propriedades da loja](./assets/widget-gift-registry-search-storefront-properties.png){width="700" zoomable="yes"}

1. Na seção **[!UICONTROL Layout Updates]**, clique em **[!UICONTROL Add Layout Update]**.

1. Para determinar onde a Pesquisa do Registro de presentes aparece na loja, faça o seguinte:

   - Defina **[!UICONTROL Display On]** para as páginas em sua loja onde deseja que o bloco de Pesquisa do Registro de Presentes apareça.

   - Se aplicável, escolha o **[!UICONTROL Categories]** onde deseja que ele seja exibido.

   - Defina **[!UICONTROL Container]** para o local na página para colocar o bloco de Pesquisa do Registro de Presentes.

   ![Registro de presentes - atualizações de layout](./assets/widget-gift-registry-search-layout-updates.png){width="500" zoomable="yes"}

1. No painel esquerdo, escolha **[!UICONTROL Widget Options]**.

1. Para determinar como os visitantes do site podem pesquisar registros de presentes, selecione os seguintes itens que se aplicam:

   - [!UICONTROL All Forms]
   - [!UICONTROL Registrant Name Search]
   - [!UICONTROL Registrant Email Search]
   - [!UICONTROL Gift Registry ID Search]

   ![Registro de presentes - opções de widget](./assets/widget-gift-registry-search-widget-options.png){width="700" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado a atualizar o cache de páginas, clique no link na mensagem na parte superior do espaço de trabalho e siga as instruções.

## Descrições dos campos

### [!UICONTROL Settings]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Type] | Identifica `Gift Registry Search` como o tipo de Widget. |
| [!UICONTROL Design Theme] | O tema usado pela loja onde a Pesquisa do Registro de Presentes deve aparecer. |

{style="table-layout:auto"}

### [!UICONTROL Storefront Properties]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Widget Title] | Um nome para referência interna. |
| [!UICONTROL Assign to Store Views] | Identifica as exibições de loja onde a Pesquisa do Registro de Presentes deve estar disponível. |
| [!UICONTROL Sort Order] | Indica a ordem em que o bloco Pesquisa do Registro de Presentes será exibido se houver outros blocos atribuídos para serem exibidos no mesmo local. |

{style="table-layout:auto"}

### [!UICONTROL Layout Updates]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Display On] | Indique as páginas específicas ou os tipos de páginas em que o bloco de pesquisa do Registro de presentes é exibido. |
| [!UICONTROL Categories] | Se aplicável, identifica as páginas de categoria em que a Pesquisa no Registro de presentes é exibida. |
| [!UICONTROL Container] | Indica o bloco de layout da página onde a Pesquisa no Registro de presentes é colocada. As opções variam por modelo e tema. |

{style="table-layout:auto"}

### [!UICONTROL Widget Options]

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Quick Search Form Types] | Determina os tipos de pesquisas que podem ser executadas com a Pesquisa do Registro de presentes. Opções: `All Forms` / `Registrant Name Search` /` Registrant Email Search` / `Gift Registry ID Search` |

{style="table-layout:auto"}
