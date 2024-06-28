---
title: '[!DNL Adobe Commerce B2B] notas de versão'
description: Revise as notas de versão para obter informações sobre alterações no [!DNL Adobe Commerce B2B] versões.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 17eec4e7755ce4e83fb0533940bdce6c96ddc717
workflow-type: tm+mt
source-wordcount: '6867'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] notas de versão

Essas notas de versão para a extensão B2B capturam adições e correções que o Adobe adicionou durante um ciclo de lançamento, incluindo:

![Novo](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e aprimoramentos
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

>[!NOTE]
>
>Consulte [Disponibilidade do produto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) para obter informações sobre versões da extensão B2B do Commerce compatíveis com versões disponíveis do Adobe Commerce.

## B2B 1.5.0-beta

{{$include /help/_includes/b2b-beta-note.md}}

*13 de novembro de 2023*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

A versão B2B v1.5.0-beta inclui novos recursos, melhorias de qualidade e correções de erros.

![Novo](../assets/new.svg) As melhorias nos recursos de cotação ajudam os Compradores e os Vendedores a gerenciar cotações e negociações de cotações com mais eficiência.

- **Salvar Cotação como Rascunho**<!--B2B-2566-->—Ao criar um [solicitação de cotação](quote-request.md) no carrinho de compras, os compradores agora podem salvar a cotação como rascunho selecionando **[!UICONTROL Save as Draft]** no [!UICONTROL Request a Quote] formulário.

  A cotação de rascunho não tem uma data de expiração. Os compradores podem revisar e atualizar cotações de rascunho a partir do [!UICONTROL My Quotes] no painel de contas.

- **Renomear Cotação**<!--B2B-2596-->—Os compradores agora podem alterar o nome de uma cotação a partir do [Detalhes da cotação](account-dashboard-my-quotes.md#quote-actions) selecionando o **[!UICONTROL Rename]** opção. Essa opção está disponível para compradores autorizados ao editar a cotação. Os eventos de alteração de nome são registrados no Log de Histórico de Cotações.

- **Cotação Duplicada**<!--B2B-2701-->—Compradores e vendedores agora podem criar uma nova cotação copiando uma cotação existente. Uma cópia é criada na exibição de detalhes da Cotação selecionando  **[!UICONTROL Create Copy]** no [Exibição detalhada da cotação](quote-price-negotiation.md#button-bar) no Administrador ou no [Loja](account-dashboard-my-quotes.md#quote-actions).

- **Bloqueio de desconto de item de linha**<!--B2B-2597-->—Durante a negociação de cotas, os vendedores podem usar o bloqueio de desconto de item de linha para obter mais flexibilidade ao aplicar descontos. Por exemplo, um Vendedor pode aplicar um desconto de item de linha especial a um item e bloquear o item para evitar mais descontos. Quando um item está bloqueado, o preço do item não pode ser atualizado quando um desconto em nível de cotação é aplicado. Consulte [Iniciar cotação para um comprador](sales-rep-initiates-quote.md).

![Novo ](../assets/new.svg)**Gerenciamento da Empresa**<!--B2B-2901-->— Agora, os comerciantes podem exibir e gerenciar empresas da Adobe Commerce como organizações hierárquicas, atribuindo empresas a empresas-pai designadas. Depois que uma empresa é atribuída a uma empresa principal, o administrador da empresa principal pode gerenciar a conta da empresa. Somente usuários administradores autorizados podem adicionar e gerenciar atribuições da empresa. Para obter detalhes, consulte [Gerenciar hierarquia da empresa](assign-companies.md).

- Na página Empresas, uma nova **[!UICONTROL Company Type]** O campo identifica empresas principais e secundárias. Os comerciantes podem filtrar a exibição da empresa por tipo de empresa e gerenciar empresas usando itens de linha ou ações em massa.

- Os comerciantes podem adicionar e gerenciar atribuições da empresa a partir do novo **[!UICONTROL Company Hierarchy]** seção no [!UICONTROL Company Account] página.

- Os desenvolvedores de API podem usar o novo endpoint da API REST de Relações com a empresa `/V1/company/{parentId}/relations` para criar, exibir e remover atribuições da empresa. Consulte [Gerenciar objetos da empresa](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) no *Guia do desenvolvedor da API da Web*.

![Problema corrigido](../assets/fix.svg)<!--ACP2E-1984-->Comerciantes que clicam no **[!UICONTROL Print]** na visualização de detalhes da Cotação no Admin agora são solicitados a salvar a cotação como um PDF. Anteriormente, os comerciantes eram redirecionados para uma página que continha detalhes de cotação.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1742-->Anteriormente, ao enviar uma cotação de cliente com porcentagem 0 e alterar a quantidade, o administrador lança uma exceção, mas salva a quantidade. Depois que essa correção se aplicar, para o `0 percentage` a exceção adequada com uma mensagem será lançada.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1742-->Durante a negociação de cotas, um vendedor agora pode especificar uma `0%` desconto no campo Desconto de cotação da Cotação Negociada e envie a cotação de volta ao comprador. Anteriormente, se o vendedor inserisse um desconto de 0% e enviasse a cotação de volta ao comprador, o Administrador retornaria uma `Exception occurred during quote sending` mensagem de erro.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-2097-->A validação do ReCaptcha agora funciona corretamente durante o processo de finalização de uma cotação B2B quando o ReCaptcha V3 é configurado para finalização de loja. Anteriormente, a validação falhava com uma `recaptcha validation failed, please try again` mensagem de erro.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1825-->As ordens de compra não podem mais ser feitas por um usuário associado à empresa após o bloqueio dela. Anteriormente, um usuário associado à empresa podia fazer pedidos de compra quando a empresa era bloqueada.

![Problema corrigido](../assets/fix.svg)<!--ACP2E-1933-->Os administradores da empresa agora podem adicionar usuários da empresa na loja. Anteriormente, o Commerce registrava um erro quando um usuário administrador tentava adicionar um novo usuário: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2-p1

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança 2.4.7-p1 e 2.4.6-p6 do Adobe Commerce.


## B2B v1.4.2

*10 de outubro de 2023*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

A versão B2B v1.4.2 inclui melhorias de qualidade e correções de erros

![Problema corrigido](../assets/fix.svg) <!--B2B-2897-->Se um Vendedor criar uma cotação de comprador que inclua um SKU de produto não disponível no catálogo compartilhado associado à empresa compradora, o sistema exibirá a mensagem de erro `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  O Vendedor não pode salvar a cotação até que ele remova o produto que não está disponível. Anteriormente, a cotação era salva com o SKU indisponível incluído e a cotação não era carregada na loja.

## B2B v1.4.1

*7 de agosto de 2023*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatível com o Adobe Commerce 2.4.7-beta1.

A versão B2B v1.4.1 inclui melhorias de qualidade e correções de erros.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1825-->As ordens de compra não podem mais ser feitas por um usuário associado à empresa após o bloqueio dela. Anteriormente, um usuário associado à empresa podia fazer pedidos de compra quando a empresa era bloqueada.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1943-->O status do produto com backorder agora é exibido corretamente na loja. Anteriormente, os produtos que estavam disponíveis para remessa eram identificados incorretamente como em backorder.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1862-->Se o formulário de registro da empresa incluir um atributo de tipo de arquivo do cliente, o arquivo carregado durante o processo de registro agora será incluído nas informações de conta do Administrador da empresa, após a criação da empresa. Anteriormente, o anexo estava ausente.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1793-->O seletor de amostras de um produto configurável agora é exibido conforme esperado na página de configuração do item de lista de requisições. Anteriormente, o seletor de amostras era exibido como um campo suspenso na página de configuração do item de lista de requisições.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1968-->Ao usar o [Consulta do GraphQL da empresa](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) para retornar os detalhes da empresa, os resultados agora são retornados com êxito sem erro.

## B2B v1.4.0

*13 de junho de 2023*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatível com o Adobe Commerce 2.4.7-beta1

Esta versão inclui novos recursos e melhorias para cotações negociáveis B2B e várias correções de erros.

![Novo](../assets/new.svg) Adição de compatibilidade com o Adobe Commerce 2.4.7-beta1.

![Novo](../assets/new.svg) **Cotações iniciadas pelo vendedor**—Os vendedores agora podem iniciar um orçamento para um comprador diretamente das grades de Cotação e Cliente no Admin. Esse recurso simplifica o processo de cotação e reduz a complexidade para os clientes. Se um cliente não tiver iniciado uma ordem, um vendedor poderá criar rapidamente uma cota em nome do cliente e iniciar o processo de negociação. Anteriormente, só era possível criar cotações na loja pelo comprador ou por um vendedor conectado como cliente.

![Novo](../assets/new.svg) **Negociação e descontos de item de linha**—<!--B2B-2440--> Dentro de uma cotação, compradores e vendedores B2B agora podem negociar no nível do item de linha, aplicando descontos e trocando notas até que um acordo seja alcançado. A criação de notas e as atualizações estão incluídas no item da linha e no histórico de cotações para rastrear a comunicação. Anteriormente, compradores e vendedores só podiam trocar notas e aplicar descontos no nível da cotação.

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe os detalhes corretos durante o pagamento quando a opção Pedidos de compra está habilitada e uma cotação virtual criada com a opção de pagamento PayPal foi selecionada. Anteriormente, os totais eram exibidos como zero sob essas condições.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1504--> Os erros de validação não ocorrem mais quando você tenta salvar uma empresa com um limite de crédito que excede 999. Anteriormente, para limites de crédito de empresa maiores que 999, o Adobe commerce inseriu um separador de vírgula, o que causou um erro de validação que impedia que as atualizações fossem salvas.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1474-->  O endereço de entrega selecionado agora permanece inalterado quando você faz um pedido com uma cotação negociável. Anteriormente, quando você fazia um pedido, o endereço de entrega selecionado era alterado para o endereço de entrega padrão.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1429--> Nas definições de Configuração da loja para Recursos B2B, a variável **[!UICONTROL Enable Shared Catalog direct products price assigning]** O campo agora é desativado automaticamente. Na loja, ele fica oculto quando a variável **[!UICONTROL Enable Company]** configuração ou **[!UICONTROL Enable Shared Catalog]** está definida como **[!UICONTROL No]**.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1683--> Ao criar uma conta de empresa na loja, o Commerce agora valida o endereço de email antes de processar o registro da empresa. Se o endereço de email for inválido, a operação falhará e nenhuma atualização de conta será processada. Anteriormente, uma conta de cliente era criada mesmo se a solicitação para criar uma conta de empresa falhasse devido a um endereço de email inválido.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1664--> As SKUs de produto que incluem aspas duplas no Catálogo compartilhado e na estrutura de preços não causam mais erros no Administrador.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1498--> Atualização da configuração de verniz para o aplicativo Commerce para impedir que usuários convidados vejam dados de outros grupos de clientes.

### Problema conhecido

Se você instalar ou atualizar o B2B 1.4.0 em [Adobe Commerce versão 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), o seguinte erro ocorre:

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Você pode corrigir esse problema adicionando dependências manuais para o pacote de segurança B2B adicionando dependências manuais para o pacote de segurança B2B com uma [marca de estabilidade](https://getcomposer.org/doc/04-schema.md#package-links). Para obter instruções, consulte [Base de conhecimento Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*14 de março de 2023*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Lançada a versão B2B 1.3.5-p2 para suportar compatibilidade com o Adobe Commerce 2.4.6-p2.

![Novo](../assets/new.svg) Lançada a versão B2B 1.3.5-p1 para oferecer suporte à compatibilidade com o Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>Depois de atualizar o Commerce da versão 2.4.6 para a [versão mais recente](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6), certifique-se de atualizar para a versão de patch B2B 1.3.5 compatível. Ou atualize a extensão B2B da versão 1.3.5 para a versão 1.4.0 ou posterior para obter os recursos mais recentes.

![Novo](../assets/new.svg) Adição de suporte para o Adobe Commerce 2.4.6.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-689--> O Adobe Commerce agora exibe os detalhes corretos durante o pagamento quando a opção Pedidos de compra está habilitada e uma cotação virtual criada com a opção de pagamento PayPal foi selecionada. Anteriormente, os totais eram exibidos como zero sob essas condições.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-609--> A lista de grupos de clientes para o **Permitir Categoria de Navegação** a configuração não contém mais grupos de clientes relacionados a catálogos compartilhados.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1244--> O atributo de cliente Número de Imposto/IVA agora funciona conforme esperado com contas de administrador de empresa no Administrador e na loja. Os atributos de Imposto/IVA personalizados não são mais necessários para criar uma conta da empresa. Anteriormente, quando um comerciante criava uma conta da empresa com um atributo personalizado de Imposto/IVA, a Adobe Commerce exibia um erro de validação na vitrine e no Administrador.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1236--> A desativação do recurso de catálogo compartilhado em um escopo específico agora funciona corretamente. Anteriormente, o Adobe Commerce definia um escopo inválido quando um comerciante salvava a configuração de catálogo compartilhado.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1203--> Agora, os usuários administradores podem salvar valores de atributos personalizados de clientes para usuários de empresas. Anteriormente, os atributos personalizados do cliente para usuários da empresa não podiam ser salvos.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1221--> Os problemas de desempenho são resolvidos com a validação das permissões da empresa fornecidas pelo GraphQL quando muitas permissões da empresa já estão atribuídas.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1242--> O Adobe Commerce não lança mais um erro na página do carrinho quando o Pedido rápido é usado para adicionar um produto em uma quantidade que excede o estoque disponível.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1090--> O desempenho do `SELECT` as operações de permissões da empresa foram aprimoradas.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-2456--> As consultas de categoria agora retornam preços de produto de acordo com as configurações da loja quando não há permissões de categoria explicitamente definidas na categoria que está sendo consultada.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-6829--> A variável **[!UICONTROL Place Order]** agora funciona conforme esperado ao concluir uma compra com uma solicitação de cotação aprovada. Problemas com a cotação negociável `negotiableQuoteCheckoutSessionPlugin` plug-in foram resolvidos.

## B2B v1.3.4

*9 de agosto de 2022*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Adição de suporte para o Adobe Commerce 2.4.5.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-453-->O Adobe Commerce não envia mais notificações por email sempre que uma Empresa existente é atualizada por uma chamada de API. Agora, os emails são enviados somente quando uma empresa é criada.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-406-->O Adobe Commerce agora calcula corretamente o total geral de uma cotação negociável quando a variável **[!UICONTROL Enable Cross Border Trade]** a configuração de cálculo de imposto está habilitada.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-322-->Os produtos configuráveis agora são movidos para a última posição na lista de produtos depois que o estoque é atualizado quando o **[!UICONTROL Move out of stock to the bottom]** está ativada. Uma nova consulta de banco de dados personalizado é implementada para garantir que a ordem de classificação do índice Elasticsearch agora atenda à ordem de classificação habilitada pelo Administrador. Anteriormente, os produtos configuráveis e seus produtos derivados não eram movidos para a parte inferior da lista quando essa configuração era ativada.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-308-->O email de Ordem de compra agora respeita a configuração de envio de email de cada site em uma implantação multissite. Uma verificação para a **[!UICONTROL Disable Email Communications]** é adicionada à lógica personalizada para filas de email. Anteriormente, o Adobe Commerce não respeitava a configuração de envio de email para o site secundário.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-302-->O título do campo SKU da página Pedido rápido é alterado para maior clareza.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-543-->O Adobe Commerce agora exibe uma mensagem de erro mais informativa quando um comprador insere um SKU inválido no **Insira o SKU ou o nome do produto** campo.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1753-->A variável **[!UICONTROL Account Created in]** O campo para um administrador de empresa agora retém seu valor como esperado depois que você salva a empresa.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-722 -->A variável `customer` a consulta não retorna mais resultados vazios quando recupera listas de requisições filtradas por `uid`.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-210 -->Adição de um plug-in antes da `collectQuoteTotals` chamada para garantir que os créditos da loja sejam aplicados apenas uma vez.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-665 -->Os clientes agora são redirecionados para a página de logon quando sua conta é excluída por um administrador do Admin. Anteriormente, o Adobe Commerce emitia um erro. O plug-in (`SessionPlugin`) bloco de código agora está dentro do `try…catch` bloco. Anteriormente, esse código não era encapsulado dentro do bloco genérico de manipulação de exceções.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-661 --> Na página Pedido rápido no modo móvel, pressionando **Enter** depois de inserir um nome de produto válido ou SKU, agora o leva ao próximo campo, conforme esperado.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-607 -->O nome da empresa agora está visível, conforme esperado, nas seções de endereço de faturamento e envio do fluxo de trabalho de finalização.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-375 -->O crédito da loja agora está indisponível quando a variável **[!UICONTROL Zero Subtotal Checkout]** método de pagamento desabilitado. Anteriormente, a caixa de seleção Armazenar crédito não funcionava durante a realização do pedido pelo administrador. O aplicativo não colocou o pedido com o crédito da loja e exibiu este erro: `The requested Payment Method is not available`.

## B2B v1.3.3

*9 de agosto de 2022*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Adição de suporte para o Adobe Commerce 2.4.4.

![Problema corrigido](../assets/fix.svg) <!--- MC-41985--> O tempo necessário para atualizar do Adobe Commerce 2.3.x para o Adobe Commerce 2.4.x em implantações com mais de 100.000 funções da empresa foi substancialmente reduzido.

![Problema corrigido](../assets/fix.svg) <!--- MC-42153--> O POST `V1/order/:orderId/invoice` a solicitação agora suporta a criação de faturas parciais quando o **[!UICONTROL Payment on Account]** método de pagamento está habilitado. Anteriormente, o Adobe Commerce exibia este erro: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Problema corrigido](../assets/fix.svg) <!--- MC-41975--> O PayPal Payflow Pro agora funciona conforme esperado com a cotação negociável B2B quando o carrinho do cliente contém outros produtos. O Adobe Commerce agora processa o pedido com êxito e envia um email ao cliente, conforme esperado. Anteriormente, o Adobe Commerce emitia um erro fatal e enviava um email de confirmação para o cliente com valor zero.

![Problema corrigido](../assets/fix.svg) <!--- MC-41819--> A paginação agora é exibida corretamente na página de resultados da pesquisa do catálogo depois de excluir alguns produtos do catálogo compartilhado.

![Problema corrigido](../assets/fix.svg) <!--- MC-42886--> Os atributos personalizados do cliente agora são salvos conforme esperado ao criar ou salvar um usuário da empresa no Administrador.

![Problema corrigido](../assets/fix.svg) <!--- MC-42927--> A variável **[!UICONTROL Submit]** No formulário Criar nova empresa, o botão agora está desativado após um clique para impedir vários envios de formulários. Anteriormente, você podia enviar esse formulário várias vezes clicando nesse botão repetidamente, o que gerou um erro.

![Problema corrigido](../assets/fix.svg) <!--- MC-42787--> O Adobe Commerce não exibe mais o link de reordenação na loja quando um comprador faz logon em uma loja para a qual os reordenamentos foram desativados.

![Problema corrigido](../assets/fix.svg) <!--- MC-43115--> A Pesquisa rápida de pedido por SKU agora não diferencia maiúsculas de minúsculas quando o catálogo compartilhado está ativado.

![Problema corrigido](../assets/fix.svg) <!--- MC-42203--> Agora é possível atualizar um arquivo para um atributo do cliente ao criar uma empresa. Anteriormente, ao tentar criar uma empresa com um anexo do tipo `File`, a Adobe Commerce não criou a empresa e registrou este erro no log de exceções: `Something went wrong while saving file`.

![Problema corrigido](../assets/fix.svg) <!--- MC-42242--> Agora é possível criar uma empresa com uma conta de cliente que tenha um atributo personalizado com um (`File`) ou (`Image`) tipo. Anteriormente, se a conta tivesse uma dessas opções personalizáveis, o carregador de página de edição da Empresa não resolvia o, o que impedia a edição dos detalhes da empresa.

![Problema corrigido](../assets/fix.svg) <!--- MC-42268--> A variável `products` a consulta agora retorna uma `total_count` quando o catálogo compartilhado está ativado.

![Problema corrigido](../assets/fix.svg) <!--- MC-42203-->  Agora é possível atualizar um arquivo para um atributo do cliente ao criar uma empresa. Anteriormente, ao tentar criar uma empresa com um anexo do tipo `File`, a Adobe Commerce não criou a empresa e registrou este erro no log de exceções: `Something went wrong while saving file`.

![Problema corrigido](../assets/fix.svg) <!--- MC-43178--> A variável _Configuração da empresa_ e _Criar empresa_ as páginas agora funcionam como esperado depois de desativar um método de envio online. A verificação foi adicionada para impedir a tentativa de processamento de módulos de envio desabilitados. Anteriormente, o Adobe Commerce exibia este erro: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Problema corrigido](../assets/fix.svg) <!--- MC-42214--> A variável _Categoria_ A página do agora exibe dados de produto consistentes enquanto as permissões são geradas durante a indexação parcial. Um novo indexador parcial para permissões de diretório foi adicionado a este processo. Anteriormente, os dados exibidos enquanto o indexador era executado estavam incorretos.

![Problema corrigido](../assets/fix.svg) <!--- MC-42567--> A variável `categoryList` o query agora retorna o número correto de produtos quando as permissões de catálogo são usadas e os produtos são atribuídos a um catálogo compartilhado.

![Problema corrigido](../assets/fix.svg) <!--- MC-42528--> A variável `categoryList` a consulta agora respeita as permissões da categoria e retorna somente as categorias permitidas. Anteriormente, retornava todas as categorias atribuídas e não atribuídas.

![Problema corrigido](../assets/fix.svg) <!--- MC-42399--> A variável `rest/V1/company/{id}` a solicitação agora retorna `is_purchase_order_enabled` valores de atributo conforme esperado.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-128--> Os atributos personalizados do cliente agora são exibidos conforme esperado na _Administrador da empresa_ guia.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-130--> O bloco Minha lista de desejos na página Minha conta agora é exibido, conforme esperado, para Administradores da empresa e Usuários da empresa.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-133--> Os erros de Pedido rápido não são mais exibidos no carrinho de compras. Anteriormente, o Adobe Commerce exibia esse erro no carrinho de compras quando o SKU não era encontrado no catálogo:  `The SKU was not found in the catalog`.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-194--> As operações de salvamento do catálogo compartilhado foram otimizadas para execução mais rápida. Anteriormente, salvar um catálogo compartilhado com muitos grupos de clientes podia levar vários minutos.

![Problema corrigido](../assets/fix.svg) <!--- MC-42240--> O Adobe Commerce agora exclui todas as permissões de subcategoria da `sharedcatalog_category_permissions` tabela quando a categoria principal é excluída. Anteriormente, somente os dados da categoria principal eram removidos.

## B2B v1.3.2

*29 de agosto de 2022*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Adição de suporte para o Adobe Commerce 2.4.3.

![Problema corrigido](../assets/fix.svg) <!--- MC-39862--> O Adobe Commerce agora envia emails de atualização sobre cotações negociáveis expiradas com sucesso. Anteriormente, quando uma cotação negociável expirava, o Adobe Commerce não enviava emails de atualização.

![Problema corrigido](../assets/fix.svg) <!--- MC-40682--> O Adobe Commerce agora envia emails de atualização sobre cotações negociáveis prestes a expirar e expiradas quando um `cron` tarefa ausente.

### Empresa

![Problema corrigido](../assets/fix.svg) <!--- MC-41542--> O campo suspenso Criar novo país da página de conta da empresa não lista mais os valores de opção vazios. Anteriormente, os dois primeiros valores de opção e o código do país `AN` estavam vazias.

![Problema corrigido](../assets/fix.svg) <!--- MC-41260--> Clicar no **[!UICONTROL Return]** para um pedido que foi criado por um usuário da empresa agora redireciona um usuário administrativo para a página Criar devolução, conforme esperado. Anteriormente, o administrador era redirecionado para a página Histórico de pedidos.

![Problema corrigido](../assets/fix.svg) <!--- MC-40798--> O Adobe Commerce não falha mais com um erro de falta de memória ao executar o `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` durante `bin/magento setup:upgrade`. Anteriormente, o Adobe Commerce não usava o tamanho do lote para a coleção ao inicializar permissões, mas carregava uma coleção de todas as funções da empresa.

![Problema corrigido](../assets/fix.svg) <!--- MC-40551--> Os usuários da empresa agora podem editar e atualizar valores de atributos personalizados do cliente. Anteriormente, esses atributos não se vinculavam corretamente ao formulário criar e editar usuário. Um usuário da empresa poderia inserir valores de atributo diferentes, mas o Adobe Commerce não salvou esses valores corretamente.

![Problema corrigido](../assets/fix.svg) <!--- MC-32653--> A árvore de recursos para permissões de função da empresa agora pode ser traduzida conforme esperado. Anteriormente, a árvore de permissões não era traduzida, mesmo se arquivos de tradução válidos estivessem presentes.

![Problema corrigido](../assets/fix.svg) <!--- MC-40358--> O Adobe Commerce agora salva valores de atributos do cliente personalizados para usuários B2B, conforme esperado. Anteriormente, a criação de uma conta de empresa que contivesse atributos personalizados do cliente acionava um erro de modelo e o Adobe Commerce não carregava o formulário com êxito. Adicionar um argumento ao layout de `company_create_account` resolveu esse problema.

![Problema corrigido](../assets/fix.svg) <!--- MC-41721--> Os filtros de usuário da empresa, como Mostrar todos os usuários, Mostrar usuários ativos e Mostrar usuários inativos agora funcionam conforme esperado. Anteriormente, filtrar ações na página do usuário da empresa causava um erro de JavaScript.

### Crédito da empresa

![Problema corrigido](../assets/fix.svg) <!--- MC-41551--> Os administradores com contas restritas que incluem apenas privilégios no nível do site agora podem criar uma empresa que usa uma moeda diferente da do site.

![Problema corrigido](../assets/fix.svg) <!--- MC-41523--> O Adobe Commerce agora envia emails da empresa do site correto `from` endereço de email e escopo. Anteriormente, a Adobe Commerce não considerava o escopo do site ao enviar a atribuição de crédito da empresa ou atualizar o email.

### Pedido rápido

![Problema corrigido](../assets/fix.svg) <!--- MC-42104--> A criação de um pedido usando o Pedido rápido a partir de um arquivo CSV agora funciona conforme esperado com SKUs inexistentes.

![Problema corrigido](../assets/fix.svg) <!--- MC-40268--> O uso do Pedido rápido para pesquisar em vários SKUs agora funciona conforme esperado. Anteriormente, os resultados incluíam entradas duplicadas.

![Problema corrigido](../assets/fix.svg) <!--- MC-40261--> A exibição da lista de Produtos adicionados agora trata SKUs inseridas em minúsculas e maiúsculas da mesma forma quando você usa SKUs para selecionar vários produtos durante o Pedido rápido.

![Problema corrigido](../assets/fix.svg) <!--- MC-40225--> O uso do Pedido rápido agora adiciona produtos na quantidade especificada pelo comprador. Anteriormente, a Adobe Commerce adicionava um produto somente quando as quantidades especificadas pelo comprador excediam um.

![Problema corrigido](../assets/fix.svg) <!--- MC-41283--> O recurso de preenchimento automático Pedido rápido agora funciona com SKUs parciais.

![Problema corrigido](../assets/fix.svg) <!--- MC-41299--> O Adobe Commerce agora exibe produtos que foram configurados como **Não visível individualmente** na lista de sugestão automática e nos resultados da pesquisa da página Ordem rápida.

![Problema corrigido](../assets/fix.svg) <!--- MC-42402--> Os compradores agora podem usar o formulário Pedido rápido para adicionar vários produtos por SKUs que incluem caracteres em maiúsculas. Anteriormente, somente o primeiro produto era adicionado.

### Cotação negociável

![Problema corrigido](../assets/fix.svg) <!--- MC-41232--> Os compradores agora são redirecionados para a página de cotação negociável depois de colar o link para uma cotação negociável no campo URL e fazer logon com êxito. Anteriormente, os compradores eram redirecionados para a página Minha conta.

![Problema corrigido](../assets/fix.svg) <!--- MC-39317--> A reorganização agora funciona conforme esperado para pedidos que contêm um produto com uma Opção de data personalizável para uma conta de cliente que foi criada durante a finalização da compra. Anteriormente, o Adobe Commerce não processava a reordenação e exibia este erro: `The product has required options. Enter the options and try again`.

![Problema corrigido](../assets/fix.svg) <!--- MC-39063--> O endereço de entrega de uma cotação negociável não pode mais ser editado durante o check-out quando o módulo Ordem de Compra estiver desabilitado. Esse comportamento resultou de uma correção anterior na qual `isQuoteAddressLocked` foi removido do renderizador de check-out de cotação negociável.

![Problema corrigido](../assets/fix.svg) <!--- MC-38967--> Os comerciantes agora podem adicionar produtos a uma cotação negociável do Administrador.

### Ordens de compra

![Problema corrigido](../assets/fix.svg) <!--- MC-39983--> O Adobe Commerce agora exibe uma mensagem de erro informativa, conforme esperado, quando você faz uma ordem de compra usando a Finalização expressa do PayPal quando o **[!UICONTROL Name Prefix]** atributo está definido como `required`. Anteriormente, o Adobe Commerce não colocava o pedido nem exibia uma mensagem de erro.

![Problema corrigido](../assets/fix.svg) <!--- MC-39620--> O componente da interface do usuário para o endereço de faturamento no módulo Ordem de compra agora usa o endereço de cotação corretamente quando o Google Tag Manager está ativado. Anteriormente, ocorria um erro de JavaScript na página de pagamento.

### Listas de requisições

![Problema corrigido](../assets/fix.svg) <!--- MC-40426--> Os comerciantes agora podem usar o POST `rest/all/V1/requisition_lists` ponto final para criar uma lista de requisições para um cliente. Anteriormente, o Adobe Commerce exibia este erro 400 quando você tentava criar uma lista de requisições: `Could not save Requisition List`.

![Problema corrigido](../assets/fix.svg) <!--- MC-41123--> A variável **[!UICONTROL Add to Requisition List]** O botão agora é exibido para produtos em estoque de um carrinho de compras quando o carrinho também contém produtos indisponíveis. Anteriormente, se um carrinho continha dois produtos, um deles estava indisponível, a variável _[!UICONTROL Add to Requisition List]_não foi exibido para nenhum dos produtos.

![Problema corrigido](../assets/fix.svg) <!--- MC-40877--> Agora você pode usar a REST API para adicionar um produto a uma lista de requisições.

![Problema corrigido](../assets/fix.svg) <!--- MC-40155--> Lista de requisições **[!UICONTROL Latest Activity Date]** Os valores de agora seguem o formato local.

![Problema corrigido](../assets/fix.svg) <!--- MC-39580--> O Adobe Commerce não lança mais um erro fatal quando você edita um pacote de produtos de uma lista de requisições.

![Problema corrigido](../assets/fix.svg) <!--- MC-40454--> O Adobe Commerce agora exibe o preço correto do produto quando você adiciona um produto com uma opção personalizável `(File)` para uma lista de desejos a partir de uma lista de requisições. O link para o arquivo carregado também está visível, conforme esperado. Anteriormente, o Adobe Commerce exibia preços de produtos incorretos e não exibia o link para o arquivo.

![Problema corrigido](../assets/fix.svg) <!--- MC-36383--> Produtos com uma opção personalizada `(File)` agora pode ser adicionado a um carrinho de compras a partir de uma lista de requisições.

### Catálogo compartilhado

![Problema corrigido](../assets/fix.svg) <!--- MC-40497--> Um administrador com uma função limitada a um site específico agora pode criar, exibir e editar um catálogo compartilhado. Anteriormente, o Adobe Commerce emitia um erro fatal quando um administrador com uma função limitada tentava criar um catálogo compartilhado.

![Problema corrigido](../assets/fix.svg) <!--- MC-41337--> Os resultados da navegação em camadas agora incluem uma contagem precisa de produtos com atributos filtrados, e os compradores agora podem aplicar vários filtros. Anteriormente, somente um filtro podia ser aplicado, e o Adobe Commerce exibia uma contagem de produtos imprecisa na navegação em camadas.

![Problema corrigido](../assets/fix.svg) <!--- MC-40779--> O Adobe Commerce agora exibe corretamente as contagens de produtos em filtros de navegação em camadas nos resultados da pesquisa. Anteriormente, um plug-in para a página Resultados da pesquisa não usava o Elasticsearch, mas emitia uma nova consulta ao banco de dados.

![Problema corrigido](../assets/fix.svg) <!--- MC-39978--> O Adobe Commerce não exclui mais os preços de camada quando um comerciante exclui todos os produtos de um catálogo compartilhado padrão.

![Problema corrigido](../assets/fix.svg) <!--- MC-39802--> Agora os filtros são filtrados pela categoria atual e exibidos corretamente em todas as páginas quando os catálogos compartilhados estão ativados. Anteriormente, os filtros eram calculados incorretamente somente para a página atual e não eram filtrados pela categoria atual.

![Problema corrigido](../assets/fix.svg) <!--- MC-39522--> O GRAPHQL `products` a consulta não retorna mais o intervalo de preços e a categoria de um produto para produtos que não estão atribuídos a um catálogo compartilhado quando o catálogo compartilhado está habilitado. Anteriormente, a consulta retornava as agregações do produto, mesmo que o produto em si não fosse retornado na variável `items` matriz.

## B2B v1.3.1

*9 de fevereiro de 2021*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Adição de suporte para o Adobe Commerce 2.4.2.

![Novo](../assets/new.svg) Os métodos de pagamento online agora são compatíveis com ordens de compra.

![Problema corrigido](../assets/fix.svg) Adicionar um produto configurável ao carrinho diretamente de uma lista de requisições quando esse produto era usado em um pedido anterior não retornava mais um erro do sistema.

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe a guia Requer minha aprovação corretamente para ordens de compra quando uma configuração de banco de dados dividido é implantada.

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe detalhes sobre pacotes de produtos e cartões-presente quando você exibe pedidos de compra.

![Problema corrigido](../assets/fix.svg) Os compradores agora são redirecionados como esperado depois de fazer logon em sua conta enquanto navegam em uma loja onde **[!UICONTROL Website Restriction]** está ativado e **[!UICONTROL Restriction Mode]** está definida como `Private Sales: Login Only`. Anteriormente, os compradores eram redirecionados para a página inicial da loja. <!--- MC-38934-->

![Problema corrigido](../assets/fix.svg) O histórico de pedidos agora é carregado conforme esperado na página do painel de conta de um administrador de empresa em implantações com uma hierarquia de empresa B2B que contém muitos clientes (maior que 13000). Anteriormente, o histórico do pedido era carregado lentamente ou não era carregado, e o Adobe Commerce exibia um erro 503. <!--- MC-38830-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais várias mensagens de advertência idênticas quando você adiciona um produto não configurado com opções personalizáveis a uma Lista de Requisições a partir de uma página Categoria. <!--- MC-38342-->

![Problema corrigido](../assets/fix.svg) Os produtos novos e duplicados agora ficam visíveis conforme esperado na página de categoria quando os catálogos compartilhados B2B são ativados. <!--- MC-38307-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora mantém a `store_id` que é associado a um administrador de empresa quando o grupo de clientes de uma empresa é atualizado. Anteriormente, a variável `store_id` alterado para o armazenamento padrão quando o grupo foi atualizado. <!--- MC-38196-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora salva um produto agrupado em uma lista de requisições como uma lista de produtos simples da mesma forma que adiciona um produto agrupado a um carrinho de compras. Anteriormente, devido à forma como o Adobe Commerce salvava os produtos agrupados, o link de um produto agrupado da lista de requisições sempre era redirecionado para produtos simples e não para o produto agrupado. <!--- MC-38049-->

![Problema corrigido](../assets/fix.svg) Agora você pode filtrar pedidos por **[!UICONTROL Company Name]** ao exportar informações do pedido no formato CSV. Anteriormente, o Adobe Commerce registrava um erro no `var/export/{file-id}`. <!--- MC-37785-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe o pop-up Criar lista de requisições conforme esperado quando você seleciona a guia Criar nova lista de requisições na loja. <!--- MC-37915-->

![Problema corrigido](../assets/fix.svg) As listas de requisições agora incluem todos os produtos agrupados e quantidades que foram adicionadas à lista. Anteriormente, quando um comerciante navegava para uma lista de requisições depois de adicionar produtos a ela a partir de uma página de detalhes do produto, o Adobe Commerce exibia este erro: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Problema corrigido](../assets/fix.svg) A exibição de loja correta agora está associada ao site relevante quando você cria uma empresa em uma implantação multissite. Anteriormente, não era possível criar uma empresa, e o Adobe Commerce exibia este erro: `The store view is not in the associated website`. <!--- MC-37488-->

![Problema corrigido](../assets/fix.svg) A solicitação de produtos por SKU usando o Quick Order não resulta mais em quantidades de produtos duplicadas no arquivo CSV. <!--- MC-37427-->

![Problema corrigido](../assets/fix.svg) A variável **[!UICONTROL Add to Cart]** O botão não está mais bloqueado quando a variável _[!UICONTROL Enter Multiple SKUs]_seção da página Pedido rápido contém um valor vazio. Em vez disso, o Adobe Commerce agora exibe uma mensagem solicitando que você insira SKUs válidas. <!--- MC-37387-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe esta mensagem na página do produto quando você submete uma revisão do produto a partir de uma lista de requisições: `You submitted your review for moderation`. A revisão também aparece na página Revisões pendentes (Administrador **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Anteriormente, embora a Adobe Commerce tenha adicionado a revisão à lista de revisões pendentes, ela apresentou um erro 404 na página do produto. <!--- MC-37119-->

![Problema corrigido](../assets/fix.svg) O desempenho do `sharedCatalogUpdateCategoryPermissions` consumidor foi melhorada. Depois de criar um catálogo compartilhado, o indexador de permissões do catálogo agora usa somente a ID do grupo de clientes do catálogo compartilhado, não todos os grupos de clientes. <!--- MC-36770-->

![Problema corrigido](../assets/fix.svg) Os campos de atributo do endereço do cliente personalizado associados ao endereço não padrão de um comprador agora são salvos conforme esperado no fluxo de trabalho de check-out da loja. <!--- MC-36630-->

![Problema corrigido](../assets/fix.svg) Os pedidos de produtos que pertencem ao catálogo compartilhado padrão de uma loja agora podem ser feitos para compradores por meio da API REST de administrador (`rest/V1/carts/{<CART_ID>/items`) conforme esperado. O Adobe Commerce agora verifica se o produto foi atribuído a um catálogo público antes da validação de permissões do catálogo compartilhado em `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Anteriormente, o Adobe Commerce não adicionava o produto ao carrinho do comprador e exibia o seguinte erro: `No such shared catalog entity`. <!--- MC-36535-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora envia emails de registro de usuário da nova empresa do endereço da loja da Adobe Commerce. Anteriormente, esse email era enviado do endereço do administrador da empresa. <!--- MC-36480-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora verifica os atributos personalizados quanto à duplicação de nomes de atributos de empresa reservados antes de permitir que um comerciante salve um novo atributo. <!--- MC-36282-->

![Problema corrigido](../assets/fix.svg) A variável `credit_history` a consulta agora retorna o histórico de crédito da empresa especificada para o valor alocado originalmente e o valor comprado. Anteriormente, essa consulta retornava um erro.

![Problema corrigido](../assets/fix.svg) A variável **[!UICONTROL Company]** e  **[!UICONTROL Job Title]** os campos na página Editar informações da conta não são mais editáveis.

### Problemas conhecidos

- Compradores B2B podem usar métodos de pagamento on-line para ignorar o fluxo normal da ordem de compra. Esse cenário pode ocorrer se o comprador puder reduzir todo o total do check-out para 0 — por exemplo, por um código promocional ou cartão-presente — e depois remover o código ou o cartão-presente. Mesmo nessas condições, a Adobe Commerce ainda faz o pedido com a quantia correta com base nos preços dos itens em seu catálogo atribuído. **_Solução alternativa_**: Desabilitar cartões-presente e códigos de cupom quando os métodos de pagamento online estiverem habilitados para aprovação de ordem de compra. <!--- B2B-1603-->

- Os compradores são redirecionados para o carrinho de compras ao tentar fazer um pedido a partir de uma ordem de compra usando o Check-out expresso do PayPal quando **[!UICONTROL In-Context Mode]** está desativado. <!--- B2B-1604-->

- O Adobe Commerce às vezes exibe um erro 404 quando um comprador cria uma ordem de compra e, em seguida, navega até a página de finalização. Esse erro ocorre quando um comprador criou anteriormente uma ordem de compra diferente com um método de pagamento online antes de navegar até a página de finalização sem concluir a compra anterior. O comprador ainda pode colocar a ordem de compra. **_Solução alternativa_**: nenhuma. <!--- B2B-1605-->

- Os descontos para um método de pagamento específico persistem durante o check-out de uma ordem de compra mesmo quando o comprador altera seu método de pagamento durante o check-out final. Como resultado, os clientes podem receber um desconto ao qual não têm direito. Esse problema ocorre porque uma regra de carrinho para o método de pagamento original ainda é aplicada apesar da alteração no método de pagamento. **_Solução alternativa_**: nenhuma. Consulte a [Problema conhecido B2B do Adobe Commerce 2.4.2: o desconto permanece para Ordens de compra online após o método de pagamento ser alterado](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Knowledge base_ artigo. <!-- B2B-1012 -->

- A variável `deleteRequisitionListOutput` a consulta retorna detalhes sobre a lista de requisições deletadas em vez das listas de requisições remanescentes. <!--- MC-39894-->

## B2B v1.3.0

*15 de outubro de 2020*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

Esta versão inclui melhorias nas aprovações de pedidos, métodos de envio, carrinho de compras e registro de ações de administrador.

![Novo](../assets/new.svg) Adição de suporte para o Adobe Commerce 2.4.1.

![Novo](../assets/new.svg) As aprovações de pedidos B2B foram aprimoradas para melhorar a usabilidade e permitir ações em massa em ordens de compra.

![Novo](../assets/new.svg) Os comerciantes B2B agora podem controlar métodos de envio que são oferecidos a cada Empresa.<!--- BUNDLE-160 161 162 -->

![Novo](../assets/new.svg) Os comerciantes agora podem permitir que os usuários limpem o conteúdo de seu carrinho de compras em uma única ação e podem configurar essa capacidade de forma independente em cada site <!--- BUNDLE-108 -->

![Novo](../assets/new.svg) Compradores B2B agora podem adicionar itens individuais ou todo o conteúdo de seu carrinho de compras diretamente a uma lista de requisições. <!--- BUNDLE-145 144-->

![Novo](../assets/new.svg) Os comerciantes B2B podem criar ordens do Administrador em nome dos clientes usando Pagamento por conta como o método de pagamento. <!--- BUNDLE-166 178-->

![Novo](../assets/new.svg) Agora os comerciantes podem exibir diretamente todas as cotações associadas a um usuário na página de detalhes do cliente. <!--- BUNDLE-139 -->

![Novo](../assets/new.svg) Os comerciantes agora podem filtrar a grade Clientes agora online por Empresa. <!--- BUNDLE-137 -->

![Novo](../assets/new.svg) Agora, administradores podem filtrar clientes no Administrador por Representante de vendas. <!--- BUNDLE-110 -->

![Novo](../assets/new.svg) Para reduzir a criação de contas fraudulentas ou de spam, os comerciantes agora podem habilitar o Google reCAPTCHA no formulário Solicitação de nova empresa na loja. <!--- BUNDLE-154 -->

![Novo](../assets/new.svg) As ações do administrador tomadas nos módulos da Empresa agora são registradas no Log de ações do administrador. As ações são registradas de todos os módulos de empresa relevantes: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais o **[!UICONTROL Delete customer]** botão no **Clientes** quando o administrador conectado não tiver direitos para excluir clientes em implantações em que o B2B estiver instalado. <!--- MC-35655-->

![Problema corrigido](../assets/fix.svg) O grupo de clientes não é mais alterado automaticamente para um cliente atribuído a uma Empresa quando você edita o cliente na grade Cliente. <!--- MC-35254-->

![Problema corrigido](../assets/fix.svg) Quando um comerciante cria um catálogo compartilhado, as permissões agora são automaticamente definidas como `Allow` para o **[!UICONTROL Display Product Prices]** e **[!UICONTROL Add to Cart]** recursos em categorias quando esse acesso é atribuído ao grupo de clientes nas configurações de permissão do catálogo. Anteriormente, essas configurações eram definidas automaticamente como `Deny` mesmo quando as permissões do catálogo estavam definidas como `Allow`.<!--- MC-34792-->

![Problema corrigido](../assets/fix.svg) As permissões de categoria de catálogo compartilhado não são mais substituídas quando um produto é editado na página de edição do produto.<!--- MC-34777-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora envia uma notificação por email confirmando que um cliente tem permissão para exceder o limite de crédito designado quando um comerciante permite a **[!UICONTROL Allow To Exceed Credit Limit]** configuração. Anteriormente, o email de notificação enviado pela Adobe Commerce indicava que o cliente não tinha permissão para exceder o limite. <!--- MC-34584-->

![Problema corrigido](../assets/fix.svg) O contêiner HTML que circunda o preço do produto nas listas de requisição agora é renderizado corretamente para os filhos dos produtos agrupados. <!--- MC-36331-->

![Problema corrigido](../assets/fix.svg) Os comerciantes agora podem designar o idioma em que o email do usuário da empresa é enviado ao criar uma empresa em implantações de vários idiomas. Anteriormente, o menu suspenso permitia que os comerciantes selecionassem a exibição de loja e o idioma apropriados não eram exibidos.  <!--- MC-35777-->

![Problema corrigido](../assets/fix.svg) Os campos personalizados de atributos de endereço do cliente agora são exibidos conforme esperado no fluxo de trabalho de finalização da loja. <!--- MC-35607-->

![Problema corrigido](../assets/fix.svg) A guia Configuração de recursos B2B agora é aberta corretamente. <!--- MC-35458-->Os convidados agora podem usar o QuickOrder para adicionar produtos ao carrinho e, em seguida, remover itens com êxito. Anteriormente, quando um comprador usava o QuickOrder para adicionar vários produtos ao carrinho e, em seguida, removia um produto, o produto não era removido. <!--- MC-35327-->

![Problema corrigido](../assets/fix.svg) Uma empresa agora pode ser atualizada usando o PUT da API REST `/V1/company/:companyId` solicitação sem especificar o `region_id` quando o estado é configurado como **não obrigatório**. Anteriormente, mesmo que `region_id` não era necessário, o Adobe Commerce emitiu um erro se não tivesse sido especificado. <!--- MC-35304-->

![Problema corrigido](../assets/fix.svg) Ao criar ou atualizar uma Empresa B2B usando a API REST (`http://magento.local/rest/V1/company/2`, onde `2` representa a ID da empresa), a resposta agora inclui as configurações para `applicable_payment_method` ou `available_payment_methods` conforme esperado. <!--- MC-35248-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais uma página 404 quando um comerciante usa o **Enter** em vez de clicar no botão **[!UICONTROL Save]** botão ao criar uma lista de requisições na loja.<!--- MC-35094-->

![Problema corrigido](../assets/fix.svg) As permissões de categoria não são mais alteradas quando um novo produto é atribuído a um catálogo público compartilhado. Anteriormente, as permissões de categoria eram duplicadas. <!--- MC-34386-->

![Problema corrigido](../assets/fix.svg) O PUT do ponto de acesso da REST API `rest/default/V1/company/{id}`, que é usado para atualizar o email da Empresa, não diferencia mais maiúsculas de minúsculas. <!--- MC-34308-->

![Problema corrigido](../assets/fix.svg) A desativação dos módulos de recompensa não afeta mais os recursos B2B nas contas do cliente. Anteriormente, quando os módulos de recompensa eram desativados, as seguintes guias relacionadas a B2B não eram exibidas: Perfil da empresa, Usuários da empresa e Funções e permissões.<!--- MC-34191-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora usa o nome correto do remetente nas notificações por email quando alterações são feitas em contas da empresa. Anteriormente, o Adobe Commerce usava o nome geral do remetente do contato definido no escopo padrão para todos os emails. <!--- MC-33917-->

![Problema corrigido](../assets/fix.svg) Agora é possível implementar com êxito o envio múltiplo de pedidos que contêm produtos físicos e virtuais. <!--- MC-33818-->

![Problema corrigido](../assets/fix.svg) Os comerciantes agora podem criar usuários da empresa a partir do _[!UICONTROL Company Users]_seção nas páginas Minha conta e Estrutura da empresa quando **[!UICONTROL Access Restriction]**está ativado e **[!UICONTROL Restriction Mode]**está definida como `Sales: Login Only`. Anteriormente, o Adobe Commerce exibia este erro quando um comerciante tentava criar um usuário: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Problema corrigido](../assets/fix.svg) A Adobe Commerce não redefine mais o grupo de clientes de um cliente para o padrão quando um cliente salva suas informações de conta. <!--- MC-33554-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não lança mais um erro fatal quando um administrador atribui um cliente que tem um carrinho de compras ativo a um grupo de clientes. <!--- MC-33313-->

![Problema corrigido](../assets/fix.svg) A Adobe Commerce agora fornece uma `addToCart` Evento DataLayer para pedidos rápidos e páginas de listas de Requisição.  <!--- MC-33295-->

![Problema corrigido](../assets/fix.svg) Os emails de notificação enviados aos representantes de vendas atribuídos a uma empresa agora incluem o logotipo corporativo atribuído. Anteriormente, o email de notificação incluía o logotipo padrão da LUMA, não o logotipo corporativo carregado. <!--- MC-33232-->

![Problema corrigido](../assets/fix.svg) Uma lista de requisições agora inclui todos os produtos agrupados e as quantidades que foram adicionadas à lista. Anteriormente, quando um comerciante navegava para uma lista de requisições depois de adicionar produtos a ela a partir de uma página de detalhes do produto, o Adobe Commerce exibia este erro: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problema corrigido](../assets/fix.svg) A variável `products` a consulta agora retorna uma `total_count` quando o catálogo compartilhado está ativado. <!--- MC-42268-->

![Problema corrigido](../assets/fix.svg) As páginas Configuração da empresa e Criar empresa agora funcionam como esperado depois de desativar um método de envio online. A verificação foi adicionada para impedir a tentativa de processamento de módulos de envio desabilitados. Anteriormente, o Adobe Commerce exibia este erro: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Problema corrigido](../assets/fix.svg) O consumo de memória de teste de integração foi reduzido, o que melhora o desempenho do teste e reduz o tempo necessário para a conclusão do teste. <!--- AC-266-->

## B2B v1.2.0

*28 de julho de 2020*

[!BADGE Compatível]{type=Informative tooltip="Compatível"}

![Novo](../assets/new.svg) Adição de suporte para o Adobe Commerce 2.4.0.

![Novo](../assets/new.svg) Storefront Order Search, com agradecimento pela contribuição de Marek Mularczyk do [Divante](https://www.divante.com/) e membros da comunidade.

![Novo](../assets/new.svg) As Ordens de Compra são aprimoradas e regravadas. Agora elas são incluídas por padrão no Adobe Commerce.

![Novo](../assets/new.svg) As Regras de Aprovação de Ordem de Compra foram implementadas. Essas regras permitem que os usuários controlem o workflow Ordem de Compra criando regras de compra para ordens.

![Novo](../assets/new.svg) Agora, o logon como cliente está incluído por padrão no Adobe Commerce. Esse recurso permite que os funcionários do site ajudem os clientes fazendo logon como cliente para ver o que veem.

![Problema corrigido](../assets/fix.svg) As agregações de atributo agora estão funcionando corretamente para a Navegação em camadas com o Elasticsearch

![Problema corrigido](../assets/fix.svg) A pesquisa de pedidos por caracteres especiais agora está funcionando corretamente.

![Problema corrigido](../assets/fix.svg) Clicar no **[!UICONTROL Clear All]** Agora, o botão expande todos os filtros, em vez de recolhê-los.

![Problema corrigido](../assets/fix.svg) O SKU/nome do produto agora está incluído no resumo do filtro de pesquisa do Histórico de pedidos.

![Problema corrigido](../assets/fix.svg) O Indicador de Classificação agora é exibido corretamente na Grade Minhas Ordens de Compra.

![Problema corrigido](../assets/fix.svg) Agora, você pode clicar nos botões Aprovar, Cancelar, Rejeitar e Ordem de compra apenas uma vez. Anteriormente, você podia clicar no botão várias vezes.

![Problema corrigido](../assets/fix.svg) Os botões Aprovar, Rejeitar, Cancelar e Validar da ordem de compra agora são renderizados corretamente em dispositivos móveis.

![Problema corrigido](../assets/fix.svg) Anteriormente, a aprovação de uma Ordem de compra com um desconto que expirou colocava a ordem no valor total e não atualizava o total da Ordem de compra. Agora, o total da ordem de compra é atualizado para mostrar o total correto.

![Problema corrigido](../assets/fix.svg) Na versão 2.3.4, foi introduzido um problema em que os atributos de extensão personalizados não eram copiados do Endereço do cliente para o Endereço da cotação. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Com o B2B instalado, um erro SQL seria exibido ao atribuir categorias a catálogos compartilhados. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Devido a um valor de tipo de variável incorreto, os administradores não puderam adicionar produtos configuráveis a um pedido. Os menus suspensos de opção não eram preenchidos. Esse recurso agora funciona corretamente.

![Problema corrigido](../assets/fix.svg) Anteriormente, ao editar permissões de categoria para o grupo Não conectado, ocorria um erro ao salvar as alterações. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Uma correção foi adicionada para permitir que os administradores de loja adicionem produtos a um pedido que não está no catálogo compartilhado. Anteriormente, uma mensagem de erro era exibida ao adicionar um item que não estava no catálogo.

![Problema corrigido](../assets/fix.svg) Anteriormente, após executar o comando `php bin/magento indexer:set-dimensions-mode catalog_product_price website` e, em seguida, tentar criar um catálogo compartilhado, ocorreria um erro. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Ao adicionar uma empresa e atribuir o administrador de empresa a um site não padrão, a ID de site incorreta foi enviada, causando um erro. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Anteriormente, depois que um cliente era movido para outro grupo de clientes, adicionar um produto a um pedido usando _Pedido rápido_ falhará com um erro. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Anteriormente, ao tentar fazer check-out usando a WebAPI com uma cotação B2B, um valor incorreto era enviado para a API, causando a ocorrência de um erro. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Anteriormente, ao configurar uma empresa para &quot;Ativa&quot; por meio da API, ocorria um erro. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Devido a um erro desnecessário `form` , a página do pedido será atualizada automaticamente quando você pressionar Enter após alterar um encargo de remessa proposto. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Anteriormente, ao definir um limite de exibição de produto em uma página de catálogo e esse limite era menor que o número total de produtos, ocorria um erro. Esse recurso agora funciona conforme esperado.

![Problema corrigido](../assets/fix.svg) Anteriormente, ao alterar o administrador de uma empresa, o endereço do administrador original era copiado para o novo administrador, fornecendo dois endereços. Agora, somente o endereço correto é adicionado.

![Problema corrigido](../assets/fix.svg) Anteriormente, o uso da API para salvar um item de cotação quando o Git estava definido como &quot;Permitido e notificar o cliente&quot; falhava. Essa chamada de API agora funciona conforme esperado.

![Problema corrigido](../assets/fix.svg) O Imposto Fixo do Produto agora é exibido na página de detalhes Cotações.

![Problema corrigido](../assets/fix.svg) Anteriormente, clicar em um anexo na guia Comentários da página Minhas cotações não baixava o arquivo. Esse comportamento agora funciona conforme esperado.

### Problemas conhecidos

- O Adobe Commerce lança uma exceção durante a atualização para B2B 1.2.0 em uma implantação de vários sites. Quando `setup:upgrade` for executado, esse erro ocorrerá no `PurchaseOrder` módulo: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Solução alternativa**: Instale o `B2B-716 Add NonTransactionableInterface` à interface `InitPurchaseOrderSalesSequence` correção de dados, que agora está disponível no **Minha conta** > **Downloads** seção de `magento.com`.
- Se um código de desconto expirar antes de uma Ordem de Compra (OC) ser aprovada, a OC continuará a exibir o valor descontado, mas uma vez aprovada a OC, a ordem será colocada no total não descontado. **Solução alternativa**: Instale o `B2B-709 Purchase Order Discount patch` correção para esse problema, que agora está disponível no **Minha conta** > **Downloads** seção de `magento.com`.
- Se os itens em uma ordem de compra estiverem esgotados ou em quantidade insuficiente quando a ordem de compra for convertida em uma ordem real, ocorrerá um erro. Se as ordens pendentes estiverem ativadas, a ordem será processada normalmente.
