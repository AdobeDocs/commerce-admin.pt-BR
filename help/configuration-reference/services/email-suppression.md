---
title: '[!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]'
description: Revise as configurações na página [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression] do Administrador do Commerce.
feature: Configuration, Communications
badgeSaas: label="Somente SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplicável somente a projetos do Adobe Commerce as a Cloud Service e do Adobe Commerce Optimizer (infraestrutura SaaS gerenciada pela Adobe)."
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
source-git-commit: f4d7033067a99421224ab2159b1b95775e5e949f
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]

{{config}}

O [!UICONTROL Email Suppression] permite que os administradores desativem categorias específicas de email automatizado do sistema sem afetar o restante do email da loja ou exigir o envolvimento do desenvolvedor. Use esse recurso para interromper temporária ou permanentemente determinadas notificações, por exemplo, emails de pedidos durante uma migração de dados ou emails de marketing.

>[!IMPORTANT]
>
>Notificações de administrador relacionadas à segurança, como códigos de autenticação de dois fatores e emails de redefinição de senha de administrador, nunca são suprimidas por esse recurso.

As configurações desta página se aplicam por [exibição de loja](../../getting-started/websites-stores-views.md#scope-settings) para que você possa suprimir diferentes categorias de email para diferentes vitrines.

>[!NOTE]
>
>Desativar a supressão imediatamente restaura o delivery de email normal, mas os emails enviados durante o período de supressão não são enfileirados.

## [!UICONTROL Email Suppression]

![Supressão de email](./assets/email-suppression.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Email Suppression] | Exibição da loja | Chave principal liga/desliga para o recurso. Quando definido como `No` (padrão), qualquer outra configuração nesta página é ignorada e todos os emails são enviados normalmente. |
| [!UICONTROL Disabled Functional Areas] | Exibição da loja | Selecione uma ou mais categorias comerciais cujos emails são suprimidos. Consulte [Categorias comerciais](#business-categories) para saber o que cada categoria inclui. |
| [!UICONTROL Disabled Template IDs] | Exibição da loja | Lista opcional separada por vírgulas de modelos de email específicos a serem suprimidos individualmente, independentemente da categoria. Use o código do modelo (por exemplo, `customer_password_forgot_email_template`) ou a ID numérica do modelo para um modelo personalizado que você criou no Administrador. |

{style="table-layout:auto"}

### Categorias comerciais {#business-categories}

| Categoria | Emails típicos incluídos |
|--- |--- |
| Conta do cliente | Criação de conta, redefinição de senha, alterações nas informações da conta. |
| Order Management | Confirmação da ordem, NFF, entrega, aviso de crédito e cancelamento da ordem. |
| Devoluções (RMA) | Notificações de autorização para devolução de mercadorias. |
| Check-out e pagamento | Emails relacionados a check-out e pagamento por link. |
| Marketing | Boletins informativos, alertas de produto, compartilhamento de lista de desejos, enviar um email para um amigo, lembretes, convites, registro de presentes. |
| Crédito e prêmios da loja | Cartões-presente, pontos de recompensa, alterações no saldo de crédito da loja. |
| B2B | Notificações de empresa, cotação negociável e ordem de compra. |
| Notificações do sistema | Notificações operacionais, como importação, exportação e emails de formulário de contato programados. |

{style="table-layout:auto"}
