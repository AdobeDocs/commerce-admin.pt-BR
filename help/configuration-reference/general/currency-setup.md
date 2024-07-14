---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: Revise as configurações na página [!UICONTROL General] &gt; [!UICONTROL Currency Setup] do Administrador do Commerce.
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>Consulte [Configuração de moeda](../../stores-purchase/currency-configuration.md) para obter mais detalhes sobre essas configurações.

## [!UICONTROL Currency Options]

![Configuração de Moeda > Opções de Moeda](./assets/currency-setup-currency-options.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Site | A moeda principal usada para todas as transações de pagamento online. Para várias exibições de loja, o escopo do preço deve ser definido na configuração [Catálogo](../catalog/catalog.md). |
| [!UICONTROL Default Display Currency] | Exibição da loja | A moeda principal usada para exibir preços. |
| [!UICONTROL Allowed Currencies] | Exibição da loja | As moedas aceitas pela loja para pagamento. |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>A partir da versão 2.4.6, o serviço [[!DNL Fixer.io]](https://fixer.io/) será substituído pelo serviço [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). É altamente recomendável usar uma conta APILayer em vez de uma conta [!DNL Fixer.io] obsoleta.

![Configuração de Moeda > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL API key] | Global | A chave usada para acessar o serviço de conversão por meio da conta [!DNL fixer.io]. Para obter mais informações, consulte [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Determina o número de segundos de inatividade antes que uma sessão do Fixer.io expire. Valor padrão: `100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![Configuração de Moeda > Api de Correção (APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL API key] | Global | A chave usada para acessar o serviço de conversão por meio da conta [!DNL APILayer]. Para obter mais informações, consulte [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Determina o número de segundos de inatividade antes que uma sessão [!DNL APILayer] expire. O valor padrão é `100`. |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![Configuração de moeda > API de conversão de moeda](./assets/currency-setup-converter.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL API key] | Global | A chave usada para acessar o serviço de conversão. Para obter mais informações, consulte [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Determina o número de segundos de inatividade antes que uma sessão [!DNL Currency Converter] expire. Valor padrão:`100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![Configuração de Moeda > Configurações de Importação Agendadas](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

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
