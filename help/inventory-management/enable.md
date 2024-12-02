---
title: Habilitar [!DNL Inventory Management]
description: Saiba como habilitar [!DNL Inventory Management] no nível de loja global ou de produto.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Habilitar [!DNL Inventory Management]

Para gerenciar o inventário de produtos, habilite o [!DNL Inventory Management] na loja global ou no nível do produto. Quando a opção _Gerenciar Estoque_ está habilitada, o [!DNL Inventory Management] rastreia automaticamente as quantidades de produtos disponíveis para o site por meio de estoques e fontes configuradas. Cada recurso e opção inicia o rastreamento e os relatórios quando ativados, sem configuração adicional.

Sua empresa executa e faz atualizações de inventário na velocidade das vendas. À medida que os clientes fazem compras, você recebe informações exatas e atualizadas sobre as ações disponíveis por canal e fonte de vendas. As Quantidades Venáveis Disponíveis são atualizadas por estoque quando os clientes adicionam produtos ao carrinho e concluem compras e quando e quando você gerencia pedidos, cria remessas e emite reembolsos. Chegadas de atualizações de estoque novas ou transferidas para suas fontes, imediatamente disponíveis para vendas online. Backorders são concluídos até os limites especificados sem ordens infinitas ou configurações adicionais. E você informa e conclui entregas parciais ou completas através de uma ou mais origens com recomendações, fornecendo controle total sobre o preenchimento da ordem e o inventário em estoque.

>[!NOTE]
>
>Por padrão, o [!DNL Inventory Management] é habilitado durante a instalação ou atualização do [!DNL Commerce]. Dependendo das suas necessidades comerciais, talvez você queira habilitar ou desabilitar o [!DNL Inventory Management] rastreado em [!DNL Commerce].

Como essa configuração funciona em inventários de uma ou várias origens:

- Para usar [!DNL Inventory Management], habilite _[!UICONTROL Manage Stock]_.

- As configurações de [!UICONTROL Manage Stock] no nível de produto substituem a configuração da loja.

- Para usar o Order Management ou serviços de terceiros (como ERP), desabilite [!UICONTROL Manage Stock].

- Se a configuração do nível de produto usar o padrão do sistema, a configuração da loja será substituída.

Com o [!DNL Inventory Management] habilitado, consulte o seguinte para definir todas as configurações:

- [Configurando Opções Globais](global-options.md) - Configurações que afetam todo o catálogo, consideradas as configurações padrão do sistema.

- [Configurando Opções de Produto](product-options.md) - Configurações de um produto específico que substitui as opções globais.

## Habilitar ou desabilitar [!DNL Inventory Management]

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Inventory]**.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) _Opções do Estoque de Produtos_ e configure:

   ![Opções de Estoque de Produtos](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Para gerenciar o inventário e usar todos os recursos do [!DNL Commerce], defina **[!UICONTROL Manage Stock]** como `Yes` (padrão).

   - Para desativar [!DNL Inventory Management], desmarque a caixa de seleção **[!UICONTROL Use system value]** e defina **[!UICONTROL Manage Stock]** como `No`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Gerenciar estoque de uma loja

Consulte [Configurar Opções Globais](global-options.md).

## Gerenciar estoque de um produto

Consulte [Configurando Opções de Produto](product-options.md).
