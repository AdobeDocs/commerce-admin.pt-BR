---
title: 'Instalar a extensão  [!DNL Adobe Commerce B2B] '
description: Saiba como instalar o  [!DNL Adobe Commerce B2B] metapackage.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 25964363ca5c4ec849e231d4eccb5f60b682a499
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# Instalar a extensão [!DNL Adobe Commerce B2B]

A extensão B2B do Adobe Commerce `magento/extension-b2b` está disponível para todas as versões do Adobe Commerce com suporte. Ele é instalado após a instalação do Adobe Commerce.


## Requisitos

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html), todas as versões com suporte
- PHP 8.1, 8.2 e 8.3 (requer B2B 1.5.0)
- [!DNL Composer]

>[!IMPORTANT]
>
>O Adobe Commerce B2B versão 1.4.2+ não é compatível com o PHP 8.3. Se você atualizar a instância do Commerce para o Commerce versão 2.4.7+, certifique-se de que a versão do PHP instalada na instância é o PHP 8.2 para manter a compatibilidade com B2B 1.4.2+.

## Plataformas compatíveis

- Adobe Commerce na infraestrutura em nuvem (ECE)
- Adobe Commerce no local (EE)

## Etapas de instalação

>[!BEGINSHADEBOX]

**Pré-requisitos**

- Acesse [repo.magento.com](https://repo.magento.com/) para baixar a extensão. Para geração de chaves e obtenção dos direitos necessários, consulte [Obter suas chaves de autenticação](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Salve as chaves de autenticação para instalação definindo-as globalmente no diretório [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home). Ou salve-os em um arquivo [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) no diretório raiz do aplicativo Adobe Commerce.

- [Versão com suporte da extensão B2B](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/release/product-availability)-Determine a versão mais recente da extensão B2B com suporte na versão do Adobe Commerce implantada.

- Verifique as notas de versão para obter as informações mais atuais sobre compatibilidade de versão, atualizações ou alterações que podem afetar os requisitos de instalação ou atualização.

   - [Notas de versão B2B](release-notes.md)
   - [Notas de versão do Adobe Commerce](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Instale a extensão B2B (`magento/b2b-extension`) usando o Composer. A extensão é um metapackage de compositor que inclui a coleção de módulos que habilitam os recursos B2B para uma instância do Adobe Commerce. Para obter uma lista de módulos incluídos, consulte [Pacotes B2B](packages.md).

>[!BEGINTABS]

>[!TAB Infraestrutura em nuvem]

>[!TIP]
>
>Ao instalar o Adobe Commerce B2B na infraestrutura em nuvem, a Adobe recomenda que você implante seu aplicativo do Adobe Commerce em uma integração ou ambiente de preparo antes de começar.

A Adobe recomenda trabalhar em uma ramificação de desenvolvimento ao adicionar a extensão B2B ao projeto. Se você não tiver uma ramificação, consulte [Criar uma ramificação para desenvolvimento](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/develop/cli-branches). Ao instalar a extensão B2B, o nome da extensão `Magento_B2b` é inserido automaticamente no arquivo `app/etc/config.php`. Não há necessidade de editar o arquivo diretamente.

**Para instalar a extensão B2B**:

1. Na estação de trabalho local, altere para o diretório do projeto.

1. Criar ou dar baixa em uma ramificação de desenvolvimento.

1. Adicione a extensão B2B à seção `require` do arquivo `composer.json`.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Atualize as dependências do projeto.

   ```bash
   composer update
   ```

1. Adicionar, confirmar e enviar alterações de código.

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >Enviar atualizações para o ambiente de nuvem inicia o processo de implantação da nuvem do Commerce para aplicar as alterações. Verifique o status da implantação no [log de implantação](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/develop/deploy/process). Se você encontrar erros de implantação, consulte [Recuperar de falha de componente](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Após a conclusão da build e implantação, use o SSH para fazer logon no ambiente remoto e verificar se a extensão B2B está instalada e ativada.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Um nome de extensão usa o formato: `<VendorName>_<ComponentName>`.

   Exemplo de resposta:

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB No local]

1. No diretório raiz do aplicativo Adobe Commerce, atualize o `composer.json` para adicionar as dependências da extensão B2B:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Se ocorrer um erro, por exemplo:

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Verifique a ortografia do pacote, a restrição de versão e se o pacote está disponível e corresponde ao requisito de estabilidade mínima (estável).

1. Se solicitado, insira suas [chaves de autenticação](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

   Sua _chave pública_ é seu nome de usuário; sua _chave privada_ é sua senha. Se você tiver armazenado suas chaves públicas e privadas no `auth.json`, não será solicitado a autenticar.

1. Execute os seguintes comandos depois que o Composer terminar de atualizar os módulos:

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >No modo de Produção, você pode receber uma mensagem para `Please rerun Magento compile command`. Digite os comandos para concluir a instalação. A Adobe Commerce não solicita que você execute o comando compilar no modo de Desenvolvedor.

>[!ENDTABS]

Após concluir a instalação, configure e inicie os consumidores de mensagens.

## Consumidores de mensagens

A extensão B2B do Adobe Commerce usa MySQL para gerenciamento de fila de mensagens. A tabela a seguir lista os consumidores de mensagem que oferecem suporte aos recursos B2B. Depois de instalar a extensão, inicie os consumidores de mensagem para os recursos B2B necessários para sua loja da Commerce.

| Consumidor | Descrição |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Atualiza o preço de cada produto em um catálogo compartilhado. Necessário quando a opção [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está habilitada nas configurações do Sistema de Administração. |
| `sharedCatalogUpdateCategoryPermissions` | Atualiza categorias atribuídas a uma categoria de catálogo compartilhado. Necessário quando a opção [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está habilitada nas configurações do Sistema de Administração. |
| `negotiableQuotePriceUpdate` | Atualiza preços para cotações negociáveis. Necessário quando a opção [**[!UICONTROL Quotes]**](quotes.md) está habilitada nas configurações do Sistema de Administração. |
| `purchaseorder.toorder` | Converte ordem de compra em ordem. Necessário quando a opção [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está habilitada nas configurações do Sistema de Administração. |
| `purchaseorder.transactional.email` | Envie emails de ordem de compra. Necessário quando a opção [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está habilitada nas configurações do Sistema de Administração. |
| `purchaseorder.validation` | Valida a ordem de compra em relação às [regras de aprovação](account-dashboard-approval-rules.md) relevantes. Necessário quando a opção [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está habilitada nas configurações do Sistema de Administração. |
| `quoteItemCleaner` | Exclui cotações de preço inválidas ou inativas quando um produto é excluído do catálogo ou removido do carrinho. Necessário quando a opção [**[!UICONTROL Quotes]**](quotes.md) está habilitada nas configurações do Sistema de Administração. |
| `inventoryQtyCounter` | Corrige de forma assíncrona o índice de estoque depois que um pedido é feito ou um produto é removido. Necessário quando a opção [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) está habilitada para o Inventory management nas definições de configuração de Administração. Consulte [Práticas recomendadas de desempenho](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Cria mensagens para cada tarefa individual de uma [operação em massa](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), como importar ou exportar itens, alterar preços em uma escala em massa e atribuir produtos a um depósito. Necessário quando a opção [**Operações em massa do administrador**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) para [!DNL Inventory Management] está definida como **Executar de forma assíncrona** nas definições de configuração do Sistema de Administração. |

{style="table-layout:auto"}

>[!NOTE]
>
>Para obter uma lista de todos os consumidores de mensagens do Adobe Commerce, consulte [Consumidores da fila de mensagens](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/configuration-guide/message-queues/consumers) no _Guia de Configuração_.

### Configurar consumidores de mensagem

Evite possíveis problemas de processamento ou atrasos adicionando os seguintes parâmetros quando você [iniciar os consumidores de mensagens](#start-message-consumers) para recursos B2B.

- `--max-messages <value>`— Especifica o número máximo de mensagens que cada consumidor deve processar antes de terminar (padrão = 10000). Embora a Adobe não o recomende, você pode usar 0 para impedir que o consumidor encerre. A prática recomendada para um aplicativo PHP é reiniciar processos de longa execução para evitar possíveis vazamentos de memória.

- `--batch-size <value>`— Permite limitar os recursos do sistema consumidos pelos consumidores (CPU, memória). Usar lotes menores reduz o uso de recursos e, portanto, resulta em um processamento mais lento.  Se especificado, as mensagens em uma fila serão consumidas em lotes de `<value>` cada. Essa opção é aplicável somente para o consumidor do lote. Se `--batch-size` não estiver definido, o consumidor do lote receberá todas as mensagens disponíveis em uma fila.

Para obter informações sobre opções de configuração adicionais, consulte [Configuração-específica](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues?lang=pt-BR#specific-configuration).

### Iniciar consumidores de mensagem

Para habilitar operações assíncronas para recursos B2B, você deve iniciar vários consumidores de mensagem.

1. Listar os consumidores de mensagem disponíveis:

   ```bash
   bin/magento queue:consumers:list
   ```

   O comando retorna os consumidores de mensagens disponíveis, incluindo todos os [consumidores de mensagens B2B](#message-consumers).

1. Inicie cada consumidor separadamente:

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   Por exemplo:

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>Para executá-lo em segundo plano, anexe `&` ao comando, retorne a um prompt e continue executando os comandos. Por exemplo: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Para obter mais informações, consulte [Gerenciar filas de mensagens](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) no _Guia de Configuração_.

### Adicionar consumidores de mensagem ao cron

Você pode automatizar o agendamento de execução para os consumidores de mensagens `SharedCatalogUpdateCategoryPermissions` e `SharedCatalogUpdatePrice` adicionando o agendamento ao arquivo de configuração cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Você também pode definir agendas para consumidores de mensagens nas [Configurações de armazenamento](../systems/cron.md) em Admin.

## Habilitar recursos B2B no Administrador

Depois de instalar a extensão B2B do Adobe Commerce e iniciar os consumidores de mensagens, você também deve [habilitar os recursos B2B no Administrador](enable-basic-features.md).

