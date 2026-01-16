---
title: Google reCAPTCHA Enterprise
description: Saiba como configurar o Google reCAPTCHA Enterprise para proteger sua loja do Adobe Commerce as a Cloud Service contra bots e atividades fraudulentas.
role: Admin
feature: Configuration, Security
badgeSaas: label="Somente SaaS" type="Positive" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplicável somente a projetos do Adobe Commerce as a Cloud Service (infraestrutura SaaS gerenciada pela Adobe)."
source-git-commit: dde1d634a1c6c7435668a8ad6084b926cc0d6193
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[!BADGE Sandbox]{type=Caution tooltip="Os itens listados estão disponíveis atualmente apenas em ambientes de sandbox. O Adobe lança atualizações para a sandbox primeiro, para que você possa testar as alterações futuras antes de elas serem implantadas na produção."}

A [Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) oferece proteção avançada de bot para sua loja Adobe Commerce as a Cloud Service usando análise de risco adaptável e aprendizado de máquina para diferenciar usuários humanos e bots. Isso ajuda a evitar atividades fraudulentas, spam e abuso em seu site.

>[!NOTE]
>
>Esse recurso NÃO fornece suporte ao reCAPTCHA para o administrador.

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

1. No painel esquerdo, em _[!UICONTROL Security]_, escolha **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Conclua a seção **[!UICONTROL reCAPTCHA Enterprise]** da seguinte maneira.

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
