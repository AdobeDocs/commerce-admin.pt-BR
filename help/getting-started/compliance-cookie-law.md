---
title: Conformidade com a lei de cookies
description: Para acompanhar a legislação de muitos países em relação ao uso de cookies, o Adobe Commerce e o Magento Open Source oferecem aos comerciantes uma variedade de métodos para obter o consentimento do cliente.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: abdd70f63ce9ce49ea7e6552951c644480f6024f
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 0%

---

# Conformidade com a lei de cookies

Os cookies são arquivos pequenos que são salvos no computador de cada visitante do site e usados como locais de retenção temporários para obter informações. As informações salvas em cookies são usadas para personalizar a experiência de compra, vincular visitantes aos carrinhos de compras, medir os padrões de tráfego e melhorar a eficácia das promoções. Para acompanhar a legislação de muitos países em relação ao uso de cookies, o Adobe Commerce e o Magento Open Source oferecem aos comerciantes uma variedade de métodos para obter o consentimento do cliente. Para obter uma lista dos cookies padrão no Adobe Commerce e no Magento Open Source, consulte [Referência de cookie](#default-cookies).

>[!NOTE]
>
>Se você modificar as [configurações de privacidade do Google](../merchandising-promotions/google-tools.md#google-privacy-settings) padrão para que estejam em conformidade com o [Regulamento Geral sobre a Proteção de Dados](compliance-gdpr.md), não será necessário obter o consentimento do usuário para o uso de cookies do Google Analytics.

## Modo de restrição de cookies

Quando o modo de restrição de cookies está ativado, os visitantes da sua loja são notificados de que os cookies são necessários para operações com recursos completos. Dependendo do tema, a mensagem pode aparecer acima do cabeçalho, abaixo do rodapé ou em outro lugar na página. A mensagem vincula à sua política de privacidade para obter mais informações e incentiva os visitantes a clicar no botão Permitir para conceder o consentimento. Após o consentimento ser concedido, a mensagem desaparece.

Sua [política de privacidade](privacy-policy.md)) deve incluir o nome de sua loja e informações de contato, e explicar a finalidade de cada cookie usado por sua loja. Para saber mais, consulte [Referência de cookie](#default-cookies).

>[!NOTE]
>
>Se você alterar a chave do URL da política de privacidade, também deverá criar uma regravação de URL personalizada para redirecionar o tráfego para a nova chave do URL. Caso contrário, o link na mensagem Modo de restrição de cookie retornará `404 Page Not Found`.

![Exemplo de vitrine - aviso de restrição de cookies](./assets/storefront-cookie-restriction-message.png){width="600"}

### Etapa 1: Ativar o modo de restrição de cookie

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel de navegação esquerdo, em **[!UICONTROL General]**, escolha **[!UICONTROL Web]**.

1. Expanda a seção **[!UICONTROL Default Cookie Settings]** e faça o seguinte:

   ![Configuração da Web - configurações de cookie padrão](./assets/web-default-cookie-settings.png){width="600"}

   - Insira o **[!UICONTROL Cookie Lifetime]** em segundos.

   - Para disponibilizar cookies para outras pastas, digite o **[!UICONTROL Cookie Path]**. Para disponibilizar os cookies em qualquer lugar do site, insira uma barra (`/`). Este valor pode conter somente o caminho do cookie e **_não pode_** conter nenhum outro parâmetro de cookie.

   - Para disponibilizar os cookies para um subdomínio, insira o nome do subdomínio no campo **[!UICONTROL Cookie Domain]** (`subdomain.yourdomain.com`). Para disponibilizar cookies para todos os subdomínios, insira o nome do domínio precedido por um ponto (`.yourdomain.com`). Este valor pode conter somente o domínio do cookie e **_não pode_** conter nenhum outro parâmetro de cookie.

   - Para impedir que linguagens de script, como JavaScript, obtenham acesso a cookies, verifique se **Usar somente HTTP** está definido como `Yes`.

   - Defina **[!UICONTROL Cookie Restriction Mode]** como `Yes`.

     Se necessário, desmarque a caixa de seleção e clique em **[!UICONTROL OK]** para confirmar a alternância de escopo.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado a atualizar o cache, clique no link **[!UICONTROL Cache Management]** na mensagem do sistema e atualize cada cache inválido.

### Etapa 2: atualizar sua política de privacidade

Atualize sua [política de privacidade](privacy-policy.md) para que ela reflita as informações coletadas por sua empresa e como elas são usadas.

## Cookies padrão

Os cookies padrão no Adobe Commerce e no Magento Open Source são classificados como Isentos/Não Isentos para ajudar os comerciantes a atender aos requisitos de regras de privacidade, como o [GDPR](compliance-gdpr.md). Os comerciantes devem usar essas informações como guia e consultar consultores jurídicos para atualizar suas Políticas de privacidade e cookies como parte de uma estratégia abrangente de conformidade com o regulamento de privacidade.

Os cookies a seguir são usados pelo [!DNL Commerce] &quot;imediatamente&quot; para instalações na nuvem e no local. Esses cookies podem ser exigidos por uma funcionalidade explicitamente solicitada pelo cliente. Para saber mais sobre a duração dos cookies da sessão, consulte [Duração da sessão](../customers/customer-online-options.md).

Alguns desses cookies podem fornecer opções de configuração, incluindo ativar/desativar, conforme necessário.

### Cookies de funcionalidade solicitados (isentos)

#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Captura a SKU, o nome, o preço e a quantidade do produto removidos do carrinho. Permite que o Google Analytics saiba quando um produto foi adicionado ao carrinho.

#### `guest-view`

Vincula um pedido de convidado a um convidado (porque não há conta para convidado).

#### `login_redirect`

Salva o URL de redirecionamento para encaminhar o usuário se o logon e o registro do usuário forem bem-sucedidos. Salva a página em que um usuário estava antes de fazer logon (para determinar o local para o qual ele retornará após fazer logon).

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Armazena conteúdo de banner localmente para melhorar o desempenho. O conteúdo do banner é qualquer conteúdo que um comerciante exibisse em seu site.

#### `mage-messages`

Rastreia mensagens de erro e outras notificações mostradas ao usuário, como a mensagem de consentimento do cookie e várias mensagens de erro. A mensagem é excluída do cookie depois de ser mostrada ao comprador. Não há uma opção para desativar esse cookie. É assim que as informações únicas são comunicadas ao usuário, como mensagens de erro.

#### `product_data_storage` (armazenamento local)

Armazena a configuração de dados de produtos usados para usar as funções &quot;Visualizado recentemente&quot; e &quot;Comparar produtos&quot;. Armazena as configurações específicas de um usuário (por exemplo, se ele visualizou um produto recentemente ou comparou produtos).

#### `recently_compared_product` (armazenamento local)

Armazena IDs de produtos de produtos comparados recentemente.

#### `recently_compared_product_previous` (armazenamento local)

Armazena IDs de produtos comparados anteriormente para facilitar a navegação.

#### `recently_viewed_product` (armazenamento local)

Armazena IDs de produtos visualizados recentemente para facilitar a navegação.

#### `recently_viewed_product_previous` (armazenamento local)

Armazena IDs de produtos visualizados recentemente para facilitar a navegação.

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) permite que a Google Analytics saiba quando um produto foi removido do carrinho.

#### `stf`

Registra as mensagens de hora que são enviadas pelo módulo SendFriend ([Enviar por Email para um Amigo](../stores-purchase/email-a-friend.md)). Quando um comprador envia um link para um produto, esse cookie registra um carimbo de data e hora e mantém uma contagem.

#### `X-Magento-Vary`

Indica quando uma nova versão de uma página precisa ser disponibilizada do cache. Oferece suporte ao desempenho do site.

#### `form_key`

Um mecanismo de segurança que retém um valor gerado aleatoriamente para impedir ataques de falsificação de solicitação entre sites (CSRF), ajudando a determinar se uma solicitação veio de uma fonte original ou de um ator incorreto. Essa é uma prática padrão do setor para impedir ataques de CSRF.

#### `mage-cache-sessid`

Útil para determinar quando limpar o armazenamento local no navegador após a expiração da sessão. Isso é usado para determinar se o armazenamento local deve ser limpo. A ausência desse cookie aciona a limpeza do armazenamento local.

#### `mage-cache-storage`

Armazenamento local de conteúdo específico do visitante que habilita as funções de comércio eletrônico. Não é usado por padrão, mas quando é usado, é usado para agilizar a finalização para que as informações básicas do usuário estejam disponíveis quando alguém sair e retornar.

#### `mage-cache-storage-section-invalidation`

Armazena informações relacionadas às seções da página que precisam ser invalidadas e removidas.

#### `persistent_shopping_cart`

Armazena a ID de chave de um carrinho persistente para possibilitar a restauração do carrinho por um comprador anônimo.

#### `private_content_version`

Acrescenta um número e hora aleatórios e exclusivos às páginas com conteúdo do cliente para impedir que sejam armazenadas em cache no servidor. Ela é definida em vários lugares: no PHP, no JavaScript como um cookie e no JavaScript para armazenamento local.

#### `section_data_ids`

Armazena informações específicas do cliente relacionadas a ações iniciadas pelo comprador, como exibição de lista de desejos e informações de check-out.

#### `store`

Rastreia a exibição/localidade de loja específica selecionada pelo comprador.

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Armazenamento local para a funcionalidade de banner. Banner significa ativos gerais do site e todas as informações exibidas para um comprador.

#### `PHPSESSID`

Rastreia sessões de usuários na loja. Esses são os compradores que usam os produtos finais.

#### `admin`

Rastreia as sessões do usuário no lado do Administrador.

#### `loggedOutReasonCode`

Definido quando um usuário administrador é bloqueado após um determinado número de tentativas de senha malsucedidas.

#### `section_data_clean`

Definido quando um usuário alterna a exibição de armazenamento. A presença desse cookie aciona o JavaScript para recarregar determinadas seções na página para refletir a exibição de armazenamento correta.

#### `lang`

Definido indiretamente pelo módulo Admin Analytics. Sendo usado somente em uma área administrativa de um armazenamento. Não aplicável aos compradores.

#### `s_fid`

Definido indiretamente pelo módulo Admin Analytics. Carimbo de data/hora da ID de visitante único de fallback. É usado para identificar um visitante único se o cookie padrão `s_vi` não estiver disponível devido a restrições de cookies de terceiros. Sendo usado somente em uma área administrativa de um armazenamento. Não aplicável aos compradores.

#### `s_cc`

Definido indiretamente pelo módulo Admin Analytics. Ele é definido e lido pelo código JavaScript para determinar se os cookies estão ativados. Sendo usado somente em uma área administrativa de um armazenamento. Não aplicável aos compradores.

#### `apt.sid`

Definido pela biblioteca Gainsight PX usada indiretamente pelo módulo Admin Analytics. A finalidade desse cookie é permitir o rastreamento de ID de sessão persistente no domínio de nível superior do produto e ele é usado como ID de referência para a sessão ativa. Sendo usado somente em uma área administrativa de um armazenamento. Não aplicável aos compradores.

#### `apt.uid`

Definido pela biblioteca Gainsight PX usada indiretamente pelo módulo Admin Analytics. A finalidade desse cookie é permitir o rastreamento de ID persistente no domínio de nível superior do produto e ele é usado como ID de referência para a entidade do usuário. Sendo usado somente em uma área administrativa de um armazenamento. Não aplicável aos compradores.

#### `s_sq`

Definido indiretamente pelo módulo Admin Analytics. Usado pelo recurso do ClickMap que coleta dados sobre onde os visitantes clicam e no que clicam. Armazena informações de cada clique. Sendo usado somente em uma área administrativa de um armazenamento. Não aplicável aos compradores.

#### `pagebuilder_modal_dismissed`

Definido pelo Módulo do Page Builder. Contém um sinalizador que impede que prompts subsequentes solicitem a um administrador que confirme a abertura de uma determinada ação se o administrador os tiver rejeitado explicitamente antes. Sendo usado somente em uma área administrativa de um armazenamento. Não aplicável aos compradores.

#### `pagebuilder_template_apply_confirm`

Definido pelo Módulo do Page Builder. Contém um sinalizador que impede que prompts subsequentes solicitem a um administrador que confirme a abertura de uma determinada ação se o administrador os tiver rejeitado explicitamente antes. Sendo usado somente em uma área administrativa de um armazenamento. Não aplicável aos compradores.

#### `accordion-&lbrace;VARIABLE&rbrace;-&lbrace;VARIABLE&rbrace;`

Ser usado como parte da implementação da funcionalidade de guias somente em uma área administrativa de uma loja. Não aplicável aos compradores.

## Cookies de recomendações de produto

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Os cookies a seguir são usados pelas Recomendações de Produto para clientes do Adobe Commerce. Estes cookies são instalados com o [módulo DataServices](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg_dnt`: permite [restringir a coleta de dados do Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/developer/setting-cookie) se você tiver um código personalizado para gerenciar o consentimento de cookies no site.
- `user_allowed_save_cookie`: Usado para [modo de restrição de cookies](#cookie-restriction-mode).
- `authentication_flag`: indica se um comprador entrou ou saiu. Este cookie é atualizado ao mesmo tempo que o cookie `dataservices_customer_id`.
- `dataservices_customer_id`: indica se um comprador entrou ou saiu. Este cookie contém o identificador exclusivo do cliente no sistema.
- `dataservices_customer_group`: indica o grupo de um cliente. Este cookie é armazenado como uma soma de verificação [sha1](https://en.wikipedia.org/wiki/SHA-1) da ID de grupo do cliente.
- `dataservices_cart_id`: identifica as ações do carrinho de um comprador. Esse cookie contém a ID de carrinho exclusiva do cliente no sistema.
- `dataservices_product_context`: identifica as interações de produto de um comprador. Este cookie contém a ID de cotação exclusiva do cliente no sistema.

## Cookies adicionais

![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Os cookies a seguir estão definidos para clientes do Adobe Commerce. Estes cookies são instalados com o [módulo DataServices](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg`: Definido pelo rastreador Snowplow JavaScript. Mais informações podem ser encontradas na [documentação do Snowplow](https://docs.snowplow.io/docs/sources/trackers/javascript-trackers/web-tracker/tracker-setup/initialization-options/).
- `com.adobe.alloy.getTld`: Dado o nome de host da página da Web atual, este é o domínio mais alto que não é um &quot;sufixo público&quot;, conforme descrito em https://publicsuffix.org. Essencialmente, esse é o domínio mais alto que pode aceitar cookies. Este cookie faz parte do [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
