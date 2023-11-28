---
title: Lembretes de email
description: Saiba mais sobre lembretes de email que podem ser enviados automaticamente para os clientes quando um conjunto específico de condições é atendido.
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Lembretes de email

{{ee-feature}}

O objetivo de um lembrete por email é incentivar as pessoas que visitaram sua loja a aproveitar uma promoção e fazer uma compra. Lembretes de email podem ser enviados automaticamente para os clientes quando um conjunto específico de condições é atendido. Por exemplo, você pode enviar um lembrete para clientes que adicionaram algo ao carrinho ou lista de desejos, mas ainda não fizeram uma compra. Você pode usar lembretes de email para incentivar os clientes a retornar à sua loja e incluir uma [código do cupom](price-rules-cart-coupon.md) como incentivo. Os códigos de cupom podem ser gerados automaticamente para cada lote de lembretes de email, para fornecer controle sobre as ofertas associadas a cada lote.

Os lembretes de email podem ser acionados depois de um número específico de dias desde que um carrinho foi abandonado ou para qualquer outra condição que você queira definir. As condições comuns incluem valor total do carrinho, quantidade, itens no carrinho e assim por diante.

>[!NOTE]
>
>Se um cliente tiver mais de um carrinho abandonado correspondente, uma lista de desejos ou uma combinação de ambos, o lembrete de email será acionado apenas uma vez para esse cliente. Para acionar o mesmo lembrete de email novamente, use o _[!UICONTROL Repeat Schedule]_para definir o número de dias entre emails.

![Lembretes de email](./assets/email-reminders.png){width="700" zoomable="yes"}

## Configurar lembretes de email

As regras de lembrete de email podem ser enviadas em intervalos regulares por minuto, hora ou dia. A configuração determina quantos emails são enviados em um lote e a identidade de armazenamento que aparece como remetente da mensagem.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Promotions]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Automated Email Reminder Rules]** e faça o seguinte:

   ![Configuração dos clientes - regras automatizadas de lembrete de email](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - Definir **[!UICONTROL Enable Reminder Emails]** para `Yes`.

   - Para definir com que frequência executar verificações para novos clientes que qualificam lembretes de email automatizados, defina **[!UICONTROL Frequency]** a um dos seguintes:

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - Defina as **[!UICONTROL Interval]**, com base no _[!UICONTROL Frequency]_configuração.

   - Definir **[!UICONTROL Start Time]** à hora, aos minutos e ao segundo em que o email é enviado, com base em um relógio de 24 horas.

   - Para limitar o número de emails que podem ser enviados em um lote, insira o número no campo **[!UICONTROL Maximum Emails per One Run]** campo.

   - Para evitar tentativas repetidas de envio de email com falha, insira o número máximo de tentativas na **[!UICONTROL Email Send Failure Threshold]** campo.

   - Definir **[!UICONTROL Reminder Email Sender]** para o [armazenar contato](../getting-started/store-details.md#store-email-addresses) que aparece como o remetente do email de lembrete.

   Para obter uma lista detalhada dessas opções, consulte [Regras de lembrete de email automatizado](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) no _Referência de configuração_.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Modelos de lembrete de email

O modelo padrão de lembrete de email pode ser personalizado e modelos adicionais podem ser criados para diferentes promoções. Os lembretes de email têm uma seleção de variáveis específicas que podem ser incorporadas à mensagem. As informações nessas variáveis são determinadas pela regra de lembrete de email que você configurou e pela regra de preço do carrinho associada ao cupom. O botão Inserir variável pode ser usado para inserir a tag de marcação com a variável no modelo. Para saber mais, consulte [E-mail](../systems/email-templates.md).

![Visualização do lembrete de email](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### Personalizar um modelo de lembrete de email

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Clique em **[!UICONTROL Add New Template]**.

1. No **[!UICONTROL Template]** lista em `Magento_Reminder`, escolha o **[!UICONTROL Promotion Notification/Reminder]** modelo.

1. Clique em **[!UICONTROL Load Template]**.

Siga o padrão [instruções](../systems/email-template-custom.md) para personalizar o modelo.

### Variáveis de lembrete de email

#### Código do cupom

```
{{var coupon.getCode()|escape}}
```

#### Limite de Uso do Cupom

```
{{var coupon.usage_limit|escape}}
```

#### Uso Do Cupom Por Cliente

```
{{var coupon.usage_per_customer|escape}}
```

#### URL da conta do cliente

```
{{var this.getUrl($store,'customer/account/',[_nosid:1])}}
```

#### Nome do Cliente

```
{{var customer_data.name|escape}}
```

#### Modelo de rodapé de email

```
{{template config_path="design/email/footer_template"}}
```

#### Modelo de cabeçalho de email

```
{{template config_path="design/email/header_template"}}
```

#### Enviar imagem de logotipo por email - Alt

```
{{var logo_alt}}
```

#### URL da imagem do logotipo de email

```
{{var logo_url}}
```

#### Descrição da promoção

```
{{var promotion_description|escape|nl2br}}
```

#### Nome da promoção

```
{{var promotion_name|escape}}
```

#### Nome do armazenamento

```
{{var store.frontend_name}}
```

#### Armazenar URL

```
{{store url=""}}
```
