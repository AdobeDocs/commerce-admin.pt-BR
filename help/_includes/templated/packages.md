---
source-git-commit: fefaf699dda58e9c908c6b85b0cc16432edb90b6
workflow-type: tm+mt
source-wordcount: '2078'
ht-degree: 0%

---
# Adobe Commerce com pacotes B2B

<!-- The 'packages' variable contains the 'packages' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'packages-dev' variable contains the 'packages-dev' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'product' variable contains data of the 'magento/product-enterprise-edition' package
 -->

<!-- The edition variable contains `commerce-b2b` value from the _data/names.yml file
 -->

O Adobe Commerce B2B usa o Composer para gerenciar pacotes PHP.

O arquivo `composer.json` declara a lista de pacotes, enquanto o arquivo `composer.lock` armazena uma lista completa dos pacotes (uma versão completa de cada pacote e suas dependências) usados para criar uma instalação do Adobe Commerce B2B.

A documentação de referência a seguir é gerada a partir do arquivo `composer.lock`, e ela abrange os pacotes necessários incluídos no Adobe Commerce B2B 1.5.2.

## Dependências

`magento/extension-b2b 1.5.2` tem as seguintes dependências:

```config
magento/framework: >=103.0.6 <103.0.9
magento/magento2-b2b-base: 1.5.2
magento/module-b2b: 100.5.2
magento/module-bundle-negotiable-quote: 100.5.1
magento/module-bundle-requisition-list: 100.5.1
magento/module-bundle-requisition-list-graph-ql: 1.5.1
magento/module-bundle-shared-catalog: 100.5.1
magento/module-checkout-address-search-negotiable-quote: 100.5.1
magento/module-checkout-agreements-negotiable-quote: 100.5.1
magento/module-checkout-agreements-purchase-order: 1.5.1
magento/module-company: 102.0.2
magento/module-company-asynchronous-operations: 1.5.1
magento/module-company-credit: 100.5.2
magento/module-company-credit-graph-ql: 1.5.1
magento/module-company-customer-import-export: 1.5.0
magento/module-company-graph-ql: 1.5.2
magento/module-company-negotiable-quote: 1.5.1
magento/module-company-negotiable-quote-template: 1.5.1
magento/module-company-payment: 100.5.1
magento/module-company-quote: 1.5.2
magento/module-company-quote-graph-ql: 1.5.2
magento/module-company-relation: 1.5.2
magento/module-company-relation-shared-catalog: 1.5.1
magento/module-company-shipping: 1.5.1
magento/module-configurable-negotiable-quote: 100.5.1
magento/module-configurable-requisition-list: 100.5.1
magento/module-configurable-requisition-list-graph-ql: 1.5.1
magento/module-configurable-shared-catalog: 100.5.1
magento/module-downloadable-company: 1.5.1
magento/module-downloadable-requisition-list-graph-ql: 1.5.1
magento/module-gift-card-negotiable-quote: 100.5.1
magento/module-gift-card-requisition-list: 100.5.1
magento/module-gift-card-requisition-list-graph-ql: 1.5.1
magento/module-gift-card-shared-catalog: 100.5.1
magento/module-grouped-requisition-list: 100.5.1
magento/module-grouped-shared-catalog: 100.5.1
magento/module-negotiable-quote: 101.0.2
magento/module-negotiable-quote-async-order: 1.5.1
magento/module-negotiable-quote-duplicate: 1.5.2
magento/module-negotiable-quote-duplicate-graph-ql: 1.5.1
magento/module-negotiable-quote-graph-ql: 1.5.1
magento/module-negotiable-quote-requisition-list: 1.5.1
magento/module-negotiable-quote-requisition-list-graph-ql: 1.5.1
magento/module-negotiable-quote-shared-catalog: 100.5.1
magento/module-negotiable-quote-template: 1.5.2
magento/module-negotiable-quote-template-graph-ql: 1.5.2
magento/module-negotiable-quote-template-shared-catalog: 1.5.1
magento/module-negotiable-quote-weee: 100.5.1
magento/module-order-history-search: 100.5.2
magento/module-paypal-negotiable-quote: 1.5.1
magento/module-paypal-purchase-order: 1.5.1
magento/module-purchase-order: 100.5.2
magento/module-purchase-order-graph-ql: 1.5.1
magento/module-purchase-order-rule: 100.5.2
magento/module-purchase-order-rule-graph-ql: 1.5.1
magento/module-quick-order: 100.5.1
magento/module-quick-order-graph-ql: 1.5.1
magento/module-requisition-list: 100.5.2
magento/module-requisition-list-graph-ql: 1.5.1
magento/module-shared-catalog: 100.5.2
magento/module-shared-catalog-graph-ql: 1.5.1
magento/security-package-b2b: 1.0.6
```

## Licenças de terceiros

### Apache-2.0, somente LGPL-2.1

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/opensearch-project/opensearch-php.git">opensearch-project/opensearch-php</a>
    </td>
    <td>biblioteca</td>
    <td>Cliente PHP para OpenSearch</td>
  </tr>
  </tbody>
</table>

### Apache-2.0

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/adobe/stock-api-libphp.git">astock/stock-api-libphp</a>
    </td>
    <td>biblioteca</td>
    <td>Biblioteca de API do Adobe Stock</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/awslabs/aws-crt-php.git">aws/aws-crt-php</a>
    </td>
    <td>biblioteca</td>
    <td>AWS Common Runtime para PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/aws/aws-sdk-php.git">aws/aws-sdk-php</a>
    </td>
    <td>biblioteca</td>
    <td>AWS SDK para PHP - Use o Amazon Web Services no seu projeto PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/api.git">abrir-telemetria/api</a>
    </td>
    <td>biblioteca</td>
    <td>API para OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/context.git">abrir-telemetria/contexto</a>
    </td>
    <td>biblioteca</td>
    <td>Implementação de contexto para OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree
    </td>
    <td>metapackage</td>
    <td>Braintree Magento</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/wikimedia/less.php.git">wikimedia/less.php</a>
    </td>
    <td>biblioteca</td>
    <td>Porta PHP do processador LESS</td>
  </tr>
  </tbody>
</table>

### Cláusula BSD- 2

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/Bacon/BaconQrCode.git">bacon/bacon-qr-code</a>
    </td>
    <td>biblioteca</td>
    <td>O BaconQrCode é um gerador de código QR para PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/DASPRiD/Enum.git">dasprid/enum</a>
    </td>
    <td>biblioteca</td>
    <td>Implementação do PHP 7.1 enum</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webimpress/safe-writer.git">webimpress/safe-writer</a>
    </td>
    <td>biblioteca</td>
    <td>Ferramenta para gravar arquivos com segurança, para evitar condições de corrida</td>
  </tr>
  </tbody>
</table>

### BSD-3-Cláusula

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_File.git">colinmollenhour/cache-backend-file</a>
    </td>
    <td>magento-módulo</td>
    <td>O back-end do stock Zend_Cache_Backend_Arquivo apresenta um desempenho extremamente ruim para a limpeza por tags que tornam-no inutilizável à medida que aumenta o número de itens em cache. Este back-end faz muitas mudanças que resultam em um grande aumento de desempenho, especialmente para a limpeza tag.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/php-redis-session-abstract.git">colinmollenhour/php-redis-session-abstract</a>
    </td>
    <td>biblioteca</td>
    <td>Um manipulador de sessão baseado em Redis com bloqueio otimista</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/duosecurity/duo_universal_php.git">duosecurity/duo_universal_php</a>
    </td>
    <td>biblioteca</td>
    <td>Uma implementação em PHP do Duo Universal SDK.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/firebase/php-jwt.git">firebase/php-jwt</a>
    </td>
    <td>biblioteca</td>
    <td>Uma biblioteca simples para codificar e decodificar JSON Web Tokens (JWT) no PHP. Deve estar em conformidade com as especificações atuais.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-captcha.git">laminas/laminas-captcha</a>
    </td>
    <td>biblioteca</td>
    <td>Gerar e validar CAPTCHAs usando Figlets, imagens, ReCaptcha e muito mais</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-code.git">laminas/laminas-code</a>
    </td>
    <td>biblioteca</td>
    <td>Extensões para a API de reflexão do PHP, varredura de código estático e geração de código</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-config.git">laminas/laminas-config</a>
    </td>
    <td>biblioteca</td>
    <td>O fornece uma interface do usuário baseada em propriedade de objeto aninhado para acessar esses dados de configuração no código do aplicativo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-di.git">laminas/laminas-di</a>
    </td>
    <td>biblioteca</td>
    <td>Injeção de dependência automatizada para contêineres PSR-11</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-escaper.git">laminas/laminas-escaper</a>
    </td>
    <td>biblioteca</td>
    <td>Escapar com segurança do HTML, atributos do HTML, JavaScript, CSS e URLs</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-eventmanager.git">laminas/laminas-eventmanager</a>
    </td>
    <td>biblioteca</td>
    <td>Acionar e ouvir eventos em um aplicativo PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-feed.git">laminas/laminas-feed</a>
    </td>
    <td>biblioteca</td>
    <td>fornece funcionalidade para criar e consumir feeds RSS e Atom</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-filter.git">laminas/laminas-filter</a>
    </td>
    <td>biblioteca</td>
    <td>Filtrar e normalizar dados e arquivos programaticamente</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-http.git">laminas/laminas-http</a>
    </td>
    <td>biblioteca</td>
    <td>Fornece uma interface fácil para executar solicitações do HTTP (Hyper-Text Transfer Protocol)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-i18n.git">laminas/laminas-i18n</a>
    </td>
    <td>biblioteca</td>
    <td>Fornecer traduções para seu aplicativo e filtrar e validar valores internacionalizados</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-json.git">laminas/laminas-json</a>
    </td>
    <td>biblioteca</td>
    <td>fornece métodos convenientes para serializar PHP nativo para JSON e decodificar JSON para PHP nativo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-loader.git">laminas/laminas-loader</a>
    </td>
    <td>biblioteca</td>
    <td>Estratégias de carregamento automático e plug-in</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-modulemanager.git">laminas/laminas-modulemanager</a>
    </td>
    <td>biblioteca</td>
    <td>Sistema modular de aplicativo para aplicativos laminas-mvc</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-mvc.git">laminas/laminas-mvc</a>
    </td>
    <td>biblioteca</td>
    <td>Camada MVC orientada por eventos do Laminas, incluindo aplicativos MVC, controladores e plug-ins</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-permissions-acl.git">laminas/laminas-permissions-acl</a>
    </td>
    <td>biblioteca</td>
    <td>Oferece uma implementação leve e flexível de ACL (Access Control List, lista de controle de acesso) para gerenciamento de privilégios</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-recaptcha.git">laminas/laminas-recaptcha</a>
    </td>
    <td>biblioteca</td>
    <td>Invólucro OOP para o serviço Web ReCaptcha</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-router.git">laminas/laminas-router</a>
    </td>
    <td>biblioteca</td>
    <td>Sistema de roteamento flexível para aplicativos DE HTTP e console</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-server.git">laminas/laminas-server</a>
    </td>
    <td>biblioteca</td>
    <td>Criar servidores de RPC baseados em reflexão</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-servicemanager.git">laminas/laminas-servicemanager</a>
    </td>
    <td>biblioteca</td>
    <td>Contêiner de injeção de dependência orientada pela fábrica</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-session.git">laminas/laminas-session</a>
    </td>
    <td>biblioteca</td>
    <td>Interface orientada a objetos para sessões e armazenamento em PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-soap.git">laminas/laminas-soap</a>
    </td>
    <td>biblioteca</td>
    <td></td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-stdlib.git">laminas/laminas-stdlib</a>
    </td>
    <td>biblioteca</td>
    <td>Extensões SPL, utilitários de matriz, manipuladores de erros e muito mais</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-text.git">texto laminas/laminas</a>
    </td>
    <td>biblioteca</td>
    <td>Criar FIGlets e tabelas baseadas em texto</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-translator.git">laminas/laminas-translator</a>
    </td>
    <td>biblioteca</td>
    <td>Interfaces para o componente tradutor de laminas-i18n</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-uri.git">laminas/laminas-uri</a>
    </td>
    <td>biblioteca</td>
    <td>Um componente que auxilia na manipulação e validação » Uniforme Identificadores de recursos (URIs)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-validator.git">laminas/laminas-validator</a>
    </td>
    <td>biblioteca</td>
    <td>Classes de validação para uma grande variedade de domínios e a capacidade de encadear validadores para criar critérios de validação complexos</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-view.git">laminas/laminas-visualização</a>
    </td>
    <td>biblioteca</td>
    <td>Suporte flexível visualização camada, fornecendo várias camadas visualização, auxiliares e muito mais</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/marc-mabe/php-enum.git">marc-mabe/php-enum</a>
    </td>
    <td>biblioteca</td>
    <td>Implementação simples e rápida de enumerações com PHP nativo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/nikic/PHP-Parser.git">nikic/php-parser</a>
    </td>
    <td>biblioteca</td>
    <td>Um analisador PHP escrito em PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpfui/recaptcha.git">phpfui/recaptcha</a>
    </td>
    <td>biblioteca</td>
    <td>O biblioteca do cliente para o reCAPTCHA do Google para PHP 8.4 e superior</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tedious/JShrink.git">tedivm/jshrink</a>
    </td>
    <td>biblioteca</td>
    <td>Javascript Minifier integrado em PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tubalmartin/YUI-CSS-compressor-PHP-port.git">tubalmartin/cssmin</a>
    </td>
    <td>biblioteca</td>
    <td>Um porta PHP do compressor YUI CSS</td>
  </tr>
  </tbody>
</table>

### Modificação de cláusula-BSD-3

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_Redis.git">colinmollenhour/cache-backend-redis</a>
    </td>
    <td>magento-módulo</td>
    <td>Zend_Cache backend usando Redis com suporte total para tags.</td>
  </tr>
  </tbody>
</table>

### ISC

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/paragonie/sodium_compat.git">paragonie/dium_compat</a>
    </td>
    <td>biblioteca</td>
    <td>Implementação PHP pura de libsódio; usa a extensão PHP se ela existir</td>
  </tr>
  </tbody>
</table>

### LGPL-2.1 ou posterior

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/ezyang/htmlpurifier.git">ezyang/htmlpurifier</a>
    </td>
    <td>biblioteca</td>
    <td>Filtro HTML compatível com padrões escrito em PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-amqplib/php-amqplib.git">php-amqplib/php-amqplib</a>
    </td>
    <td>biblioteca</td>
    <td>Anteriormente videlalvaro/php-amqplib.  Esta biblioteca é uma implementação PHP pura do protocolo AMQP. Foi testado contra RabbitMQ.</td>
  </tr>
  </tbody>
</table>

### MIT

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/braintree/braintree_php.git">braintree/braintree_php</a>
    </td>
    <td>biblioteca</td>
    <td>Biblioteca cliente PHP Braintree</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/math.git">brick/math</a>
    </td>
    <td>biblioteca</td>
    <td>Biblioteca aritmética de precisão arbitrária</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/varexporter.git">exportador/brick</a>
    </td>
    <td>biblioteca</td>
    <td>Uma alternativa poderosa para var_export(), que pode exportar fechamentos e objetos sem __set_state()</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ChristianRiesen/base32.git">christian-riesen/base32</a>
    </td>
    <td>biblioteca</td>
    <td>Codificador/decodificador Base32 de acordo com RFC 4648</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/credis.git">colinmollenhour/credis</a>
    </td>
    <td>biblioteca</td>
    <td>O Credis é uma interface leve para o valor principal Redis armazenamento que vincula os phpredis biblioteca quando disponíveis para melhor desempenho.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/ca-bundle.git">composer/ca-pacote</a>
    </td>
    <td>biblioteca</td>
    <td>Permite encontrar um caminho para o sistema de pacote da CA e inclui um fallback para o pacote da CA Mozilla.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/class-map-generator.git">composer/class-map-generator</a>
    </td>
    <td>biblioteca</td>
    <td>Utilitários para escanear o código PHP e gerar mapas de classe.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/composer.git">composer/compositor</a>
    </td>
    <td>biblioteca</td>
    <td>O Composer ajuda você a declarar, gerenciar e instalar dependências de projetos PHP. Isso garante que você tenha a pilha certa em todos os lugares.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/metadata-minifier.git">composer/metadados-minifier</a>
    </td>
    <td>biblioteca</td>
    <td>Pequena utilidade biblioteca que lida com minificação e expansão metadados.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/pcre.git">compositor/pcre</a>
    </td>
    <td>biblioteca</td>
    <td>Biblioteca de encapsulamento PCRE que oferece substituições preg_* seguras para tipos.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/semver.git">compositor/semver</a>
    </td>
    <td>biblioteca</td>
    <td>Biblioteca de servidor que oferece utilitários, análise de restrição de versão e validação.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/spdx-licenses.git">composer/spdx-licenses</a>
    </td>
    <td>biblioteca</td>
    <td>Licenças SPDX lista e validação biblioteca.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/xdebug-handler.git">composer/xdebug-handler</a>
    </td>
    <td>biblioteca</td>
    <td>Reinicia um processo sem Xdebug.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/doctrine/lexer.git">doutrina/lexer</a>
    </td>
    <td>biblioteca</td>
    <td>Biblioteca de analisadores Lexer de Doutrina PHP que pode ser usada em Analisadores Descendentes Recursivos.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/egulias/EmailValidator.git">guias/validador de email</a>
    </td>
    <td>biblioteca</td>
    <td>Uma biblioteca para validar emails em relação a vários RFCs</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elastic-transport-php.git">elástico/transporte</a>
    </td>
    <td>biblioteca</td>
    <td>Biblioteca PHP de transporte HTTP para produtos Elastic</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elasticsearch-php.git">elasticsearch/elasticsearch</a>
    </td>
    <td>biblioteca</td>
    <td>Cliente PHP para Elasticsearch</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/endroid/qr-code.git">endroid/qr-code</a>
    </td>
    <td>biblioteca</td>
    <td>Código QR Endroid</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/guzzlestreams.git">ezimuel/guzzlestreams</a>
    </td>
    <td>biblioteca</td>
    <td>Bifurcação de garoa/transmissões (abandonada) para ser usada com elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/ringphp.git">ezimuel/ringphp</a>
    </td>
    <td>biblioteca</td>
    <td>Bifurcação de guzzle/RingPHP (abandonado) para ser usado com elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/guzzle.git">guzzlehttp/guzzle</a>
    </td>
    <td>biblioteca</td>
    <td>Guzzle é um cliente PHP HTTP biblioteca</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/promises.git">guzzlehttp/promessas</a>
    </td>
    <td>biblioteca</td>
    <td>Guzzle promete biblioteca</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/psr7.git">guzzlehttp/psr7</a>
    </td>
    <td>biblioteca</td>
    <td>Implementação de mensagem PSR-7 que também fornece métodos comuns de utilitários</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jsonrainbow/json-schema.git">justinarco-íris/json-schema</a>
    </td>
    <td>biblioteca</td>
    <td>Um biblioteca para validar um schema json.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem.git">liga/flysystem</a>
    </td>
    <td>biblioteca</td>
    <td>Abstração de armazenamento de arquivo para PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-aws-s3-v3.git">liga/flysystem-aws-s3-v3</a>
    </td>
    <td>biblioteca</td>
    <td>Adaptador de sistema de arquivos AWS S3 para Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-local.git">liga/flysystem-local</a>
    </td>
    <td>biblioteca</td>
    <td>Adaptador de sistema de arquivos local para Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/mime-type-detection.git">league/mime-type-detection</a>
    </td>
    <td>biblioteca</td>
    <td>Detecção de tipo MIME para Flysystem</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/monolog.git">monólogo/monólogo</a>
    </td>
    <td>biblioteca</td>
    <td>Envia seus registros para arquivos, soquetes, caixas de entrada, bancos de dados e vários serviços da Web</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jmespath/jmespath.php.git">mtdowling/jmespath.php</a>
    </td>
    <td>biblioteca</td>
    <td>Especificar declarativamente como extrair elementos de um documento JSON</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/constant_time_encoding.git">paragonie/constant_time_encoding</a>
    </td>
    <td>biblioteca</td>
    <td>Implementações de tempo constante da codificação RFC 4648 (Base-64, Base-32, Base-16)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/random_compat.git">paragonie/random_compat</a>
    </td>
    <td>biblioteca</td>
    <td>PHP 5.x polyfill para random_bytes() e random_int() do PHP 7</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/emogrifier.git">pelago/emotificador</a>
    </td>
    <td>biblioteca</td>
    <td>Converte estilos CSS em atributos de estilo em linha no seu código HTML</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/discovery.git">php-http/discovery</a>
    </td>
    <td>composer-plugin</td>
    <td>Localiza e instala implementações PSR-7, PSR-17, PSR-18 e HTTPlug</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/httplug.git">php-http/httplug</a>
    </td>
    <td>biblioteca</td>
    <td>HTTPlug, a abstração do cliente HTTP para PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/promise.git">php-http/promessa</a>
    </td>
    <td>biblioteca</td>
    <td>Promessa usada para solicitações HTTP assíncronas</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/CssXPath.git">phpgt/cssxpath</a>
    </td>
    <td>biblioteca</td>
    <td>Converta seletores de CSS em consultas XPath.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/Dom.git">phpgt/dom</a>
    </td>
    <td>biblioteca</td>
    <td>API DOM moderna.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/PropFunc.git">phpgt/propfunc</a>
    </td>
    <td>biblioteca</td>
    <td>Funções do acessador de propriedades e mutador.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/mcrypt_compat.git">phpseclib/mcrypt_compat</a>
    </td>
    <td>biblioteca</td>
    <td>polyfill do PHP 5.x-8.x para extensão mcrypt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/phpseclib.git">phpseclib/phpseclib</a>
    </td>
    <td>biblioteca</td>
    <td>Biblioteca de comunicações seguras PHP - implementações de PHP puro de RSA, AES, SSH2, SFTP, X.509 etc.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/cache.git">psr/cache</a>
    </td>
    <td>biblioteca</td>
    <td>Interface comum para o armazenamento em cache de bibliotecas</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/clock.git">psr/clock</a>
    </td>
    <td>biblioteca</td>
    <td>Interface comum para a leitura do relógio.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/container.git">psr/container</a>
    </td>
    <td>biblioteca</td>
    <td>Interface comum de contêiner (PHP FIG PSR-11)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/event-dispatcher.git">psr/event-dispatcher</a>
    </td>
    <td>biblioteca</td>
    <td>Interfaces padrão para manipulação de eventos.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-client.git">psr/http-client</a>
    </td>
    <td>biblioteca</td>
    <td>Interface comum para clientes HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-factory.git">psr/http-fatory</a>
    </td>
    <td>biblioteca</td>
    <td>PSR-17: interfaces comuns para fábricas de mensagens HTTP PSR-7</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-message.git">psr/http-message</a>
    </td>
    <td>biblioteca</td>
    <td>Interface comum para mensagens HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/log.git">psr/log</a>
    </td>
    <td>biblioteca</td>
    <td>Interface comum para bibliotecas de registro</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ralouphie/getallheaders.git">ralouphie/getallheaders</a>
    </td>
    <td>biblioteca</td>
    <td>Um polyfill para getallheaders.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/collection.git">ramsey/coleção</a>
    </td>
    <td>biblioteca</td>
    <td>Um biblioteca PHP para representar e manipular coleções.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/uuid.git">ramsey/uuid</a>
    </td>
    <td>biblioteca</td>
    <td>Uma biblioteca PHP para geração e trabalho com identificadores universalmente exclusivos (UUIDs).</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/reactphp/promise.git">reação/promessa</a>
    </td>
    <td>biblioteca</td>
    <td>Uma implementação leve de promessas/A do CommonJS para PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/PHP-CSS-Parser.git">sabberworm/php-css-parser</a>
    </td>
    <td>biblioteca</td>
    <td>Analisador para arquivos CSS escritos em PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/jsonlint.git">seld/jsonlint</a>
    </td>
    <td>biblioteca</td>
    <td>Linter JSON</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/phar-utils.git">seld/phar-utils</a>
    </td>
    <td>biblioteca</td>
    <td>utilitários de formato de arquivo PHAR, para quando o PHP lhe mostrar</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/signal-handler.git">seld/manipulador de sinal</a>
    </td>
    <td>biblioteca</td>
    <td>Manipulador simples de sinais Unix que falha silenciosamente quando os sinais não são suportados para um fácil desenvolvimento entre plataformas</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/aes-key-wrap.git">spomky-labs/aes-key-wrap</a>
    </td>
    <td>biblioteca</td>
    <td>Encapsulamento de chave AES para PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/otphp.git">spomky-labs/otphp</a>
    </td>
    <td>biblioteca</td>
    <td>Uma biblioteca PHP para gerar senhas únicas de acordo com RFC 4226 (algoritmo HOTP) e RFC 6238 (algoritmo TOTP) e compatível com o Google Authenticator</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/pki-framework.git">spomky-labs/pki-framework</a>
    </td>
    <td>biblioteca</td>
    <td>Uma estrutura PHP para gerenciamento da Infraestrutura de Chave Pública. Ele inclui certificados de chave pública X.509, certificados de atributo, solicitações de certificação e validação do caminho de certificação.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/config.git">symfony/config</a>
    </td>
    <td>biblioteca</td>
    <td>Ajuda a localizar, carregar, combinar, preencher automaticamente e validar valores de configuração de qualquer tipo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/console.git">symfony/console</a>
    </td>
    <td>biblioteca</td>
    <td>Facilita a criação de interfaces de linha de comando belas e testáveis</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/css-selector.git">symfony/css-seletor</a>
    </td>
    <td>biblioteca</td>
    <td>Converte seletores CSS em expressões XPath</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/dependency-injection.git">injeção de symfony/dependência</a>
    </td>
    <td>biblioteca</td>
    <td>Permite padronizar e centralizar a forma como os objetos são construídos em suas aplicativo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/deprecation-contracts.git">symfony/deprecation-contracts</a>
    </td>
    <td>biblioteca</td>
    <td>Uma função e convenção genéricas para acionar avisos de substituição</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/error-handler.git">symfony/error-handler</a>
    </td>
    <td>biblioteca</td>
    <td>Fornece ferramentas para gerenciar erros e facilitar a depuração do código PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher.git">symfony/event-dispatcher</a>
    </td>
    <td>biblioteca</td>
    <td>Fornece ferramentas que permitem que os componentes do aplicativo se comuniquem entre si despachando eventos e ouvindo-os</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher-contracts.git">symfony/event-dispatcher-contracts</a>
    </td>
    <td>biblioteca</td>
    <td>Abstrações genéricas relacionadas ao evento de despacho</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/filesystem.git">symfony/filesystem</a>
    </td>
    <td>biblioteca</td>
    <td>Fornece utilitários básicos para o sistema de arquivos</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/finder.git">symfony/finder</a>
    </td>
    <td>biblioteca</td>
    <td>Localiza arquivos e diretórios por meio de uma interface intuitiva e fluente</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client.git">symfony/http-client</a>
    </td>
    <td>biblioteca</td>
    <td>Fornece métodos avançados para buscar recursos HTTP de forma síncrona ou assíncrona</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client-contracts.git">symfony/http-client-contracts</a>
    </td>
    <td>biblioteca</td>
    <td>Abstraçãos genéricas relacionadas a clientes HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-foundation.git">symfony/http-foundation</a>
    </td>
    <td>biblioteca</td>
    <td>Define uma camada orientada a objetos para a especificação HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-kernel.git">symfony/http-kernel</a>
    </td>
    <td>biblioteca</td>
    <td>Fornece um processo estruturado para converter uma solicitação em uma resposta</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/intl.git">symfony/intl</a>
    </td>
    <td>biblioteca</td>
    <td>Fornece acesso aos dados localização da UI biblioteca</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mailer.git">symfony/mailer</a>
    </td>
    <td>biblioteca</td>
    <td>Ajuda a enviar emails</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mime.git">symfony/mime</a>
    </td>
    <td>biblioteca</td>
    <td>Permite manipular mensagens MIME</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-ctype.git">symfony/polyfill-ctype</a>
    </td>
    <td>biblioteca</td>
    <td>Polyfill Symfony para funções ctype</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-grapheme.git">symfony/polyfill-intl-grapheme</a>
    </td>
    <td>biblioteca</td>
    <td>Polifill symfony para funções grapheme_* da intl</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-idn.git">symfony/polyfill-intl-idn</a>
    </td>
    <td>biblioteca</td>
    <td>polyfill Symfony para as funções idn_to_ascii e idn_to_utf8 da intl</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-normalizer.git">symfony/polyfill-intl-normalizer</a>
    </td>
    <td>biblioteca</td>
    <td>Symfony polyfill para a classe Normalizer da intl e funções relacionadas</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-mbstring.git">symfony/polyfill-mbstring</a>
    </td>
    <td>biblioteca</td>
    <td>Preenchimento múltiplo Symfony para a extensão Mbstring</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php73.git">symfony/polyfill-php73</a>
    </td>
    <td>biblioteca</td>
    <td>Symfony polyfill reforçando alguns recursos do PHP 7.3+ para versões mais baixas do PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php80.git">symfony/polyfill-php80</a>
    </td>
    <td>biblioteca</td>
    <td>Symfony polyfill reforçando alguns recursos do PHP 8.0+ para versões mais baixas do PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php81.git">symfony/polyfill-php81</a>
    </td>
    <td>biblioteca</td>
    <td>Symfony polyfill reforçando alguns recursos do PHP 8.1+ para versões mais baixas do PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php82.git">symfony/polyfill-php82</a>
    </td>
    <td>biblioteca</td>
    <td>Symfony polyfill reforçando alguns recursos do PHP 8.2+ para versões mais baixas do PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php83.git">symfony/polyfill-php83</a>
    </td>
    <td>biblioteca</td>
    <td>Suporte polifill symfony com alguns recursos PHP 8.3+ para versões PHP mais baixas</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/process.git">symfony/processo</a>
    </td>
    <td>biblioteca</td>
    <td>Executa comandos em subprocessos</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/service-contracts.git">symfony/service-contracts</a>
    </td>
    <td>biblioteca</td>
    <td>Abstrações genéricas relacionadas com serviços de escrita</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/string.git">symfony/string</a>
    </td>
    <td>biblioteca</td>
    <td>Fornece uma API orientada a objetos para strings e lida com bytes, pontos de código UTF-8 e clusters de grapheme de forma unificada</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-dumper.git">symfony/var-dumper</a>
    </td>
    <td>biblioteca</td>
    <td>Fornece mecanismos para percorrer qualquer variável PHP arbitrária</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-exporter.git">symfony/var-exporter</a>
    </td>
    <td>biblioteca</td>
    <td>Permite exportar qualquer estrutura de dados PHP serializável para código PHP simples</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/yaml.git">symfony/yaml</a>
    </td>
    <td>biblioteca</td>
    <td>Carrega e despeja arquivos YAML</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/web-token/jwt-framework.git">web-token/jwt-estrutura</a>
    </td>
    <td>pacote-sínfona</td>
    <td>Assinatura de objeto JSON e biblioteca de criptografia para PHP e Pacote Symfony.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webonyx/graphql-php.git">webonyx/graphql-php</a>
    </td>
    <td>biblioteca</td>
    <td>Uma porta PHP da implementação de referência do GraphQL</td>
  </tr>
  </tbody>
</table>

### OSL-3.0, AFL-3.0

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-customer-balance
    </td>
    <td>magento2-module</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-vale-presente
    </td>
    <td>magento2-module</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-vale-presente-conta
    </td>
    <td>magento2-module</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-present-wrapping
    </td>
    <td>magento2-module</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-graph-ql
    </td>
    <td>magento2-module</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-award
    </td>
    <td>magento2-module</td>
    <td>N/D</td>
  </tr>
  </tbody>
</table>

### OSL-3.0

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### PHP

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/2tvenom/CBOREncode.git">2tvenom/cborencode</a>
    </td>
    <td>biblioteca</td>
    <td>Codificador CBOR para PHP</td>
  </tr>
  </tbody>
</table>

### Proprietário

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### proprietário

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-core
    </td>
    <td>magento2-module</td>
    <td>Bifurcação do módulo Magento Braintree 2.2.0 de Gene Commerce para PayPal.</td>
  </tr>
  </tbody>
</table>
