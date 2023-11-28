---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Revise as configurações no [!UICONTROL Customers] &gt; [!UICONTROL Promotions] página do Administrador do Commerce.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Regras de lembrete de email automatizado](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Global | Habilita lembretes de email automatizados. Se estiver definido como Não, as configurações restantes serão ignoradas. Opções: `Yes` / `No` |
| [!UICONTROL Frequency] | Global | Indica a frequência com que o Commerce deve verificar se há novos clientes qualificados para os lembretes de email automatizados. Opções: <br/>**`Minute Intervals`**- Envia o email de acordo com o intervalo selecionado. (5 minutos, 10 minutos, 15 minutos, 20 minutos ou 30 minutos)<br/>**`Hourly`** - Envia emails a cada hora, no minuto após a hora especificada. Insira um valor entre 0-59. <br/>**`Daily`**- Envia emails diariamente, a partir da Hora de início. |
| [!UICONTROL Interval] | Global | O intervalo deve ser igual ou maior que o período de inicialização do cron.php. Opções: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Global | Define o dia, o minuto e o segundo em que o email é enviado. Especificado no formato de 24 horas, com base na hora do sistema no servidor. |
| [!UICONTROL Maximum Emails per One Run] | Global | Limita o número de emails enviados em um bloco agendado. |
| [!UICONTROL Email Send Failure Threshold] | Global | O número de vezes que o lembrete tenta enviar notificações para um endereço de email específico e falha. Quando o valor é definido como 0, não há limite e as notificações continuam a ser enviadas apesar de todas as falhas. |
| [!UICONTROL Reminder Email Sender] | Exibição da loja | A identidade da loja que aparece como o remetente do email. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Códigos de cupom específicos gerados automaticamente](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Define o comprimento do código do cupom, excluindo prefixo, sufixo e separadores. |
| [!UICONTROL Code Format] | Global | Define o formato do código do cupom. As opções incluem: <br/>**`Alphanumeric`**- Qualquer combinação de letras e números.<br/>**`Alphabetical`** - Somente letras. <br/>**`Numeric`**- Somente números. |
| [!UICONTROL Code Prefix] | Global | Um valor que é anexado ao início de todos os códigos de cupom. Se não quiser usar um prefixo, deixe o campo em branco. |
| [!UICONTROL Code Suffix] | Global | Um valor que é anexado ao final de todos os códigos. Se não quiser usar um sufixo, deixe o campo em branco. |
| [!UICONTROL Dash Every X Characters] | Global | O intervalo para inserir um traço (-) em todos os códigos de cupom. Se não quiser usar um traço, deixe o campo em branco. <br/>_**Nota:**_ Os códigos de cupom que diferem somente por um traço são considerados códigos diferentes. |

{:style=&quot;table-layout:auto&quot;}
