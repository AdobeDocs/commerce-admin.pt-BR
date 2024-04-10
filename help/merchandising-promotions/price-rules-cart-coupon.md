---
title: Códigos de cupom
description: Saiba como usar códigos de cupons com regras de preço de carrinho para aplicar um desconto quando um conjunto de condições é atendido.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 7407df02ca62e36b4dd60dba418eae3e6aa34491
workflow-type: tm+mt
source-wordcount: '1839'
ht-degree: 0%

---

# Códigos de cupom

Os códigos de cupons são usados com [regras de preço do carrinho](price-rules-cart.md) para aplicar um desconto quando um conjunto de condições for atendido. Por exemplo, um código de cupom pode ser criado para um grupo de clientes específico ou para qualquer pessoa que faça uma compra acima de um determinado valor. Para aplicar o cupom a uma compra, o cliente pode inserir o código do cupom no carrinho ou possivelmente na caixa registradora do seu _tijolo e argamassa_ armazenamento. Estas são algumas das maneiras de usar cupons na loja:

- Cupons de email para clientes
- Produzir cupons impressos
- Criar cupons na loja para usuários móveis

Os códigos de cupom podem ser enviados por email ou incluídos em boletins informativos, catálogos e anúncios. A lista de códigos de cupom pode ser exportada e enviada para uma impressora comercial. Você também pode criar cupons na loja com um código de resposta rápida que os compradores podem digitalizar com seus smartphones. O código QR pode ser vinculado a uma página em seu site com mais informações sobre a promoção.

A partir do Commerce 2.4.7, os compradores podem aplicar vários cupons a um carrinho. Os comerciantes também podem aplicar vários cupons usando a assistência para compras.

## Configurar códigos de cupom

O comprimento e o formato dos códigos de cupom gerados automaticamente são controlados pela configuração. Os caracteres podem ser definidos como todos os números, todas as letras ou uma combinação. Você pode inserir um traço em intervalos definidos para facilitar a leitura e adicionar um prefixo e um sufixo para associar o código a uma campanha ou iniciativa específica.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Promotions]**.

   ![Configuração dos clientes - códigos de cupom específicos gerados automaticamente](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Expanda a **[!UICONTROL Auto Generated Specific Coupon Codes]** seção.

   ![Configuração dos clientes - códigos de cupom específicos gerados automaticamente](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Insira o **[!UICONTROL Code Length]**, incluindo prefixo, sufixo e separadores.

1. Defina o **[!UICONTROL Code Format]** a um dos seguintes:

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. Para **[!UICONTROL Code Prefix]**, insira o valor que deseja que apareça no início de todos os códigos de cupom.

1. Para **[!UICONTROL Code Suffix]**, insira o valor que deseja que apareça no final de todos os códigos de cupom.

1. Para **[!UICONTROL Dash Every X Characters]**, digite o número de caracteres entre cada traço.

   Os códigos de cupom com diferentes padrões de traço são considerados códigos diferentes, mesmo se os números forem os mesmos.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Criar cupons

>[!NOTE]
>
>Antes de criar cupons, use o `bin/magento cron:run` comando para verificar se o cron está em execução. Consulte [Executar cron a partir da linha de comando](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) no _Guia de configuração_ para obter mais informações.

### Método 1: criar um cupom específico

1. Siga as instruções para criar um [regra de preço do carrinho](price-rules-cart.md).

1. No **[!UICONTROL Rule Information]** seção, definir **[!UICONTROL Coupon]** para `Specific Coupon`.

1. Insira um **[!UICONTROL Coupon Code]** a ser usado com a promoção.

   O formato do código (numérico, alfanumérico ou alfabético) é determinado pelo [configuração](#configure-coupon-codes).

1. Para limitar o número de vezes que o cupom pode ser usado, faça o seguinte:

   - Insira o número de **[!UICONTROL Uses per Coupon]**.
   - Insira o número de **[!UICONTROL Uses per Customer]**.

   Para uso ilimitado, deixe esses campos em branco.

   ![Regra de preço do carrinho - informações de cupom](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se houver uso simultâneo do mesmo cupom por vários clientes ao mesmo tempo, é possível que o limite de uso definido seja excedido devido ao processamento atrasado do cupom.

1. Para tornar o cupom válido por um período de tempo, faça o seguinte:

   - ![Magento Open Source](../assets/open-source.svg) (Somente Magento Open Source) Conclua o **De** e **Para** datas. Para selecionar a data, clique no link **Calendário** (![Ícone de calendário](../assets/icon-calendar.png)) ao lado de cada campo. Se você deixar o intervalo de datas vazio, a regra não expirará.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente no Adobe Commerce) Siga um destes procedimentos:

     **Opção 1:** Agendar uma nova atualização

      - Clique em **[!UICONTROL Schedule New Update]** no canto superior direito da página.

        ![Agendar atualização](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Insira o **[!UICONTROL Update Name]** e **[!UICONTROL Description]**.

      - Escolha o **Data de início** e **[!UICONTROL End Date]** no Calendário ( ![Ícone de calendário](../assets/icon-calendar.png) ). Se você deixar o intervalo de datas vazio, a regra não expirará.

      - Quando terminar, clique em **[!UICONTROL Save]**.

        ![Regra de preço do carrinho - alteração agendada](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **Opção 2:** Atribuir a uma atualização existente:

      - Selecionar **[!UICONTROL Assign to Another Update]**.

      - Localize a atualização na lista e clique em **[!UICONTROL Select]**.

1. Conclua o [regra de preço do carrinho](price-rules-cart.md) conforme necessário.

### Método 2: Gerar um lote de cupons

A geração de cupons de desconto é uma operação assíncrona, executada em segundo plano para que você possa continuar trabalhando no Administrador sem esperar a conclusão da operação. O sistema exibe uma mensagem quando a tarefa é concluída.

1. Siga as instruções para criar um [regra de preço do carrinho](price-rules-cart.md).

1. Em **[!UICONTROL Coupon Code]**, selecione o **[!UICONTROL Use Auto Generation]** caixa de seleção

1. Para limitar o número de vezes que cada cliente pode usar o cupom, insira o número de **[!UICONTROL Uses per Customer]**.

   ![Regra de preço do carrinho - gerar cupons numerados automaticamente](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se houver uso simultâneo do mesmo cupom por vários clientes ao mesmo tempo, é possível que o limite de uso definido seja excedido devido ao processamento atrasado do cupom.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Manage Coupon Codes]** e faça o seguinte:

   ![Regra de preço do carrinho - gerenciar códigos de cupom](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - Para **[!UICONTROL Coupons Qty]**, insira o número de cupons que deseja gerar.

   - Insira o **[!UICONTROL Code Length]**, sem incluir o prefixo, sufixo ou separadores.

   - Defina o **[!UICONTROL Code Format]** a um dos seguintes:

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Opcional) Insira um **[!UICONTROL Code Prefix]** para ser adicionado ao início do código.

   - (Opcional) Insira um **[!UICONTROL Code Suffix]** para ser adicionado ao final do código.

   - (Opcional) Para **[!UICONTROL Dash Every X Characters]**, digite o número de caracteres entre cada traço. Por exemplo, se o código tiver 12 caracteres e houver um traço a cada quatro caracteres, ele terá a aparência de `xxxx-xxxx-xxxx`. Os traços facilitam a leitura e a inserção dos códigos.

1. Quando terminar, clique em **[!UICONTROL Generate]**.

   O sistema exibe `Message is added to queue, wait to get your coupons soon`.

   Após a conclusão do trabalho cron, a lista de códigos gerados é exibida.

   | Campo | Descrição |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | Um código exclusivo de cupom que foi criado e pode ser usado para receber condições especiais. |
   | [!UICONTROL Created] | A data em que o código do cupom foi criado. |
   | [!UICONTROL Used] | Indica se o cupom foi usado. |
   | [!UICONTROL Times Used] | Indica quantas vezes o código do cupom foi usado. |

   {style="table-layout:auto"}

Você pode exportar códigos de cupom para um arquivo CSV ou Excel XML selecionando o formato do arquivo e clicando em **[!UICONTROL Export]**.

Para excluir códigos de cupom, selecione um ou mais códigos na lista. Selecionar `Delete` do **[!UICONTROL Actions]**  e clique em **[!UICONTROL Submit]**.

>[!NOTE]
>
>Embora o Commerce permita a configuração de vários códigos de cupom, um cliente pode usar apenas um código de cupom no carrinho. Para permitir o uso de mais de um código de cupom no carrinho simultaneamente, considere usar uma extensão correspondente de [Commerce Marketplace](https://marketplace.magento.com/).

## Relatório de cupons

A variável _Cupons_ O relatório agrega dados de cada cupom usado durante um intervalo de datas específico. Como os cupons são aplicados a partir do carrinho de compras, o relatório inclui dados de todos os cupons resgatados, independentemente da [status do pedido](../stores-purchase/order-status.md). Como resultado, o relatório pode incluir os totais projetados e reais. O relatório pode ser filtrado por uma exibição de loja específica, período de tempo, status do pedido e regra de preço do carrinho.

No exemplo a seguir, o código de cupom &quot;H20&quot; foi usado por dois clientes. Um dos pedidos é faturado, mas o outro ainda é _pendente_. As colunas Subtotal de Vendas projetado, Desconto de Vendas e Total de Vendas mostram os valores agregados de ambas as ordens, mas somente a ordem faturada real aparece nas colunas Subtotal, Desconto e Total. Cada linha no relatório representa uma promoção de cupom única.

![Relatório de cupons](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Executar o relatório

1. No _Admin_ barra lateral, vá para **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Se você tiver várias exibições de loja, defina **[!DNL Store View]** no canto superior esquerdo para estabelecer o escopo do relatório.

1. Para atualizar as vendas [statistics](../getting-started/sales-reports.md#refresh-statistics) para o dia, clique no link _Última atualização_ na parte superior do espaço de trabalho.

   Em seguida, clique para selecionar a variável **[!UICONTROL Coupons]** e clique em **[!UICONTROL Refresh]**.

   ![Relatório de cupons - atualizar estatísticas](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. Para filtrar os dados, faça o seguinte:

   ![Relatório de cupom - filtros](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - Definir **[!UICONTROL Date Used]** a um dos seguintes:

      - `Order Created`
      - `Order Updated`

     A variável _Pedido atualizado_ O relatório do é criado em tempo real e não requer uma atualização.

   - Para definir o período coberto pelo relatório, defina **[!UICONTROL Period]** a um dos seguintes:

      - `Day`
      - `Month`
      - `Year`

   - Para definir o intervalo de datas do relatório, informe o **De** e **Para** datas no formato M/D/AA.

   - Para imprimir um relatório de um [status do pedido](../stores-purchase/order-status.md), definir **[!UICONTROL Order Status]** para `Specified` e escolha o status do pedido na lista.

   - Para omitir linhas sem dados do relatório, defina **[!UICONTROL Empty Rows]** para `No`.

   - Para definir a atividade de cupom incluída no relatório, siga um destes procedimentos:

      - Para incluir todas as atividades de cupom de todas as regras de preço, defina **[!UICONTROL Cart Price Rule]** para `Any`.
      - Para incluir apenas a atividade relacionada a uma regra de preço específica, defina **[!UICONTROL Cart Price Rule]** para `Specified` e selecione a regra de preço do carrinho na lista.

1. Quando estiver pronto para executar o relatório, clique em **[!UICONTROL Show Report]**.

   O relatório é exibido na parte inferior da página.

### Opções de filtro

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Date Used] | Identifica o campo de data usado como base do relatório. Opções:<br/>**[!UICONTROL Order Created]**: gera o relatório com base na data em que o pedido foi feito pelo cliente. Para garantir que os dados mais atuais sejam incluídos, clique no link da mensagem para atualizar as estatísticas.<br/>**[!UICONTROL Order Updated]**: gera o relatório com base na data em que os pedidos foram atualizados pela última vez. Esse relatório usa dados em tempo real e não requer a atualização de estatísticas. |
| [!UICONTROL Period] | Determina o tipo de intervalo de datas usado para o relatório. Opções: `Day` / `Month` / `Year` |
| [!UICONTROL From] | Indica a primeira data no intervalo de dados de pedido que está incluído no relatório. |
| [!UICONTROL To] | Indica a última data no intervalo de dados de pedido que está incluído no relatório. |
| [!UICONTROL Order Status] | Filtra o relatório por status de pedido. O relatório pode ser gerado para todos os pedidos ou pode ser limitado a um status de pedido específico. Opções: <br/>**[!UICONTROL Any]**: inclui todos os pedidos, independentemente do status.<br/>**[!UICONTROL Specified]**: inclui somente pedidos com o status especificado. Os pedidos cancelados não são incluídos no relatório. |
| [!UICONTROL Empty Rows] | Determina se o relatório inclui linhas de dados vazios que possam ser recuperadas. Opções: `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | Determina quais promoções de cupom são incluídas no relatório. Opções:<br/>**[!UICONTROL Any]**: inclui informações da ordem para qualquer promoção de cupom usada durante o intervalo de datas especificado.<br/>**[!UICONTROL Specified]**: Inclui apenas informações da ordem da promoção de cupom selecionada durante o intervalo de datas especificado. |

{style="table-layout:auto"}

### Colunas do relatório

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Interval] | Indica o intervalo de datas de uso do cupom a ser incluído no relatório. O intervalo pode ser um dia, mês ou ano específico ou um intervalo de datas. A data do intervalo é formatada como nos exemplos a seguir, de acordo com o valor definido em **[!UICONTROL Period]** configuração:<br/>`Day`: 21/06/19<br/>`Month`: 6/2019<br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | O Código de Desconto inserido pelos clientes no carrinho de compras para receber o desconto. |
| [!UICONTROL Price Rule] | O nome da regra de preço associada ao cupom. |
| [!UICONTROL Uses] | O número de vezes que o cupom foi usado durante o intervalo de datas especificado para o relatório. |
| [!UICONTROL Sales Subtotal] | O Subtotal projetado de todos os pedidos feitos com o cupom. <br/>O Subtotal de Vendas representa o Subtotal agregado de todas as ordens qualificadas e inclui `Pending` ordens de venda ainda não faturadas. |
| [!UICONTROL Sales Discount] | O valor de Desconto projetado de todos os pedidos feitos com o cupom. <br/>O Desconto representa a quantia de desconto agregada de todas as ordens qualificadas e inclui `Pending` ordens de venda ainda não faturadas. |
| [!UICONTROL Sales Total] | O Total Geral projetado de todos os pedidos feitos com o cupom. O Total de Vendas inclui todas as taxas de remessa e manuseio, menos o valor do desconto. <br/>O Total de Vendas representa o valor total geral agregado de todos os pedidos qualificados e inclui `Pending` ordens de venda ainda não faturadas. O valor inclui o Subtotal mais Entrega e Manuseio, menos o Desconto, mais Imposto. <br/> Calculado por: `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | O Subtotal agregado de todas as ordens faturadas que usaram o cupom. |
| [!UICONTROL Discount] | O Desconto agregado de todas as ordens faturadas que usaram o cupom. |
| [!UICONTROL Total] | O Total do Pedido agregado de todas as ordens faturadas que usaram o cupom. |

{style="table-layout:auto"}
