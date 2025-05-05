---
title: '[!DNL Google Tag Manager]'
description: Saiba como usar [!DNL Google Tag Manager] para gerenciar as muitas tags (trechos de código) relacionadas aos seus eventos campanha de marketing em seus Adobe Systems sites Comércio.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 22a619db0b0673dc520b9bdc5d6cd0c8ffecdf08
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] é uma ferramenta poderosa que o ajuda a gerenciar e implantar várias tags (trechos de código) associadas aos seus eventos campanha de marketing. [!DNL Google Tag Manager] proporciona a capacidade de adicionar rastreamento tags ao seu site para medir o público-alvo ou personalizar, redirecionar ou conduzir iniciativas marketing para mecanismo de pesquisa.

[!DNL Google Tag Manager] transfere diretamente dados e eventos para a [!DNL Google Analytics]Enhanced Ecommerce e outras soluções de análise de terceiros para produzir uma visão clara de quão bem seu site, produtos e promoções estão se saindo.

Você deve ter uma [!DNL Google Analytics] e [!DNL Tag Manager] conta para continuar esse processo. As instruções a seguir o orientam pelo processo de configurar suas contas do Google, configurar suas Comércio armazenamento e criar um tag.

>[!NOTE]
>
>Se sua empresa estiver sujeita a regulamentos de privacidade como o [Regulamento Geral sobre a Proteção de Dados](../getting-started/compliance-gdpr.md) e/ou a Lei[&#128279;](../getting-started/compliance-ccpa.md) de Privacidade do Consumidor da Califórnia, consulte o [Google Privacy Configurações](google-tools.md#google-privacy-settings).

## Etapa 1. Configurar o [!DNL Google Analytics] conta

Consulte [Configurar Search](https://support.google.com/analytics/answer/1012264) do site no Google Ajuda para obter o básico necessário para começar. Consulte também os guias do Google para [Google Analytics](https://support.google.com/analytics/answer/9304153) e [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Entre na sua conta [!DNL Google Analytics].

1. Para habilitar **[!UICONTROL Internal Site Search Tracking]**, faça o seguinte:

   - Navegue até **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Defina **[!UICONTROL Site Search Tracking]** como `On`.

   - Definir parâmetro **[!UICONTROL Query]** como `q`.

   - Ao concluir, **[!UICONTROL Save]** as configurações.

1. Para ativar recursos de exibição, faça o seguinte:

   - Escolha **[!UICONTROL Property Settings]**.

   - Em _[!UICONTROL Advertising Features]_, defina **[!UICONTROL Enable Demographics and Interest Reports]**&#x200B;como `On`.

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

1. Baixe o GTM_M2_Config_json.txt do arquivo [vinculado, abra o arquivo em uma editor e salve-o como `GTM_M2_Config.json`.](./assets/GTM_M2_Config_json.txt)

   O arquivo json é carregado diretamente.[!DNL Google Tag Manager]

1. Navegue até **[!UICONTROL Admin]** > **[!UICONTROL Container]** de > **[!UICONTROL Import Container]**.

1. Clique **[!UICONTROL Choose container file]** e selecione o arquivo json.

1. Em **[!UICONTROL Choose workspace]**, clique **[!UICONTROL New]** em .

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

1. Siga as instruções do Google para publicar o novo container.

## Etapa 3. Configurar o armazenamento

{{gtag-api-note}}

1. Faça logon no Administrador do armazenamento de Comércio.

1. Na barra lateral do __ Administrador, vá até **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Google API]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Google Analytics]** e configure o seguinte:

   ![Configuração de vendas - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Defina **[!UICONTROL Enable]** como `Yes`.

   - Defina **[!UICONTROL Account type]** como `Google Tag Manager`.

   - **[!UICONTROL Container ID]** No campo, insira sua ID GTM (`GTM-xxxxxx`).

   - Se você também estiver usando Google Analytics para conteúdo experimentos, defina **Enable Content Experiments** como `Yes`.

   - Use os valores padrão dos campos restantes.

1. Ao concluir, clique **[!UICONTROL Save Config]** em .

1. Teste suas [!DNL Google Tag Manager] configurações e verifique se tudo funciona corretamente.

>[!NOTE]
>
>Cada container está associada a um site e você só precisa de uma container por conta. Se você tem uma Comércio de vários sites instância, é necessário contêineres separados.

## Descrições de campo

| Campo | Escopo | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable] | Armazenar Exibir | Determina se Google Analytics Comércio eletrônico aprimorado pode ser usado para analisar atividade no seu armazenamento. Opções: `Yes` / `No` |
| [!UICONTROL Account type] | Exibição da loja | Determina o código de rastreamento do Google usado para monitorar a atividade e o tráfego da loja. Opções: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Exibição da loja | Determina se as informações de identificação são removidas dos endereços IP que aparecem nos resultados do Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Exibição da loja | Ativa os Experimentos de conteúdo do Google, que podem ser usados para testar até dez versões diferentes da mesma página. Opções: `Yes` / `No` |
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

   - Em _[!UICONTROL Choose a Tag Type]_, selecione **[!UICONTROL AdWords Conversion Tracking]**&#x200B;e clique em **[!UICONTROL Continue]**.

1. Insira o conta e **[!UICONTROL Conversion Label]** clique **[!UICONTROL Continue]** em **[!UICONTROL Conversion ID]** &quot;AdWords&quot;.

### Etapa 2. Criar uma regra

Continuando desde a [!DNL Google Tag Manager] painel, o próximo passo é criar uma regra que dispara os tag no página de conversão.

1. Em **[!UICONTROL Fire On]**, clique **[!UICONTROL Some Pages]** em .

1. _[!UICONTROL Choose Pages]_&#x200B;Na seção, preencha as seguintes configurações:

   - **[!UICONTROL Name]** - Digite um nome para a descrição da página.

   - **[!UICONTROL Variable]** `url`

   - **Operação** - `matches RegEx`

     Para saber mais, consulte [os operadores](https://support.google.com/tagmanager/answer/7679109) de seletor Regex e CSS na Ajuda do Google Tag Manager.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Selecione a caixa de seleção verde e clique **[!UICONTROL Save]** em .

   O acionador configurado aparece como uma botão azul na seção Ativar.

1. Ao concluir, clique **[!UICONTROL Save Tag]** em .

### Etapa 3. Visualização e publicar

A próxima etapa do processo é pré-visualização o tag. Cada vez que o tag é visualizado, um instantâneo da versão é salvo. Quando estiver satisfeito com os resultados, vá para a versão que deseja usar e clique **[!UICONTROL Publish]** em .

## Personalizar tag HTML com JavaScript

Esta seção explica como adicionar um Nonce CSP à tag HTML personalizada JavaScript para execução no página de checkout, garantindo o cumprimento dos requisitos da Política de Segurança de Conteúdo (CSP). Essa adição aumenta a segurança do site evitando a execução de scripts não autorizados. Para obter informações mais detalhadas, consulte a documentação da [Política](https://developer.adobe.com/commerce/php/development/security/content-security-policies) de segurança de conteúdo.

>[!NOTE]
>
>A importação da variável global para o `cspNonce` Google Tag Manager é suportada apenas na Adobe Systems Comércio versão 2.4.8 e posteriores.

>[!WARNING]
>
>Adicionar scripts desconhecidos às suas armazenamento pode arriscar o compromisso dos dados. Scripts autorizados na página de checkout podem roubar informações confidenciais do cliente, incluindo detalhes do pagamento. É essencial tomar precauções para proteger seus conta do Google Tag Manager. Adicione apenas scripts confiáveis, analise e audite regularmente suas tags e implementar fortes medidas de segurança curtir autenticação de dois fatores (2FA) e controles de acesso.

### Etapa 1. Criar uma variável Nonce CSP

Você pode criar uma variável CSP Nonce que pode ser usada no Gerenciador de tags da Google importando a configuração da variável ou configurando-a manualmente.

#### Importar a configuração da variável

A variável CSP Nonce está incluída no contêiner de exemplo [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt). Você pode criar a variável importando esse código para o espaço de trabalho.

#### Criar a variável manualmente

Se você não puder importar a configuração da variável, conclua as etapas abaixo para criá-la.

1. No espaço de trabalho, navegue até a **seção Variáveis** na barra lateral.
1. Clique na **Novo** botão na parte inferior do página na **seção Variáveis definidas** pelo usuário.
1. Atribua um nome ao variável `gtmNonce`.
1. Clique no ícone de lápis para editar o variável.
1. Selecione **JavaScript Variável** na **seção Página Variável** .
1. No campo Nome **da** Variável global, insira `window.cspNonce`.
1. Salvar o variável.

Para saber mais sobre [&#128279;](https://support.google.com/tagmanager/answer/7683362?hl=en)as Variáveis do Gerenciador de tags do Google, consulte [os tipos de variável definidos](https://support.google.com/tagmanager/answer/7683056?hl=en) pelo usuário para a Web na documentação do Google. Esta documentação oferece orientações detalhadas sobre como criar e gerenciar variáveis personalizadas para adaptar suas gerenciamento de tags para necessidades marketing e analíticas específicas.

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
