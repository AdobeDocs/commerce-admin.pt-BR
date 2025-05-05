---
title: Site, loja e escopo de exibição
description: Saiba mais sobre a hierarquia de sites, lojas e visualizações de loja que você pode usar para fornecer experiências de compra para seus clientes.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Site, loja e escopo de exibição

Cada instalação do Adobe Commerce e do Magento Open Source tem uma [hierarquia](../stores-purchase/stores.md) de sites, lojas e visualizações de loja. O termo _escopo_ determina onde na hierarquia se aplica uma entidade de banco de dados (como um produto, atributo ou categoria), elemento de conteúdo ou definição de configuração. Sites, lojas e visualizações de loja têm relacionamentos pai/filho de um para muitos. Uma única instalação pode ter vários sites, e cada site pode ter várias lojas e visualizações de loja.

>[!NOTE]
>
>Para saber mais, consulte [Vários sites ou lojas](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=pt-BR) na documentação para desenvolvedores do [!DNL Commerce].

## Sites

As instalações começam com um único [site](../stores-purchase/stores.md#add-websites), que é chamado de _Site Principal_ por padrão. Você também pode configurar vários sites para uma única instalação, cada um com seu próprio endereço IP e domínio.

## Lojas

Um único site pode ter várias [lojas](../stores-purchase/stores.md#add-stores), cada uma com seu próprio menu principal. As lojas compartilham o catálogo de produtos, mas podem ter uma seleção diferente de produtos e design. Todas as lojas no mesmo site compartilham o Administrador e o check-out.

## Visualizações da loja

Cada loja disponível para os clientes é apresentada de acordo com uma _[visualização](../stores-purchase/store-views.md)_ específica. Inicialmente, uma loja tem uma única visualização padrão. Visualizações de loja adicionais podem ser adicionadas para oferecer suporte a diferentes idiomas ou para outros fins. Os clientes podem usar o seletor de idioma no cabeçalho para alterar a exibição da loja.

Ao trabalhar com sites, lojas e visualizações de loja, lembre-se do seguinte:

- As instâncias do Commerce têm um modelo em cascata: global → site → loja → visualização da loja.
- Cada site tem no mínimo uma visualização de loja e loja padrão.
- Cada exibição de loja pode ter um URL de base diferente.
- A função principal de um site é a configuração de recursos de nível superior.
- A função principal de um armazenamento é a configuração de categoria raiz.
- A função principal de uma visualização de loja é a configuração das informações de tradução e do símbolo de moeda.

## Configurações de escopo

Se a sua instalação do Adobe Commerce ou Magento Open Source tiver uma hierarquia de sites, lojas ou modos de exibição, você poderá definir o contexto ou o _escopo_ de uma definição de configuração. O contexto de muitas entidades de banco de dados também pode receber um escopo específico para determinar como ele é usado na hierarquia de armazenamento. Para saber mais, consulte [Escopo do produto](../catalog/introduction.md#product-scope) e [Escopo do preço](../catalog/catalog-price-scope.md).

Algumas definições de configuração, como código postal, têm um escopo global porque o mesmo valor é usado em todo o sistema. O escopo do [site](../stores-purchase/stores.md#add-websites) se aplica a todos os armazenamentos abaixo desse nível na hierarquia, incluindo todos os armazenamentos e suas exibições. Qualquer item com o escopo de [exibição de repositório](../stores-purchase/store-views.md) pode ser definido de forma diferente para cada exibição de repositório, que normalmente é usada para oferecer suporte a vários idiomas. Para substituir os valores padrão das definições de configuração, consulte [Definir o escopo](../configuration-reference/scope-change.md#set-the-scope).

A menos que o armazenamento esteja sendo executado no [modo de armazenamento único](#single-store-mode), o escopo de cada definição de configuração aparece em texto pequeno abaixo do rótulo do campo. Se a sua instalação incluir vários sites, lojas ou modos de exibição, escolha o [modo de exibição de loja](../stores-purchase/store-views.md) no qual as configurações se aplicam antes de fazer qualquer alteração.

![Hierarquia de sites, lojas e exibições de loja](./assets/scope-multisite.svg){width="550"}

| Escopo | Descrição |
|--- |--- |
| [!UICONTROL Global] | Configurações e recursos de todo o sistema que estão disponíveis durante toda a instalação. |
| [!UICONTROL Website] | Configurações e recursos limitados ao site atual. Cada site tem uma loja padrão. |
| [!UICONTROL Store] | Configurações e recursos limitados ao armazenamento atual. Cada loja tem uma categoria raiz padrão (menu principal) e uma visualização de loja padrão. |
| [!UICONTROL Store View] | Configuração e recursos limitados à exibição de loja atual. |

{style="table-layout:auto"}

## Modo de armazenamento único

Se a sua instalação do Commerce tiver apenas uma única visualização de loja e loja, você poderá simplificar a visualização desativando todas as opções de visualização de loja e indicadores de escopo. O modo de armazenamento único será substituído se você [adicionar mais exibições de armazenamento](../stores-purchase/store-views.md) posteriormente.

![Escopo - exibição única](./assets/scope-single-view.svg){width="550"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Em **[!UICONTROL General]**, role para baixo até a parte inferior da página e expanda a seção **[!UICONTROL Single-Store Mode]**.

1. Defina **[!UICONTROL Enable Single-Store Mode]** como `Yes`.

   ![Configuração geral - Habilitar Modo de Repositório Único](./assets/general-single-store-mode.png){width="400"}

1. Clique em **[!UICONTROL Save Config]**.

1. Quando solicitado a atualizar o cache, faça o seguinte:

   - Clique no link **[!UICONTROL Cache Management]** na mensagem do sistema na parte superior da página.

     ![Mensagem do sistema - gerenciamento de cache](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Marque a caixa de seleção **[!UICONTROL Page Cache]**.

   - Com **[!UICONTROL Actions]** definido como `Refresh`, clique em **[!UICONTROL Submit]**
