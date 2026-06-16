---
title: O que é o administrador?
description: Saiba mais sobre o [!DNL Commerce] Administrador, o local onde os comerciantes configuram produtos e promoções, gerenciam pedidos e executam outras tarefas administrativas.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
TQID: https://experienceleague.adobe.com/A0DuYohA907-EHXQ6fyy2Sz83Y6cFZ7PDY5SmtBa14Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 0%

---

# O que é o administrador?

A loja _Admin_ é o back office protegido por senha onde você, como comerciante, configura produtos e promoções, gerencia pedidos e executa outras tarefas administrativas. Todas as tarefas básicas de configuração e operações de gerenciamento de repositório são executadas pelo _Administrador_.

Para maior segurança, o logon de _Administrador_ é protegido por [autenticação de dois fatores](../systems/security-two-factor-authentication.md) e pode ser configurado para exigir um [CAPTCHA](../systems/security-captcha.md). Para saber mais, acesse [Configurando a Segurança do Administrador](../systems/security-admin.md).

![Barra lateral e painel do administrador](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Suas credenciais iniciais de [entrada](admin-signin.md) foram configuradas durante a instalação do Adobe Commerce ou do Magento Open Source. Se você esquecer a senha, uma senha temporária poderá ser enviada para o endereço de email associado à conta. Para aumentar a segurança, configure seu armazenamento para exigir um nome de usuário com diferenciação de maiúsculas e minúsculas e uma senha forte.

Além da conta de usuário Admin padrão, sua empresa pode criar quantas [contas adicionais](../systems/permissions-users-all.md) forem necessárias para gerenciar as contas de cliente de armazenamento e suporte. Cada conta pode ser associada a uma [função](../systems/permissions-user-roles.md) específica e a um nível de acesso, com base na empresa _que você precisa saber_. O endereço de email associado a cada conta de usuário Administrador deve ser exclusivo.

{{ims-admin-note}}

## Coleta de dados de uso

Na primeira vez que você fizer logon no _Administrador_, será solicitado a conceder permissão Adobe para coletar dados de uso para todos os usuários Administradores. Ao permitir a coleta de dados de uso pelo administrador, você ajuda a Adobe a melhorar a experiência de uso do administrador do Adobe Commerce e de produtos e serviços relacionados.

![Permitir coleta de dados de uso administrativo](./assets/admin-usage-data.png){width="600"}

Os usuários individuais não são identificados nos dados de uso. A configuração de coleta de dados pode ser alterada a qualquer momento a partir da configuração de [Uso do Administrador](../configuration-reference/advanced/admin.md#admin-usage).

Para o Adobe Commerce, permitir a coleta de dados também habilita o _Guia no Produto_, que foi projetado para trazer conteúdo interativo para o _Administrador_. Ele fornece ajuda, dicas de ferramentas, guias passo a passo, informações de integração, anúncios de recursos e muito mais.
