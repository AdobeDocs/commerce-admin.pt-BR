---
title: Configurar máximo da lista de requisições
description: Saiba mais sobre a configuração da lista de requisições, que controla o número máximo que pode ser mantido para cada conta de cliente.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Configurar máximo da lista de requisições

Quando o recurso de lista de requisições estiver ativado, os clientes poderão criar várias listas de itens comprados com frequência e usar essas listas para colocação de ordem. Ele está disponível tanto para usuários conectados quanto para convidados. Você pode habilitar listas de requisições ao [configurar os recursos B2B](enable-basic-features.md).

Um cliente pode ter várias listas que se concentram em produtos de diferentes fornecedores, compradores, equipes, campanhas ou qualquer outra coisa que simplifique fluxos de trabalho comuns. [A funcionalidade da lista de requisições](requisition-lists.md) é semelhante às listas de desejos, com as seguintes diferenças:

- Uma lista de requisições não é apagada depois de enviar itens ao carrinho de compras. Ele pode ser usado várias vezes.
- A interface do usuário para listas de requisição usa uma exibição compacta para exibir muitos itens.

Por padrão, os clientes podem manter até 999 listas de requisições para suas contas. Mas você pode modificar a configuração e especificar um número mais baixo para diminuir a carga em seu armazenamento.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Requisition Lists]**.

   ![Listas de requisições - configuração geral](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Number of Requisition Lists]**, insira o número máximo de listas de requisições que podem ser mantidas para cada conta de cliente.

   O número mínimo é `2`, e o máximo é `999`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
