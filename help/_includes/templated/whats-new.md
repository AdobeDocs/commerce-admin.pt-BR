---
source-git-commit: 78d6e7fa263246e8fa52aa0386b35e4bb39553ad
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 2%

---
# Modelo de novidades

## Novidades

Esta seção contém as alterações feitas nos últimos 60 dias. Excluímos todas as atualizações secundárias, como a edição de cópia, desta lista.

### 10 de fevereiro de 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrição</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Atualizações na documentação de Administração da versão de fevereiro do Adobe Commerce as a Cloud Service:<br />- Adição de documentação para <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/order-management/invoices#custom-capture-amounts">valores de captura personalizados</a> ao criar faturas na API REST, o que permite que os comerciantes capturem valores personalizados ao criar faturas para capturas parciais e cenários de pagamento especializados.<br />- Indica quais relatórios no <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/start/reporting/reports-menu">menu Relatórios</a> agora são somente PaaS.</p>
</td>
      <td>
        Atualização importante
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/0c602db5a7291b95d725bce59df53923490d6b96">confirmar</a></td>
    </tr>
  </tbody>
</table>

### 2 de fevereiro de 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrição</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Atualização de <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law">Conformidade com a lei de cookies</a> para adicionar a chave <code class="language-plaintext highlighter-rouge">mage-cache-timeout</code> localStorage ausente e converter a lista de cookies isentos em um formato de tabela.</p>
</td>
      <td>
        Técnico, feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/ebb6348c6b5a30f5de4025f39bae0061b397a4b9">confirmar</a></td>
    </tr>
    <tr>
      <td><p>[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se a projetos do Adobe Commerce na Nuvem (infraestrutura do PaaS gerenciada pela Adobe) e somente a projetos locais."} Atualização dos pré-requisitos para configurar a integração do IMS com o Adobe Commerce para fornecer informações sobre a solicitação de acesso ao Adobe Admin Console.</p>
</td>
      <td>
        Técnico, feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/8ea546c5e1cc9296c8b056ea7e25984a66d43851">confirmar</a></td>
    </tr>
  </tbody>
</table>

### 31 de janeiro de 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrição</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Atualização dos <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-groups">Grupos de clientes</a> no Guia de gerenciamento de clientes para esclarecer que os usuários administradores não podem editar o Grupo de clientes de um cliente depois que ele é atribuído a uma empresa.</p>
</td>
      <td>
        Técnico
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/pull/81">pull request</a></td>
    </tr>
  </tbody>
</table>

### 20 de janeiro de 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrição</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>As referências de produto foram alteradas de "Adobe Sensei" para "Adobe AI" para refletir as atualizações de marca da Adobe.</p>
</td>
      <td>
        Feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/4077b922dae0ed9a9050a5f6160143a636646daa">confirmar</a></td>
    </tr>
  </tbody>
</table>

### 16 de janeiro de 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrição</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Foi adicionado um esclarecimento quando os emails <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/config/sales/sales-emails#order-ready-for-pickup-in-store">Pedido pronto para retirada na loja</a> estão disponíveis.</p>
</td>
      <td>
        Feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/65fd67dcd3c14daddfc0f36493dc6da3630898a1">confirmar</a></td>
    </tr>
  </tbody>
</table>

### 15 de janeiro de 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrição</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Adição dos seguintes recursos ao Adobe Commerce as a Cloud Service:<br />- Adição de suporte ao <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/captcha/security-google-recaptcha-enterprise">Google reCAPTCHA Enterprise</a>, que fornece proteção de bot avançada com análise de risco adaptável e recursos de aprendizado de máquina.<br />- Transforme os números de rastreamento de remessa incluídos nos emails do comprador de texto sem formatação em links clicáveis ao <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-settings#shipment-tracking-urls">habilitar as URLs de Rastreamento Personalizado</a>. Esse recurso é compatível com USPS, UPS, FedEx e DHL.<br />- Agora você pode combinar descontos de preços em camadas com descontos de regras de catálogo usando <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/pricing/product-price-tier#enable-tier-pricing-for-catalog-price-rules">regras de preços de catálogo</a>. Esse aprimoramento permite criar estratégias de preços mais dinâmicas e competitivas.</p>
</td>
      <td>
        Atualização importante, novo tópico
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/70e73b47c4b0342ade3deab64dbe39f29b82191f">confirmar</a></td>
    </tr>
  </tbody>
</table>

### 17 de dezembro de 2025

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrição</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Atualização do <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty">tópico de recompensas e fidelidade</a> para esclarecer como o imposto é calculado quando os clientes usam pontos de premiação ou armazenam crédito durante o check-out.</p>
</td>
      <td>
        Feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/1154cd5ced746ac6dfd609946528f281774bbaaa">confirmar</a></td>
    </tr>
  </tbody>
</table>
