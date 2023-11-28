---
title: Desabilitar origens de estoque
description: Saiba como desabilitar fontes e modificar informações, incluindo localização e ponto de contato.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Desabilitar fontes

Para garantir que todos os dados de pedido sejam mantidos em [!DNL Commerce], as origens não podem ser excluídas. Origens, pedidos e entregas estão diretamente conectados uns aos outros. Você pode desabilitar fontes e modificar informações, incluindo local e ponto de contato.

Dependendo do status de suas localizações, talvez você queira desativar uma origem. Uma origem desabilitada retém todas as atribuições por estoques e produtos, mas não é acessada para estoque e ordens.

Quando uma origem é desabilitada:

- [!DNL Inventory Management] ignora e não lista a origem para entrega ou processamento de ordem.
- Os estoques não acessam quantidades de estoque da origem para totais de estoque agregados.
- As entregas de ordem não podem ser atribuídas a locais desativados.

Não é possível desativar a Origem padrão. [!DNL Commerce] O usa essa fonte para todos os produtos novos e importados, para produtos de pacote e para suporte a sistemas de terceiros. Você pode ativar ou desativar fontes personalizadas a qualquer momento.

Configuração de uma origem para `disabled` O é útil para as seguintes situações:

- Adição de uma loja ou depósito - À medida que você abre novas lojas ou ativa novos depósitos e locais de remessa, adicione uma entrada de origem para configurar o inventário de produtos usando a importação e conectar a estoques em potencial.
- Remessas sazonais - Feriados podem ser uma época movimentada do ano. Você pode restringir o envio somente de locais de remessa específicos, como depósitos, para manter os locais tradicionais bem estocados e focados nos compradores locais. Ou você pode adicionar novos locais de remessa por um tempo limitado para lidar com taxas mais altas de ordens de venda e de entrada.
- Fechando um local - Ao fechar um local para movimentação para novas instalações ou permanentemente, desative para interromper novas entregas do local.

## Desativar uma ou mais fontes personalizadas

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Marque a caixa de seleção de cada origem personalizada habilitada que você deseja desabilitar.

1. Clique em _Ações_ no canto superior esquerdo e escolha **[!UICONTROL Disable]**.

   ![[!DNL Inventory Management] fontes - menu Ações](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. Na caixa de diálogo de confirmação, clique em **[!UICONTROL OK]**.

## Ativar ou desativar uma única fonte personalizada

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Localize uma fonte personalizada e clique em **[!UICONTROL Edit]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o _Geral_ seção e alteração **[!UICONTROL Is Enabled]**:

   | Opção | Descrição |
   | ----- | ----- |
   | `Yes` | Origem ativada. A quantidade é adicionada à Quantidade Venável. A origem faz uma lista com a quantidade atual ao entregar ordens. O Algoritmo de Seleção de Origem verifica a origem para entrega. |
   | `No` | Origem desabilitada. As quantidades não são adicionadas às Quantidades Venáveis. A origem não é listada ao encaminhar ordens. As opções de remessa ignoram esta origem. |

1. Clique em **[!UICONTROL Save and Close]**.
