---
title: Configuração de design
description: A Configuração de design facilita a edição de regras e definições de configuração relacionadas ao design, exibindo as configurações em uma única página.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Configuração de design

A configuração Design facilita a edição de regras e definições de configuração relacionadas ao design, exibindo as configurações em uma única página.

![Página Configuração de design](./assets/configuration.png){width="700" zoomable="yes"}

## Alterar a configuração de design

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de loja que deseja configurar e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

   A página exibe as configurações de design atuais para a exibição de loja.

1. Para alterar o tema padrão, defina **[!UICONTROL Applied Theme]** ao tema que deseja aplicar à exibição.

   Se nenhum tema for especificado, o tema padrão do sistema será usado. Algumas extensões de terceiros modificam o tema padrão do sistema.

1. Se o tema deve ser usado apenas para um dispositivo específico, defina o **[!UICONTROL User Agent Rules]**.

   ![Regras de usuário-agente](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   Para cada tipo de dispositivo em que você deseja especificar um tema:

   - Clique em **[!UICONTROL Add New User Agent Rule]**.

   - Para **[!UICONTROL Search String]**, digite a ID do navegador do dispositivo específico.

     Uma string de pesquisa pode ser uma expressão normal ou uma expressão regular compatível com Perl (PCRE) (consulte [Agente do usuário](https://en.wikipedia.org/wiki/User_agent) para obter mais informações). A sequência de pesquisa a seguir identifica o Firefox:

         /^mozilla/i
     
   - Para **[!UICONTROL Theme Name]**, escolha o tema a ser usado para o dispositivo especificado.

   >[!NOTE]
   >
   >É possível adicionar quantas regras desejar para os dispositivos designados. As cadeias de caracteres de pesquisa são correspondidas na ordem em que são inseridas.

1. Em _[!UICONTROL Other Settings]_, expanda cada seção e siga as instruções nos tópicos vinculados para editar as configurações, conforme necessário.

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![Outras configurações que afetarão o design](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.
