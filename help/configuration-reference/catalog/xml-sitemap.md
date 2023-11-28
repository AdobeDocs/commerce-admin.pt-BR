---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: Revise as configurações no [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] página do Administrador do Commerce.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Opções de Categorias](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Frequency] | Exibição da loja | Determina a frequência com que as categorias de mapa de site são atualizadas. Opções: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Exibição da loja | Um valor entre `0.0` e `1.0` que determina a prioridade das atualizações do mapa de site da categoria em relação a outro conteúdo. Zero (`0.0`) tem a prioridade mais baixa. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Products Options]

![Opções de produtos](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Frequency] | Exibição da loja | Determina a frequência com que os produtos de mapa de site são atualizados. Opções: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Exibição da loja | Um valor entre `0.0` e `1.0` que determina a prioridade das atualizações do mapa de site do produto em relação a outro conteúdo. Zero (`0.0`) tem a prioridade mais baixa. |
| [!UICONTROL Add Images into Sitemap] | Exibição da loja | Determina a extensão com que as imagens são incluídas no mapa do site. Opções: `None` / `Base Only` / `All` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Pages Options]

![Opções de páginas do CMS](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Frequency] | Exibição da loja | Determina a frequência com que as páginas CMS do mapa de site são atualizadas. Opções: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Exibição da loja | Um valor entre `0.0` e `1.0` que determina a prioridade das atualizações do mapa de site da página do CMS em relação a outro conteúdo. Zero (`0.0`) tem a prioridade mais baixa. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Store Url Options]

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Frequency] | Exibição da loja | Determina com que frequência os URLs de armazenamento são atualizados. Opções: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Exibição da loja | Um valor entre `0.0` e `1.0` que determina a prioridade das atualizações de URL de armazenamento em relação a outro conteúdo. Zero (`0.0`) tem a prioridade mais baixa. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Generation Settings]

![Configurações de geração](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Exibição da loja | Determina se um mapa de site XML está disponível para o armazenamento. Opções: `Yes` / `No` |
| [!UICONTROL Start Time] | Exibição da loja | Especifica a hora, os minutos e o segundo do dia em que o mapa do site é atualizado. |
| [!UICONTROL Frequency] | Exibição da loja | Determina a frequência com que o mapa do site é atualizado. Opções: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Exibição da loja | O endereço de email da pessoa que recebe a notificação se ocorrer um erro durante o processo de atualização do mapa de site. Para vários endereços, separe cada um com uma vírgula. |
| [!UICONTROL Error Email Sender] | Site | Identifica o contato da loja que aparece como o remetente da notificação de erro. Opções: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Site | Identifica o modelo de email usado para a notificação de erro. Modelo padrão: `Sitemap generate Warnings` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Sitemap File Limits]

![Limites de arquivo do mapa do site](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Exibição da loja | Determina o número máximo de URLs que podem ser incluídos em um único mapa de site. |
| [!UICONTROL Maximum File Size] | Exibição da loja | Determina o tamanho máximo do mapa de site gerado, em bytes. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Search Engine Submission Settings]

![Configurações de Envio do Mecanismo de Pesquisa](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Exibição da loja | Permite que as diretivas sejam enviadas para o arquivo robots.txt. Opções: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
