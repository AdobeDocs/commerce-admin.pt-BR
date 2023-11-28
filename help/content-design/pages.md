---
title: Páginas
description: Saiba mais sobre os detalhes das principais páginas de conteúdo incluídas com o [!DNL Commerce] loja de demonstração e alteração da configuração das Páginas padrão.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---

# Páginas

O conteúdo pode ser visualizado em termos de prazo de validade, como qualquer produto em uma loja. Você sabia que a vida de prateleira do conteúdo de redes sociais é de menos de 24 horas? A vida útil potencial do conteúdo que você cria pode ajudá-lo a decidir onde investir seus recursos.

O conteúdo com uma longa vida útil às vezes é chamado de _conteúdo permanente_. Exemplos de conteúdo permanente incluem histórias de sucesso de clientes, _como_ instruções e perguntas frequentes. Por outro lado, o conteúdo que é perecível por natureza inclui eventos, notícias do setor e press releases.

![A página Sobre nós incluída com a loja de amostra Luma ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Páginas de conteúdo principal

A variável [!DNL Commerce] a loja de demonstração tem exemplos de páginas de conteúdo principais para ajudar você a começar. Todas essas páginas podem ser modificadas para atender às suas necessidades. Examine as seguintes páginas da loja e verifique se o conteúdo transmite sua mensagem, voz e marca.

### Início

A demonstração [Início](../getting-started/storefront.md#home-page) A página inclui um banner, um carrossel de imagens, vários blocos estáticos com links e uma lista de novos produtos.

### Política de privacidade

A loja [Política de privacidade](../getting-started/privacy-policy.md) A página deve ser atualizada com suas próprias informações. Como prática recomendada, sua política de privacidade deve explicar aos clientes o tipo de informações que sua empresa coleta e como elas são usadas.

### 404 Não encontrado

A página 404 Página não encontrada é nomeada para o código de resposta que é retornado quando uma página não pode ser encontrada. Os redirecionamentos de URL reduzem o número de vezes que esta página é exibida. No entanto, para aqueles momentos em que é necessário, você pode muito bem aproveitar a oportunidade para oferecer alguns links para produtos que o cliente pode achar interessante.

### Acesso negado

{{b2b-feature}}

A variável [Acesso negado](../b2b/account-company-roles-permissions.md) é exibida quando as permissões atribuídas a um usuário da empresa impedem o acesso à página.

### Ativar cookies

A variável [Ativar cookies](../getting-started/compliance-cookie-law.md) é exibida quando os visitantes do site não têm cookies ativados nos navegadores. A página fornece instruções passo a passo e ilustradas para ativar cookies para os navegadores mais populares.

### Serviço indisponível

A variável [Serviço 503 Indisponível](../configuration-reference/general/general.md) A página é nomeada com o código de resposta retornado quando o servidor não está disponível.

### Sobre nós

A página Sobre nós é vinculada a partir do rodapé da sua loja. Você pode incluir imagens, vídeo, links para comunicados de imprensa e anúncios. A página de exemplo tem uma imagem à direita e uma decorativa para indicar o final da página.

### Atendimento ao cliente

A página Atendimento ao cliente é outro nó na hierarquia da página. Os dois cabeçalhos na página têm conteúdo que só se torna visível quando o cliente clica no cabeçalho.

![Página do Atendimento ao cliente na loja](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Configurar páginas padrão

A variável _Páginas padrão_ determina a landing page associada à variável [URL base](../stores-purchase/store-urls.md) e a página inicial correspondente. Também determina qual página aparece quando uma _Página não encontrada_ ocorre um erro e se uma [caminho da navegação estrutural](../catalog/navigation-breadcrumb-trail.md) aparece na parte superior de cada página.

1. No _Admin_ barra lateral, vá para  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Web]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Default Pages]** seção.

   ![Páginas padrão](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Campo | [Escopo](../getting-started/websites-stores-views.md#scope-settings) | Descrição |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Exibição da loja | Indica a landing page associada ao URL base. Por padrão, esse campo está definido como `cms` para indicar uma página do [!DNL Commerce] sistema de gerenciamento de conteúdo. Você também pode usar um tipo diferente de página de aterrissagem, como um blog. Por exemplo, se um blog estiver instalado no servidor em `magento/blog`, você pode inserir o nome da pasta `blog` como um caminho relativo para a seleção de páginas. |
   | [!UICONTROL CMS Home Page] | Exibição da loja | Para escolher a home page da loja, basta selecionar a página CMS na lista. Por padrão, a Página inicial do CMS lista toda a seleção de páginas do CMS disponíveis para sua loja. |
   | [!UICONTROL Default No-route URL] | Exibição da loja | Contém o URL da página padrão que você deseja que apareça quando um `404 Page not Found` ocorre um erro. O valor padrão é `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Exibição da loja | Identifica uma página CMS específica que você deseja que apareça quando ocorrer um erro 404 Página não encontrada. A página padrão é `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Exibição da loja | Identifica uma página CMS específica que aparece quando os cookies não estão ativados para o navegador. A página explica por que os cookies são usados e como ativá-los para cada navegador. A página padrão é `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Exibição da loja | Determina se uma trilha de navegação estrutural aparece em todas as páginas do CMS no catálogo. Opções: `Yes` / `No` |

   {style="table-layout:auto"}

1. Para **[!UICONTROL Default Web URL]**, insira o caminho relativo para a pasta na [!DNL Commerce] instalação que contém a landing page.

   A configuração padrão, `cms`, indica uma página do [!DNL Commerce] sistema de gerenciamento de conteúdo.

   >[!NOTE]
   >
   >Para uma exibição de loja específica, desmarque a opção **[!UICONTROL Use Default]** caixa de seleção ao lado de _[!UICONTROL Default Web URL]_e qualquer outra configuração padrão a ser alterada.

1. Definir **[!UICONTROL CMS Home Page]** à página do CMS que será usada como página inicial. Outras páginas criadas podem ser usadas como página inicial, como:

   - Bem-vindo à Loja Online Exclusiva
   - Pontos de Recompensa
   - Sobre nós
   - Atendimento ao cliente
   - Ativar cookies
   - Política de privacidade
   - Empresa: Acesso Negado

1. Para **[!UICONTROL Default No-route URL]**, insira o caminho relativo para a pasta na [!DNL Commerce] instalação em que a página é redirecionada quando uma _Página 404 Não Encontrada_ ocorre um erro.

   O valor padrão é `cms/index/noRoute`.

1. Definir **[!UICONTROL CMS No Route Page]** para a página do CMS que aparece quando um _Página 404 Não Encontrada_ ocorre um erro.

1. Definir **[!UICONTROL CMS No Cookies Page]** para a página CMS que aparece quando os cookies são desativados no navegador. A página explica por que os cookies são usados e como ativá-los para cada navegador. A página padrão é `Enable Cookies`.

1. Se quiser que uma trilha de navegação estrutural seja exibida na parte superior de todas as páginas do CMS, defina **[!UICONTROL Show Breadcrumbs for CMS Pages]** para `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
