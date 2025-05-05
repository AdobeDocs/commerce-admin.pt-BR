---
title: Notas de versão para  [!DNL Page Builder]
description: Revise as notas de versão para obter informações sobre todas as  [!DNL Page Builder]  versões.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2813'
ht-degree: 0%

---

# Notas de versão para [!DNL Page Builder]

Essas notas de versão descrevem versões de [!DNL Page Builder] e incluem:

![Novos](../assets/new.svg) Novos recursos

![Correção de um problema](../assets/fix.svg) Correções e melhorias

![Problema conhecido](../assets/bug.svg) Problemas conhecidos

>[!IMPORTANT]
>
>A partir da versão 2.4.3, o [!DNL Page Builder] está disponível como uma extensão agrupada no Magento Open Source. Agora, ela é a ferramenta de edição de conteúdo padrão para Adobe Commerce e Magento Open Source e pode substituir o editor WYSIWG por qualquer módulo de terceiros.

## 1.7.2 para Commerce 2.4.5

![Novo](../assets/new.svg) **Nova entidade de wrapper - [!DNL Columns] contêiner introduzido para layouts de coluna** - Anteriormente, os usuários só podiam adicionar colunas dentro de outro tipo de conteúdo de container/wrapper, como um [!DNL Tab] ou [!DNL Row]. Agora, o [!DNL Column] tem seu próprio invólucro e pode ser adicionado diretamente no palco. Além disso, o contêiner [!DNL Columns] tem um elemento de configurações no qual os usuários podem especificar a configuração dessa entidade wrapper.<!--- PB-500-->

![Novo](../assets/new.svg) **Novas opções de menu para duplicar, ocultar e excluir grupos de Colunas** - Com essas novas opções, os usuários podem duplicar, ocultar e excluir grupos de [!DNL Columns] — da mesma forma que fazem com os tipos de conteúdo.<!--- PB-507-->

![Novo](../assets/new.svg) <!-- Issue 594 -->**Novo suporte a colunas com várias linhas adicionado ao Grupo de colunas** - Com essa adição, os usuários podem manipular várias linhas de colunas dentro de um grupo [!DNL Columns] para tornar os layouts de colunas muito mais flexíveis.<!--- PB-108-->

Consulte [Layout - Coluna](./column.md) para obter informações sobre como usar o novo grupo [!DNL Columns].

## 1.7.1 para Commerce 2.4.4

![Problema corrigido](../assets/fix.svg) O Page Builder agora é compatível com o PHP 8.1.<!--- AC-1300-->

![Problema corrigido](../assets/fix.svg) Os comerciantes agora podem adicionar texto alternativo (`alt_text`) às imagens (Imagem, Faixa, Slide) para melhorar a acessibilidade do conteúdo.<!--- PB-1193-->

![Correção de um problema](../assets/fix.svg) Os usuários administradores com permissões restritas apenas à edição de conteúdo não veem mais um erro ao usar o Page Builder para adicionar um widget de produto a uma página do CMS. O Page Builder também exibe uma contagem de produto precisa na página de configurações do widget. Anteriormente, o Page Builder exigia permissões para o módulo Catálogo ao recuperar a contagem de produtos e exibia este erro: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Problema corrigido](../assets/fix.svg) Problemas de exibição com o menu Formato do Page Builder agora são resolvidos com a atualização da biblioteca TinyMCE 5. <!--- AC-446-->

![Problema corrigido](../assets/fix.svg) Agora é possível usar o mouse para editar o valor **Texto para Exibição** no pop-up Inserir Link. <!--- AC-982-->

![Problema corrigido](../assets/fix.svg) O Page Builder agora exibe todas as opções conforme esperado no menu de opções Tamanho da Fonte. Anteriormente, nem todas as opções eram exibidas. <!--- AC-1056-->

![Correção de um problema](../assets/fix.svg) Atualizou a dependência do Composer `phpgt/dom` para a extensão `magento/magento2-page-builder` para as versões mais recentes. <!--- magento/magento2-page-builder/pull/779-->

![Problema corrigido](../assets/fix.svg) O Page Builder não redimensiona mais as caixas de diálogo Inserir link e Inserir imagem ao exibir o controle deslizante em uma pequena coluna. <!--- AC-973-->

![Problema corrigido](../assets/fix.svg) O menu Propriedades da tabela do Page Builder agora é exibido conforme esperado. <!--- AC-407-->

![Problema corrigido](../assets/fix.svg) Os pontos do controle deslizante não são mais exibidos no link Inserir ou na modal da imagem quando o mouse não está passando sobre o controle deslizante. <!--- AC-406-->

![Problema corrigido](../assets/fix.svg) O tamanho da fonte usado para exibir as opções do menu Tabela foi otimizado. <!--- AC-396-->

![Correção do problema](../assets/fix.svg) Correção de anomalias com o posicionamento das caixas de diálogo Inserir/Editar Imagem e Inserir/Editar Link. <!--- AC-397-->

![Problema corrigido](../assets/fix.svg) O Page Builder não lança mais um erro ao clicar em **Editor de texto** para um banner. <!--- AC-398-->

![Problema corrigido](../assets/fix.svg) O Page Builder não converte mais todos os blocos dinâmicos em um idioma durante a atualização. <!--- MC-42265-->

## 1.6.0 para Adobe Commerce 2.4.2

![Novo](../assets/new.svg) <!-- Issue 558 -->**Novo estilo [!DNL Page Builder]** - [!DNL Page Builder] fez grandes melhorias na forma como estiliza o conteúdo. As alterações agora facilitam a criação de seletores de CSS simples para substituir os estilos de tipo de conteúdo existentes. Essas alterações possibilitam a criação de [!DNL Page Builder] temas com grande capacidade de resposta para todos os tipos de conteúdo.

![Novo](../assets/new.svg) <!-- Issue 429 -->**Contêiner de linha agora opcional** - Agora você pode criar conteúdo em [!DNL Page Builder] sem exigir um contêiner de linha. Além da Linha, os seguintes tipos de conteúdo agora podem ser arrastados e soltos diretamente no palco: HTML, Bloco, Bloco dinâmico, Colunas e Guias.

![Novo](../assets/new.svg) <!-- Issue 636 -->**Novo alternador de visor responsivo** - Agora você pode visualizar seu conteúdo [!DNL Page Builder] em diferentes larguras de dispositivo (pontos de interrupção) usando os novos botões do alternador de visor Admin acima do estágio. O seletor de visor simula como o conteúdo é estilizado quando exibido na loja usando dispositivos diferentes.

![Novo](../assets/new.svg) <!-- Issue 637 -->**Novos campos de formulário específicos do ponto de interrupção** - Os valores de campo do tipo de conteúdo agora podem ser definidos como pontos de interrupção específicos do visor. Os indicadores de ícone ao lado dos campos mostram a janela de visualização à qual o valor do campo de tipo de conteúdo é aplicado.

![Novas](../assets/new.svg) <!-- Issue 559 -->**Entradas removidas de campo de formulário predefinidas** - Configurações avançadas de formulário para margens, preenchimentos e propriedades relacionadas à borda (borda, largura da borda e raio da borda) agora estão definidos como `default`, para que os valores possam ser definidos pelo CSS de um módulo.

![Novo](../assets/new.svg) <!-- Issue 635, 557,  -->**Espaçamento de estágio adicionado** - Agora as linhas e colunas fornecem permissões de espaçamento adicionais sobre tipos de conteúdo contidos no estágio, mas não na loja. O espaçamento de estágio extra facilita o acesso aos menus de opção mouse sobre para os tipos de conteúdo contêiner e contido.

![Correção de um problema](../assets/fix.svg) <!-- MC-37348 -->**Correção da rolagem automática para análises** - A rolagem automática para análises de produtos na loja agora está corrigida.

![Problema corrigido](../assets/fix.svg) <!-- MC-36227 -->**Conteúdo corrigido** - As descrições longas de categorias e produtos não são mais cortadas.

![Problema corrigido](../assets/fix.svg) <!-- MC-35402 -->**Conteúdo de categoria de sangria completa e largura total fixo** - O conteúdo da categoria agora pode ser exibido em um layout de largura completa ou sangria completa.

![Problema corrigido](../assets/fix.svg) <!-- MC-37989 -->**Aprimoramentos de segurança**

## 1.5.1 para Adobe Commerce 2.4.1-p1

![Problema corrigido](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Exibição de erros** - Corrigido um problema no qual [!DNL Page Builder] exibia um erro ao adicionar subcategorias do catálogo no Administrador.

## 1.5.0 para Adobe Commerce 2.4.1

![Novo](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Edição imersiva, em tela inteira** - A edição de conteúdo [!DNL Page Builder] agora é apenas em tela cheia para todas as áreas controladas por [!DNL Page Builder]. Essa alteração inclui páginas do CMS, páginas de Produto e Categoria, Blocos e Blocos dinâmicos. A edição em tela cheia coloca o foco no conteúdo e fornece uma visualização que melhor corresponde à experiência do usuário na loja.

![Novas](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] visualizações de conteúdo &#x200B;**- Por padrão, o [!DNL Page Builder] agora fornece visualizações de conteúdo não apenas para páginas CMS, Blocos e Blocos Dinâmicos, mas também para páginas de Produto e Categoria. É possível configurar esse recurso para ser ativado ou desativado para páginas de Produto e Categoria usando a nova configuração de Visualização de conteúdo do [!DNL Page Builder], acessada na configuração de armazenamento em Gerenciamento de conteúdo > Ferramentas de conteúdo avançadas.

![Novo](../assets/new.svg) <!-- Issue 543 -->**Acesso aprimorado às descrições resumidas do produto** - Por padrão, uma descrição curta do produto agora é exibida antes da descrição mais longa. Essa alteração resulta em uma correspondência com a ordem em que eles aparecem na loja e evita a necessidade de rolar pelo conteúdo de descrição mais longa para obter acesso à descrição curta.

![Novo](../assets/new.svg) <!-- Issue 419 -->**Impediu links aninhados em Banners e Slides** - Adicionando links ao conteúdo e aos elementos externos de Banners e Slides criou links aninhados que não eram exibidos ou se comportavam corretamente na loja. Para resolver o problema, não é mais possível adicionar links a *ambos* a área Texto da Mensagem e o atributo Link para Banners e Slides.

![Correção de um problema](../assets/fix.svg) <!-- Issue 421 --> Correção de um problema em que a definição de um raio de borda vazio em um Item de guia causava erros e quebrava o conteúdo do Item de guia.

![Correção de um problema](../assets/fix.svg) <!-- Issue 422 --> Correção de um problema em que a adição de determinadas combinações de condições ao filtro Condição de produtos causava erros que impediam o salvamento do formulário Produtos.

![Correção de um problema](../assets/fix.svg) <!-- Issue 425 -->Correção de um problema em que o tipo de conteúdo do Controle Deslizante não se comportava corretamente quando a configuração de Loop Infinito era desabilitada.

![Problema corrigido](../assets/fix.svg) <!-- Issue 426 -->Corrigido o preço mínimo anunciado para que funcionasse agora em [!DNL Page Builder].

![Correção de um problema](../assets/fix.svg) <!-- Issue 436 -->Corrigido o problema no Safari e no IE 11 que impedia arrastar e soltar uma Imagem na área de carregamento em Banners e Slides.

![Correção de um problema](../assets/fix.svg) <!-- Issue 525 -->Corrigido o problema no qual o tipo de conteúdo do Controle Deslizante não respondia no Firefox.

![Correção de um problema](../assets/fix.svg) <!-- Issue 567 -->Corrigido o problema no qual a configuração do widget criava seletores incorretos no DOM para as diferentes aparências.

![Correção de um problema](../assets/fix.svg) <!-- Issue 609 -->Corrigido o problema no qual a barra de ferramentas Cabeçalho ocultava o menu de opções do tipo de conteúdo, que impedia o acesso ao formulário e a outras opções.

![Correção de um problema](../assets/fix.svg) <!-- Issue 612, 613 -->Correção de problemas em que os controles deslizantes e várias linhas que usavam planos de fundo de paralaxe não eram renderizados corretamente após alternar o modo de tela cheia várias vezes.

![Correção de um problema](../assets/fix.svg) <!--MC-35220-->Corrigido o problema no qual a tentativa de copiar o conteúdo de um tipo de conteúdo de Cabeçalho para um tipo de conteúdo de Texto impedia [!DNL Page Builder] de salvar.

![Correção de um problema](../assets/fix.svg) <!-- MC-34620 -->Corrigido o tipo de conteúdo de texto para manipular e salvar corretamente caracteres não latinos-1.

![Correção de um problema](../assets/fix.svg) <!-- MC-34679 -->Correção de [!DNL Page Builder] estilos CSS que fazia com que o Safari 13.1 renderizasse incorretamente o menu de site do tema Luma para pequenas portas de exibição e telas móveis.

![Correção de um problema](../assets/fix.svg) <!-- MC-34848 -->Corrigido o tipo de conteúdo HTML para exibir corretamente widgets inseridos, como &quot;Pedir por SKU&quot; na Loja.

## 1.4.1 para Adobe Commerce 2.4.0-p1

![Novo](../assets/new.svg) <!-- PB-590 --> atualizado para TinyMCE 4. Remoção do TinyMCE 3 para melhorar a segurança.

## 1.4.0 para Adobe Commerce 2.4.0

![Novo](../assets/new.svg) <!-- PB-494 -->Suporte adicionado para o PHP 7.4.

![Correção de um problema](../assets/fix.svg) <!-- MC-31247 -->Correção de um problema em que o tipo de conteúdo Produtos não mostrava produtos configuráveis quando a condição era definida como preço.

![Correção de um problema](../assets/fix.svg) <!-- PB-179 -->Corrigido a configuração de alinhamento de Produtos para posicionar somente o próprio contêiner do produto, não o conteúdo do contêiner do produto, como nome do produto, preço, botões, imagens e outros elementos.

![Problema corrigido](../assets/fix.svg) <!-- MC-33556 -->Melhorias de desempenho.

![Correção de um problema](../assets/fix.svg) de aprimoramentos de segurança.

## 1.3.3-p1 para Adobe Commerce 2.3.6-p1

![Correção de um problema](../assets/fix.svg) de aprimoramentos de segurança.

## 1.3.3 para Adobe Commerce 2.3.6

![Correção de um problema](../assets/fix.svg) <!-- MC-32766 -->Correção do tipo de conteúdo Texto para salvar corretamente as diretivas de variável adicionadas aos atributos html.

![Correção de um problema](../assets/fix.svg) <!-- MC-34590 -->Corrigido o tipo de conteúdo de texto para manipular e salvar corretamente caracteres não latinos-1.

![Correção de um problema](../assets/fix.svg) <!-- MC-34677 -->Correção de [!DNL Page Builder] estilos CSS que fazia com que o Safari 13.1 renderizasse incorretamente o menu de site do tema Luma para pequenas portas de exibição e telas móveis.

![Problema corrigido](../assets/fix.svg) <!-- MC-34846 -->Corrigido o tipo de conteúdo de HTML para exibir corretamente widgets inseridos como _Solicitar por SKU_ na loja.

![Correção de um problema](../assets/fix.svg) que corrigia um erro que, ocasionalmente, impedia os usuários de salvar formulários de tipo de conteúdo. O erro (&quot;[!DNL Page Builder] foi renderizado por 5 segundos sem liberar bloqueios&quot;) fez com que o ícone do carregador girasse indefinidamente após tentar salvar um formulário.

## 1.3.2 para Adobe Commerce 2.3.5-p2

![Novos](../assets/new.svg) aprimoramentos de segurança.

## 1.3.1 para Adobe Commerce 2.3.5-p1

Esta versão do [!DNL Page Builder] é apenas uma atualização de número de versão para o Adobe Commerce 2.3.5-p1. Todos os recursos descritos para a versão 1.3.0 se aplicam a esta versão também.

## 1.3.0 para Adobe Commerce 2.3.5

![Novos](../assets/new.svg) **Modelos** - [!DNL Page Builder] agora tem modelos que podem ser criados a partir de conteúdo existente e aplicados a novas áreas de conteúdo. [!DNL Page Builder] modelos salvam o conteúdo e os layouts de páginas, blocos, blocos dinâmicos, atributos de produto e descrições de categoria existentes. Por exemplo, você pode salvar uma página do CMS [!DNL Page Builder] existente como modelo e, em seguida, aplicar esse modelo (com todo o seu conteúdo e layouts) para criar rapidamente as Páginas do CMS para o seu site. Este novo recurso está documentado aqui: [Modelos](templates.md).

![Novo](../assets/new.svg) **Planos de Fundo de Vídeo para Linhas, Banners e Controles Deslizantes** - [!DNL Page Builder] Linhas, Banners e Controles Deslizantes agora podem usar vídeos para seus planos de fundo. Estes novos recursos estão documentados aqui: [Linhas](row.md), [Banners](banner.md), [Sliders](slider.md).

![Novo](../assets/new.svg) **Adições e aprimoramentos de suporte de vídeo** - [!DNL Page Builder] agora oferece suporte a uma variedade maior de formatos de vídeo. Além dos vídeos do YouTube e do Vimeo, o tipo de conteúdo do Vídeo e os planos de fundo do vídeo agora oferecem suporte a links de URL de vídeo para formatos de vídeo como `.mp4` e outros formatos compatíveis com o navegador. O tipo de conteúdo Vídeo também adiciona um recurso de reprodução automática. Estes novos recursos estão documentados aqui: [Tipo de conteúdo do vídeo](video.md).

![Novo](../assets/new.svg) **Linhas de Altura Completa, Banners e Controles Deslizantes** - [!DNL Page Builder] Linhas, Banners e Controles Deslizantes agora podem definir suas alturas para a altura completa da página usando um número com qualquer unidade CSS (px, %, vh, em) ou um cálculo entre unidades (100vh - 237px). Estes novos recursos estão documentados aqui: [Linhas](row.md), [Banners](banner.md), [Sliders](slider.md).

![Nova](../assets/new.svg) **Biblioteca de atualização de tipo de conteúdo** - Os desenvolvedores agora podem criar versões de [!DNL Page Builder] tipos de conteúdo sem introduzir problemas incompatíveis com versões anteriores. Antes desta versão, alterações significativas nas configurações de tipo de conteúdo criariam problemas de exibição e perda de dados com tipos de conteúdo [!DNL Page Builder] salvos anteriormente. A nova biblioteca de atualização elimina esses problemas. A biblioteca foi projetada para atualizar versões anteriores de tipos de conteúdo salvas no banco de dados para que correspondam às alterações de configuração nas novas versões. O [!DNL Page Builder] executa a biblioteca de atualização em tipos de conteúdo nativos, conforme necessário para uma nova versão. Essa alteração garante que os tipos de conteúdo [!DNL Page Builder] internos sejam sempre atualizados para corresponder a qualquer alteração feita nos tipos de conteúdo para uma versão mais recente.

>[!IMPORTANT]
>
>Se você tiver criado entidades de banco de dados adicionais para armazenar conteúdo [!DNL Page Builder], _deverá_ adicionar essas entidades ao seu `etc/di.xml`. Caso contrário, o conteúdo [!DNL Page Builder] armazenado na sua entidade não será atualizado, causando possível perda de dados e problemas de exibição. Por exemplo, se você criou uma entidade de blog que armazena conteúdo [!DNL Page Builder], deve adicionar a entidade de blog ao arquivo `etc/di.xml` como um tipo `UpgradableEntitiesPool` para que a biblioteca de atualização possa atualizar os tipos de conteúdo [!DNL Page Builder] usados no blog. Para obter mais informações e instruções sobre como usar a biblioteca de atualização, consulte [Atualizar tipos de conteúdo](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) no _Guia do Desenvolvedor do Page Builder_.

![Nova](../assets/new.svg) **Documentação para adicionar novas aparências** - As informações do desenvolvedor agora foram publicadas sobre [adição de aparências](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) para tipos de conteúdo existentes ou personalizados.

![Correção de um problema](../assets/fix.svg) **Várias correções**

- &#x200B;<!-- PB-50 -->Correção de um problema em que o menu TinyMCE para o conteúdo do slide era exibido abaixo de outros tipos de conteúdo se o contêiner principal do slide fosse duplicado.
- &#x200B;<!-- PB-166 -->Atualização de [!DNL Page Builder] para implementar um método destroy para evitar vazamentos de memória em alguns cenários.
- &#x200B;<!-- PB-170 -->Aprimoramento do desempenho do TinyMCE quando várias instâncias são usadas no estágio de Administração.
- &#x200B;<!-- PB-252 -->Correção de um problema em que o tipo de conteúdo Bloco dinâmico não é renderizado no estágio de Administração se a linha superior estiver marcada como oculta.
- &#x200B;<!-- PB-273 -->Refinamento dos eventos de passar o mouse no estágio de Administração ao remover um atraso de 200 ms de vários controles da interface do usuário. Essa alteração facilita o trabalho com itens de conteúdo aninhados no estágio.
- &#x200B;<!-- PB-294 -->Correção de um problema em que o símbolo de moeda era escapado incorretamente no widget Lista de produtos no Bloco/Bloco dinâmico no estágio Administração.
- &#x200B;<!-- PB-296 -->Correção de um problema em que o total de produto no painel de edição [!DNL Page Builder] não funcionava para produtos de estoque MSI personalizados.
- &#x200B;<!-- PB-317 -->Correção de um problema em que salvar o conteúdo do [!DNL Page Builder] com imagens de plano de fundo no Microsoft Edge não renderiza essas imagens na loja.
- &#x200B;<!-- PB-390 -->Correção de um problema em que o conteúdo [!DNL Page Builder] aninhado não era salvo se os usuários clicassem no botão Salvar antes que a página fosse totalmente renderizada.
- &#x200B;<!-- PB-418 -->Correção de um erro de exceção lançado em trabalhos cron devido à análise [!DNL Page Builder].

## 1.2.2 para Adobe Commerce 2.3.4-p2

![Novos](../assets/new.svg) aprimoramentos de segurança.

## 1.2.1 para Adobe Commerce 2.3.4-p1

![Novos](../assets/new.svg) aprimoramentos de segurança.

## 1.2.0 para Adobe Commerce 2.3.4

![Nova](../assets/new.svg) integração de **[!DNL Page Builder]com o PWA Studio** - Adição da renderização de conteúdo [!DNL Page Builder] ao aplicativo Venia no PWA Studio. O conteúdo [!DNL Page Builder] agora pode ser visualizado no aplicativo PWA Studio Venia. Consulte a documentação [!DNL Page Builder] em [PWA Studio] para obter todas as informações sobre este novo recurso.

![Novo](../assets/new.svg) **Carrossel de produtos adicionado** - <!-- PB-77, PB-173, PB-175 -->O tipo de conteúdo Produtos agora fornece uma opção para exibir seus produtos no formato de carrossel/controle deslizante, incluindo várias opções para personalizar o carrossel de acordo com suas necessidades.

![Novo](../assets/new.svg) **Classificação de SKU de produto adicionada** - <!-- PB-69 -->O tipo de conteúdo Produtos agora fornece uma opção para classificar seus produtos por SKU na ordem em que você os adiciona a uma lista no Administrador.

![Novo](../assets/new.svg) **Classificação de Categoria de Produto Adicionada** - <!-- PB-181 -->. O tipo de conteúdo Produtos agora fornece uma opção para classificar seus produtos por categoria _posição_, exibindo-os na mesma ordem em que aparecem no Catálogo do Commerce.

![Novo](../assets/new.svg) **Totais de seleção de produtos adicionados** - <!-- PB-107 -->. O editor Admin do tipo de conteúdo Produtos agora exibe o número total de produtos que correspondem às opções de seleção de produtos.

![Correção de um problema](../assets/fix.svg) **Várias correções**

- &#x200B;<!-- PB-237 -->Aprimoramentos de segurança.
- &#x200B;<!-- PB-41 -->Pesquisas corrigidas na interface do usuário selecionam componentes para fazer apenas uma solicitação AJAX por termo de pesquisa.
- &#x200B;<!-- PB-76, PB-84-->Pré-visualizações do produto atualizadas no Administrador para corresponder à loja, incluindo a classificação por estrelas, a cor e as opções de tamanho do produto, quando relevantes.
- &#x200B;<!-- PB-169 -->Correção de um problema em que [!DNL Page Builder] não podia ser salvo quando a minificação e o agrupamento de JavaScript estavam habilitados no Commerce.
- &#x200B;<!-- PB-241 -->Correção das visualizações de Produtos, Blocos e Blocos dinâmicos do Administrador para renderização correta em instalações do Commerce que definem URLs diferentes para o Administrador e o front-end.
- &#x200B;<!-- PB-238 -->Correção das visualizações de Produtos, Blocos e Blocos dinâmicos do Administrador para renderização correta em instalações do Commerce com B2B instalado com a opção _Somente logon_ habilitada. Antes dessa correção, a visualização do [!DNL Page Builder] fazia com que a página fosse redirecionada para o logon da conta do cliente.
- &#x200B;<!-- PB-239 -->Correção de um erro de sessão que pode ocorrer ao visualizar uma página grande no Administrador [!DNL Page Builder].
- &#x200B;<!-- PB-248 -->Atualização de [!DNL Page Builder] estilos MENOS para impedir a duplicação de estilo de vitrine.

## 1.1.1 para Adobe Commerce 2.3.3-p1

![Novos](../assets/new.svg) aprimoramentos de segurança.

## 1.1.0 para Adobe Commerce 2.3.3

![Novo](../assets/new.svg) <!-- MC-15250 -->Classificação de produto explícita adicionada ao tipo de conteúdo Produtos.

![Novo](../assets/new.svg) <!-- MC-17823 -->Adição de botões para inserir imagens, widgets e variáveis no tipo de conteúdo HTML.

![Correção de um problema](../assets/fix.svg) Melhoria na segurança [!DNL Page Builder].

![Problema corrigido](../assets/fix.svg) <!-- MC-1805 -->Atualizado [!DNL Page Builder] para oferecer suporte ao PHP versão 7.3.

![Correção de um problema](../assets/fix.svg) <!-- MC-4137 -->Atualização do TinyMCE para a versão 4.9.5. Essa atualização, juntamente com as melhorias adicionais, corrigiu vários problemas do editor em linha TinyMCE:

- Variáveis, imagens e links de imagem são adicionados onde o cursor está posicionado.
- Tabelas e células da tabela podem ser alinhadas ao centro.
- Copiar/colar agora cola o conteúdo na posição do cursor.
- Os links podem ser aplicados ao texto selecionado.
- Os marcadores estão alinhados corretamente.
- As alterações no editor integrado podem ser salvas sem primeiro clicar fora do editor.

![Correção de um problema](../assets/fix.svg) <!-- MC-3880 -->Correção de um problema em que a altura mínima e o alinhamento vertical eram inconsistentes entre as seções no painel de edição para cada tipo de conteúdo.

![Correção de um problema](../assets/fix.svg) <!-- MC-14994 -->Correção de um problema em que a barra de ferramentas do tipo de conteúdo Cabeçalho era posicionada incorretamente quando solta pela primeira vez no palco.

![Correção de um problema](../assets/fix.svg) <!-- MC-15742 -->Correção das margens embutidas em código nos tipos de conteúdo Controle Deslizante e Vídeo.

![Correção de um problema](../assets/fix.svg) <!-- MC-16241 -->Correção de um problema no qual o símbolo de asterisco obrigatório era exibido duas vezes em campos de formulário.

## 1.0.3 para Adobe Commerce 2.3.2-p2

![Novos](../assets/new.svg) aprimoramentos de segurança.

## 1.0.2 para Adobe Commerce 2.3.2-p1

![Novos](../assets/new.svg) aprimoramentos de segurança.

## 1.0.1 para Adobe Commerce 2.3.2

![Novo](../assets/new.svg) Garante a compatibilidade com o Adobe Commerce 2.3.2.

## 1.0.0 para Adobe Commerce 2.3.1

![Nova](../assets/new.svg) Versão de disponibilidade geral


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
