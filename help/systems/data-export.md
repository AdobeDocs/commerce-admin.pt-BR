---
title: Exportar dados
description: Saiba mais sobre atributos e filtros de exportação de dados e como exportar dados de sua loja.
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Exportar dados

A melhor maneira de se familiarizar com a estrutura do banco de dados é exportar os dados e abri-los em uma planilha. Depois de se familiarizar com o processo, você pode usá-lo como uma maneira eficiente de gerenciar grandes quantidades de informações.

Caracteres especiais — como o sinal de igual, símbolos maiores e menores que, aspas simples e duplas, barra invertida, barra vertical e símbolos de E comercial — podem causar problemas durante a transferência de dados. Para garantir que esses caracteres especiais sejam interpretados corretamente, eles podem ser marcados como uma _sequência de escape_. Por exemplo, se os dados incluírem uma cadeia de caracteres de texto como `code="str"`, `code="str2"`, colocar o texto entre aspas duplas garante que as aspas duplas originais sejam entendidas como parte dos dados: `"code="str""`. Quando o sistema encontra um conjunto duplo de aspas duplas, ele entende que o conjunto externo de aspas duplas está delimitando os dados reais.

A exportação de dados é uma operação assíncrona, executada em segundo plano para que você possa continuar trabalhando no Administrador sem esperar a conclusão da operação. O sistema exibe uma mensagem quando a tarefa é concluída.

## Critérios de exportação

Os filtros de exportação são usados para especificar os dados que você deseja incluir no arquivo de exportação, com base no valor do atributo. Além disso, você pode especificar quais dados de atributo deseja incluir ou excluir da exportação.

![Critérios de exportação de dados](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### Exportar filtros

Você pode usar filtros para determinar quais SKUs estão incluídos no arquivo de exportação. Por exemplo, se você inserir um valor no filtro País de fabricação, o arquivo CSV exportado incluirá somente produtos fabricados nesse país.

O tipo de filtro corresponde ao tipo de dados. Para campos de data, você pode escolher a data no ![Ícone do calendário](../assets/icon-calendar.png). Consulte [Tipos de Entrada de Atributo](../catalog/attributes-input-types.md) para obter mais informações.

O formato da data é determinado pela [localidade](../getting-started/store-details.md#locale-options).

Para incluir apenas registros com um valor específico, como um SKU, insira o valor no campo Filtro. Alguns campos, como Preço, Peso e Definir Produto como Novo, têm uma faixa de valores de/até.

### Excluir atributos

A caixa de seleção na primeira coluna é usada para excluir atributos do arquivo de exportação. Se um atributo for excluído, a coluna associada nos dados de exportação será incluída, mas estará vazia.

| Excluir | Filtro | Resultado |
|--- |--- |--- |
| ![Caixa de seleção](../assets/checkbox-clear.png) desmarcada | Não | O arquivo exportado contém cada atributo para todos os registros existentes. |
| ![Caixa de seleção](../assets/checkbox-clear.png) desmarcada | Sim | O arquivo de exportação contém cada atributo com apenas os registros permitidos pelo filtro. |
| ![Caixa de seleção](../assets/checkbox-selected.png) selecionada | Não | O arquivo de exportação não inclui a coluna do atributo excluído, mas inclui todos os registros existentes. |
| ![Caixa de seleção](../assets/checkbox-selected.png) selecionada | Sim | O arquivo de exportação não inclui a coluna para o atributo excluído e contém apenas os registros permitidos pelo filtro. |

{style="table-layout:auto"}

## Exportar dados

1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Na seção _Configurações de Exportação_, defina **[!UICONTROL Entity Type]** como um dos seguintes:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![Configurações de exportação de dados](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. Aceite o padrão **[!UICONTROL Export File Format]** de CSV.

1. Para colocar qualquer caractere especial que possa ser encontrado nos dados como uma _sequência de escape_, marque a caixa de seleção **[!UICONTROL Fields Enclosure]**.

1. Se necessário, altere a exibição dos atributos de entidade.

   Por padrão, a seção Atributos da Entidade lista todos os atributos disponíveis em ordem alfabética. Você pode usar os [controles de lista](../getting-started/admin-grid-controls.md) padrão para procurar atributos específicos e classificar a lista. Os controles de Filtro de pesquisa e redefinição controlam a exibição da lista, mas não têm efeito na seleção de atributos a serem incluídos no arquivo de exportação.

   ![Atributos de entidade filtrados da exportação de dados](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. Para filtrar os dados exportados com base no valor do atributo, faça o seguinte:

   - Para exportar apenas registros com valores de atributo específicos, insira o valor necessário na coluna **[!UICONTROL Filter]**. O exemplo a seguir exporta somente um SKU específico.

   - Para omitir um atributo da exportação, marque a caixa de seleção **[!UICONTROL Exclude]** no início da linha. Por exemplo, para exportar apenas as colunas `sku` e `image`, marque a caixa de seleção de todos os outros atributos. A coluna aparece no arquivo de exportação, mas sem valores.

1. Role para baixo e clique em **[!UICONTROL Continue]** no canto inferior direito da página.

   Após a conclusão da tarefa, o arquivo é processado por meio de uma fila de mensagens (verifique se o trabalho cron está em execução). O arquivo exportado é salvo no `var/export/ folder`. Para obter mais informações sobre a fila de mensagens, consulte [Gerenciar filas de mensagens](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=pt-BR) no _Guia de Configuração_.

   Você pode salvar ou abrir o arquivo CSV exportado como uma planilha, editar os dados e importá-los de volta para o armazenamento.

   >[!NOTE]
   >
   >Por padrão, todos os arquivos exportados estão na pasta `<Magento-root-directory>/var/export`. Se o módulo de Armazenamento remoto estiver habilitado, todos os arquivos exportados estarão na pasta `<remote-storage-root-directory>/import_export/export`.

## Solução de problemas de recursos

Para obter ajuda com a solução de problemas de exportação de dados, consulte os seguintes artigos da Base de conhecimento de suporte da Commerce:

- [O arquivo .csv de produtos exportados não aparece](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html?lang=pt-BR)
