---
title: Estrutura de armazenamento e site
description: Saiba mais sobre a hierarquia de exibição de site, loja e loja.
exl-id: d745cbd0-151b-4f82-bb6c-fb6b9565a014
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Estrutura de armazenamento e site

Quando o Adobe Commerce ou o Magento Open Source é instalado, uma hierarquia que inclui um site principal, uma loja e uma visualização de loja é criada. Você pode criar sites adicionais, lojas e visualizações de loja, conforme necessário. Por exemplo, além do site principal, você pode ter sites adicionais com um domínio diferente. Em cada site, você pode ter várias lojas e, em cada loja, visualizações de loja separadas. Muitas instalações têm um site e uma loja, mas com várias visualizações de loja para suportar diferentes idiomas.

Antes de começar, planeje com antecedência a hierarquia do catálogo de lojas, pois ela é mencionada em toda a configuração. Cada loja pode ter uma [categoria raiz](../catalog/category-root.md) separada, o que torna possível ter um conjunto totalmente diferente de opções de menu principal para cada loja.

![Diagrama de escopo](./assets/scope-multisite.svg){width="550"}

## Adicionar lojas

Uma única instalação do Adobe Commerce ou Magento Open Source pode ter várias lojas que compartilham um Administrador. As lojas que estão no mesmo site têm o mesmo endereço IP e domínio, usam o mesmo certificado de segurança e compartilham um único processo de finalização.

O importante a entender é que as lojas usam o mesmo código e compartilham um Administrador. Cada loja pode ter um catálogo separado ou as lojas podem compartilhar um catálogo. Cada loja pode ter uma [categoria raiz](../catalog/category-root.md) separada, o que permite ter um menu principal diferente para cada loja. As lojas também podem ter diferentes marcas, apresentações e conteúdo. Reserve algum tempo para planejar a hierarquia da loja tendo em mente o crescimento futuro antes de começar, pois ela é usada em toda a configuração.

![Escopo - vários armazenamentos](./assets/scope-multistore.svg){width="550"}

Estes são alguns exemplos de como URLs podem ser configurados para várias lojas:

| URL | Descrição |
| --- | ----------- |
| `yourdomain.com/store1`<br>`yourdomain.com/store2` | Cada loja tem um caminho diferente, mas compartilha um domínio. |
| `store1.yourdomain.com`<br>`store2.yourdomain.com` | Cada armazenamento tem um subdomínio diferente do domínio primário. |

As instalações de várias lojas do Adobe Commerce devem ser configuradas no Admin e também na linha de comando do servidor. O [Guia de Configuração](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) do Adobe Commerce fornece instruções detalhadas para configurar o ambiente do servidor.

### Etapa 1: Escolher o domínio de armazenamento

O primeiro passo é escolher como você deseja posicionar a loja. Os armazenamentos devem compartilhar um domínio, cada um com um subdomínio ou ter domínios claramente diferentes? Para cada armazenamento, siga um destes procedimentos:

- Para colocar o armazenamento um nível abaixo do domínio primário, não é necessário fazer nada.
- Configure um subdomínio do seu domínio primário.
- Configure um domínio primário diferente.

### Etapa 2: criar o armazenamento

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Clique em **[!UICONTROL Create Store]** e defina as opções para o novo armazenamento:

   - **[!UICONTROL Web Site]** — Escolha um site que seja o pai do novo armazenamento. Se a instalação tiver apenas um site, aceite o padrão (`Main Website`).

   - **[!UICONTROL Name]** — Digite um nome para o novo armazenamento. O nome é somente para referência interna.

   - **[!UICONTROL Code]** — Digite um código em caracteres minúsculos para identificar o armazenamento. Por exemplo: `mainstore`.

   - **[!UICONTROL Root Category]** — Defina para a [categoria raiz](../catalog/category-root.md) que define a estrutura da categoria para o menu principal do novo armazenamento. Selecione uma categoria raiz específica para o armazenamento, caso já tenha sido criada. Caso contrário, selecione `Default Category`. Você pode voltar mais tarde e atualizar a configuração.

   ![Criar armazenamento - opções de armazenamento](./assets/stores-all-store-information.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Save Store]**.

### Etapa 3: criar uma visualização de loja padrão

1. Clique em **[!UICONTROL Create Store View]** e defina as opções de exibição da loja:

   - **[!UICONTROL Store]** — Defina para o novo armazenamento criado.

   - **[!UICONTROL Name]** — Digite um nome para a exibição. Por exemplo, `English`.

   - **[!UICONTROL Code]** — Digite um código para a exibição em caracteres minúsculos.

   - **[!UICONTROL Status]** — Definido como `Enabled`.

   - **[!UICONTROL Sort Order]** — Digite um número para determinar a posição do armazenamento quando listado com outros armazenamentos.

1. Clique em **[!UICONTROL Save Store View]**.

   Se você abrir sua loja no modo de edição, poderá ver que agora ela tem uma visualização padrão.

   ![Novo armazenamento com exibição padrão](./assets/new-store-default-view.png){width="600" zoomable="yes"}

### Etapa 4: configurar o URL de armazenamento

1. Na barra lateral _Admin_, clique em **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Em _[!UICONTROL General]_, no painel esquerdo à esquerda, escolha **[!UICONTROL Web]**.

1. No canto superior esquerdo, defina **[!UICONTROL Store View]** para a exibição criada para o novo armazenamento.

1. Quando solicitado a confirmar a alternância do [escopo](../getting-started/websites-stores-views.md#scope-settings), clique em **[!UICONTROL OK]**.

   ![Escolher a exibição da loja](./assets/create-store-config-view.png){width="600" zoomable="yes"}

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Base URLs]** e insira a URL de base do armazenamento.

   Se necessário, desmarque a caixa de seleção **[!UICONTROL Use system value]** para alterar a configuração.

   ![Configuração geral - URLs de base Web](./assets/config-general-web-base-urls-clear-checkbox.png){width="600" zoomable="yes"}

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Secure Base URLs]** e repita a etapa anterior se desejar configurar a [URL segura](store-urls.md) do armazenamento.

1. Clique em **[!UICONTROL Save Config]**.

### Etapa 5: configurar o servidor

Para configurar o servidor para suportar vários sites, consulte [Vários sites ou lojas](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) no _Guia de Configuração_.

Para obter ajuda sobre como configurar o servidor Web, consulte os seguintes recursos:

- [Configurar vários sites com NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Configurar vários sites com o Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

Para o Adobe Commerce na infraestrutura em nuvem, consulte [Configurar vários sites ou lojas](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).

## Adicionar sites

Vários sites podem ser configurados a partir de uma única instalação do Adobe Commerce ou Magento Open Source com o mesmo domínio ou domínios diferentes. Por padrão, as lojas que estão no mesmo site têm o mesmo endereço IP e domínio, usam o mesmo certificado de segurança e compartilham um único processo de finalização. Se você quiser que cada loja tenha um processo de finalização dedicado em seu próprio domínio, cada loja deve ter um endereço IP distinto e um certificado de segurança separado.

As instalações em vários sites do Adobe Commerce ou Magento Open Source devem ser configuradas no Admin e também na linha de comando do servidor. O [Guia de Configuração](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) do Commerce fornece instruções detalhadas para configurar o ambiente do servidor.

![Escopo - sites](./assets/scope-multisite.svg){width="550"}

### Etapa 1: criar um site

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. No canto superior direito, clique em **[!UICONTROL Create Website]**.

1. Defina as opções de **[!UICONTROL Web Site Information]**:

   ![Criar site - opções](./assets/create-website-info.png){width="600" zoomable="yes"}

   - **[!UICONTROL Name]** — Insira o domínio do novo site. Por exemplo, `domain.com`.

   - **[!UICONTROL Code]** — Digite um código que seja usado no servidor para apontar para o domínio.

     O código deve começar com uma letra minúscula (a-z) e pode incluir qualquer combinação de letras (a-z), números (0-9) e o símbolo de sublinhado (_).

   - **[!UICONTROL Sort Order]** — _(Opcional)_ Insira um número para determinar a sequência na qual este site está listado com outros sites. Para que este site apareça na parte superior da lista, digite um zero (`0`).

1. Clique em **[!UICONTROL Save Web Site]**.

1. Configure cada [exibição de armazenamento](#add-stores) e [exibição de armazenamento](store-views.md) necessária para o novo site.

   Em seguida, é possível abrir o site no modo de edição para definir a loja padrão.

### Etapa 2: configurar o URL de armazenamento

Para configurar as [URLs de armazenamento](store-urls.md), siga as instruções.

### Etapa 3: configurar o servidor

Para configurar o servidor para suportar vários sites, consulte [Vários sites ou lojas](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) no _Guia de Configuração_.

Para obter ajuda com a configuração do servidor Web, consulte os seguintes tutoriais:

- [Configurar vários sites com NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Configurar vários sites com o Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

Para o Adobe Commerce na infraestrutura em nuvem, consulte [Configurar vários sites ou lojas](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).
