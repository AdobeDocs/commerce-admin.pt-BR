---
title: Instale o [!DNL B2B for Adobe Commerce] extensão
description: Saiba como instalar o [!DNL B2B for Adobe Commerce] metapackage.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: e57aa4e8919c2de5341c4b8363197d6380bbb0f6
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 0%

---


# Instale o [!DNL B2B for Adobe Commerce] extensão

A extensão B2B para Adobe Commerce só está disponível para o Adobe Commerce v2.2.0 ou posterior. Ele é instalado após a instalação do Adobe Commerce.

Instale a versão mais recente da extensão B2B que é compatível com a versão do Adobe Commerce implantada.

>[!NOTE]
>
>Essas instruções de instalação se aplicam ao Adobe Commerce implantado no local. Para instalar a extensão B2B para projetos do Commerce implantados na infraestrutura em nuvem, consulte o [Guia de infraestrutura do Commerce Cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## Requisitos

- Adobe Commerce versão 2.3.x ou posterior
- [Versão compatível da extensão B2B](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- Válido [chaves de autenticação](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) para baixar as extensões do Adobe Commerce.

  Salve as chaves de autenticação para instalação definindo-as globalmente em seu [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) diretório. Ou salve-os em um [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) no diretório raiz do aplicativo Adobe Commerce.

Antes de instalar ou atualizar a extensão B2B, verifique as notas de versão para obter as informações mais atuais sobre compatibilidade de versão, atualizações ou alterações que podem afetar os requisitos de instalação ou atualização.

- [Notas de versão B2B](release-notes.md)
- [Notas de versão do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## Etapas de instalação

1. No diretório raiz do aplicativo do Adobe Commerce, atualize o `composer.json` para adicionar as dependências da extensão B2B:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Se ocorrer um erro, por exemplo:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Verifique a ortografia do pacote, a restrição de versão e se o pacote está disponível e corresponde ao requisito de estabilidade mínima (estável).

1. Se solicitado, insira o [chaves de autenticação](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   Seu _chave pública_ é seu nome de usuário; seu _chave privada_ é sua senha. Se você armazenou suas chaves públicas e privadas no `auth.json`, você não receberá uma solicitação para autenticar.

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

Após concluir a instalação, configure e inicie os consumidores de mensagens, incluindo [especificação de parâmetros para consumidores de mensagem](#configure-message-consumers).

## Consumidores de mensagens

A extensão B2B para Adobe Commerce usa MySQL para gerenciamento de fila de mensagens. A tabela a seguir lista os consumidores de mensagem que oferecem suporte aos recursos B2B. Depois de instalar a extensão, inicie os consumidores de mensagem para os recursos B2B necessários para sua loja do Commerce.

| Consumidor | Descrição |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Atualiza o preço de cada produto em um catálogo compartilhado. Obrigatório quando a variável [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está habilitada nas configurações do Admin System. |
| `sharedCatalogUpdateCategoryPermissions` | Atualiza categorias atribuídas a uma categoria de catálogo compartilhado. Obrigatório quando a variável [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está habilitada nas configurações do Admin System. |
| `negotiableQuotePriceUpdate` | Atualiza preços para cotações negociáveis. Obrigatório quando a variável [**[!UICONTROL Quotes]**](quotes.md) está habilitada nas configurações do Admin System. |
| `purchaseorder.toorder` | Converte ordem de compra em ordem. Obrigatório quando a variável [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está habilitada nas configurações do Admin System. |
| `purchaseorder.transactional.email` | Envie emails de ordem de compra. Obrigatório quando a variável [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está habilitada nas configurações do Admin System. |
| `purchaseorder.validation` | Valida a ordem de compra em relação aos itens relevantes [regras de aprovação](account-dashboard-approval-rules.md). Obrigatório quando a variável [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está habilitada nas configurações do Admin System. |
| `quoteItemCleaner` | Exclui cotações de preço inválidas ou inativas quando um produto é excluído do catálogo ou removido do carrinho. Obrigatório quando a variável [**[!UICONTROL Quotes]**](quotes.md) está habilitada nas configurações do Admin System. |
| `inventoryQtyCounter` | Corrige de forma assíncrona o índice de estoque depois que um pedido é feito ou um produto é removido. Obrigatório quando a variável [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) está ativada para o Inventory management nas configurações de Admin. Consulte [Práticas recomendadas de desempenho](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | Cria mensagens para cada tarefa individual de um [operação em massa](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), como importar ou exportar itens, alterar preços em uma escala em massa e atribuir produtos a um depósito. Obrigatório quando a variável [**Operações em massa do administrador**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) opção para [!DNL Inventory Management] está definida como **Executar de forma assíncrona** nas configurações do sistema Admin. |

{style="table-layout:auto"}

>[!NOTE]
>
>Para obter uma lista de todos os consumidores de mensagens do Adobe Commerce, consulte [Consumidores da fila de mensagens](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) no _Guia de configuração_.

### Configurar consumidores de mensagem

Evite possíveis problemas de processamento ou atrasos adicionando os seguintes parâmetros quando você [iniciar os consumidores de mensagem](#start-message-consumers) para recursos B2B.

- `--max-messages <value>`— Especifica o número máximo de mensagens que cada consumidor deve processar antes de terminar (padrão = 10000). Embora não o recomendemos, você pode usar 0 para impedir que o consumidor seja encerrado. A prática recomendada para um aplicativo PHP é reiniciar processos de longa execução para evitar possíveis vazamentos de memória.

- `--batch-size <value>`— Permite limitar os recursos do sistema consumidos pelos consumidores (CPU, memória). Usar lotes menores reduz o uso de recursos e, portanto, resulta em um processamento mais lento.  Se especificadas, as mensagens em uma fila serão consumidas em lotes de `<value>` cada. Essa opção é aplicável somente para o consumidor do lote. Se `--batch-size` não estiver definido, o consumidor em lote receberá todas as mensagens disponíveis em uma fila.

Para obter informações sobre opções de configuração adicionais, consulte [Configuração específica](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

### Iniciar consumidores de mensagem

Para habilitar operações assíncronas para recursos B2B, você deve iniciar vários consumidores de mensagem.

1. Listar os consumidores de mensagem disponíveis:

   ```bash
   bin/magento queue:consumers:list
   ```

   O comando retorna os consumidores de mensagem disponíveis, incluindo todos [Consumidores de mensagem B2B](#message-consumers).

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

Para obter mais informações, consulte [Gerenciar filas de mensagens](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) no _Guia de configuração_.

### Adicionar consumidores de mensagem ao cron

Você tem a opção de automatizar a programação de execução para o `SharedCatalogUpdateCategoryPermissions` e `SharedCatalogUpdatePrice` consumidores de mensagem adicionando o agendamento ao arquivo de configuração cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Você também pode configurar agendas para consumidores de mensagens no [Configurações da loja](../systems/cron.md) em Admin.

## Habilitar recursos B2B no Administrador

Depois de instalar a extensão B2B para Adobe Commerce e iniciar os consumidores de mensagem, você também deve [ativar recursos B2B no Administrador](enable-basic-features.md).
