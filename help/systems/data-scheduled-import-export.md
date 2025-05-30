---
title: Importação e exportação programadas
description: Saiba como gerenciar operações programadas de importação e exportação de dados.
exl-id: 74ba40f1-a540-4425-9500-2c730c1145e7
feature: Products, Customers, Data Import/Export
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '2429'
ht-degree: 0%

---

# Importação e exportação programadas

{{ee-feature}}

Importações e exportações programadas podem ser executadas diariamente, semanalmente ou mensalmente. Os arquivos a serem importados ou exportados podem residir em servidores Adobe Commerce locais ou em servidores FTP remotos. A Importação/Exportação programada é implementada por padrão e não requer configuração adicional. Todas as importações e exportações programadas são gerenciadas pelo cron job scheduler.

## Acessar importação/exportação programada

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Imports/Exports]**.

   ![Importação/exportação de dados agendada](./assets/data-scheduled-import-export.png){width="700" zoomable="yes"}

1. Para criar um novo trabalho agendado de importação ou exportação, clique no botão apropriado e siga as instruções para o tipo de trabalho agendado.

   - [Adicionar exportação programada](#schedule-an-export)
   - [Adicionar importação agendada](#schedule-an-import)

1. Quando o registro é salvo, o trabalho aparece na grade _[!UICONTROL Scheduled Import/Export]_.

   >[!NOTE]
   >
   >Ao criar ou atualizar uma importação/exportação programada, isso resulta em uma alteração na configuração do sistema. Depois de salvar, certifique-se de endereçar o aviso de invalidação de cache exibido na parte superior da página de Administração e liberar o cache para aplicar a programação nova ou atualizada.

1. [!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} Após cada trabalho agendado, uma cópia do arquivo é colocada no diretório `var/log/import_export` no servidor local do Adobe Commerce.

   Os detalhes de cada operação não são gravados no log. Se ocorrer um erro, será enviada uma notificação do trabalho de importação/exportação que falhou, com uma descrição do erro.

## Agendar uma importação

Para o formato de arquivo de importação disponível e os tipos de entidades de importação, o processo de importação programado é semelhante ao processo de importação manual:

- O arquivo de importação deve estar no formato .CSV
- Você pode importar dados de produtos e clientes

A vantagem de usar a importação agendada é que você pode importar automaticamente um arquivo de dados várias vezes depois de especificar os parâmetros de importação e agendar apenas uma vez.

Os detalhes de cada operação de importação não são gravados em um log, mas quando há uma falha, você recebe um email de _Falha na importação_ com uma descrição do erro. O resultado do último trabalho de importação programado é mostrado na coluna Último resultado na página Importação/Exportação programada.

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} Após cada operação de importação, uma cópia do arquivo de importação é colocada no diretório `var/log/import_export` no servidor onde o Adobe Commerce ou o Magento Open Source está implantado. O carimbo de data e hora, o marcador da entidade importada (produtos ou clientes) e o tipo da operação (nesse caso, importação) são adicionados ao nome do arquivo de importação.

Após cada trabalho de importação programado, uma operação de reindexação é executada automaticamente. No front-end, as alterações nas descrições e outras informações de texto são refletidas depois que os dados atualizados são inseridos no banco de dados, e as alterações nos preços são refletidas somente após a operação de reindexação.

### Etapa 1: concluir as configurações de importação

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. No canto superior direito, clique em **[!UICONTROL Add Scheduled Import]**.

1. Defina as opções de agendamento e importação:

   - **[!UICONTROL Name]** — Digite um nome para a importação agendada.

   - **[!UICONTROL Description]** — Insira uma breve descrição que explique a finalidade da importação e como ela deve ser usada.

   - **[!UICONTROL Entity Type]** — Defina como um dos seguintes:

      - `Products`
      - `Advanced Pricing`
      - `Customers and Addresses (single file)`
      - `Customer Addresses`
      - `Customer Finances`
      - `Customers Main File`
      - `Stock Sources`

   - **[!UICONTROL Import Behavior]** — Defina como um dos seguintes:

      - `Add/Update Complex Data` — Adiciona ou atualiza novos dados complexos aos dados complexos existentes para entradas existentes no banco de dados. Este é o valor padrão.
      - `Replace` — Substitui entidades complexas existentes no banco de dados.
      - `Delete Entities` — Exclui entradas existentes no banco de dados.
      - `Custom Action` - Personaliza entidades existentes no banco de dados.

     >[!NOTE]
     >
     >Para os tipos de entidade _[!UICONTROL Advanced Pricing]_,_[!UICONTROL Products]_, _[!UICONTROL Customers and Addresses (single file)]_&#x200B;e_[!UICONTROL Stock Sources]_, esses comportamentos de importação são exibidos: `Add/Update`, `Replace` e `Delete`. Para os tipos de entidade _Finanças do Cliente_, _Arquivo Principal do Cliente_ e _Clientes e Endereços_, esses comportamentos de importação são exibidos: `Add/Update Complex Data`, `Delete Entities` e `Custom Action`.

   - **[!UICONTROL Start Time]** — Defina como a hora, os minutos e os segundos em que a importação está agendada para começar.

   - **[!UICONTROL Frequency]** — Defina como um dos seguintes: `Daily`, `Weekly` ou `Monthly`

   - **[!UICONTROL On Error]** - Defina como um dos seguintes: `Stop Import` ou `Continue Processing`

   - **[!UICONTROL Status]** — Para ativar a importação agendada, defina como `Enabled`.

   - **[!UICONTROL Field Separator]** — Insira o caractere usado para separar campos no arquivo de importação. O caractere padrão é uma vírgula.

   - **[!UICONTROL Multiple Value Separator]** — Insira o caractere usado para separar vários valores em um campo.

   ![Importação de dados - configurações de importação agendadas](./assets/data-transfer-scheduled-import-settings.png){width="600" zoomable="yes"}

### Etapa 2: completar as informações do arquivo de importação

1. Defina **[!UICONTROL Server Type]** como um dos seguintes:

   - `Local Server` - Importa os dados do mesmo servidor em que o Adobe Commerce está instalado.
   - `Remote FTP` - Importa os dados de um servidor remoto.

   ![Importação de dados - informações do arquivo de importação agendado](./assets/data-transfer-scheduled-import-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Quando o módulo de armazenamento remoto está habilitado, o `Local Server` muda automaticamente para `Remote Storage`.

1. Insira o **[!UICONTROL File Directory]** de onde o arquivo de importação se origina.

   - `Local Server` - Insira um caminho relativo na instalação do Commerce. Por exemplo, `var/import`. Se o módulo de Armazenamento remoto estiver configurado, use `import_export/import`.
   - `Remote FTP server` - Digite a URL e o caminho completos para a pasta de importação no servidor remoto.

1. Insira o **[!UICONTROL File Name]** a ser importado.

1. Para **[!UICONTROL Images File Directory]**, insira o caminho para o diretório onde as imagens do produto são armazenadas.

   Em um servidor local, insira um caminho relativo como: `var/import`. Em um armazenamento remoto, insira um caminho relativo como: `import_export/import` ou `import_export/import/some/dir`.

### Etapa 3: configurar os emails de importação com falha

![Importação de dados - falha ao importar emails](./assets/data-transfer-scheduled-import-email-fail.png){width="600" zoomable="yes"}

1. Defina **[!UICONTROL Failed Email Receiver]** para o contato de armazenamento que receberá a notificação se ocorrer um erro durante a importação.

1. Defina **[!UICONTROL Failed Email Sender]** para o contato de armazenamento que aparece como remetente da notificação.

1. Defina **[!UICONTROL Failed Email Template]** para o modelo usado para a notificação.

1. Para **[!UICONTROL Send Failed Email Copy To]**, insira o endereço de email de qualquer pessoa que deverá receber uma cópia da notificação.

   Separe vários endereços de email com vírgula.

1. Defina **[!UICONTROL Failed Email Copy Method]** como um dos seguintes:

   - `Bcc` - Envia uma cópia de cortesia oculta da notificação de importação com falha. O nome e o endereço do recipient estão incluídos na distribuição de email original, mas ocultos da visualização.
   - `Separate Email` - Envia uma cópia da notificação de importação com falha como um email separado.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   O novo trabalho de importação agendado é adicionado à lista na página _[!UICONTROL Scheduled Import/Export]_. Nessa página, ele pode ser executado imediatamente para teste e edição. O arquivo de importação é validado antes da execução de cada trabalho de importação.

>[!NOTE]
>
>Ao criar ou atualizar uma importação/exportação programada, isso resulta em uma alteração na configuração do sistema. Depois de salvar, certifique-se de endereçar o aviso de invalidação de cache exibido na parte superior da página de Administração e liberar o cache para aplicar a programação nova ou atualizada.

### Descrições dos campos

#### [!UICONTROL Import Settings]

| Campo | Descrição |
| ----- | ----------- | 
| [!UICONTROL Name] | O nome da importação. Ajuda a diferenciá-lo se muitas importações programadas diferentes forem criadas. |
| [!UICONTROL Description] | (Opcional) Você pode inserir uma descrição. |
| [!UICONTROL Entity Type] | Define os dados a serem importados. |
| [!UICONTROL Import Behavior] | Define como os dados complexos são tratados se as entidades que estão sendo importadas existirem no banco de dados. Dados complexos para produtos incluem categorias, sites, opções personalizadas, preços de níveis, produtos relacionados, vendas adicionais, vendas cruzadas e dados de produtos associados. Dados complexos para clientes incluem endereços. Opções:<br>**[!UICONTROL Add/Update Complex Data]**- Os novos dados complexos são adicionados ou atualizados para os dados complexos existentes de entradas existentes no banco de dados. Este é o valor padrão.<br>**[!UICONTROL Add/Update]** - Novos dados são adicionados às entradas existentes no banco de dados. Todos os campos, exceto `sku`, podem ser atualizados para produtos. Quaisquer vários valores de campo que não estejam listados no arquivo CSV, como categorias ou sites, permanecem no banco de dados após a importação.<br>**[!UICONTROL Replace]**- Os dados complexos existentes para as entidades existentes são substituídos.<br>**[!UICONTROL Delete Entities]** - Se existirem entidades importadas no banco de dados, elas serão excluídas do banco de dados.<br>**[!UICONTROL Custom Action]**- As entidades complexas existentes são personalizadas durante o processo de importação. |
| [!UICONTROL Start Time] | Defina a hora de início, os minutos e os segundos da importação. |
| [!UICONTROL Frequency] | Defina com que frequência a importação é executada. Opções: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL On Error] | Defina o comportamento do sistema caso sejam encontrados erros durante a validação do arquivo. Opções:<br>**Parar Importação** — O arquivo não será importado se algum erro for encontrado durante a validação. Este é o valor padrão.<br>**Continuar Processando** - Caso sejam encontrados erros durante a validação, mas a importação for possível, o arquivo será importado. |
| [!UICONTROL Status] | A importação é ativada por padrão. Você pode suspendê-lo definindo o Status como `Disabled`. |
| [!UICONTROL Field Separator] | Determina o caractere usado para separar campos. Valor padrão: `,` (vírgula) |
| [!UICONTROL Multiple Value Separator] | Determina o caractere usado para separar vários valores dentro de um campo. Valor padrão: `,` (vírgula) |

{style="table-layout:auto"}

#### [!UICONTROL Import File Information]

| Campo | Descrição |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Você pode importar de um arquivo no mesmo servidor em que o Commerce está implantado (selecione `Local Server`) ou do servidor FTP remoto (selecione `Remote FTP`). Se você selecionar _[!UICONTROL Remote FTP]_, serão exibidas opções adicionais para credenciais e configurações de transferência de arquivos. Se o módulo de armazenamento remoto estiver habilitado, o tipo `Local Server` será alternado automaticamente para `Remote Storage`. |
| [!UICONTROL File Directory] | Especifique o diretório onde o arquivo de importação está localizado. Se o Tipo de Servidor estiver definido como _[!UICONTROL Local Server]_, especifique o caminho relativo para o diretório de instalação do Commerce. Por exemplo: `var/import` ou `import_export/import` para armazenamento remoto. |
| [!UICONTROL File Name] | Especifique o nome do arquivo de importação. |
| [!UICONTROL Images File Directory] | Insira o caminho para o diretório onde as imagens do produto são armazenadas. Para um servidor local, insira um caminho relativo. Por exemplo: `var/import` ou `import_export/import` para armazenamento remoto. |

{style="table-layout:auto"}

#### [!UICONTROL Import Failed Emails]

| Campo | Descrição |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Especifique o endereço de email para o qual uma notificação por email (email de importação com falha) será enviada se a importação falhar. |
| [!UICONTROL Failed Email Sender] | Especifique o endereço de email usado como remetente do email de falha na importação. |
| [!UICONTROL Failed Email Template] | Selecione um modelo para o email de falha na importação. Por padrão, somente a opção Falha ao importar (Modelo padrão da localidade) está disponível. Modelos personalizados podem ser criados em _[!UICONTROL System]_>_[!UICONTROL Transactional Emails]_. |
| [!UICONTROL Send Failed Email Copy To] | O endereço de email para o qual uma cópia do email de falha de importação é enviada. |
| [!UICONTROL Send Failed Email Copy Method] | Selecione o método de envio de cópia para o email de falha na importação. |

{style="table-layout:auto"}

## Agendar uma exportação

A Exportação Agendada é semelhante a uma [Exportação](data-export.md) manual no formato de arquivo de exportação disponível e nos tipos de entidades que podem ser exportadas:

- É possível exportar para o formato CSV
- É possível exportar dados do produto e do cliente

A vantagem de usar a Exportação agendada é que você pode exportar dados várias vezes automaticamente, depois de especificar os parâmetros de exportação, e agendar apenas uma vez.

Os detalhes de cada exportação não são gravados em um log, mas, se houver falha, você receberá um email Export Failed, que contém a descrição do erro. O resultado do último trabalho de exportação é exibido na coluna Último resultado na página Importação/Exportação programada.

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."} Após cada exportação, o arquivo de exportação é colocado no local definido pelo usuário e uma cópia no diretório `var/log/import_export` no servidor onde o Adobe Commerce ou o Magento Open Source está implantado. O carimbo de data e hora e o marcador da entidade exportada (produtos ou clientes) e o tipo da operação (nesse caso, exportação) são adicionados ao nome do arquivo de exportação.

### Etapa 1: concluir as configurações de exportação

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. No canto superior direito, clique em **[!UICONTROL Add Scheduled Export]** e faça o seguinte:

   - Insira um **[!UICONTROL Name]** para a exportação agendada.

   - Insira um breve **[!UICONTROL Description]** que explique a finalidade da exportação e como ela deve ser usada.

   - Defina **[!UICONTROL Entity Type]** como um dos seguintes:

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

     A seção _[!UICONTROL Entity Attributes]_&#x200B;na parte inferior da página é atualizada para refletir o Tipo de Entidade selecionado.

   - Defina **[!UICONTROL Start Time]** como a hora, os minutos e os segundos em que a exportação está agendada para começar.

   - Defina **[!UICONTROL Frequency]** como um dos seguintes:

      - `Daily`
      - `Weekly`
      - `Monthly`

1. Para ativar a exportação agendada, defina **[!UICONTROL Status]** como `Enabled`.

1. Aceitar `CSV` como o **[!UICONTROL File Format]** padrão.

   ![Configurações de exportação agendadas](./assets/data-transfer-scheduled-export-settings.png){width="600" zoomable="yes"}

### Etapa 2: completar as informações do arquivo de exportação

1. Defina **[!UICONTROL Server Type]** como um dos seguintes:

   - `Local Server` - Para salvar o arquivo de exportação no mesmo servidor em que o Commerce está instalado.
   - `Remote FTP` — Para salvar o arquivo de exportação em um servidor remoto.

   ![Informações do arquivo de exportação agendado](./assets/data-transfer-scheduled-export-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Quando o módulo de armazenamento remoto está habilitado, o `Local Server` muda automaticamente para `Remote Storage`.

1. Para **[!UICONTROL File Directory]**, insira o diretório onde o arquivo de exportação deve ser salvo da seguinte maneira:

   - Para **[!UICONTROL Local Server]**, insira um caminho relativo na instalação do Commerce, como `var/export`. Se o módulo de armazenamento remoto estiver configurado, use `import_export/export`.
   - Para **[!UICONTROL Remote FTP server]**, insira a URL e o caminho completos para a pasta de destino no servidor de destino.

1. Se o servidor _[!UICONTROL Remote FTP]_&#x200B;estiver selecionado, insira as credenciais de conexão para o servidor e selecione as configurações adicionais:

   - Para **[!UICONTROL FTP Host[:Port]]**, insira o endereço do host FTP remoto.
   - Para **[!UICONTROL User Name]**, digite o nome de usuário usado para acessar o servidor remoto.
   - Para **[!UICONTROL Password]**, digite a senha da conta de nome de usuário fornecida.
   - Para **[!UICONTROL File Mode]**, escolha `Binary` ou `ASCII`.
   - Para **[!UICONTROL Passive Mode]**, escolha `No` ou `Yes`.

### Etapa 3: configurar os emails de falha de exportação

1. Defina **[!UICONTROL Failed Email Receiver]** para o contato de armazenamento que receberá a notificação se ocorrer um erro durante a exportação.

1. Defina **[!UICONTROL Failed Email Sender]** para o contato de armazenamento que aparece como remetente da notificação.

1. Defina **[!UICONTROL Failed Email Template]** para o modelo usado para a notificação.

1. Para **[!UICONTROL Send Failed Email Copy To]**, insira o endereço de email de qualquer pessoa que deverá receber uma cópia da notificação.

   Para vários endereços de email, separe com vírgula.

1. Defina **[!UICONTROL Failed Email Copy Method]** como um dos seguintes:

   - `Bcc` - Envia uma cópia de cortesia oculta. O nome e o endereço do recipient estão incluídos na distribuição de email original, mas estão ocultos na visualização.
   - `Separate Email` — Envia a cópia como um email separado.

### Etapa 4: Escolher os atributos de entidade

1. Na seção _[!UICONTROL Entity Attributes]_, escolha os atributos que deseja incluir nos dados de exportação.

   - Para filtrar os dados exportados por valor de atributos, insira o valor de atributo na coluna _[!UICONTROL Filter]_.
   - Para excluir produtos ou clientes com determinados valores de atributo, insira os valores dos atributos que deseja excluir e marque a caixa de seleção na coluna Ignorar.

1. Quando terminar, clique em **[!UICONTROL Save]**.

   O novo trabalho de exportação agendado é adicionado à lista na página _[!UICONTROL Scheduled Import/Export]_. Nessa página, ela pode ser executada imediatamente, para teste e editada.

>[!NOTE]
>
>Ao criar ou atualizar uma importação/exportação programada, isso resulta em uma alteração na configuração do sistema. Depois de salvar, certifique-se de endereçar o aviso de invalidação de cache exibido na parte superior da página de Administração e liberar o cache para aplicar a programação nova ou atualizada.

### Descrições dos campos

#### [!UICONTROL Export Settings]

| Campo | Descrição |
| ----- | ----------- | 
| [!UICONTROL Name] | O nome da exportação. Ajuda a diferenciá-lo se muitas exportações programadas diferentes forem criadas. |
| [!UICONTROL Description] | (Opcional) Uma descrição da exportação programada. |
| [!UICONTROL Entity Type] | Identifica os dados a serem exportados. Depois que a seleção é feita, os Atributos da entidade aparecem abaixo. Opções: `Advanced Pricing` / `Products` / `Customer Finances` / `Customers Main File` / `Customer Addresses` / `Stock Sources` |
| [!UICONTROL Start Time] | Defina a hora de início, os minutos e os segundos da exportação. |
| [!UICONTROL Frequency] | Defina com que frequência o trabalho de exportação é executado. Opções: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Status] | Uma nova exportação agendada é ativada por padrão. Você pode suspendê-la definindo o Status como Desativado. Opções: `Enabled` / `Disabled` |
| [!UICONTROL File Format] | Selecione o formato do arquivo de exportação. Atualmente, apenas a opção `.CSV` está disponível. |

{style="table-layout:auto"}

#### [!UICONTROL Export Settings Information]

| Campo | Descrição |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Determina o local do arquivo de exportação. Opções:<br>**Servidor Local** — Coloca o arquivo de exportação no mesmo servidor em que o Commerce está implantado. Se o módulo de armazenamento remoto estiver habilitado, `Local Server` será alternado para `Remote Storage`.<br>**FTP remoto** — Coloca o arquivo de exportação em um servidor remoto. Opções adicionais para credenciais e configurações de transferência de arquivos são exibidas. |
| [!UICONTROL File Directory] | Especifique o diretório onde o arquivo de exportação é colocado. Caso _[!UICONTROL Server Type]_&#x200B;esteja definido como `Local Server`, especifique o caminho relativo ao caminho de instalação do Commerce. Por exemplo, `var/export` ou `import_export/export` para armazenamento remoto. |

{style="table-layout:auto"}

#### [!UICONTROL Export Failed Emails]

| Campo | Descrição |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Especifique o endereço de email para o qual uma notificação por email (email de falha na exportação) será enviada se a exportação falhar. |
| [!UICONTROL Failed Email Sender] | Especifique o endereço de email usado como remetente de email com falha na exportação. |
| [!UICONTROL Failed Email Template] | Selecione um modelo para o email de exportação com falha. Por padrão, somente a opção `Export Failed (Default Template from Locale)` está disponível. |
| [!UICONTROL Send Failed Email Copy To] | O endereço de email para o qual uma cópia do email de exportação com falha é enviada. |
| [!UICONTROL Send Failed Email Copy Method] | Especifique o método de envio de cópia para o email de falha na exportação. |

{style="table-layout:auto"}
