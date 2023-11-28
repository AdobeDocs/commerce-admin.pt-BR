---
title: Permissões de administrador
description: Saiba mais sobre as contas de usuário administrador e como as funções são usadas para conceder acesso às funções de gerenciamento de armazenamento.
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Permissões de administrador

O Adobe Commerce e o Magento Open Source usam funções e permissões para criar diferentes níveis de acesso ao Administrador. Quando o armazenamento é configurado pela primeira vez, você recebe um conjunto de credenciais de logon para a função de Administrador com permissões totais. No entanto, é possível restringir o nível de permissões com base no &quot;conhecimento necessário&quot; para outras pessoas que trabalham no site. Por exemplo, um membro da equipe de design pode receber acesso somente às ferramentas de design de conteúdo, mas não às áreas com informações de clientes e pedidos.

Além disso, você pode restringir ainda mais o acesso de Administrador a apenas um site específico ou conjunto de sites e seus dados associados. Se você tiver várias marcas ou unidades de negócios com lojas separadas na mesma instalação do Commerce, poderá fornecer acesso de Administrador a cada unidade de negócios, mas ocultar e proteger seus dados de outros usuários Administradores.

Quando o acesso de um usuário administrador é restrito a um site ou loja específica, aqueles em que ele não está autorizado não estão visíveis ou aparecem esmaecidos. Somente os dados de vendas e outros dados de sites e lojas permitidos são exibidos para o usuário.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Por padrão, o sistema registra automaticamente (registra) todas as ações executadas por um usuário quando ele aplica alterações a uma loja. As ações de administrador podem ser revisadas no [Relatório de Logs de Ação](action-log-report.md). Configurar logon [Registro de ações do administrador](action-log.md) nas configurações administrativas avançadas da sua loja.

![Administrador - todas as contas de usuário](./assets/users-all.png){width="700" zoomable="yes"}
