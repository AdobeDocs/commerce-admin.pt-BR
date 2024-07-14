---
title: Atualizar taxas de câmbio
description: Saiba como definir taxas de moeda manualmente ou importá-las para sua loja.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Atualizar taxas de câmbio

As taxas de moeda podem ser definidas manualmente ou importadas para o armazenamento. Para garantir que sua loja tenha as taxas mais atuais, você pode configurar as taxas de moeda para serem atualizadas automaticamente de acordo com o agendamento.

Antes de importar taxas de câmbio, conclua a [configuração de taxa de câmbio](currency-configuration.md) para especificar as moedas que você aceita e estabelecer a conexão e o agendamento de importação.

![Taxas de câmbio](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Atualizar uma taxa de câmbio manualmente

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Clique na taxa que você deseja alterar e insira o novo valor para cada moeda compatível.

1. Quando terminar, clique em **[!UICONTROL Save Currency Rates]**.

## Importar taxas de moeda

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Defina **[!UICONTROL Import Service]** para o provedor de taxa de moeda.

   O provedor padrão é `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >A partir da versão 2.4.6, o serviço [[!DNL Fixer.io]](https://fixer.io/) será substituído pelo serviço [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). É altamente recomendável usar uma conta APILayer em vez de uma conta [!DNL Fixer.io] obsoleta.

1. Clique em **[!UICONTROL Import]**.

   As taxas atualizadas aparecem na lista _[!UICONTROL Currency Rates]_. Se as taxas foram alteradas desde a última atualização, a taxa antiga aparece abaixo para referência.

1. Quando terminar, clique em **[!UICONTROL Save Currency Rates]**.

1. Quando solicitado a atualizar o cache, clique no link **[!UICONTROL Cache Management]** e atualize o cache inválido.

   ![Mensagem do sistema - atualizar o cache inválido](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Importar taxas de moeda de acordo com a programação

1. Verifique se o [Cron](../systems/cron.md) está habilitado para o seu armazenamento.

1. Para especificar as moedas que você aceita e estabelecer a conexão e o agendamento de importação, conclua a [Configuração de Taxa de Moeda](currency-configuration.md).

1. Para verificar se as taxas foram importadas de acordo com o cronograma, verifique a lista _[!UICONTROL Currency Rates]_.

1. Aguarde o período de tempo da configuração de frequência estabelecida para o agendamento e verifique as taxas novamente.
