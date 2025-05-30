---
title: Extensões do Adobe
description: Revise informações sobre extensões para o Adobe Commerce e o Magento Open Source lançadas pela Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 0%

---

# Extensões do Adobe

Este tópico fornece informações sobre extensões PHP para Adobe Commerce e Magento Open Source lançadas pela Adobe.

As extensões adicionam recursos, funcionalidades, serviços e integrações ao Administrador e à loja. Algumas dessas extensões são desenvolvidas por meio das contribuições da Comunidade da Magento Open Source. Algumas extensões são instaladas por padrão e outras exigem instalação separada.

+++Saiba mais sobre a extensão do Adobe Commerce

O Adobe fornece duas abordagens principais para estender ou personalizar seus projetos do Adobe Commerce:

- Extensibilidade em processo: usa código personalizado e extensões executadas no processo do aplicativo Adobe Commerce, como extensões PHP. Essa abordagem tradicional permite uma integração profunda, mas requer um gerenciamento cuidadoso durante as atualizações.

- Extensibilidade fora do processo: usa código personalizado e aplicativos que operam independentemente do software principal. Essa abordagem moderna ajuda a reduzir o custo total de propriedade ao:

   - Simplificação de atualizações, pois as extensões são dissociadas do núcleo
   - Fornecendo aos desenvolvedores mais controle sobre o tempo e os métodos de implementação
   - Habilitação de dimensionamento e manutenção independentes de componentes de extensão

O Adobe Commerce oferece estratégias e ferramentas para dar suporte a ambos os tipos de extensibilidade. Para saber mais, consulte [extensibilidade do Adobe Commerce](https://developer.adobe.com/commerce/extensibility/).

+++

## Extensões do Adobe instaladas por padrão

As seguintes extensões do Adobe estão incluídas com o Adobe Commerce e instaladas automaticamente com o aplicativo do Adobe Commerce. Algumas extensões exigem mais configuração ou ativação no Administrador, conforme observado na descrição da extensão.

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

## Extensões do Adobe que exigem instalação

O Adobe oferece extensões adicionais que devem ser instaladas separadamente usando o Composer. Essas extensões estão disponíveis por meio de diferentes canais:

- Acesso ao repositório (repo.magento.com)

  As extensões a seguir exigem o provisionamento de conta e credenciais para a instalação. Entre em contato com o representante de conta da Adobe para obter assistência.

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [Integração do AEM Assets para o Commerce](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  As seguintes extensões do Adobe estão disponíveis publicamente em [marketplace.magento.com](https://marketplace.magento.com). Essas extensões estão disponíveis sem custo adicional.

   - [Live Search](#live-search)
   - [Recomendações de produto](#product-recommendations)
   - [Serviço de catálogo](#catalog-service)
   - [Payment Services](#payment-services)

### [!DNL Adobe Commerce B2B]

![Adobe Commerce](../assets/adobe-logo.svg) somente Adobe Commerce, requer uma licença separada.

O [!DNL Adobe Commerce B2B] é uma extensão integrada que transforma lojas Commerce padrão em plataformas business-to-business abrangentes. Ele permite que as empresas gerenciem estruturas organizacionais complexas com vários compradores, funções personalizadas e permissões de compra em contas unificadas da empresa. As principais funcionalidades incluem catálogos e preços específicos da empresa, cotações negociáveis, gerenciamento de ordens de compra, listas de requisições e recursos de pedidos rápidos. A solução oferece suporte a modelos B2B e B2C em uma única instância, tornando-a flexível para diversas necessidades de negócios. A extensão requer uma licença separada e integra-se perfeitamente aos principais recursos do Adobe Commerce para fornecer uma solução completa de comércio eletrônico B2B.

Para obter o provisionamento, entre em contato com o representante de conta da Adobe. Para obter detalhes sobre implementação e etapas de configuração, consulte o [[!DNL B2B for Adobe Commerce] Guia do Usuário](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=pt-BR).

### [!DNL AEM Assets Integration for Commerce]

![Adobe Commerce](../assets/adobe-logo.svg) somente Adobe Commerce, também requer licenças para Adobe Experience Manager (AEM) Assets e AEM Dynamic Media.

O [!DNL AEM Assets Integration for Commerce] conecta o Adobe Commerce com o sistema de Gerenciamento de ativos digitais (DAM) da Adobe Experience Manager para fornecer controle centralizado sobre todos os ativos digitais. Essa integração permite a sincronização automatizada de ativos, atualizações em tempo real e reutilização eficiente de conteúdo em várias lojas de comércio. Ao combinar os eficientes recursos de gerenciamento de ativos da AEM com o Commerce, as empresas se beneficiam de fluxos de trabalho simplificados, experiências consistentes com a marca e entrega de mídia otimizada por meio de infraestruturas baseadas em nuvem.

Para obter o provisionamento, entre em contato com o representante de conta da Adobe. Para obter detalhes sobre implementação e etapas de configuração, consulte o [[!DNL Assets Integration] Guia do Usuário](../content-design/aem-assets-integration.md).

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) somente Adobe Commerce

O Live Search é um recurso exclusivo da Adobe Commerce que fornece uma solução de pesquisa habilitada por IA com funcionalidade de &quot;pesquisa conforme você digita&quot; em tempo real. Ele fornece resultados rápidos e relevantes com miniaturas de produtos enquanto os compradores digitam, juntamente com facetas inteligentes que ajustam automaticamente os filtros com base no comportamento de compra. A solução inclui recursos de merchandising para impulsionar e enterrar produtos, gerenciamento de sinônimos e análise de pesquisa. Incluído no Adobe Commerce sem custo adicional, o [!DNL Live Search] substitui a funcionalidade de pesquisa padrão por uma experiência de pesquisa mais sofisticada, baseada em SaaS. Requer configuração mínima para começar.

Para obter detalhes sobre a implementação e requisitos técnicos, consulte o [Guia do Usuário do Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=pt-BR).

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) somente Adobe Commerce

O [!DNL Product Recommendations] é um recurso exclusivo da Adobe Commerce, desenvolvido pela tecnologia de IA da Adobe Sensei, que fornece sugestões personalizadas de produtos para toda a jornada de compras do cliente. A solução analisa o comportamento do comprador e os relacionamentos de produtos em tempo real para gerar automaticamente recomendações relevantes, não exigindo regras de merchandising manuais. Essa abordagem orientada por IA ajuda a aumentar as taxas de conversão e o potencial de receita, além de criar experiências de descoberta de produtos mais envolventes para os compradores.

Para obter detalhes sobre a implementação e as práticas recomendadas, consulte o [[!DNL Product Recommendations] Guia do Usuário](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html?lang=pt-BR).

### [!DNL Catalog Service]

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} instalações do Adobe Commerce e do Magento Open Source

O [!DNL Catalog Service] é uma solução de alto desempenho para o Adobe Commerce e o Magento Open Source que fornece acesso otimizado a dados de catálogo por meio de pontos de extremidade do GraphQL. Ele mantém um banco de dados sincronizado separado para obter detalhes do produto e informações relacionadas, ignorando a comunicação direta do aplicativo para fornecer tempos de carregamento de página mais rápidos. O serviço é particularmente valioso para páginas de detalhes de produtos, listas de categorias e páginas de resultados de pesquisa, tornando-o ideal para implementações de comércio tradicionais e headless.

Para obter instruções de instalação e detalhes técnicos, consulte o [[!DNL Catalog Service] Guia do Usuário](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html?lang=pt-BR).

>[!NOTE]
>
>Os Serviços de catálogo são instalados automaticamente quando o Live Search ou as Recomendações de produto são ativadas. A instalação manual não é necessária.

### [!DNL Payment Services]

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} instalações do Adobe Commerce e do Magento Open Source

O [!DNL Payment Services] é uma solução de pagamento pronta para uso para lojas Adobe Commerce e Magento Open Source que fornece recursos abrangentes de processamento de pagamento. O serviço integra a funcionalidade de gateway de pagamento seguro com proteção contra fraude integrada, ao mesmo tempo em que oferece várias opções de pagamento, incluindo cartões de crédito/débito, PayPal, Venmo (EUA) e planos PayLater. Ele apresenta relatórios de transação unificados e gerenciamento de pedidos por meio da interface do administrador do Commerce, facilitando aos comerciantes o rastreamento de pagamentos, o gerenciamento do fluxo de caixa e a reconciliação de dados financeiros, tudo em um único local.

Para obter etapas de configuração detalhadas e opções de pagamento, consulte o [[!DNL Payment Services] Guia do Usuário](https://experienceleague.adobe.com/pt-br/docs/commerce/payment-services/overview).
