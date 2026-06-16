---
title: Ferramentas do site do Google
description: Saiba mais sobre as integrações das ferramentas do Google que você pode usar para otimizar seu conteúdo, analisar seu tráfego e conectar seu catálogo a agregadores de compras e marketplaces.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
TQID: https://experienceleague.adobe.com/P-IniOyLDfDk8oe1v9ysmRV6yC7IWpxUBaFF--2YMCg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 662
ht-degree: 0%

---

# Ferramentas do site do Google

A configuração da sua loja está integrada às seguintes ferramentas do Google para ajudar a otimizar o seu conteúdo, analisar o seu tráfego e conectar o seu catálogo a agregadores de compras e marketplaces.

- [Google Analytics](google-analytics.md) - Use o _Google Universal Analytics_ para definir dimensões e métricas personalizadas adicionais para rastreamento, com suporte para interações offline e de aplicativos móveis e acesso a atualizações contínuas.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Use o Google Tag Manager para gerenciar as várias tags relacionadas aos eventos de campanha de marketing.

- [Google AdWords](google-adwords.md) - Crie uma campanha do Google AdWords e rastreie as conversões da sua loja.

{{gtag-api-note}}

## Configurações de privacidade do Google

Se a sua empresa precisa cumprir com as regras de privacidade, como o [GDPR](../getting-started/compliance-gdpr.md) ou a [CCPA](../getting-started/compliance-ccpa.md), altere as configurações padrão das ferramentas do Google para atender aos requisitos de privacidade. Siga estas etapas para garantir que o uso dos dados do cliente permaneça em conformidade.

### Etapa 1: atualizar configurações do Google

1. [Entre](https://www.google.com/analytics/){: target="_blank"} na conta da Google Analytics da sua empresa.

1. Na parte inferior da barra lateral esquerda, escolha **[!UICONTROL Admin]** e navegue até a conta que deseja editar (se aplicável).

1. Na coluna **[!UICONTROL Account]**, clique em **[!UICONTROL Account Settings]**.

1. Desative o compartilhamento de dados para atender aos requisitos de regulamento de privacidade.

   As configurações padrão do Google Analytics compartilham os dados da empresa com a Google e outras partes. Para desativar o compartilhamento de dados, desmarque a caixa de seleção das seguintes configurações:

   - Produtos e serviços da Google
   - Benchmarking
   - Suporte técnico
   - Especialistas de conta

1. Aceite o _Aditamento de Processamento de Dados_.

   Os Termos de processamento de dados do Google Ads descrevem como a Google processa dados e as medidas que ela toma para garantir a segurança dos dados para empresas que estão sujeitas ao GDPR. Um registro de suas entidades legais e informações de contato também é mantido com o aditamento. Para [saber mais](https://support.google.com/analytics/answer/3379636){: target="_blank"}, clique no link da mensagem na parte superior da página.

   - Role a página para baixo até **[!UICONTROL Data Processing Amendment]**.
   - Clique em **[!UICONTROL Review Amendment]** para ler os _Termos de processamento de dados do Google Ads_.
   - Clique em **[!UICONTROL Accept]**.
   - Clique em **[!UICONTROL Save]**.

1. Conclua os detalhes da _Administração do DPA_.

   - Clique em **[!UICONTROL Manage DPA Details]** para abrir a página de administração do DPA, onde é possível editar os contatos e as entidades legais de sua organização.

   - Na seção **[!UICONTROL Legal Entities]**, clique no ícone _Editar_ ( ![ícone de edição do Google](./assets/google-icon-edit.png) ) e adicione um ou mais nomes registrados para sua organização. Quando terminar, clique em **[!UICONTROL Save]**.

   - Na seção **Contatos**, clique no ícone _Adicionar_ ( ![ícone de adição do Google](./assets/google-icon-add.png) ) e insira as informações do primeiro contato. Em seguida, marque a caixa de seleção de cada função aplicável e clique em **[!UICONTROL Add]**.

      - Contato Principal - (Endereço de Email de Notificação) O contato para o qual os avisos são enviados.
      - Responsável pela proteção de dados - (se aplicável) A pessoa designada para facilitar a conformidade com o regulamento de privacidade.
      - Representante do Espaço Econômico Europeu (EEA) - (se aplicável) A pessoa que representa clientes fora da EU em relação às obrigações do GDPR.

     Repita para adicionar outro contato, se aplicável.

### Etapa 2: Modificar as bibliotecas JS do Google

A Google oferece suporte a três bibliotecas JavaScript para medir o uso do site, dependendo do produto Google: `gtag.js`, `analytics.js` e `ga.js`. Para atender aos requisitos de privacidade, o código padrão pode ser modificado da seguinte maneira:

#### Tornar endereços IP anônimos

Para tornar os endereços IP anônimos usados pelo **_Google Universal Analytics_**, adicione o seguinte trecho à biblioteca do `analytics.js` no seu servidor Web:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Para saber mais, consulte a [Referência de campo do Analytics.js](https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference){: target="_blank"} na Ajuda do Google.

Se você usar a biblioteca herdada `ga.js`, adicione o seguinte trecho:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Para tornar os endereços IP anônimos usados pelo **_Google Tag Manager_**, defina o parâmetro `anonymize_ip` como `true` na biblioteca `gtag.js` no seu servidor Web.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Para saber mais, consulte [Anonimização de IP no Analytics](https://support.google.com/analytics/answer/2763052) na Ajuda do Google.

#### Forçar SSL

Para forçar todos os dados do Google a serem transmitidos por uma SSL (camada de soquete seguro), adicione o seguinte trecho à biblioteca do `analytics.js` no seu servidor Web.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Etapa 3: atualizar sua política de privacidade

Atualize sua [política de privacidade](../getting-started/privacy-policy.md) para informar que sua empresa:

- Usa o Google Analytics
- Mascara endereços IP para ocultar informações pessoais
- Desativou o Compartilhamento de dados da Google
- Não usa outros serviços da Google com cookies da Google Analytics
