---
title: Mapas do site
description: Saiba como configurar um mapa do site para indexar todas as páginas e imagens dos sites do Commerce.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 0%

---

# Mapas do site

Um mapa de site melhora a maneira como sua loja é indexada por mecanismos de pesquisa e é projetado para encontrar páginas que podem ser ignoradas por rastreadores da Web. Um mapa do site pode ser configurado para indexar todas as páginas e imagens.

Quando ativado, o Commerce cria um arquivo chamado `sitemap.xml` que é salvo na sua instalação no local especificado. A configuração oferece a capacidade de definir a frequência das atualizações e a prioridade para cada tipo de conteúdo. O mapa do site deve ser atualizado com a mesma frequência que as alterações de conteúdo do site, que podem ser diárias, semanais ou mensais.

Enquanto o site estiver em desenvolvimento, você poderá incluir instruções no `robots.txt` arquivo para que os rastreadores da web evitem indexar o site. Antes do lançamento, é possível alterar as instruções para permitir que o site seja indexado.

Para obter informações técnicas, consulte [Adicionar mapa do site e robots.txt][1] no _Guia do Commerce na infraestrutura em nuvem_.

![Grade do mapa do site](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## Etapa 1. Configurar o mapa do site

Conclua o [Configuração do mapa do site XML](#site-map-configuration) para determinar o que está incluído e com que frequência o mapa do site é atualizado.

## Etapa 2. Gerar o mapa do site

1. No _Admin_ , acesse **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Clique em **[!UICONTROL Add Site Map]**.

   ![Grade do mapa do site](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. Insira o mapa do site **[!UICONTROL Filename]**. Por exemplo: `sitemap.xml`

1. Insira o **[!UICONTROL Path]** para determinar onde o arquivo de mapa do site deve residir no servidor. Verifique se o caminho é gravável.

   - `/sitemap/` - Coloca o arquivo do mapa do site em um diretório chamado _mapa do site_.

   - `/` - Coloca o arquivo do mapa do site no caminho base ou raiz da instalação do Commerce.

   ![Novo mapa do site](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save & Generate]**.

   Pode levar alguns minutos para que o mapa do site apareça na grade.

## Etapa 3. Configure e ative o robots.txt (opcional)

Conclua o [robôs de mecanismo de pesquisa](seo-overview.md#search-engine-robots) configuração com instruções que direcionam os mecanismos de pesquisa para rastrear as partes do site que você deseja indexar.

## Etapa 4. Enviar o mapa do site para mecanismos de pesquisa

É possível enviar o mapa do site para diferentes mecanismos de pesquisa fornecendo a eles o link para o `sitemap.xml` arquivo na instalação do Commerce. Para copiar o link, faça o seguinte:

1. No _Mapa do site_ clique com o botão direito do mouse no URL na variável **[!UICONTROL Link for Google]** coluna.

1. No menu, escolha **[!UICONTROL Copy Link Address]**.

Para obter mais informações, consulte as instruções do mecanismo de pesquisa específico. Aqui estão os links para instruções para dois dos principais mecanismos de pesquisa:

- [Google][2]
- [Microsoft® Bing][3]

## Etapa 5: Restaurar instruções anteriores do robô (opcional)

Agora é possível restaurar as restrições originais (padrão).

## Gerencie mapas de site e o robots.txt para vários sites

Se você tiver vários sites, poderá simplificar o processo de criação e envio de mapas de site. Simplesmente [criar](#site-map-configuration) um ou mais mapas de site que incluem URLs para todos os armazenamentos verificados e salvam os mapas de site em um único local. Todos os sites devem ser verificados em [Console de pesquisa do Google](https://support.google.com/webmasters/answer/7451001).

Para criar mapas de site para uma instância multiarmazenamento, faça o seguinte:

1. Crie uma pasta chamada `sitemaps` na raiz do site e, em seguida, crie subpastas para cada domínio:

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Crie ou edite as listagens de mapa de site para cada loja e defina o **[!UICONTROL Path]** para o que você criou para a loja:

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. Se necessário, atualize o arquivo robots.txt.

   Para garantir que as aranhas do mecanismo de pesquisa sejam direcionadas corretamente aos novos mapas de site, você pode atualizar ou criar o arquivo robots.txt. Adicione as seguintes linhas na parte superior.

       Mapa do site do site
       Mapa do site: https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       Mapa do site: https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>Se o site usar o [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html) mecanismo do servidor Web, você deve atualizar o [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) arquivo na raiz do site para direcionar qualquer outra solicitação de mapa de site para o local adequado.

## Descrições da coluna

| Coluna | Descrição |
|------|-----------|
| [!UICONTROL ID] | O número de registro sequencial do mapa do site atual. |
| [!UICONTROL Filename] | O nome do arquivo do mapa do site. |
| [!UICONTROL Path] | O local onde o mapa do site reside no servidor. Por exemplo: <br/>`/sitemap/` - Coloca o arquivo do mapa do site em um diretório chamado _mapa do site_, um nível abaixo da raiz da instalação do Commerce. <br/>`/` - Coloca o arquivo de mapa do site no caminho base ou raiz da instalação do Commerce. |
| [!UICONTROL Link for Google] | A URL do mapa do site que deve ser enviado para o Google e outros mecanismos de pesquisa. |
| [!UICONTROL Last Generated] | Indica a data e a hora em que o mapa do site foi gerado pela última vez. |
| [!UICONTROL Store View] | A exibição de loja onde o mapa do site se aplica. |
| [!UICONTROL Generate] | Regenera o mapa do site. |

{style="table-layout:auto"}

## Configuração do mapa do site

O mapa do site deve ser atualizado com a mesma frequência que as alterações de conteúdo do site, o que pode ocorrer diariamente, semanalmente ou mensalmente. A configuração permite definir a frequência e a prioridade para cada tipo de conteúdo.

### Etapa 1. Definir a frequência e a prioridade das atualizações de conteúdo

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL XML Sitemap]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Categories Options]** e faça o seguinte:

   >[!NOTE]
   >
   >Se necessário, limpe a caixa de seleção **[!UICONTROL Use system value]** para alterar essas configurações.

   - Definir **[!UICONTROL Frequency]** a um dos seguintes:

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - Para **[!UICONTROL Priority]**, insira um valor entre `0.0` e `1.0`. Zero tem a prioridade mais baixa.

   ![Mapa de site XML - Opções de categorias](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte [Opções de Categorias](../configuration-reference/catalog/xml-sitemap.md#categories-options) no _Referência de configuração_.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Products Options]** e preencha a seção **[!UICONTROL Frequency]** e **[!UICONTROL Priority]** conforme necessário.

   Para obter uma lista detalhada dessas opções, consulte [Opções de produtos](../configuration-reference/catalog/xml-sitemap.md#products-options) no _Referência de configuração_.

1. Para determinar a extensão da inclusão de imagens no mapa do site, defina **[!UICONTROL Add Images into Sitemap]** a um dos seguintes:

   - `None`
   - `Base Only`
   - `All`

   ![Configuração do catálogo - produtos de mapa de site XML](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL CMS Pages Options]** e preencha a seção **[!UICONTROL Frequency]** e **[!UICONTROL Priority]** conforme necessário.

   ![Configuração do catálogo - Páginas CMS do mapa de site XML](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte [Opções de páginas do CMS](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) no _Referência de configuração_.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Store Url Options]** e preencha a seção **[!UICONTROL Frequency]** e **[!UICONTROL Priority]** conforme necessário.

   ![Configuração do catálogo - URL de armazenamento do mapa de site XML](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte [Armazenar Opções De Url](../configuration-reference/catalog/xml-sitemap.md#store-url-options) no _Referência de configuração_.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Etapa 2. Concluir as configurações de geração

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Generation Settings]** seção.

   Se necessário, limpe a caixa de seleção **Usar valor do sistema** para alterar essas configurações.

   ![Configuração do catálogo - Configurações de geração de mapa de site XML](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte [Configurações de geração](../configuration-reference/catalog/xml-sitemap.md#generation-settings) no _Referência de configuração_.

1. Para gerar um mapa de site, defina **[!UICONTROL Enabled]** para `Yes` e faça o seguinte:

   - Definir **[!UICONTROL Start Time]** à hora, aos minutos e ao segundo em que você deseja que o mapa do site seja atualizado.

   - Definir **[!UICONTROL Frequency]** a um dos seguintes:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - Para **[!UICONTROL Error Email Recipient]**, insira o endereço de email da pessoa que receberá a notificação se ocorrer um erro durante uma atualização do mapa de site.

   - Definir **[!UICONTROL Error Email Sender]** ao contato da loja que aparece como o remetente da notificação de erro.

   - Definir **[!UICONTROL Error Email Template]** ao template usado para a notificação de erro.

### Etapa 3. Definir os limites de arquivo do mapa do site

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Sitemap File Limits]** seção.

   ![Configuração do catálogo - Limites de arquivo de mapa de site XML](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   Para obter uma lista detalhada dessas opções, consulte [Limites de arquivo do mapa do site](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) no _Referência de configuração_.

1. Para **[!UICONTROL Maximum No of URLs per File]**, insira o número máximo de URLs que podem ser incluídos no mapa do site.

   Por padrão, o limite é de 50.000.

1. Para **[!UICONTROL Maximum File Size]**, insira o maior tamanho em bytes alocado para o mapa de site.

   O tamanho padrão é 10.485.760 bytes.

### Etapa 4. Definir as configurações de envio do mecanismo de pesquisa

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Search Engine Submission Settings]** seção.

   ![Configuração do catálogo - Configurações de envio do mecanismo de pesquisa do mapa de site XML](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. Se estiver usando um `robots.txt` arquivo para fornecer instruções aos mecanismos de pesquisa que rastreiam seu site, defina **[!UICONTROL Enable Submission to Robots.txt]** para `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
