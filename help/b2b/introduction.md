---
title: Introdução a  [!DNL Adobe Commerce B2B]
description: Saiba como usar recursos B2B integrados para atender às necessidades de clientes empresariais.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 2%

---

# Introdução ao [!DNL Adobe Commerce B2B]

Diferentemente do modelo padrão B2B (Business to Business), os recursos integrados B2B são projetados para atender às necessidades de vendedores (comerciantes da Adobe Commerce) que têm clientes que são empresas. Ele acomoda empresas com estruturas organizacionais complexas e vários usuários com várias funções e níveis de permissão de compra. Um cliente B2B típico pode ser o gerente de uma loja de varejo ou um comprador que faz compras em nome de uma empresa. Em ambos os casos, a transação ocorre entre a sua empresa e a deles. Você também pode vender produtos diretamente para o consumidor. [!DNL Adobe Commerce B2B] é uma solução integrada que oferece suporte aos modelos B2B e B2C.

Com a [instalação](install.md) e a [habilitação](enable-basic-features.md) da extensão B2B na sua loja da Adobe Commerce, a experiência de compra pode ser personalizada com catálogos e preços específicos do cliente, além de conteúdo e promoções direcionadas.

## Contas da empresa

O componente da conta da empresa é uma entidade-chave dentro do B2B da qual todos os outros recursos são de alguma forma dependentes. Ele permite unir vários compradores que pertencem a uma única empresa em uma única conta de empresa (ou conta corporativa). O administrador da empresa pode criar uma estrutura da empresa (divisões, subdivisões e usuários) que reflita o modelo operacional da empresa e forneça diferentes funções e permissões de usuário para os membros da empresa. Essa estrutura permite que o administrador da empresa controle a atividade do usuário para a conta da empresa: solicitação, cotação, compra, acesso a informações de crédito da empresa ou perfil e assim por diante.

No Administrador, o administrador do site do Commerce pode configurar como a empresa opera no site. A configuração determina os recursos B2B disponíveis para usuários da empresa, incluindo métodos de pagamento, níveis de precificação, a capacidade de negociar preços usando cotas, a capacidade de criar listas de requisição e muito mais.

Para obter mais informações, consulte [Contas da empresa](account-companies.md).

>[!NOTE]
>
>Quando habilitada, sua loja pode dar às empresas a opção de _Pagar na Conta_, o que significa fazer compras em uma linha de crédito da empresa. Como comerciante, você pode alocar crédito para uma conta da empresa e gerenciar configurações de crédito para uma empresa, além de reembolso de crédito.

## Gerenciamento da empresa

O gerenciamento da empresa ajuda os administradores comerciais a simplificar a administração e o gerenciamento de organizações B2B com modelos operacionais complexos.

Com o Administrador, os usuários com as permissões apropriadas podem criar um **[!UICONTROL Company Hierarchy]** que reflita a estrutura organizacional de uma empresa comercial composta por várias empresas. Essa hierarquia permite exibir e gerenciar empresas como um grupo. Por exemplo, o administrador pode designar uma empresa-mãe e atribuir todas as empresas que operam como subsidiárias da empresa-mãe. Em seguida, o administrador da empresa principal pode exibir e gerenciar as contas da empresa para todas as empresas atribuídas.

Para obter mais informações, consulte [Gerenciamento da Empresa](manage-companies.md).

## Serviços para o Adobe Commerce

Os serviços da Adobe Commerce são serviços hospedados que fornecem recursos estendidos para a Adobe Commerce e a Magento Open Source. Os serviços que oferecem suporte a fluxos de trabalho B2B são:

* [Serviço de catálogo](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html)
* [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html)
* [Recomendações de produto](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html)

## Catálogos compartilhados

Catálogos compartilhados são os níveis de preços que permitem definir preços personalizados por produto para diferentes empresas em um ou vários sites. Ao usar catálogos compartilhados, você pode vender produtos aplicando diferentes níveis de preço para diferentes grupos de clientes. O suporte para catálogos compartilhados está disponível somente para lojas Commerce configuradas para dar suporte a contas da empresa.

Para obter mais informações, consulte [Trabalhando com Catálogos Compartilhados](catalog-shared.md).

## Pedido rápido

Configure o Pedido rápido para reduzir o processo de pedido a vários cliques para clientes conectados quando eles souberem o nome do produto ou SKU dos produtos que desejam solicitar.

Para obter mais informações, consulte [Pedidos rápidos](quick-order.md).

## Cotações Negociáveis

Use o recurso Cotações para iniciar a negociação de preços entre um comprador e um vendedor da empresa.

* Um comprador autorizado pode iniciar uma cotação do carrinho de compras.

* Um vendedor pode iniciar um orçamento para um comprador com o Administrador.

Compradores e vendedores usam a cota para gerenciar o processo de negociação - como adicionar itens, atualizar quantidades, solicitar e aplicar descontos - até que cheguem a um acordo. A grade _Cotas_ no Administrador lista cada cotação recebida e mantém um histórico da comunicação entre comprador e vendedor.

O suporte para Cotações Negociáveis está disponível apenas para lojas Commerce configuradas para suportar contas da Empresa.

Para obter mais informações, consulte [Cotações negociáveis](quotes.md).

## Aprovações de ordem de compra

Quando Ordens de Compra são ativadas para uma conta de empresa, todas as ordens são criadas automaticamente como Ordens de Compra (OC). Os usuários da empresa com as permissões necessárias podem criar, editar e excluir OCs que eles criam e OCs criadas por usuários subordinados. Dependendo de sua função e da ordem, os usuários da empresa podem estar sujeitos a várias regras de aprovação.

Para obter mais informações, consulte [Pedidos de Compra para Empresas](purchase-order-flow.md).

## Listas de requisições

Os clientes podem usar a lista de requisições para economizar tempo ao comprar produtos encomendados com frequência, pois podem adicionar itens ao carrinho diretamente na lista. Eles podem manter várias listas que se concentram em produtos de diferentes fornecedores, compradores, equipes, campanhas ou qualquer outra coisa que simplifique o fluxo de trabalho.

Para obter mais informações, consulte [Listas de Requisições](requisition-lists.md).
