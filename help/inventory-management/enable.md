---
title: Habilitar [!DNL Inventory Management]
description: Saiba como habilitar [!DNL Inventory Management] no nível de loja global ou de produto.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/evCX34nY-m7WQnZt3xw7ng6-It7Xlf5DTanjKbP1fCk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 337
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
