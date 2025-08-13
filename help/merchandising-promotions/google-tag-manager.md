---
title: '[!DNL Google Tag Manager]'
description: Saiba como usar o [!DNL Google Tag Manager] para gerenciar as várias tags (trechos de código) relacionadas aos eventos de campanha de marketing nos sites do Adobe Commerce.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 9c25196367023a44fa76e441d485693493a4c058
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

O [!DNL Google Tag Manager] é uma ferramenta poderosa que ajuda você a gerenciar e implantar com eficiência várias tags (trechos de código) associadas aos eventos de campanha de marketing. O [!DNL Google Tag Manager] oferece a capacidade de adicionar tags de rastreamento ao seu site para medir a audiência ou personalizar, redirecionar ou conduzir iniciativas de marketing de mecanismo de pesquisa.

O [!DNL Google Tag Manager] transfere dados e eventos diretamente para o [!DNL Google Analytics], Enhanced Ecommerce e outras soluções de análise de terceiros para produzir uma imagem clara do desempenho de seu site, de seus produtos e promoções.

Você deve ter uma conta de [!DNL Google Analytics] e [!DNL Tag Manager] para continuar esse processo. As instruções a seguir orientam você pelo processo de configuração das contas do Google, configuração da loja do Commerce e criação de uma tag.

>[!NOTE]
>
>Se a sua empresa estiver sujeita a regulamentos de privacidade como o [Regulamento Geral sobre a Proteção de Dados](../getting-started/compliance-gdpr.md) e/ou a [Lei de Privacidade do Consumidor da Califórnia](../getting-started/compliance-ccpa.md), consulte as [Configurações de Privacidade da Google](google-tools.md#google-privacy-settings).

## Etapa 1. Configurar sua conta do [!DNL Google Analytics]

Consulte [Configurar pesquisa de site](https://support.google.com/analytics/answer/1012264) na Ajuda do Google para obter as noções básicas necessárias para começar. Consulte também os guias do Google para o [Google Analytics](https://support.google.com/analytics/answer/9304153) e o [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Entre na sua conta [!DNL Google Analytics].

1. Para habilitar **[!UICONTROL Internal Site Search Tracking]**, faça o seguinte:

   - Navegue até **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Defina **[!UICONTROL Site Search Tracking]** como `On`.

   - Definir parâmetro **[!UICONTROL Query]** como `q`.

   - Ao concluir, **[!UICONTROL Save]** as configurações.

1. Para ativar recursos de exibição, faça o seguinte:

   - Escolha **[!UICONTROL Property Settings]**.

   - Em _[!UICONTROL Advertising Features]_, defina **[!UICONTROL Enable Demographics and Interest Reports]**como `On`.

   - **[!UICONTROL Save]** as configurações.

1. Para ativar o rastreamento de comércio eletrônico, faça o seguinte:

   - Navegue até **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Defina **[!UICONTROL Enable Ecommerce]** como `On`.

   - Defina **[!UICONTROL Enable Enhanced Ecommerce Reporting]** como `On`.

   - **[!UICONTROL Save]** as configurações.

1. Recarregue a página e verifique se todas as configurações permanecem `On`.

   >[!NOTE]
   >
   >Se nem todas as configurações forem `On`, repita as etapas anteriores, salve e recarregue a página. Repita esse processo até que todas as configurações sejam definidas como `On`.

## Etapa 2. Configurar sua conta do [!DNL Google Tag Manager]

As instruções a seguir mostram como configurar um novo container com as configurações básicas. Um exemplo de arquivo de configuração (.json) do [Composer](https://developer.adobe.com/commerce/php/development/composer/) é usado para simplificar o processo, importando para gerar uma marca em um novo contêiner. Para este exemplo, é recomendável criar um contêiner, em vez de modificar um contêiner existente.

>[!NOTE]
>
>Para obter informações adicionais, consulte [Exportação e importação de contêineres](https://support.google.com/tagmanager/answer/6106997) da Google. Essas instruções fornecem uma apresentação para importar uma amostra de JSON em um novo container.

1. Baixe o arquivo vinculado [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), abra-o em um editor e salve-o como `GTM_M2_Config.json`.

   O arquivo json é carregado diretamente para [!DNL Google Tag Manager].

1. Navegue até **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Clique em **[!UICONTROL Choose container file]** e selecione o arquivo json.

1. Em **[!UICONTROL Choose workspace]**, clique em **[!UICONTROL New]**.

1. Insira um título e uma descrição, depois clique em **[!UICONTROL Save]**.

1. Para importar o arquivo, selecione uma das seguintes ações:

   - A opção **[!UICONTROL Overwrite]** deve ser selecionada para um novo container.

   - A opção **[!UICONTROL Merge]** deve ser selecionada se você estiver usando um contêiner existente.

1. Clique em **[!UICONTROL Preview]** para examinar as marcas, os disparadores e as variáveis.

1. Para editar o **[!UICONTROL Google Analytics ID]** que é referenciado nas variáveis, faça o seguinte:

   - Navegue até **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Escolha **[!UICONTROL Google Analytics]** e atualize o espaço reservado (`UA-xxxxxx-x`) com seu próprio **[!UICONTROL GA ID]**.

1. Siga as instruções da Google para adicionar tags, acionadores e variáveis ao novo container.

   Se você tiver configurações em outro container que deseja usar, elas poderão ser movidas para o novo container.

1. Clique em **[!UICONTROL Confirm]** quando terminar.

1. Siga as instruções da Google para publicar o novo container.

## Etapa 3. Configurar sua loja

{{gtag-api-note}}

1. Faça logon no Admin da sua loja da Commerce.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Google API]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Google Analytics]** e configure o seguinte:

   ![Configuração de vendas - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Defina **[!UICONTROL Enable]** como `Yes`.

   - Defina **[!UICONTROL Account type]** como `Google Tag Manager`.

   - No campo **[!UICONTROL Container ID]**, digite sua ID de GTM (`GTM-xxxxxx`).

   - Se você também estiver usando o Google Analytics para experimentos de conteúdo, defina **Habilitar experimentos de conteúdo** para `Yes`.

   - Use os valores padrão para os campos restantes.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Teste as configurações do [!DNL Google Tag Manager] e verifique se tudo funciona corretamente.

>[!NOTE]
>
>Cada contêiner está associado a um site e você só precisa de um contêiner por conta. Se você tiver uma instância do Commerce com vários sites, precisará de containers separados.

## Descrições dos campos

| Campo | Escopo | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable] | Exibição da loja | Determina se o Ecommerce aprimorado do Google Analytics pode ser usado para analisar a atividade na sua loja. Opções: `Yes` / `No` |
| [!UICONTROL Account type] | Exibição da loja | Determina o código de rastreamento do Google usado para monitorar a atividade e o tráfego da loja. Opções: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Exibição da loja | Determina se as informações de identificação são removidas dos endereços IP que aparecem nos resultados do Google Analytics. |
| [!UICONTROL Container Id] | Exibição da loja | Se [!DNL Google Tag Manager] já estiver instalado e configurado para o armazenamento, a ID do Contêiner aparecerá automaticamente neste campo. |
| [!UICONTROL List property for the catalog page] | Exibição da loja | Identifica a propriedade do Gerenciador de tags associada à página do catálogo. Valor padrão: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Exibição da loja | Identifica a propriedade do Gerenciador de tags associada ao bloco de venda cruzada. Valor padrão: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Exibição da loja | Identifica a propriedade do Tag Manager associada ao bloco de venda adicional. Valor padrão: `Up-sell` |
| [!UICONTROL List property for the related products block] | Exibição da loja | Identifica a propriedade do Tag Manager associada ao bloco de produtos relacionados. Valor padrão: `Related Products` |
| [!UICONTROL List property for the search results page] | Exibição da loja | Identifica a propriedade do Gerenciador de tags associada à página de resultados da pesquisa. Valor padrão: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Exibição da loja | Identifica a propriedade do Tag Manager associada aos rótulos para promoções internas. Valor padrão: `Label` |

{style="table-layout:auto"}

## Criar uma tag para rastrear conversões

Se você tiver uma conta do Google AdWords, poderá criar uma tag que rastreia conversões. O exemplo a seguir mostra como usar o [!DNL Google Tag Manager] e o [!DNL Google Analytics] para criar uma tag que é acionada na página de conversão _Sucesso_ do seu armazenamento.

### Etapa 1. Criar uma tag

1. Faça logon em sua conta do [!DNL Google Tag Manager] e clique no link do contêiner que você criou para sua loja.

1. Na caixa **[!UICONTROL New Tag]**, clique em **[!UICONTROL Add a new tag]**.

1. Obtenha as seguintes informações da sua conta do AdWords:

   - ID de conversão
   - Rótulo de conversão

   Se precisar de ajuda, visite o [site de suporte](https://support.google.com/tagmanager/answer/6105160) da Google.

1. No painel [!DNL Google Tag Manager], clique em **[!UICONTROL Google AdWords]** e faça o seguinte:

   - Clique no espaço reservado do título e insira um nome para a nova tag.

   - Em **[!UICONTROL Choose Product]**, selecione **[!UICONTROL Google AdWords]**.

   - Em _[!UICONTROL Choose a Tag Type]_, selecione **[!UICONTROL AdWords Conversion Tracking]**e clique em **[!UICONTROL Continue]**.

1. Insira o **[!UICONTROL Conversion ID]** e **[!UICONTROL Conversion Label]** da sua conta do AdWords e clique em **[!UICONTROL Continue]**.

### Etapa 2. Criar uma regra

Continuando no painel [!DNL Google Tag Manager], a próxima etapa é criar uma regra que acione a tag na página de conversão.

1. Em **[!UICONTROL Fire On]**, clique em **[!UICONTROL Some Pages]**.

1. Na seção _[!UICONTROL Choose Pages]_, conclua as seguintes configurações:

   - **[!UICONTROL Name]** - Digite um nome para a descrição da página.

   - **[!UICONTROL Variable]** `url`

   - **Operação** - `matches RegEx`

     Para saber mais, consulte [Operadores de seletor de Regex e CSS](https://support.google.com/tagmanager/answer/7679109) na Ajuda do Gerenciador de Tags da Google.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Marque a caixa de seleção verde e clique em **[!UICONTROL Save]**.

   O acionador configurado aparece como um botão azul na seção Acionar.

1. Quando terminar, clique em **[!UICONTROL Save Tag]**.

### Etapa 3. Pré-visualizar e publicar

A próxima etapa do processo é pré-visualizar a tag. Cada vez que a tag é visualizada, um instantâneo da versão é salvo. Quando estiver satisfeito com os resultados, vá para a versão que deseja usar e clique em **[!UICONTROL Publish]**.

## Personalizar tag do HTML com o JavaScript

Esta seção explica como adicionar um Nonce CSP ao HTML Tag JavaScript personalizado para execução na página de check-out, garantindo a conformidade com os requisitos da Política de segurança de conteúdo (CSP). Essa adição melhora a segurança do site, impedindo a execução de scripts não autorizados. Para obter informações mais detalhadas, consulte a documentação da [Política de Segurança de Conteúdo](https://developer.adobe.com/commerce/php/development/security/content-security-policies).

>[!NOTE]
>
>Somente o Adobe Commerce versão 2.4.8 e posterior oferece suporte à importação da variável global `cspNonce` para o Google Tag Manager.

>[!WARNING]
>
>Adicionar scripts desconhecidos ao armazenamento pode comprometer os dados. Os scripts autorizados na página de check-out podem roubar informações confidenciais do cliente, incluindo detalhes de pagamento. É essencial tomar precauções para proteger sua conta do Google Tag Manager. Adicione somente scripts confiáveis, revise e faça auditorias regularmente em suas tags e implemente medidas de segurança rígidas, como autenticação de dois fatores (2FA) e controles de acesso.

### Etapa 1. Criar uma variável Nonce CSP

Você pode criar uma variável CSP Nonce que pode ser usada no Gerenciador de tags da Google importando a configuração da variável ou configurando-a manualmente.

#### Importar a configuração da variável

A variável CSP Nonce está incluída no contêiner de exemplo [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt). Você pode criar a variável importando esse código para o espaço de trabalho.

#### Criar a variável manualmente

Se você não puder importar a configuração da variável, conclua as etapas abaixo para criá-la.

1. No seu espaço de trabalho, navegue até a seção **Variáveis** da barra lateral.
1. Clique no botão **Novo** na parte inferior da página na seção **Variáveis definidas pelo usuário**.
1. Nomeie a variável `gtmNonce`.
1. Clique no ícone de lápis para editar a variável.
1. Selecione **Variável JavaScript** na seção **Variável de página**.
1. No campo **Nome da Variável Global**, digite `window.cspNonce`.
1. Salve a variável.

Para saber mais sobre [Variáveis do Google Tag Manager](https://support.google.com/tagmanager/answer/7683056?hl=en), consulte [Tipos de variáveis definidas pelo usuário para a Web](https://support.google.com/tagmanager/answer/7683362?hl=en) na documentação do Google. Esta documentação oferece orientação detalhada sobre como criar e gerenciar variáveis personalizadas para adaptar seu gerenciamento de tags a necessidades analíticas e de marketing específicas.

### Etapa 2. Criar uma tag HTML personalizada

1. No seu espaço de trabalho, navegue até a seção **Marcas** da barra lateral.
1. Clique no botão **Novo**.
1. Na seção **Configuração de Marca**, selecione **Marca HTML Personalizada**.
1. Insira a JavaScript necessária na área de texto e adicione um atributo nonce à tag de abertura `<script>` que aponte para a variável criada na etapa anterior. Por exemplo:

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. Selecione **Documentos de suporte.write**.
1. Na seção **Acionamento**, selecione o acionador desejado. Por exemplo, **Inicialização de consentimento - Todas as páginas**.

Para obter mais informações sobre [Tags](https://support.google.com/tagmanager/answer/3281060) no Gerenciador de Tags da Google, consulte [Tags personalizadas](https://support.google.com/tagmanager/answer/6107167) na documentação da Google.
