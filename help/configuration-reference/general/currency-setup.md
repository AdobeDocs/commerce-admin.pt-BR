---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: Revise as configurações no [!UICONTROL General] &gt; [!UICONTROL Currency Setup] página do Administrador do Commerce.
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 3%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>Consulte [Configuração de moeda](../../stores-purchase/currency-configuration.md) para obter mais detalhes sobre essas configurações.

## [!UICONTROL Currency Options]

![Moeda Configuração > Opções de Moeda](./assets/currency-setup-currency-options.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Site | A moeda principal usada para todas as transações de pagamento online. Para várias exibições de loja, o escopo do preço deve ser definido no campo [Catálogo](../catalog/catalog.md) configuração. |
| [!UICONTROL Default Display Currency] | Exibição da loja | A moeda principal usada para exibir preços. |
| [!UICONTROL Allowed Currencies] | Exibição da loja | As moedas aceitas pela loja para pagamento. |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>A partir da versão 2.4.6, a variável [[!DNL Fixer.io]](https://fixer.io/) serviço está obsoleto e foi substituído pelo [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) serviço. É altamente recomendável usar uma conta APILayer em vez de uma conta obsoleta [!DNL Fixer.io] conta.

![Configuração de moeda > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL API key] | Global | A chave usada para acessar o serviço de conversão por meio de [!DNL fixer.io] conta. Para obter mais informações, consulte [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Determina o número de segundos de inatividade antes que uma sessão do Fixer.io expire. Valor padrão: `100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![Configuração de moeda > Api de correção (APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL API key] | Global | A chave usada para acessar o serviço de conversão por meio de [!DNL APILayer] conta. Para obter mais informações, consulte [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Determina o número de segundos de inatividade antes de uma [!DNL APILayer] sessão expira. O valor padrão é `100`. |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![Configuração de moeda > API do Conversor de moeda](./assets/currency-setup-converter.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL API key] | Global | A chave usada para acessar o serviço de conversão. Para obter mais informações, consulte [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Determina o número de segundos de inatividade antes de um [!DNL Currency Converter] sessão expira. Valor padrão:`100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![Configuração de Moeda > Configurações de Importação Programada](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enabled] | Exibição da loja | Determina se a importação programada está ativada para taxas de moeda. Opções: `Yes` / `No` |
| [!UICONTROL Service] | Exibição da loja | Especifica o serviço que fornece os dados para a importação agendada. O valor padrão é `fixer.io` |
| [!UICONTROL Start Time] | Exibição da loja | Indica a hora de início por hora, minuto e segundo, com base em um relógio de 24 horas. |
| [!UICONTROL Frequency] | Exibição da loja | Determina com que frequência a importação agendada ocorre. Opções: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Exibição da loja | Identifica o endereço de email de cada pessoa que é notificada por email sobre erros de importação programados. Para vários recipients, separe cada entrada com uma vírgula. |
| [!UICONTROL Error Email Sender] | Site | Identifica o contato da loja que aparece como o remetente da notificação de erro por email. Remetente padrão: `General Contact` |
| [!UICONTROL Error Email Template] | Site | Especifica o modelo que é usado como base para a notificação de erro por email. Modelo padrão: `Currency Update Warnings` |

{style="table-layout:auto"}
