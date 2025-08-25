---
title: Gerenciar crédito da empresa
description: Saiba mais sobre as linhas de crédito da empresa, definição de parâmetros e processamento de pagamentos por conta.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Gerenciar crédito da empresa

O crédito da empresa permite que empresas B2B façam compras com uma linha de crédito pré-aprovada, em vez de exigir pagamento imediato. Quando o [Pagamento na Conta](../b2b/enable-basic-features.md#configure-payment-on-account) está habilitado, as empresas podem comprar até o limite de crédito e exibir seu status de crédito no painel de contas.

![Crédito da empresa](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

O crédito da empresa permite:

* **Estender termos de crédito**—Permitir que clientes empresariais confiáveis comprem por conta com pagamento diferido
* **Definir limites de crédito**—Controle a exposição financeira estabelecendo limites de crédito para cada empresa
* **Rastrear atividade de crédito** — Monitore em tempo real todas as transações de crédito, pagamentos e saldos pendentes
* **Simplifique as transações B2B** — simplifique o processo de compra para empresas com relações de crédito estabelecidas
* **Suporte a fluxos de trabalho complexos** — integre-se a ordens de compra, cotações e processos de aprovação

## Pré-requisitos

Antes de configurar o crédito da empresa, verifique se:

* Os recursos B2B são ativados na instalação do Adobe Commerce
* [Pagamento na Conta](../b2b/enable-basic-features.md#configure-payment-on-account) configurado e habilitado
* As contas da empresa estão configuradas corretamente com as informações de negócios necessárias
* Você tem permissões administrativas para gerenciar configurações de crédito da empresa
* As configurações de moeda são definidas se estiverem operando em várias moedas

## Casos de uso

O crédito da empresa é ideal para:

* **Relacionamentos B2B estabelecidos**—Clientes empresariais de longo prazo com histórico de pagamentos comprovado
* **Clientes de grandes empresas** — Empresas que fazem compras regulares e significativas que exigem prazos de pagamento estendidos
* **Negócios sazonais** — Empresas com fluxo de caixa cíclico que precisam de um tempo de pagamento flexível
* **Aquisição corporativa**—Organizações com compras centralizadas, mas processamento de pagamento distribuído
* **Parceiros da cadeia de fornecimento**—Distribuidores, Revendedores e parceiros de canal que requerem facilidades de crédito

## Noções básicas sobre configurações de Crédito da Empresa

Você pode configurar os seguintes parâmetros relacionados a crédito para cada perfil de empresa:

* **Moeda de Crédito** — Moeda para todas as transações e saldos de crédito
* **Limite de Crédito**— Valor máximo que a empresa pode ter a qualquer momento
* **Permitir Exceder Limite de Crédito**— Se as empresas podem fazer pedidos que excedem o crédito disponível
* **Motivo da Alteração** — Campo de documentação para registrar modificações na configuração de crédito

Para obter detalhes sobre essas configurações e a configuração do perfil da empresa, consulte [Criar uma Conta da Empresa](account-company-create.md).

>[!NOTE]
>
>Se uma empresa tiver um saldo pendente, um aviso será exibido para o administrador da loja na parte superior das ordens de venda quando visualizado pelo Administrador. Isso ajuda a garantir o reconhecimento do status do crédito durante o processamento do pedido.

## Atividade de crédito da empresa

A seção [!UICONTROL Company Credit] do perfil da empresa exibe um histórico completo de todas as transações de crédito, alterações de saldo e atividades de pagamento em um formato de grade.

![Atividade de Crédito da Empresa](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

A grade exibe as seguintes informações para cada transação:

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL Date] | A data da transação. Para exibir a data e a hora, passe o mouse sobre a data. |
| [!UICONTROL Operation] | O tipo de atividade associada à transação. Valores: <br/>**[!UICONTROL Allocated]**- Crédito atribuído à empresa.<br/>**[!UICONTROL Updated]** - Uma alteração foi aplicada a um dos seguintes campos: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- Um pedido foi feito.<br/>**[!UICONTROL Reimbursed]** - O saldo pendente foi reembolsado. <br/>**[!UICONTROL Refunded]**- Valor do memorando de crédito reembolsado.<br/>**[!UICONTROL Reverted]** - O pedido foi cancelado e o valor foi devolvido ao saldo de crédito. |
| [!UICONTROL Amount] | O valor da transação associado aos seguintes tipos de transação: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>Para valores de compra, o valor aparece na moeda de exibição do armazenamento e no formato da configuração de moeda de crédito, seguido da taxa de conversão atual (se aplicável). Por exemplo: <br/>EUR 20.000,00 ($22.400,00) <br/>USD/EUR 0,8928 |
| [!UICONTROL Outstanding Balance] | O valor reembolsado, menos o total devido de todos os pedidos feitos usando o método Pagamento por Conta. O valor pode aparecer como um valor positivo ou negativo. <br/>**[!UICONTROL Positive value]**- Um pagamento antecipado é representado como um valor positivo.<br/>**[!UICONTROL Negative value]** - Um valor devido é representado como um valor negativo. |
| [!UICONTROL Available Credit] | A soma de _[!UICONTROL Credit Limit]_&#x200B;e_[!UICONTROL Outstanding Balance]_. Se a empresa excedeu o limite de crédito, o valor aparece como um valor negativo. |
| [!UICONTROL Credit Limit] | O valor do crédito estendido para a empresa. |
| [!UICONTROL Updated By] | O nome da pessoa que iniciou a operação. |
| [!UICONTROL Custom Reference Number] | O número de referência personalizado associado à transação. |
| [!UICONTROL Comment] | Uma compilação dos valores do campo `Reason for Change`, de acordo com o tipo de operação. <br/>**[!UICONTROL Purchased]**- Inclui comentários da compra, o número do pedido e o link para o pedido.<br/>**[!UICONTROL Reimbursed]** - Inclui comentários da transação reembolsada. |
| [!UICONTROL Action] | Somente para `Reimbursed` operações. **[!UICONTROL Edit]** - Permite que o valor de reembolso seja atualizado. |

{style="table-layout:auto"}

## Atualizar as informações de crédito

Quando os clientes fazem pagamentos, os administradores atualizam as informações de crédito no Administrador.

1. Na barra lateral _Admin_, vá para **Clientes > Empresas**.

1. Localize a empresa na grade e abra-a no modo _Editar_.

1. Expanda a seção **Crédito da Empresa**.

1. Para **Limite de Crédito**, insira o novo valor.

1. Altere os outros valores conforme necessário.

1. Quando as atualizações estiverem concluídas, clique em **[!UICONTROL Save]**.

## Receber Pagamentos

Um saldo reembolsado é um pagamento off-line feito por uma empresa em relação ao saldo de sua conta. O administrador de loja insere o valor manualmente no perfil da empresa, usando o botão _Reembolsar Saldo_. Quando o valor é enviado, o sistema recalcula o saldo pendente e o crédito disponível da empresa e registra a ação no histórico de crédito da empresa. O valor reembolsado é inserido na moeda de crédito, conforme especificado na configuração.

### Aplicar um pagamento a uma conta da empresa

1. Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Localize o registro da empresa na lista e abra-o no modo **[!UICONTROL Edit]**.

1. Na parte superior da página, clique em **Reembolsar saldo**.

1. Na caixa de diálogo, adicione as informações de pagamento:

   ![Saldo de reembolso](./assets/company-reimburse-balance.png){width="500"}

   * Insira o **Valor** do pagamento.

     O valor pode ser inserido como um valor positivo ou negativo.

   * Se aplicável, insira o **Número de Referência Personalizado** para referência.

     Somente um número de referência personalizado pode ser inserido por reembolso. Para aplicar o pagamento a várias OCs, crie um reembolso separado para cada uma.

   * Conforme necessário, insira um **Comentário** para descrever o reembolso.

1. Clique em **Reembolso**.

   O sistema atualiza saldos e histórico de crédito automaticamente para refletir o reembolso.

### Editar um reembolso

1. Abra o perfil da empresa no modo **[!UICONTROL Edit]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **Crédito da Empresa**.

1. Localize a transação de reembolso na grade e clique em **[!UICONTROL Edit]**.

1. Faça as alterações necessárias no **Número de Referência Personalizado** e no **Comentário**.

   O valor do reembolso não pode ser alterado.

1. Clique em **[!UICONTROL Save]**.

## Informações de crédito da vitrine

Os administradores da empresa podem exibir suas informações de crédito no painel de contas, incluindo saldo pendente, crédito disponível, limite de crédito e faturas pendentes. Quando os pedidos são cancelados, os valores retornam ao saldo da empresa e são exibidos no campo Histórico da Alocação de Crédito.

![Crédito da empresa](./assets/company-credit.png){width="700" zoomable="yes"}

## Demonstração de crédito da empresa

Saiba mais sobre como gerenciar o crédito da empresa assistindo a este vídeo de demonstração:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12&learn=on)

## Considerações de segurança

Ao gerenciar créditos da empresa, implemente medidas de segurança robustas para proteger dados financeiros sigilosos:

* **Controle de Acesso**—Restringir permissões de gerenciamento de crédito somente a pessoal autorizado
* **Trilhas de Auditoria** — Manter logs abrangentes de todas as transações e modificações de crédito
* **Proteção de dados**—Criptografa informações financeiras confidenciais em trânsito e em repouso
* **Fluxos de Trabalho de Aprovação** — Implementar processos de aprovação de vários níveis para ajustes de crédito significativos
* **Revisões Regulares**—Conduza auditorias periódicas do acesso dos usuários e das relações de crédito

## Práticas recomendadas

* &#x200B;
   * **Gerenciamento de Política de Crédito**—Ao gerenciar o crédito da empresa, estabeleça políticas claras para definir limites de crédito com base no histórico de pagamento do cliente e nos relacionamentos comerciais. Examine regularmente os saldos pendentes e os padrões de pagamento para avaliar o risco e sempre documente as alterações nas configurações de crédito com motivos detalhados para fins de auditoria.

Processar os pagamentos imediatamente para manter saldos precisos e garantir que as configurações de moeda de crédito se alinhem às operações comerciais principais de cada empresa.

* **Conformidade e segurança**—Restrinja as permissões de gerenciamento de crédito somente a pessoal autorizado, implemente fluxos de trabalho de aprovação para ajustes de crédito significativos e proteja informações financeiras confidenciais de acordo com as políticas de segurança da sua organização. Análises regulares do acesso do usuário e das relações de crédito ajudam a manter a supervisão e a conformidade adequadas.

>[!MORELIKETHIS]
>
>* [Habilitar Recursos B2B](enable-basic-features.md) * Configurar Pagamento na Conta e outras funcionalidades B2B
>* [Criar uma Conta de Empresa](account-company-create.md) * Configurar contas da empresa com recursos de crédito
>* [Gerenciar Empresas](manage-companies.md) * Visão geral dos recursos de gerenciamento da empresa
>* [Funções e permissões da empresa](account-company-roles-permissions.md) * Configure o acesso do usuário para gerenciamento de crédito
>* [Fluxo de Trabalho de Ordem de Compra](purchase-order-flow.md) * Entenda como o crédito se integra a ordens de compra
>* [Referência de Configuração B2B](../configuration-reference/general/b2b-features.md) - Definições de configuração detalhadas para recursos B2B
