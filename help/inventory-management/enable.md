---
title: "Ativar [!DNL Inventory Management]"
description: Saiba como habilitar [!DNL Inventory Management] no nível de loja global ou de produto.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Ativar [!DNL Inventory Management]

Para gerenciar o inventário de produtos, ative o [!DNL Inventory Management] no nível de loja global ou de produto. Quando a variável _Gerenciar estoque_ estiver ativada, [!DNL Inventory Management] rastreia automaticamente as quantidades de produtos disponíveis para o site por meio de estoques e fontes configurados. Cada recurso e opção inicia o rastreamento e os relatórios quando ativados, sem configuração adicional.

Sua empresa executa e faz atualizações de inventário na velocidade das vendas. À medida que os clientes fazem compras, você recebe informações exatas e atualizadas sobre as ações disponíveis por canal e fonte de vendas. As Quantidades Venáveis Disponíveis são atualizadas por estoque quando os clientes adicionam produtos ao carrinho e concluem compras e quando e quando você gerencia pedidos, cria remessas e emite reembolsos. Chegadas de atualizações de estoque novas ou transferidas para suas fontes, imediatamente disponíveis para vendas online. Backorders são concluídos até os limites especificados sem ordens infinitas ou configurações adicionais. E você informa e conclui entregas parciais ou completas através de uma ou mais origens com recomendações, fornecendo controle total sobre o preenchimento da ordem e o inventário em estoque.

>[!NOTE]
>
>Por padrão, [!DNL Inventory Management] está habilitado ao instalar ou atualizar [!DNL Commerce]. Dependendo das necessidades da sua empresa, talvez você queira ativar ou desativar o [!DNL Inventory Management] no prazo de [!DNL Commerce].

Como essa configuração funciona em inventários de uma ou várias origens:

- Para usar [!DNL Inventory Management], ativar _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] as configurações no nível de produto substituem a configuração da loja.

- Para usar o Order Management ou serviços de terceiros (como ERP), desative [!UICONTROL Manage Stock].

- Se a configuração do nível de produto usar o padrão do sistema, a configuração da loja será substituída.

Com [!DNL Inventory Management] habilitado, consulte o seguinte para definir todas as configurações:

- [Configuração de opções globais](global-options.md) - Configurações que afetam todo o catálogo, consideradas as configurações padrão do sistema.

- [Configuração das opções de produto](product-options.md) - Configurações de um produto específico que substitui as opções globais.

## Ativar ou desativar [!DNL Inventory Management]

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Inventory]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) _Opções de estoque do produto_ e configure:

   ![Opções de estoque do produto](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Para gerenciar o inventário e usar todas as [!DNL Commerce] recursos, definir **[!UICONTROL Manage Stock]** para `Yes` (padrão).

   - Para desativar [!DNL Inventory Management], desmarque a opção **[!UICONTROL Use system value]** caixa de seleção e definir **[!UICONTROL Manage Stock]** para `No`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Gerenciar estoque de uma loja

Consulte [Configurar opções globais](global-options.md).

## Gerenciar estoque de um produto

Consulte [Configuração das opções de produto](product-options.md).
