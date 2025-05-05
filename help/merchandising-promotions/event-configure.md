---
title: Configurar eventos
description: Saiba como concluir a configuração básica para ativar eventos e configurar o bloco de eventos na barra lateral da loja.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Configurar eventos

{{ee-feature}}

Antes de criar um evento, você deve concluir a configuração básica para ativar eventos e configurar o bloco de eventos na barra lateral.

## Ativar e configurar eventos

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** abaixo de.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Catalog Events]** e faça o seguinte:

   ![Configuração de catálogo - eventos de catálogo](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Defina **[!UICONTROL Enable Catalog Events Functionality]** como `Yes`.

   - Defina **[!UICONTROL Enable Catalog Event Widget on Storefront]** como `Yes`.

   - Insira o **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Por padrão, esse valor está definido como `5`. Para exibir apenas um evento no controle deslizante por vez, digite `1`.

   - Insira o número de **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Por padrão, esse valor está definido como `2`. Se desejar que o controle deslizante exiba o próximo evento em sequência quando clicado, digite `1`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Restrições de acesso

O acesso a uma venda, evento ou site privado pode ser limitado a clientes registrados que fazem logon ou estendido a clientes não registrados que devem se registrar antes de obter acesso.

![Configuração geral - restrições de site](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Restringir acesso

O acesso a uma venda, evento ou site privado pode ser limitado a clientes registrados que fazem logon ou estendido a clientes não registrados que devem se registrar antes de obter acesso.

![Configuração geral - restrições de site](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL General]** e escolha **[!UICONTROL General]** abaixo de.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Website Restrictions]**.

1. Defina **[!UICONTROL Access Restriction]** como `Yes`.

1. Defina **[!UICONTROL Restriction Mode]** como um dos seguintes:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Defina **[!UICONTROL Startup Page]** como um dos seguintes:

   - `To login form (302 Found)` - Os usuários são redirecionados para o formulário de logon antes de obter acesso ao site.

   - `To landing page (302 Found)` - Os usuários são redirecionados para a página de aterrissagem especificada até que façam logon.

     >[!IMPORTANT]
     >
     >Certifique-se de incluir um link para a página de logon da página de destino para que os clientes possam fazer logon para acessar o site.

1. Escolha o **[!UICONTROL Landing Page]** que aparece antes que os clientes façam logon no site de venda particular.

1. Para permitir que bots e spiders de mecanismo de pesquisa saibam que a página de aterrissagem está correta e que não há outras páginas no site a serem indexadas, defina **[!UICONTROL HTTP Response]** como `200 OK`.

   Em todos os outros casos, defina como `503 Service Unavailable`.

   >[!NOTE]
   >
   >Aplicável somente se o modo de restrição estiver definido como _Site Fechado_. A página de aterrissagem é renderizada como HTML bruto.

1. Se quiser que os campos nos formulários de logon do cliente e senha esquecida sejam preenchidos automaticamente a partir de entradas anteriores, defina **[!UICONTROL Enable Autocomplete on login/forgot password forms]** como `Yes`.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

### Restringir vendas

Por padrão, os produtos que aparecem em eventos futuros ou fechados não estão disponíveis para venda geral e o botão _[!UICONTROL Add to Cart]_&#x200B;não aparece na lista de produtos ou na página de produtos.

Para restaurar o botão _[!UICONTROL Add to Cart]_&#x200B;para um evento fechado, o evento deve ser excluído (consulte [Atualizar eventos](event-create.md#update-events)). No entanto, se um produto estiver associado a outra categoria que não tem restrições de venda, o botão estará disponível na página do produto. Da mesma forma, o bloco de ticker não será exibido na página do produto se o produto estiver associado a outra categoria que não tenha restrições de venda.
