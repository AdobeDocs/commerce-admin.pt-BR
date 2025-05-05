---
title: Integração do Adobe Experience Cloud para o administrador do Commerce
description: Saiba mais sobre a extensão de experiência unificada de administração que integra o Commerce com o Experience Cloud para que os clientes possam acessar projetos do Commerce na página inicial do Experience Cloud.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: 61874f3dac4f574ad393e8ae258f3d6c56c8f37e
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Integração do Adobe Experience Cloud para o Commerce

<table style="border:1px solid red">
<tr><td><img alt="Recurso do Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Recurso exclusivo somente no Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=pt-BR#product-editions">Saiba mais</a>)</td></tr>
</table>

Integre projetos do Adobe Commerce com o Experience Cloud ativando a extensão Admin Unified Experience. Quando a integração estiver ativa, os administradores poderão acessar os projetos da Commerce no Adobe Experience Cloud.

![Acessar o Commerce pela home page do Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Exibir projetos disponíveis do Commerce

Os administradores podem exibir os projetos do Commerce aos quais têm permissão de acesso selecionando **[!UICONTROL Commerce]** na home page do Experience Cloud.

![Espaço de trabalho do Commerce Projects no Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Os administradores podem abrir o Administrador e a Loja para cada projeto no espaço de trabalho [!DNL Commerce Projects] e exibir informações adicionais.

- **Instantâneo da home page da loja da Commerce**—Instantâneo da home page da loja. Se um projeto tiver vários sites, o instantâneo mostrará a página inicial do site padrão.

- **[Nome do projeto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=pt-BR)** — Identifica o ambiente do projeto de nuvem da instância. O nome padrão do Projeto é o [nome da ramificação Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html?lang=pt-BR) no projeto de nuvem. Altere ou atualize o nome do projeto nas [configurações do Repositório de Experiência Unificado](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[URL da Loja](../stores-purchase/store-urls.md)** — Mostra a URL base do site padrão.

- **[Tipo de ambiente](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=pt-BR)** — as instâncias do Commerce implantadas em um ambiente de desenvolvimento ou de preparo são identificadas com um rótulo [!UICONTROL Development] ou [!UICONTROL Staging]. As instâncias que não têm um rótulo são implantadas em um ambiente de Produção.

- **Acesso de Administrador do Commerce**—Abra o Administrador clicando em **[!UICONTROL Open]**.

- **Acesso à vitrine**—Abra a vitrine selecionando **[!UICONTROL Open storefront]** no menu de opções.

- **Acesso rápido para selecionar projetos**—Selecione **[!UICONTROL Add to Favorites]** no menu de opções para adicionar um projeto à guia [!UICONTROL Favorites].

## Fluxo de autenticação

Quando a integração Experience Cloud estiver habilitada, os administradores usarão o fluxo de trabalho a seguir para autenticar e acessar projetos Commerce.

1. Faça logon por meio da página de logon do Experience Cloud.

   ![Página de Entrada do Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Os administradores devem fazer logon no Experience Cloud com o perfil de negócios Adobe para a organização associada à instância do Commerce. Consulte [Gerenciar perfis de Adobe](https://helpx.adobe.com/br/enterprise/using/manage-adobe-profiles.html).

1. Na página inicial do Experience Cloud, abra o [!UICONTROL Commerce Projects workspace] selecionando **[!UICONTROL Open]**.

1. Acesse o Administrador de um projeto selecionando **[!UICONTROL Open]**.

1. Na página Logon do Adobe Commerce, selecione **[!UICONTROL Sign in with Adobe ID]** para concluir a autenticação e abrir o Administrador.

   ![Página de Entrada do Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Consulte [Gerenciar a Integração de Experience Cloud](admin-unified-experience-integration-manage.md) para obter detalhes sobre como o fluxo de trabalho de autenticação é afetado quando a integração de Experience Cloud é habilitada ou desabilitada.

## Requisitos

- Adobe Commerce 2.4.5 ou posterior
- Adobe Commerce na infraestrutura em nuvem
- Extensões do Adobe Commerce

   - Extensão de experiência unificada do administrador do Commerce (`magento/module-unified-experience`)

     Se o módulo não estiver disponível na instância do Commerce, ele poderá ser instalado usando o Composer.

   - [Serviço de Eventos Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/)—Necessário para enviar dados do evento para gerenciar o acesso de administrador aos projetos Commerce a partir do Experience Cloud.

     A integração de Adobe I/O Events com o Commerce é habilitada pela extensão de Evento do Commerce (`magento/commerce-eventing`) que está disponível com o Adobe Commerce 2.4.4 e versões posteriores.

## Habilitar a integração

Habilite a integração seguindo as instruções para [Configurar a Integração do Experience Cloud com o Administrador do Commerce](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Se a integração de Experience Cloud já estiver habilitada na instância do Commerce, consulte [Gerenciar a Integração de Experience Cloud](admin-unified-experience-integration-manage.md) para obter detalhes sobre como alterar ou atualizar a configuração, gerenciar o acesso do administrador e solucionar problemas.
