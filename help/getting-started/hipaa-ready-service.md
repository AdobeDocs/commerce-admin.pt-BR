---
title: Disponibilidade para HIPAA no Adobe Commerce
description: Saiba como você pode adicionar o módulo HIPAA-Ready da Adobe Commerce e obter recursos e funcionalidades adicionais que permitem cumprir suas obrigações com a HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 7e132d66523feba579baf0bae14e1de9de4d6591
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 0%

---

# Disponibilidade para HIPAA no Adobe Commerce

>[!IMPORTANT]
>
>**Aviso legal**<br/>
>Estas informações são destinadas a ajudar os clientes do Adobe a responder às suas perguntas sobre o Adobe HIPAA-Ready Services. Não constitui um aconselhamento jurídico. Os comerciantes devem consultar seu próprio serviço jurídico para entender suas obrigações conforme a HIPAA e o uso e a configuração apropriados dos produtos de Adobe.

>[!BEGINSHADEBOX]

**HIPAA (Health Insurance Portability and Accountability Act, Lei de Portabilidade e Responsabilidade de Seguros de Saúde)**

A HIPAA (Health Insurance Portability and Accountability Act, Lei de Portabilidade e Responsabilidade do Seguro de Saúde) é a principal lei federal de privacidade da área de saúde nos Estados Unidos e é aplicada pelo Departamento de Saúde e Serviços Humanos (HHS) dos EUA. HIPAA se aplica a _Entidades Cobertas_ (como prestadores de cuidados de saúde, seguradoras e câmaras de compensação) e _Associados de Negócios_ (como as entidades que prestam serviços a entidades abrangidas). Os requisitos da HIPAA são definidos em três regras separadas: Regra de privacidade, Regra de segurança e Regra de notificação de violação. O Adobe atua como um Business Associate para determinados produtos, o que o Adobe classifica como &quot;Serviços prontos para HIPAA&quot;. Os dados regulamentados pela HIPAA são chamados de _Informações de saúde protegidas_ ou PHI. PHI é um subconjunto de informações de saúde que (1) é criado ou recebido por um prestador de cuidados de saúde, plano de saúde ou câmara de compensação de cuidados de saúde, (2) se relaciona com a saúde ou condição física ou mental passada, presente ou futura de um indivíduo, com a prestação de cuidados de saúde a um indivíduo, ou com o pagamento passado, presente ou futuro pela prestação de cuidados de saúde a um indivíduo, e (3) identifica o indivíduo ou a respeito do qual há uma base razoável para acreditar que a informação pode ser usada para identificar o indivíduo. As Regras de Privacidade e Segurança da HIPAA exigem que uma Entidade Coberta obtenha garantias por escrito de um Associado Comercial na forma de um Contrato de Associado Comercial, ou BAA, exigindo que o Associado Comercial proteja a privacidade e a segurança da PHI ʼ Entidade Coberta. Para obter mais informações, consulte [Produtos e serviços HIPAA e Adobe](https://www.adobe.com/trust/compliance/hipaa-ready.html) no Centro de confiança do Adobe.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA-Ready

O Adobe Commerce HIPAA-Ready tem recursos e funcionalidades adicionais que permitem aos comerciantes cumprir com suas respectivas obrigações com a HIPAA.

O Adobe Commerce HIPAA-Ready é fornecido como uma extensão do Adobe Commerce, `magento/hipaa-ee` que está disponível para projetos do Adobe Commerce na infraestrutura em nuvem ou Adobe Managed Services. O processo de instalação Adobe Commerce HIPAA-Ready desativa alguns serviços e recursos nativos para atender aos requisitos da HIPAA. Consulte [Serviços e recursos desabilitados](#disabled-services-and-features).

*Esses materiais são destinados apenas a fins informativos. O fornecimento dessas informações não confere ao destinatário nenhum direito contratual ou de outro tipo. Embora tenham sido envidados esforços para garantir a exatidão das informações à data em que foram fornecidas, não é feita qualquer declaração de que tais informações sejam exatas e completas. A Adobe não assume nenhuma obrigação de atualizar essas informações à medida que a lei ou os produtos de Adobe mudam. Além disso, este documento não deve ser distribuído a nenhuma parte além do recipient pretendido sem o consentimento por escrito da Adobe.*

## Requisitos do sistema

O Adobe Commerce deve ser implantado no Adobe Commerce na infraestrutura em nuvem ou no Adobe Commerce Managed Services com a versão 2.4.6-p3 ou posterior (sem versões beta).

## Instalação

Instale a versão mais recente da extensão Adobe HIPAA-Ready Services (`magento/hipaa-ee`) em uma instância que esteja executando o Adobe Commerce versão 2.4.6-p3 ou posterior. A extensão é entregue como um metapackage de compositor do [repo.magento.com](https://repo.magento.com) repositório.

>[!BEGINSHADEBOX]

**Pré-requisito**

Você deve ter acesso a [repo.magento.com](https://repo.magento.com) para instalar a extensão. Para geração de chaves e obtenção dos direitos necessários, consulte [Obter suas chaves de autenticação](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

1. Na estação de trabalho local, altere para o diretório do projeto do Adobe Commerce na infraestrutura em nuvem.

   >[!NOTE]
   >
   >Para obter informações sobre como gerenciar os ambientes de projeto do Commerce localmente, consulte  [Gerenciamento de ramificações com a CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) no _Guia do usuário do Adobe Commerce na infraestrutura em nuvem_.

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

   Enviar as atualizações inicia o [Processo de implantação da nuvem do Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) para aplicar as alterações. Verifique o status da implantação no [implantar log](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Verificar instalação

Depois que as atualizações forem implantadas, verifique se `Hipaa*` extensão instalada

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
   <truncated for brevity>
   ```

   Todos os módulos com prefixo `Magento_Hipaa` deve estar na seção de módulos habilitados.

## Aprimoramentos de recursos para prontidão para HIPAA

A variável `magento/hipaa-ee` O pacote do apresenta algumas alterações e aprimoramentos ao produto base do Commerce. As seções a seguir fornecem detalhes sobre essas alterações e como elas alteram o produto base.

### Logs de ação

O registro de auditoria é um requisito da HIPAA. No Adobe Commerce, a variável [Logs de ação](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) O recurso registra todas as alterações feitas por um usuário administrador que trabalha na sua loja. Para atender aos requisitos da HIPAA para o Log de auditoria, o recurso foi atualizado para registrar todas as ações de usuário administrador e cliente executadas por meio da interface do usuário do administrador e por meio de chamadas de API.

#### Relatório de logs de ação

A variável _Logs de ação_ grade de relatório (**[!UICONTROL System]** > Logs de ação > Relatório) é modificado para acomodar as ações do cliente executadas por meio da interface do usuário e da API de administração.

1. Adição de duas colunas:
   - ***Origem***: exibe onde a ação foi executada.
Valores: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Tipo de cliente***: exibe o tipo de cliente.
Valores: Cliente | Admin | Integração

2. A variável foi renomeada ***Nome de usuário*** coluna para ***Identificador do cliente***
   - ***Identificador do cliente***: exibe a ID de logon do usuário que executou a ação.
Valores:
      - um email se o Tipo de cliente for Cliente
      - um nome de usuário se o tipo de cliente for Admin
      - um nome se o Tipo de cliente for Integração

3. A variável foi renomeada ***Nome completo da ação*** coluna para ***Target***
   - ***Target***: exibe o nome da ação.
Valores:
      - um endpoint se a Origem for uma API REST ou SOAP
      - um nome de consulta ou mutação se uma API do GraphQL
      - um nome de ação se for uma interface do usuário do administrador ou do cliente.

#### Configurar ações do administrador para fazer logon

Este recurso não está disponível porque todas as ações devem ser registradas por padrão.

### Importar e exportar recursos

Os aprimoramentos nos recursos de importação e exportação se concentram em melhorar a experiência administrativa e fornecer maior visibilidade sobre as ações do usuário.

>[!NOTE]
>
>Esses ***As melhorias não alteram a lógica principal de Importação e Exportação***; em vez disso, eles estendem a funcionalidade para oferecer um registro mais abrangente e uma atribuição de dados aprimorada. A funcionalidade fundamental de importação e exportação permanece inalterada. Os usuários podem continuar usando os recursos e fluxos de trabalho existentes sem interrupções.

#### Registro de ação administrativa

Uma das principais melhorias nos recursos de importação e exportação é o registro aprimorado de ações administrativas. Esse aprimoramento apresenta a capacidade de detalhar as atividades associadas à importação e exportação de dados, contribuindo para melhorar o rastreamento e a capacidade de auditoria. As ações a seguir são registradas e refletidas na variável **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**grade:

| Tipo | Ações |
| ---- | ------- |
| Importar | <ul><li>Um usuário administrador executa uma importação<li>Um usuário administrador baixa um arquivo importado<li>Um usuário administrador baixa um arquivo de erro<ul/> |
| Exportar | <ul><li>Solicitações de um usuário administrador<li>Um usuário administrador baixa um arquivo exportado<ul/> |
| Importações/exportações programadas | <ul><li>Um usuário administrador programa a exportação<li>Um usuário administrador edita uma exportação agendada<li>Um usuário administrador executa uma exportação agendada<li>Um usuário administrador exclui uma exportação agendada<li>Um usuário administrador programa uma importação<li>Um usuário administrador edita uma importação agendada<li>Um usuário administrador executa uma importação agendada<li>Um usuário administrador exclui uma importação agendada<li>Um usuário administrador executa uma exclusão em massa de operações de importação/exportação<ul/> |

### Melhorias na exibição e filtragem e classificação aprimoradas

Para capacitar os usuários administradores com grades mais informativas, o serviço HIPAA-Ready oferece várias melhorias para exibir, filtrar e classificar dados.

#### Importar histórico ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Ativação da filtragem para todas as colunas, exceto para **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**, e **[!UICONTROL Summary]**.

#### Exportar ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Adição de um **[!UICONTROL ID]** coluna.
- Adição de um **[!UICONTROL Requested At]** coluna (_data e hora da solicitação de exportação_).
- Adição de um **[!UICONTROL User]** coluna (_nome de usuário de um administrador que fez a solicitação_).
- Remoção de um **[!UICONTROL Action]** coluna.
- Moveu o **[!UICONTROL Download]** link para um **[!UICONTROL File name]** coluna (_como a grade Importar Histórico_).
- Desativada a ação responsável pela exclusão de um arquivo exportado (_para melhorar o rastreamento_).
- Classificação ativada para todas as colunas, exceto **[!UICONTROL File name]**.
- Filtragem ativada para todas as colunas.

#### Importações e exportações programadas ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Adição de um **[!UICONTROL ID]** coluna.
- Adição de um **[!UICONTROL Scheduled At]** coluna (a _data e hora agendadas da importação ou exportação_).
- Adição de um **[!UICONTROL User]** coluna (a _nome de usuário de um usuário administrador que agendou a importação ou exportação_).

## Serviços e recursos desabilitados

Para estar em conformidade com os requisitos da HIPAA, alguns serviços e recursos compatíveis com o Adobe Commerce não estão disponíveis ou estão desativados por padrão. Os comerciantes têm a opção de reativar ou usar esses serviços e recursos por sua conta e risco.

### Serviços

- **Serviços da Adobe Commerce**— nenhum dos serviços da Adobe Commerce ou de extensibilidade está disponível na oferta de preparação para HIPAA. Esses serviços incluem, entre outros:

   - Live Search
   - API Mesh
   - Construtor de aplicativos
   - Serviço de catálogo

- **[Serviço SendGrid](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**—Este serviço está desativado por padrão porque o aplicativo não é compatível com HIPAA. Os comerciantes podem enviar uma solicitação de suporte para ativar o Sendgrid, mas devem reconhecer que assumem o risco de usar o serviço.

### Recursos desabilitados por padrão

Os recursos a seguir são desativados por padrão no módulo de preparação para HIPAA. Os comerciantes podem ativar qualquer um desses recursos por sua conta e risco.

- **[Check-out de convidado](../stores-purchase/checkout-guest.md)**— esse recurso apresenta um risco potencial para vários aspectos da HIPAA, incluindo registro, controle de acesso, higiene e linhagem de PHI e possivelmente mais.

- **[Recurso de informativo](../merchandising-promotions/newsletters.md)**—Este recurso está desativado para impedir que a PHI seja usada em um contexto de marketing.

- **[Configuração do serviço de relatório avançado](../getting-started/business-intelligence.md)**— Essa configuração é desativada para impedir que o PHI seja usado para análise e relatórios.
