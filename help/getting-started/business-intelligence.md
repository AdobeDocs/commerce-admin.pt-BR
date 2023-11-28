---
title: '[!DNL Business Intelligence] ferramentas'
description: Saiba como os comerciantes do Adobe Commerce e do Magento Open Source podem usar ferramentas de business intelligence para obter os insights usados para tomar decisões comerciais sólidas.
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# [!DNL Business Intelligence] ferramentas

Use ferramentas de business intelligence para obter o insight usado para tomar boas decisões de negócios.

## [!DNL Business Intelligence] account

Quando você ativa um [!DNL Business Intelligence] por meio do Adobe, você obtém acesso a cinco painéis com aproximadamente 70 relatórios. Esses relatórios foram projetados para fornecer insights sobre seus dados e responder a perguntas como &quot;Como meus pedidos estão crescendo mês a mês?&quot;, &quot;Quem são meus clientes mais fiéis?&quot; e &quot;Minha estratégia de cupom está funcionando?&quot; Para obter informações detalhadas sobre esse conjunto de ferramentas, consulte [Guia do usuário do MBI][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] está incluído na Adobe Commerce e no Magento Open Source. Esse recurso oferece acesso a um conjunto de relatórios dinâmicos com base em seus produtos, pedidos e dados do cliente, com um painel personalizado adaptado às suas necessidades comerciais. Enquanto [!DNL Advanced Reporting] usos [!DNL Business Intelligence] para o analytics, não é necessário ter uma conta Business Intelligence para usar [!DNL Advanced Reporting].

Para obter informações técnicas, consulte a [[!DNL Advanced Reporting]][2]{:target=&quot;_blank&quot;} tópico na documentação do desenvolvedor.

>[!NOTE]
>
>[!DNL Business Intelligence] as contas usam relatórios integrados, em vez da [!DNL Advanced Reporting] recurso.

![Painel de relatórios avançado](./assets/reporting-advanced.png){width="700"}

### Requisitos

* O site deve ser executado em um servidor Web público.

* O domínio deve ter um certificado de segurança (SSL) válido.

* [!DNL Commerce] O deve ter sido instalado ou atualizado com êxito sem erros.

* No [!DNL Commerce] configuração para [armazenar URLs](../stores-purchase/store-urls.md), o **[!UICONTROL Base URL (Secure)]** a configuração da exibição de armazenamento deve apontar para a URL segura. Por exemplo: `https://yourdomain.com`.

* No [!DNL Commerce] configuração para URLs de armazenamento, **[!UICONTROL Use Secure URLs on Storefront]** e **[!UICONTROL Use Secure URLs in Admin]** deve ser definido como `Yes`.

* [[!DNL Commerce] crontab][3] é criado e os trabalhos cron estão em execução no servidor instalado.

>[!NOTE]
>
>[!DNL Advanced Reporting] pode ser usado somente com [!DNL Commerce] instalações que utilizaram continuamente uma única [moeda de base](../stores-purchase/currency-configuration.md).


### Etapa 1: ativar [!DNL Advanced Reporting]

No [!DNL Commerce] configuração, [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) é ativado por padrão e inicia automaticamente se o cron for [configurado](../configuration-reference/advanced/system.md) e em execução. Uma tentativa de estabelecer a assinatura é iniciada no início de cada hora nas próximas 24 horas até ser bem-sucedida. O status da assinatura é &quot;pendente&quot; até que a assinatura seja estabelecida com êxito.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel de navegação esquerdo, onde **[!UICONTROL General]** for expandido, escolha **[!UICONTROL Advanced Reporting]** e faça o seguinte:

   * Verifique se **[!UICONTROL Advanced Reporting Service]** está definida como `Enable` (a configuração padrão).

   * Defina o **[!UICONTROL Time of day to send data]** de acordo com a hora, os minutos e o segundo, de acordo com um relógio de 24 horas, que você deseja que o serviço receba dados atualizados da sua loja. Por padrão, os dados são enviados às 2:00.

   * Em **[!UICONTROL Industry Data]**, escolha o **[!UICONTROL Industry]** que melhor descreva sua empresa.

   ![Configuração avançada de relatórios](./assets/advanced-reporting-config.png){width="400"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando solicitado, clique em **[[!UICONTROL Cache Management]](../systems/cache-management.md)** na mensagem na parte superior da página e atualize todos os caches inválidos.

1. Aguarde durante a noite ou até depois do horário da próxima atualização agendada. Em seguida, verifique o status da sua assinatura. Se o status ainda for _pendente_, certifique-se de que sua instalação atenda a todos os requisitos.

### Etapa 2: acesso [!DNL Advanced Reporting]

1. Siga um destes procedimentos:

   * No _Admin_ barra lateral, escolha **[!UICONTROL Dashboard]**. Em seguida, clique em **[!UICONTROL Go to Advanced Reporting]**.
   * No _Admin_ barra lateral, vá para **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   A variável [!DNL Advanced Reporting] O painel de controle do fornece um resumo rápido de seus pedidos, clientes e produtos. Não deixe de rolar para baixo para ver o painel completo.

1. Para obter uma melhor visualização dos dados, defina o **[!UICONTROL Filters]** no canto superior direito, selecione o período e a exibição de loja que deseja incluir no relatório. Em seguida, faça o seguinte:

   * Passe o mouse sobre qualquer ponto de dados para obter mais informações.
   * Para visualizar todos os relatórios do painel, clique em cada guia.

   ![Ponto de dados](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## Access [!DNL Advanced Reporting] recursos de dados

No canto superior direito do painel Relatórios avançados, clique em **[!UICONTROL Additional Resources]**.

![Recursos de dados de relatórios avançados](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## Solução de problemas

Se você receber a mensagem 404 &quot;Page Not Found&quot; (Página não encontrada), verifique se seu armazenamento atende aos requisitos para [!DNL Advanced Reporting]. Em seguida, siga as instruções para verificar se a integração está instalada.

### Verificar se a integração está ativa

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. Verifique se **[!UICONTROL Magento Analytics user]** A integração do aparece na lista e na guia **[!UICONTROL Status]** é `Active`.

1. Para restabelecer o usuário, clique em **[!UICONTROL Reauthorize]** e faça o seguinte:

   ![Reautorizar](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * Quando solicitado, clique em **[!UICONTROL Reauthorize]** para aprovar o acesso aos recursos da API.

     ![Reautorizar acesso aos recursos da API](./assets/advanced-reporting-integration-api.png){width="600"}

   * Verifique se a lista de Tokens de integração para extensões está concluída. Em seguida, clique em **Concluído**.

     ![Tokens de integração](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. Procure a mensagem que indica a integração `Magento Analytics user` O está reautorizado.

1. Aguarde durante a noite ou até depois da hora da próxima atualização agendada.

### Verificar moeda de base única

[!DNL Advanced Reporting] pode ser usado somente com [!DNL Commerce] instalações que utilizaram apenas um único [moeda de base](../stores-purchase/currency-configuration.md) desde o momento da instalação. O resultado é que, no histórico, todos os pedidos usam a mesma moeda base. [!DNL Advanced Reporting] não funciona se você tiver, a qualquer momento, alterado sua moeda base e tiver pedidos em seu histórico que foram processados com moedas base diferentes.

Para determinar se sua loja tem várias moedas base, você pode consultar suas [!DNL Commerce] da linha de comando usando o seguinte exemplo de MySQL. Talvez seja necessário alterar os nomes das tabelas para corresponder à estrutura de dados:

```sql
select distinct base_currency_code from sales_order;
```

### Discrepância de dados

Se você observar que a variável `Data last updated...` A legenda exibe a data de ontem e não a de hoje. Pode haver um atraso de até um dia nas atualizações avançadas de relatórios. Esse atraso é devido a um tamanho de fila maior do que o esperado.

## Relatórios do painel

**[!UICONTROL Orders]**

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Revenue] | Mostra toda a receita recebida pela exibição de loja durante o período definido. |
| [!UICONTROL Orders] | Mostra todas as ordens feitas por meio da exibição de armazenamento durante o período definido. |
| [!UICONTROL AOV] | Mostra o valor médio de pedido feito por meio da exibição de loja durante o período definido. |
| [!UICONTROL Refunds] | Mostra todos os reembolsos processados pela exibição de armazenamento durante o período definido. |
| [!UICONTROL Tax Collected] | Mostra todos os impostos coletados pela exibição de armazenamento durante o período definido. |
| [!UICONTROL Shipping Collected] | Mostra todas as taxas de remessa coletadas por meio da exibição de loja durante o período definido. |
| [!UICONTROL Orders by Status] | Mostra o número de pedidos por status, para a exibição de armazenamento durante o período definido. |
| [!UICONTROL Orders by Status] | Lista um resumo do número de pedidos por status. |
| [!UICONTROL Coupon Usage] | Lista todos os códigos de cupom e o número de usuários para cada um, resgatados por meio da exibição de armazenamento durante o período definido. |
| [!UICONTROL Orders and Revenue by Billing Region] | Lista o número de ordens e receita por região para a exibição de armazenamento durante o período definido. |
| [!UICONTROL Tax Collected by Billing Region] | Lista a quantia de imposto coletado por região para a exibição de armazenamento durante o período definido. |
| [!UICONTROL Shipping Fees Collected by Shipping Region] | Lista as taxas de remessa coletadas por região para a exibição de loja durante o período definido. |

{style="table-layout:auto"}

**[!UICONTROL Customers]**

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Unique Customers] | Mostra o número de contas de clientes exclusivas associadas à exibição de loja durante o período definido. |
| [!UICONTROL New Registered Accounts] | Mostra o número de novas contas de clientes registradas com a exibição de loja durante o período definido. |
| [!UICONTROL Top Coupon Users] | Lista os principais usuários de cupom por ID do cliente e o número de pedidos feitos com cupons para a exibição de loja durante o período definido. |
| [!UICONTROL Customer KPI Table] | Lista o número de pedidos, a receita e o valor médio de pedido por ID do cliente para a exibição de armazenamento durante o período definido. |

{style="table-layout:auto"}

**[!UICONTROL Products]**

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Quantity of Products Sold] | Mostra o número de produtos vendidos por meio da exibição de loja durante o período definido. |
| [!UICONTROL Products Added to Wishlists] | Lista todos os produtos adicionados às listas de desejos por meio da exibição de loja durante o período definido. |
| [!UICONTROL Best Selling Products by Quantity] | Lista os produtos mais vendidos e a quantidade vendida por meio da exibição de loja durante o período definido. |
| [!UICONTROL Best Selling Products by Revenue] | Lista os produtos mais vendidos e a receita gerada pela venda do produto por meio da exibição da loja durante o período definido. |

{style="table-layout:auto"}


[1]: https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html
[2]: https://developer.adobe.com/commerce/php/development/advanced-reporting/
[3]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
