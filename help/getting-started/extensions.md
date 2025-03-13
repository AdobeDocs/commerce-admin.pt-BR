---
title: Extensões do Adobe
description: Revise informações sobre extensões para o Adobe Commerce e o Magento Open Source lançadas pela Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Extensões do Adobe

Este tópico fornece informações sobre extensões para o Adobe Commerce e o Magento Open Source lançadas pela Adobe. As extensões adicionam recursos, funcionalidades, serviços e integrações ao Administrador e à loja. Algumas dessas extensões são desenvolvidas por meio das contribuições da Comunidade da Magento Open Source. Algumas extensões exigem instalação separada e outras são instaladas por padrão.

## Extensões instaladas

Algumas extensões são instaladas automaticamente com o Adobe Commerce ou Magento Open Source.

### [!DNL Inventory Management]

O [!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) oferece gerenciamento avançado de estoque e remessa em um ou vários locais e canais de vendas com proteção de check-out simultâneo e algoritmos de correspondência de remessa. Rastreie as quantidades de inventário, forneça aos clientes quantias exatas de estoque comercializável e faça entregas de acordo com as recomendações ou seleções manuais para controlar todo o inventário. Definir configurações de gerenciamento globalmente, por origem e por produto.

>[!NOTE]
>
>Esta extensão foi desenvolvida como parte do projeto [[!DNL Inventory Management]](https://github.com/magento/inventory) (anteriormente MSI) por meio do programa de Engenharia da Comunidade.

O [!DNL Inventory Management] é instalado com todos os recursos habilitados por padrão. Não são necessárias etapas adicionais para habilitar esses recursos de inventário. Para obter detalhes sobre os recursos do [!DNL Inventory Management], consulte o [[!DNL Inventory Management] Guia do Usuário](../inventory-management/guide-overview.md).

### Braintree

PayPal e Gene Commerce desenvolveram juntos a extensão oficial do Braintree para as lojas Commerce 2.4.x. Apresentando uma experiência de checkout aprimorada projetada para impulsionar a conversão, as atualizações incluem opções do PayLater que mostram automaticamente mensagens e botões relevantes do PayLater para os consumidores durante as compras e durante o checkout.

Esta extensão é instalada por padrão, mas requer uma [conta do Braintree](https://www.braintreepayments.com/) e a configuração no Administrador para ser habilitada para sua loja. Para determinar as tarifas que se aplicam ao usar o Braintree para processar suas transações, verifique o [preço do Braintree](https://www.braintreepayments.com/braintree-pricing).

Para obter informações sobre a configuração do Braintree no Administrador, consulte o tópico do [Braintree](../stores-purchase/braintree.md) no _Guia de Experiência de Vendas e Compras_.

### Google reCAPTCHA

O Google reCAPTCHA fornece um nível maior de segurança para a vitrine e a interface do usuário do administrador do que o disponível com o CAPTCHA padrão e oferece a capacidade de:

- Verifique quando os clientes criam contas, recuperam senhas, fazem logon em suas contas ou entram em contato com sua empresa.
- Aumente a segurança quando os usuários administradores fizerem logon.

Ele reduz possíveis erros do usuário ao inserir um código Captcha e incentiva a conversão do carrinho sem adicionar barreiras durante o checkout. [Habilite e configure o reCAPTCHA](../systems/security-google-recaptcha.md) usando verificações invisíveis ou interativas para aprimorar o acesso seguro ao Administrador e à loja do [!DNL Commerce].

### Autenticação de dois fatores

O Administrador do [!DNL Commerce] fornece todo o acesso à sua loja, pedidos e dados do cliente. A [Autenticação de dois fatores](../systems/security-two-factor-authentication.md) (2FA ou TFA) melhora a segurança exigindo autenticação adicional, além do nome de logon e da senha padrão, para acessar o Administrador [!DNL Commerce] de todos os dispositivos. A extensão dá suporte a vários autenticadores, incluindo o Autenticador do Google, Authy, [!DNL Duo] e chaves U2F. Essa autenticação se aplica somente aos usuários administradores. Não está disponível para contas de clientes da loja.

Esses recursos são ativados por padrão. Cada usuário administrador deve instalar e configurar um dos autenticadores compatíveis.

>[!NOTE]
>
>As lojas Adobe Commerce que habilitaram a autenticação do Adobe Identity Management Services (IMS) para o Administrador têm o Commerce 2FA nativo desabilitado. Os usuários que estão conectados ao Administrador com suas credenciais do Adobe não precisam se autenticar novamente para muitas tarefas de Administrador. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [Visão Geral da Integração do Adobe Identity Management Service (IMS)](./adobe-ims-integration-overview.md).

## Extensões para adicionar

O [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) é o recurso de comércio eletrônico global para aplicativos e serviços que expandem as soluções do [!DNL Commerce] com novos recursos e funcionalidades avançados. A Adobe lança várias extensões por meio do [!DNL Marketplace] que podem ser instaladas e configuradas na loja da Adobe Commerce ou da Magento Open Source para fornecer integrações e recursos aprimorados.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) somente Adobe Commerce

A extensão do [!DNL Live Search] conecta sua loja ao serviço Live Search, uma plataforma de pesquisa gratuita da Adobe Commerce que capacita os vendedores para fornecer aos clientes uma experiência de pesquisa com IA. Criado com a inteligência artificial do Adobe, o Adobe Sensei, o Intelligent Faceting ajuda os comerciantes a fazer mais com menos, removendo o trabalho manual sobre facetas/filtragens.

Consulte o [Guia do Usuário do Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html) para obter mais informações.

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) somente Adobe Commerce

A extensão do [!DNL Product Recommendations] conecta sua loja ao serviço de recomendações de produtos, uma ferramenta de marketing poderosa que você pode usar para aumentar as conversões, a receita e o envolvimento. O [!DNL Product Recommendations] foi criado pela Adobe Commerce e é impulsionado por sua inteligência artificial testada em batalha, o Adobe Sensei, para que você possa impulsionar o engajamento e a conversão com confiança. Esse recurso remove o trabalho manual necessário para fazer recomendações relevantes do produto para cada comprador.

Consulte o [[!DNL Product Recommendations] Guia do Usuário](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=en) para obter mais informações.

### [!DNL Catalog Service]

O [!DNL Catalog Service] permite que você forneça aos clientes uma experiência de produto otimizada enquanto aumenta o desempenho, melhora a escalabilidade e aumenta as conversões. Consulte o [[!DNL Catalog Service] Guia do Usuário](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html) para obter mais informações.

### [!DNL Payment Services]

O [!DNL Payment services] for Adobe Commerce e Magento Open Source é uma solução de pagamento totalmente integrada que simplifica o processo de gerenciamento de pagamentos e oferece aos clientes a oportunidade de pagar à sua maneira. Reconcilie com segurança todos os dados de pagamento e transação com o administrador do Adobe Commerce, permitindo gerenciar pedidos e pagamentos em um único local e, ao mesmo tempo, fornecer um check-out perfeito. Consulte o [[!DNL Payment Services] Guia do Usuário](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html) para obter mais informações.

### [!DNL Store Fulfillment]

O Atendimento da loja para Adobe Commerce e Magento Open Source permite uma compra on-line superior, coleta na loja (BOPIS) e maximiza a produtividade dos funcionários ao fornecer um fluxo de trabalho de atendimento abrangente, habilitado por meio de um dispositivo móvel. Consulte o [[!DNL Store Fulfillment] Guia do Usuário](https://experienceleague.adobe.com/docs/commerce/store-fulfillment/guide-overview.html) para obter mais informações.

### [!DNL Amazon Sales Channel]

O [!DNL Amazon Sales Channel] for Adobe Commerce permite que você integre seu banco de dados do Amazon Seller Central com seu catálogo de produtos [!DNL Commerce] e gerencie suas listas e vendas do Amazon no Administrador do Commerce. Consulte o [[!DNL Amazon Sales] Guia do Usuário](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) para obter mais informações.

### [!DNL Channel Manager]

O [!DNL Channel Manager] permite que você aumente as vendas, alcance novos clientes, simplifique as operações e economize tempo integrando um catálogo de produtos Adobe Commerce ou Magento Open Source ao Walmart Marketplace. Após instalar e configurar a extensão, sua equipe poderá gerenciar facilmente listagens, estoque, pedidos, devoluções e reembolsos do Walmart Marketplace no [!DNL Commerce Admin]. Consulte o [[!DNL Channel Manager] Guia do Usuário](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) para obter mais informações.
