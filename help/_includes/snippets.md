---
title: Trechos
description: Notas e elementos visuais reutilizados para observar um recurso ou página que se aplica a uma edição específica
source-git-commit: 911ae6ec19d7497bf5246b0aaa384471749c5d64
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Trechos

## Recurso somente EE {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Recurso do Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Recurso exclusivo somente no Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Saiba mais</a>)</td></tr>
</table>

## Recurso somente B2B {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Recurso B2B do Adobe Commerce" src="../assets/b2b.svg" width="20" height="20" /> Recurso exclusivo disponível somente com o <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">B2B para Adobe Commerce</a></td></tr>
</table>

## Recurso somente CE {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="recurso Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> É necessário um método alternativo para o Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Saiba mais</a>)</td></tr>
</table>

## Nota de autenticação do administrador do IMS {#ims-admin-note}

>[!NOTE]
>
>Os comerciantes do Adobe Commerce que têm um Adobe ID e desejam um logon simplificado para produtos Adobe Commerce e Adobe Business podem integrar a autenticação de administrador do Commerce ao fluxo de trabalho de autenticação do Adobe IMS. Depois que essa integração for ativada para a loja da Commerce, cada usuário administrador deverá usar suas credenciais de Adobe, e não as credenciais da conta da Commerce, para fazer logon. Consulte [Visão geral da integração do Adobe Commerce com o Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Observação sobre APIs GTag {#gtag-api-note}

>[!NOTE]
>
>A partir da versão 2.4.5, a integração de serviços da Google é atualizada para oferecer suporte ao uso das APIs GTag. O GTag é um mecanismo unificado para integração com a funcionalidade do Google para páginas da Web e oferece suporte aos mais novos recursos e oportunidades para rastreamento e gerenciamento de conteúdo por meio dos Serviços da Google. Para obter mais informações, consulte [Documentação do desenvolvedor do Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Nota de salto automática de reescrita de URL {#url-rewrite-skip}

>[!NOTE]
>
>Quando os redirecionamentos automáticos estão ativados e você salva uma categoria, todas as regravações de produto e categoria são geradas em tempo real e armazenadas em tabelas de regravação por padrão. Esse processo pode resultar em problemas significativos de desempenho para categorias com muitos produtos atribuídos. A solução é alterar esse padrão e ignorar a geração de regravações de URL de produtos/categorias para salvar categorias. Nesse caso, as substituições de produto são geradas somente para o URL do produto canônico. Consulte [Redirecionamentos automáticos de produto](/help/merchandising-promotions/url-redirect-product-automatic.md) para obter mais informações.

## Observação sobre parâmetros de reescrita de URL {#url-rewrite-params}

>[!IMPORTANT]
>
>No processo de redirecionamento, todos os parâmetros de GET especificados no URL são removidos por motivos de segurança.

## Nova regra de preço {#new-price-rule}

>[!NOTE]
>
>As regras de preço são processadas automaticamente com outras regras do sistema. A frequência de processamento depende da [configuração do cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). Ao criar uma regra de preço, aguarde tempo suficiente para ela entrar no sistema. Quando tiver certeza de que está no sistema, teste a regra.

## Definições de configuração {#config}

Para acessar as definições de configuração da loja, escolha **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**do_ Admin _barra lateral.

## Descontinuação da API UPS {#ups-api}

>[!IMPORTANT]
>
>A partir de junho de 2024, os comerciantes do Adobe Commerce não poderão mais transacionar com a integração atual do UPS. Isso ocorre porque as APIs do United Parcel Service (UPS) usadas pela integração nativa do Adobe Commerce atualmente não oferecem suporte ao modelo de segurança OAuth 2.0 necessário. Para saber mais sobre essa alteração, consulte [_Guia de migração da chave de acesso do portal do desenvolvedor_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Os comerciantes devem [aplicar uma atualização de correção de qualidade](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) para o armazenamento para migrar da API SOAP para a API RESTful, que oferece suporte aos protocolos de autenticação OAuth 2.0.


## Documentação disponível {#docs-links}

| Recurso de documentação | Descrição |
|----------------------- | ----------- |
| [Documentação do comerciante do Adobe Commerce 2.4](../landing/home.md) | Documentação voltada para o comerciante do Adobe Commerce |
| [Documentação dos Serviços para o Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Documentação para dar suporte a uma coleção de serviços que ajudam os comerciantes a integrar os principais componentes de seus negócios à loja. |
| [Guia da infraestrutura do Commerce na nuvem](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Procedimentos passo a passo para implantar o Adobe Commerce em uma plataforma de hospedagem em nuvem gerenciada e automatizada. |
| [Guias operacionais do Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Documentação de sistemas sobre os conceitos, processos, ferramentas e práticas recomendadas para desenvolver, implantar e manter projetos do Adobe Commerce. |
| [Documentação do desenvolvedor do Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Documentação voltada para desenvolvedores usada para personalizar o Adobe Commerce e integrar-se com sistemas de terceiros |

{style="table-layout:auto"}
