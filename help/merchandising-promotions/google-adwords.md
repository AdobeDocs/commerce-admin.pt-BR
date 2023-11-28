---
title: Google AdWords
description: Saiba como configurar sua loja do Commerce para o rastreamento de conversão do Google AdWords para medir os cliques em anúncios que levam a uma venda ou outra ação valiosa.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# Google AdWords

[Google AdWords][1] O é um serviço que você pode usar para colocar anúncios nos resultados da Pesquisa da Google e nas páginas das empresas na Rede de exibição da Google. O painel do AdWords inclui ferramentas para gerenciar campanhas, rastrear respostas e medir resultados.

O rastreamento de conversão mostra o número de cliques em anúncios que resultam em uma venda ou outra ação valiosa. A variável _Sucesso_ A página que aparece para o cliente depois que um pedido é enviado é usada para rastrear conversões porque aparece somente após uma venda. Depois de concluir a configuração do Google AdWords para sua loja, não há necessidade de copiar o script de rastreamento de conversão para a página Sucesso, pois o Commerce já tem as informações necessárias. Para saber mais, consulte [Ajuda do Google AdWords][2].

![Anúncio Adobe nos resultados de pesquisa do Google](./assets/google-adwords-adobe-ad.png){width="500"}

## Etapa 1. Criar uma campanha do Google AdWords

1. Visita [Google AdWords][3]e cadastre-se em uma conta.

1. Siga as instruções para criar uma campanha.

1. Para configurar o rastreamento de conversão para sua campanha, faça o seguinte:

   - No **[!UICONTROL Tools]** do painel do AdWords, escolha **[!UICONTROL Conversions]** e clique em **[!UICONTROL Conversion]**.

   - Quando solicitado para a origem da conversão, escolha **[!UICONTROL Website]**.

   - Insira um nome para a ação de conversão que deseja rastrear e clique em **[!UICONTROL Done]**.

   - Clique em **[!UICONTROL Value]** e, se aplicável, atribua um valor à conversão. Por exemplo:

      - Se você ganha US$ 5 em cada venda, escolha `Each time it happens` e atribua um valor de `$5`.
      - Se o valor de cada venda variar, deixe o valor em branco.

     Para concluir, clique em **[!UICONTROL Done]**.

   - Clique em **[!UICONTROL Conversion windows]** e conclua as configurações para determinar por quanto tempo as conversões devem ser rastreadas, a categoria dos relatórios e o modelo de atribuição.

1. Quando terminar, clique em **[!UICONTROL Save and Continue]**.

## Etapa 2. Obtenha sua tag de conversão

1. Em **[!UICONTROL Install your tag]**, escolha contar conversões em **[!UICONTROL Page load]**.

1. Como opção, você pode adicionar a variável **[!UICONTROL Google Site Stats]** notificação para a página de conversão.

   A notificação aparece no canto inferior com um link para os padrões de segurança e uso de cookies da Google.

1. Para escolher como deseja gerenciar a tag do AdWords, siga um destes procedimentos:

   - Se você planeja adicionar o script ao seu armazenamento, escolha **[!UICONTROL Save instructions and tag]**.
   - Se você planeja que outra pessoa adicione o script à sua loja, escolha **[!UICONTROL Email instructions and tag]**.

1. Quando terminar, clique em **[!UICONTROL Done]**.

## Etapa 3. Configurar sua loja

{{gtag-api-note}}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Se estiver configurando o Google AdWords para uma exibição de loja específica, faça o seguinte:

   - No canto superior esquerdo, escolha a **[!UICONTROL Store View]** que deve ser configurado.

   - Quando solicitado a confirmar a alternância do escopo, clique em **[!UICONTROL OK]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Google API]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Google AdWords]** e faça o seguinte:

   - Definir **[!UICONTROL Enable]** para `Yes`.

   - Insira o **[!UICONTROL Conversion ID]** do seu script do Google AdWords.

   ![Configuração de vendas - API do Google Ads](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Para formatar a notificação de Início do Google Sites, faça o seguinte:

   - Definir **[!UICONTROL Conversion Language]** ao idioma identificado no script do Google AdWords.

   - Insira o **[!UICONTROL Conversion Format]** a ser usado para a notificação de Status do Google Sites na página de conversão.

      - `1`  - Exibe uma notificação em uma linha com um link para obter mais informações sobre o rastreamento do Google.
      - `2` - Exibe uma notificação em duas linhas com um link para obter mais informações sobre o rastreamento do Google.
      - `3` - Não exibe nenhuma notificação ao cliente.

   - Insira o [código hexadecimal][4]{:target=&quot;_blank&quot;} para a **[!UICONTROL Conversion Color]** que você deseja usar para o rótulo de notificação Estatísticas de site do Google.

   - Insira o texto criptografado para o **[!UICONTROL Conversion Label]** que aparece na notificação de Início do Google Sites.

     Por exemplo: `MlEYCOKBnGoQz6CZoAM`

     **Exemplo de código de tag do Google AdWords**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. Definir **[!UICONTROL Conversion Value Type]** a um dos seguintes:

   - `Dynamic` - Determina que ocorreu uma conversão com base no valor dinâmico do Valor do pedido.
   - `Constant` - Determina se uma conversão ocorreu com base em um valor específico inserido.

   Para um _Constante_ tipo de valor de conversão, insira um **[!UICONTROL Value]** para o _[!UICONTROL Order Amount]_para se qualificar como uma conversão.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Etapa 4. Verificar a configuração

Em poucas horas, o status de rastreamento no painel do Google AdWords será alterado de `Unverified` para `No recent conversions` ou `Recording conversions`. Quando alguém clica em seu anúncio e faz uma compra, a conversão é exibida na página Ações de conversão do painel e do relatório de campanha.

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
