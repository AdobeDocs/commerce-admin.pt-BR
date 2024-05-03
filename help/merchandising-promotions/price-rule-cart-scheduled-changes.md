---
title: Alterações agendadas para regras de preço do carrinho
description: Saiba como aplicar regras de preço do carrinho de compras conforme agendado como parte de uma campanha e agrupado com outras alterações de conteúdo.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Alterações agendadas para regras de preço do carrinho

{{ee-feature}}

As regras de preço do carrinho podem ser aplicadas de acordo com a programação como parte de uma campanha e agrupadas com outras alterações de conteúdo. Você pode criar uma campanha com base em alterações programadas em uma regra de preço ou aplicar as alterações a uma campanha existente.

>[!NOTE]
>
>A variável [!UICONTROL From] e [!UICONTROL To] os campos foram removidos em ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce e não podem ser modificados diretamente na regra de preço do carrinho. Você deve criar uma atualização agendada para essas ativações.

![Regras de preço do carrinho - alterações programadas](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Todas as atualizações programadas são aplicadas consecutivamente. Isso significa que qualquer entidade pode ter apenas uma atualização agendada em um ponto do tempo. Qualquer atualização agendada é aplicada a todas as exibições de loja dentro de seu período de tempo. Como resultado, uma entidade não pode ter atualizações agendadas diferentes para exibições de loja diferentes ao mesmo tempo. Todos os valores de atributo de entidade em todas as exibições de armazenamento, que não são afetados pela atualização agendada atual, são obtidos dos valores padrão, e não da atualização agendada anterior.

Se houver várias regras de preço em execução na mesma campanha, a variável _[!UICONTROL Priority]_a configuração da regra de preço determina qual regra tem prioridade. Para saber mais, consulte [Preparo de conteúdo](../content-design/content-staging.md).

Lembre-se dos seguintes avisos:

- Se uma campanha que inclui uma regra de preço for criada inicialmente sem uma data final, a campanha não poderá ser editada posteriormente para incluir uma data final. É recomendável adicionar uma data de término ao criar a campanha ou criar uma versão duplicada da campanha existente e adicionar a data de término à duplicação, conforme necessário.
- Ao usar uma atualização agendada para habilitar uma regra de preço de carrinho com uma data final, defina a regra como desabilitada inicialmente. As regras que já estão ativas não respeitam a data final.
- Os cupons não estão conectados às regras de preço do carrinho. Uma Atualização programada não fornece acesso à _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_, e_[!UICONTROL Uses per Customer]_ campos no _[!UICONTROL Rule Information]_guia. Além disso, todas as configurações do_[!UICONTROL Manage Coupon Codes]_ não estão disponíveis.

>[!IMPORTANT]
>
>Campaign **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** deve ser definido usando o **_padrão_** Fuso horário do administrador, que é convertido do fuso horário local de cada site. Considere um exemplo em que você tem vários sites em fusos horários diferentes, mas deseja iniciar a campanha com base em um fuso horário dos EUA. Nesse caso, você precisa agendar uma atualização separada para cada fuso horário local e definir **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** convertido de cada fuso horário do site local para o fuso horário padrão do Administrador.
