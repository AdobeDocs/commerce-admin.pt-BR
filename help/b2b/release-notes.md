---
title: Notas de versão do [!DNL Adobe Commerce B2B]
description: Revise as notas de versão para obter informações sobre as alterações nas versões  [!DNL Adobe Commerce B2B] .
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 298dae1e7ff3ec2af42d70a255075877458eeb4f
workflow-type: tm+mt
source-wordcount: '9030'
ht-degree: 0%

---

# Notas de versão do [!DNL Adobe Commerce B2B]

Essas notas de versão para a extensão B2B capturam adições e correções que o Adobe adicionou durante um ciclo de versão, incluindo:

![Novos](../assets/new.svg) Novos recursos
![Problema corrigido](../assets/fix.svg) Correções e melhorias
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

>[!NOTE]
>
>Consulte [Disponibilidade do produto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html?lang=pt-BR) para obter informações sobre versões da extensão B2B do Commerce com suporte para versões disponíveis do Adobe Commerce.

## B2B v1.5.3-alpha2

*12 de agosto de 2025*

Compatível com o Adobe Commerce versão 2.4.9-alpha2

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.5.2-p2

*12 de agosto de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.8-p2, 2.4.7-p7 e 2.4.6-p12.
Compatível com as versões 2.4.7 a 2.4.7-p6 do Adobe Commerce, 2.4.6 a 2.4.6-p11.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.5.2-p1

*10 de junho de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.8-p1, 2.4.7-p6 e 2.4.6-p11.
Compatível com as versões 2.4.7 a 2.4.7-p5 do Adobe Commerce, 2.4.6 a 2.4.6-p10

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-50](https://helpx.adobe.com/br/security/products/magento/apsb25-50.html).

## B2B 1.5.2

*8 de abril, 2025*

[!BADGE Compatível]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.8, 2.4.7-p5 e 2.4.6-p10.
Compatível com as versões 2.4.7 a 2.4.7-p4, 2.4.6 a 2.4.6-p9 do Adobe Commerce

A versão B2B v1.5.2 inclui melhorias de qualidade e correções de erros.

### Gerenciamento da empresa

![Novos](../assets/new.svg)<!-- B2B-4123 -->Os administradores agora podem gerenciar várias empresas de uma única conta usando o alternador de empresa de vitrine. Os principais benefícios incluem:

- **Gerenciamento simplificado de várias empresas**—Os administradores agora podem supervisionar várias empresas de uma conta de usuário, eliminando a necessidade de criar e gerenciar logons separados para cada empresa.
- **Alternância eficiente da empresa** — Uma interface intuitiva permite que os administradores alternem rapidamente entre empresas e façam atualizações, melhorando a produtividade ao gerenciar várias entidades.
- **Operações simplificadas** — gerentes regionais e líderes empresariais podem gerenciar centralmente todas as suas empresas, permitindo tomadas de decisão mais rápidas e operações de negócios mais tranquilas.

Esse aprimoramento se baseia no recurso de associação de várias empresas do B2B 1.5.0, que permitia que os usuários pertencessem a várias empresas, mas não oferecia acesso de administrador entre empresas. O alternador da empresa elimina a necessidade de contas de administrador separadas, mantendo controles de acesso adequados e visualizações específicas da empresa.

### Empresa

![Correção de um problema](../assets/fix.svg)<!-- B2B-4480 --> em que os clientes convidados viam uma mensagem de erro `No such entity with cartId = ?` ao fazer logon como um usuário da empresa com produtos em seus carrinhos de compras.

### Cotação negociável

![Problema corrigido](../assets/fix.svg) A versão B2B v1.5.2 inclui as seguintes correções para cotações negociáveis:

- &#x200B;<!-- B2B-3252 -->O campo [!UICONTROL Line Item Discount Amount] agora valida a entrada para evitar a inserção de valores de desconto negativos.
- &#x200B;<!-- B2B-3224 -->Correção de um problema de experiência do usuário em que as notas de item de linha longa eram truncadas e de difícil leitura para clientes B2B.
- &#x200B;<!-- B2B-2865 -->Os clientes B2B agora podem especificar quantidades de produtos usando valores decimais (como 1,5 ou 2,75) ao criar aspas.

### Modelo de cotação

![Novo](../assets/new.svg)<!-- B2B-4104 --> Nova capacidade para compradores e vendedores B2B de anexar links de documentos externos a modelos de cotação. Esse recurso permite vincular a documentos hospedados em serviços como o DocuSign e o Adobe Sign diretamente de aspas, complementando o recurso de anexo de arquivo existente. Os principais benefícios incluem:

- Colaboração simplificada por meio do acesso direto a contratos e contratos essenciais
- Maior transparência com acesso instantâneo à documentação mais recente
- Negociações de cotação mais rápidas, eliminando a necessidade de baixar e fazer upload de arquivos
- Gerenciamento flexível de documentos usando serviços externos de hospedagem de documentos

## B2B 1.5.1

*11 de fevereiro de 2025*

[!BADGE Compatível]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.7-p4+ e 2.4.6-p9+.
Compatível com o Adobe Commerce versões 2.4.8-beta1 a 2.4.8-beta2, 2.4.7 a 2.4.7-p3, 2.4.6 a 2.4.6-p8

A versão B2B v1.5.1 inclui melhorias de qualidade e correções de erros.

### Empresa

![Correção do problema](../assets/fix.svg)<!-- B2B-4422 --> Se um cliente tentar mudar de empresa na página Detalhes da Cotação, o sistema agora redireciona o cliente para uma página *Acesso Negado* para garantir que uma cotação criada para uma empresa não possa ser usada para fazer um pedido com os preços de outra empresa. Anteriormente, um usuário podia criar uma cotação com o preço de uma empresa e, em seguida, mudar para outra empresa para fazer um pedido com preços diferentes.

### Descontos de item de linha

![Correção do problema](../assets/fix.svg)<!-- B2B-2938 --> Melhoria na eficiência do sistema ao solucionar uma degradação de desempenho observada no cenário de recálculo de cotação. Anteriormente, duas novas entidades eram adicionadas a cada item da linha do carrinho, o que causava um aumento notável nas solicitações do banco de dados, resultando em um desempenho mais lento.

### Cotação negociável

![Problema corrigido](../assets/fix.svg)<!-- B2B-3820 --> O sistema agora mantém a posição dos elementos da interface do usuário quando a validação do JavaScript é aplicada aos campos *[!UICONTROL min/max qty]* na página Modelo de cotação da vitrine da Luma. Anteriormente, aplicar a validação do JavaScript a esses campos fazia com que outros elementos da interface do usuário na página mudassem.

### Carrinho de compras

![Problema corrigido](../assets/fix.svg)<!-- B2B-4222 --> Apresentou um novo sistema de gerenciamento de carrinho de compras projetado para simplificar a experiência de compras para usuários que gerenciam várias contas da empresa. O novo sistema associa carrinhos de compras a empresas individuais em vez da conta do cliente para simplificar a experiência de compras e melhorar o fluxo de trabalho, suportando os seguintes recursos.

- **Carrinhos específicos da empresa:**—Os carrinhos de compras agora estão vinculados a empresas individuais para dar suporte a preços e opções de produto específicos da empresa.
- **Alternância perfeita**—Os usuários podem alternar facilmente entre diferentes contas da empresa sem afetar o conteúdo do carrinho de cada empresa.
- **Integridade contextual** — todos os detalhes do carrinho permanecem no contexto da respectiva empresa, fornecendo uma experiência de compra consistente e confiável.

## B2B 1.5.0

*30 de outubro de 2024*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.7-p3+ e 2.4.6-p8+.
Compatível com o Adobe Commerce versões 2.4.8-beta1, 2.4.7 a 2.4.7-p2, 2.4.6 a 2.4.6-p7.

A versão 1.5.0 do Adobe Commerce B2B também é compatível com o PHP 8.3 e oferece suporte ao [GraphQL Application Server](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/performance-best-practices/concepts/application-server).

A versão B2B v1.5.0 inclui novos recursos, melhorias de qualidade e correções de erros.

>[!NOTE]
>
> Saiba mais sobre as alterações incompatíveis com versões anteriores (BICs) introduzidas na versão B2B 1.5.0 revisando os destaques e as informações de referência no tópico [Alterações incompatíveis com versões anteriores](backward-incompatible-changes.md).

### Gerenciamento da Empresa

![Novo](../assets/new.svg) **Gerenciamento de Empresas**<!--B2B-2901-->—Os comerciantes agora podem exibir e gerenciar empresas da Adobe Commerce como organizações hierárquicas, atribuindo empresas a empresas principais designadas. Depois que uma empresa é atribuída a uma empresa principal, o administrador da empresa principal pode gerenciar a conta da empresa. Somente usuários administradores autorizados podem adicionar e gerenciar atribuições da empresa. Para obter detalhes, consulte [Gerenciar hierarquia da empresa](manage-company-hierarchy.md).

- Adicione e gerencie atribuições de empresa da nova seção *[!UICONTROL Company Hierarchy]* na página *[!UICONTROL Company Account]* do Administrador.

- Classifique e filtre empresas pela nova configuração *[!UICONTROL Company Type]*. Na grade de empresas, a coluna *[!UICONTROL Company Type]* indica se uma empresa é uma empresa individual ou parte da hierarquia organizacional (pai ou filho).

![Novo](../assets/new.svg) **Gerenciar a configuração da empresa na escala**<!--B2B-2849-->—Altere rapidamente as configurações da empresa para empresas selecionadas usando a ação em massa *[!UICONTROL Change company setting]* agora disponível ao gerenciar empresas da grade *[!UICONTROL Companies]* ou *[!UICONTROL Company Hierarchy]*. Por exemplo, se você criar um novo catálogo compartilhado para um grupo de empresas, poderá alterar a configuração do catálogo compartilhado em uma única ação, em vez de editar cada empresa individualmente.

![Novos](../assets/new.svg) Desenvolvedores de API podem usar o novo ponto de extremidade de API REST de Relações da Empresa `/V1/company/{parentId}/relations` para criar, exibir e remover atribuições da empresa. Consulte [Gerenciar objetos da empresa](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) no *Guia do Desenvolvedor da API Web*.

### Contas da empresa

![Novo](../assets/new.svg)<!--B2B-2828--> **Atribuição multiempresa** — Simplifique o acesso à conta da empresa para usuários da empresa atribuindo um usuário a várias empresas. Por exemplo, se você tiver um comprador que faz pedidos de vários locais da empresa, crie uma única conta e atribua todas as empresas com as quais o comprador trabalha a essa conta. Em seguida, o comprador pode fazer logon uma vez e alternar entre as contas da empresa escolhendo a empresa na loja.

>[!NOTE]
>
>Um usuário da empresa pode ser atribuído a várias empresas, mas ele pode ser o administrador da empresa somente para uma empresa.

![Novo](../assets/new.svg) <!--B2B-2747--> **Seletor de escopo da empresa** — Fornece aos usuários da empresa atribuídos a várias empresas a capacidade de alterar empresas na loja. Quando o escopo é alternado, os dados são atualizados para mostrar as informações com base no novo contexto da empresa. Por exemplo, se a nova empresa usar um catálogo compartilhado diferente, o usuário da empresa verá produtos, preços e outras informações com base no novo catálogo compartilhado. O conteúdo relacionado a pedidos, cotações e modelos de cotação também é atualizado com base no contexto da empresa selecionada.

>[!NOTE]
>O conteúdo do carrinho de compras reflete os itens selecionados pelo cliente atual. Se o cliente tiver um carrinho de compras ativo e selecionar uma empresa diferente, será solicitado que ele atualize o carrinho para refletir a variedade do produto, os preços e os descontos promocionais com base no novo contexto da empresa. Os produtos que não estão disponíveis no catálogo associado à nova empresa são removidos do carrinho. Se o produto tiver um preço ou disponibilidade diferente, o carrinho será atualizado para refletir os dados disponíveis no contexto da empresa selecionada.<!--B2B-4222-->

![Problema corrigido](../assets/fix.svg)<!--ACP2E-1933--> Os administradores da empresa agora podem adicionar usuários da empresa pela loja. Anteriormente, o Commerce registrava um erro quando um usuário administrador tentava adicionar um novo usuário: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

### Cotas e Modelos de Cotação

As melhorias nos recursos de cotação ajudam os Compradores e os Vendedores a gerenciar cotações e negociações de cotações com mais eficiência.

![Novo](../assets/new.svg) **Modelos de cotação**—<!--B2B-3367-->Compradores e vendedores agora podem simplificar o processo de cotação criando modelos de cotação reutilizáveis e personalizáveis. Usando modelos de cota, o processo de negociação de cota pode ser concluído uma vez e os compradores podem gerar cotas vinculadas pré-aprovadas para ordens repetitivas em vez de passar pelo processo de negociação de cota para cada ordem. Os modelos de cota estendem a funcionalidade de cota existente adicionando os seguintes recursos avançados:

- **Limites de pedidos** permitem que os vendedores definam compromissos de pedidos mínimos e máximos, garantindo que o comprador siga os volumes de compras acordados.
- **A definição de quantidades mínimas e máximas de ordem de item** oferece ao comprador a flexibilidade de ajustar quantidades de ordem na cotação vinculada sem exigir um novo modelo ou negociação adicional.
- **Rastreie o número de cotações vinculadas geradas e ordens concluídas com êxito** para obter informações sobre o cumprimento de contratos negociados.
- **Cotações vinculadas** são cotações pré-aprovadas que o comprador gera a partir de um modelo de cotação ativo para enviar ordens recorrentes com base nas condições negociadas no modelo de cotação.

![Novo](../assets/new.svg) **melhorias nos recursos de cotação existentes**

- **As regras atualizadas da Lista de Controle de Acesso (ACL) da Commerce** permitem que gerentes e supervisores B2B gerenciem cotações e modelos de cotações de usuários subordinados. Regras separadas oferecem suporte à configuração granular para acesso de visualização, edição e exclusão.

- **Salvar Cotação como Rascunho**<!--B2B-2566-->—Ao criar uma [solicitação de cotação](quote-request.md) do carrinho de compras, os compradores agora podem salvar a cotação como rascunho para que possam revisá-la e atualizá-la antes de iniciar o processo de negociação de cotação com o vendedor. A cotação de rascunho não tem uma data de expiração. Os compradores podem revisar e atualizar cotações de rascunho na seção [!UICONTROL My Quotes] do painel de conta.

- **Renomear Cotação**<!--B2B-2596-->—Os compradores agora podem alterar o nome de uma cotação na página [Detalhes da cotação](account-dashboard-my-quotes.md#quote-actions) selecionando a opção **[!UICONTROL Rename]**. Essa opção está disponível para compradores autorizados ao editar a cotação. Os eventos de alteração de nome são registrados no Log de Histórico de Cotações.

- **Cotação Duplicada**<!--B2B-2701--> — Compradores e vendedores agora podem criar uma nova cotação copiando uma cotação existente. Uma cópia é criada a partir da exibição de detalhes da Cotação selecionando **[!UICONTROL Create Copy]** na [exibição de detalhes da Cotação](quote-price-negotiation.md#button-bar) na Administração ou na [Loja](account-dashboard-my-quotes.md#quote-actions).

- **Mover item de cotação para lista de requisição**<!--B2B-2755-->—Os compradores agora têm a flexibilidade de remover produtos de uma cotação e salvá-los em uma lista de requisições se decidirem não incluí-los no processo de negociação de cota.

- **Remover vários produtos de uma cotação**<!--B2B-2881-->—Em cotações com um grande número de produtos, os compradores agora podem remover vários produtos da cotação selecionando-os e usando a opção *[!UICONTROL Remove]* do controle *[!UICONTROL Actions]* na página Detalhes da cotação. Em versões anteriores, um comprador tinha que excluir um produto de cada vez.

- **Bloqueio de desconto de item de linha**<!--B2B-2597-->—Durante a negociação de cota, os vendedores podem usar o bloqueio de desconto de item de linha para obter mais flexibilidade ao aplicar descontos durante o processo de negociação de cota. Por exemplo, um Vendedor pode aplicar um desconto de item de linha especial a um item e bloquear o item para evitar mais descontos. Quando um item está bloqueado, o preço do item não pode ser atualizado quando um desconto em nível de cotação é aplicado. Consulte [Iniciar cotação para um comprador](sales-rep-initiates-quote.md).

![Problema corrigido](../assets/fix.svg) **Correções para recursos de cotação existentes**

- Os comerciantes que clicam no botão *[!UICONTROL Print]* na exibição de detalhes da Cotação no Administrador agora são solicitados a salvar a cotação como uma PDF. Anteriormente, os comerciantes eram redirecionados para uma página que continha detalhes de cotação. <!--ACP2E-1984-->

- Anteriormente, ao enviar uma cotação de cliente com porcentagem de `0` e alterar a quantidade, o administrador lança uma exceção, mas salva a quantidade. Depois que essa correção for aplicada, para a exceção adequada `0 percentage`, uma mensagem será emitida. <!--ACP2E-1742-->

- Durante a negociação da cotação, um vendedor agora pode especificar um desconto de `0%` no campo Desconto da cotação da cotação negociada e enviar a cotação de volta ao comprador. Anteriormente, se o vendedor tivesse inserido um desconto de 0% e devolvesse a cotação ao comprador, o Administrador retornaria uma mensagem de erro `Exception occurred during quote sending`. <!--ACP2E-1742-->

- A validação do ReCaptcha agora funciona corretamente durante o processo de finalização de uma cotação B2B quando o ReCaptcha V3 é configurado para finalização de loja. Anteriormente, a validação falhava com uma mensagem de erro `recaptcha validation failed, please try again`.  <!--ACP2E-2097-->

### Ordens de Compra

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1825-->Ordens de compra não podem mais ser feitas por um usuário associado à empresa após o bloqueio dela. Anteriormente, um usuário associado à empresa podia fazer pedidos de compra quando a empresa era bloqueada.

## B2B v1.4.2-p7

*12 de agosto de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.7-p7+ e 2.4.6-p12+.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

{{b2b-compatibility}}

## B2B v1.4.2-p6

*10 de junho de 2025*

Versões de patch de segurança [!BADGE com suporte]{type=Informative tooltip="Compatível"} do Adobe Commerce 2.4.7-p6+ e 2.4.6-p11+.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-50](https://helpx.adobe.com/br/security/products/magento/apsb25-50.html).

{{b2b-compatibility}}

## B2B v1.4.2-p5

*8 de abril, 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.7-p5+ e 2.4.6-p10+.

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança do Adobe Commerce 2.4.7-p5+ e 2.4.6-p10+.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-26](https://helpx.adobe.com/br/security/products/magento/apsb25-26.html).

{{b2b-compatibility}}

## B2B v1.4.2-p4

*11 de fevereiro de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.7-p4+ e 2.4.6-p9+.

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança do Adobe Commerce 2.4.7-p4+ e 2.4.6-p9+.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-08](https://helpx.adobe.com/br/security/products/magento/apsb25-08.html).

{{b2b-compatibility}}

## B2B v1.4.2-p3

*8 de outubro de 2024*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.7-p3+ e 2.4.6-p8+.

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança do Adobe Commerce 2.4.7-p3+ e 2.4.6-p8+.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB24-73](https://helpx.adobe.com/br/security/products/magento/apsb24-73.html).

{{b2b-compatibility}}

## B2B v1.4.2-p2

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.7-p2+ e 2.4.6-p7+.

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança do Adobe Commerce 2.4.7-p2+ e 2.4.6-p7+.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no Boletim de segurança xxxx.

{{b2b-compatibility}}

## B2B v1.4.2-p1

*9 de agosto de 2024*

Versões de patch de segurança [!BADGE com suporte]{type=Informative tooltip="Compatível"} do Adobe Commerce 2.4.7-p1+ e 2.4.6-p6+.

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança do Adobe Commerce 2.4.7-p1+ e 2.4.6-p6+.

{{b2b-compatibility}}

## B2B v1.4.2

*10 de outubro de 2023*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} no Adobe Commerce versão 2.4.7 e versão de 2.4.6 para 2.4.6-p5.

A versão B2B v1.4.2 inclui melhorias de qualidade e correções de erros.

![Problema corrigido](../assets/fix.svg) <!--B2B-2897-->Se um Vendedor criar uma cotação de comprador que inclua uma SKU de produto não disponível no catálogo compartilhado associado à empresa compradora, o sistema exibirá a mensagem de erro `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  O Vendedor não pode salvar a cotação até que ele remova o produto que não está disponível. Anteriormente, a cotação era salva com o SKU indisponível incluído e a cotação não era carregada na loja.

>[!IMPORTANT]
>
>O Adobe Commerce B2B versão 1.4.2+ é compatível com o PHP 8.2. Se você atualizar a instância do Commerce para a versão 2.4.7+, certifique-se de que a instância usa o PHP versão 8.2 para manter a compatibilidade com o Adobe Commerce versão B2B. Além disso, o B2B 1.4.2+ atualmente não oferece suporte ao [GraphQL Application Server](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.1

*7 de agosto de 2023*

[!BADGE Com Suporte]{type=Informative tooltip="Compatível"} [Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=pt-BR). Compatível com o Adobe Commerce 2.4.7-beta1.

A versão B2B v1.4.1 inclui melhorias de qualidade e correções de erros.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1825-->Ordens de compra não podem mais ser feitas por um usuário associado à empresa após o bloqueio dela. Anteriormente, um usuário associado à empresa podia fazer pedidos de compra quando a empresa era bloqueada.

![Problema corrigido](../assets/fix.svg) O status de <!--ACP2E-1943-->Produto com backorder agora é exibido corretamente na loja. Anteriormente, os produtos que estavam disponíveis para remessa eram identificados incorretamente como em backorder.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1862-->Se o formulário de registro da empresa incluir um atributo de tipo de arquivo de cliente, o arquivo carregado durante o processo de registro agora será incluído nas informações de conta do Administrador da Empresa após a criação da empresa. Anteriormente, o anexo estava ausente.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1793-->O seletor de amostra de um produto configurável agora é exibido conforme esperado na página de configuração do item de lista de requisições. Anteriormente, o seletor de amostras era exibido como um campo suspenso na página de configuração do item de lista de requisições.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1968-->Ao usar a [consulta de GraphQL da Empresa](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) para retornar detalhes da empresa, os resultados agora são retornados sem erro com êxito.

## B2B v1.4.0

*13 de junho de 2023*

[!BADGE Com Suporte]{type=Informative tooltip="Compatível"} [Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=pt-BR). Compatível com o Adobe Commerce 2.4.7-beta1

Esta versão inclui novos recursos e melhorias para cotações negociáveis B2B e várias correções de erros.

![Novo](../assets/new.svg) Compatibilidade adicionada com o Adobe Commerce 2.4.7-beta1.

![Novo](../assets/new.svg) **Cotações iniciadas pelo vendedor**—Os vendedores agora podem iniciar uma cotação para um comprador diretamente da Cotação e das grades do Cliente no Administrador. Esse recurso simplifica o processo de cotação e reduz a complexidade para os clientes. Se um cliente não tiver iniciado uma ordem, um vendedor poderá criar rapidamente uma cota em nome do cliente e iniciar o processo de negociação. Anteriormente, só era possível criar cotações na loja pelo comprador ou por um vendedor conectado como cliente.

![Novo](../assets/new.svg) **Descontos e negociação de item de linha**—<!--B2B-2440--> Dentro de uma cotação, compradores e vendedores B2B agora podem negociar no nível de item de linha, aplicando descontos e trocando notas até que um contrato seja alcançado. A criação de notas e as atualizações estão incluídas no item da linha e no histórico de cotações para rastrear a comunicação. Anteriormente, compradores e vendedores só podiam trocar notas e aplicar descontos no nível da cotação.

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe os detalhes corretos durante o pagamento quando a opção Ordens de Compra está habilitada e uma cotação virtual que foi criada com a opção de pagamento PayPal foi selecionada. Anteriormente, os totais eram exibidos como zero sob essas condições.

![Correção de um problema](../assets/fix.svg) <!--ACP2E-1504--> Os erros de validação não ocorrem mais quando você tenta salvar uma empresa com um limite de crédito que excede 999. Anteriormente, para limites de crédito de empresa maiores que 999, o Adobe commerce inseriu um separador de vírgula, o que causou um erro de validação que impedia que as atualizações fossem salvas.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1474--> O endereço de entrega selecionado agora permanece inalterado quando você faz um pedido com uma cotação negociável. Anteriormente, quando você fazia um pedido, o endereço de entrega selecionado era alterado para o endereço de entrega padrão.

![Correção de um problema](../assets/fix.svg) <!--ACP2E-1429--> Nas configurações de Armazenamento para Recursos B2B, o campo **[!UICONTROL Enable Shared Catalog direct products price assigning]** agora é desabilitado automaticamente. Na loja, ele fica oculto quando a configuração **[!UICONTROL Enable Company]** ou **[!UICONTROL Enable Shared Catalog]** está definida como **[!UICONTROL No]**.

![Correção de um problema](../assets/fix.svg) <!--ACP2E-1683--> Ao criar uma conta da empresa na loja, a Commerce agora valida o endereço de email antes de processar o registro da empresa. Se o endereço de email for inválido, a operação falhará e nenhuma atualização de conta será processada. Anteriormente, uma conta de cliente era criada mesmo se a solicitação para criar uma conta de empresa falhasse devido a um endereço de email inválido.

![Correção de um problema](../assets/fix.svg) nas SKUs do produto <!--ACP2E-1664--> que incluem aspas duplas no Catálogo Compartilhado e a estrutura de preços não causa mais erros no Administrador.

![Problema corrigido](../assets/fix.svg) <!--ACP2E-1498--> Atualizado a configuração de verniz do aplicativo Commerce para impedir que usuários convidados vejam dados de outros grupos de clientes.

### Problema conhecido

Se você instalar ou atualizar o B2B 1.4.0 no [Adobe Commerce versão 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=pt-BR), ocorrerá o seguinte erro:

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Você pode corrigir esse problema adicionando dependências manuais para o pacote de segurança B2B adicionando dependências manuais para o pacote de segurança B2B com uma [marca de estabilidade](https://getcomposer.org/doc/04-schema.md#package-links). Para obter instruções, consulte a [Base de Dados de Conhecimento Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html?lang=pt-BR).

## B2B v1.3.5-p12

*12 de agosto de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.6-p12+.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.3.5-p10

*8 de abril, 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.6-p10+.

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança 2.4.6-p10 do Adobe Commerce.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-26](https://helpx.adobe.com/br/security/products/magento/apsb25-26.html).

## B2B v1.3.5-p9

*11 de fevereiro de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.6-p9+.

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança do Adobe Commerce 2.4.6-p9.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-08](https://helpx.adobe.com/br/security/products/magento/apsb25-08.html).

## B2B v1.3.5-p8

*8 de outubro de 2024*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.6-p8+.

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança do Adobe Commerce 2.4.6-p8.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB24-73](https://helpx.adobe.com/br/security/products/magento/apsb24-73.html).

## B2B v1.3.5-p7

*9 de agosto de 2024*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} versões de patch de segurança do Adobe Commerce 2.4.6-p7+.

![Novo](../assets/new.svg) Compatibilidade adicionada com as versões de patch de segurança do Adobe Commerce 2.4.6-p7.

## B2B v1.3.5

*14 de março de 2023*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} Adobe Commerce 2.4.0 - 2.4.6 e versões mais recentes

![Novo](../assets/new.svg) Lançado B2B versão 1.3.5-p2 para oferecer suporte à compatibilidade com o Adobe Commerce 2.4.6-p2.

![Novo](../assets/new.svg) Lançado B2B versão 1.3.5-p1 para oferecer compatibilidade com o Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>Depois de atualizar o Commerce da versão 2.4.6 para a [mais recente](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=pt-BR#2.4.6), atualize para a versão de patch B2B 1.3.5 compatível. Ou atualize a extensão B2B da versão 1.3.5 para a versão 1.4.0 ou posterior para obter os recursos mais recentes.

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.6.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-689--> O Adobe Commerce agora exibe os detalhes corretos durante o pagamento quando a opção Ordens de Compra está habilitada e uma cotação virtual criada com a opção Pagamento do PayPal foi selecionada. Anteriormente, os totais eram exibidos como zero sob essas condições.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-609--> A lista de grupos de clientes da configuração **Permitir Navegação da Categoria** não contém mais grupos de clientes que estejam relacionados a catálogos compartilhados.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1244--> O atributo de cliente Número de Imposto/IVA agora funciona conforme esperado com contas de administrador de empresa no Administrador e na loja. Os atributos de Imposto/IVA personalizados não são mais necessários para criar uma conta da empresa. Anteriormente, quando um comerciante criava uma conta da empresa com um atributo personalizado de Imposto/IVA, a Adobe Commerce exibia um erro de validação na vitrine e no Administrador.

![Correção de um problema](../assets/fix.svg) <!--- ACP2E-1236--> Desabilitar o recurso de catálogo compartilhado em um escopo específico agora funciona corretamente. Anteriormente, o Adobe Commerce definia um escopo inválido quando um comerciante salvava a configuração de catálogo compartilhado.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1203--> Os usuários administradores agora podem salvar valores de atributos personalizados de clientes para usuários da empresa. Anteriormente, os atributos personalizados do cliente para usuários da empresa não podiam ser salvos.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1221--> Os problemas de desempenho são resolvidos com a validação das permissões da empresa fornecidas pelo GraphQL quando muitas permissões da empresa já estão atribuídas.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1242--> O Adobe Commerce não lança mais um erro na página do carrinho quando o Pedido rápido é usado para adicionar um produto em uma quantidade que excede o estoque disponível.

![Correção de um problema](../assets/fix.svg) <!--- ACP2E-1090--> O desempenho das operações de `SELECT` permissões da empresa foi aprimorado.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-2456--> As consultas de Categoria agora retornam preços de produto de acordo com as configurações da loja quando não há permissões de categoria definidas explicitamente na categoria que está sendo consultada.

![Correção de um problema](../assets/fix.svg) <!--- ACP2E-6829--> O botão **[!UICONTROL Place Order]** agora funciona conforme esperado ao concluir uma compra com uma solicitação de cotação aprovada. Problemas com o plug-in de cotação negociável `negotiableQuoteCheckoutSessionPlugin` foram resolvidos.

## B2B v1.3.4-p14

*12 de agosto de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.3.4-p13

*10 de junho de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.5-p12.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-50](https://helpx.adobe.com/br/security/products/magento/apsb25-50.html).

## B2B v1.3.4-p12

*8 de abril, 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.5-p12.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-26](https://helpx.adobe.com/br/security/products/magento/apsb25-26.html).

## B2B v1.3.4-p11

*11 de fevereiro de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.5-p11.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-08](https://helpx.adobe.com/br/security/products/magento/apsb25-08.html).

## B2B v1.3.4-p10

*9 de outubro de 2024*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.5-p10.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB24-73](https://helpx.adobe.com/br/security/products/magento/apsb24-73.html).

## B2B v1.3.4

*9 de agosto de 2022*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.5.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-453-->O Adobe Commerce não envia mais notificações por email sempre que uma Empresa existente é atualizada por uma chamada de API. Agora, os emails são enviados somente quando uma empresa é criada.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-406-->O Adobe Commerce agora calcula corretamente o total geral de uma cotação negociável quando a configuração de cálculo de imposto **[!UICONTROL Enable Cross Border Trade]** está habilitada.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-322-->Os produtos configuráveis agora são movidos para a última posição na lista de produtos depois que o estoque é atualizado quando a configuração **[!UICONTROL Move out of stock to the bottom]** é habilitada. Uma nova consulta de banco de dados personalizado é implementada para garantir que a ordem de classificação do índice Elasticsearch agora atenda à ordem de classificação habilitada pelo Administrador. Anteriormente, os produtos configuráveis e seus produtos derivados não eram movidos para a parte inferior da lista quando essa configuração era ativada.

![Correção de um problema](../assets/fix.svg) <!--- ACP2E-308-->O email de Ordem de Compra agora respeita a configuração de envio de email de cada site em uma implantação multissite. Uma verificação da configuração **[!UICONTROL Disable Email Communications]** é adicionada à lógica personalizada para filas de email. Anteriormente, o Adobe Commerce não respeitava a configuração de envio de email para o site secundário.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-302-->O título do campo SKU da página Pedido rápido é alterado para maior clareza.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-543-->O Adobe Commerce agora exibe uma mensagem de erro mais informativa quando um comprador insere um SKU inválido no campo **Inserir SKU ou Nome do Produto**.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-1753-->O campo **[!UICONTROL Account Created in]** de um administrador de empresa agora retém seu valor como esperado depois que você salva a empresa.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-722 -->A consulta `customer` não retorna mais resultados vazios quando recupera listas de requisições filtradas por `uid`.

![Correção de um problema](../assets/fix.svg) <!--- ACP2E-210 -->Adição de um plug-in antes da chamada `collectQuoteTotals` para garantir que os créditos de armazenamento sejam aplicados apenas uma vez.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-665 -->Os clientes agora são redirecionados para a página de logon quando sua conta é excluída por um administrador do Administrador. Anteriormente, o Adobe Commerce emitia um erro. O bloco de código do plug-in (`SessionPlugin`) agora está dentro do bloco `try…catch`. Anteriormente, esse código não era encapsulado dentro do bloco genérico de manipulação de exceções.

![Correção de um problema](../assets/fix.svg) <!--- ACP2E-661 --> Na página Pedido rápido no modo móvel, pressionar **Enter** depois de inserir um nome de produto válido ou SKU agora leva o comprador para o próximo campo, conforme esperado.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-607 -->O nome da empresa agora está visível, conforme esperado, nas seções de endereço de entrega e cobrança do fluxo de trabalho de check-out.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-375 -->O crédito da loja agora não está disponível quando o método de pagamento **[!UICONTROL Zero Subtotal Checkout]** está desabilitado. Anteriormente, a caixa de seleção Armazenar crédito não funcionava durante a realização do pedido pelo administrador. O aplicativo não colocou o pedido com o crédito da loja e exibiu este erro: `The requested Payment Method is not available`.

## B2B v1.3.3-p15

*12 de agosto de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-71](https://helpx.adobe.com/security/products/magento/apsb25-71.html).

## B2B v1.3.3-p14

*10 de junho de 2025*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.5-p12.

![Problema corrigido](../assets/fix.svg) Inclui as correções de segurança documentadas no [Boletim de Segurança APSB25-50](https://helpx.adobe.com/br/security/products/magento/apsb25-50.html).

## B2B v1.3.3

*9 de agosto de 2022*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.4.

![Correção de um problema](../assets/fix.svg) <!--- MC-41985--> O tempo necessário para atualizar do Adobe Commerce 2.3.x para o Adobe Commerce 2.4.x em implantações com mais de 100.000 funções da empresa foi substancialmente reduzido.

![Problema corrigido](../assets/fix.svg) <!--- MC-42153--> A solicitação POST `V1/order/:orderId/invoice` agora oferece suporte à criação de faturas parciais quando o método de pagamento **[!UICONTROL Payment on Account]** está habilitado. Anteriormente, o Adobe Commerce exibia este erro: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Problema corrigido](../assets/fix.svg) <!--- MC-41975--> O PayPal Payflow Pro agora funciona conforme esperado com a cotação negociável B2B quando o carrinho do cliente contém outros produtos. O Adobe Commerce agora processa o pedido com êxito e envia um email ao cliente, conforme esperado. Anteriormente, o Adobe Commerce emitia um erro fatal e enviava um email de confirmação para o cliente com valor zero.

![Problema corrigido](../assets/fix.svg) <!--- MC-41819--> A paginação agora é exibida corretamente na página de resultados da pesquisa do catálogo depois de excluir alguns produtos no catálogo compartilhado.

![Problema corrigido](../assets/fix.svg) <!--- MC-42886--> Os atributos personalizados do cliente agora são salvos conforme esperado ao criar ou salvar um usuário da empresa no Administrador.

![Problema corrigido](../assets/fix.svg) <!--- MC-42927--> O botão **[!UICONTROL Submit]** no formulário Criar nova empresa agora está desabilitado após um clique para impedir vários envios de formulários. Anteriormente, você podia enviar esse formulário várias vezes clicando nesse botão repetidamente, o que gerou um erro.

![Problema corrigido](../assets/fix.svg) <!--- MC-42787--> O Adobe Commerce não exibe mais o link de reordenação na loja quando um comprador faz logon em uma loja para a qual as reordenações foram desabilitadas.

![Problema corrigido](../assets/fix.svg) <!--- MC-43115--> A pesquisa de Pedidos Rápidos por SKU agora diferencia maiúsculas de minúsculas quando o catálogo compartilhado está habilitado.

![Problema corrigido](../assets/fix.svg) <!--- MC-42203--> Agora é possível atualizar um arquivo para um atributo do cliente ao criar uma empresa. Anteriormente, ao tentar criar uma empresa com um anexo do tipo `File`, a Adobe Commerce não criava a empresa e registrava este erro no log de exceções: `Something went wrong while saving file`.

![Problema corrigido](../assets/fix.svg) <!--- MC-42242--> Agora é possível criar uma empresa com uma conta de cliente que tenha um atributo personalizado com um tipo (`File`) ou (`Image`). Anteriormente, se a conta tivesse uma dessas opções personalizáveis, o carregador de página de edição da Empresa não resolvia o, o que impedia a edição dos detalhes da empresa.

![Problema corrigido](../assets/fix.svg) <!--- MC-42268--> A consulta `products` agora retorna um campo `total_count` preciso quando o catálogo compartilhado é habilitado.

![Problema corrigido](../assets/fix.svg) <!--- MC-42203--> Agora é possível atualizar um arquivo para um atributo do cliente ao criar uma empresa. Anteriormente, ao tentar criar uma empresa com um anexo do tipo `File`, a Adobe Commerce não criava a empresa e registrava este erro no log de exceções: `Something went wrong while saving file`.

![Problema corrigido](../assets/fix.svg) <!--- MC-43178--> As páginas _Configuração da Empresa_ e _Criar Empresa_ agora funcionam como esperado depois que você desabilita um método de envio online. A verificação foi adicionada para impedir a tentativa de processamento de módulos de envio desabilitados. Anteriormente, o Adobe Commerce exibia este erro: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Problema corrigido](../assets/fix.svg) <!--- MC-42214--> A página _Categoria_ agora exibe dados de produto consistentes enquanto as permissões estão sendo geradas durante a indexação parcial. Um novo indexador parcial para permissões de diretório foi adicionado a este processo. Anteriormente, os dados exibidos enquanto o indexador era executado estavam incorretos.

![Problema corrigido](../assets/fix.svg) <!--- MC-42567--> A consulta `categoryList` agora retorna o número correto de produtos quando são usadas permissões de catálogo e os produtos são atribuídos a um catálogo compartilhado.

![Problema corrigido](../assets/fix.svg) <!--- MC-42528--> Agora a consulta `categoryList` respeita permissões de categoria e retorna somente categorias permitidas. Anteriormente, retornava todas as categorias atribuídas e não atribuídas.

![Problema corrigido](../assets/fix.svg) <!--- MC-42399--> A solicitação `rest/V1/company/{id}` agora retorna `is_purchase_order_enabled` valores de atributo conforme esperado.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-128--> Os atributos personalizados do cliente agora são exibidos conforme esperado na guia _Administrador da Empresa_.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-130--> O bloco Minha Lista de Desejos na página Minha Conta agora é exibido conforme esperado para Administradores da Empresa e Usuários da Empresa.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-133--> Erros de pedidos rápidos não são mais exibidos no carrinho de compras. Anteriormente, o Adobe Commerce exibia esse erro no carrinho de compras quando o SKU não era encontrado no catálogo: `The SKU was not found in the catalog`.

![Problema corrigido](../assets/fix.svg) <!--- ACP2E-194--> As operações de salvamento do catálogo compartilhado foram otimizadas para execução mais rápida. Anteriormente, salvar um catálogo compartilhado com muitos grupos de clientes podia levar vários minutos.

![Correção de um problema](../assets/fix.svg) <!--- MC-42240--> O Adobe Commerce agora exclui todas as permissões de subcategoria da tabela `sharedcatalog_category_permissions` quando a categoria pai é excluída. Anteriormente, somente os dados da categoria principal eram removidos.

## B2B v1.3.2

*29 de agosto de 2022*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.3.

![Problema corrigido](../assets/fix.svg) <!--- MC-39862--> O Adobe Commerce agora envia emails de atualização sobre cotações negociáveis expiradas. Anteriormente, quando uma cotação negociável expirava, o Adobe Commerce não enviava emails de atualização.

![Problema corrigido](../assets/fix.svg) <!--- MC-40682--> O Adobe Commerce agora envia com êxito emails de atualização sobre cotações negociáveis prestes a expirar e expiradas quando um trabalho `cron` está ausente.

### Empresa

![Correção de um problema](../assets/fix.svg) <!--- MC-41542--> O campo suspenso Criar novo país de página de conta da empresa não lista mais os valores de opção vazios. Anteriormente, os dois primeiros valores de opção e o código do país `AN` estavam vazios.

![Correção de um problema](../assets/fix.svg) <!--- MC-41260--> Ao clicar no botão **[!UICONTROL Return]** para um pedido criado por um usuário da empresa, o usuário administrativo é redirecionado para a página Criar Retorno conforme esperado. Anteriormente, o administrador era redirecionado para a página Histórico de pedidos.

![Correção de um problema](../assets/fix.svg) [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} <!--- MC-40798--> O Adobe Commerce não falha mais com um erro de memória insuficiente ao executar o método `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` durante `bin/magento setup:upgrade`. Anteriormente, o Adobe Commerce não usava o tamanho do lote para a coleção ao inicializar permissões, mas carregava uma coleção de todas as funções da empresa.

![Problema corrigido](../assets/fix.svg) <!--- MC-40551--> Os usuários da empresa agora podem editar e atualizar valores de atributos personalizados do cliente. Anteriormente, esses atributos não se vinculavam corretamente ao formulário criar e editar usuário. Um usuário da empresa poderia inserir valores de atributo diferentes, mas o Adobe Commerce não salvou esses valores corretamente.

![Problema corrigido](../assets/fix.svg) <!--- MC-32653--> A árvore de recursos para permissões de função de empresa agora pode ser traduzida conforme esperado. Anteriormente, a árvore de permissões não era traduzida, mesmo se arquivos de tradução válidos estivessem presentes.

![Problema corrigido](../assets/fix.svg) <!--- MC-40358--> O Adobe Commerce agora salva os valores de atributos personalizados do cliente para usuários B2B conforme esperado. Anteriormente, a criação de uma conta de empresa que contivesse atributos personalizados do cliente acionava um erro de modelo e o Adobe Commerce não carregava o formulário com êxito. Adicionar um argumento ao layout de `company_create_account` resolveu esse problema.

![Correção de um problema](../assets/fix.svg) <!--- MC-41721--> Os filtros de usuário da empresa, como Mostrar todos os usuários, Mostrar usuários ativos e Mostrar usuários inativos, agora funcionam conforme esperado. Anteriormente, filtrar ações na página de usuário da empresa causava um erro de JavaScript.

### Crédito da empresa

![Problema corrigido](../assets/fix.svg) <!--- MC-41551--> Os administradores com contas restritas que incluem apenas privilégios no nível do site agora podem criar uma empresa que usa uma moeda diferente da do site.

![Problema corrigido](../assets/fix.svg) <!--- MC-41523--> O Adobe Commerce agora envia emails da empresa do escopo e endereço de email `from` corretos. Anteriormente, a Adobe Commerce não considerava o escopo do site ao enviar a atribuição de crédito da empresa ou atualizar o email.

### Pedido rápido

![Problema corrigido](../assets/fix.svg) <!--- MC-42104--> Criar um pedido usando o Pedido rápido a partir de um arquivo CSV agora funciona conforme esperado com SKUs inexistentes.

![Problema corrigido](../assets/fix.svg) <!--- MC-40268--> O uso do Pedido rápido para pesquisar em várias SKUs agora funciona conforme esperado. Anteriormente, os resultados incluíam entradas duplicadas.

![Problema corrigido](../assets/fix.svg) <!--- MC-40261--> A exibição da lista de Produtos Adicionados agora trata SKUs inseridas em minúsculas e maiúsculas da mesma forma quando você usa SKUs para selecionar vários produtos durante o Pedido Rápido.

![Correção de um problema](../assets/fix.svg) <!--- MC-40225--> O uso do Pedido rápido agora adiciona produtos na quantidade especificada pelo comprador. Anteriormente, a Adobe Commerce adicionava um produto somente quando as quantidades especificadas pelo comprador excediam um.

![Problema corrigido](../assets/fix.svg) <!--- MC-41283--> O recurso de preenchimento automático Pedido rápido agora funciona com SKUs parciais.

![Problema corrigido](../assets/fix.svg) <!--- MC-41299--> O Adobe Commerce agora exibe produtos que foram configurados como **Não visíveis individualmente** na lista de sugestão automática e nos resultados de pesquisa da página Pedido rápido.

![Problema corrigido](../assets/fix.svg) <!--- MC-42402--> Os compradores agora podem usar o formulário Pedido rápido para adicionar vários produtos por SKUs que incluem caracteres em maiúsculas. Anteriormente, somente o primeiro produto era adicionado.

### Cotação negociável

![Problema corrigido](../assets/fix.svg) <!--- MC-41232--> Os compradores agora são redirecionados para a página de cotação negociável depois de colar o link em uma cotação negociável no campo URL e fazer logon com êxito. Anteriormente, os compradores eram redirecionados para a página Minha conta.

![Problema corrigido](../assets/fix.svg) <!--- MC-39317--> A reorganização agora funciona conforme esperado em pedidos que contêm um produto com uma Opção Personalizável de Data para uma conta de cliente que foi criada durante o check-out. Anteriormente, o Adobe Commerce não processava a reordenação e exibia este erro: `The product has required options. Enter the options and try again`.

![Problema corrigido](../assets/fix.svg) <!--- MC-39063--> O endereço de remessa de uma cotação negociável não é mais editável durante o check-out quando o módulo Ordem de Compra está desabilitado. Este comportamento resultou de uma correção anterior na qual `isQuoteAddressLocked` foi removido do renderizador de check-out de cotação negociável.

![Problema corrigido](../assets/fix.svg) <!--- MC-38967--> Os comerciantes agora podem adicionar produtos a uma cotação negociável do Administrador.

### Ordens de compra

![Problema corrigido](../assets/fix.svg) <!--- MC-39983--> O Adobe Commerce agora exibe uma mensagem de erro informativa, conforme esperado, quando você faz uma ordem de compra usando o Check-out do PayPal Express quando o atributo **[!UICONTROL Name Prefix]** está definido como `required`. Anteriormente, o Adobe Commerce não colocava o pedido nem exibia uma mensagem de erro.

![Problema corrigido](../assets/fix.svg) <!--- MC-39620--> O componente da interface do usuário para o endereço de cobrança no módulo Ordem de Compra agora usa o endereço de cotação corretamente quando o Google Tag Manager está habilitado. Anteriormente, ocorria um erro de JavaScript na página de pagamento.

### Listas de requisições

![Problema corrigido](../assets/fix.svg) <!--- MC-40426--> Os comerciantes agora podem usar o ponto de extremidade POST `rest/all/V1/requisition_lists` para criar uma lista de requisições para um cliente. Anteriormente, o Adobe Commerce exibia este erro 400 quando você tentava criar uma lista de requisições: `Could not save Requisition List`.

![Problema corrigido](../assets/fix.svg) <!--- MC-41123--> O botão **[!UICONTROL Add to Requisition List]** agora é exibido para produtos em estoque de um carrinho de compras quando o carrinho também contém produtos indisponíveis. Anteriormente, se um carrinho continha dois produtos, um deles estava indisponível, o botão _[!UICONTROL Add to Requisition List]_&#x200B;não era exibido para nenhum dos produtos.

![Problema corrigido](../assets/fix.svg) <!--- MC-40877--> Agora você pode usar a API REST para adicionar um produto a uma lista de requisições.

![Problema corrigido](../assets/fix.svg) <!--- MC-40155--> Os valores **[!UICONTROL Latest Activity Date]** da lista de requisições agora seguem o formato de localidade.

![Problema corrigido](../assets/fix.svg) <!--- MC-39580--> O Adobe Commerce não lança mais um erro fatal quando você edita um produto agrupado de uma lista de requisições.

![Problema corrigido](../assets/fix.svg) <!--- MC-40454--> O Adobe Commerce agora exibe o preço correto do produto quando você adiciona um produto com uma opção personalizável `(File)` a uma lista de desejos de uma lista de requisições. O link para o arquivo carregado também está visível, conforme esperado. Anteriormente, o Adobe Commerce exibia preços de produtos incorretos e não exibia o link para o arquivo.

![Problema corrigido](../assets/fix.svg) <!--- MC-36383--> Os produtos com uma opção personalizável `(File)` agora podem ser adicionados a um carrinho de compras a partir de uma lista de requisições.

### Catálogo compartilhado

![Problema corrigido](../assets/fix.svg) <!--- MC-40497--> Um administrador com uma função limitada a um site específico agora pode criar, exibir e editar um catálogo compartilhado. Anteriormente, o Adobe Commerce emitia um erro fatal quando um administrador com uma função limitada tentava criar um catálogo compartilhado.

![Problema corrigido](../assets/fix.svg) <!--- MC-41337--> Os resultados da navegação em camadas agora incluem uma contagem precisa de produtos com atributos filtrados, e os compradores agora podem aplicar vários filtros. Anteriormente, somente um filtro podia ser aplicado, e o Adobe Commerce exibia uma contagem de produtos imprecisa na navegação em camadas.

![Problema corrigido](../assets/fix.svg) <!--- MC-40779--> O Adobe Commerce agora exibe corretamente as contagens de produtos nos filtros de navegação em camadas nos resultados da pesquisa. Anteriormente, um plug-in para a página Resultados da pesquisa não usava o Elasticsearch, mas emitia uma nova consulta ao banco de dados.

![Problema corrigido](../assets/fix.svg) <!--- MC-39978--> O Adobe Commerce não exclui mais os preços de camada quando um comerciante exclui todos os produtos de um catálogo compartilhado padrão.

![Problema corrigido](../assets/fix.svg) <!--- MC-39802--> Agora os filtros são filtrados pela categoria atual e exibidos corretamente em todas as páginas quando os catálogos compartilhados estão habilitados. Anteriormente, os filtros eram calculados incorretamente somente para a página atual e não eram filtrados pela categoria atual.

![Problema corrigido](../assets/fix.svg) <!--- MC-39522--> A consulta do GraphQL `products` não retorna mais o intervalo de preços e a categoria de um produto para produtos que não estão atribuídos a um catálogo compartilhado quando o catálogo compartilhado está habilitado. Anteriormente, a consulta retornava as agregações do produto, mesmo que o produto em si não fosse retornado na matriz `items`.

## B2B v1.3.1

*9 de fevereiro de 2021*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.2.

![Novos](../assets/new.svg) Métodos de pagamento online agora têm suporte para ordens de compra.

![Correção de um problema](../assets/fix.svg) A adição de um produto configurável ao carrinho diretamente de uma lista de requisições quando esse produto era usado em um pedido anterior não retornava mais um erro do sistema.

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe a guia Requer minha aprovação corretamente para ordens de compra quando uma configuração de banco de dados dividido é implantada.

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe detalhes sobre produtos agrupados e cartão-presente quando você exibe ordens de compra.

![Problema corrigido](../assets/fix.svg) Os compradores agora são redirecionados conforme esperado depois de fazer logon em sua conta enquanto navegam em um armazenamento onde **[!UICONTROL Website Restriction]** está habilitado e **[!UICONTROL Restriction Mode]** está definido como `Private Sales: Login Only`. Anteriormente, os compradores eram redirecionados para a página inicial da loja. <!--- MC-38934-->

![Problema corrigido](../assets/fix.svg) O histórico de pedidos agora é carregado conforme esperado na página do painel de conta de um administrador de empresa em implantações com uma hierarquia de empresa B2B que contém muitos clientes (maior que 13000). Anteriormente, o histórico do pedido era carregado lentamente ou não era carregado, e o Adobe Commerce exibia um erro 503. <!--- MC-38830-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais várias mensagens de aviso idênticas quando você adiciona um produto não configurado com opções personalizáveis a uma Lista de Requisições a partir de uma página Categoria. <!--- MC-38342-->

![Problema corrigido](../assets/fix.svg) Produtos novos e duplicados agora ficam visíveis, conforme esperado, na página de categoria quando catálogos compartilhados B2B são habilitados. <!--- MC-38307-->

![Problema corrigido](../assets/fix.svg) A Adobe Commerce agora mantém o `store_id` correto que está associado a um administrador de empresa quando o grupo de clientes de uma empresa é atualizado. Anteriormente, o `store_id` era alterado para o armazenamento padrão quando o grupo era atualizado. <!--- MC-38196-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora salva um produto agrupado em uma lista de requisições como uma lista de produtos simples, da mesma forma que adiciona um produto agrupado a um carrinho de compras. Anteriormente, devido à forma como o Adobe Commerce salvava os produtos agrupados, o link de um produto agrupado da lista de requisições sempre era redirecionado para produtos simples e não para o produto agrupado. <!--- MC-38049-->

![Correção de um problema](../assets/fix.svg) Agora é possível filtrar pedidos pelo campo **[!UICONTROL Company Name]** ao exportar informações do pedido no formato CSV. Anteriormente, o Adobe Commerce registrava um erro em `var/export/{file-id}`. <!--- MC-37785-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe o pop-up Criar lista de requisições conforme esperado ao selecionar a guia Criar nova lista de requisições na loja. <!--- MC-37915-->

![Problema corrigido](../assets/fix.svg) As listas de requisições agora incluem todos os produtos agrupados e quantidades que foram adicionadas à lista. Anteriormente, quando um comerciante navegava para uma lista de requisições depois de adicionar produtos a ela a partir de uma página de detalhes do produto, o Adobe Commerce exibia este erro: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Problema corrigido](../assets/fix.svg) A exibição de armazenamento correta agora está associada ao site relevante quando você cria uma empresa em uma implantação multissite. Anteriormente, você não podia criar uma empresa, e o Adobe Commerce exibiu este erro: `The store view is not in the associated website`. <!--- MC-37488-->

![Problema corrigido](../assets/fix.svg) A solicitação de produtos por SKU usando o Pedido rápido não resulta mais em quantidades de produtos duplicadas no arquivo CSV. <!--- MC-37427-->

![Correção de um problema](../assets/fix.svg) O botão **[!UICONTROL Add to Cart]** não é mais bloqueado quando a seção _[!UICONTROL Enter Multiple SKUs]_&#x200B;da página Pedido rápido contém um valor vazio. Em vez disso, o Adobe Commerce agora exibe uma mensagem solicitando que você insira SKUs válidas. <!--- MC-37387-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora exibe esta mensagem na página do produto quando você envia uma revisão do produto a partir de uma lista de requisições: `You submitted your review for moderation`. A revisão também aparece na página Revisões pendentes (Administrador **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Anteriormente, embora a Adobe Commerce tenha adicionado a revisão à lista de revisões pendentes, ela apresentou um erro 404 na página do produto. <!--- MC-37119-->

![Problema corrigido](../assets/fix.svg) O desempenho do consumidor `sharedCatalogUpdateCategoryPermissions` foi aprimorado. Depois de criar um catálogo compartilhado, o indexador de permissões do catálogo agora usa somente a ID do grupo de clientes do catálogo compartilhado, não todos os grupos de clientes. <!--- MC-36770-->

![Problema corrigido](../assets/fix.svg) Os campos de atributo de endereço personalizado do cliente associados ao endereço não padrão de um comprador agora são salvos conforme esperado no fluxo de trabalho de check-out da vitrine. <!--- MC-36630-->

![Problema corrigido](../assets/fix.svg) Os pedidos de produtos que pertencem ao catálogo compartilhado padrão de uma loja agora podem ser feitos para compradores por meio da API REST de Administrador (`rest/V1/carts/{<CART_ID>/items`), conforme esperado. O Adobe Commerce agora verifica se o produto foi atribuído a um catálogo público antes da validação de permissões de catálogo compartilhado em `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Anteriormente, o Adobe Commerce não adicionava o produto ao carrinho do comprador e exibia este erro: `No such shared catalog entity`. <!--- MC-36535-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora envia novos emails de registro de usuário da empresa do endereço da Adobe Commerce Store. Anteriormente, esse email era enviado do endereço do administrador da empresa. <!--- MC-36480-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora verifica os atributos personalizados quanto à duplicação de nomes de atributos de empresa reservados antes de permitir que um comerciante salve um novo atributo. <!--- MC-36282-->

![Problema corrigido](../assets/fix.svg) A consulta `credit_history` agora retorna o histórico de crédito da empresa especificada para o valor originalmente alocado e o valor adquirido. Anteriormente, essa consulta retornava um erro.

![Problema corrigido](../assets/fix.svg) Os campos **[!UICONTROL Company]** e **[!UICONTROL Job Title]** da página Editar Informações da Conta não são mais editáveis.

### Problemas conhecidos

- Compradores B2B podem usar métodos de pagamento on-line para ignorar o fluxo normal da ordem de compra. Esse cenário pode ocorrer se o comprador puder reduzir todo o total do check-out para 0 — por exemplo, por um código promocional ou cartão-presente — e depois remover o código ou o cartão-presente. Mesmo nessas condições, a Adobe Commerce ainda faz o pedido com a quantia correta com base nos preços dos itens em seu catálogo atribuído. **_Solução alternativa_**: desabilite cartões-presente e códigos de cupom quando os métodos de pagamento online estiverem habilitados para aprovação de ordem de compra. <!--- B2B-1603-->

- Os compradores são redirecionados para o carrinho de compras quando tentam fazer um pedido de uma ordem de compra usando o Check-out Expresso do PayPal quando **[!UICONTROL In-Context Mode]** está desativado. <!--- B2B-1604-->

- O Adobe Commerce às vezes exibe um erro 404 quando um comprador cria uma ordem de compra e, em seguida, navega até a página de finalização. Esse erro ocorre quando um comprador criou anteriormente uma ordem de compra diferente com um método de pagamento online antes de navegar até a página de finalização sem concluir a compra anterior. O comprador ainda pode colocar a ordem de compra. **_Solução alternativa_**: nenhuma. <!--- B2B-1605-->

- Os descontos para um método de pagamento específico persistem durante o check-out de uma ordem de compra mesmo quando o comprador altera seu método de pagamento durante o check-out final. Como resultado, os clientes podem receber um desconto ao qual não têm direito. Esse problema ocorre porque uma regra de carrinho para o método de pagamento original ainda é aplicada apesar da alteração no método de pagamento. **_Solução alternativa_**: nenhuma. Consulte o artigo [Adobe Commerce 2.4.2 B2B conhecido: o desconto permanece para Ordens de Compra online depois que o método de pagamento é alterado](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html?lang=pt-BR) _Knowledge Base_. <!-- B2B-1012 -->

- A consulta `deleteRequisitionListOutput` retorna detalhes sobre a lista de requisições excluída em vez das listas de requisições restantes. <!--- MC-39894-->

## B2B v1.3.0

*15 de outubro de 2020*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

Esta versão inclui melhorias nas aprovações de pedidos, métodos de envio, carrinho de compras e registro de ações de administrador.

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.1.

![As novas](../assets/new.svg) aprovações de pedidos B2B foram aprimoradas para melhorar a usabilidade e permitir ações em massa em ordens de compra.

![Novos](../assets/new.svg) comerciantes B2B agora podem controlar os métodos de envio oferecidos a cada Empresa.<!--- BUNDLE-160 161 162 -->

![Novos](../assets/new.svg) Comerciantes agora podem permitir que os usuários limpem o conteúdo de seus carrinhos de compras em uma única ação e podem configurar esta habilidade independentemente em cada site <!--- BUNDLE-108 -->

![Novos](../assets/new.svg) compradores B2B agora podem adicionar itens individuais ou todo o conteúdo de seu carrinho de compras diretamente a uma lista de requisições. <!--- BUNDLE-145 144-->

![Novos](../assets/new.svg) comerciantes B2B podem criar pedidos do Administrador em nome de clientes usando Pagamento na Conta como método de pagamento. <!--- BUNDLE-166 178-->

![Novos](../assets/new.svg) Comerciantes agora podem ver diretamente todas as cotações associadas a um usuário na página de detalhes do cliente. <!--- BUNDLE-139 -->

![Novos](../assets/new.svg) Comerciantes agora podem filtrar a grade Clientes Agora Online por Empresa. <!--- BUNDLE-137 -->

![Novos](../assets/new.svg) administradores agora podem filtrar clientes no Administrador por Representante de vendas <!--- BUNDLE-110 -->

![Novo](../assets/new.svg) Para reduzir a criação de contas fraudulentas ou de spam, os comerciantes agora podem habilitar o Google reCAPTCHA no formulário Solicitação de nova empresa na loja. <!--- BUNDLE-154 -->

![Novas](../assets/new.svg) Ações de administrador realizadas nos módulos da Empresa agora estão registradas no Log de Ações de Administrador. Ações são registradas de todos os módulos de empresa relevantes: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`. <!--- BUNDLE-180 181 182 183 -->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais o botão **[!UICONTROL Delete customer]** na página **Clientes** quando o administrador conectado não tem direitos para excluir clientes em implantações em que o B2B está instalado. <!--- MC-35655-->

![Problema corrigido](../assets/fix.svg) O grupo de clientes não é mais alterado automaticamente para um cliente atribuído a uma Empresa quando você edita o cliente na grade Cliente. <!--- MC-35254-->

![Correção de um problema](../assets/fix.svg) Quando um comerciante cria um catálogo compartilhado, as permissões agora são automaticamente definidas como `Allow` para os recursos **[!UICONTROL Display Product Prices]** e **[!UICONTROL Add to Cart]** em categorias quando o grupo de clientes recebe esse acesso nas configurações de permissão do catálogo. Anteriormente, essas configurações eram automaticamente definidas como `Deny`, mesmo quando as permissões do catálogo eram definidas como `Allow`.<!--- MC-34792-->

![Problema corrigido](../assets/fix.svg) As permissões de categoria do catálogo compartilhado não são mais substituídas quando um produto é editado na página de edição do produto.<!--- MC-34777-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora envia uma notificação por email confirmando que um cliente tem permissão para exceder o limite de crédito designado quando um comerciante habilita a configuração **[!UICONTROL Allow To Exceed Credit Limit]**. Anteriormente, o email de notificação enviado pela Adobe Commerce indicava que o cliente não tinha permissão para exceder o limite. <!--- MC-34584-->

![Problema corrigido](../assets/fix.svg) O contêiner HTML que circunda o preço do produto nas listas de requisições agora é renderizado corretamente para os filhos de produtos agrupados. <!--- MC-36331-->

![Problema corrigido](../assets/fix.svg) Os comerciantes agora podem designar o idioma em que o email do usuário da empresa é enviado ao criar uma empresa em implantações de vários idiomas. Anteriormente, o menu suspenso permitia que os comerciantes selecionassem a exibição de loja e o idioma apropriados não eram exibidos.  <!--- MC-35777-->

![Problema corrigido](../assets/fix.svg) Os campos de atributos personalizados do endereço do cliente agora são exibidos conforme esperado no fluxo de trabalho de check-out da loja. <!--- MC-35607-->

![Problema corrigido](../assets/fix.svg) A guia de configuração Recursos B2B agora é aberta corretamente. <!--- MC-35458-->Os convidados agora podem usar o QuickOrder para adicionar produtos ao carrinho e depois remover itens com êxito. Anteriormente, quando um comprador usava o QuickOrder para adicionar vários produtos ao carrinho e, em seguida, removia um produto, o produto não era removido. <!--- MC-35327-->

![Problema corrigido](../assets/fix.svg) Agora uma empresa pode ser atualizada usando a solicitação REST API PUT `/V1/company/:companyId` sem especificar o `region_id` quando o estado está configurado como **não necessário**. Anteriormente, mesmo que `region_id` não fosse necessário, o Adobe Commerce emitia um erro se não estivesse especificado. <!--- MC-35304-->

![Correção de um problema](../assets/fix.svg) Ao criar ou atualizar uma Empresa B2B usando a API REST (`http://magento.local/rest/V1/company/2`, em que `2` representa a ID da empresa), a resposta agora inclui as configurações para `applicable_payment_method` ou `available_payment_methods`, conforme esperado. <!--- MC-35248-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não exibe mais uma página 404 quando um comerciante usa o botão **Inserir** em vez de clicar no botão **[!UICONTROL Save]** ao criar uma lista de requisições na loja.<!--- MC-35094-->

![Problema corrigido](../assets/fix.svg) Permissões de categoria não são mais alteradas quando um novo produto é atribuído a um catálogo público compartilhado. Anteriormente, as permissões de categoria eram duplicadas. <!--- MC-34386-->

![Correção de um problema](../assets/fix.svg) O ponto de extremidade da API REST PUT `rest/default/V1/company/{id}`, que é usado para atualizar o email da Empresa, não diferencia mais maiúsculas de minúsculas. <!--- MC-34308-->

![Problema corrigido](../assets/fix.svg) Desabilitar módulos de premiação não afeta mais os recursos B2B nas contas do cliente. Anteriormente, quando os módulos de premiação eram desabilitados, as seguintes guias relacionadas a B2B não eram exibidas: Perfil da Empresa, Usuários da Empresa e Funções e Permissões.<!--- MC-34191-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce agora usa o nome correto do remetente nas notificações por email quando alterações são feitas nas contas da empresa. Anteriormente, o Adobe Commerce usava o nome geral do remetente do contato definido no escopo padrão para todos os emails. <!--- MC-33917-->

![Problema corrigido](../assets/fix.svg) Agora é possível implementar com êxito o envio múltiplo de pedidos que contêm produtos físicos e virtuais. <!--- MC-33818-->

![Problema corrigido](../assets/fix.svg) Os comerciantes podem agora criar usuários da empresa na seção _[!UICONTROL Company Users]_&#x200B;das páginas Minha Conta e Estrutura da Empresa quando o **[!UICONTROL Access Restriction]**&#x200B;está habilitado e o **[!UICONTROL Restriction Mode]**&#x200B;está definido como `Sales: Login Only`. Anteriormente, o Adobe Commerce exibia este erro quando um comerciante tentava criar um usuário: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não redefine mais o grupo de clientes padrão quando um cliente salva suas informações de conta. <!--- MC-33554-->

![Problema corrigido](../assets/fix.svg) O Adobe Commerce não lança mais um erro fatal quando um administrador atribui um cliente que tem um carrinho de compras ativo a um grupo de clientes. <!--- MC-33313-->

![Problema corrigido](../assets/fix.svg) A Adobe Commerce agora fornece um evento DataLayer `addToCart` para páginas de listas de Pedidos Rápidos e Requisições.  <!--- MC-33295-->

![Problema corrigido](../assets/fix.svg) Os emails de notificação enviados aos representantes de vendas atribuídos a uma empresa agora incluem o logotipo corporativo atribuído. Anteriormente, o email de notificação incluía o logotipo padrão da LUMA, não o logotipo corporativo carregado. <!--- MC-33232-->

![Problema corrigido](../assets/fix.svg) Uma lista de requisições agora inclui todos os produtos agrupados e quantidades que foram adicionadas à lista. Anteriormente, quando um comerciante navegava para uma lista de requisições depois de adicionar produtos a ela a partir de uma página de detalhes do produto, o Adobe Commerce exibia este erro: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problema corrigido](../assets/fix.svg) A consulta `products` agora retorna um campo `total_count` preciso quando o catálogo compartilhado é habilitado. <!--- MC-42268-->

![Correção de um problema](../assets/fix.svg) As páginas Configuração de empresa e Criar empresa agora funcionam como esperado depois que você desabilita um método de envio online. A verificação foi adicionada para impedir a tentativa de processamento de módulos de envio desabilitados. Anteriormente, o Adobe Commerce exibia este erro: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Problema corrigido](../assets/fix.svg) O consumo de memória de teste de integração foi reduzido, o que melhora o desempenho do teste e reduz o tempo necessário para a conclusão do teste. <!--- AC-266-->

## B2B v1.2.0

*28 de julho de 2020*

[!BADGE Com suporte]{type=Informative tooltip="Compatível"} para Adobe Commerce 2.4.0 e versões mais recentes

![Novo](../assets/new.svg) Suporte adicionado para o Adobe Commerce 2.4.0.

![Nova](../assets/new.svg) Pesquisa de Pedido de Vitrines, com agradecimento pela contribuição de Marek Mularczyk do [Divante](https://www.divante.com/) e membros da comunidade.

![Novas](../assets/new.svg) Ordens de Compra foram aprimoradas e regravadas. Agora elas são incluídas por padrão no Adobe Commerce.

![Novas](../assets/new.svg) Regras de Aprovação de Ordem de Compra foram implementadas. Essas regras permitem que os usuários controlem o workflow Ordem de Compra criando regras de compra para ordens.

![Novo](../assets/new.svg) Faça logon como Cliente agora é incluído por padrão no Adobe Commerce. Esse recurso permite que os funcionários do site ajudem os clientes fazendo logon como cliente para ver o que veem.

![Problema corrigido](../assets/fix.svg) As agregações de atributo agora estão funcionando corretamente para a Navegação em camadas com o Elasticsearch

![Problema corrigido](../assets/fix.svg) A pesquisa de pedidos por caracteres especiais agora está funcionando corretamente.

![Correção de um problema](../assets/fix.svg) Clicar no botão **[!UICONTROL Clear All]** agora expande todos os filtros, em vez de recolhê-los.

![Problema corrigido](../assets/fix.svg) O SKU/Nome do Produto agora está incluído no resumo do filtro de pesquisa do Histórico de Pedidos.

![Problema corrigido](../assets/fix.svg) O Indicador de Classificação agora é exibido corretamente na Grade Minhas Ordens de Compra.

![Problema corrigido](../assets/fix.svg) Agora, você pode clicar nos botões Aprovar, Cancelar, Rejeitar e Ordem de compra apenas uma vez. Anteriormente, você podia clicar no botão várias vezes.

![Correção de um problema](../assets/fix.svg) Os botões Aprovar, Rejeitar, Cancelar e Validar da Ordem de Compra agora são renderizados corretamente em dispositivos móveis.

![Correção de um problema](../assets/fix.svg) Anteriormente, a aprovação de uma Ordem de Compra com um desconto que expirou colocava a ordem no valor total e não atualizava o total da Ordem de Compra. Agora, o total da ordem de compra é atualizado para mostrar o total correto.

![Correção de um problema](../assets/fix.svg) Introduzido na versão 2.3.4, em que os atributos de extensão personalizados não eram copiados do Endereço do Cliente para o Endereço da Cotação. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Com B2B instalado, um erro SQL seria exibido ao atribuir categorias a catálogos compartilhados. Esse problema foi corrigido.

![Correção do problema](../assets/fix.svg) Devido a um valor de tipo de variável incorreto, os administradores não puderam adicionar produtos configuráveis a um pedido. Os menus suspensos de opção não eram preenchidos. Esse recurso agora funciona corretamente.

![Correção de um problema](../assets/fix.svg) anteriormente, ao editar Permissões de Categoria para o grupo Não Conectado, ocorria um erro ao salvar as alterações. Esse problema foi corrigido.

![Problema corrigido](../assets/fix.svg) Uma correção foi adicionada para permitir que os administradores de loja adicionem produtos a um pedido que não está no catálogo compartilhado. Anteriormente, uma mensagem de erro era exibida ao adicionar um item que não estava no catálogo.

![Correção de um problema](../assets/fix.svg) [!BADGE PaaS somente]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} Anteriormente, após executar o comando `php bin/magento indexer:set-dimensions-mode catalog_product_price website` e tentar criar um catálogo compartilhado, ocorria um erro. Esse problema foi corrigido.

![Correção de um problema](../assets/fix.svg) Ao adicionar uma empresa e atribuir o administrador da empresa a um site não padrão, a ID de site incorreta foi enviada, causando um erro. Esse problema foi corrigido.

![Correção de um problema](../assets/fix.svg) anteriormente, depois que um cliente era movido para outro grupo de clientes, a adição de um produto a um pedido usando o _Pedido rápido_ falhava com um erro. Esse problema foi corrigido.

![Correção de um problema](../assets/fix.svg) anteriormente, ao tentar fazer check-out usando a WebAPI com uma cotação B2B, um valor incorreto era enviado para a API, causando um erro. Esse problema foi corrigido.

![Correção de um problema](../assets/fix.svg) anteriormente, ao definir uma empresa como &quot;Ativa&quot; por meio da API, ocorria um erro. Esse problema foi corrigido.

![Correção de um problema](../assets/fix.svg) Devido a uma marca `form` desnecessária, a página do pedido é atualizada automaticamente quando você pressiona Enter após alterar um encargo de remessa proposto. Esse problema foi corrigido.

![Correção de um problema](../assets/fix.svg) anteriormente, ao definir um limite de exibição de produto em uma página de catálogo e esse limite era menor que o número total de produtos, ocorreu um erro. Esse recurso agora funciona conforme esperado.

![Problema corrigido](../assets/fix.svg) anteriormente, ao alterar o administrador de uma empresa, o endereço do administrador original seria copiado para o novo administrador, dando a ele dois endereços. Agora, somente o endereço correto é adicionado.

![Correção de um problema](../assets/fix.svg) anteriormente, o uso da API para salvar um item de cotação quando o Git está definido como &quot;Permitido e Notificar Cliente&quot; falharia. Essa chamada de API agora funciona conforme esperado.

![Problema corrigido](../assets/fix.svg) O Imposto Fixo do Produto agora é exibido na página de detalhes das Cotações.

![Problema corrigido](../assets/fix.svg) anteriormente, clicar em um anexo na guia Comentários da página Minhas Cotações não baixaria o arquivo. Esse comportamento agora funciona conforme esperado.

### Problemas conhecidos

- O Adobe Commerce lança uma exceção durante a atualização para B2B 1.2.0 em uma implantação de vários sites. Quando `setup:upgrade` é executado, este erro ocorre no módulo `PurchaseOrder`: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Solução alternativa**: instale a interface `B2B-716 Add NonTransactionableInterface` para o hotfix de patch de dados `InitPurchaseOrderSalesSequence`, que agora está disponível na seção **Minha Conta** > **Downloads** de `magento.com`.
- Se um código de desconto expirar antes de uma Ordem de Compra (OC) ser aprovada, a OC continuará a exibir o valor descontado, mas uma vez aprovada a OC, a ordem será colocada no total não descontado. **Solução alternativa**: instale o hotfix `B2B-709 Purchase Order Discount patch` para esse problema, que agora está disponível na seção **Minha Conta** > **Downloads** de `magento.com`.
- Se os itens em uma ordem de compra estiverem esgotados ou em quantidade insuficiente quando a ordem de compra for convertida em uma ordem real, ocorrerá um erro. Se as ordens pendentes estiverem ativadas, a ordem será processada normalmente.
