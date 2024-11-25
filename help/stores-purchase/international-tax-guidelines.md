---
title: Diretrizes de imposto por país
description: Revisar configurações de imposto recomendadas de acordo com o país.
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---

# Diretrizes de imposto por país

## Configuração de imposto dos EUA

Essas configurações recomendadas podem ser usadas para a maioria das configurações de impostos para lojas nos Estados Unidos.

| Opção de imposto | Recomendação |
|--- |--- |
| Carregar preços de catálogo | Excluindo imposto |
| FPT | Não, porque o FPT não é tributado. |
| Imposto baseado em | Origem da remessa |
| Cálculo de Imposto | No total |
| Envio de impostos? | Não |
| Aplicar desconto | Antes do imposto |
| Comentário | Todas as zonas de imposto têm a mesma prioridade; idealmente, uma zona para estado e uma ou mais zonas para pesquisa de código postal. |

{style="table-layout:auto"}

### Classes de imposto

| Classe de imposto | Configuração recomendada |
|--- |--- |
| Classe de imposto para remessa | Nenhum |

{style="table-layout:auto"}

### Configurações de cálculo

| Opção | Configuração recomendada |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Cálculo de destino de imposto padrão

| Opção | Configuração recomendada |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | Estado onde a empresa está localizada. |
| [!UICONTROL Default Post Code] | O CEP usado em suas zonas de imposto. |

{style="table-layout:auto"}

### Configurações de exibição de preço

| Opção | Configuração recomendada |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Configurações de exibição do carrinho de compras

| Opção | Configuração recomendada |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Configurações de ordens, faturas, avisos de crédito e exibição

| Opção | Configuração recomendada |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Impostos fixos do produto (FPT)

| Opção | Configuração recomendada |
|--- |--- |
| [!UICONTROL Enable FPT] | `No`, exceto na Califórnia. |

{style="table-layout:auto"}

## Configuração de imposto do Reino Unido

Essas configurações recomendadas podem ser usadas para a maioria das configurações de impostos para lojas no Reino Unido.

### Configuração de imposto B2C do Reino Unido

| Opção de imposto | Recomendação |
|--- |--- |
| Carregar preços de catálogo | Excluindo imposto |
| FPT | Sim, incluindo FPT e descrição |
| Imposto baseado em | [!UICONTROL Shipping Address] |
| Cálculo de Imposto | No total |
| Envio de impostos? | Sim |
| Aplicar desconto | Antes de impostos, desconto sobre preços, incluindo impostos. |
| Comentário | Para comerciantes que marcam NFFs do fornecedor (incluindo IVA). |

{style="table-layout:auto"}

### Configuração de imposto B2B do Reino Unido

| Opção de imposto | Recomendação |
|--- |--- |
| Carregar preços de catálogo | Excluindo imposto |
| FPT | Sim, incluindo FPT e descrição |
| Imposto baseado em | [!UICONTROL Shipping Address] |
| Cálculo de Imposto | No item |
| Envio de impostos? | Sim |
| Aplicar desconto | Antes de impostos, desconto sobre preços, incluindo impostos. |
| Comentário | Para os comerciantes B2B fornecerem considerações mais simples sobre a cadeia de fornecimento de IVA. O cálculo de imposto na linha também é válido; no entanto, verifique com sua jurisdição de tributação. A configuração pressupõe que um comerciante esteja na cadeia de suprimentos e que os bens vendidos sejam usados por outros fornecedores para descontos de IVA e assim por diante. Essa definição facilita a diferenciação de imposto por item para uma geração de descontos mais rápida. <br/><br/>**_Observação:_**algumas jurisdições exigem estratégias de arredondamento diferentes não suportadas atualmente pela Commerce e nem todas as jurisdições permitem imposto no nível do item ou da linha. |

{style="table-layout:auto"}

## Configuração de imposto do Canadá

>[!IMPORTANT]
>
>Os comerciantes que estão em uma província de GST/PST (Montreal) devem criar uma regra de imposto e mostrar um valor de imposto combinado. Certifique-se de consultar uma autoridade fiscal qualificada em caso de dúvidas.

| Opção de imposto | Recomendação |
|--- |--- |
| Carregar preços de catálogo | Excluindo imposto |
| FPT | Sim, incluindo FPT, descrição e aplicar imposto a FPT. |
| Imposto baseado em | Origem da remessa |
| Cálculo de Imposto | No total |
| Envio de impostos? | Sim |
| Aplicar desconto | Antes do imposto |

{style="table-layout:auto"}

O exemplo a seguir mostra como configurar alíquotas de imposto GST para o Canadá e alíquotas de imposto PST para Saskatchewan, com regras de imposto que calculam e exibem as duas alíquotas de imposto. Essas informações descrevem um exemplo de configuração; certifique-se de verificar as alíquotas e regras de imposto corretas para suas jurisdições de imposto. Ao configurar impostos, defina o escopo da loja para aplicar a configuração a todas as lojas e sites aplicáveis.

- O imposto fixo do produto é incluído para mercadorias relevantes como um atributo do produto.
- Em Quebec, PST é referido como TVQ. Se você quiser configurar uma taxa para Quebec, certifique-se de usar TVQ como o identificador.

### Etapa 1: Concluir configurações de cálculo de imposto

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Para uma configuração multissite, defina **[!UICONTROL Store View]** para o site e armazene que é o destino da configuração.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Tax]**.

1. Clique em para expandir cada seção na página e concluir as seguintes configurações:

#### Configurações de Cálculo de Imposto

| Campo | Configuração recomendada |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` (se disponível) |

{style="table-layout:auto"}

#### Classes de Impostos

| Campo | Configuração recomendada |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (remessa tributada) |

{style="table-layout:auto"}

#### Cálculo do Destino do Imposto Padrão

| Campo | Configuração recomendada |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | (conforme apropriado) |
| [!UICONTROL Default Postal Code] | `*` (asterisco) |

{style="table-layout:auto"}

#### Configurações de exibição do carrinho de compras

| Campo | Configuração recomendada |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### Impostos Fixos sobre Produtos

| Campo | Configuração recomendada |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| Todas as configurações de exibição de FPT | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### Etapa 2: Configurar Imposto Canadense de Mercadorias e Serviços (GST)

Para imprimir o número GST em NFFs e outros documentos de vendas, inclua-o no nome das alíquotas de imposto aplicáveis. O GST é exibido como parte do valor de GST em qualquer resumo de pedido.

#### Gerenciar Zonas de Imposto e Taxas

| Campo | Configuração recomendada |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` (asterisco) |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (asterisco) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Fase 3: Configurar o Imposto Provinciano Canadense (PST)

Configure outra alíquota do imposto para a província aplicável.

#### Informações sobre Alíquota de Imposto

| Campo | Configuração recomendada |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (asterisco) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Etapa 4: Criar uma regra de imposto GST

Para evitar a composição do imposto e exibir corretamente o imposto calculado como itens de linha separados para GST e PST, defina prioridades diferentes para cada regra e marque a caixa de seleção **Calcular somente subtotal**. Cada imposto aparece como um item de linha separado, mas as quantias de imposto não são compostas.

#### Informações sobre Regra de Imposto

| Campo | Configuração recomendada |
|--- |--- |
| Nome | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | Marque essa caixa de seleção. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Etapa 5: Criar uma Regra de Imposto PST para Saskatchewan

Para esta regra de imposto, defina a prioridade como 0 e marque a caixa de seleção **Calcular somente subtotal**. Cada imposto aparece como um item de linha separado, mas as quantias de imposto não são compostas.

#### Informações sobre Regra de Imposto

| Campo | Configuração recomendada |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | Marque essa caixa de seleção. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Etapa 6: salvar e testar os resultados

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Retorne à loja e crie uma ordem de amostra para testar os resultados.

## Configuração de imposto da UE

O exemplo a seguir mostra uma loja com sede na França que vende mais de 100 mil euros na França e mais de 100 mil euros na Alemanha.

- Os cálculos de impostos são gerenciados no nível do site.
- A conversão de moeda e as opções de exibição de imposto são controladas individualmente no nível de exibição de loja (marque a caixa de seleção Usar Website para sobrepor o padrão).
- Ao definir o país de imposto padrão, você pode mostrar dinamicamente o imposto correto para a jurisdição.
- O imposto fixo do produto é incluído para mercadorias relevantes como um atributo do produto.
- Talvez seja necessário editar o catálogo para garantir que ele seja exibido na categoria/site/exibição de loja correta.

### Fase 1: Criar três classes de imposto do produto

Para este exemplo, presume-se que não são necessárias várias classes de imposto sobre produtos com IVA reduzido.

1. Criar uma classe de imposto de produto padrão IVA.

1. Criar uma classe de imposto do produto com IVA Reduzido.

1. Criar uma classe de imposto de produto sem IVA.

### Etapa 2: Criar alíquotas de imposto para França e Alemanha

Crie as seguintes alíquotas de imposto:

| Alíquotas de imposto | Configurações  |
|--- |--- |
| França-PadrãoIVA | País: França <br/>Estado/Região: * <br/>CEP: * <br/>Taxa: 20% |
| França - IVA reduzido | País: França <br/>Estado/Região: * <br/>CEP: * <br/>Taxa: 5% |
| Alemanha - IVA padrão | País: Alemanha <br/>Estado/Região: * <br/>CEP: * Taxa: 19% |
| Alemanha - IVA reduzido | País: Alemanha <br/>Estado/Região: * <br/>CEP: * <br/>Taxa: 7% |

{style="table-layout:auto"}

### Etapa 3: Configurar as regras de imposto

Crie as seguintes regras de imposto:

| Regras de imposto | Configurações  |
|--- |--- |
| Varejo-França-PadrãoIVA | Classe do Cliente: Cliente de Varejo <br/>Classe do Imposto: VAT-Padrão <br/>Alíquota de Imposto: France-StandardVAT <br/>Prioridade: 0 <br/>Ordem de Classificação: 0 |
| Varejo-França - IVA Reduzido | Classe do Cliente: Cliente de Varejo <br/>Classe de Imposto: IVA Reduzido <br/>Alíquota de Imposto: França-IVA Reduzido <br/>Prioridade: 0 <br/>Ordem de Classificação: 0 |
| Varejo-Alemanha-PadrãoIVA | Classe do Cliente: Cliente de Varejo <br/>Classe do Imposto: VAT-Padrão <br/>Alíquota de Imposto: Germany-StandardVAT <br/>Prioridade: 0 <br/>Ordem de Classificação: 0 |
| Varejo-Alemanha-IVA Reduzido | Classe do Cliente: Cliente de Varejo <br/>Classe de Imposto: IVA Reduzido <br/>Alíquota de Imposto: Alemanha-IVA Reduzido <br/>Prioridade: 0 <br/>Ordem de Classificação: 0 |

{style="table-layout:auto"}

### Etapa 4: Configurar uma exibição de loja na Alemanha

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. No site padrão, crie uma exibição de loja para **[!UICONTROL Germany]**.

1. Em seguida, faça o seguinte:

   - Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - No canto superior esquerdo, defina **[!UICONTROL Default Config]** para a loja da França.

   - Na página Geral, expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Countries Options]** e defina o país padrão como `France`.

   - Preencha as opções de local, conforme necessário.

1. No canto superior esquerdo, escolha a **[!UICONTROL Store View]** alemã.

1. Na página _Geral_, expanda ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** e defina o país padrão como `Germany`.

1. Preencha as opções de local, conforme necessário.

### Etapa 5: Definir configurações de imposto para a França

Conclua as seguintes definições de imposto geral:

| Campo | Configuração recomendada |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (remessa tributada) |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` (asterisco) |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### Etapa 6: Definir configurações de imposto para a Alemanha

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No canto superior direito, defina **[!UICONTROL Store View]** como a exibição para a loja alemã e clique em **[!UICONTROL OK]** para confirmar.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Tax]**.

1. Na seção **[!UICONTROL Default Tax Destination Calculation]**, faça o seguinte:

   - Desmarque a caixa de seleção **[!UICONTROL Use Website]** após cada campo,

   - Para corresponder às Configurações de Envio do seu site [ponto de origem](shipping-settings.md#point-of-origin), atualize os seguintes valores:

      - País Padrão
      - Estado padrão
      - Código postal padrão

     Essa configuração garante que o imposto seja calculado corretamente quando os preços do produto incluírem imposto.

     ![Cálculo de Destino de Imposto Padrão](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
