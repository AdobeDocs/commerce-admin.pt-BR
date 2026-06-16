---
title: Lista de verificação do Pré-lançamento
description: Use esta lista para verificar as configurações necessárias para garantir que tudo esteja correto antes que sua loja entre em produção.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
TQID: https://experienceleague.adobe.com/cthgB115wuL6ewlKBtfOXwfqevj2jpbdARQHB9pvIcc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 416
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
