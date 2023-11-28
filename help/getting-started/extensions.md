---
title: Extensões do Adobe
description: Revise as informações sobre as extensões para o Adobe Commerce e o Magento Open Source lançado pelo Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: c22ad5c3220f14588131d6b29a88dab3c5347681
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# Extensões do Adobe

Este tópico fornece informações sobre extensões para o Adobe Commerce e o Magento Open Source lançadas pelo Adobe. As extensões adicionam recursos, funcionalidades, serviços e integrações ao Administrador e à loja. Algumas dessas extensões são desenvolvidas por meio de contribuições da Comunidade Magento Open Source. Algumas extensões exigem instalação separada e outras são instaladas por padrão.

## Extensões instaladas

Algumas extensões são instaladas automaticamente com o Adobe Commerce ou o Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) O oferece gerenciamento aprimorado de estoque e remessa em um ou vários locais e canais de vendas com proteção de finalização de compra simultânea e algoritmos de correspondência de remessa. Rastreie as quantidades de inventário, forneça aos clientes quantias exatas de estoque comercializável e faça entregas de acordo com as recomendações ou seleções manuais para controlar todo o inventário. Definir configurações de gerenciamento globalmente, por origem e por produto.

>[!NOTE]
>
>Esta extensão foi desenvolvida no âmbito do [[!DNL Inventory Management]](https://github.com/magento/inventory) (anteriormente MSI) através do programa comunitário de engenharia.

[!DNL Inventory Management] O é instalado com todos os recursos ativados por padrão. Não são necessárias etapas adicionais para habilitar esses recursos de inventário. Para obter detalhes sobre o [!DNL Inventory Management] recursos, consulte a [[!DNL Inventory Management] Guia do usuário](../inventory-management/guide-overview.md).

### Braintree

Juntos, PayPal e Gene Commerce desenvolveram a extensão Braintree oficial para lojas Commerce 2.4.x. Apresentando uma experiência de checkout aprimorada projetada para impulsionar a conversão, as atualizações incluem opções do PayLater que mostram automaticamente mensagens e botões relevantes do PayLater para os consumidores durante as compras e durante o checkout.

Esta extensão é instalada por padrão, mas requer um [conta Braintree](https://www.braintreepayments.com/) e a configuração no Admin a ser habilitada para sua loja. Para determinar as tarifas que se aplicam ao usar o Braintree para processar suas transações, marque a opção [preços de Braintree](https://www.braintreepayments.com/braintree-pricing).

Para obter informações sobre a configuração do Braintree em Admin, consulte [Braintree](../stores-purchase/braintree.md) tópico no _Guia de experiência de vendas e compras_.

### Google reCAPTCHA

O Google reCAPTCHA fornece um nível maior de segurança para a vitrine e a interface do usuário do administrador do que o disponível com o CAPTCHA padrão e oferece a capacidade de:

- Verifique quando os clientes criam contas, recuperam senhas, fazem logon em suas contas ou entram em contato com sua empresa.
- Aumente a segurança quando os usuários administradores fizerem logon.

Ele reduz possíveis erros do usuário ao inserir um código Captcha e incentiva a conversão do carrinho sem adicionar barreiras durante o checkout. [Ativar e configurar o reCAPTCHA](../systems/security-google-recaptcha.md) utilizar controlos invisíveis ou interativos para melhorar o acesso seguro ao [!DNL Commerce] Administrador e loja.

### Autenticação de dois fatores

A variável [!DNL Commerce] O administrador fornece todo o acesso à loja, aos pedidos e aos dados do cliente. [Autenticação de dois fatores](../systems/security-two-factor-authentication.md) (2FA ou TFA) melhora a segurança exigindo autenticação adicional, além do nome e da senha padrão de logon, para acessar o [!DNL Commerce] Administrador de todos os dispositivos. A extensão oferece suporte a vários autenticadores, incluindo Google Authenticator, Authy, [!DNL Duo], e chaves U2F. Essa autenticação se aplica somente aos usuários administradores. Não está disponível para contas de clientes da loja.

Esses recursos são ativados por padrão. Cada usuário administrador deve instalar e configurar um dos autenticadores compatíveis.

>[!NOTE]
>
>As lojas Adobe Commerce que habilitaram a autenticação IMS (Adobe Identity Management Services) para o Administrador têm o Commerce 2FA nativo desabilitado. Os usuários que estão conectados ao Administrador com suas credenciais de Adobe não precisam se autenticar novamente para muitas tarefas de Administrador. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [Visão geral da integração do Adobe Identity Management Service (IMS)](./adobe-ims-integration-overview.md).

## Extensões para adicionar

A variável [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) é o recurso de comércio eletrônico global para aplicativos e serviços que se expandem [!DNL Commerce] com novos recursos e funcionalidades avançados. O Adobe lança várias extensões por meio do [!DNL Marketplace] que pode ser instalado e configurado na Adobe Commerce ou na Magento Open Source store para fornecer integrações e recursos aprimorados.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Somente Adobe Commerce

A variável [!DNL Live Search] A extensão do conecta sua loja ao serviço Live Search, uma plataforma de pesquisa gratuita da Adobe Commerce que capacita os vendedores de forma contínua a fornecer aos clientes uma experiência de pesquisa aprimorada por IA. Criada com a inteligência artificial Adobe, a Adobe Sensei e a Intelligent Faceting ajudam os comerciantes a fazer mais com menos, removendo o trabalho manual sobre facetas/filtragens.

Consulte a [Guia do usuário do Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) para obter mais informações.

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Somente Adobe Commerce

A variável [!DNL Product Recommendations] A extensão do conecta sua loja ao serviço Recommendations de produtos, uma ferramenta de marketing poderosa que você pode usar para aumentar as conversões, a receita e o envolvimento. [!DNL Product Recommendations] O foi criado pela Adobe Commerce e é impulsionado por sua inteligência artificial testada em batalha, o Adobe Sensei, para que você possa impulsionar o engajamento e a conversão com confiança. Esse recurso remove o trabalho manual necessário para fazer recomendações relevantes do produto para cada comprador.

Consulte a [[!DNL Product Recommendations] Guia do usuário](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) para obter mais informações.

### [!DNL Catalog Service]

A variável [!DNL Catalog Service] O permite que você forneça aos clientes uma experiência de produto otimizada enquanto aumenta o desempenho, melhora a escalabilidade e aumenta as conversões. Consulte a [[!DNL Catalog Service] Guia do usuário](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) para obter mais informações.

### [!DNL Payment Services]

[!DNL Payment services] O para Adobe Commerce e Magento Open Source é uma solução de pagamento totalmente integrada que simplifica o processo de gerenciamento de pagamentos e oferece aos clientes a oportunidade de pagar do seu jeito. Reconcilie com segurança todos os dados de pagamento e transação com o administrador do Adobe Commerce, permitindo gerenciar pedidos e pagamentos em um único local e, ao mesmo tempo, fornecer um check-out perfeito. Consulte a [[!DNL Payment Services] Guia do usuário](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) para obter mais informações.

### [!DNL Quick Checkout]

[!DNL Quick Checkout] O para Adobe Commerce oferece uma experiência de check-out perfeita, projetada para converter compradores convidados únicos em titulares de conta fiéis.
Consulte a [[!DNL Quick Checkout] Guia do usuário](https://experienceleague.adobe.com/docs/commerce-merchant-services/quick-checkout/overview.html) para obter mais informações.

### [!DNL Store Fulfillment]

O Atendimento da loja para Adobe Commerce e Magento Open Source permite uma compra on-line superior, coleta na loja (BOPIS) experiência do cliente e maximiza a produtividade do funcionário, fornecendo um fluxo de trabalho de atendimento abrangente ativado por meio de um dispositivo móvel. Consulte a [[!DNL Store Fulfillment] Guia do usuário](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) para obter mais informações.

### [!DNL Amazon Sales Channel]

A variável [!DNL Amazon Sales Channel] O para Adobe Commerce permite integrar seu banco de dados da lista do Amazon Seller Central ao seu [!DNL Commerce] catálogo de produtos e gerencie suas listas e vendas do Amazon no Administrador do Commerce. Consulte a [[!DNL Amazon Sales] Guia do usuário](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) para obter mais informações.

### [!DNL Channel Manager]

[!DNL Channel Manager] O permite aumentar as vendas, alcançar novos clientes, simplificar as operações e economizar tempo, integrando um catálogo de produtos Adobe Commerce ou Magento Open Source ao Walmart Marketplace. Após instalar e configurar a extensão, sua equipe poderá gerenciar facilmente as listagens, o inventário, os pedidos, as devoluções e os reembolsos do Walmart Marketplace [!DNL Commerce Admin]. Consulte a [[!DNL Channel Manager] Guia do usuário](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) para obter mais informações.
