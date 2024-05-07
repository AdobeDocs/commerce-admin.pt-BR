---
title: Disponibilidade para HIPAA no Adobe Commerce
description: Saiba como você pode adicionar o módulo HIPAA-Ready da Adobe Commerce e obter recursos e funcionalidades adicionais que permitem cumprir suas obrigações com a HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: c21c8b76e37e617885bae3492801b45093a6b5a5
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 0%

---

# Disponibilidade para HIPAA no Adobe Commerce

>[!IMPORTANT]
>
>**Aviso legal**<br/>
>Estas informações são destinadas a ajudar os clientes do Adobe a responder às suas perguntas sobre o Adobe HIPAA-Ready Services. Não constitui um aconselhamento jurídico. Os comerciantes devem consultar seu próprio serviço jurídico para entender suas obrigações conforme a HIPAA e o uso e a configuração apropriados dos produtos de Adobe.

## HIPAA (Health Insurance Portability and Accountability Act, Lei de Portabilidade e Responsabilidade de Seguros de Saúde)

A HIPAA (Health Insurance Portability and Accountability Act, Lei de Portabilidade e Responsabilidade do Seguro de Saúde) é a principal lei federal de privacidade da área de saúde nos Estados Unidos e é aplicada pelo Departamento de Saúde e Serviços Humanos (HHS) dos EUA. HIPAA se aplica a _Entidades Cobertas_ (como prestadores de cuidados de saúde, seguradoras e câmaras de compensação) e _Associados de Negócios_ (como as entidades que prestam serviços a entidades abrangidas). Os requisitos da HIPAA são definidos em três regras separadas: Regra de privacidade, Regra de segurança e Regra de notificação de violação. O Adobe atua como um Business Associate para determinados produtos, o que o Adobe classifica como &quot;Serviços prontos para HIPAA&quot;. Os dados regulamentados pela HIPAA são chamados de _Informações de saúde protegidas_ ou PHI. PHI é um subconjunto de informações de saúde que (1) é criado ou recebido por um prestador de cuidados de saúde, plano de saúde ou câmara de compensação de cuidados de saúde, (2) se relaciona com a saúde ou condição física ou mental passada, presente ou futura de um indivíduo, com a prestação de cuidados de saúde a um indivíduo, ou com o pagamento passado, presente ou futuro pela prestação de cuidados de saúde a um indivíduo, e (3) identifica o indivíduo ou a respeito do qual há uma base razoável para acreditar que a informação pode ser usada para identificar o indivíduo. As Regras de Privacidade e Segurança da HIPAA exigem que uma Entidade Coberta obtenha garantias por escrito de um Associado Comercial na forma de um Contrato de Associado Comercial, ou BAA, exigindo que o Associado Comercial proteja a privacidade e a segurança da PHI ʼ Entidade Coberta.

## Adobe Commerce HIPAA-Ready

O Adobe Commerce HIPAA-Ready tem recursos e funcionalidades adicionais que permitem aos comerciantes cumprir com suas respectivas obrigações com a HIPAA. Você pode instalar o Adobe Commerce HIPAA-Ready (`magento/hipaa-ee`) para sua Adobe Commerce na infraestrutura em nuvem. Também há alguns recursos que devem ser desativados para estar em conformidade com a HIPAA.

*Esses materiais são destinados apenas a fins informativos. O fornecimento dessas informações não confere ao destinatário nenhum direito contratual ou de outro tipo. Embora tenham sido feitos esforços para garantir a precisão das informações a partir da data em que foram fornecidas, nenhuma declaração é feita de que tais informações são precisas e completas, e a Adobe não assume nenhuma obrigação de atualizar essas informações à medida que a lei ou os produtos de Adobe mudam. Além disso, este documento não deve ser distribuído a nenhuma parte além do recipient pretendido sem o consentimento por escrito da Adobe.*

## Requisitos do sistema

A preparação para a HIPAA no Adobe Commerce tem os mesmos requisitos de sistema da Adobe Commerce com os requisitos adicionais:

- Adobe Commerce versão 2.4.6-p3 ou mais recente (não beta)
- Adobe Commerce na infraestrutura em nuvem ou Adobe Commerce no Managed Services
- Versão mais recente da `magento/hipaa-ee` extensão

## Instalação

O Adobe HIPAA-Ready Services é tecnicamente um metapackage de compositor `magento/hipaa-ee` que contém links para módulos especiais. Este metapackage reside no repositório [repo.magento.com](https://repo.magento.com).

1. Para poder instalar `magento/hipaa-ee` metapackage, você deve ter acesso a ele. Para geração de chaves e obtenção dos direitos necessários, consulte [Obter suas chaves de autenticação](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. Verifique o ambiente em que você instalará o pacote e certifique-se de que ele atenda às [requisitos do sistema](#system-requirements).

1. Adicionar o metapackage `magento/hipaa-ee` à configuração do compositor.

   A maneira mais simples é usando a CLI do compositor. Por exemplo:

   ```shell
   composer require magento/hipaa-ee
   ```

1. Se o Adobe Commerce ainda não estiver instalado, você poderá iniciar a instalação (siga as instruções [Instruções de instalação](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)).

   Se o Adobe Commerce já estiver instalado, após o download dos módulos, execute `bin/magento setup:upgrade` e siga as recomendações.

   ```shell
   bin/magento setup:upgrade
   ```

   Quando esse comando estiver em execução, os módulos recém-baixados serão ativados e os scripts para instalá-los serão iniciados. Para saber mais sobre o gerenciamento de módulo, consulte [Ativar ou desativar módulos](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. Após a conclusão do processo de instalação ou atualização, verifique se `Hipaa*` foram incluídos módulos relevantes.

   Execute o comando:

   ```shell
   bin/magento module:status
   ```

   Se o pacote HIPAA Composer foi adicionado corretamente, você verá os módulos HIPAA na saída do comando. Por exemplo:

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

O registro de auditoria é um requisito da HIPAA. No Adobe Commerce, a variável [Logs de ação](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) O recurso registra todas as alterações feitas por um usuário administrador que trabalha na sua loja. Para atender aos requisitos da HIPAA sobre o Log de auditoria, há alterações no recurso para registrar todas as ações de usuário administrador e cliente executadas por meio da interface do usuário do administrador e por meio de chamadas de API.

#### Relatório de logs de ação

A variável _Logs de ação_ grade de relatório (**[!UICONTROL System]** > Logs de ação > Relatório) é modificado para acomodar as ações do cliente executadas por meio da interface do usuário e da API de administração.

1. Duas colunas adicionais:
   - ***Origem***: exibe onde a ação foi executada.\
     Valores: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Tipo de cliente***: exibe o tipo de cliente.\
     Valores: Cliente | Admin | Integração


2. Renomear ***Nome de usuário*** para ***Identificador do cliente***
   - ***Identificador do cliente***: exibe a ID de logon do usuário que executou a ação\
     Valores:
      - um email se o Tipo de cliente for Cliente
      - um nome de usuário se o tipo de cliente for Admin
      - um nome se o Tipo de cliente for Integração

3. Renomear ***Nome completo da ação*** para ***Target***
   - ***Target***: exibe o nome da ação\
     Valores:
      - um endpoint se a Origem for API REST ou API SOAP
      - um nome de consulta/mutação se a API do GraphQL
      - um nome de ação se for a interface do usuário do administrador ou do cliente.

#### Configurar ações do administrador para fazer logon

Este recurso não está disponível porque todas as ações devem ser registradas por padrão.

### Importar/exportar recursos

Os aprimoramentos nos recursos de importação/exportação se concentram em melhorar a experiência administrativa e fornecer maior visibilidade sobre as ações do usuário.

>[!NOTE]
>
>Esses ***As melhorias não alteram a lógica principal de Importação/Exportação***; em vez disso, eles estendem a funcionalidade para oferecer um registro mais abrangente e uma atribuição de dados aprimorada. A funcionalidade fundamental de importação/exportação permanece inalterada. Os usuários podem continuar usando os recursos e fluxos de trabalho existentes sem interrupções.

#### Registro de ação administrativa

Uma das principais melhorias nos recursos de importação/exportação é o registro aprimorado de ações administrativas. Isso introduz a capacidade de se aprofundar em atividades associadas à importação/exportação de dados, contribuindo para melhorar o rastreamento e a capacidade de auditoria. As ações a seguir são registradas e refletidas na variável **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**grade:

| Tipo | Ações |
| ---- | ------- |
| Importar | <ul><li>Um usuário administrador executa uma importação<li>Um usuário administrador baixa um arquivo importado<li>Um usuário administrador baixa um arquivo de erro<ul/> |
| Exportar | <ul><li>Solicitações de um usuário administrador<li>Um usuário administrador baixa um arquivo exportado<ul/> |
| Importações/exportações programadas | <ul><li>Um usuário administrador programa a exportação<li>Um usuário administrador edita uma exportação agendada<li>Um usuário administrador executa uma exportação agendada<li>Um usuário administrador exclui uma exportação agendada<li>Um usuário administrador programa uma importação<li>Um usuário administrador edita uma importação agendada<li>Um usuário administrador executa uma importação agendada<li>Um usuário administrador exclui uma importação agendada<li>Um usuário administrador executa uma exclusão em massa de operações de importação/exportação<ul/> |

### Melhorias na exibição e filtragem/classificação aprimorada

Para capacitar os usuários administradores com grades mais informativas, há várias melhorias na exibição de dados e nos recursos de filtragem e classificação:

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

#### Importações/exportações programadas ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Adição de um **[!UICONTROL ID]** coluna.
- Adição de um **[!UICONTROL Scheduled At]** coluna (_data e hora agendadas da importação ou exportação_).
- Adição de um **[!UICONTROL User]** coluna (_nome de usuário de um usuário administrador que agendou a importação/exportação_).

## Recursos desativados para preparação para HIPAA

### Serviços SaaS

Nenhum dos serviços SaaS oferecidos para o Adobe Commerce está disponível na oferta de preparação para HIPAA. Isso inclui, mas não está limitado a:

- Live Search
- API Mesh
- Construtor de aplicativos
- Serviço de catálogo

### Checkout de convidado desativado por padrão

- A verificação de visitantes apresenta um risco potencial para vários aspectos da HIPAA, incluindo registro, controle de acesso, higiene e linhagem de PHI e possivelmente mais.
- O Check-out de convidado é desativado por padrão no módulo de preparação para HIPAA, mas pode ser ativado por comerciantes por seu próprio risco.

### Recurso de informativo desativado por padrão

- O recurso de boletim informativo está desativado por padrão para impedir que o PHI seja usado em um contexto de marketing, mas pode ser ativado pelo comerciante por sua conta e risco.

### Desabilitar a configuração padrão do serviço Relatório Avançado

A configuração do serviço Relatórios avançados é desativada por padrão para impedir que o PHI seja usado para análise e relatórios, mas pode ser ativada pelo comerciante por sua conta e risco.

### Serviço Sendgrid desativado por padrão

O serviço Sendgrid está desabilitado por padrão porque o aplicativo não é compatível com HIPAA. Os comerciantes podem enviar uma solicitação de suporte para ativar o Sendgrid, mas devem reconhecer que assumirão o risco de usar o serviço.
