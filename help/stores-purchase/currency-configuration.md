---
title: Configuração de moeda
description: Saiba mais sobre como definir o escopo da moeda base e como especificar as moedas que você aceita e a moeda que deseja usar para exibição de preço.
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Configuração de moeda

Antes de configurar taxas de moeda individuais, você deve primeiro definir o escopo da [moeda de base](../configuration-reference/general/currency-setup.md). Ela é definida como global por padrão, o que aplica a configuração da moeda base a todo o [hierarquia de loja](../getting-started/websites-stores-views.md). Se você tiver uma instalação de Adobe Commerce ou Magento Open Source multissite, poderá gerenciar várias moedas base definindo o escopo para o nível do site.

Também é possível especificar as moedas que você aceita e qual moeda deseja usar para a exibição de [preços](../catalog/catalog-price-scope.md) na sua loja. No diagrama a seguir, o escopo da moeda base é definido no nível do site, para que cada site possa ter uma moeda base diferente.

![Diagrama do escopo de moeda](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## Fase 1: Escolher as moedas aceitas

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No canto superior esquerdo, defina **[!UICONTROL Scope]** à exibição de loja onde a configuração se aplica.

1. No painel esquerdo, em _Geral_, escolha **[!UICONTROL Currency Setup]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Currency Options]** e defina as seguintes opções:

   - **[!UICONTROL Base Currency]** — Defina para a moeda principal que você usa para transações on-line.

   - **[!UICONTROL Default Display Currency]** — Defina para a moeda que você usa para exibir preços na exibição de armazenamento.

   - **[!UICONTROL Allowed Currencies]** — Selecione todas as moedas que você aceita como pagamento na visualização de loja. Selecione também a moeda principal.

     Para várias moedas, mantenha pressionada a tecla Ctrl (PC) ou Command (Mac) e clique em cada opção.

   ![Configuração geral - opções de moeda](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   Para obter uma descrição detalhada de cada uma dessas configurações, consulte [Opções de moeda](../configuration-reference/general/currency-setup.md) no _Guia de referência de configuração_.

1. Quando for solicitado atualizar o cache, clique em _Fechar_ ( ![Fechar caixa](../assets/icon-close-x.png) ) no canto superior direito da mensagem do sistema.

   Você pode [atualizar o cache](../systems/cache-management.md) posteriormente.

1. Defina o escopo da moeda base:

   - No painel esquerdo, expanda **[!UICONTROL Catalog]** e escolha **[!UICONTROL Catalog]** por baixo.

   - Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Price]** seção. (Esta seção só aparecerá se o escopo estiver definido como **[!UICONTROL Store View:]** _Configuração padrão_.)

   - Definir **[!UICONTROL Catalog Price Scope]** para `Global` ou `Website`.

   ![Configuração do catálogo - opções de preço](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## Etapa 2: configurar a conexão de importação

1. Role até a parte superior da página.

1. No painel esquerdo, expanda **[!UICONTROL General]** e escolha **[!UICONTROL Currency Setup]**.

1. Configure sua conexão com o serviço de moeda:

   Há três opções de serviço: _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_, e _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >A partir da versão 2.4.6, a variável [[!DNL Fixer.io]](https://fixer.io/) serviço está obsoleto e foi substituído pelo [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) serviço. É altamente recomendável usar uma conta APILayer em vez de uma conta obsoleta [!DNL Fixer.io] conta.

   - _Para se conectar à [serviço fixer.io](https://fixer.io/):_

      - Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Fixer.io]** seção.

      - Entre no fixer.io **[!UICONTROL API key]**.

      - Para **[!UICONTROL Connection Timeout in Seconds]**, insira o número de segundos de inatividade permitidos antes que a conexão expire.

     ![Configuração geral - configuração de moeda - Opções de Fixer.io](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _Para se conectar à [[!DNL Fixer Api (APILayer)] serviço](https://apilayer.com/):_

      - Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Fixer Api (APILayer)]** seção.

      - Insira seu [!DNL APILayer] **[!UICONTROL API key]**.

      - Para **[!UICONTROL Connection Timeout in Seconds]**, insira o número de segundos de inatividade permitidos antes que a conexão expire.

     ![Configuração geral - configuração de moeda - Opções da API de correção (APILayer)](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _Para se conectar à [[!DNL Currency Convertor API] serviço](https://free.currencyconverterapi.com/):_

      - Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Currency Convertor API]** seção.

      - Insira seu conversor de moeda **[!UICONTROL API key]**.

      - Para **[!UICONTROL Connection Timeout in Seconds]**, insira o número de segundos de inatividade permitidos antes que a conexão expire.

     ![Configuração geral - configuração de moeda - Opções da API do Conversor de moeda](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## Etapa 3: definir as configurações de importação programadas

1. Continuando com a Configuração de Moeda, expanda ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Scheduled Import Settings]** seção.

   ![Configuração geral - configurações de importação agendadas para a moeda](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. Para atualizar automaticamente as taxas de moeda, defina **[!UICONTROL Enabled]** para `Yes`.

1. Defina as opções de atualização:

   - **[!UICONTROL Service]** — Defina para o provedor de taxa. O valor padrão é `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** — Defina para a hora, os minutos e o segundo que as taxas serão atualizadas de acordo com o agendamento.

   - **[!UICONTROL Frequency]** — Para determinar com que frequência as taxas são atualizadas, defina como um dos seguintes:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]** — Digite o endereço de e-mail da pessoa que receberá a notificação por e-mail se ocorrer um erro durante o processo de importação.

     Para inserir vários endereços de email, separe cada um com vírgula.

   - **[!UICONTROL Error Email Sender]** — Defina como [armazenar contato](../getting-started/store-details.md#store-email-addresses) que aparece como o remetente da notificação de erro.

   - **[!UICONTROL Error Email Template]** — Defina para o template de email usado para a notificação de erro.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Quando for solicitado que você atualize o cache, clique na guia **[!UICONTROL Cache Management]** vincular e atualizar o cache inválido.

   ![Mensagem do sistema - atualizar o cache inválido](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## Etapa 4: Atualizar as taxas de câmbio

As taxas de câmbio devem ser atualizadas com os valores atuais antes de entrarem em vigor. [Atualizar as taxas](currency-update.md) manualmente ou para importar as taxas automaticamente.

## Etapa 5: Personalizar símbolos de moeda (opcional)

O Gerenciamento de Símbolos de Moeda oferece a capacidade de personalizar o símbolo associado a cada moeda que é aceita como pagamento em sua loja.

![Símbolos de moeda](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   Cada moeda ativada para o armazenamento aparece na variável _[!UICONTROL Currency]_lista.

1. Altere as configurações na lista conforme necessário:

   - Insira um símbolo personalizado para cada moeda que deseja usar ou selecione a **[!UICONTROL Use Standard]** para cada moeda.

   - Para substituir o símbolo padrão, desmarque a caixa _[!UICONTROL Use Standard]_e insira o símbolo que deseja usar.

   >[!NOTE]
   >
   >Não é possível alterar o alinhamento do símbolo de moeda da esquerda para a direita.

1. Quando terminar, clique em **[!UICONTROL Save Currency Symbols]**.

1. Quando for solicitado que você atualize o cache, clique na guia **[!UICONTROL Cache Management]** vincular e atualizar qualquer cache inválido.
