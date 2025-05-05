---
title: Disponibilidade para HIPAA no Adobe Commerce
description: Saiba como adicionar a extensão do Adobe Commerce pronta para HIPAA e obtenha recursos e funcionalidades adicionais que permitem cumprir com as suas obrigações com a HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 2807c36fdb4ca169c31a5e92b4dab278a45c474c
workflow-type: tm+mt
source-wordcount: '2375'
ht-degree: 1%

---

# Disponibilidade para HIPAA no Adobe Commerce

>[!IMPORTANT]
>
>**Aviso de isenção legal**<br/>
>Estas informações são destinadas a ajudar os clientes da Adobe a responder às suas perguntas sobre os serviços prontos para a HIPAA da Adobe. Não constitui um aconselhamento jurídico. Os comerciantes devem consultar seu próprio departamento jurídico para entender suas obrigações conforme a HIPAA e o uso e a configuração apropriados dos produtos da Adobe.

>[!BEGINSHADEBOX]

**HIPAA (Health Insurance Portability and Accountability Act, Lei de Portabilidade e Responsabilidade do Seguro de Saúde)**

A HIPAA (Health Insurance Portability and Accountability Act, Lei de Portabilidade e Responsabilidade do Seguro de Saúde) é a principal lei federal de privacidade da área de saúde nos Estados Unidos e é aplicada pelo Departamento de Saúde e Serviços Humanos (HHS) dos EUA. A HIPAA se aplica a _Entidades Cobertas_ (como provedores de assistência médica, seguradoras e centros de compensação) e _Associados Comerciais_ (como as entidades que fornecem serviços a entidades cobertas). Os requisitos da HIPAA são definidos em três regras separadas: Regra de privacidade, Regra de segurança e Regra de notificação de violação. A Adobe atua como um Business Associate para determinados produtos, que a Adobe classifica como &quot;Serviços prontos para a HIPAA&quot;. Os dados regulamentados pela HIPAA são chamados de _Informações de Integridade Protegidas_ ou PHI. PHI é um subconjunto de informações de saúde que (1) é criado ou recebido por um prestador de cuidados de saúde, plano de saúde ou câmara de compensação de cuidados de saúde, (2) se relaciona com a saúde ou condição física ou mental passada, presente ou futura de um indivíduo, com a prestação de cuidados de saúde a um indivíduo, ou com o pagamento passado, presente ou futuro pela prestação de cuidados de saúde a um indivíduo, e (3) identifica o indivíduo ou a respeito do qual há uma base razoável para acreditar que a informação pode ser usada para identificar o indivíduo. As Regras de Privacidade e Segurança da HIPAA exigem que uma Entidade Coberta obtenha garantias por escrito de um Associado Comercial na forma de um Contrato de Associado Comercial, ou BAA, exigindo que o Associado Comercial proteja a privacidade e a segurança da PHI ʼ Entidade Coberta. Para obter mais informações, consulte [Produtos e serviços da HIPAA e da Adobe](https://www.adobe.com/trust/compliance/hipaa-ready.html) na Central de Confiabilidade da Adobe.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA-Ready

A extensão Adobe Commerce HIPAA-Ready adiciona recursos e funcionalidades adicionais às instalações do Adobe Commerce, permitindo que os comerciantes cumpram com suas respectivas obrigações com a HIPAA.

A extensão HIPAA-Ready da Adobe Commerce, `magento/hipaa-ee` está disponível para projetos Adobe Commerce na infraestrutura em nuvem ou Adobe Managed Services. O processo de instalação Adobe Commerce HIPAA-Ready desativa alguns serviços e recursos nativos para atender aos requisitos da HIPAA. Consulte [Serviços e recursos desabilitados](#disabled-services-and-features).

>[!NOTE]
>
>O acesso aos recursos e funcionalidades prontos para a HIPAA está disponível somente para comerciantes que compraram o complemento de assistência médica da Adobe Commerce.

*Estes materiais são apenas para fins informativos. O fornecimento dessas informações não confere ao destinatário nenhum direito contratual ou de outro tipo. Embora tenham sido envidados esforços para garantir a exatidão das informações à data em que foram fornecidas, não é feita qualquer declaração de que tais informações sejam exatas e completas. A Adobe não assume nenhuma obrigação de atualizar essas informações à medida que a lei ou os produtos da Adobe mudarem. Além disso, este documento não deve ser distribuído a terceiros que não sejam o destinatário pretendido sem o consentimento por escrito da Adobe.*

## Requisitos do sistema

A tabela a seguir mostra a compatibilidade entre as versões do Adobe Commerce e a extensão pronta para HIPAA:

| Adobe Commerce | Compatível | Notas |
|----------------|-----------|-------|
| 2.4.7-p4 - 2.4.7-p5 | 1.2.0 | O suporte para 2.4.7-p4 requer um [hotfix](https://experienceleague.adobe.com/pt-br/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/hotfix-for-hipaa-package-1-2-0-compatibility-with-adobe-commerce-2-4-7-p4) |
| 2.4.6-p9 - 2.4.6-p10 | 1.2.0 | |
| 2.4.6-p8 | 1.1.0 | O suporte para [serviços de dados](#adobe-commerce-services) foi introduzido na versão 1.1.0 |
| 2.4.6-p3 - 2.4.6-p7 | 1.0.0 | |

>[!IMPORTANT]
>
>- A extensão pronta para HIPAA está disponível apenas para Adobe Systems Comércio na Cloud ou na Adobe Systems Comércio projetos Managed Services.
>- A extensão está disponível como um metapackage do Composer em `repo.magento.com`.
>- O acesso aos recursos prontos para HIPAA e funcionalidade requer o complemento de cuidados de saúde para Adobe Systems Comércio.
>- Adobe Systems não há suporte Comércio versões beta.

## Instalação

**Pré-requisito**

>[!BEGINSHADEBOX]

- A Adobe provisionou sua conta do Adobe Commerce para acessar a extensão HIPAA Ready.
- Acesso ao [repo.magento.com](https://repo.magento.com) para instalar a extensão. Para geração de chaves e obtenção dos direitos necessários, consulte [Obter suas chaves de autenticação](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=pt-BR).

>[!ENDSHADEBOX]

Instale a versão mais recente da extensão HIPAA-Ready Services da Adobe (`magento/hipaa-ee`) em uma instância que esteja executando o Adobe Commerce versão 2.4.7-p5 ou 2.4.6-p3 a 2.4.6-p8. A extensão é entregue como um metapackage de compositor do [repositório.magento.com](https://repo.magento.com). O metapackage inclui a coleção de módulos que habilitam os recursos HIPAA para uma instância do Adobe Commerce.

>[!NOTE]
>
>Para garantir que os dados do evento de back office enviados para o Experience Platform estejam prontos para HIPAA, consulte o [guia de extensão de Conexão de Dados](https://experienceleague.adobe.com/pt-br/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension).

1. Na estação de trabalho local, altere para o diretório do projeto do Adobe Commerce na infraestrutura em nuvem.

   >[!NOTE]
   >
   >Para obter informações sobre o gerenciamento local de ambientes de projeto do Commerce, consulte [Gerenciamento de ramificações com a CLI](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/develop/cli-branches) no _Guia do Usuário do Adobe Commerce na Infraestrutura da Nuvem_.

1. Faça check-out da ramificação de ambiente para atualizar usando a CLI da Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Adicionar o metapackage `magento/hipaa-ee` à configuração do compositor usando a CLI do compositor.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Atualize as dependências do pacote.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Adicione, commite e pressione o código atualizado no nuvem ambiente.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   Mover as atualizações inicia a [Comércio nuvem processo](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/develop/deploy/process) implantação aplicação das alterações. Verifique o status do implantação no [log](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log) de implantar.

### Verificar instalação

Depois que as atualizações forem implantadas, verifique se a `Hipaa*` extensão está instalada

1. Use o SSH para fazer logon no ambiente de nuvem remoto.

   ```shell
   magento-cloud ssh
   ```

1. Na linha de comando, use a Adobe Systems CLI Comércio para verificar o status módulo.

   ```shell
   bin/magento module:status
   ```

1. Verifique se os módulos HIPAA estão incluídos na lista dos módulos habilitados:

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   Todos os módulos com `Magento_Hipaa` prefixos devem estar na seção de módulos habilitados.

## Aprimoramentos de recursos para preparação HIPAA

A extensão `magento/hipaa-ee` apresenta algumas alterações e aprimoramentos ao produto base do Commerce. As seções a seguir fornecem detalhes sobre essas alterações e como elas alteram o produto base.

### Logs de ação

O registro de auditoria é um requisito da HIPAA. No Adobe Commerce, o recurso [Logs de ação](../../systems/action-log.md) registra todas as alterações feitas por um usuário administrador que trabalha na sua loja. Para atender aos requisitos da HIPAA para o Log de auditoria, o recurso foi atualizado para registrar todas as ações de usuário administrador e cliente executadas por meio da interface do usuário do administrador e por meio de chamadas de API.

Os logs de ação também capturam eventos quando os serviços da Adobe acessam os dados da loja. Você pode identificar esses eventos filtrando a Ação &quot;Dados enviados fora&quot; no relatório Logs de ação.

#### Relatório de logs de ação

A grade de relatório _Logs de Ação_ (**[!UICONTROL System]** > Logs de Ação > Relatório) foi modificada para acomodar as ações do cliente executadas por meio da interface do usuário e da API de Administração.

1. Adição de duas colunas:
   - ***Source***: mostra onde a ação foi executada.
Valores: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Tipo de Cliente***: exibe o tipo de cliente.
Valores: Cliente | Admin | Integração

2. Coluna ***Nome de Usuário*** renomeada para ***Identificador de Cliente***
   - ***Identificador do Cliente***: Exibe a ID de logon do usuário que executou a ação.
Valores:
      - um email se o Tipo de cliente for Cliente
      - um nome de usuário se o tipo de cliente for Admin
      - um nome se o Tipo de cliente for Integração

3. Renomeação da coluna Nome da ação ***completa para*** Target **&#x200B;**&#x200B;**
   - **&#x200B;**&#x200B;**Target: Exibe o nome da ação.
Valores:
      - um terminal se Origem for uma API REST ou UMA API SOAP
      - um nome de query ou mutação se uma API GraphQL
      - um nome de ação se um administrador interface ou o Cliente interface.

#### Configurar ações de administrador para o fazendo logon

Este recurso não está disponível porque todas as ações devem ser registradas por padrão.

### Restrição de resultados Search do cliente HIPAA

A restrição de resultados Search do cliente HIPAA funcionalidade na Adobe Systems Comércio garante a conformidade com as regulamentações da HIPAA, limitando o acesso às Informações de Saúde Protegidas (PHI) e às Informações Pessoais Identificáveis (PII). Esse recurso restringe a capacidade de pesquisa e visualização registros de clientes com base em funções usuário, garantindo que apenas os usuários autorizados possam acessar essas informações.

#### Principais recursos

- **Restrições Search: os usuários sem as funções necessárias** não podem pesquisa nem visualização registros de clientes.
- **Search obrigatório para acesso**: ao contrário do Adobe Systems padrão Comércio comportamento, não é possível ver as informações do cliente sem executar uma pesquisa. Isso garante que os usuários saibam detalhes específicos sobre um cliente para localizar suas informações.
- **Resultados Search limitados**: Search resultados correspondentes aos critérios são limitados a 10 registros, garantindo que apenas um número gerenciável de registros seja exibido de cada vez.
- **Número mínimo de filtros**: os usuários devem aplicar no mínimo três filtros (por exemplo, email, sobrenome e estado) para realizar uma pesquisa, garantindo que as pesquisas sejam específicas e direcionadas.
- **Filtrar Notificações**: quando pesquisa restrições são ativadas, os usuários são notificados a aplicar filtros para refinar seus resultados de pesquisa.

#### Configuração

A configuração para limitar o número de clientes no pesquisa resultados está localizada no painel administrador em **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**. Essa configuração é ativada por padrão quando a `hipaa-ee` extensão é instalada.

- **Número limite de clientes na grade**: esta configuração permite ativar ou desativar a limitação no número de clientes exibidos na grade pesquisa resultados.
- **Customer Grid Search Result Limit**: esta configuração especifica o número máximo de registros do cliente que podem ser exibidos na grade pesquisa resultados.

#### Áreas funcionais afetadas

As grades do cliente na página Criar Pedido do Administrador (**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]**) e na página Clientes (**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**) são afetadas pela funcionalidade de restrição dos resultados da pesquisa.

- Os filtros são abertos por padrão.
- Os usuários devem aplicar um mínimo de três filtros para realizar uma pesquisa.
- Os resultados da pesquisa são limitados a 10 registros por padrão.
- Se houver mais registros que correspondam aos critérios de pesquisa, as notificações informarão os usuários sobre o limite de resultados e a necessidade de refinar sua pesquisa.
- A paginação em grade não está disponível.
- Os resultados e filtros de pesquisa anteriores aplicados não são salvos ao sair da página.

A funcionalidade de restrição de resultados de pesquisa também se aplica à API REST para pesquisa de cliente (`/V1/customers/search`).

- Sem filtros aplicados ou com filtros insuficientes, a API retorna uma mensagem de erro indicando que o número necessário de filtros é necessário para executar uma pesquisa.
- Quando filtros suficientes são aplicados por usuários autorizados, a API retorna resultados dentro do limite especificado.
- Quando os resultados são limitados, uma mensagem é adicionada à resposta, indicando o número total de registros encontrados e o limite aplicado atual.

### recursos de Importar e exportação

Os aprimoramentos nos recursos de importação e exportação estão focados em melhorar o experiência administrativo e proporcionar melhor visibilidade às ações de usuário.

>[!NOTE]
>
>Esses ***aprimoramentos não alteram a lógica*** principal de Importar e de Exportação; ampliam a funcionalidade para oferta fazendo logon mais abrangentes e melhores atribuição de dados. As funcionalidade fundamentais de importação e exportação permanecem inalteradas. Os usuários podem continuar a usar os recursos e as workflows existentes sem qualquer interrupção.

#### Ação administrativa fazendo logon

Uma das principais melhorias nos recursos de importação e exportação é o aprimoramento fazendo logon das ações administrativas. Essa melhoria introduz a capacidade de aprofundar as atividades associadas à importação e à exportação de dados, contribuindo para a melhoria das rastreamento e da auditabilidade. As seguintes ações agora são registradas e refletidas no **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**&#x200B;grade:

| Tipo | Ações |
| ---- | ------- |
| Importação | <ul><li>Um usuário administrador executa uma importação<li>Um usuário administrador baixa um arquivo importado<li>Um usuário administrador baixa um arquivo de erro<ul/> |
| Exportar | <ul><li>Solicitações de um usuário administrador<li>Um usuário administrador baixa um arquivo exportado<ul/> |
| Importações/exportações programadas | <ul><li>Um administrador usuário agenda a exportação<li>Um administrador usuário edita uma exportação agendada<li>Um administrador usuário executa uma exportação agendada<li>Um administrador usuário exclui uma exportação agendada<li>Um administrador usuário agenda uma importação<li>Um administrador usuário edita uma importação agendada<li>Um administrador usuário executa uma importação agendada<li>Um administrador usuário exclui uma importação agendada<li>Um administrador usuário executa uma exclusão em massa das operações de importação/exportação<ul/> |

### Aprimoramentos de exibição e filtragem e classificação aprimorados

Para capacitar usuários administradores com grades mais informativas, o serviço HIPAA-Ready fornece vários aprimoramentos para exibir, filtrar e classificar dados.

#### histórico de Importar ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Ativação da filtragem para todas as colunas, exceto para **[!UICONTROL Imported File]**, **[!UICONTROL Error File]** e **[!UICONTROL Execution Time]**&#x200B;**[!UICONTROL Summary]**.

#### Exportar ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Adicionada uma **[!UICONTROL ID]** coluna.
- Adicionada uma **[!UICONTROL Requested At]** coluna (_data e hora em que a exportação foi solicitada_).
- Adicionada uma **[!UICONTROL User]** coluna (_nome de usuário de um administrador que fez o solicitação_).
- Remoção de uma **[!UICONTROL Action]** coluna.
- **[!UICONTROL Download]** O link foi movido para uma **[!UICONTROL File name]** coluna (_curtir à grade_ do Histórico Importar).
- Desabilitou a ação responsável pela exclusão de um arquivo exportado (_para melhorar os rastreamento_).
- Ativação da classificação para todas as colunas, exceto **[!UICONTROL File name]**.
- Ativação da filtragem para todas as colunas.

#### Importações e exportações agendadas ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Adicionada uma **[!UICONTROL ID]** coluna.
- Adicionada uma **[!UICONTROL Scheduled At]** coluna (a data e a _hora em que a importação ou exportação estava agendada_).
- Adição de uma coluna **[!UICONTROL User]** (o _nome de usuário de um usuário Administrador que agendou a importação ou exportação_).

## Serviços e ferramentas prontos para HIPAA

Esta seção descreve os serviços de Adobe Systems prontos para HIPAA que estão disponíveis para uso com a oferta HIPAA para Adobe Systems Comércio. Ela também descreve ferramentas que podem ser usadas para ajudar a monitor principais controles de segurança e conformidade para suas armazenamento.

| Serviço | Produção | Preparo | preparo_para_suporte | Desenvolvimento |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce com complemento de assistência médica | Sim | Sim | Sim | Não |
| SendGrid | Não | Não | Não | Não |
| Serviço de email simples do AWS | Sim | Sim | Sim | Não |

### Serviços Comércio da Adobe Systems

A tabela a seguir identifica Adobe Systems serviços Comércio disponíveis para a oferta de preparação HIPAA. Esses serviços incluem, entre outros:

| Serviço | Não produção | Produção |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/overview/) | Sim | Sim |
| [Malha de API para Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/) | Sim | Sim |
| [Exportação de dados do SaaS](https://experienceleague.adobe.com/pt-br/docs/commerce/saas-data-export/overview) | Sim | Sim |
| [Live search](https://experienceleague.adobe.com/pt-br/docs/commerce/live-search/overview) | Não | Não |
| [recomendações do produto](https://experienceleague.adobe.com/pt-br/docs/commerce/product-recommendations/overview) | Não | Não |
| [Serviços de pagamento](https://experienceleague.adobe.com/pt-br/docs/commerce/payment-services/guide-overview) | Não | Não |
| [Eventos de escritório Anterior de conexão de dados](https://experienceleague.adobe.com/pt-br/docs/commerce/data-connection/event-forwarding/events-backoffice) | Sim | Sim |
| [Eventos de storefront de conexão de dados](https://experienceleague.adobe.com/pt-br/docs/commerce/data-connection/event-forwarding/events#storefront-events) | Não | Não |
| [Audience Activation](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/customers/audience-activation) | Não | Não |

### Ferramentas

A [Ferramenta](../../systems/security-scan.md) de Verificação de Segurança para Adobe Systems Comércio ajuda você a monitor armazenamento para garantir que todos os controles de segurança necessários estejam ativados e operacionais. Além das verificações de segurança padrão, a Adobe Systems melhorou a ferramenta de exibir verificações específicas hipaa para clientes que usam a oferta HIPAA para Adobe Systems Comércio. As verificações HIPAA na Ferramenta de Verificação de Segurança foram projetadas para garantir que:

- Os módulos de auditoria não estão desabilitados
- A autenticação de dois fatores (2FA) não está desabilitada
- Os recursos de marketing estão desativados
- Todas as extensões instaladas correspondem a uma lista de permissões predefinida
- Nenhum serviço de Adobe Systems não suportado está instalado

Você pode [configurar a ferramenta](../../systems/security-scan.md#run-a-security-scan) para enviar notificações por e-mail com detalhes de verificações agendadas ou [relatórios visualização](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/launch/overview#to-review-the-report) manualmente.

## Recursos desativados

Para atender aos requisitos HIPAA, alguns recursos suportados pelo Adobe Systems Comércio não estão disponíveis ou desabilitados por padrão. Os comerciantes têm a opção de reativar ou usar esses recursos por sua conta e risco.

Os recursos a seguir são desativados por padrão no módulo de preparação para HIPAA. Os comerciantes podem ativar qualquer um desses recursos por sua conta e risco.

- **[Email transacional](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html?lang=pt-BR)** — SendGrid está desabilitado por padrão porque o serviço não está pronto para HIPAA. O Adobe Commerce fornece uma opção de integração que você pode usar com sua própria conta do [AWS Simple Email Service](https://docs.aws.amazon.com/ses/). Entre em contato com o Gerente técnico de conta do cliente ou com o Suporte da Adobe Commerce para obter detalhes sobre a configuração.

- **[Check-out de convidado](../../stores-purchase/checkout-guest.md)**—Este recurso apresenta um risco potencial para vários aspectos da HIPAA, incluindo registro, controle de acesso, higiene e linhagem de PHI e possivelmente mais.

- **[Recurso de boletim informativo](../../merchandising-promotions/newsletters.md)** — esse recurso está desabilitado para impedir que o PHI seja usado em um contexto de marketing.

- **[Configuração do serviço Relatórios Avançados](../../getting-started/business-intelligence.md)**—Esta configuração está desabilitada para impedir que o PHI seja usado para análise e relatórios.
