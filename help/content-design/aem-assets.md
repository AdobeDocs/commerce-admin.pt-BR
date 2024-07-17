---
title: Integração do Experience Manager Assets para o Commerce
description: Saiba como integrar o Experience Manager Assets à sua instância  [!DNL Commerce]  para acessar inúmeros ativos de mídia para usar em sua loja.
feature: CMS, Media, Configuration, Integration
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Integração do Experience Manager Assets para o Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

A integração entre o Commerce e o Adobe Experience Manager (AEM) Assets AEM combina os recursos robustos do como um sistema de Gerenciamento de ativos digitais (DAM) com o Adobe Commerce para melhorar as experiências de comércio eletrônico. Essa integração aproveita os poderosos recursos de gerenciamento de ativos do AEM para fornecer uma maneira contínua, escalável e eficiente de gerenciar e fornecer ativos em vitrines de comércio.

**Principais recursos**

- **Gerenciamento centralizado de ativos**

   - **AEM Assets como o Source Único da Verdade**-O AEM Assets serve como repositório central para todos os ativos digitais, garantindo que todas as plataformas de comércio eletrônico tenham acesso aos ativos aprovados na marca.

   - **Gerenciamento de ativos em massa** - As organizações podem gerenciar grandes volumes de ativos com eficiência, graças aos recursos robustos de gerenciamento de ativos do AEM. Isso permite que profissionais de marketing e comerciantes mapeiem grandes conjuntos de imagens para novas linhas de produtos com eficiência.

- **Experiências personalizadas do Commerce** - Usando os serviços GenAI no AEM, as organizações podem gerar milhões de variações de produtos para experiências personalizadas de comércio eletrônico. Profissionais de marketing e merchandisers podem usar essas imagens para criar lojas dinâmicas para lançamentos de produtos e campanhas sazonais, aprimorando o engajamento e aumentando as taxas de conversão.

- **Correspondência automatizada de ativos** - A integração inclui um Serviço de Mecanismo de Regras que corresponde automaticamente ativos no AEM a produtos no Adobe Commerce com base na SKU ou em outros atributos principais. O serviço garante que os ativos e as variações de produtos mais recentes estejam sempre disponíveis em lojas de comércio eletrônico. Também reduz o esforço manual necessário para gerenciar ativos, liberando tempo para atividades mais estratégicas.

- **Processos simplificados**
   - **Habilite e configure a integração do Administrador do Commerce**. Os administradores e desenvolvedores podem instalar e configurar a integração do Adobe Commerce usando ferramentas e processos familiares.
   - **Atualizações Dinâmicas** - Mantenha as imagens do produto atualizadas com as últimas alterações no sistema de gerenciamento de ativos. Essas atualizações automatizadas garantem que as vitrines de comércio sempre tenham as informações mais atualizadas do produto.
   - **Gerenciamento eficiente de catálogo**-Simplifica a manutenção do catálogo de produtos automatizando a limpeza e a atualização de ativos.

## Integrar o Commerce e o Experience Manager Assets

>[!BEGINSHADEBOX]

**Pré-requisitos**

- O Adobe Commerce deve ser configurado com a [integração do Commerce Admin com o Adobe ID](/help/getting-started/adobe-ims-config.md) com uma ID de organização atribuída.
- O Experience Manager Assets deve ser atribuído como um produto à mesma ID da organização.
- O usuário que configura a integração deve ter uma conta na mesma organização com direitos administrativos para acessar o Adobe Commerce e o Experience Manager Assets.

>[!ENDSHADEBOX]

Habilitar a integração do Commerce com o Experience Manager Assets ao concluir as seguintes tarefas:

1. [Configurar o projeto do Experience Manager Assets para gerenciar ativos do Commerce](aem-assets-configure-aem.md)

1. [Instale a extensão Integração do Experience Manager Assets e configure o Adobe Commerce](aem-assets-configure-commerce.md)

1. [Habilitar sincronização de ativos](aem-assets-setup-synchronization.md)
