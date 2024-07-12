---
title: Configurar o serviço de sincronização
description: "Saiba como conectar seus projetos do Adobe Commerce e do Experience Manager Assets ao Serviço de mecanismo de regras da Assets para habilitar a sincronização de ativos entre esses dois sistemas."
feature: CMS, Media
source-git-commit: 9d7b1b58b472a99196213e5ab109142bc57b1692
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---


# Configurar o serviço de sincronização

O ARES (Asset Rules Engine Service) é um serviço de vários locatários que integra o AEM Assets ao Adobe Commerce. Este serviço sincroniza ativos entre o Adobe Commerce e o Experience Manager. O serviço ARES corresponde automaticamente ativos no AEM a produtos no Adobe Commerce com base no SKU ou em outros atributos principais. Ele também garante que os ativos e as variações de produto mais recentes estejam sempre disponíveis no site de comércio eletrônico.

Para configurar o serviço, você precisa registrar sua ID de locatário usando a API GraphQL ARES e selecionar a regra correspondente para sincronizar ativos.

## Escolher uma estratégia correspondente

A integração do AEM Assets para Commerce suporta duas estratégias correspondentes para sincronizar ativos entre o Adobe Commerce e o AEM Assets.

- **MatchBySku**-Esta é a regra de correspondência padrão que corresponde ativos com base na SKU (Unidade de Manutenção de Estoque) do produto. O SKU é um identificador exclusivo para cada produto. Essa regra corresponde a SKU nos metadados do ativo à SKU do produto Commerce para garantir que os ativos estejam associados aos produtos corretos.

- **ExternalMatcher**-Esta regra de correspondência se destina a cenários mais complexos ou a requisitos de negócios específicos que exigem lógica de correspondência personalizada. Para usar essa regra, você deve ter um código personalizado implementado no Adobe Developer App Builder que define como os ativos são correspondidos aos produtos.

Para integração inicial, use a estratégia `MatchBySku`. Se necessário, é possível alterar a estratégia de correspondência posteriormente.

## Registrar um locatário

>[!BEGINSHADEBOX]

**Pré-requisito**

- [O projeto do AEM Assets foi configurado com metadados Commerce necessários para mapear ativos](aem-assets-configure-aem.md).

- [Instalar e configurar a Integração do Experience Manager Assets no Adobe Commerce](aem-assets-configure-commerce.md).

>[!ENDSHADEBOX]

## Coletar credenciais

Você precisa das credenciais a seguir para autenticar e conectar seu ambiente de projeto do Commerce e do AEM Assets com os serviços SaaS da Commerce.

| Dados necessários | Source | Onde encontrá-lo |
| ---------- | ------ | ------------- |
| Chave de API da conta Magento | Commerce | Forneça a chave de API pública para o ambiente do Commerce que você está usando, Preparo ou Produção. Você pode encontrar as chaves de API para os ambientes de Produção e Preparo na página [Configuração do Commerce Service Connector](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) em Admin ou na página [!UICONTROL My Account] na seção [!UICONTROL API Portal]. |
| Identificador de projeto SaaS da Commerce <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Administrador do Commerce | Esses valores identificam o ambiente Commerce e o espaço de dados SaaS e o projeto ao qual se conectar. Os valores vêm da [configuração do Identificador SaaS do Commerce Services Connector].(aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| AEM `programId`<br>`environmentId` | [Ambiente de criação do AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | Abra a página do AEM Sites e selecione **[!UICONTROL Assets]**.  Copie as IDs de projeto e ambiente da URL: `https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/` |
| baseURL | vitrine da Commerce | A [URL base](../stores-purchase/store-urls.md) da sua loja da Commerce. |
| Credenciais OAuth para acesso à API | Administrador do Commerce | Você pode encontrar essas credenciais nas [configurações do Commerce para a integração com o Assets](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release). |

## Registrar inquilino

Conclua o registro do locatário enviando uma solicitação ao Serviço de mecanismo de regras da Assets para adicionar credenciais de autenticação e IDs do locatário. A solicitação inclui credenciais e identificadores de projeto necessários para estabelecer as conexões entre o serviço, o projeto do Commerce e o projeto do Experience Manager Assets.

Envie a solicitação usando um cliente GraphQL ou cURL.

>[!BEGINTABS]

>[!TAB Solicitação GraphQL]

Use um cliente GraphQL para enviar uma solicitação POST ao ponto de extremidade de API `https://commerce.adobe.io/assets-integration/graphql`

**Cabeçalhos obrigatórios**

Especifique os seguintes cabeçalhos HTTP para a solicitação:

- `x-api-key`: Chave de API da sua conta Magento
- `magento-environment-Id`: Identificador SaaS
- `x-gw-signature`: Token JWT associado à MAGEID

**Solicitação:**

**Sintaxe**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**Exemplo de uso**

Registre um locatário e selecione a regra `matchBySku` para mapear ativos entre o Adobe Commerce e o projeto do AEM Assets.

**Solicitação:**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**Resposta**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB cSolicitação de URL]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### Campos de entrada

#### AemInput

Identifica a instância do AEM Assets para armazenar ativos do Commerce. Essas informações podem ser obtidas na visualização Meus programas do Cloud Manager ou no URL de criação de conteúdo.

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| `programId` | String! | Identificador exclusivo do seu projeto no AEM Cloud Service |
| `environmentId` | String! | ID do ambiente de projeto que você está usando, como Produção, Preparo ou Desenvolvimento |

#### CommerceInput

Este campo de entrada fornece as credenciais de autenticação do OAuth para o acesso da API ao catálogo do Commerce. Você pode encontrar essas credenciais nas [configurações do Commerce para a integração com o Assets](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| `baseUrl` | String | A [URL base](../stores-purchase/store-urls.md) da sua loja da Commerce. |
| `credentials` | [CommerceCredentialsInput](#commercecredentialsinput)! | Especifica as credenciais para acessar a instância do Commerce. |
| `extensionVersion` | String | Opcional. A versão da integração do AEM Assets para a extensão do Commerce instalada na instância do Commerce. |
| `version` | String | Opcional. A versão do aplicativo Commerce instalada na instância do Commerce. |

#### CommerceCredentialsInput

Este campo de entrada fornece as credenciais do OAuth para o acesso da API ao catálogo do Commerce. Você pode encontrar essas credenciais nas [configurações do Commerce para a integração com o Assets](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| `accessToken` | String! | O token de acesso gerado para a integração do Assets. |
| `accessTokenSecret` | String! | O segredo do token de acesso gerado para a integração com o Assets. |
| `consumerKey` | String! | A chave do consumidor gerada para a integração do Assets. |
| `consumerSecret` | String! | O segredo do consumidor gerado para a integração com o Assets. |

#### ExternalMatcherInput

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| assetToProductUrl | String! | <!--Add field description--> |
| productToAssetUrl | String! | <!--Add field description--> |
| credenciais | [ExternalMatcherCredentialsInput](#externalmatchercredentials)! | Credenciais para acessar o projeto do App Builder para a integração do AEM Assets com o Commerce. |

#### ExternalMatcherCredentials

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| `oauthServerUrl` | String! |    |
| `clientId` | String! |      |
| `clientSecret` | String! |    |
| `imsOrgId` | String! | A organização IMS onde o AEM Assets e o Adobe Commerce são provisionados. |

#### MatchBySkuRuleInput

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| metadataField | String! | Especifique o campo de metadados de ativos a ser usado para correspondência. Usar `commerce:skus` |

#### EntradaRegra

Especifica a regra de correspondência a ser usada para sincronizar ativos entre o Adobe Commerce e o AEM Assets.

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| externalMatcher | [ExternalMatcherInput](#externalmatcherinput) | Seleciona a regra externalMatcher para correspondência de ativos e especifica os dados necessários para usá-la. |
| MatchBySkuRule | [MatchBySkuRuleInput](#matchbyskuruleinput) | Seleciona MatchBySkuRule para correspondência de ativos e especifica os dados necessários para usá-lo. |

#### RuleTypeInput

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| RuleType | enum | Especifica uma lista de regras de correspondência de ativos disponíveis para a Integração do AEM Assets para Commerce. Os valores disponíveis são `matchBySKU` ou `externalMatcher`. |

#### TenantInput

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| `aem` | [AemInput!](#aeminput) | Identifica a instância do AEM Assets na AEM Cloud Service em que você armazena os ativos do Commerce. |
| `commerce` | [CommerceInput!](#commerceinput) | Fornece informações e credenciais do projeto do Commerce para acesso à API |
| `enabled` | Booleano! | Ative ou desative a sincronização de ativos entre o Adobe Commerce e o AEM Assets. |
| `projectId` | String! | A ID do projeto SaaS da [configuração do Identificador SaaS do Commerce Services Connector](aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| `rule` | [RuleInput!](#ruleinput) | Especifica a regra de correspondência a ser usada para sincronizar ativos entre o Adobe Commerce e o AEM Assets. Especifique `[matchBySkuRule](#matchbyskuruleinput)` ou `[externalMatcher](#externalmatcherinput)`. |

### Campos de saída

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| dados | [registerTenant] | Retorna as informações de registro do locatário e as mensagens de erro do servidor. |

#### RegisterTenantResponse

| Campo | Tipo de dados | Descrição |
| ----- | --------- | ----------- |
| tenantId | String! | Retorna a ID do locatário que foi registrada. Essa ID garante que os dados da integração do AEM Assets para Commerce sejam armazenados e recuperados do espaço de dados SaaS associado ao ambiente do Commerce. |
| userErrors | [[userError!]!](#usererror) | Retorna qualquer mensagem de erro gerada pela solicitação. |

#### UserError

| Erro | Descrição |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | Esse erro ocorre se a ID de ambiente especificada no cabeçalho `Magento-Environment-Id` não for atribuída à conta IMS. Este erro pode ocorrer porque a conta IMS não foi conectada quando o [Commerce Services Connector](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) foi configurado para a instância do Commerce. |
| `Client ID is invalid` | O cabeçalho `x-api-key` está incorreto. |
| `Client ID is missing` | O cabeçalho `x-api-key` não foi fornecido. |
| `JWT is required` | O cabeçalho `x-gw-signature` não foi fornecido. |
| `JWT is invalid` | O cabeçalho `x-gw-signature` não foi fornecido. |
| `Tenant already exists` | Um locatário com o `mageID` fornecido (obtido do token JWT) e `saasId` (fornecido pelo cabeçalho `Magento-Environment-Id`) já foi registrado. |
| `Unexpected error when connecting with AEM Assets` | Este erro ocorre devido a valores `programId` ou `environmentId` inválidos ou inexistentes. |
| `Unable to connect with AEM Assets` | Há dois motivos possíveis para esse erro:<br>1. A conta de ativo do AEM está associada a uma Id de organização IMS diferente da fornecida para o Adobe Commerce.<br>2. Os metadados `commerce:isCommerce` não existem no AEM Assets, indicando que não há ativos aprovados para enviar do AEM Assets para a instância do Commerce. |
| `Unexpected error when connecting with Commerce` | Este erro ocorre quando um comércio inválido `baseURL` é fornecido. |
| `Unable to connect with Commerce, unauthorized` | Credenciais de comércio inválidas foram fornecidas, resultando em acesso não autorizado. |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | O campo `Rule` contém um valor incorreto. Para a solicitação RegisterTenant, os tipos de regra disponíveis são definidos pela enumeração [RuleTypeInput](#ruletypeinput). |

## Habilitar a integração do Experience Manager Assets

Depois de registrar o locatário, a última etapa do processo de integração é ativar a extensão Integração da Experience Manager Assets para o Commerce no Administrador.

1. Ative a extensão.

   1. Vá para **Lojas** > Configurações > **Configuração** > **Catálogo**.

   1. Abra a configuração do Catálogo selecionando **[!UICONTROL Catalog]**.

   1. Expandir **[!UICONTROL AEM Assets integration]**.

   1. Defina **[!UICONTROL Integration enabled]** como `yes`.

      ![Integração do AEM Assets para a configuração do administrador do Commerce](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}
