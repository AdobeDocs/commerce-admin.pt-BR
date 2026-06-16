---
title: Google reCAPTCHA Enterprise
description: Saiba como configurar o Google reCAPTCHA Enterprise para proteger sua loja do Adobe Commerce as a Cloud Service contra bots e atividades fraudulentas.
role: Admin
feature: Configuration, Security
badgeSaas: label="Somente SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplicável somente a projetos do Adobe Commerce as a Cloud Service (infraestrutura SaaS gerenciada pela Adobe)."
exl-id: 2c88488c-8ff1-41db-b81b-89ad164e134d
TQID: https://experienceleague.adobe.com/oMZleuJsp2QiDD7IsMDV647LWKm938lNvY4--o6G3c8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

A [Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) oferece proteção avançada de bot para sua loja Adobe Commerce as a Cloud Service usando análise de risco adaptável e aprendizado de máquina para diferenciar usuários humanos e bots. Isso ajuda a evitar atividades fraudulentas, spam e abuso em seu site.

>[!NOTE]
>
>Esse recurso NÃO fornece suporte ao reCAPTCHA para o administrador.

A [integração do reCAPTCHA](https://experienceleague.adobe.com/developer/commerce/storefront/dropins/user-auth/recaptcha/) descreve como adicionar suporte ao reCAPTCHA Enterprise em sua loja.

Consulte [Google reCAPTCHA V3 e V2](security-google-recaptcha.md) para obter informações sobre como configurar outras versões do Google reCAPTCHA.

## Recursos

O Google reCAPTCHA Enterprise inclui os seguintes recursos:

- **Detecção avançada de bot**: usa os modelos de aprendizado de máquina da Google Cloud para detecção superior de bot
- **Análise de pontuação de risco**: fornece pontuações de risco detalhadas (0,0-1,0) para cada interação
- **Limites configuráveis**: definir pontuações de risco mínimas aceitáveis por locatário
- **Suporte a vários locatários**: configuração por locatário com projetos isolados da Google Cloud
- **Credenciais criptografadas**: credenciais de conta de serviço armazenadas e criptografadas em um banco de dados
- **Proteção de formulário**: protege todos os formulários padrão do Commerce, incluindo logon, check-out, revisões de produtos e muito mais.

## Pré-requisitos

Você precisa dos seguintes recursos antes de configurar o Google reCAPTCHA Enterprise para sua loja Adobe Commerce as a Cloud Service:

- Uma conta ativa da Google Cloud com o reCAPTCHA Enterprise ativado.
- Acesso ao Google Cloud Console para criar e gerenciar chaves reCAPTCHA Enterprise.

Em instalações de vários locatários do Adobe Commerce as a Cloud Service, cada locatário deve ter seu próprio projeto da Google Cloud e chaves reCAPTCHA Enterprise.

## Etapa 1: configurar o Google reCAPTCHA Enterprise

Siga estas etapas gerais para configurar o Google reCAPTCHA Enterprise para sua loja. Para obter instruções detalhadas, consulte a [documentação do Google reCAPTCHA Enterprise](https://docs.cloud.google.com/recaptcha/docs/overview).

1. [Crie um projeto da Google Cloud](https://developers.google.com/workspace/guides/create-project) para sua implementação do reCAPTCHA Enterprise.

1. Habilite a [API corporativa do reCAPTCHA](https://docs.cloud.google.com/recaptcha/docs/prepare-environment).

1. Crie uma chave do site [reCAPTCHA Enterprise](https://docs.cloud.google.com/recaptcha/docs/choose-key-type) baseada em pontuação.

1. Crie uma Conta de Serviço com a função IAM `roles/recaptchaenterprise.admin`.

1. Baixe o arquivo de chave JSON da conta de serviço, que contém as credenciais necessárias para autenticar sua loja do Adobe Commerce as a Cloud Service com o Google reCAPTCHA Enterprise.

## Etapa 2: configurar o Google reCAPTCHA para a loja

1. Na barra lateral do Adobe Commerce _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expanda _[!UICONTROL Security]_&#x200B;e escolha **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Role para baixo até a seção **[!UICONTROL reCAPTCHA Enterprise]** e conclua a configuração da seguinte maneira.

   - Para **[!UICONTROL Site Key]**, copie e cole sua chave do site reCAPTCHA Enterprise do seu Google Cloud Console.

   - Para **[!UICONTROL Google Cloud Project ID]**, copie e cole a ID do projeto do seu projeto do Google Cloud.

   - Para **[!UICONTROL Service Account JSON]**, copie o conteúdo do arquivo de chave JSON da Conta de Serviço que você baixou em [Etapa 1: Configurar o Google reCAPTCHA Enterprise](#step-1-set-up-google-recaptcha-enterprise).

   - Para **[!UICONTROL Minimum Score Threshold]**, insira a pontuação mínima (0.0-1.0) para identificar quando uma interação do usuário é sinalizada como um risco potencial. Uma pontuação de 1,0 é uma interação típica do usuário, e 0,0 provavelmente é um bot.

   - Para **[!UICONTROL Badge Position]**, escolha a posição do selo reCAPTCHA invisível em cada página. Opções: `Inline` / `Bottom Right` / `Bottom Left`.

   - Para **[!UICONTROL Theme]**, escolha `Light Theme` (padrão) ou `Dark Theme` para determinar o estilo da caixa do reCAPTCHA do Google.

   - Para **[!UICONTROL Language Code]**, insira um [código de dois caracteres](https://developers.google.com/recaptcha/docs/language) que especifique o idioma usado para texto e mensagens do Google reCAPTCHA.

   - Para **[!UICONTROL Validation Failure Message]**, opcionalmente, altere a mensagem exibida na loja quando a validação não for bem-sucedida.


1. Expanda a seção **[!UICONTROL Storefront]** e defina cada formulário de vitrine eletrônica que você deseja proteger para **[!UICONTROL reCAPTCHA Enterprise]**.

   {{recaptcha-forms-list}}

   ![Configuração de opções de vitrine eletrônica](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Etapa 3: salvar a configuração

1. Quando as configurações estiverem concluídas, clique em **[!UICONTROL Save Config]**.

1. Na mensagem na parte superior do espaço de trabalho, clique em **[!UICONTROL Cache Management]** e atualize cada cache inválido.
