---
title: Impostos
description: Saiba como configurar sua loja para calcular impostos de acordo com os requisitos de sua localidade.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Impostos

Configure sua loja para calcular impostos de acordo com os requisitos de sua localidade. Você pode configurar [classes de imposto](tax-class.md) para produtos e grupos de clientes, e criar [regras de imposto](tax-rules.md) que combinam classes de produto e cliente, zonas de imposto e alíquotas. O Commerce também fornece definições de configuração para impostos fixos de produtos, impostos compostos e exibição para preços entre fronteiras internacionais. Se você precisar coletar um [imposto sobre o valor acrescentado](vat.md), você pode configurar sua loja para calcular automaticamente a quantidade apropriada com a validação.

>[!NOTE]
>
>O Adobe Commerce e o Magento Open Source versões 2.4.0 a 2.4.3 incluíam a extensão desenvolvida pelo fornecedor Vertex usada para integrar com a Vertex Cloud para fornecer gerenciamento de impostos e limpeza de endereços. A partir da versão 2.4.4, essa extensão não será mais fornecida com a versão principal e deverá ser instalada e atualizada do Commerce Marketplace ou diretamente do fornecedor. [Vértice de contato](https://marketplace.magento.com/partner/vertex_inc) para obter informações sobre a extensão e a documentação.<br><br>
>
>Se você tiver a extensão agrupada ativada e configurada, deverá atualizar o arquivo composer.json como parte do processo de atualização 2.4.4 e gerenciar as atualizações de extensão a partir de agora. Consulte [Atualizar módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) no _Guia de atualização_.

## Referência rápida

Algumas configurações de imposto têm uma opção de opções que determina como o imposto é calculado e apresentado ao cliente. Para obter mais informações, consulte [Diretrizes Fiscais Internacionais](international-tax-guidelines.md).

Use as tabelas a seguir como referência ao definir as configurações de cálculo de imposto:

### Métodos de cálculo de imposto

As opções de método de cálculo de imposto incluem [!UICONTROL Unit Price], [!UICONTROL Row Total], e [!UICONTROL Total]. A tabela a seguir explica como o arredondamento (para dois dígitos) é tratado para configurações diferentes.

| Configuração | Cálculo e exibição |
|--- |--- |
| [!UICONTROL Unit Price] | O Commerce calcula o imposto para cada item e exibe preços com imposto incluído. Para calcular o total de imposto, ele arredonda o imposto para cada item e os soma. |
| [!UICONTROL Row Total] | O Commerce calcula o imposto para cada linha. Para calcular o total do imposto, ele arredonda o imposto para cada item de linha e os soma. |
| [!UICONTROL Total] | O Commerce calcula o imposto para cada item e adiciona esses valores de imposto para calcular a quantia total de imposto não arredondada para o pedido. Em seguida, ele aplica o modo de arredondamento especificado ao imposto total para determinar o imposto total do pedido. |

{style="table-layout:auto"}

### Preços de catálogo com ou sem imposto

Os campos de exibição possíveis variam dependendo do método de cálculo e se os preços de catálogo incluem ou excluem impostos. Os campos de exibição têm precisão de duas casas decimais em cálculos normais. Algumas combinações de configurações de preço exibem preços que incluem e excluem imposto. Quando ambos aparecem no mesmo item da linha, pode ser confuso para os clientes e aciona um [aviso](taxes.md#warning-messages).

| Configuração | Cálculo e exibição |
|--- |--- |
| [!UICONTROL Excluding Tax] | Usando esta configuração, o preço-base do item é usado conforme é informado e os métodos de cálculo do imposto são aplicados. |
| [!UICONTROL IncludingTax] | Usando esta configuração, o preço-base do item que exclui o imposto é calculado primeiro. Esse valor é usado como o preço base e os métodos de cálculo do imposto são aplicados. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Há alterações em relação a versões anteriores para comerciantes da UE ou outros comerciantes de IVA que exibem preços, incluindo impostos, e operam em vários países com várias visualizações de loja. Se você carregar os preços com mais de dois dígitos de precisão, o Commerce arredondará automaticamente todos os preços para dois dígitos, para garantir que um preço consistente seja apresentado aos compradores.

### Preços de envio com ou sem imposto

| Configuração | Exibir | Cálculo |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | Aparece sem imposto. | Cálculo normal. O frete é adicionado ao total do carrinho, normalmente exibido como um item separado. |
| [!UICONTROL Including Tax] | Pode ser imposto incluso ou imposto pode ser exibido separadamente. | O envio é tratado como outro item no carrinho com impostos, usando os mesmos cálculos. |

{style="table-layout:auto"}

### Valores de imposto como itens de linha

Para exibir duas quantias de imposto diferentes como itens de linha separados, como GST e PST para lojas canadenses, é necessário definir prioridades diferentes para as regras de imposto relacionadas. No entanto, em cálculos de impostos anteriores, impostos com prioridades diferentes seriam automaticamente compostos. Para exibir corretamente quantias de imposto separadas sem uma composição incorreta das quantias de imposto, é possível definir prioridades diferentes e também selecionar a variável _Calcular somente o subtotal_ caixa de seleção Essa configuração produz valores de imposto calculados corretamente que aparecem como itens de linha separados.

## Mensagens de aviso

Algumas combinações de opções relacionadas a impostos podem ser confusas para os clientes e acionar um aviso. Essas condições podem ocorrer quando o método de cálculo do imposto é definido como `Row` ou `Total`e ao cliente são apresentados preços que excluem e incluem impostos. Também pode ocorrer quando há imposto por item no carrinho. Como o cálculo do imposto é arredondado, o valor que aparece no carrinho pode ser diferente do valor que um cliente espera pagar.

Se o cálculo do imposto for baseado em uma configuração problemática, serão exibidas as seguintes advertências:

![Ponto de exclamação](../assets/icon-warning.png) **Aviso**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![Ponto de exclamação](../assets/icon-warning.png) **Aviso**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## Lugar das entregas de bens digitais (UE)

Os comerciantes da União Europeia (UE) devem comunicar seus bens digitais vendidos por trimestre a cada país membro. Os bens digitais são tributados com base no endereço de entrega do cliente. A lei exige que os comerciantes executem um relatório de impostos e identifiquem os valores de impostos relevantes para bens digitais, em vez de bens físicos.

Os comerciantes devem comunicar todos os bens digitais vendidos por países membros da UE trimestralmente a uma administração fiscal central, juntamente com o pagamento devido pelo imposto cobrado durante o período.

Os comerciantes que ainda não atingiram o limiar (50 mil/100 mil euros de atividade anual) devem continuar a comunicar os bens físicos vendidos aos Estados-Membros da UE onde registraram números de IVA.

Os comerciantes auditados para impostos pagos por bens digitais devem fornecer duas informações de apoio para estabelecer o local de residência do cliente.

- O endereço de entrega do cliente e um registro de uma transação de pagamento bem-sucedida podem ser usados para estabelecer o local de residência do cliente. (O pagamento é aceito somente se o endereço de entrega corresponder às informações do provedor de serviço de pagamento.)
- As informações também podem ser capturadas diretamente do armazenamento de dados nas tabelas do banco de dados do Commerce.

_**Para coletar informações sobre imposto de mercadorias digitais, faça o seguinte:**_

1. Carregar as taxas de imposto para todos os países membros da UE.

1. Crie uma classe de imposto de produto de mercadorias digitais.

1. Atribua todas as mercadorias digitais à classe de imposto de produto de mercadorias digitais.

1. Criar [regras de imposto](tax-rules.md) para mercadorias físicas, usando classes de imposto do produto físico e associando-as às alíquotas de imposto apropriadas.

1. Crie regras de imposto para seus bens digitais, usando a classe de imposto do produto para bens digitais, e associe-as às taxas de imposto apropriadas para países membros da UE.

1. Execute o relatório de imposto para o período apropriado e colete as informações de mercadorias digitais necessárias.

1. Exportar os valores de imposto relacionados às alíquotas de imposto para a classe de imposto do produto de mercadorias digitais.

Recursos adicionais:

- [Comissão Europeia - Fiscalidade e União Aduaneira][1]
- [Alterações no local de fornecimento da UE 1015][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html
