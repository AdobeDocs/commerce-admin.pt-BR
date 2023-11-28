---
title: Criar etiquetas e pacotes de remessa
description: Saiba como empacotar itens em um pedido e criar etiquetas de remessa.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '1896'
ht-degree: 0%

---

# Criar etiquetas de remessa

Para criar etiquetas de remessa, você deve primeiro configurar sua conta de transportadora para etiquetas de suporte. Em seguida, siga as instruções para inserir uma descrição do pacote e seu conteúdo.

Depois de configurar as informações de etiqueta de remessa e enviar um pedido, o Commerce se conecta ao sistema da transportadora, envia um pedido e recebe uma etiqueta de remessa e um número de rastreamento. Se existir uma etiqueta para esta remessa no sistema, ela será substituída por uma nova. No entanto, os números de rastreamento existentes não são substituídos. Qualquer novo número de rastreamento é adicionado ao existente.

## Etapa 1: entre em contato com suas transportadoras

Antes de começar, verifique se suas contas de remessa estão configuradas para processar etiquetas. Algumas operadoras podem cobrar uma taxa extra para adicionar etiquetas de remessa à sua conta.

Entre em contato com cada transportadora usada para ativar as etiquetas de remessa da sua loja.

Siga as instruções fornecidas por cada transportadora para adicionar o suporte à etiqueta de remessa à sua conta.

- **FedEx** - Contato [Serviços de integração da Web FedEx][1] para saber mais sobre os requisitos de impressão de etiquetas para sua conta.
- **USPS** - Consulte o [Portal da API de Ferramentas da Web][4] em Centro de suporte ao despachante para saber como configurar suas credenciais de impressão de etiquetas.
- **UPS**- Contato [UPS][2] para confirmar se sua conta oferece suporte a etiquetas de remessa. Para gerar etiquetas de remessa, você deve usar a opção UPS XML.
- **DHL** - Contato [Soluções de comércio eletrônico da DHL][3] para saber mais sobre os requisitos de impressão de etiquetas para sua conta.

## Etapa 2: atualizar a configuração de cada operadora

1. Verifique se o seu [Armazenar informações](../getting-started/store-details.md#store-information) está concluído.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e selecione **[!UICONTROL Shipping Settings]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Origin]** e configure a variável **[!UICONTROL Shipping Origin Address]**.

1. Siga as instruções abaixo para cada conta de operadora ativada para a impressão de etiquetas.

### Configuração da UPS

O United Parcel Service envia tanto internamente quanto internacionalmente. No entanto, as etiquetas de remessa podem ser geradas apenas para remessas originárias dos Estados Unidos.

1. No _[!UICONTROL Sales]_no painel esquerdo, escolha **[!UICONTROL Delivery Methods]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL UPS]** seção.

1. Verifique se o no-break **[!UICONTROL Shipper Number]** está correto.

   O número do seu despachante aparece somente quando [!DNL United Parcel Service XML] está ativado.

1. Clique em **[!UICONTROL Save Config]**.

### Configuração da USPS

A variável [!DNL United States Postal Service] navios, tanto a nível nacional como internacional.

1. Continuar no **[!UICONTROL Delivery Methods]** configuração, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL USPS]** seção.

1. Verifique se **[!UICONTROL Secure Gateway URL]** está correto.

1. Insira o **[!UICONTROL Password]** fornecido a você pelo USPS.

1. Definir **[!UICONTROL Size]** para `Large` e insira valores para as seguintes dimensões:

   - Length
   - Largura
   - Altura
   - Girth

1. Clique em **[!UICONTROL Save Config]**.

### Configuração do FedEx

A FedEx é uma empresa nacional e internacional. Lojas localizadas fora dos Estados Unidos podem criar etiquetas FedEx apenas para remessas internacionais.

{{beta2-updates}}

1. Continuar no **[!UICONTROL Delivery Methods]** configuração, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL FedEx]** seção.

1. Verifique se as credenciais FedEx a seguir estão corretas:

   - Número do Medidor
   - Chave
   - Senha

1. Clique em **[!UICONTROL Save Config]**.

### Configuração DHL

A DHL presta serviços de transporte internacional.

1. Continuar no **[!UICONTROL Delivery Methods]** configuração, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL DHL]** seção.

1. Verifique se **[!UICONTROL Gateway URL]** está correto.

1. Verifique se as credenciais a seguir estão completas:

   - ID de acesso
   - Senha
   - Número da conta

1. Clique em **[!UICONTROL Save Config]**.

## Etapa 3: Criar etiquetas de remessa

### Método 1: Criar etiqueta para nova entrega

1. No _Admin_ barra lateral, vá para **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Localize a ordem na grade e abra o registro.

   O status do pedido deve ser `Pending` ou `Processing`.

1. No canto superior direito, clique em **[!UICONTROL Ship]**.

1. Confirme as informações de envio de acordo com os requisitos da transportadora.

1. No canto inferior direito, selecione a **[!UICONTROL Create Shipping Label]** caixa de seleção

1. Clique em **[!UICONTROL Submit Shipment]**.

1. Adicionar ou atualizar produtos no pacote:

   - Para adicionar produtos do pedido ao pacote, clique em **[!UICONTROL Add Products]**. A variável _[!UICONTROL Quantity]_mostra o número máximo de produtos disponíveis para o pacote.

   - Marque a caixa de seleção de cada produto a ser adicionado ao pacote e insira o **[!UICONTROL Quantity]** de cada um. Em seguida, clique em **[!UICONTROL Add Selected Product(s) to Package]**.

   - Para adicionar um pacote, clique em **[!UICONTROL Add Package]**.

   - Para excluir um pacote, clique em **[!UICONTROL Delete Package]**.

   - Para cancelar um pedido, clique em **[!UICONTROL Cancel]**. Um rótulo de remessa não é criado e o _[!UICONTROL Create Shipping Label]_está desmarcada.

   >[!NOTE]
   >
   >Se você usar um tipo de pacote diferente do padrão ou exigir uma assinatura, o custo de envio pode ser diferente do que você cobrou do cliente. Qualquer diferença no custo de envio não é refletida em sua loja.

1. Clique em **[!UICONTROL OK]**.

   O Commerce se conecta ao sistema da transportadora, envia o pedido e recebe um rótulo de remessa e um número de rastreamento para cada pacote.

### Método 2: Criar etiqueta para entrega existente

1. No _Admin_ barra lateral, vá para **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Localize o pedido na grade e abra o formulário de remessa.

1. No _[!UICONTROL Shipping and Tracking Information]_clique em **[!UICONTROL Create Shipping Label]**.

1. Distribua os produtos solicitados aos pacotes apropriados e clique em **[!UICONTROL OK]**.

1. Para revisar as informações do pacote, clique em **[!UICONTROL Show Packages]**.

## Etapa 4: Imprimir as etiquetas

As etiquetas de remessa são geradas no formato PDF e podem ser impressas no Administrador. Cada rótulo inclui o número do pedido e o número do pacote.

>[!NOTE]
>
>Como uma ordem de remessa individual para cada pacote é criada, várias etiquetas de remessa podem ser recebidas para uma única remessa.

### Método 1: Imprimir etiqueta do formulário de remessa

1. No _Barra lateral de administração_, vá para uma das seguintes páginas e localize o registro de remessa:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Localize a ordem na grade e abra o registro. No painel esquerdo, escolha **[!UICONTROL Shipments]**. Em seguida, abra o registro de remessa.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Localizar a remessa na grade e abrir o registro.

1. Para baixar o arquivo PDF, acesse o _[!UICONTROL Shipping and Tracking]_do formulário e clique em **[!UICONTROL Print Shipping Label]**.

   Dependendo das configurações do navegador, as etiquetas de remessa podem ser visualizadas e impressas diretamente do arquivo PDF.

   A variável _[!UICONTROL Print Shipping Label]_aparecerá somente depois que a transportadora gerar etiquetas para a entrega. Se o botão estiver ausente, clique em **[!UICONTROL Create Shipping Label]**. O botão é exibido depois que o Commerce recebe o rótulo da operadora.

### Método 2: imprimir etiquetas para várias ordens

1. No _Barra lateral de administração_, vá para uma das seguintes páginas e selecione os pedidos ou remessas para impressão:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Na grade, marque a caixa de seleção de cada pedido com etiquetas de remessa a serem impressas.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Na grade, marque a caixa de seleção de cada remessa com etiquetas a serem impressas.

1. Defina o **[!UICONTROL Actions]** controle para `Print Shipping Labels`.

1. Clique em **[!UICONTROL Submit]**.

Um conjunto completo de etiquetas de remessa é impresso para cada remessa relacionada às ordens selecionadas.

## Configurações de operadora necessárias

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Type] | Os tipos de pacote diferem por transportadora e método. O tipo de pacote padrão para cada operadora é selecionado inicialmente. O USPS não exige o tipo de pacote para remessas domésticas. |
| [!UICONTROL Customs Value] | (Remessas internacionais apenas) O valor declarado ou o preço de venda do conteúdo de uma remessa internacional. |
| [!UICONTROL Total Weight] | O peso total de todos os produtos adicionados ao pacote é calculado automaticamente. O valor também pode ser alterado manualmente e inserido como libras ou quilogramas. |
| [!UICONTROL Length, Width, Height] | (Opcional) As dimensões do pacote são usadas somente para pacotes personalizados. Você pode especificar as unidades de medida como polegadas ou centímetros.<br/><br/>**[!UICONTROL Not Required]**: nenhuma confirmação de entrega é enviada ao armazenamento pela transportadora da remessa.<br/><br/>**[!UICONTROL No Signature]**: uma confirmação de delivery sem a assinatura do recipient é enviada ao armazenamento pela transportadora.<br/><br/>**[!UICONTROL Signature Required]**: a transportadora da remessa obtém a assinatura do destinatário e fornece ao armazenamento uma cópia impressa.<br/><br/>**[!UICONTROL Direct]**: (Somente FedEx) O FedEx obtém uma assinatura de alguém no endereço de entrega. Se ninguém estiver disponível para assinar o pacote, a operadora tentará entregar o pacote em outro momento.<br/><br/>**[!UICONTROL Indirect]**: (Somente para deliveries residenciais FedEx) A FedEx obtém a assinatura de alguém (possivelmente um vizinho ou gerente de prédio) no endereço de delivery. O recipient pode deixar uma tag de porta FedEx assinada para autorizar que o pacote seja deixado sem que ninguém presente o assine.<br/><br/>**[!UICONTROL Contents]**: (Somente USPS) Selecione uma das seguintes descrições do pacote:<br/>- Presente<br/>- Documentos<br/>- Amostra comercial<br/>- Mercadorias de retorno<br/>- Mercadorias<br/>- Outro <br/><br/>**[!UICONTROL Explanation]**: (somente USPS) uma descrição detalhada do conteúdo do pacote.<br/><br/>**[!UICONTROL Adult Required]**: a transportadora obtém a assinatura de um destinatário adulto e fornece uma cópia impressa à loja. |

{style="table-layout:auto"}

## Criar pacotes

A variável _[!UICONTROL Create Packages]_é exibida quando você opta por criar um rótulo de entrega. Você pode começar a configurar o primeiro pacote imediatamente.

### Configurar um pacote

>[!NOTE]
>
>Se você selecionar o valor não padrão para a variável [!UICONTROL Type] ou optar por exigir uma confirmação da assinatura, o preço de uma entrega pode ser diferente daquele que você cobrou ao cliente.

1. Para exibir uma lista de produtos entregues e adicioná-los ao pacote, clique em **[!UICONTROL Add Products]**.

   - Especifique os produtos e as quantidades.

     A variável _[!UICONTROL Qty]_mostra a quantidade máxima disponível para adicionar. Para o primeiro pacote, o número é a quantidade total do produto a ser enviado.

   - Para adicionar os produtos ao pacote, clique em **[!UICONTROL Add Selected Product(s) to Package]**.

1. Para adicionar um pacote, clique em **[!UICONTROL Add Package]**.

   É possível adicionar vários pacotes e editá-los ao mesmo tempo.

1. Para excluir um pacote, clique em **[!UICONTROL Delete Package]**.

Depois que os produtos forem adicionados ao pacote, a quantidade não poderá ser editada diretamente.

### Aumentar a quantidade

1. Clique em **[!UICONTROL Add Selection]**.

1. Informe a quantidade adicional.

   O número é adicionado à quantidade anterior do produto na embalagem.

### Reduzir a quantidade

1. Excluir o produto do pacote.

1. Clique em **[!UICONTROL Add Selection]**.

1. Insira o novo valor menor.

### Gerar etiquetas de remessa

Depois de distribuir todos os produtos, o número total de pacotes que você usará é igual ao número do último pacote na lista. A variável _OK_ O botão estará desativado até que todos os itens entregues sejam distribuídos para os pacotes e todas as informações necessárias sejam concluídas.

Para gerar os rótulos, clique em **[!UICONTROL OK]**.

Você pode clicar em **[!UICONTROL Cancel]** para interromper o processo, se necessário. Os pacotes não são salvos e o processo de etiqueta de remessa é cancelado.

### Descrições dos campos

| Campo | Descrição |
|--- |--- |
| [!UICONTROL Type] | Especifica o tipo de um pacote. Selecione um dos valores predefinidos. Os tipos de pacote disponíveis são diferentes para cada transportadora. Quando a janela pop-up Criar pacotes é aberta, o pacote padrão da transportadora é exibido no campo Tipo. Se você selecionar um pacote que não foi criado por uma transportadora, será necessário inserir as dimensões do pacote. Para etiquetas de remessa criadas para remessas DHL, FedEx e UPS, o campo Tipo de Mercadorias é definido como `Merchandise`. Para USPS, o campo reflete o valor do _Conteúdo_ no campo _[!UICONTROL Create Packages]_janela. |
| [!UICONTROL Total Weight] | O peso total de um pacote. O campo é pré-preenchido com o peso total dos produtos em um pacote. A unidade de medida pode ser definida como libras ou quilogramas. |
| [!UICONTROL Length] | O comprimento de um pacote, número inteiro e números de ponto flutuante. O campo é ativado se o tipo de pacote personalizado for usado. A unidade de medida pode ser definida como polegadas ou centímetros. |
| [!UICONTROL Width] | A largura de um pacote, número inteiro e números de ponto flutuante. O campo é ativado se o tipo de pacote personalizado for usado. As unidades de medida podem ser especificadas por meio do menu suspenso ao lado do campo Height; selecione entre polegadas e centímetros. |
| [!UICONTROL Height] | A altura de um pacote, número inteiro e números de ponto flutuante. O campo é ativado se o tipo de pacote personalizado for usado. As unidades de medida podem ser especificadas por meio do menu suspenso ao lado do campo Height; selecione entre polegadas e centímetros. |
| [!UICONTROL Signature] | Define a confirmação da entrega. Opções:<br/><br/>**[!UICONTROL Not Required]**: nenhuma carta de confirmação de delivery é enviada a você.<br/><br/>**[!UICONTROL No Signature]**: uma carta de confirmação de delivery sem a assinatura de um recipient é enviada a você.<br/><br/>**[!UICONTROL Signature Required]**: a transportadora obterá a assinatura do destinatário e fornecerá a cópia impressa.<br/><br/>**[!UICONTROL Adult Required]**: A transportadora obtém a assinatura do destinatário adulto e fornece a cópia impressa.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx obtém uma assinatura de alguém no endereço de entrega e tenta novamente a entrega se ninguém estiver disponível para assinar o pacote.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: A FedEx obtém uma assinatura de uma das três formas a seguir:<br/>(1) de alguém no endereço de entrega; <br/>2) de um vizinho, gestor de edifícios ou outra pessoa no endereço; ou <br/>(3) o recipient pode deixar uma tag FedEx Door assinada autorizando o lançamento do pacote sem que ninguém esteja presente. Disponível somente para entregas residenciais. As opções podem variar um pouco de acordo com os diferentes métodos de envio. Para obter as informações mais recentes, consulte os recursos da transportadora. |
| [!UICONTROL Contents] | (Disponível somente para remessas USPS) Descrição do conteúdo do pacote. Opções: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Somente remessas USPS) Descrição detalhada do conteúdo do pacote. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
