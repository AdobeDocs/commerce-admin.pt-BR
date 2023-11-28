---
title: O que é o administrador?
description: Saiba mais sobre o [!DNL Commerce] Administrador, o local onde os comerciantes configuram produtos e promoções, gerenciam pedidos e executam outras tarefas administrativas.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# O que é o administrador?

Sua loja _Admin_ O é o back office protegido por senha onde você, como comerciante, configura produtos e promoções, gerencia pedidos e executa outras tarefas administrativas. Todas as tarefas básicas de configuração e operações de gerenciamento de armazenamento são executadas no _Admin_.

Para obter segurança adicional, a variável _Admin_ o logon está protegido por [autenticação de dois fatores](../systems/security-two-factor-authentication.md)e podem ser configuradas para exigir uma [CAPTCHA](../systems/security-captcha.md). Para saber mais, acesse [Configuração da segurança do administrador](../systems/security-admin.md).

![Barra lateral e painel do administrador](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Seu inicial [fazer logon](admin-signin.md) as credenciais do foram configuradas durante a instalação do Adobe Commerce ou do Magento Open Source. Se você esquecer a senha, uma senha temporária poderá ser enviada para o endereço de email associado à conta. Para aumentar a segurança, configure seu armazenamento para exigir um nome de usuário com diferenciação de maiúsculas e minúsculas e uma senha forte.

Além da conta de usuário Admin padrão, sua empresa pode criar quantos [contas adicionais](../systems/permissions-users-all.md) que você precisa para gerenciar as contas de cliente de armazenamento e suporte. Cada conta pode ser associada a um [função](../systems/permissions-user-roles.md) e nível de acesso, com base nas _precisa saber_. O endereço de email associado a cada conta de usuário Administrador deve ser exclusivo.

{{ims-admin-note}}

## Coleta de dados de uso

Na primeira vez que você fizer logon na _Admin_, você será solicitado a conceder permissão de Adobe para coletar dados de uso para todos os usuários administradores. Ao permitir a coleta de dados de uso pelo administrador, você ajuda o Adobe a melhorar a experiência de uso do administrador do Adobe Commerce e de produtos e serviços relacionados.

![Permitir coleta de dados de uso administrativo](./assets/admin-usage-data.png){width="600"}

Os usuários individuais não são identificados nos dados de uso. A configuração de coleta de dados pode ser alterada a qualquer momento no [Uso do administrador](../configuration-reference/advanced/admin.md#admin-usage) configuração.

No Adobe Commerce, permitir a coleta de dados também permite _Orientação no produto_, que foi projetado para trazer conteúdo interativo à _Admin_. Ele fornece ajuda, dicas de ferramentas, guias passo a passo, informações de integração, anúncios de recursos e muito mais.
