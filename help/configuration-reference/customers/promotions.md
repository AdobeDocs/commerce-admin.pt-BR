---
title: '[!UICONTROL Customers] > [!UICONTROL Promotions]'
description: Revise as configurações na página [!UICONTROL Customers] > [!UICONTROL Promotions] do Administrador do Commerce.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
TQID: https://experienceleague.adobe.com/Sc1-Wacd9emNUOl9GabUK-J3OLH-eNX2hvk6m8oyjYc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Regras Automatizadas de Lembrete de Email](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules#configure-email-reminders) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Global | Habilita lembretes de email automatizados. Se estiver definido como Não, as configurações restantes serão ignoradas. Opções: `Yes` / `No` |
| [!UICONTROL Frequency] | Global | Indica a frequência com que a Commerce deve verificar se há novos clientes qualificados para os lembretes de email automatizados. Opções: <br/>**`Minute Intervals`**- Envia o email de acordo com o intervalo selecionado. (5 minutos, 10 minutos, 15 minutos, 20 minutos ou 30 minutos)<br/>**`Hourly`** - Envia emails de hora em hora, no minuto após a hora especificada. Insira um valor entre 0 e 59. <br/>**`Daily`**- Envia emails diariamente, a partir da Hora de Início. |
| [!UICONTROL Interval] | Global | O intervalo deve ser igual ou maior que o período de inicialização do cron.php. Opções: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Global | Define o dia, o minuto e o segundo em que o email é enviado. Especificado no formato de 24 horas, com base na hora do sistema no servidor. |
| [!UICONTROL Maximum Emails per One Run] | Global | Limita o número de emails enviados em um bloco agendado. |
| [!UICONTROL Email Send Failure Threshold] | Global | O número de vezes que o lembrete tenta enviar notificações para um endereço de email específico e falha. Quando o valor é definido como 0, não há limite e as notificações continuam a ser enviadas apesar de todas as falhas. |
| [!UICONTROL Reminder Email Sender] | Exibição da loja | A identidade da loja que aparece como o remetente do email. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Códigos de Cupom Específicos Gerados Automaticamente](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart-coupon#configure-coupon-codes)  -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Define o comprimento do código do cupom, excluindo prefixo, sufixo e separadores. |
| [!UICONTROL Code Format] | Global | Define o formato do código do cupom. As opções incluem: <br/>**`Alphanumeric`**- Qualquer combinação de letras e números.<br/>**`Alphabetical`** - Somente letras. <br/>**`Numeric`**- Somente números. |
| [!UICONTROL Code Prefix] | Global | Um valor que é anexado ao início de todos os códigos de cupom. Se não quiser usar um prefixo, deixe o campo em branco. |
| [!UICONTROL Code Suffix] | Global | Um valor que é anexado ao final de todos os códigos. Se não quiser usar um sufixo, deixe o campo em branco. |
| [!UICONTROL Dash Every X Characters] | Global | O intervalo para inserir um traço (-) em todos os códigos de cupom. Se não quiser usar um traço, deixe o campo em branco. <br/>_&#x200B;**Observação:**&#x200B;_ códigos de cupom que diferem somente por um traço são considerados códigos diferentes. |

{style="table-layout:auto"}
