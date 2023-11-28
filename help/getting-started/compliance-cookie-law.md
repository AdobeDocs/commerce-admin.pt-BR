---
title: Conformidade com a lei de cookies
description: Para acompanhar a legislação de muitos países em relação ao uso de cookies, a Adobe Commerce e a Magento Open Source oferecem aos comerciantes uma variedade de métodos para obter o consentimento do cliente.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2145'
ht-degree: 0%

---

# Conformidade com a lei de cookies

Os cookies são arquivos pequenos que são salvos no computador de cada visitante do site e usados como locais de retenção temporários para obter informações. As informações salvas em cookies são usadas para personalizar a experiência de compra, vincular visitantes aos carrinhos de compras, medir os padrões de tráfego e melhorar a eficácia das promoções. Para acompanhar a legislação de muitos países em relação ao uso de cookies, a Adobe Commerce e a Magento Open Source oferecem aos comerciantes uma variedade de métodos para obter o consentimento do cliente. Para obter uma lista dos cookies padrão no Adobe Commerce e no Magento Open Source, a variável [Referência de cookie](#default-cookies).

>[!NOTE]
>
>Se você modificar o padrão [Configurações de privacidade do Google](../merchandising-promotions/google-tools.md#google-privacy-settings) para dar cumprimento ao [Regulamento Geral sobre a Proteção de Dados](compliance-gdpr.md), não é necessário obter o consentimento do usuário para o uso de cookies Google Analytics.

## Método 1: consentimento implícito

Consentimento implícito significa que os visitantes da sua loja entendem claramente que os cookies são uma parte necessária das operações e, ao usar o seu site, concederam indiretamente permissão para usá-los. A chave para obter o consentimento implícito é fornecer informações suficientes para que um visitante tome uma decisão informada. Muitas lojas exibem uma mensagem na parte superior de todas as páginas padrão que fornece uma breve visão geral de como os cookies são usados, com um link para a política de privacidade da loja. A política de privacidade deve descrever o tipo de informações que sua loja coleta e como elas são usadas.

## Método 2: consentimento expresso

Operar sua loja em _modo de restrição de cookie_ O exige que os visitantes expressem seu consentimento antes que qualquer cookie possa ser salvo em seus computadores. A menos que o consentimento seja concedido, muitos recursos da loja não estarão disponíveis. Por exemplo, se o Google Analytics estiver disponível para sua loja, ele poderá ser chamado somente após o visitante ter concedido permissão para usar cookies.

## Modo de restrição de cookies

Quando o modo de restrição de cookies está ativado, os visitantes da sua loja são notificados de que os cookies são necessários para operações com recursos completos. Dependendo do tema, a mensagem pode aparecer acima do cabeçalho, abaixo do rodapé ou em outro lugar na página. A mensagem vincula à sua política de privacidade para obter mais informações e incentiva os visitantes a clicar no botão Permitir para conceder o consentimento. Após o consentimento ser concedido, a mensagem desaparece.

Seu [política de privacidade](privacy-policy.md)) deve incluir o nome da sua loja e as informações de contato, e explicar a finalidade de cada cookie usado por sua loja. Para saber mais, consulte [Referência de cookie](#default-cookies).

>[!NOTE]
>
>Se você alterar a chave do URL da política de privacidade, também deverá criar uma regravação de URL personalizada para redirecionar o tráfego para a nova chave do URL. Caso contrário, o link na mensagem Modo de restrição de cookie retornará `404 Page Not Found`.

![Exemplo de vitrine - aviso de restrição de cookie](./assets/storefront-cookie-restriction-message.png){width="600"}

### Etapa 1: Ativar o modo de restrição de cookie

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel de navegação esquerdo, em **[!UICONTROL General]**, escolha **[!UICONTROL Web]**.

1. Expanda a **[!UICONTROL Default Cookie Settings]** e faça o seguinte:

   ![Configuração da Web - configurações de cookie padrão](./assets/web-default-cookie-settings.png){width="600"}

   - Insira o **[!UICONTROL Cookie Lifetime]** em segundos.

   - Se quiser disponibilizar cookies para outras pastas, insira o **[!UICONTROL Cookie Path]**. Para disponibilizar os cookies em qualquer lugar do site, insira uma barra (`/`). Esse valor pode conter somente o caminho do cookie e **_não é possível_** contém quaisquer outros parâmetros de cookie.

   - Para disponibilizar os cookies para um subdomínio, digite o nome do subdomínio no campo **[!UICONTROL Cookie Domain]** campo (`subdomain.yourdomain.com`). Para disponibilizar cookies para todos os subdomínios, digite o nome do domínio precedido por um ponto (`.yourdomain.com`). Esse valor pode conter somente o domínio do cookie e **_não é possível_** contém quaisquer outros parâmetros de cookie.

   - Para impedir que linguagens de script, como JavaScript, obtenham acesso a cookies, verifique se **Usar somente HTTP** está definida como `Yes`.

   - Definir **[!UICONTROL Cookie Restriction Mode]** para `Yes`.

     Se necessário, desmarque a caixa de seleção e clique em **[!UICONTROL OK]** para confirmar a alternância do escopo.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando for solicitado que você atualize o cache, clique na guia **[!UICONTROL Cache Management]** na mensagem do sistema. Em seguida, atualize cada cache inválido.

### Etapa 2: atualizar sua política de privacidade

Atualize seu [política de privacidade](privacy-policy.md) para que reflita as informações coletadas por sua empresa e como elas são usadas.

## Cookies padrão

Os cookies padrão no Adobe Commerce e no Magento Open Source são classificados como Isentos/Não isentos para ajudar os comerciantes a atender aos requisitos de regulamentos de privacidade, como o [GDPR](compliance-gdpr.md). Os comerciantes devem usar essas informações como guia e consultar consultores jurídicos para atualizar suas Políticas de privacidade e cookies como parte de uma estratégia abrangente de conformidade com o regulamento de privacidade.

Os seguintes cookies são usados pelo [!DNL Commerce] &quot;pronto para uso&quot; para instalações no local e em nuvem. Esses cookies podem ser exigidos por uma funcionalidade explicitamente solicitada pelo cliente. Para saber mais sobre a duração dos cookies da sessão, consulte [Duração da sessão](../customers/customer-online-options.md).

Alguns desses cookies podem fornecer opções de configuração, incluindo ativar/desativar, conforme necessário.

### Cookies de funcionalidade solicitados (isentos)


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Usado pelo Google Tag Manager. Registra o SKU, o nome, o preço e a quantidade do produto removidos do carrinho e disponibiliza as informações para integração futura por scripts de terceiros.

#### `guest-view`

Armazena a ID do pedido que os compradores convidados usam para recuperar o status do pedido. Exibição de pedidos de convidado. Usado em _[!DNL Orders and Returns]_widgets.

- É Seguro? Não
- Somente HTTP: Sim
- Política de expiração: sessão
- Módulo: `Magento_Sales`

#### `login_redirect`

Preserva a página de destino que estava sendo carregada antes que o cliente fosse direcionado para fazer logon. Um redirecionamento de login é usado com o mini carrinho para clientes conectados se a variável [Exibir Mini Carrinho](../stores-purchase/cart-configuration.md#mini-cart) a opção de configuração está definida como `Yes`.

- É Seguro? Não
- Somente HTTP: Não
- Política de expiração: sessão
- Módulo: `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Somente no Adobe Commerce) Armazena conteúdo de banner localmente para melhorar o desempenho.

#### `mage-messages`

Rastreia mensagens de erro e outras notificações mostradas ao usuário, como a mensagem de consentimento do cookie e várias mensagens de erro. A mensagem é excluída do cookie depois de ser mostrada ao comprador.

Não há uma opção para desativar esse cookie.

- É Seguro? Não
- Somente HTTP: Não
- Política de expiração: duração de 1 ano. Limpo no front-end quando a mensagem é exibida para o usuário.
- Módulo: `Magento_Theme`

#### `mage-translation-storage` (armazenamento local)

Armazena conteúdo traduzido quando solicitado pelo comprador. Usado quando [Estratégia de tradução](../configuration-reference/advanced/developer.md) está configurado como &quot;Dicionário (tradução na loja)&quot;.

- É Seguro? Não
- Somente HTTP: Não
- Política de Expiração: por regras de armazenamento local
- Módulo: `Magento_Translation`

#### `mage-translation-file-version` (armazenamento local)

Rastreia a versão das traduções no armazenamento local. Usado quando [Estratégia de tradução](../configuration-reference/advanced/developer.md) está configurado como `Dictionary (Translation on Storefront side)`.

- É Seguro? Não
- Somente HTTP: Não
- Política de Expiração: por regras de armazenamento local
- Módulo: `Magento_Translation`

#### `product_data_storage` (armazenamento local)

Armazena a configuração de dados de produtos relacionados a Produtos visualizados/comparados recentemente.

- É Seguro? Não
- Somente HTTP: Não
- Política de Expiração: por regras de armazenamento local
- Módulo: `Magento_Catalog`

#### `recently_compared_product` (armazenamento local)

Armazena IDs de produtos de produtos comparados recentemente.

- É Seguro? Não
- Somente HTTP: Não
- Política de Expiração: por regras de armazenamento local
- Módulo: `Magento_Catalog`

#### `recently_compared_product_previous` (armazenamento local)

Armazena IDs de produtos comparados anteriormente para facilitar a navegação.

- É Seguro? Não
- Somente HTTP: Não
- Política de Expiração: por regras de armazenamento local
- Módulo: `Magento_Catalog`

#### `recently_viewed_product` (armazenamento local)

Armazena IDs de produtos visualizados recentemente para facilitar a navegação.

- É Seguro? Não
- Somente HTTP: Não
- Política de Expiração: por regras de armazenamento local
- Módulo: `Magento_Catalog`

#### `recently_viewed_product_previous` (armazenamento local)

Armazena IDs de produtos visualizados recentemente para facilitar a navegação.

- É Seguro? Não
- Somente HTTP: Não
- Política de Expiração: por regras de armazenamento local
- Módulo: `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Usado por [Gerenciador de tags da Google](../merchandising-promotions/google-tag-manager.md). Registra o SKU, o nome, o preço e a quantidade do produto adicionados ao carrinho, e disponibiliza as informações para integração futura por scripts de terceiros.

#### `stf`

Registra as horas em que as mensagens são enviadas pelo SendFriend ([Enviar para um amigo](../stores-purchase/email-a-friend.md)).

- É Seguro? Sim
- Somente HTTP: Sim
- Política de expiração: sessão
- Módulo: `Magento_SendFriend`

#### `X-Magento-Vary`

Configuração que melhora o desempenho ao usar o cache de conteúdo estático do Varnish.

- É Seguro? Sim
- Somente HTTP: Sim
- Política de expiração: baseada na configuração do PHP session.cookie_lifetime
- Módulo: `Magento_PageCache`

#### `form_key`

Uma medida de segurança que anexa uma sequência aleatória a todos os envios de formulário para proteger os dados da CSRF (Falsificação de solicitação entre sites).

- É Seguro? Não
- Somente HTTP: Não
- Política de expiração:
   - PHP: baseado na configuração do PHP session.cookie_lifetime
   - JS: Session
- Módulo: Cache de página

#### `mage-cache-sessid`

O valor desse cookie aciona a limpeza do armazenamento de cache local. Quando o cookie é removido pelo aplicativo de back-end, o Administrador limpa o armazenamento local e define o valor do cookie como `true`.

- É Seguro? Não
- Somente HTTP: Não
- Política de expiração: sessão
- Módulo: `Magento_Customer`

#### `mage-cache-storage`

Armazenamento local de conteúdo específico do visitante que habilita as funções de comércio eletrônico.

- É Seguro? Não
- Somente HTTP: Não
- Política de expiração: sessão
- Módulo: `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage` (armazenamento local)

Armazenamento local de conteúdo específico do visitante que habilita as funções de comércio eletrônico.

- É Seguro? Não
- Somente HTTP: Não
- Política de expiração: sessão
- Módulo: `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` (armazenamento local)

Força o armazenamento local de seções de conteúdo específicas que devem ser invalidadas.

- É Seguro? Não
- Somente HTTP: Não
- Política de Expiração: por armazenamento local
- Módulo: `Magento_Customer`

#### `persistent_shopping_cart`

Armazena a chave (ID) do carrinho persistente para permitir a restauração do carrinho por um comprador anônimo.

- É Seguro? Sim
- Somente HTTP: Sim
- Política de expiração: com base em [Carrinho de compras persistente](../stores-purchase/cart-persistent.md) - Configuração de duração da persistência (segundos)
- Módulo: `Magento_Persistent`

#### `private_content_version`

Acrescenta um número e hora aleatórios e exclusivos às páginas com conteúdo do cliente para impedir que sejam armazenadas em cache no servidor.

Ela é definida em vários lugares: no PHP, no JavaScript como um cookie e no JavaScript como armazenamento local.

Somente para HTTP=`Yes` (com base na solicitação ), significa que o cookie é seguro se definido durante a solicitação HTTPS e inseguro se definido durante a solicitação HTTP.

- É Seguro? `Yes` (com base no pedido), `No`
- Somente HTTP: `No`
- Política de expiração: com base em [Carrinho de compras persistente](../stores-purchase/cart-persistent.md) - Configuração de duração da persistência (segundos)
   - PHP: `1` ano / `315360000s` (dez anos)
   - JS: `1` dia
   - Armazenamento local JS: por regras de armazenamento local (para sempre)
- Módulo: `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

Armazena informações específicas do cliente relacionadas a ações iniciadas pelo comprador, como exibição de lista de desejos e informações de check-out.

- É Seguro? `No`
- Somente HTTP: `No`
- Política de expiração: `Session`
- Módulo: `Magento_Customer`

#### `store`

Rastreia a exibição/localidade da loja específica selecionada pelo comprador.

- É Seguro? `No`
- Somente HTTP: `Yes`
- Política de expiração: `1` ano
- Módulo: `Magento_Store`

#### `mage-banners-cache-storage` - armazenamento local

![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Armazenamento local para a funcionalidade Banner.

- É Seguro? `No`
- Somente HTTP: `No`
- Política de Expiração: por regras de armazenamento local
- Módulo: `Magento_Banner`

## cookies do Google Analytics

Os seguintes cookies são usados quando [Google Analytics](../merchandising-promotions/google-analytics.md) ou o Google Universal Analytics está totalmente ativado para a sua instalação. Para desativar esses cookies para conformidade com o regulamento de privacidade, consulte [Configurações de privacidade do Google](../merchandising-promotions/google-tools.md#google-privacy-settings). Para saber mais, consulte [Uso de cookies do Google Analytics em sites][1].

### Cookies do Google Universal Analytics - não isentos

![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Bibliotecas de JavaScript: `gtag.js` e `analytics.js`

- `_ga`: diferencia visitantes do site.
- `_gid`: diferencia visitantes do site.
- `gat`: usado para limitar a taxa de solicitação.
- `dc_gtm_<property-id>`: acelera a taxa de solicitação quando o Google Analytics é implantado com [Gerenciador de tags da Google](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`: contém um token que pode ser usado para recuperar uma ID do cliente do serviço de ID do cliente do AMP. Outros valores possíveis incluem recusa, solicitação de transferência ou um erro ao recuperar uma ID do cliente do serviço de ID do cliente da AMP.
- `_gac_<property-id>`: contém informações relacionadas à campanha para o usuário. As tags de conversão do Google AdWords leem este cookie se o Google Analytics estiver vinculado à [AdWord][2] conta.

### Cookies Google Analytics - não isentos

![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Biblioteca JavaScript: `ga.js`

- `__utma`: diferencia compradores e sessões. Esse cookie é criado quando a biblioteca do JavaScript é executada e não há cookies `__utma` cookie. O cookie é atualizado sempre que os dados são enviados para o Google Analytics.
- `__utmt`: usado para limitar a taxa de solicitação.
- `__utmb`: determina novas sessões/visitas. Esse cookie é criado quando a biblioteca do JavaScript é executada e não há cookies `__utmb` cookie. O cookie é atualizado sempre que os dados são enviados para o Google Analytics.
- `_utmz`: salva a fonte de tráfego ou campanha que explica como o comprador chegou ao site. O cookie é criado quando a biblioteca JavaScript do é executada e é atualizado sempre que os dados são enviados para o Google Analytics.
- `__utmv`: armazena dados de variáveis personalizadas no nível do visitante. Este cookie é criado quando um desenvolvedor usa o `_setCustomVar` com uma variável personalizada de nível de visitante. Este cookie é atualizado sempre que os dados são enviados para o Google Analytics.

## Cookies do Recommendations do produto

![Adobe Commerce](../assets/adobe-logo.svg) (Somente no Adobe Commerce) Os cookies a seguir são usados pelo Recommendations do produto para clientes do Adobe Commerce. Esses cookies são instalados com o [Módulo DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`: permite [restringir a coleta de dados do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) se você tiver um código personalizado para gerenciar o consentimento do cookie em seu site.
- `user_allowed_save_cookie`: Usado para [modo de restrição de cookie](#cookie-restriction-mode).
- `authentication_flag`: indica se um comprador entrou ou saiu. Este cookie é atualizado ao mesmo tempo que a variável `dataservices_customer_id` cookie.
- `dataservices_customer_id`: indica se um comprador entrou ou saiu. Este cookie contém o identificador exclusivo do cliente no sistema.
- `dataservices_customer_group`: indica o grupo de um cliente. Este cookie é armazenado como [sha1](https://en.wikipedia.org/wiki/SHA-1) soma de verificação da ID de grupo do cliente.
- `dataservices_cart_id`: identifica as ações do carrinho de um comprador. Esse cookie contém a ID de carrinho exclusiva do cliente no sistema.
- `dataservices_product_context`: identifica as interações de produto de um comprador. Este cookie contém a ID de cotação exclusiva do cliente no sistema.

## Cookies adicionais

![Adobe Commerce](../assets/adobe-logo.svg) (Somente no Adobe Commerce) Os seguintes cookies são definidos para clientes do Adobe Commerce. Esses cookies são instalados com o [Módulo DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`: Definido pelo rastreador de JavaScript do Snowplow. Mais informações podem ser encontradas no [Documentação do Snowplow](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`: Considerando o nome de host da página da Web atual, esse é o domínio mais importante que não é um &quot;sufixo público&quot;, conforme descrito em https://publicsuffix.org. Essencialmente, esse é o domínio mais alto que pode aceitar cookies. Este cookie faz parte da [SDK da Web da Alloy](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
