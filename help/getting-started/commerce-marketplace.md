---
title: '[!DNL Adobe Commerce Marketplace]'
description: Saiba mais sobre o  [!DNL Commerce Marketplace], que oferece aos comerciantes uma seleção de soluções com curadoria e fornece aos desenvolvedores qualificados as ferramentas, a plataforma e o local ideal para criar um negócio próspero.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 7b5c331625e4c4dab0e41156722c4a8deb4aa4c0
workflow-type: tm+mt
source-wordcount: '1293'
ht-degree: 0%

---

# Adobe Commerce Marketplace

O [Adobe Commerce Marketplace][1] é a loja de aplicativos que oferece aos comerciantes uma seleção de soluções com curadoria e fornece aos desenvolvedores qualificados as ferramentas, a plataforma e o local ideal para criar um negócio próspero. O [!DNL Commerce Marketplace] oferece uma seleção de extensões que estão disponíveis gratuitamente e outras que estão à venda. As compras podem ser pagas com cartão de crédito ou [PayPal][2].

Todas as extensões disponíveis em [!DNL Commerce Marketplace] passaram por uma revisão abrangente. O [Programa de Qualidade de Extensão][3] (EQP) combina o conhecimento especializado [!DNL Commerce], as diretrizes de desenvolvimento e as ferramentas de verificação para garantir que todas as extensões no Commerce Marketplace atendam aos padrões de codificação e às práticas recomendadas. O processo de revisão inclui uma verificação automatizada e uma revisão manual de controle de qualidade. Durante o processo, a estrutura e o código de cada extensão são examinados e testados em busca de evidências de infecção por vírus/malware e qualquer indicação de plágio. A revisão inclui um exame técnico profundo e uma verificação de sanidade conduzida por um engenheiro do [!DNL Commerce], com foco na documentação, estrutura de codificação, desempenho, escalabilidade, segurança e compatibilidade com o núcleo do [!DNL Commerce].

Embora você possa comprar extensões de outras fontes, somente as extensões disponíveis no [!DNL Commerce Marketplace] serão verificadas por meio de uma ampla revisão técnica e de marketing dentro do Programa de Qualidade da Extensão.

## Recursos do aplicativo

Os desenvolvedores tradicionalmente usam o PHP para criar extensões em andamento para adicionar recursos, funcionalidades, serviços e integrações ao Adobe Commerce. Ao criar aplicativos com extensibilidade fora do processo, em vez de extensões, você pode evitar problemas de compatibilidade.

Os seguintes recursos fornecem um ponto de partida para que os novos participantes se familiarizem com os aplicativos:

### Recursos do Commerce

- [Configurando Eventos de E/S para Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Configurando Eventos para Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Configurando o SDK da Interface do Administrador](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Convertendo uma extensão em um aplicativo](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Recursos do App Builder

- [Visão geral do Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Configurando a API Mesh para o Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Implantando aplicativos App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD para aplicativos App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Introdução ao App Builder/Developer Console
   - [Introdução ao App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Noções básicas sobre projetos e espaços de trabalho](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] credenciais

Antes de instalar uma extensão adquirida do [!DNL Commerce Marketplace], entre na sua conta do [!DNL Commerce] e verifique se você tem uma chave de acesso ativa. Você pode entrar na sua conta do [!DNL Commerce] a partir do cabeçalho do [[!DNL Marketplace]][1] ou do [Magento.com][6].

Sua chave de acesso é um conjunto de chaves públicas e privadas usadas para sincronizar sua instalação do [!DNL Commerce] com sua conta do [!DNL Commerce] e verificar suas credenciais. Depois que sua conta for sincronizada, você deverá inserir sua chave privada sempre que instalar uma extensão ou um módulo do Commerce Marketplace ou atualizar sua instalação do [!DNL Commerce].

Você pode criar várias chaves de acesso para diferentes propósitos e ativá-las ou desativá-las conforme necessário. No entanto, você deve usar a mesma chave de acesso usada para instalar o software [!DNL Commerce]. Por exemplo, não é possível usar uma chave de acesso do Magento Open Source para atualizar ou atualizar o Adobe Commerce, ou vice-versa. Você também não pode usar uma chave de acesso que pertença a outro usuário ou que seja de uma [conta compartilhada](commerce-account-share.md).

### Criar uma chave de acesso

1. Entre na sua conta [!DNL Commerce].

1. Na página _[!UICONTROL My Account]_, escolha a guia **[!UICONTROL Marketplace]**.

1. No canto superior direito próximo ao seu nome, clique na seta para baixo e escolha **[!UICONTROL My Profile]**.

   ![Seu [!DNL Marketplace] perfil](./assets/marketplace-profile.png){width="600"}

1. Na guia _[!UICONTROL Marketplace]_, em&#x200B;_[!UICONTROL My Products]_, clique em **[!UICONTROL Access Keys]** e siga um destes procedimentos:

   - Verifique se você já tem um conjunto de chaves de acesso para suas compras do Marketplace. É possível criar vários conjuntos de chaves de acesso para diferentes propósitos.

   ![Chaves de Acesso](./assets/access-keys.png){width="600"}

   - Clique em **[!UICONTROL Create a New Access Key]**. Digite um nome para o novo par de chaves e clique em **[!UICONTROL OK]**. Os caracteres válidos incluem caracteres maiúsculos e minúsculos e hifens em vez de espaços.

1. Quando terminar, clique em **[!UICONTROL OK]**.

   Sua nova chave de acesso está ativada e aparece na lista.

   Observe o link _Copiar_ após cada chave pública e privada. Na próxima etapa, copie e cole esses valores para sincronizar o armazenamento com o Commerce Marketplace.

## Processo de instalação

>[!IMPORTANT]
>
>A partir do Adobe Commerce e do Magento Open Source 2.4.0, o Assistente de Instalação da Web é removido e você deve usar a linha de comando para [instalar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) ou [atualizar](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) sua instância. Este requisito também inclui [módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) e [extensões](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

O processo de instalação das compras do [!DNL Marketplace] é diferente para as instalações _locais_ do Commerce e para as instalações hospedadas na [Arquitetura da Adobe Cloud][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Suporte

Se precisar de ajuda com a instalação do ou com o uso de uma extensão, verifique primeiro na documentação que acompanha a extensão. Se não conseguir encontrar a resposta para sua pergunta, use as informações de contato na lista de extensões para entrar em contato diretamente com o desenvolvedor. Se o que você comprar no Marketplace não atender às suas necessidades, você pode [solicitar reembolso](#refund-requests) em 25 dias a partir da data de compra. A Adobe analisa todas as solicitações de reembolso e (se aprovado) emite o reembolso apropriado. Para problemas relacionados ao Commerce Marketplace:

Método 1: vá para o [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/), navegue até a parte inferior da página e clique em [!UICONTROL Contact Us], que abrirá um formulário para enviar um tíquete.

Método 2: [Suporte por email](mailto:commercemarketplacesupport@adobe.com).

### Problemas de check-out

Os campos de endereço no perfil da conta devem ser preenchidos para fins de verificação no sistema de compras do Marketplace.

1. Adicione os campos de endereço no perfil da conta do Marketplace.
1. Salve o perfil atualizado.
1. Continue com o check-out.

### Problemas de logon

Problemas de logon normalmente estão relacionados a uma incompatibilidade entre sua MAGEID e o endereço de email no banco de dados da conta. Entre em contato com o Suporte do Marketplace para obter assistência.

>[!INFO]
>
>As compras de aplicativos e extensões não podem ser [transferidas](#purchase-transfers) para uma nova conta.

### Perguntas sobre código aberto

A equipe de Suporte do Marketplace resolve problemas relacionados somente aos sites [commercemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) e [commerce.developer.adobe.com/](https://commercedeveloper.adobe.com/). Envie suas dúvidas sobre o Magento Open Source para o [Fórum da Comunidade](https://community.magento.com/) ou [contate um parceiro](https://business.adobe.com/products/magento/partners.html) que possa ajudar com o Magento Open Source.

### Solicitações de reembolso

Para solicitar um reembolso para uma compra no Marketplace, faça logon em sua conta e siga estas etapas:

1. Clique em [!UICONTROL **Meu Perfil**] > [!UICONTROL **Histórico de Compras**].
1. Localize a compra e clique em [!UICONTROL **Solicitar um Reembolso**].
1. Preencha o formulário de ordem de reembolso.

O Suporte do Marketplace solicitará informações após a solicitação de reembolso ser gerada. A opção de reembolso está disponível por 25 dias após a data de compra. Consulte o [Contrato de Cliente do Marketplace](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Faturas de ordem

Você pode baixar faturas de pedidos do [!UICONTROL **Histórico de compras**] na sua conta do Marketplace. A fatura não fornece o IVA ou o endereço do vendedor porque não é um requisito do Marketplace neste momento.

Para baixar uma fatura de pedido para uma compra do Marketplace, faça logon em sua conta do Marketplace e siga estas etapas:

1. Clique em [!UICONTROL **Meu Perfil**] > [!UICONTROL **Histórico de Compras**].
1. Localize a compra.
1. Clique no ícone da impressora no canto superior direito do pedido.

### Transferências de compra

A equipe de suporte do Marketplace não pode transferir compras para uma conta diferente. Você deve comprar todos os aplicativos e extensões na conta principal do Commerce para evitar problemas de instalação e implantação. O Adobe Commerce tem direito a um identificador exclusivo. Como o Composer é usado para instalação, somente um conjunto de [chaves de acesso](#create-an-access-key) vinculadas à conta principal pode ser usado. A única solução disponível é [solicitar um reembolso](#refund-requests) da conta de compras do Marketplace (se permitido pela política de reembolso da Adobe Commerce).

Você pode [compartilhar](commerce-account-share.md) uma instância do Commerce por meio da conta principal. O acesso compartilhado concede permissões especiais a uma conta subordinada de uma conta principal. O ponto de acesso compartilhado é gerado a partir da conta principal. A conta principal pode ser a conta qualificada da Commerce, a conta principal do comerciante ou uma conta compartilhada em uma organização.

Essas permissões especiais concedem o mesmo nível de acesso ao Adobe Commerce que o principal, no entanto, ele não é transferido para o Adobe Commerce Marketplace ou para o Portal do desenvolvedor. Isso significa que a compra de uma extensão de uma conta subordinada no Marketplace não pode ser compartilhada com a conta principal. O acesso compartilhado é uma rua unidirecional (conta principal a ser subordinada). Ele não funciona quando uma conta subordinada está tentando compartilhar de volta com a conta principal.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/products/magento/magento-commerce.html
