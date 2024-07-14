---
title: Redes sociais e RSS feeds
description: Saiba como adicionar mídias sociais e outras integrações de RSS feed para criar uma percepção de marca e produto.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# Redes sociais e RSS feeds

Muitos comerciantes usam mídias sociais e outras ferramentas digitais para criar uma percepção da marca e do produto. É possível integrar sua loja às redes sociais instalando uma extensão do Marketplace ou adicionando um plug-in às páginas de conteúdo. Use RSS feeds para publicar informações de produto em sites de agregação de compras e até mesmo incluí-los em informativos. Os clientes podem assinar seus RSS feeds para saber mais sobre novos produtos e promoções.

## Redes sociais

Seu armazenamento pode ser conectado a redes sociais instalando uma [extensão do Marketplace](../getting-started/commerce-marketplace.md). Além disso, é possível adicionar facilmente plug-ins sociais, como o botão _Curtir_, a blocos CMS que podem ser incorporados a páginas em toda a loja.

Os sites de rede social têm vários plug-ins que podem ser facilmente adicionados à sua loja. Além disso, há muitas extensões no Commerce Marketplace que podem ser usadas para integrar sua loja às redes sociais. O exemplo a seguir mostra como adicionar um botão _Curtir_ do Facebook à sua loja.

>[!NOTE]
>
>O Adobe Commerce removeu a integração nativa do Facebook _Magento Social_ e não oferece mais suporte à extensão. Vá para o [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} para localizar extensões alternativas para integração com o Facebook.

### Etapa 1. Obter o código do botão

1. No site de desenvolvedores Meta, vá para a página [configuração de botão](https://developers.facebook.com/docs/plugins/like-button).

1. Para **[!UICONTROL URL to Like]**, insira a URL da página do armazenamento da qual você deseja que as pessoas _Goste_.

   Por exemplo, você pode inserir o URL da home page da sua loja.

1. Escolha o **[!UICONTROL Layout]** para o botão.

1. Digite a **[!UICONTROL Width]** em pixels que está disponível em seu site para o botão e qualquer mensagem de texto associada.

1. Defina **[!UICONTROL Action Type]** como um dos seguintes:

   - `Like`
   - `Recommend`

1. Clique em **[!UICONTROL Get Code]** para copiar o código gerado para a área de transferência.

### Etapa 2. Criar um bloco de conteúdo

1. Retorne ao Administrador da loja.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. No canto superior direito, clique em **[!UICONTROL Add New Block]**.

1. Insira um **[!UICONTROL Block Title]** descritivo para referência interna.

   Por exemplo: `Facebook Like Button`.

1. Atribua um **[!UICONTROL Identifier]** exclusivo ao bloco, usando todos os caracteres minúsculos e sublinhados, em vez de espaços.

   Por exemplo: `facebook_like_button`.

1. Se a instância do Commerce tiver várias exibições de armazenamento, escolha cada **[!UICONTROL Store View]** em que o bloco deverá estar disponível.

1. Adicione o trecho de código ao conteúdo do bloco, dependendo da ferramenta de conteúdo:

   - Ao usar o [!DNL Page Builder], adicione um bloco [HTML Code](../page-builder/html-code.md) ao estágio e cole o trecho de código que você copiou do site do Facebook. Caso contrário, cole o trecho de código na caixa **[!UICONTROL Content]**.

   - Com o editor, cole o trecho de código que você copiou do site do Facebook na caixa **[!UICONTROL Content]**.

1. Se o bloco não estiver pronto para entrar no ar, defina **[!UICONTROL Enable Block]** como `No`.

1. Quando terminar, clique em **[!UICONTROL Save Block]**.

### Etapa 3. Colocar o bloco

1. Adicione o bloco, dependendo da ferramenta de conteúdo:

   - Ao usar o [!UICONTROL Page Builder], siga as instruções para [adicionar o bloco](../page-builder/block.md) ao estágio.

   - Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. No canto superior direito, clique em **[!UICONTROL Add Widget]** e faça o seguinte:

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Disponível somente com Adobe Commerce B2B) Na seção _Configurações_, defina **[!UICONTROL Type]** como `CMS Static Block` e clique em **[!UICONTROL Continue]**.

   - Verifique se **[!UICONTROL Design Theme]** está definido como o tema atual.

   - Clique em **[!UICONTROL Continue]**.

1. Na seção **[!UICONTROL Storefront Properties]**, faça o seguinte:

   - Para **[!UICONTROL Widget Title]**, insira um título para referência interna.

   - Defina **[!UICONTROL Assign to Store Views]** como `All Store Views`, ou para o modo de exibição em que você deseja que o aplicativo esteja disponível. Para selecionar várias exibições, mantenha pressionada a tecla Ctrl (PC) ou a tecla Command (Mac) e clique em cada opção.

   - Insira um número no campo **[!UICONTROL Sort Order]** para determinar a ordem do bloco se ele foi designado para aparecer no mesmo local da página que outros elementos de conteúdo. A posição superior é zero.

1. Na seção _[!UICONTROL Layout Updates]_, clique em **[!UICONTROL Add Layout Update]**e defina **[!UICONTROL Display On]**como a categoria, o produto ou a página em que deseja que o bloco apareça.

   Por exemplo, se você escolher `All Pages` e posicionar o bloco no cabeçalho ou no rodapé, o bloco aparecerá no mesmo lugar em todas as páginas da loja.

   Para colocar o bloco em uma página específica, faça o seguinte:

   - Defina **[!UICONTROL Display On]** como `Specified Page` e selecione o **[!UICONTROL Page]** onde deseja que o bloco apareça.

   - Escolha o **[!UICONTROL Block Reference]** para identificar o local na página onde o bloco será colocado.

   - Aceite a configuração padrão para **[!UICONTROL Template]**, que é definida como `CMS Static Block Default Template`.

   - Clique em **[!UICONTROL Save and Continue Edit]**.

1. No painel à esquerda, escolha **[!UICONTROL Widget Options]**.

1. Clique em **[!UICONTROL Select Block…]** e escolha o bloco que deseja posicionar.

1. Quando terminar, clique em **[!UICONTROL Save]**.

1. Quando solicitado, siga as instruções na parte superior do espaço de trabalho para atualizar o índice e o cache da página.

   O widget agora aparece na lista _[!UICONTROL Widgets]_.

### Etapa 4. Verificar o local no armazenamento

Volte para a loja para verificar se o bloco está no local correto. Para mover o bloco, você pode reabrir o widget e tentar uma página ou referência de bloco diferente.

## RSS feeds

RSS (Really Simple Syndication) é um formato de dados baseado em XML usado para distribuir informações online. Seus clientes podem assinar seus RSS feeds para saber mais sobre novos produtos e promoções. Os RSS feeds também podem ser usados para publicar informações de produto em sites de agregação de compras e podem ser incluídos em boletins informativos.

Quando os RSS feeds estão habilitados, quaisquer adições a produtos, especiais, categorias e cupons são automaticamente enviadas aos assinantes de cada feed. Um link para todos os RSS feeds publicados está no rodapé da loja.

![Ícone de RSS feed](./assets/icon-rss.png){width="100"}<br/>

O software necessário para ler um feed RSS é chamado de leitor de feed, e permite que as pessoas assinem manchetes, blogs, podcasts e muito mais. O Google Reader é um dos muitos leitores de feeds que estão disponíveis online gratuitamente.

![Exemplo de vitrine - RSS feed](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### Benefícios da configuração de um feed RSS

- Baixe a atualização mais recente da sua loja ou blog
- Anúncios leves
- Ações ordinárias
- Aumentar o SEO
- Aumentar vendas

### Tipos de RSS feeds

| RSS Feed | Descrição |
|--- |--- |
| [!UICONTROL Wish List] | Quando ativado, um link de feed RSS é exibido na parte superior das páginas da lista de desejos do cliente. Além disso, a página de compartilhamento da lista de desejos inclui uma caixa de seleção que permite incluir um link para o feed de listas de desejos compartilhadas. |
| [!UICONTROL New Products] | Publica a notificação de novos produtos adicionados ao catálogo. |
| [!UICONTROL Special Products] | Publica a notificação de quaisquer produtos com preços especiais. |
| [!UICONTROL Coupons / Discounts] | Publica a notificação de todos os cupons ou descontos especiais disponíveis na loja. |
| [!UICONTROL Top Level Category] | Publica uma notificação de qualquer alteração na estrutura de categoria de nível superior do catálogo, que é refletida no menu principal. |
| [!UICONTROL Customer Order Status] | Oferece aos clientes a capacidade de rastrear o status do pedido pelo feed RSS. Quando ativado, um link de feed RSS é exibido no pedido. |

{style="table-layout:auto"}

### Configurar RSS feeds para sua loja

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No canto superior direito, defina **[!UICONTROL Store View]** para as exibições em que os feeds deverão estar disponíveis.

   Se for solicitada sua confirmação, clique em **[!UICONTROL OK]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL RSS Feeds]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Rss Config]** e defina **[!UICONTROL Enable RSS]** como `Enable`.

   ![Configuração do catálogo - RSS feeds](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Se necessário, desmarque a caixa de seleção **[!UICONTROL Use Default]** para alterar o valor padrão.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Wish List]** e defina **[!UICONTROL Enable RSS]** como `Enable`.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Catalog]** e defina outros feeds como `Enable`, conforme necessário.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Catálogo - Configurações de RSS feeds](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Order]** e defina **[!UICONTROL Customer Order Status Notification]** como `Enable`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Veja o resultado na loja com `/rss` no final da URL da página.

