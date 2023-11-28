---
title: '[!DNL Adobe Commerce Marketplace]'
description: Saiba mais sobre o [!DNL Commerce Marketplace], que oferece aos comerciantes uma seleção de soluções com curadoria e fornece aos desenvolvedores qualificados as ferramentas, a plataforma e o local ideal para criar um negócio próspero.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 1a5a00493e9994343c7decc763f2decdd11192c7
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] O é a loja de aplicativos que oferece aos comerciantes uma seleção de soluções com curadoria e fornece aos desenvolvedores qualificados as ferramentas, a plataforma e o local ideal para criar um negócio próspero. [!DNL Commerce Marketplace] O oferece uma seleção de extensões disponíveis gratuitamente e outras que estão à venda. As compras podem ser pagas com cartão de crédito ou [PayPal][2].

Todas as extensões disponíveis em [!DNL Commerce Marketplace] foram aprovados numa análise aprofundada. A variável [Programa de qualidade de extensão][3] (EQP) combina [!DNL Commerce] experiência, diretrizes de desenvolvimento e ferramentas de verificação para garantir que todas as extensões no Commerce Marketplace atendam aos padrões de codificação e às práticas recomendadas. O processo de revisão inclui uma verificação automatizada e uma revisão manual de controle de qualidade. Durante o processo, a estrutura e o código de cada extensão são examinados e testados em busca de evidências de infecção por vírus/malware e qualquer indicação de plágio. A revisão inclui um exame técnico aprofundado e uma verificação de sanidade realizada por um [!DNL Commerce] com foco na documentação, estrutura de codificação, desempenho, escalabilidade, segurança e compatibilidade com o [!DNL Commerce] principal.

Embora seja possível comprar extensões de outras fontes, somente as extensões que estão disponíveis em [!DNL Commerce Marketplace] são verificados por meio de ampla revisão técnica e de marketing dentro do Programa de qualidade de extensão.

## Recursos do aplicativo

Os desenvolvedores tradicionalmente usam o PHP para criar extensões em andamento para adicionar recursos, funcionalidades, serviços e integrações ao Adobe Commerce. Ao criar aplicativos com extensibilidade fora do processo, em vez de extensões, você pode evitar problemas de compatibilidade.

Os seguintes recursos fornecem um ponto de partida para que os novos participantes se familiarizem com os aplicativos:

### Recursos de comércio:

- [Configuração de eventos de E/S para o Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Configuração de eventos para o Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Configuração do SDK da interface do administrador](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Conversão de uma extensão em um aplicativo](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Recursos do Construtor de aplicativos:

- [Visão geral do Construtor de aplicativos do Commerce](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Configuração da malha de API para o Construtor de aplicativos do Adobe Developer](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Implantar aplicativos do App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD para aplicativos do App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Introdução ao App Builder/Developer Console
   - [Introdução ao App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Noções básicas sobre projetos e espaços de trabalho](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] credenciais

Antes de instalar uma extensão adquirida do [!DNL Commerce Marketplace], faça logon no [!DNL Commerce] e verifique se você tem uma chave de acesso ativa. Você pode entrar no seu [!DNL Commerce] conta no cabeçalho de [[!DNL Marketplace]][1] ou [Magento.com][6].

Sua chave de acesso é um conjunto de chaves públicas e privadas usadas para sincronizar sua [!DNL Commerce] instalação com o seu [!DNL Commerce] e verifique suas credenciais. Depois que sua conta for sincronizada, você deverá inserir sua chave privada sempre que instalar uma extensão ou um módulo do Commerce Marketplace ou atualizar sua [!DNL Commerce] instalação.

Você pode criar várias chaves de acesso para diferentes propósitos e ativá-las ou desativá-las conforme necessário. No entanto, você deve usar a mesma chave de acesso usada para instalar o [!DNL Commerce] software. Por exemplo, você não pode usar uma chave de acesso Magento Open Source para atualizar ou atualizar o Adobe Commerce, ou vice-versa. Você também não pode usar uma chave de acesso que pertença a outro usuário ou que seja de um [conta compartilhada](commerce-account-share.md).

### Criar uma chave de acesso

1. Faça logon no [!DNL Commerce] conta.

1. No _[!UICONTROL My Account]_escolha a **[!UICONTROL Marketplace]**guia.

1. No canto superior direito próximo ao seu nome, clique na seta para baixo e escolha **[!UICONTROL My Profile]**.

   ![Seu [!DNL Marketplace] perfil](./assets/marketplace-profile.png){width="600"}

1. No _[!UICONTROL Marketplace]_em_[!UICONTROL My Products]_, clique em **[!UICONTROL Access Keys]**, e siga um destes procedimentos:

   - Verifique se você já tem um conjunto de chaves de acesso para suas compras do Marketplace. É possível criar vários conjuntos de chaves de acesso para diferentes propósitos.

   ![Teclas de acesso](./assets/access-keys.png){width="600"}

   - Clique em **[!UICONTROL Create a New Access Key]**. Insira um nome para o novo par de chaves e clique em **[!UICONTROL OK]**. Os caracteres válidos incluem caracteres maiúsculos e minúsculos e hifens em vez de espaços.

1. Quando terminar, clique em **[!UICONTROL OK]**.

   Sua nova chave de acesso está ativada e aparece na lista.

   Observe a _Copiar_ após cada chave pública e privada. Na próxima etapa, você copiará e colará esses valores para sincronizar o armazenamento com o Commerce Marketplace.

## Processo de instalação

>[!IMPORTANT]
>
>A partir do Adobe Commerce e do Magento Open Source 2.4.0, o Assistente de configuração da Web será removido e você deverá usar a linha de comando para [instalar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) ou [atualização](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) sua instância. Este requisito também inclui [módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) e [extensões](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

O processo de instalação do [!DNL Marketplace] compras é diferente para _no local_ instalações do Commerce do que as instalações hospedadas em [a arquitetura de nuvem do Adobe][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Suporte

Se precisar de ajuda com a instalação do ou com o uso de uma extensão, verifique primeiro na documentação que acompanha a extensão. Se não conseguir encontrar a resposta para sua pergunta, use as informações de contato na lista de extensões para entrar em contato diretamente com o desenvolvedor.

Se o que você comprar no Commerce Marketplace não atender às suas necessidades, você pode solicitar um reembolso dentro de 25 dias a partir da data de compra. A Adobe revisa todas as solicitações de reembolso e, se aprovada, emite o reembolso apropriado.

Para questões de suporte relacionadas ao Commerce Marketplace, consulte [[!DNL Marketplace] Centro de ajuda][5].

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
