---
title: Disponibilidade para HIPAA no Adobe Commerce
description: Saiba como adicionar a extensão do Adobe Commerce pronta para HIPAA e obtenha recursos e funcionalidades adicionais que permitem cumprir com as suas obrigações com a HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: b380977e74c7f49c4d179e633242e3d7e6b1e1e7
workflow-type: tm+mt
source-wordcount: '2300'
ht-degree: 1%

---

# Disponibilidade para HIPAA no Adobe Commerce

>[!IMPORTANT]
>
>**Aviso de isenção legal**<br/>
>Estas informações são destinadas a ajudar os clientes do Adobe a responder às suas perguntas sobre o Adobe HIPAA-Ready Services. Não constitui um aconselhamento jurídico. Os comerciantes devem consultar seu próprio serviço jurídico para entender suas obrigações conforme a HIPAA e o uso e a configuração apropriados dos produtos de Adobe.

>[!BEGINSHADEBOX]

**HIPAA (Health Insurance Portability and Accountability Act, Lei de Portabilidade e Responsabilidade do Seguro de Saúde)**

A HIPAA (Health Insurance Portability and Accountability Act, Lei de Portabilidade e Responsabilidade do Seguro de Saúde) é a principal lei federal de privacidade da área de saúde nos Estados Unidos e é aplicada pelo Departamento de Saúde e Serviços Humanos (HHS) dos EUA. A HIPAA se aplica a _Entidades Cobertas_ (como provedores de assistência médica, seguradoras e centros de compensação) e _Associados Comerciais_ (como as entidades que fornecem serviços a entidades cobertas). Os requisitos da HIPAA são definidos em três regras separadas: Regra de privacidade, Regra de segurança e Regra de notificação de violação. O Adobe atua como um Business Associate para determinados produtos, o que o Adobe classifica como &quot;Serviços prontos para HIPAA&quot;. Os dados regulamentados pela HIPAA são chamados de _Informações de Integridade Protegidas_ ou PHI. PHI é um subconjunto de informações de saúde que (1) é criado ou recebido por um prestador de cuidados de saúde, plano de saúde ou câmara de compensação de cuidados de saúde, (2) se relaciona com a saúde ou condição física ou mental passada, presente ou futura de um indivíduo, com a prestação de cuidados de saúde a um indivíduo, ou com o pagamento passado, presente ou futuro pela prestação de cuidados de saúde a um indivíduo, e (3) identifica o indivíduo ou a respeito do qual há uma base razoável para acreditar que a informação pode ser usada para identificar o indivíduo. As Regras de Privacidade e Segurança da HIPAA exigem que uma Entidade Coberta obtenha garantias por escrito de um Associado Comercial na forma de um Contrato de Associado Comercial, ou BAA, exigindo que o Associado Comercial proteja a privacidade e a segurança da PHI ʼ Entidade Coberta. Para obter mais informações, consulte [Produtos e Serviços da HIPAA e do Adobe](https://www.adobe.com/trust/compliance/hipaa-ready.html) no Centro de Confiabilidade do Adobe.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA-Ready

A extensão Adobe Commerce HIPAA-Ready adiciona recursos e funcionalidades adicionais às instalações do Adobe Commerce, permitindo que os comerciantes cumpram com suas respectivas obrigações com a HIPAA.

A extensão HIPAA-Ready da Adobe Commerce, `magento/hipaa-ee` está disponível para projetos Adobe Commerce na infraestrutura em nuvem ou Adobe Managed Services. O processo de instalação Adobe Commerce HIPAA-Ready desativa alguns serviços e recursos nativos para atender aos requisitos da HIPAA. Consulte [Serviços e recursos desabilitados](#disabled-services-and-features).

>[!NOTE]
>
>O acesso aos recursos e funcionalidades prontos para a HIPAA está disponível somente para comerciantes que compraram o complemento de assistência médica da Adobe Commerce.

*Estes materiais são apenas para fins informativos. O fornecimento dessas informações não confere ao destinatário nenhum direito contratual ou de outro tipo. Embora tenham sido envidados esforços para garantir a exatidão das informações à data em que foram fornecidas, não é feita qualquer declaração de que tais informações sejam exatas e completas. A Adobe não assume nenhuma obrigação de atualizar essas informações à medida que a lei ou os produtos de Adobe mudam. Além disso, este documento não deve ser distribuído a nenhuma parte além do destinatário pretendido sem o consentimento por escrito do Adobe.*

## Requisitos do sistema

O Adobe Commerce deve ser implantado no Adobe Commerce na infraestrutura em nuvem ou no Adobe Commerce Managed Services com a versão 2.4.6-p3 - 2.4.6-p8 (sem versões beta).

## Instalação

**Pré-requisito**

>[!BEGINSHADEBOX]

- O Adobe provisionou sua conta do Adobe Commerce para acessar a extensão HIPAA Ready.
- Acesso ao [repo.magento.com](https://repo.magento.com) para instalar a extensão. Para geração de chaves e obtenção dos direitos necessários, consulte [Obter suas chaves de autenticação](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

Instale a versão mais recente da extensão Adobe HIPAA-Ready Services (`magento/hipaa-ee`) em uma instância que esteja executando o Adobe Commerce versão 2.4.6-p3 - 2.4.6-p8. A extensão é entregue como um metapackage de compositor do [repositório.magento.com](https://repo.magento.com). O metapackage inclui a coleção de módulos que habilitam os recursos HIPAA para uma instância do Adobe Commerce.

>[!NOTE]
>
>Para garantir que os dados do evento de back office enviados para o Experience Platform estejam prontos para HIPAA, consulte o [guia de extensão de Conexão de Dados](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/install#install-the-data-services-hipaa-extension).

1. Na estação de trabalho local, altere para o diretório do projeto do Adobe Commerce na infraestrutura em nuvem.

   >[!NOTE]
   >
   >Para obter informações sobre o gerenciamento local de ambientes de projeto do Commerce, consulte [Gerenciamento de ramificações com a CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) no _Guia do Usuário do Adobe Commerce na Infraestrutura da Nuvem_.

1. Faça check-out da ramificação de ambiente para atualizar usando a CLI do Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Adicionar o metapackage `magento/hipaa-ee` à configuração do compositor usando a CLI do compositor.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Atualizar dependências de pacote.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Adicione, confirme e envie por push o código atualizado para o ambiente de nuvem.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   O envio das atualizações inicia o [processo de implantação da nuvem do Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) para aplicar as alterações. Verifique o status da implantação no [log de implantação](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Verificar instalação

Depois que as atualizações forem implantadas, verifique se a extensão `Hipaa*` está instalada

1. Use o SSH para fazer logon no ambiente de nuvem remoto.

   ```shell
   magento-cloud ssh
   ```

1. Na linha de comando, use a Adobe Commerce CLI para verificar o status do módulo.

   ```shell
   bin/magento module:status
   ```

1. Verifique se os módulos HIPAA estão incluídos na lista de módulos habilitados:

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

   Todos os módulos com o prefixo `Magento_Hipaa` devem estar na seção de módulos habilitados.

## Aprimoramentos de recursos para prontidão para HIPAA

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

3. A coluna ***Nome da Ação Completa*** foi renomeada para ***Destino***
   - ***Destino***: exibe o nome da ação.
Valores:
      - um endpoint se o Source for uma API REST ou SOAP
      - um nome de consulta ou mutação se uma API do GraphQL
      - um nome de ação se for uma interface do usuário do administrador ou do cliente.

#### Configurar ações do administrador para fazer logon

Este recurso não está disponível porque todas as ações devem ser registradas por padrão.

### Restrição dos resultados de pesquisa do cliente HIPAA

A funcionalidade HIPAA Customer Search Results Restriction (Restrição de resultados de pesquisa de clientes HIPAA) no Adobe Commerce garante a conformidade com as normas HIPAA, limitando o acesso a PHI (Protected Health Information, informações protegidas de saúde) e PII (Personally Identifying Information, informações pessoais identificáveis). Esse recurso restringe a capacidade de pesquisar e visualizar registros de clientes com base nas funções de usuário, garantindo que somente usuários autorizados possam acessar essas informações.

#### Principais recursos

- **Restrições de Pesquisa**: Usuários sem as funções necessárias não podem pesquisar ou exibir registros de clientes.
- **Pesquisa obrigatória pelo Access**: ao contrário do comportamento padrão do Adobe Commerce, não é possível ver as informações do cliente sem realizar uma pesquisa. Isso garante que os usuários saibam detalhes específicos sobre um cliente para localizar suas informações.
- **Resultados de Pesquisa Limitados**: os resultados de pesquisa correspondentes aos critérios são limitados a 10 registros, garantindo que apenas um número gerenciável de registros seja exibido por vez.
- **Número mínimo de filtros**: os usuários devem aplicar no mínimo três filtros (por exemplo, email, sobrenome e estado) para realizar uma pesquisa, garantindo que as pesquisas sejam específicas e direcionadas.
- **Notificações de Filtro**: quando as restrições de pesquisa estão habilitadas, os usuários são notificados para aplicar filtros e refinar os resultados da pesquisa.

#### Configuração

A configuração para limitar o número de clientes nos resultados da pesquisa está localizada no painel de administração em **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**. Essa configuração é habilitada por padrão quando a extensão `hipaa-ee` é instalada.

- **Limitar Número de Clientes na Grade**: esta configuração permite habilitar ou desabilitar a limitação do número de clientes exibidos nos resultados da pesquisa de grade.
- **Limite de Resultados de Pesquisa de Grade do Cliente**: essa configuração especifica o número máximo de registros do cliente que podem ser exibidos nos resultados da pesquisa de grade.

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
- Quando os resultados forem limitados, uma mensagem será adicionada à resposta indicando o número total de registros encontrados e o limite aplicado atual.

### Importar e exportar recursos

Os aprimoramentos nos recursos de importação e exportação se concentram em melhorar a experiência administrativa e fornecer maior visibilidade sobre as ações do usuário.

>[!NOTE]
>
>Esses ***aprimoramentos não alteram a lógica principal de Importação e Exportação***; em vez disso, eles estendem a funcionalidade para oferecer um log mais abrangente e atribuições de dados aprimoradas. A funcionalidade fundamental de importação e exportação permanece inalterada. Os usuários podem continuar usando os recursos e fluxos de trabalho existentes sem interrupções.

#### Registro de ação administrativa

Uma das principais melhorias nos recursos de importação e exportação é o registro aprimorado de ações administrativas. Esse aprimoramento apresenta a capacidade de detalhar as atividades associadas à importação e exportação de dados, contribuindo para melhorar o rastreamento e a capacidade de auditoria. As seguintes ações foram registradas e refletidas na grade **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**:

| Tipo | Ações |
| ---- | ------- |
| Importar | <ul><li>Um usuário administrador executa uma importação<li>Um usuário administrador baixa um arquivo importado<li>Um usuário administrador baixa um arquivo de erro<ul/> |
| Exportar | <ul><li>Solicitações de um usuário administrador<li>Um usuário administrador baixa um arquivo exportado<ul/> |
| Importações/exportações programadas | <ul><li>Um usuário administrador programa a exportação<li>Um usuário administrador edita uma exportação agendada<li>Um usuário administrador executa uma exportação agendada<li>Um usuário administrador exclui uma exportação agendada<li>Um usuário administrador programa uma importação<li>Um usuário administrador edita uma importação agendada<li>Um usuário administrador executa uma importação agendada<li>Um usuário administrador exclui uma importação agendada<li>Um usuário administrador executa uma exclusão em massa de operações de importação/exportação<ul/> |

### Melhorias na exibição e filtragem e classificação aprimoradas

Para capacitar os usuários administradores com grades mais informativas, o serviço HIPAA-Ready oferece várias melhorias para exibir, filtrar e classificar dados.

#### Importar histórico ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Filtragem habilitada para todas as colunas, exceto para **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** e **[!UICONTROL Summary]**.

#### Exportar ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Adicionada uma coluna **[!UICONTROL ID]**.
- Adição de uma coluna **[!UICONTROL Requested At]** (_data e hora em que a exportação foi solicitada_).
- Adição de uma coluna **[!UICONTROL User]** (_nome de usuário de um administrador que fez a solicitação_).
- Coluna **[!UICONTROL Action]** removida.
- O link **[!UICONTROL Download]** foi movido para uma coluna **[!UICONTROL File name]** (_como a grade Histórico de Importação_).
- Desabilitada a ação responsável pela exclusão de um arquivo exportado (_para melhorar o rastreamento_).
- Classificação habilitada para todas as colunas, exceto **[!UICONTROL File name]**.
- Filtragem ativada para todas as colunas.

#### Importações e exportações agendadas ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Adicionada uma coluna **[!UICONTROL ID]**.
- Adição de uma coluna **[!UICONTROL Scheduled At]** (a _data e hora agendadas da importação ou exportação_).
- Adição de uma coluna **[!UICONTROL User]** (o _nome de usuário de um usuário Administrador que agendou a importação ou exportação_).

## Ferramentas e serviços prontos para HIPAA

Esta seção descreve os serviços da Adobe prontos para HIPAA que estão disponíveis para uso com a oferta HIPAA para Adobe Commerce. Ele também descreve ferramentas que podem ser usadas para ajudar a monitorar os principais controles de segurança e conformidade da sua loja.

| Serviço | Produção | Estágios | preparo_para_suporte | Desenvolvimento |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce com complemento de assistência médica | Sim | Sim | Sim | Não |
| SendGrid | Não | Não | Não | Não |
| Serviço de email simples AWS | Sim | Sim | Sim | Não |

### Serviços da Adobe Commerce

A tabela a seguir identifica os serviços da Adobe Commerce que estão disponíveis para a oferta de preparação para a HIPAA. Esses serviços incluem, entre outros:

| Serviço | Não produção | Produção |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/overview/) | Sim | Sim |
| [Malha de API para Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/) | Sim | Sim |
| [Exportação De Dados SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) | Sim | Sim |
| [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overviewhttps://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) | Não | Não |
| [Recommendations do produto](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/overview) | Não | Não |
| [Serviços de pagamento](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/payment-services/guide-overview) | Não | Não |
| [Eventos de Back-Office da Conexão de Dados](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice) | Sim | Sim |
| [Eventos de Data Connection Storefront](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#storefront-events) | Não | Não |
| [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) | Não | Não |

### Ferramentas

A [Ferramenta de Verificação de Segurança](../../systems/security-scan.md) para Adobe Commerce ajuda a monitorar seu armazenamento para garantir que todos os controles de segurança necessários estejam habilitados e operacionais. Além das verificações de segurança padrão, o Adobe aprimorou a ferramenta para exibir verificações específicas de HIPAA para clientes que usam a oferta HIPAA para Adobe Commerce. As verificações de HIPAA na Ferramenta de verificação de segurança foram criadas para garantir que:

- Os módulos de auditoria não estão desabilitados
- A autenticação de dois fatores (2FA) não está desabilitada
- Os recursos de marketing estão desativados
- Incluir na lista de permissões Todas as extensões instaladas correspondem a um arquivo de pesquisa predefinido
- Não há serviços da Adobe instalados sem suporte

Você pode [configurar a ferramenta](../../systems/security-scan.md#run-a-security-scan) para enviar notificações por email com detalhes de verificações agendadas ou [exibir relatórios manualmente](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/launch/overview#to-review-the-report).

## Recursos desabilitados

Para estar em conformidade com os requisitos da HIPAA, alguns recursos compatíveis com o Adobe Commerce não estão disponíveis ou estão desativados por padrão. Os comerciantes têm a opção de reativar ou usar esses recursos por sua conta e risco.

Os recursos a seguir são desativados por padrão no módulo de preparação para HIPAA. Os comerciantes podem ativar qualquer um desses recursos por sua conta e risco.

- **[Email transacional](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** — SendGrid está desabilitado por padrão porque o serviço não está pronto para HIPAA. O Adobe Commerce fornece uma opção de integração que você pode usar com sua própria conta do [AWS Simple Email Service](https://docs.aws.amazon.com/ses/). Entre em contato com o Gerente técnico de conta do cliente ou com o Suporte da Adobe Commerce para obter detalhes sobre a configuração.

- **[Check-out de convidado](../../stores-purchase/checkout-guest.md)**—Este recurso apresenta um risco potencial para vários aspectos da HIPAA, incluindo registro, controle de acesso, higiene e linhagem de PHI e possivelmente mais.

- **[Recurso de boletim informativo](../../merchandising-promotions/newsletters.md)** — esse recurso está desabilitado para impedir que o PHI seja usado em um contexto de marketing.

- **[Configuração do serviço Relatórios Avançados](../../getting-started/business-intelligence.md)**—Esta configuração está desabilitada para impedir que o PHI seja usado para análise e relatórios.
