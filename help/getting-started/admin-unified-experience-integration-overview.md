---
title: Integração do Adobe Experience Cloud para o administrador do Commerce
description: Saiba mais sobre a extensão Admin Unified Experience que integra o Commerce ao Experience Cloud para que os clientes possam acessar projetos do Commerce na página inicial do Experience Cloud.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Integração do Adobe Experience Cloud para o Commerce

{{ee-feature}}

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Integre projetos do Adobe Commerce com o Experience Cloud ativando a extensão Admin Unified Experience. Quando a integração está ativa, os administradores podem acessar projetos do Commerce no Adobe Experience Cloud.

![Acessar o Commerce na home page do Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Exibir projetos do Commerce disponíveis

Os administradores podem exibir os projetos de comércio aos quais têm permissão de acesso selecionando **[!UICONTROL Commerce]** na página inicial do Experience Cloud.

![Espaço de trabalho de Projetos do Commerce no Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Os administradores podem abrir o Administrador e a Loja para cada projeto no [!DNL Commerce Projects] espaço de trabalho e exibir informações adicionais.

- **Instantâneo da página inicial da vitrine do Commerce**—Instantâneo da home page da loja. Se um projeto tiver vários sites, o instantâneo mostrará a página inicial do site padrão.

- **[Nome do projeto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Identifica o ambiente do projeto de nuvem para a instância. O nome do projeto é padronizado como [Nome da ramificação Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) no projeto na nuvem. Alterar ou atualizar o nome do projeto no [Configurações da loja de experiência unificada](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[URL da vitrine](../stores-purchase/store-urls.md)**—Mostra o URL base do site padrão.

- **[Tipo de ambiente](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**— As instâncias de comércio implantadas em um ambiente de desenvolvimento ou de preparo são identificadas com um [!UICONTROL Development] ou [!UICONTROL Staging] rótulo. As instâncias que não têm um rótulo são implantadas em um ambiente de Produção.

- **Acesso de administrador do Commerce**—Abra o Admin clicando em **[!UICONTROL Open]**.

- **Acesso à vitrine**—Abra a loja selecionando **[!UICONTROL Open storefront]** no menu opções.

- **Acesso rápido a projetos selecionados**— Select **[!UICONTROL Add to Favorites]** no menu opções para adicionar um projeto à [!UICONTROL Favorites] guia.

## Fluxo de autenticação

Quando a integração Experience Cloud estiver habilitada, os administradores usarão o fluxo de trabalho a seguir para autenticar e acessar projetos do Commerce.

1. Faça logon por meio da página de logon do Experience Cloud.

   ![Página de logon do Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Os administradores devem fazer logon no Experience Cloud com o perfil de negócios Adobe para a organização associada à instância de comércio. Consulte [Gerenciar perfis de Adobe](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Na página inicial do Experience Cloud, abra a variável [!UICONTROL Commerce Projects workspace] selecionando **[!UICONTROL Open]**.

1. Acesse o administrador de um projeto selecionando **[!UICONTROL Open]**.

1. Na página Fazer logon no Adobe Commerce, selecione **[!UICONTROL Sign in with Adobe ID]** para concluir a autenticação e abrir o Admin.

   ![Página de logon do Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Consulte [Gerenciar a integração de Experience Cloud](admin-unified-experience-integration-manage.md) para obter detalhes sobre como o fluxo de trabalho de autenticação é afetado quando a integração de Experience Cloud é habilitada ou desabilitada.

## Requisitos

- Adobe Commerce 2.4.5 ou posterior
- Adobe Commerce na infraestrutura em nuvem
- Extensões do Adobe Commerce

   - Extensão da experiência unificada do administrador do Commerce (`magento/module-unified-experience`)

     Se o módulo não estiver disponível na instância do Commerce, ele poderá ser instalado usando o Composer.

   - [Serviço de Eventos Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/)—Obrigatório para enviar dados do evento para gerenciar o acesso de administradores a projetos do Commerce a partir do Experience Cloud.

     A integração de Adobe I/O Events com o Commerce é habilitada pela extensão Commerce Event (`magento/commerce-eventing`) que está disponível com o Adobe Commerce 2.4.4 e versões posteriores.

## Habilitar a integração

Habilite a integração seguindo as instruções para [Configurar a integração do Experience Cloud com o administrador de comércio](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Se a integração de Experience Cloud já estiver habilitada na instância do Commerce, consulte [Gerenciar a integração de Experience Cloud](admin-unified-experience-integration-manage.md) para obter detalhes sobre como alterar ou atualizar a configuração, gerenciar o acesso do administrador e solucionar problemas.
