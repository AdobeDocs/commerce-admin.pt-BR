---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Revise as configurações na página [!UICONTROL General] &gt; [!UICONTROL Web] do Administrador do Commerce.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web > Opções Gerais](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Campo | Escopo | Descrição |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | Global | Se as Substituições de Servidor Web estiverem ativadas, insere o Código de armazenamento da exibição atual no URL. Opções: `Yes` / `No`. <br />Quando este campo estiver definido como `Yes`, você deve incluir códigos de armazenamento nas URLs do navegador para garantir que as substituições de URL sejam mapeadas corretamente e que todas as páginas sejam abertas com êxito. Isso evita erros de _404 Página Não Encontrada_. |
| [!UICONTROL Auto-redirect to Base URL] | Exibição da loja | (Para configurações de loja única) Se houver um link quebrado em seu site, o redireciona o tráfego para o URL base, em vez de para uma página com uma mensagem &quot;Página 404 não encontrada&quot;. Opções:` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Importante:_**&#x200B;Não use o redirecionamento automático para a URL de base para configurações de várias lojas. |
| [!UICONTROL Catalog media URL format] | Global | Define o [formato de URL](../../catalog/catalog-urls.md) atribuído aos produtos e categorias. Opções: o hash exclusivo por variante de imagem (modo Herdado) define o nome de arquivo convertido como um valor de hash exclusivo. A otimização de imagem com base em parâmetros de consulta define o processo de [otimização de imagem](../../content-design/media-gallery-image-optimization.md), dependendo dos parâmetros de consulta. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Web > Otimização do mecanismo de pesquisa](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/marketing/seo/url-rewrites/url-rewrite) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | Exibição da loja | Os sistemas baseados em PHP geralmente incluem um arquivo chamado `index.php` na pasta raiz. Por padrão, o nome do arquivo aparece no URL logo após o nome da pasta raiz. Quando habilitado, o sistema omite `index.php` da URL. Essa prática recomendada de usabilidade torna cada URL mais conciso e não tem impacto no desempenho ou na classificação do site. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Web > URLs de base](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Base URL] | Exibição da loja | O endereço completo da pasta raiz do Commerce que não está sendo executada em um canal criptografado (SSL). O URL deve terminar com uma barra. |
| [!UICONTROL Base Link URL] | Exibição da loja | Uma tag de marcação usada como um espaço reservado para o URL de base. |
| [!UICONTROL Base URL for Static View Files] | Exibição da loja | Um caminho que aponta para o local dos arquivos estáticos usados pelo tema, como css, fontes, imagens e JavaScript. Um espaço reservado é usado para representar o URL base. Se a sua instalação do Commerce tiver vários sites com a mesma estrutura de pastas, você poderá ter uma pasta diferente para cada site. Defina o escopo de configuração para o site correto antes de inserir o URL base para arquivos de visualização estáticos. Você também pode especificar uma pasta fora da sua instalação do Commerce. |
| [!UICONTROL Base URL for User Media Files] | Exibição da loja | Um caminho que aponta para o local de imagens de catálogo e outros arquivos de mídia. Um espaço reservado é usado para representar o URL base. Se a sua instalação do Commerce tiver vários sites com a mesma estrutura de pastas, você poderá ter uma pasta de mídia diferente para cada um. Isso lhe dá a capacidade de fazer backup e reverter cada pasta de mídia separadamente. Você também pode especificar uma pasta de mídia fora da sua instalação do Commerce. |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Web > URLs de Base (Seguro)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | Exibição da loja | O endereço completo da pasta raiz do Commerce fornecida com o protocolo SSL/TLS criptografado. O URL deve terminar com uma barra. |
| [!UICONTROL Secure Base Link URL] | Exibição da loja | Uma tag de marcação usada como um espaço reservado para o URL base que é executado em um canal seguro. |
| [!UICONTROL Secure Base URL for Static View Files] | Exibição da loja | Uma tag de marcação que aponta para o local de arquivos estáticos, como CSS, fontes, imagens e JavaScript, usados pelo tema. Os arquivos podem estar em um canal não seguro ou seguro. Se a sua instalação do Commerce tiver vários sites com a mesma estrutura de pastas, você poderá ter uma pasta diferente para cada site. Defina o escopo de configuração para o site correto antes de inserir o URL base para arquivos de visualização estáticos. Você também pode especificar uma pasta fora da sua instalação do Commerce. |
| [!UICONTROL Secure Base URL for User Media Files] | Exibição da loja | Um caminho que aponta para o local de imagens de catálogo e outros arquivos de mídia. Os arquivos podem estar em um canal não seguro ou seguro. Um espaço reservado é usado para representar o URL base. Se a sua instalação do Commerce tiver vários sites com a mesma estrutura de pastas, você poderá ter uma pasta de mídia diferente para cada um. Isso lhe dá a capacidade de fazer backup e reverter cada pasta de mídia separadamente. Você também pode especificar uma pasta de mídia fora da sua instalação do Commerce. |
| [!UICONTROL Use Secure URLs on Storefront] | Exibição da loja | Se o domínio tiver um certificado de segurança, você pode optar por executar a loja com ou sem criptografia SSL. Opções:<br />**`Yes`**- Armazenar URLs começa com `https` para indicar que a página é entregue com protocolo criptografado e seguro.<br />**`No`** - As URLs de armazenamento começam com `http` para indicar que a página é entregue sem protocolo seguro. |
| [!UICONTROL Use Secure URLs in Admin] | Global | Se o domínio tiver um certificado de segurança, você poderá optar por executar o Administrador da loja, com ou sem criptografia SSL. Opções: <br />**`Yes`**- URLs de administradores começam com `https` para indicar que a página é entregue com protocolo criptografado e seguro.<br />**`No`** - URLs de administrador começam com `http` para indicar que a página é entregue sem protocolo seguro.<br /> Quando as URLs seguras estão habilitadas para o armazenamento e para o Administrador, dois campos adicionais parecem habilitar e configurar `HSTS`. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | Exibição da loja | Quando habilitado, o [`HSTS`][1] fornece uma medida de segurança contra ataques do tipo &quot;man in the middle&quot; e impede que os usuários substituam a mensagem de &quot;certificado inválido&quot;. Opções: `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | Exibição da loja | Quando habilitado, converte solicitações não seguras (`HTTP`) recebidas do navegador para o protocolo seguro (`HTTPS`). Opções: `Yes` / `No` |
| [!UICONTROL Offloader Header] | Global | Especifica o valor `offloader_header` na configuração do servidor para identificar o protocolo entre o cliente e o balanceador de carga. A maioria das instalações do Commerce usa o valor padrão, `X-Forwarded-Proto` (XFP) para identificar o protocolo como `HTTP` ou `HTTPS`. |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![Web > Páginas Padrão](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/content-design/elements/pages/pages#configure-default-pages) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | Exibição da loja | Indica a landing page associada ao URL base. Isso é definido por padrão como &quot;cms&quot; para indicar uma página do sistema de gerenciamento de conteúdo (CMS) do Commerce. Você também pode usar um tipo diferente de página de aterrissagem, como um blog. Por exemplo, se um blog estiver instalado no servidor em `magento/blog`, você poderá inserir o nome da pasta &quot;blog&quot; como um caminho relativo para a seleção de páginas. |
| [!UICONTROL CMS Home Page] | Exibição da loja | Para escolher a página inicial da loja, basta selecionar a página do CMS na lista. Por padrão, a Página inicial do CMS lista toda a seleção de páginas do CMS disponíveis para sua loja. |
| [!UICONTROL Default No-route URL] | Exibição da loja | Contém a URL da página padrão que você deseja exibir quando ocorrer um erro `404 Page not Found`. O valor padrão é `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | Exibição da loja | Identifica uma página específica do CMS que deve ser exibida quando ocorrer um erro 404 Página não encontrada. A página padrão é 404 Não encontrado. |
| [!UICONTROL CMS No Cookies Page] | Exibição da loja | Identifica uma página específica do CMS que aparece quando os cookies não estão ativados para o navegador. A página explica por que os cookies são usados e como ativá-los para cada navegador. A página padrão é Ativar cookies. |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | Exibição da loja | Determina se uma trilha de navegação estrutural aparece em todas as páginas do CMS no catálogo. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![Layouts padrão](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/content-design/design/layout/page-layout) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | Global | Determina o [layout](../../content-design/page-layout.md) usado por padrão para páginas de produto. Opções: <br/>**`No layout updates`**- Por padrão, as atualizações de layout não estão disponíveis para páginas de produtos.<br/>**`Empty`** - Por padrão, usa um layout em branco para páginas de produto. <br/>**`1 column`**- Por padrão, usa um layout de coluna única para páginas de produtos.<br/>**`2 columns with left bar`** - Por padrão, usa um layout de duas colunas com a barra lateral à esquerda para páginas de produtos. <br/>**`2 columns with right bar`**- Por padrão, usa um layout de duas colunas com a barra lateral à direita para páginas de produtos.<br/>**`3 columns`** - Por padrão, o usa um layout de três colunas com barras laterais à esquerda e à direita para páginas de produtos.<br/>**`Page -- Full Width`**- (Requer [!DNL Page Builder]) Por padrão, usa o layout Página — Largura total para páginas de produto.<br/>**`Category - Full Width`** - (Requer [!DNL Page Builder]) Por padrão, usa o layout Categoria - Largura total para páginas de produto. <br/>**`Product - Full Width`**- (Requer [!DNL Page Builder]) Por padrão, usa o layout Produto - Largura Total para páginas de produto. |
| [!UICONTROL Default Category Layout] | Global | Determina o [layout](../../content-design/page-layout.md) usado por padrão para páginas de categoria. Opções: <br/>**`No layout updates`**- Por padrão, as atualizações de layout não estão disponíveis para páginas de categoria.<br/>**`Empty`** - Por padrão, usa um layout em branco para páginas de categoria. <br/>**`1 column`**- Por padrão, usa um layout de coluna única para páginas de categoria.<br/>**`2 columns with left bar`** - Por padrão, usa um layout de duas colunas com a barra lateral à esquerda para páginas de categoria. <br/>**`2 columns with right bar`**- Por padrão, usa um layout de duas colunas com a barra lateral à direita para páginas de categoria.<br/>**`3 columns`** - Por padrão, usa um layout de três colunas com barras laterais à esquerda e à direita para páginas de categoria.<br/>**`Page - Full Width`**- (Requer [!DNL Page Builder]) Por padrão, usa o layout Página - Largura Total para páginas de categoria.<br/>**`Category - Full Width`** - (Requer [!DNL Page Builder]) Por padrão, usa o layout Categoria - Largura Total para páginas de categoria. <br/>**`Product - Full Width`**- (Requer [!DNL Page Builder]) Por padrão, usa o layout Produto - Largura Total para páginas de categoria. |
| Layout de página padrão | Global | Determina o [layout](../../content-design/page-layout.md) usado por padrão para páginas do CMS. Opções: <br/>**`No layout updates`**- Por padrão, as atualizações de layout não estão disponíveis para páginas do CMS.<br/>**`Empty`** - Por padrão, usa um layout em branco para páginas do CMS. <br/>**`1 column`**- Por padrão, usa um layout de coluna única para páginas do CMS.<br/>**`2 columns with left bar`** - Por padrão, usa um layout de duas colunas com a barra lateral à esquerda para páginas do CMS.<br/>**`2 columns with right bar`**- Por padrão, usa um layout de duas colunas com a barra lateral à direita para páginas do CMS.<br/>**`3 columns`** - Por padrão, o usa um layout de três colunas com barras laterais à esquerda e à direita para páginas do CMS.<br/>**`Page - Full Width`**- (Requer [!UICONTROL Page Builder]) Por padrão, usa o layout Página - Largura Total para páginas do CMS.<br/>**`Category - Full Width`** - (Requer [!UICONTROL Page Builder]) Por padrão, usa o layout Categoria - Largura total para páginas do CMS. <br/>**`Product - Full Width`**- (Requer [!DNL Page Builder]) Por padrão, usa o layout Produto - Largura Total para páginas do CMS. |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Web > Configurações de cookie padrão](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | Exibição da loja | Determina por quanto tempo um cookie pode existir antes de ser excluído automaticamente. O valor padrão é de 3.600 segundos (1 hora) |
| [!UICONTROL Cookie Path] | Exibição da loja | Especifica as pastas no servidor onde os cookies do Commerce podem ser usados. Para disponibilizar cookies do Commerce em qualquer lugar na instalação, defina o Caminho do cookie como uma única barra: `/`. Este valor pode conter somente o caminho do cookie e **_não pode_** conter nenhum outro parâmetro de cookie. |
| [!UICONTROL Cookie Domain] | Exibição da loja | Determina se os cookies do Commerce estão disponíveis para subdomínios. Por exemplo, para dar suporte a `mysubdomain`.domain.com, digite o nome do seu domínio com um ponto no início, como `.domain.com`. Este valor pode conter somente o domínio do cookie e **_não pode_** conter nenhum outro parâmetro de cookie. |
| [!UICONTROL Use HTTP Only] | Exibição da loja | Determina se os cookies do Commerce podem ser usados somente em um canal não seguro (http) ou também em um canal criptografado (https). Opções: `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Site | Determina se o modo de restrição de cookie está ativado. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Web > Validação de Sessão](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/systems/security/security-session-management#session-validation) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | Global | Verifica se o Endereço IP de uma solicitação corresponde aos dados de `$_SESSION`. A sessão é encerrada se um endereço IP diferente for detectado. Opções: `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | Global | Verifica os dados de proxy recebidos e verifica se o endereço de proxy de uma solicitação corresponde aos dados de `$_SESSION`. A sessão é encerrada se um endereço de proxy diferente for detectado. Opções: `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | Global | Verifica os dados de proxy de saída e verifica se o endereço encaminhado de uma solicitação corresponde aos dados de `$_SESSION`. A sessão é encerrada se um endereço encaminhado-for diferente for detectado. Opções: `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | Global | `USER_AGENT` refere-se ao navegador ou dispositivo usado para acessar o site. Ele verifica se o nome e a versão do navegador e do sistema operacional correspondem aos dados do `$_SESSION`. A sessão é encerrada se um agente do usuário diferente for detectado de uma solicitação para outra na mesma sessão. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![Web > Detecção de Recursos de Navegador](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/systems/security/security-browser-capabilities-detection) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | Exibição da loja | Se os cookies forem desativados pelo navegador, ele será redirecionado automaticamente para a página Nenhum cookie do CMS. Opções: `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | Exibição da loja | Se o JavaScript for desabilitado pelo navegador, ele exibirá um aviso solicitando que o usuário habilite as Opções do JavaScript: `Yes` / `No` (desabilita) |
| [!UICONTROL Show Notice if Local Storage is Disabled] | Exibição da loja | Exibe uma mensagem se o cache local estiver desativado. Opções: `Yes` / `No` |

{style="table-layout:auto"}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
