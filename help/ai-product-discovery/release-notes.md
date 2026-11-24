---
title: Notas de versão da Descoberta de produto de IA
description: Revise as notas de versão da Descoberta de produto de IA para recursos de enriquecimento de catálogo e PDP, correções, orientação de atualização, versões do Commerce compatíveis e problemas conhecidos.
feature: Release Notes
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%
---
# Notas de versão da Descoberta de produto de IA

Essas notas de versão abordam atualizações no enriquecimento de catálogo e enriquecimento de PDP, incluindo novos recursos, correções, requisitos de atualização e problemas conhecidos. Cada entrada de versão identifica a extensão ou o fluxo de trabalho afetado.

![Novos](../assets/new.svg) Novos recursos
![Correção de um problema](../assets/fix.svg) Correções e melhorias
![Problema conhecido](../assets/bug.svg) Problemas conhecidos

## Versão 2.1.3 {#release-2-1-3}

*30 de novembro de 2026*

[!BADGE Suportado]{type=Informative tooltip="Compatível"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 e 2.4.7 no PHP 8.3 a 8.5. [!DNL Adobe Commerce as a Cloud Service]

A versão 2.1.3 combina o enriquecimento da página de detalhes do produto com o enriquecimento do catálogo em um novo item de menu de Administrador chamado **Descoberta de Produto de IA**. Além disso, o suporte se estende a [!DNL Adobe Commerce as a Cloud Service].

## Versão 2.1.2 {#release-2-1-2}

*22 de outubro de 2026*

[!BADGE Suportado]{type=Informative tooltip="Compatível"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 e 2.4.7 no PHP 8.3 a 8.5.

A versão 2.1.2 torna o enriquecimento do catálogo uma extensão independente. Agora ele inclui tudo o que foi fornecido anteriormente pela extensão [!DNL Adobe Brand Visibility] separada (`magento/llm-optimizer`): aplicar sugestões aprovadas ao catálogo, revertê-las e proteger suas próprias edições contra substituição.

### Atualizar de versões anteriores {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>A versão 2.1.2 não pode ser instalada junto com a extensão [!DNL Adobe Brand Visibility]. Se ele estiver instalado, remova-o como parte da atualização.

1. Remova a extensão [!DNL Adobe Brand Visibility], se ela estiver instalada:

   ```bash
   composer remove magento/llm-optimizer
   ```

   Se a extensão tiver sido instalada copiando ou vinculando `Magento/LlmoCatalog` em `app/code`, exclua esse diretório. Não apenas desabilite o módulo: um módulo desabilitado que ainda esteja no disco pode fazer com que `setup:upgrade` descarte a tabela que armazena os valores originais dos produtos enriquecidos.

1. Atualize o enriquecimento do catálogo e aplique as alterações:

   ```bash
   composer require magento/module-catalog-enrichment:^2.1
   bin/magento setup:upgrade
   bin/magento cache:flush
   ```

   Liberar o cache após a atualização. A atualização move as concessões de acesso existentes para novos recursos de permissão, e essas concessões não entrarão em vigor até que o cache seja limpo.

### Requisitos

![Novo](../assets/new.svg) **PHP 8.3 e [!DNL Adobe Commerce] 2.4.7 ou posterior**—o PHP 8.1 está no fim da vida útil e o PHP 8.2 chega ao fim em 31 de dezembro de 2026, então não há suporte para nenhum dos dois. Não há suporte para [!DNL Adobe Commerce] 2.4.6 e versões anteriores.

### Novos recursos

![Novo](../assets/new.svg) **[!UICONTROL AI Product Discovery]menu**—As páginas de enriquecimento do catálogo agora têm sua própria seção na barra lateral do Administrador. Vá para **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**. Anteriormente, a página estava em **[!UICONTROL Catalog]**.

![Nova](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="Ainda não disponível no geral"} **[!UICONTROL Product Details Page Enrichment (Beta)]** — Uma nova página em **[!UICONTROL AI Product Discovery]** para analisar sugestões de enriquecimento para páginas de detalhes do produto. O enriquecimento da página de detalhes do produto está na versão beta e ainda não está disponível no geral.

![Novo](../assets/new.svg) **Aplicar e reverter sugestões aprovadas**—Atualizações de nome e descrição aprovadas são gravadas no catálogo por esta extensão. O Commerce registra o valor original de cada atributo enriquecido na primeira vez em que é alterado, de modo que uma reversão sempre restaura o valor que você tinha antes do enriquecimento, mesmo depois de várias sugestões terem sido aplicadas ao mesmo atributo.

![Novo](../assets/new.svg) **Suas edições são respeitadas**—Quando você altera um nome ou descrição enriquecida no formulário de produto do Administrador, com **[!UICONTROL Update Attributes]**, ou através de uma importação, seu valor é mantido e a sugestão relacionada é marcada como *Desatualizada*. Uma alteração feita no escopo padrão afeta apenas as exibições de armazenamento que herdam o valor.

![Novo](../assets/new.svg) **Acesso somente leitura ao catálogo para sugestões**—[!DNL Commerce Catalog Agent] pode ler dados de produto, categoria, conjunto de atributos e tipo de produto para selecionar produtos para análise. A leitura retorna somente atributos marcados como **[!UICONTROL Used in Product Listing]**, mais os atributos que podem ser enriquecidos. Ele não pode alterar os dados do catálogo.

### Correções e aprimoramentos

![Correção de um problema](../assets/fix.svg) **Nova tentativa de aplicação de relatórios bem-sucedida**—Se uma solicitação de aplicação for repetida depois de já ter sido concluída, a nova tentativa agora relata as alterações como aplicadas, em vez de não relatar nenhuma alteração. Nada se escreve duas vezes.

![Problema corrigido](../assets/fix.svg) **Somente serviços aprovados podem alterar o catálogo**—Aplicar e reverter aceitam somente solicitações de [!DNL Commerce Catalog Agent]. Anteriormente, qualquer token IMS válido do Adobe era aceito. A mesma verificação agora também se aplica às solicitações do SOAP.

![Correção de um problema](../assets/fix.svg) **Erros de limpeza**—Uma interrupção do Adobe IMS agora retorna `401` em vez de `500`. Portanto, a solicitação não será repetida no catálogo e um ambiente do Adobe IMS não reconhecido será rejeitado em vez de ser tratado como preparo.

![Problema corrigido](../assets/fix.svg) **Ambiente do Adobe IMS**—O enriquecimento de catálogo agora entra no ambiente do Adobe IMS de produção por padrão, inclusive em instâncias conectadas a um espaço de dados [!DNL Commerce Services] de não produção. Anteriormente, essas instâncias eram enviadas para o ambiente de preparo.

![Problema corrigido](../assets/fix.svg) **Entrar após a [!DNL Adobe Brand Visibility] alteração de domínio**—A página de enriquecimento do catálogo agora carrega de `abv.adobe.com`, que corrige um loop de entrada após o domínio anterior começar a redirecionar.

### Problemas conhecidos

![Problema conhecido](../assets/bug.svg) **Funções com [!UICONTROL Catalog] acesso completo** — Uma função de usuário salva antes desta versão com todos os **[!UICONTROL Catalog]** concedidos mantém acesso ao recurso **[!UICONTROL Catalog Enrichment Service API]**. Revise essas funções em **[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]** e limpe esse recurso onde ele não é necessário.

## Versão 1.0.2 {#release-1-0-2}

Versão inicial da página de administração de enriquecimento do catálogo. Exige que a extensão [!DNL Adobe Brand Visibility] aplique sugestões ao catálogo.
