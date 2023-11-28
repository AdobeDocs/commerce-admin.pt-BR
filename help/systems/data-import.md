---
title: Importar dados
description: Saiba mais sobre as diretrizes de importação de dados e como usar as operações de importação de dados.
exl-id: caae8811-445e-49d4-aa90-226a355732bc
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---

# Importar dados

Os dados de todos os tipos de produtos podem ser importados para a loja. Além disso, você pode importar produtos, dados de preços avançados, dados do cliente, dados de endereço do cliente e imagens do produto. A importação suporta as seguintes operações:

- Adicionar/Atualizar
- Substituir
- Excluir

## Diretrizes de importação

### Novas entidades

- As entidades são adicionadas com os valores de atributo especificados no arquivo CSV.
- Para um atributo obrigatório sem valor padrão definido, a entidade (a linha ou linhas correspondentes) não poderá ser importada se não houver um valor ou um valor inválido.
- Para um atributo obrigatório com um conjunto de valores padrão, a entidade (a linha ou linhas correspondentes) é importada e o valor padrão é definido para o atributo se não houver um valor ou um valor inválido.
- Se os dados complexos não forem válidos, a entidade (a linha ou linhas correspondentes) não poderá ser importada.

### Entidades existentes

- Para atributos que não são dados complexos, os valores do arquivo de importação, incluindo os valores vazios para os atributos não obrigatórios, substituem os valores existentes.
- Se não houver valor ou se houver um valor inválido para um atributo obrigatório, o valor existente não será substituído.
- Se os dados complexos da entidade forem inválidos, a entidade (a linha ou linhas correspondentes) não poderá ser importada, exceto se isso ocorrer quando Excluir entidades tiver sido selecionado no menu suspenso Importar comportamento.

### Dados complexos

Se existir um atributo especificado no arquivo de importação e seu valor for derivado de um conjunto definido de valores, o seguinte se aplica:

- Se o valor ainda não estiver incluído no conjunto definido de valores, a linha poderá ser importada e um valor padrão, se definido, será definido para o atributo.
- Se o valor já estiver incluído no conjunto definido, a linha correspondente não poderá ser importada.
- Se o arquivo de importação especificar um nome de atributo que ainda não está definido no sistema, ele não será criado e seus valores não serão importados.

### Arquivos inválidos

- Um arquivo não pode ser importado se todas as linhas forem inválidas.
- Um nome de dados complexo ou de serviço não existente é especificado no arquivo de importação, como uma coluna com um `_<non-existing name>` cabeçalho.

## Importar operações

| Operação | Descrição |
| --------- | ----------- |
| Adicionar/Atualizar | Os novos dados de produtos são adicionados aos dados de produtos existentes para as entradas existentes no banco de dados. Todos os campos exceto `sku` pode ser atualizado.<br><br>As novas classes de imposto especificadas nos dados de importação são criadas automaticamente.<br><br>Novas categorias de produtos especificadas no arquivo de importação são criadas automaticamente.<br><br>Novos SKUs especificados no arquivo de importação são criados automaticamente <br><br>**_Nota:_**Para produtos, é possível atualizar todos os campos, exceto SKU, por meio da importação.<br><br>**_Importante:_** Vários valores de campo, como sites ou categorias, não podem ser removidos usando o _Adicionar/Atualizar_ comportamento de importação. Esses campos permanecerão no banco de dados após a importação se não estiverem listados no arquivo CSV. |
| Substituir | Os dados existentes do produto são substituídos por novos dados.<br><br>**_Importante:_**Tenha cuidado ao substituir dados, pois os dados existentes do produto são apagados e todas as referências no sistema são perdidas.<br><br>Se um SKU nos dados de importação corresponder ao SKU de uma entidade existente, todos os campos, incluindo o SKU, serão excluídos e um novo registro será criado usando os dados CSV. Ocorre um erro se o arquivo CSV referenciar uma SKU que não existe no banco de dados. Você pode Verificar dados para exibir um erro. |
| Excluir | Todas as entidades nos dados de importação existentes no banco de dados são excluídas do banco de dados.<br><br>Excluir ignora todas as colunas nos dados de importação, exceto o SKU. É possível ignorar todos os outros atributos nos dados.<br><br>Ocorre um erro se o arquivo CSV referenciar uma SKU que não existe no banco de dados. Você pode Verificar dados para exibir um erro. |

{style="table-layout:auto"}

## Processo de importação

O tamanho do arquivo de importação é determinado pelas configurações no `php.ini` no servidor. A mensagem do sistema no _Importar_ indica o limite de tamanho atual. O tamanho padrão é 2 MB.

Caracteres especiais (como o sinal de igual, símbolos maiores e menores que, aspas simples e duplas, barra invertida, barra vertical e símbolos de E comercial) podem causar problemas durante a transferência de dados. Para garantir que esses caracteres especiais sejam interpretados corretamente, eles podem ser marcados como um _sequência de escape_. Por exemplo, se os dados incluírem uma cadeia de texto como `code="str"`, `code="str2"`, ao escolher colocar o texto entre aspas duplas, você garante que as aspas duplas originais sejam compreendidas como parte dos dados. Quando o sistema encontra um conjunto duplo de aspas duplas, ele entende que o conjunto externo de aspas duplas está delimitando os dados reais.

Ao importar dados de produtos, novos dados de produtos são adicionados às entradas de dados de produtos existentes no banco de dados. Todos os campos, exceto o SKU, podem ser atualizados por meio da importação. Todos os dados existentes do produto são substituídos pelos novos dados importados. Tenha cuidado ao substituir dados. Todos os dados existentes do produto são apagados e todas as referências no sistema são perdidas.

![Importação de dados](./assets/import-options.png){width="600" zoomable="yes"}

### Etapa 1: Preparar os dados

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Em _Importar configurações_, definir **[!UICONTROL Entity Type]** a um dos seguintes:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers and Addresses`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

1. Clique em **[!UICONTROL Download Sample File]**.

1. Localize o arquivo de exportação no local de downloads do seu navegador da Web e abra o arquivo.

   O arquivo de amostra inclui títulos de coluna com dados de espaço reservado para os tipos de produto.

   ![Importar arquivo de amostra de dados](./assets/data-export-sample-data.png){width="600" zoomable="yes"}

1. Examine a estrutura do arquivo de amostra e use-a para preparar seu arquivo de importação de CSV, certificando-se de que os cabeçalhos das colunas estejam escritos corretamente.

1. Verifique se o tamanho do arquivo de importação não excede o limite mostrado na mensagem.

   ![Notificação de tamanho da importação de dados](./assets/data-import-size-notification.png){width="600"}

1. Se os dados de importação incluírem caminhos para imagens de produtos, verifique se os arquivos de imagem foram carregados no local apropriado.

   O local padrão no servidor do Commerce é: `pub/media/import`.

   Se as imagens residirem em um servidor externo, verifique se você tem o URL completo para o diretório que contém as imagens.

### Etapa 2: Escolher o comportamento de importação

![Comportamento de importação de dados](./assets/data-import-import-behavior.png){width="600" zoomable="yes"}

1. Definir **[!UICONTROL Import Behavior]** a um dos seguintes:

   - `Add/Update` (Para produtos, você pode atualizar todos os campos, exceto o SKU por meio da importação.)
   - `Replace`
   - `Delete`

1. Para determinar o que acontece quando um erro é encontrado ao importar dados, escolha uma das seguintes opções:

   - `Stop on Error`
   - `Skip error entries`

1. Para **[!UICONTROL Allowed Errors Count]**, insira o número de erros que podem ocorrer antes que a importação seja cancelada.

   O valor padrão é 10.

1. Aceite o valor padrão de uma vírgula (`,`) para **[!UICONTROL Field separator]**.

1. Aceite o valor padrão de uma vírgula (`,`) para **[!UICONTROL Multiple value separator]**.

   Em um arquivo CSV, uma vírgula é o separador padrão. Para usar um caractere diferente, verifique se os dados no arquivo CSV correspondem ao caractere especificado.

1. Aceite o valor padrão `_EMPTY_VALUE_` para **[!UICONTROL Empty attribute value constant]**.

1. Se quiser incluir qualquer caractere especial que possa ser encontrado nos dados como um _sequência de escape_, selecione o **[!UICONTROL Fields Enclosure]** caixa de seleção

### Etapa 3: identificar o arquivo de importação

![Arquivo de importação de dados](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Choose File]** para selecionar o arquivo a ser importado.

1. Encontre o arquivo CSV que você preparou para importar e clique em **[!UICONTROL Open]**.

1. Para **[!UICONTROL Images File Directory]**, insira o caminho relativo para o local no servidor do Commerce onde as imagens carregadas são armazenadas.

   Por exemplo: `product_images`.

   >[!NOTE]
   >
   >Primeiramente com o Adobe Commerce e o Magento Open Source `2.3.2` versão, o caminho especificado em _[!UICONTROL Images File Directory]_concatena para importação no diretório base de imagens: `<Magento-root-folder>/var/import/images`. Por exemplo, posicione o `product_images` arquivos no `<Magento-root-directory>/var/import/images/product_images` pasta. O diretório base de imagens de importação pode ser configurado no `\Magento\ImportExport\etc\config.xml` arquivo. Se o módulo de Armazenamento remoto estiver habilitado, importe os arquivos para o `<remote-storage-root-directory>/var/import/images/product_images` pasta.

   Para saber mais sobre como importar imagens de produtos, consulte [Importar imagens do produto](data-import-product-images.md).

### Etapa 4: verificar os dados de importação

1. No canto superior direito, clique em **[!UICONTROL Check Data]**.

1. Aguarde alguns momentos para que o processo de validação seja concluído.

   Se os dados de importação forem válidos, a seguinte mensagem será exibida:

   ![Mensagem de sucesso - o arquivo é válido](./assets/data-import-validation-message.png){width="600"}

1. Se o arquivo for válido, clique em **[!UICONTROL Import]**.

   Caso contrário, corrija cada problema com os dados listados na mensagem e tente importar o arquivo novamente.

1. O processo de importação continua até o final dos dados, a menos que seja encontrado um erro.

   Se uma mensagem de erro for exibida nos Resultados da validação, corrija o problema nos dados e importe o arquivo novamente.

   ![Mensagem de erro - A chave de URL já existe](./assets/data-import-validation-error-url-key-exists.png){width="600"}

   Uma mensagem é exibida quando a importação é concluída.

## Importar histórico

O Commerce mantém um registro dos dados que foram importados para sua loja, incluindo a data e a hora de início, o usuário, o tempo de execução e um link para o arquivo importado. A variável _Tempo de execução_ é a duração do processo de importação.

**_Para exibir o histórico de importação:_**

No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import History]**.

![Histórico de importação de dados](./assets/data-import-history.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Por padrão, os arquivos do histórico de importação estão na `<Magento-root-directory>/var/import_history` pasta. Se o módulo de Armazenamento remoto estiver habilitado, os arquivos do histórico de importação estarão na `<remote-storage-root-directory>/import_export/import_history` pasta.

| Campo | Descrição |
|--- |--- |
| [!UICONTROL ID] | Um número interno usado para designar uma transferência. |
| [!UICONTROL Start Date & Time] | Uma data e hora específicas em que a transferência ocorreu. |
| [!UICONTROL User] | O cliente que fez a transferência. |
| [!UICONTROL Imported file] | Link para baixar o arquivo importado. |
| [!UICONTROL Error file] | O arquivo de erro correspondente. |
| [!UICONTROL Execution Time] | Intervalo de tempo do processo de importação. |
| [!UICONTROL Summary] | O número de itens criados, atualizados e excluídos ou a mensagem de erro. |

{style="table-layout:auto"}

Para baixar o _Importado/Erro_ arquivo, clique em **[!UICONTROL Download]**.
