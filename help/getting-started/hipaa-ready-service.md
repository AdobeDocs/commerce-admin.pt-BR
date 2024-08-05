---
title: Preparação da HIPAA no Adobe Systems Comércio
description: Saiba como adicionar a extensão do Adobe Commerce pronta para HIPAA e obtenha recursos e funcionalidades adicionais que permitem cumprir com as suas obrigações com a HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: bce0e581e89139875e09b671038a21976eccebca
workflow-type: tm+mt
source-wordcount: '1568'
ht-degree: 1%

---

# Preparação da HIPAA no Adobe Systems Comércio

>[!IMPORTANT]
>
>**Isenção de responsabilidade legal**<br/>
>Essas informações visam ajudar os clientes a responder em Adobe Systems suas perguntas sobre os Serviços prontos para HIPAA da Adobe Systems. Não constitui aconselhamento jurídico. Os comerciantes devem consultar seus próprios advogados para entender suas obrigações sob a HIPAA e o uso e configuração apropriados dos produtos da Adobe Systems.

>[!BEGINSHADEBOX]

**Lei de Portabilidade e Responsabilidade de Seguros de Saúde (HIPAA)**

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

O Adobe Commerce deve ser implantado no Adobe Commerce na infraestrutura em nuvem ou no Adobe Commerce Managed Services com a versão 2.4.6-p3 ou posterior (sem versões beta).

## Instalação

**Pré-requisito**

>[!BEGINSHADEBOX]

- Adobe Systems provisionou sua Adobe Systems Comércio conta para acessar a extensão HIPAA Ready.
- Acesso ao [repo.magento.com](https://repo.magento.com) para instalar a extensão. Para obter os direitos necessários para a geração de chave e para obter os direitos necessários, consulte [Obter as chaves](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) de autenticação.

>[!ENDSHADEBOX]

Instale a versão mais recente da extensão`magento/hipaa-ee` HIPAA-Ready Services da Adobe Systems em um instância que está sendo executado Adobe Systems Comércio versão 2.4.6-p3 ou posterior. A extensão é entregue como um metapackage do composer na [repo.magento.com](https://repo.magento.com) repositório. O metapackage inclui a coleção de módulos que habilitam os recursos HIPAA para um Adobe Systems Comércio instância.

1. Na estação de trabalho local, altere para o diretório do projeto para o Adobe Systems Comércio em infraestrutura em nuvem projeto.

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

1. Adicione, commite e pressione o código atualizado no nuvem ambiente.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   Mover as atualizações inicia o processo](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) de [Comércio nuvem implantação para aplicar as alterações. Verifique o status do implantação no [log](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log) de implantar.

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
   <truncated for brevity>
   ```

   Todos os módulos com `Magento_Hipaa` prefixos devem estar na seção de módulos habilitados.

## Aprimoramentos de recursos para preparação HIPAA

A `magento/hipaa-ee` extensão apresenta algumas alterações e aprimoramentos na base Comércio produto. As seções a seguir fornecem detalhes sobre essas alterações e como alterar o produto base.

### Logs de ação

O registro de auditoria é um requisito da HIPAA. No Adobe Commerce, o recurso [Logs de ação](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) registra todas as alterações feitas por um usuário administrador que trabalha na sua loja. Para atender aos requisitos da HIPAA para o Log de auditoria, o recurso foi atualizado para registrar todas as ações de usuário administrador e cliente executadas por meio da interface do usuário do administrador e por meio de chamadas de API.

#### Relatório de logs de ação

A grade de relatório _Logs de Ação_ (**[!UICONTROL System]** > Logs de Ação > Relatório) foi modificada para acomodar as ações do cliente executadas por meio da interface do usuário e da API de Administração.

1. Adição de duas colunas:
   - ***Source***: mostra onde a ação foi executada.
Valores: `Admin UI` / `Customer UI` / `REST API` / `SOAP API``GraphQL API`
   - ***Tipo*** de cliente: exibe o tipo de cliente.
Valores: Cliente | Administrador | Integração

2. Renomeação do ***nome de*** usuário colunn para ***Identificador do cliente***
   - ***Identificador*** do cliente: exibe a ID de fazer logon do usuário que realizou a ação.
Valores:
      - um email se o Tipo de cliente for Cliente
      - um nome de usuário se o Tipo de cliente for Administrador
      - um nome se o Tipo de cliente for integração

3. Renomeação da coluna Nome da ação ***completa para*** Target ******
   - ******Target: Exibe o nome da ação.
Valores:
      - um terminal se Origem for uma API REST ou UMA API SOAP
      - um nome de query ou mutação se uma API GraphQL
      - um nome de ação se um administrador interface ou o Cliente interface.

#### Configurar ações de administrador para o fazendo logon

Este recurso não está disponível porque todas as ações devem ser registradas por padrão.

### recursos de Importar e exportação

Os aprimoramentos nos recursos de importação e exportação se concentram em melhorar a experiência administrativa e fornecer maior visibilidade sobre as ações do usuário.

>[!NOTE]
>
>Esses ***aprimoramentos não alteram a lógica principal de Importação e Exportação***; em vez disso, eles estendem a funcionalidade para oferecer um log mais abrangente e atribuições de dados aprimoradas. A funcionalidade fundamental de importação e exportação permanece inalterada. Os usuários podem continuar usando os recursos e fluxos de trabalho existentes sem interrupções.

#### Registro de ação administrativa

Uma das principais melhorias nos recursos de importação e exportação é o registro aprimorado de ações administrativas. Essa melhoria introduz a capacidade de aprofundar as atividades associadas à importação e à exportação de dados, contribuindo para a melhoria das rastreamento e da auditabilidade. As seguintes ações foram registradas e refletidas na grade **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**:

| Tipo | Ações |
| ---- | ------- |
| Importar | <ul><li>Um usuário administrador executa uma importação<li>Um usuário administrador baixa um arquivo importado<li>Um usuário administrador baixa um arquivo de erro<ul/> |
| Exportar | <ul><li>Solicitações de um usuário administrador<li>Um usuário administrador baixa um arquivo exportado<ul/> |
| Importações/exportações programadas | <ul><li>Um usuário administrador programa a exportação<li>Um administrador usuário edita uma exportação agendada<li>Um administrador usuário executa uma exportação agendada<li>Um administrador usuário exclui uma exportação agendada<li>Um administrador usuário agenda uma importação<li>Um administrador usuário edita uma importação agendada<li>Um usuário administrador executa uma importação agendada<li>Um usuário administrador exclui uma importação agendada<li>Um usuário administrador executa uma exclusão em massa de operações de importação/exportação<ul/> |

### Melhorias na exibição e filtragem e classificação aprimoradas

Para capacitar os usuários administradores com grades mais informativas, o serviço HIPAA-Ready oferece várias melhorias para exibir, filtrar e classificar dados.

#### Importar histórico ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Filtragem habilitada para todas as colunas, exceto para **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** e **[!UICONTROL Summary]**.

#### Exportar ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Adicionada uma coluna **[!UICONTROL ID]**.
- Adição de uma coluna **[!UICONTROL Requested At]** (_data e hora em que a exportação foi solicitada_).
- Adição de uma coluna **[!UICONTROL User]** (_nome de usuário de um administrador que fez a solicitação_).
- Remoção de uma **[!UICONTROL Action]** coluna.
- **[!UICONTROL Download]** O link foi movido para uma **[!UICONTROL File name]** coluna (_curtir à grade_ do Histórico Importar).
- Desabilitou a ação responsável pela exclusão de um arquivo exportado (_para melhorar os rastreamento_).
- Ativação da classificação para todas as colunas, exceto **[!UICONTROL File name]**.
- Ativação da filtragem para todas as colunas.

#### Importações e exportações agendadas ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Adicionada uma coluna **[!UICONTROL ID]**.
- Adição de uma coluna **[!UICONTROL Scheduled At]** (a _data e hora agendadas da importação ou exportação_).
- Adição de uma coluna **[!UICONTROL User]** (o _nome de usuário de um usuário Administrador que agendou a importação ou exportação_).

## Serviços e recursos desabilitados

Para atender aos requisitos HIPAA, alguns serviços e recursos suportados por Adobe Systems Comércio não estão disponíveis ou desabilitados por padrão. Os comerciantes têm a opção de reativar ou usar esses serviços e recursos por sua conta e risco.

### Serviços

- **Adobe Systems Comércio serviços** — Nenhum dos serviços Adobe Systems Comércio ou serviços de extensibilidade estão disponíveis sob a oferta de preparação PARA HIPAA. Esses serviços incluem, mas não se limitam a:

   - Live Search
   - API Mesh
   - App Builder

- **[Serviço](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** SendGrid — Esse serviço está desativado por padrão porque a aplicativo não é compatível com HIPAA.

### Recursos desativados por padrão

Os seguintes recursos estão desativados por padrão na módulo de preparação para HIPAA. Os comerciantes podem habilitar qualquer um desses recursos por sua conta e risco.

- **[Check-out](../stores-purchase/checkout-guest.md)** de convidado— Este recurso apresenta um risco potencial para vários aspectos da HIPAA, incluindo fazendo logon, controle de acesso, higiene e linhagem de PHI e, potencialmente, mais.

- **[Informativo recurso](../merchandising-promotions/newsletters.md)**— Esse recurso está desativado para impedir que a PHI seja usada em um contexto marketing.

- **[Avançado configuração](../getting-started/business-intelligence.md)** do serviço de relatórios: esta configuração está desativada para impedir que o PHI seja usado para análise e relatórios.
