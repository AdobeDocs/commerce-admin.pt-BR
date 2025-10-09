---
title: '[!DNL Audience Activation]'
description: Saiba como ativar públicos-alvo da Real-Time CDP no Adobe Commerce para impulsionar a personalização em sua loja.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 5929a2ff26dadda40ecfa9e435a73343caef3cde
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 1%

---

# [!DNL Audience Activation]

A extensão [!DNL Audience Activation] permite ativar públicos-alvo da Real-Time CDP no Adobe Commerce para criar ofertas exclusivas no carrinho. Essas ofertas e incentivos incluem técnicas comuns de merchandising de comércio eletrônico, como _comprar 2 obter 1 grátis_, banners ilustrados voltados para esse cliente e preços de produtos modificados por meio de várias ofertas. Os públicos-alvo criados no Real-Time CDP são baseados em dados de vários sistemas corporativos, como ERP (Enterprise Resource Planning, planejamento de recursos corporativos), CRM (Customer Relationship Management, gerenciamento de relacionamento com o cliente), ponto de venda e sistemas de marketing. Como as informações de segmento do cliente são constantemente atualizadas, os clientes podem se tornar associados e desassociados de um segmento à medida que fazem compras em sua loja.

Você pode ativar públicos em uma loja Luma ou em uma loja [headless](#headless-support). Em uma loja Luma, as informações do público-alvo (associação de segmento) são armazenadas em um cookie no lado do Commerce. Em uma loja headless, as informações do público são passadas no cabeçalho da API do GraphQL como um parâmetro chamado: `aep-segments-membership`.

## Notas de versão

Esta seção contém informações sobre atualizações na extensão do Audience Activation e inclui:

![Novos](../assets/new.svg) - Novos recursos
![Correção](../assets/fix.svg) - Correções e melhorias
![Bug](../assets/bug.svg) - Problemas conhecidos

Consulte [Versões futuras](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para saber mais sobre os cronogramas de lançamento e o suporte.

Consulte a documentação do desenvolvedor para [saber mais sobre compatibilidade de produto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Atualizações de serviço compatíveis

Essas notas de versão descrevem alterações de recursos e correções relacionadas a extensões usadas pelo Audience Activation.

+++Atualizações de serviço compatíveis

_15 de agosto de 2023_

![Correção](../assets/fix.svg) - O [painel de Públicos-alvo do Real-Time CDP](#real-time-cdp-audiences-dashboard) foi atualizado para simplificar a filtragem.

_27 de junho de 2023_

![Correção](../assets/fix.svg) - Adição de suporte para PHP 8.2 no pacote `magento/module-data-services-graphql`.

_30 de maio de 2023_

![Novo](../assets/new.svg) - O [painel de Públicos-alvo da Real-Time CDP](#real-time-cdp-audiences-dashboard) foi atualizado para incluir a capacidade de classificar, pesquisar e filtrar os públicos-alvo ativos na sua instância do Adobe Commerce.

+++

### 2.4.0

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_24 de março de 2025_

![Novo](../assets/new.svg) - Adição de suporte ao PHP 8.4.

### 2.3.1

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_12 de novembro de 2024_

![Correção](../assets/fix.svg) - Corrigido um problema ao filtrar os públicos-alvo disponíveis do Real-Time CDP para escolher.

### 2.3.0

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_29 de julho de 2024_

![Novo](../assets/new.svg) - Sintaxe de linha de comando adicionada para que você possa [testar credenciais](#validate-the-connection) para determinar se elas precisam ser atualizadas para obter dados de público-alvo da Adobe Experience Platform.

### 2.2.0

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_12 de junho de 2024_

![Novo](../assets/new.svg) - Versão do GA para [regras de produto relacionadas](../merchandising-promotions/product-related-rule-create.md) informada por públicos.

### 2.1.1

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_4 de abril, 2024_

![Novo](../assets/new.svg) - Suporte adicionado para PHP 8.3.

### 2.2.0-beta1

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_16 de fevereiro de 2024_

![Novo](../assets/new.svg) - Se você estiver participando do beta, verifique se o arquivo `composer.json` tem o seguinte no nível raiz: ` "minimum-stability": "beta"`.
![Novo](../assets/new.svg) - (**Beta**) Adicionou a capacidade de criar [regras de produto relacionadas](../merchandising-promotions/product-related-rule-create.md) informadas pelos públicos-alvo.

### 2.1.0

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_24 de janeiro de 2024_

![Novo](../assets/new.svg) - O [painel de Públicos-alvo da Real-Time CDP](#real-time-cdp-audiences-dashboard) foi atualizado para incluir os sites que contêm os públicos-alvo e especificar quais blocos dinâmicos e regras de preço do carrinho estão configurados para usar esses públicos-alvo.

### 2.0.1

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_16 de novembro de 2023_

![Correção](../assets/fix.svg) - Estabilidade aprimorada.

### 2.0.0

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_10 de outubro de 2023_

![Novo](../assets/new.svg) - Adição de suporte para OAuth 2.0 ao [configurar](#configure-the-extension) a extensão do Audience Activation.
![Correção](../assets/fix.svg) - Estabilidade aprimorada.

### 1.2.0

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

_15 de agosto de 2023_

![Correção](../assets/fix.svg) - Atualização da versão dos componentes da interface do usuário.

### 1.1.0

_30 de maio de 2023_

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

![Novo](../assets/new.svg) - Suporte adicionado para [blocos dinâmicos](#headless-support) em uma loja headless.

### 1.0.1

_11 de maio de 2023_

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

![Correção](../assets/fix.svg) - Corrigido um problema no qual uma regra de preço de carrinho ou bloco dinâmico não era aplicada à loja.
![Correção](../assets/fix.svg) - Corrigido um problema no qual uma instalação não configurada da extensão do Audience Activation causava um erro quando um comerciante tentava criar ou atualizar um bloco dinâmico.

### 1.0.0

_31 de março de 2023_

[!BADGE Compatibilidade]{type=Informative tooltip="Compatibilidade"} Adobe Commerce versões 2.4.4 e mais recentes

![Novo](../assets/new.svg) - Versão de disponibilidade geral

## Implementação

As tarefas a seguir se aplicam às implementações do Luma e da loja headless. Para ativar públicos no Adobe Commerce, você deve:

- Instalar o Adobe Commerce versão 2.4.4 ou superior
- [Ativar](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) o Adobe Commerce como destino no Real-Time CDP
- [Instalar](#install-the-extension) a extensão [!DNL Audience Activation] no Administrador
- [Configurar](#configure-the-extension) a extensão [!DNL Audience Activation] no Administrador

### Instalar a extensão

Instale a extensão [!DNL Audience Activation] do [marketplace](https://commercemarketplace.adobe.com/magento-audiences.html) ou execute o seguinte comando:

```bash
composer require magento/audiences
```

### Configurar a extensão

Depois de instalar a extensão [!DNL Audience Activation], faça logon no Commerce Admin e conclua o seguinte:

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Entre](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html#organizationid) com sua conta da Adobe e selecione sua ID da organização.

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. No campo **[!UICONTROL Datastream ID]**, cole a ID da sequência de dados criada quando você [ativou](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) o Adobe Commerce como destino no Real-Time CDP.

   Essa sequência de dados envia dados do seu site da Commerce para a Real-Time CDP a fim de determinar se um comprador pertence a um público-alvo. Se você ainda não criou uma sequência de dados, [crie](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) no Experience Platform, [adicione](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) ao destino do Commerce no Real-Time CDP e à extensão [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection) no Administrador.

   >[!NOTE]
   >
   >Ao especificar uma ID de sequência de dados, você [associa a um site específico](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection) na extensão [!DNL Data Connection]. Se o seu armazenamento do Commerce tiver vários sites, [crie um destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) para cada site no Real-Time CDP e use uma ID de sequência de dados diferente para cada um.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expanda **[!UICONTROL Services]** e selecione **[!UICONTROL [!DNL Data Connection]]**.

1. [Adicionar](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) conta de serviço e detalhes da credencial.

## Onde usar os públicos-alvo da Real-Time CDP no Commerce

Com a extensão [!DNL Audience Activation] habilitada, você pode:

- [Criar uma regra de preço do carrinho](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) informada por públicos
- [Criar um bloco dinâmico](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) informado por públicos
- [Criar uma regra de produto relacionada](../merchandising-promotions/product-related-rule-create.md) informada por públicos

>[!TIP]
>
>Para obter um caso de uso completo sobre como exportar dados do [!DNL Commerce] para o Real-Time CDP, criar um público-alvo e depois ativá-lo para [!DNL Commerce], consulte [Criar um público-alvo no Real-Time CDP usando [!DNL Commerce] dados de eventos](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience).

## painel de públicos-alvo da Real-Time CDP

Você pode exibir todos os [públicos-alvo ativos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) que estão disponíveis para personalização na sua instância do Adobe Commerce usando o painel **Públicos-alvo da Real-Time CDP**.

Para acessar o painel **Públicos-alvo do Real-Time CDP**, vá para a barra lateral _Admin_ e, em seguida, vá para **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Painel de Públicos-Alvo do Real-Time CDP](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

O painel contém os seguintes campos:

| Coluna | Descrição |
|--- |--- |
| `Hide filters` | Permite mostrar ou ocultar os filtros que podem ser aplicados ao painel. Atualmente, o único filtro que você pode aplicar é `Last updated`. Esse filtro permite selecionar um intervalo de datas para públicos com base em quando foram atualizados pela última vez. |
| `Search` | Permite pesquisar públicos-alvo ativos na sua instância do Commerce. |
| `Name` | Nome dado ao público no Real-Time CDP. |
| `Origin` | Indica a origem do público-alvo, como `Experience Platform`. |
| `Websites` | Indica quais sites estão configurados para usar os públicos-alvo. |
| `Dynamic Blocks` | Indica quais blocos dinâmicos são configurados para usar os públicos-alvo. |
| `Cart Price Rules` | Indica quais regras de preço do carrinho estão configuradas para usar os públicos-alvo. |
| `Related Product Rules` | Indica quais regras de produto relacionadas são configuradas para usar os públicos. |
| `Last updated` | Indica quando o público-alvo foi modificado no Real-Time CDP. |
| `Sync now` | Recupera públicos novos ou atualizados da Real-Time CDP. |
| `Customize table` | Permite mostrar ou ocultar as colunas `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules` e `Last updated`. |

{style="table-layout:auto"}

## Suporte a headless

Você pode ativar públicos-alvo em uma instância do Adobe Commerce headless, como o AEM e o PWA, para exibir regras de preço do carrinho, regras de produto relacionadas ou blocos dinâmicos com base nos públicos-alvo.

### Regras de preço do carrinho e regras de produto relacionadas

Para regras de preço do carrinho e regras de produto relacionadas, uma loja headless se comunica com a Experience Platform por meio da [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). A estrutura fornece uma API do lado do servidor que é implementada usando o GraphQL. As informações de público, como o segmento de um comprador, são transmitidas para o Commerce por meio de um parâmetro de cabeçalho do GraphQL chamado: `aep-segments-membership`.

A arquitetura geral é a seguinte:

![Enviando Dados de Headless Storefront para Back-end](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Depois de [instalar](#install-the-extension) e [configurar](#configure-the-extension) a extensão, o Experience Platform Web SDK conterá as informações do público-alvo na forma de associação de segmento.

Para capturar essas associações de segmento da SDK, veja este [trecho de código](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Depois de recuperá-lo, você pode passar esses segmentos para o Commerce no cabeçalho do GraphQL. Por exemplo:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Blocos dinâmicos

Para blocos dinâmicos, as consultas `dynamicBlocks` do GraphQL podem conter o atributo de entrada `audience_id`. Se você especificar um ou mais valores `audience_id` em uma consulta `dynamicBlocks`, ela retorna uma lista de blocos dinâmicos atribuídos a esses públicos.

#### Exemplo de uso

A consulta a seguir retorna todos os blocos dinâmicos associados a várias IDs de público-alvo.

**Solicitação:**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**Resposta:**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

Saiba mais sobre a consulta do GraphQL `dynamicBlocks` na [documentação para desenvolvedores](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Recuperar públicos-alvo usando o Adobe Experience Platform Mobile SDK

Você pode recuperar públicos da Real-Time CDP usando o Adobe Experience Platform Mobile SDK.

1. [Instalar](#install-the-extension) a extensão do Audience Activation.
1. [instale e configure o SDK para seu site do Commerce móvel](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>O Adobe Experience Platform Mobile SDK para iOS é compatível com o iOS 11 ou posterior.

Após concluir a configuração, use as operações móveis do SDK para recuperar os dados do público-alvo. Por exemplo:

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }
         
                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

Depois que os dados forem recuperados, você poderá usá-los para criar [regras de preço do carrinho](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [blocos dinâmicos](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) e [regras de produto relacionadas](../merchandising-promotions/product-related-rule-create.md) informadas pelo público-alvo no aplicativo Commerce.

## Os públicos-alvo não são exibidos no Commerce

Se os públicos-alvo da Real-Time CDP não estiverem sendo exibidos no Commerce, talvez seja devido a:

- Conexão inválida
- Tipo de autenticação incorreto selecionado na página de configuração **Conexão de Dados**
- Privilégios insuficientes no token gerado

As seções a seguir descrevem como solucionar esses problemas.

### Validar a conexão

Para validar as credenciais e a resposta do Adobe Experience Platform, execute o seguinte comando:

```bash
bin/magento audiences:config:status
```

Este comando retorna o status da conexão. Adicione o sinalizador `-v` para fornecer detalhamento extra:

```
./bin/magento audiences:config:status -v  
```

Por exemplo:

```
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| Client ID                        | Client secret | Technical account ID                        | Technical account email                                 | Sandbox name |
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| 1234bd57fac8497d8933327c535347d8 | *****         | 12341E116638D6B00A495C80@techacct.adobe.com | 12345-b95b-4894-a41c-a4130d26bd80@techacct.adobe.com | dev          |
```

### Tipo de autenticação incorreto selecionado na configuração

1. Abra a instância do Commerce.
1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Expanda **[!UICONTROL Services]** e selecione **[!UICONTROL [!DNL Data Connection]]**.
1. Verifique se o método de autorização servidor para servidor especificado no campo **[!UICONTROL Authentication Type]** está correto. A Adobe recomenda usar **OAuth**. O JWT foi descontinuado. [Saiba mais](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Privilégios insuficientes no token gerado

Esse problema pode ser causado por privilégios insuficientes de API para o token gerado. Para garantir que o token tenha os privilégios corretos:

1. Identifique o administrador de sistemas do Adobe Experience Platform em sua organização.
1. Encontre o projeto e as credenciais que você usará.
1. Identifique o email da conta técnica, por exemplo: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Peça ao administrador do sistema para iniciar o Adobe Experience Platform e acessar **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. Usando o email da conta técnica mencionado acima, procure as credenciais que serão modificadas.
1. Abra as credenciais e selecione **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. Adicione a função que contém a permissão **[!UICONTROL Manage destinations]**.
1. Clique em **[!UICONTROL Save]**.
1. [Regenerar](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) o token de acesso no Console.
1. Verifique se o token fornece uma resposta válida usando a [API de Conexões de Destino](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
