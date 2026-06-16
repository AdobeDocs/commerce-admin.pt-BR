---
title: Permissões de administrador
description: Saiba mais sobre as contas de usuário administrador e como as funções são usadas para conceder acesso às funções de gerenciamento de armazenamento.
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
TQID: https://experienceleague.adobe.com/7xyouYohAbOKbwVCxZPamD-7gEiqGrqEAAg9FDm8z-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# Permissões de administrador

O Adobe Commerce e o Magento Open Source usam funções e permissões para criar diferentes níveis de acesso ao Administrador. Quando o armazenamento é configurado pela primeira vez, você recebe um conjunto de credenciais de logon para a função de Administrador com permissões totais. No entanto, é possível restringir o nível de permissões com base no &quot;conhecimento necessário&quot; para outras pessoas que trabalham no site. Por exemplo, um membro da equipe de design pode receber acesso somente às ferramentas de design de conteúdo, mas não às áreas com informações de clientes e pedidos.

Além disso, você pode restringir ainda mais o acesso de Administrador a apenas um site específico ou conjunto de sites e seus dados associados. Se você tiver várias marcas ou unidades de negócios com lojas separadas na mesma instalação do Commerce, poderá fornecer acesso de administrador a cada unidade de negócios, mas ocultar e proteger seus dados de outros usuários administradores.

Quando o acesso de um usuário administrador é restrito a um site ou loja específica, aqueles em que ele não está autorizado não estão visíveis ou aparecem esmaecidos. Somente os dados de vendas e outros dados de sites e lojas permitidos são exibidos para o usuário.

- ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Por padrão, o sistema registra automaticamente em log (registra) todas as ações executadas por um usuário quando ele aplica alterações a um armazenamento. As ações de administrador podem ser revisadas no [Relatório de Logs de Ação](action-log-report.md). Configure o logon em [Logon de Ações do Administrador](action-log.md) nas configurações administrativas avançadas do armazenamento.

![Administrador - todas as contas de usuário](./assets/users-all.png){width="700" zoomable="yes"}
