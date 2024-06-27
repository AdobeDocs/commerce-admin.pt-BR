---
title: Transferência de dados
description: Saiba mais sobre o suporte para transferência de dados, incluindo validação de dados.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: b89d6b08d0559dc769a8c51570696f033f23c7f3
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Transferências de dados

Use as ferramentas de importação e exportação para gerenciar vários registros em uma única operação. É possível importar novos itens, bem como atualizar, substituir e excluir conjuntos de produtos existentes.

Por exemplo, você pode adicionar novos produtos ao inventário, atualizar dados de produtos e dados avançados de preços e substituir um conjunto de produtos existentes por novos produtos. As ferramentas de importação e exportação ajudam a gerenciar grandes catálogos de produtos com mais eficiência, pois você pode exportar os dados, editá-los em uma planilha e importá-los de volta para sua loja em vez de executar várias operações no Administrador.


>[!NOTE]
>
>A Adobe Commerce também oferece suporte à exportação de dados SaaS para transferir dados do produto do servidor Commerce para os serviços SaaS. A exportação de dados SaaS é integrada aos serviços SaaS da Commerce, incluindo [Recommendations do produto](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html), [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview), e [Serviço de catálogo](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview). Para obter detalhes, consulte [Guia de exportação de dados SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

## Validação de dados

Todos os dados devem passar na validação para garantir a qualidade, a precisão e a integridade dos valores antes de importá-los para o armazenamento. A validação começa ao clicar em **[!UICONTROL Check Data]**. Durante o processo, todas as entidades no arquivo de importação são verificadas em relação ao seguinte:

- **Atributos** - Os nomes dos cabeçalhos de coluna são verificados para garantir que correspondam aos atributos correspondentes no banco de dados do sistema. O valor de cada atributo é verificado para garantir que ele atenda aos requisitos do tipo de dados (decimal, inteiro, varchar, texto e datetime).
- **Dados complexos** - Valores que se originam de um conjunto definido, como um tipo suspenso ou de entrada de seleção múltipla, são verificados para garantir que os valores existam no conjunto definido.
- **Dados do serviço** - Os valores nas colunas de dados de serviço são verificados para garantir que as propriedades ou valores de dados complexos sejam consistentes com o que já está definido no banco de dados do sistema.
- **Valores obrigatórios** - Para novas entidades, a presença dos valores de atributo necessários no arquivo é verificada. Para entidades existentes, não há necessidade de verificar novamente a existência de valores de atributo obrigatórios.
- **Separadores** - Embora os separadores não estejam visíveis quando visualizados em uma planilha, os valores de dados em um arquivo CSV são separados por vírgula e os valores de texto são colocados entre aspas duplas. Durante o processo de validação, a formatação dos separadores e de cada conjunto de aspas que delimita cadeias de caracteres é verificada.

Os resultados da validação são exibidos na seção Resultados da Validação e incluem as seguintes informações:

- O número de entidades verificadas
- O número de linhas inválidas
- O número de erros encontrados

Se os dados forem válidos, uma _Importação bem-sucedida_ é exibida.

![Mensagem do sistema - o arquivo é válido](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

Se a validação falhar, leia a descrição de cada erro e corrija o problema no arquivo CSV. Por exemplo, se uma linha contiver um SKU inválido, o processo de importação será interrompido e essa linha, e todas as linhas subsequentes não serão importadas. Após corrigir o problema, importe os dados novamente. Se forem encontrados muitos erros, poderá levar várias tentativas para passar na validação.

### Mensagens de validação de dados

#### Validação

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### Erros

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
