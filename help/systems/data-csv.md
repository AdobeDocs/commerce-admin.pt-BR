---
title: Arquivos de dados CSV
description: Saiba mais sobre a estrutura usada no arquivo CSV para oferecer suporte à importação e exportação de dados.
exl-id: 86e362af-2af7-4557-ac49-1efad2f0e976
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# Arquivos de dados CSV

O formato de arquivo CSV (valores separados por vírgula) é usado como a base das operações de transferência de dados e é compatível com todos os aplicativos de planilha e banco de dados. Os seguintes tipos de arquivos são suportados para importação e exportação:

- Importar: `CSV` e `ZIP` (um arquivo CSV compactado)
- Exportar: `CSV`

>[!IMPORTANT]
>
>É recomendável usar um programa que ofereça suporte à codificação UTF-8, como o Notepad++, para editar arquivos CSV. O Microsoft® Excel insere caracteres adicionais no cabeçalho da coluna do arquivo CSV, o que pode impedir que os dados sejam importados novamente para o Commerce. Se você trabalhar no Mac, poderá salvar seus dados no formato CSV (Windows).

Os arquivos CSV têm uma estrutura específica que deve corresponder ao banco de dados. Cada cabeçalho de coluna corresponde ao Código de atributo do campo representado pela coluna. Para garantir que os títulos das colunas possam ser lidos pelo Commerce, primeiro exporte os dados de sua loja como um arquivo CSV. Em seguida, você pode editar os dados e importá-los novamente para o Commerce.

Se você abrir um arquivo CSV exportado em um editor de texto, verá que os valores são separados por vírgulas e vários valores são colocados entre aspas duplas. Durante a importação, é possível especificar um caractere separador personalizado, embora o padrão seja uma vírgula.

## Estrutura do CSV de produtos

Uma exportação completa do banco de dados de produtos contém informações sobre cada produto no catálogo e os relacionamentos entre eles. Cada registro tem uma seleção fixa de colunas que correspondem aos atributos no catálogo, embora a ordem dos atributos seja ignorada durante o processo de importação.

A primeira linha da tabela contém os nomes de cada atributo, que são usados como cabeçalhos de coluna. As linhas restantes descrevem os registros de produtos individuais. Qualquer linha que comece com um valor na coluna SKU é o início de um novo registro de produto. Um único produto pode incluir várias linhas que contêm informações sobre várias imagens ou opções de produto. A próxima linha que tiver um valor na coluna SKU inicia um novo produto.

A coluna de categoria contém um caminho para cada categoria à qual o produto está atribuído. O caminho inclui a categoria raiz, seguida por uma barra (`/`) entre cada nível. Por padrão, a vírgula `,` O caractere é usado para separar caminhos de categorias diferentes. (Você pode especificar um caractere separador diferente com a variável _[!UICONTROL Multiple value separator]_opção.) Por exemplo:

`Default Category/Gear,Default Category/Gear/Bags`

Para importar dados, você precisa incluir apenas o SKU e quaisquer colunas com alterações. Quaisquer colunas em branco são ignoradas durante o processo de importação. Não é possível adicionar atributos durante o processo de importação. É possível incluir apenas atributos existentes.

Para obter uma descrição detalhada de cada atributo de produto, consulte [Estrutura do arquivo CSV de produtos](data-attributes-product.md).

| Nome da coluna | Descrição |
| ----------- | ----------- |
| `_<name>` | Os cabeçalhos de coluna que começam com um sublinhado contêm propriedades de entidade de serviço ou dados complexos. As colunas de serviço não são atributos de produto. |
| `<attribute_name>` | Os cabeçalhos de coluna com um código de atributo ou nome de campo identificam a coluna de dados. Uma coluna pode representar um atributo do sistema ou que foi criado pelo administrador de armazenamento. |

{style="table-layout:auto"}

## Estrutura CSV do cliente

O arquivo CSV de clientes contém informações do cliente do banco de dados e tem a seguinte estrutura:

A primeira linha da tabela contém os nomes das colunas de atributo (que são iguais aos códigos de atributo). Há dois tipos de nomes de coluna, conforme mostrado na tabela a seguir. Outras linhas contêm valores de atributo, dados de serviço e dados complexos. Cada linha com valores não vazios na variável `email` e `_website` columns inicia a descrição do cliente subsequente. Cada linha pode representar dados do cliente com ou sem dados de endereço ou somente os dados de endereço. Se uma linha contiver apenas os dados de endereço, os valores nas colunas, relacionados ao perfil do cliente, serão ignorados e poderão estar vazios.

Para adicionar ou substituir mais de um endereço para um cliente, adicione uma linha para cada novo endereço com dados vazios do cliente e os dados novos ou atualizados do endereço abaixo da linha de dados do cliente.

Para obter uma descrição detalhada de cada atributo do cliente, consulte [Estrutura do arquivo CSV do cliente](data-attributes-customer.md).

| Nome da coluna | Descrição |
| ----------- | ----------- |
| `_<name>` | Os cabeçalhos de coluna que começam com um sublinhado contêm propriedades de entidade de serviço ou dados complexos. As colunas de serviço não são atributos do cliente. |
| `<attribute name>` | Os nomes das colunas com valores de atributos criados pelo sistema e atributos criados pelo administrador de armazenamento. |

{style="table-layout:auto"}
