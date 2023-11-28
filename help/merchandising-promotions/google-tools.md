---
title: Ferramentas do site do Google
description: Saiba mais sobre as integrações das ferramentas do Google que você pode usar para otimizar seu conteúdo, analisar seu tráfego e conectar seu catálogo a agregadores de compras e marketplaces.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Ferramentas do site do Google

A configuração da sua loja está integrada às seguintes ferramentas do Google para ajudar a otimizar o seu conteúdo, analisar o seu tráfego e conectar o seu catálogo a agregadores de compras e marketplaces.

- [Google Analytics](google-analytics.md) - Utilização _Google Universal Analytics_ para definir dimensões e métricas personalizadas adicionais para rastreamento, com suporte para interações offline e em aplicativos móveis e acesso a atualizações contínuas.

- [Experimentos de conteúdo do Google](google-content-experiments.md) - Configurar um teste A/B para produtos, categorias ou páginas de conteúdo usando experimentos de conteúdo do Google Analytics.

- [Gerenciador de tags da Google](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Somente no Adobe Commerce) Use o Google Tag Manager para gerenciar as várias tags relacionadas a eventos de campanha de marketing.

- [Google AdWords](google-adwords.md) : crie uma campanha do Google AdWords e rastreie as conversões da sua loja.

{{gtag-api-note}}

## Configurações de privacidade do Google

Se sua empresa for obrigada a cumprir as regras de privacidade, como a [GDPR](../getting-started/compliance-gdpr.md) ou [CCPA](../getting-started/compliance-ccpa.md), altere as configurações padrão das ferramentas do Google para atender aos requisitos de privacidade. Siga estas etapas para garantir que o uso dos dados do cliente permaneça em conformidade.

### Etapa 1: atualizar configurações do Google

1. [Fazer logon][1]{: target=&quot;_blank&quot;} para a conta Google Analytics da sua empresa.

1. Na parte inferior da barra lateral esquerda, escolha **[!UICONTROL Admin]** e navegue até a conta que deseja editar (se aplicável).

1. No **[!UICONTROL Account]** clique em **[!UICONTROL Account Settings]**.

1. Desative o compartilhamento de dados para atender aos requisitos de regulamento de privacidade.

   As configurações padrão do Google Analytics compartilham os dados da empresa com a Google e outras partes. Para desativar o compartilhamento de dados, desmarque a caixa de seleção das seguintes configurações:

   - Produtos e serviços da Google
   - Benchmarking
   - Suporte técnico
   - Especialistas de conta

1. Aceite o _Aditamento de processamento de dados_.

   Os Termos de processamento de dados do Google Ads descrevem como a Google processa dados e as medidas que ela toma para garantir a segurança dos dados para empresas que estão sujeitas ao GDPR. Um registro de suas entidades legais e informações de contato também é mantido com o aditamento. Para [saiba mais][2]{: target=&quot;_blank&quot;}, clique no link na mensagem na parte superior da página.

   - Role para baixo na página até **[!UICONTROL Data Processing Amendment]**.
   - Clique em **[!UICONTROL Review Amendment]** para ler o _Termos de processamento de dados do Google Ads_.
   - Clique em **[!UICONTROL Accept]**.
   - Clique em **[!UICONTROL Save]**.

1. Conclua o _Administração do DPA_ detalhes.

   - Clique em **[!UICONTROL Manage DPA Details]** para abrir uma página de administração do DPA, onde você pode editar contatos e entidades legais de sua organização.

   - No **[!UICONTROL Legal Entities]** clique na guia _Editar_ ( ![Ícone de edição do Google](./assets/google-icon-edit.png) ) e adicione um ou mais nomes registrados para sua organização. Quando terminar, clique em **[!UICONTROL Save]**.

   - No **Contatos** clique na guia _Adicionar_ ( ![Ícone de adição do Google](./assets/google-icon-add.png) ) e insira as informações do primeiro contato. Em seguida, marque a caixa de seleção de cada função aplicável e clique em **[!UICONTROL Add]**.

      - Contato Principal - (Endereço de Email de Notificação) O contato para o qual os avisos são enviados.
      - Responsável pela proteção de dados - (se aplicável) A pessoa designada para facilitar a conformidade com o regulamento de privacidade.
      - Representante do Espaço Econômico Europeu (EEA) - (se aplicável) A pessoa que representa clientes fora da EU em relação às obrigações do GDPR.

     Repita para adicionar outro contato, se aplicável.

### Etapa 2: Modificar as bibliotecas JS do Google

O Google oferece suporte a três bibliotecas JavaScript para medir o uso do site, dependendo do produto Google: `gtag.js`, `analytics.js`, e `ga.js`. Para atender aos requisitos de privacidade, o código padrão pode ser modificado da seguinte maneira:

#### Tornar endereços IP anônimos

Para tornar os endereços IP usados pelo anônimo **_Google Universal Analytics_**, adicione o seguinte trecho à `analytics.js` no servidor Web:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Para saber mais, consulte a [Referência de campo do Analytics.js][3]{: target=&quot;_blank&quot;} na Ajuda do Google.

Se você usar o antigo `ga.js` adicione o seguinte fragmento:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Para tornar os endereços IP usados pelo anônimo **_Gerenciador de tags da Google_**, defina o `anonymize_ip` parâmetro para `true` no `gtag.js` no servidor Web.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Para saber mais, consulte [Anonimização de IP no Analytics][4] na Ajuda do Google.

#### Forçar SSL

Para forçar todos os dados do Google a serem transmitidos por uma SSL (Secure Socket Layer), adicione o seguinte trecho à `analytics.js` no servidor Web.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Etapa 3: atualizar sua política de privacidade

Atualize seu [política de privacidade](../getting-started/privacy-policy.md) para informar que sua empresa:

- Usa Google Analytics
- Mascara endereços IP para ocultar informações pessoais
- Desativou o Compartilhamento de dados da Google
- Não usa outros serviços da Google com cookies Google Analytics

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
