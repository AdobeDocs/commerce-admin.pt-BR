---
title: Lista de verificação do Pré-lançamento
description: Use esta lista para verificar as configurações necessárias para garantir que tudo esteja correto antes que sua loja entre em produção.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Lista de verificação do Pré-lançamento

Após concluir o design, o desenvolvimento e o teste do armazenamento, verifique as configurações a seguir para se certificar de que tudo está correto antes do armazenamento _entrar em funcionamento_. Para obter uma descrição abrangente de cada definição de configuração, consulte a [_Referência de Configuração_](../configuration-reference/guide-overview.md).

## Configurações gerais

- [Armazenar URLs](../stores-purchase/store-urls.md) - Verifique se as URLs de armazenamento da vitrine e do Administrador estão corretas para um ambiente de produção ativo.
- Certificado de Segurança - Antes de iniciar seu armazenamento, instale um Certificado de Segurança 100% Assinado e Confiável para o domínio especificado no URL Base.
- [Armazenar Endereços de Email](../getting-started/store-details.md#store-email-addresses) - Preencha todos os endereços de email usados para enviar e receber notificações por email, como novos pedidos, faturas, remessas, avisos de crédito, alertas de preço de produto e boletins informativos. Verifique se cada campo contém um endereço de email comercial válido.

## Configurações de marketing

- [Modelos de email](../systems/email-templates.md) - Atualize os modelos de email padrão para refletir sua marca. Certifique-se de atualizar a configuração se criar modelos.
- [Comunicações de Vendas](../stores-purchase/introduction.md#order-management-and-operations) - Verifique se suas faturas e guias de remessa contêm as informações comerciais corretas e refletem sua marca.
- [Ferramentas do Google](../merchandising-promotions/google-tools.md) - [!DNL Commerce] fornece integração com a API do Google para permitir que sua empresa use o Google Analytics e o Google AdWords.

## Configurações de vendas

- [Opções do carrinho](../stores-purchase/cart-configuration.md) - Examine as definições de configuração do carrinho para ver se há algo que você deseja alterar, como definir o valor de pedido mínimo e o tempo de vida dos preços no carrinho.
- [Opções de check-out](../stores-purchase/checkout-process.md#checkout-options) - Examine as opções de check-out para ver se há algo que você deseja alterar, como configurar termos e condições e configurar o check-out de convidado.
- [Impostos](../stores-purchase/taxes.md) - Verifique se os impostos estão configurados corretamente de acordo com suas regras de imposto comercial e requisitos locais.
- [Métodos de entrega](../stores-purchase/delivery.md) - Habilite todas as transportadoras e métodos de entrega a serem usados pela empresa.
- [PayPal](../stores-purchase/paypal.md) - Se você planeja oferecer aos seus clientes a conveniência de pagar com o PayPal, abra uma Conta de Comerciante do PayPal e configure uma forma de pagamento. Execute algumas transações de teste no Modo Sandbox antes que o armazenamento entre em funcionamento.
- [Métodos de pagamento](../stores-purchase/payments.md) - Habilite os métodos de pagamento que você planeja usar e verifique se eles estão configurados corretamente. Verifique as configurações de status do pedido, moeda aceita, países permitidos e assim por diante.

## Configurações do sistema

[Cron (Tarefas agendadas)](../systems/cron.md) - Os trabalhos Cron são usados para processar emails, regras de preços de catálogo, boletins informativos, alertas de clientes, mapas de site do Google, taxas de moeda de atualização e assim por diante. Verifique se os trabalhos Cron estão definidos para execução no intervalo de tempo apropriado, em minutos.
