---
title: Escopo da configuração
description: Saiba mais sobre como definir o escopo das configurações no Administrador do Commerce.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---

# Escopo da configuração

O seletor de Exibição de loja no canto superior esquerdo de muitas páginas de configuração filtra a exibição da página de um escopo específico e define o valor de algumas entidades usadas pelo Commerce. Ela lista cada nível na hierarquia por nome e é usada para alterar o escopo para outro nível. Todas as configurações que representam o escopo atual ficam esmaecidas, de modo que apenas aquelas que representam a configuração do escopo atual ficam disponíveis. O escopo está inicialmente definido como _Configuração Padrão_. Para usuários Administradores com acesso restrito, a lista de exibições de loja disponíveis inclui apenas aquelas às quais o usuário tem [permissão](../systems/permissions.md) para acessar.

| Nível | Descrição |
|--- |--- |
| [!UICONTROL Default Config] | A configuração padrão do sistema. |
| [!UICONTROL Main Website] | O nome do site na parte superior da hierarquia. |
| [!UICONTROL Main Website Store] | O nome da loja padrão associada ao site pai. |
| [!UICONTROL Default Store View] | O nome da exibição de loja padrão associada à loja pai. |
| [!UICONTROL Stores Configuration] | Vai para a grade Lojas, e é o mesmo que escolher [!UICONTROL Stores] > [!UICONTROL All Stores] na barra lateral do Administrador. |

{style="table-layout:auto"}

![Usar caixas de seleção de Valor do Sistema marcadas](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

A caixa de seleção _[!UICONTROL Use System Value]_à direita de muitas definições de configuração é usada para aplicar ou substituir o valor de campo padrão no escopo de configuração atual. O valor de campo padrão não pode ser alterado quando a caixa de seleção está marcada. Para alterar o valor, desmarque a caixa de seleção e insira o novo valor. Você será solicitado a confirmar sempre que alterar o valor do sistema.

O rótulo da caixa de seleção muda de acordo com o escopo atual e sempre se refere ao nível principal que está uma etapa acima na hierarquia do escopo. Como o nível pai é um contêiner para todos os itens abaixo desse nível, a configuração de escopo do nível pai é herdada, a menos que seja substituída.

## Opções de valor padrão

| Caixa de seleção | Descrição |
|--- |--- |
| [!UICONTROL Use system value] | Esta caixa de seleção aparece quando o escopo de configuração está definido como `Default Config`. |
| [!UICONTROL Use Default] | Esta caixa de seleção aparece quando o escopo de configuração é definido como Principal `Website` e se refere ao armazenamento padrão atribuído ao site. |
| [!UICONTROL Use Website] | Essa caixa de seleção aparece quando o escopo de configuração é definido para uma visualização de loja específica. Quando selecionada, ela usa a configuração do site pai associado à exibição da loja. Nesse caso, o nível da loja é ignorado porque se aplica à loja padrão associada ao site. |

{style="table-layout:auto"}

## Definir o escopo

Antes de fazer uma definição de configuração que se aplique somente a uma exibição específica de site, loja ou loja, faça o seguinte:

1. Na barra lateral _Admin_, siga um destes procedimentos:

   - Para a maioria das configurações, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Para [configurações relacionadas ao design](../content-design/configuration.md), vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. Em seguida, na grade, escolha a visualização de loja aplicável.

1. Navegue até a definição de configuração a ser alterada e faça o seguinte:

   - No canto superior esquerdo, defina **[!UICONTROL Store View]** como a exibição específica à qual a configuração se aplica. Quando solicitado a confirmar a alternância de escopo, clique em **[!UICONTROL OK]**.

     Uma caixa de seleção é exibida depois de cada campo e campos adicionais podem ficar disponíveis.

   - Desmarque a caixa de seleção **[!UICONTROL Use system value]** depois de qualquer campo que você deseja editar. Em seguida, atualize o valor da exibição.

   - Repita esse processo para cada campo que precisa ser atualizado na página.

   ![Definindo as opções de País da exibição de loja na França](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Referência rápida do escopo

| Escopo | Descrição |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Admin | Todos os sites, lojas e visualizações de loja na instalação são gerenciados pelo mesmo Administrador. |
| Configuração padrão | As configurações globais [padrão](../getting-started/websites-stores-views.md#scope-settings) são usadas por meio da hierarquia de armazenamento, a menos que sejam substituídas em um nível inferior. |
| Catálogo | O termo _catálogo_ se refere ao banco de dados de produtos como um todo e está disponível durante toda a instalação. |
| Preços do produto | Os preços do produto podem ser configurados para o aplicativo em nível global ou de site. |
| Configurações do produto | Os atributos usados como opções de [produto configurável](../catalog/product-create-configurable.md) devem ter um escopo global. |
| Clientes | As contas do cliente podem ser configuradas para o aplicativo em nível global ou de site. Cada site pode ter um conjunto separado de [contas de cliente](../customers/customer-account-scope.md) ou compartilhar contas de cliente com outros sites na instalação. |
| **[!UICONTROL Website]** |  |
| Domínio | [sites adicionais](../stores-purchase/introduction.md#store-structure) podem ser configurados como subdomínios do domínio primário ou ter endereços IP e domínios dedicados separados. |
| Clientes | As contas do cliente podem ser configuradas para o aplicativo em nível global ou de site. Cada site pode ter um conjunto separado de [contas de cliente](../customers/customer-account-scope.md) ou compartilhar contas de cliente com outros sites na instalação. |
| Moeda | Cada site pode ser atribuído a uma [moeda base](../stores-purchase/currency-configuration.md) diferente. A moeda base é usada para processar todas as transações, embora uma moeda de exibição diferente possa aparecer para o cliente, de acordo com o local da exibição da loja. |
| Produtos | Os produtos individuais são atribuídos à hierarquia no nível do site. A grade Produtos lista todos os produtos no catálogo e nos sites em que estão disponíveis. A configuração [Produto em Sites](../catalog/settings-basic-websites.md) identifica cada site em que o produto está disponível. |
| Preços do produto | [Os preços dos produtos](../catalog/catalog-price-scope.md) podem ser configurados para o aplicativo no nível global ou no nível do site. |
| Métodos de pagamento | [Os métodos de pagamento](../stores-purchase/payments.md) estão configurados no nível do site, embora o título e as instruções possam ser configurados para cada exibição de loja. |
| Check-out | O [processo de check-out](../stores-purchase/checkout-process.md) ocorre no nível do site, embora algumas opções de exibição possam ser configuradas para cada exibição de loja. Todos os armazenamentos associados a um site têm a mesma [configuração de check-out](../stores-purchase/checkout-process.md#checkout-options). |
| Países permitidos | Os países permitidos podem ser configurados no nível do site. As configurações de [países permitidos](../getting-started/store-details.md#country-options) são usadas no check-out para limitar de onde um cliente pode vir. |
| **[!UICONTROL Store]** |  |
| Domínio | Com várias lojas, cada loja pode ter o mesmo domínio, um subdomínio ou domínios distintamente diferentes. Para obter mais informações, consulte [Adicionando lojas](../stores-purchase/stores.md#add-stores). |
| Categoria raiz | Cada loja pode ter um conjunto separado de produtos e menu principal com base em uma categoria &quot;raiz&quot; e subcategorias. Cada catálogo tem uma [categoria raiz](../catalog/category-root.md) atribuída no nível de armazenamento. |
| **[!UICONTROL Store View]** |  |
| Subcategorias | As [subcategorias](../catalog/category-create.md#category-structure) que compõem o menu principal (na raiz) são atribuídas no nível de exibição de loja. |
| Localidade | Cada exibição de armazenamento pode ser atribuída a uma [localidade](../getting-started/store-details.md#locale-options) diferente. A moeda de exibição, as unidades de medida e a interface do administrador são específicas ao local. |
| Idiomas | Para oferecer suporte a vários idiomas, todo o conteúdo, incluindo descrições de produtos, deve ser [traduzido](../stores-purchase/store-localize.md#localize-products) para cada exibição de loja. |
| Exibir moeda | Uma [moeda de exibição](../stores-purchase/currency-configuration.md) diferente pode ser usada para cada exibição de loja, embora as transações sejam processadas no nível do site usando a moeda base. |

{style="table-layout:auto"}
