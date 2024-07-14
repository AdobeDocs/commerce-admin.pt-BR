---
title: Persistência do carrinho
description: Saiba como um carrinho de compras persistente rastreia itens de carrinho não comprados e salva as informações da próxima visita do cliente.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---

# Persistência do carrinho

Um carrinho de compras persistente rastreia itens não comprados que são deixados no carrinho e salva as informações para a próxima visita do cliente. Os clientes _lembrados_ podem ter o conteúdo de seus carrinhos de compras restaurado na próxima vez que visitarem sua loja.

Usar um carrinho de compras persistente pode ajudar a reduzir o número de carrinhos de compras abandonados e aumentar as vendas. É importante entender que o carrinho de compras persistente não expõe informações confidenciais da conta a qualquer momento. Enquanto o carrinho de compras persistente estiver em uso, os clientes registrados e os compradores convidados precisam fazer logon em uma conta existente ou criar uma conta antes de passar pelo checkout. Para os compradores convidados, um carrinho de compras persistente é a única maneira de recuperar informações de uma sessão anterior.

Para gerenciar o uso da persistência do carrinho de compras para o seu site ou em visualizações de loja específicas, você pode [definir configurações de persistência do carrinho de compras](#configure-a-persistent-cart). Para obter mais informações sobre como essas configurações afetam a experiência do comprador em sua vitrine, consulte [Fluxo de trabalho persistente do carrinho](#persistent-cart-workflow).

>[!NOTE]
>
>Ao usar um carrinho persistente, é recomendável definir a duração da sessão do servidor e o cookie da sessão para um período longo. Consulte [Duração da sessão](../customers/customer-online-options.md) para obter mais informações.

Para usar o carrinho de compras persistentes, o navegador do cliente deve ser definido para permitir cookies. Há dois tipos de cookies usados para operações do carrinho de compras:

- **Cookie de sessão** - Um cookie de sessão de curto prazo existe durante uma única visita ao seu site e expira quando o cliente sai ou após um período definido.

- **Cookie persistente** - Um cookie persistente de longo prazo continua existindo após o fim da sessão e salva um registro do conteúdo do carrinho de compras do cliente para referência futura.

## Fluxo de trabalho persistente do carrinho

Quando o carrinho de compras persistente está [habilitado](#configure-a-persistent-cart), o fluxo de trabalho depende:

- Os valores das configurações _Habilitar Lembrar-se de Mim_ e _Limpar Persistência no Logoff_
- A decisão do cliente de marcar ou desmarcar a caixa de seleção _Lembre-se de mim_
- Quando o cookie persistente é limpo

Quando um cookie persistente é aplicado, um link `Not Jane Smith?` é exibido no cabeçalho da página. Esse prompt oferece ao cliente a capacidade de encerrar a sessão persistente e começar a trabalhar como convidado ou fazer logon como um cliente diferente. O sistema retém um registro do conteúdo do carrinho de compras, mesmo que o cliente use dispositivos diferentes para comprar em sua loja. Por exemplo, um cliente pode adicionar um item ao carrinho de um laptop, adicionar mais itens de um dispositivo móvel e concluir o processo de finalização de um tablet.

Há um cookie independente e persistente separado para cada navegador. Se o cliente usar vários navegadores ao visitar sua loja durante uma única sessão contínua, as alterações feitas em um navegador serão refletidas em qualquer outro navegador após a atualização da página. Enquanto o carrinho de compras persistentes estiver habilitado, sua loja criará e manterá um cookie persistente separado para cada navegador usado por um cliente para fazer logon ou criar uma conta.

### Exemplo: uma sessão aberta em um computador compartilhado

Jane está terminando suas compras de fim de ano com uma sessão persistente. Ela adiciona um presente para John ao carrinho, e algo para sua mãe. Então ela vai para a cozinha fazer um lanche.

John senta-se no computador para fazer umas compras rápidas enquanto Jane está na cozinha. Sem notar o link `Not Jane Smith?` na parte superior da página, ele encontra um belo presente para Jane e o adiciona ao carrinho. Quando ele vai para o check-out e faz logon como ele mesmo, ambos os itens no carrinho de Jane são adicionados ao carrinho. John está com tanta pressa que não nota os itens adicionais durante a _Revisão do pedido_ e envia o pedido. O carrinho de Jane agora está vazio, e John comprou todos os presentes.

### Lembrar-me

Os clientes podem marcar a caixa de seleção _Lembre-se de mim_ na página de logon para salvar o conteúdo de seus carrinhos de compras.

| Lembra de Mim? | Resultado |
| ------------ |  ------ |
| Selecionado | Cria um cookie persistente e salva o conteúdo do carrinho de compras para a próxima sessão conectada do cliente. |
| Não selecionado | Não cria um cookie persistente e não salva as informações do carrinho na próxima sessão conectada do cliente. |

{style="table-layout:auto"}

### Continuar persistência no logout - não

| Ação | Resultado |
| ------ | ------ |
| Logon do cliente | Invoca o cookie persistente além do cookie de sessão, que já está em uso. |
| O cliente faz logoff | Exclui o cookie da sessão, mas o cookie persistente permanece em vigor. Na próxima vez que o cliente fizer logon, ele restaurará os itens do carrinho ou os adicionará a quaisquer novos itens colocados no carrinho. |
| O cliente não faz logoff e o cookie de sessão expira | O cookie persistente permanece em vigor. |

{style="table-layout:auto"}

### Limpar persistência no logout

| Ação | Resultado |
| ------ | ------ |
| Logon do cliente | Invoca o cookie persistente além do cookie de sessão, que já está em uso. |
| O cliente faz logoff | Exclui ambos os cookies. |
| O cliente não faz logoff, mas o cookie da sessão expira | O cookie persistente permanece em vigor. |

{style="table-layout:auto"}

## Configurações e efeitos persistentes do carrinho

| Configurações | Efeito |
|----------|--------|
| **[!UICONTROL Enable Remember Me]** está definido como `No`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**tem qualquer valor.<br/><br/>A caixa de seleção** Lembre-se de mim **não está disponível na página de logon e registro. | O cookie persistente não é usado. |
| **[!UICONTROL Enable Remember Me]** está definido como `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**tem qualquer valor.<br/><br/>** Lembre-se de Mim **não está selecionado. | O cookie de sessão é aplicado como de costume; o cookie persistente não é usado. |
| **[!UICONTROL Enable Remember Me]** está definido como `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**está definido como `Yes`.<br/><br/>** Lembre-se de Mim **está definido como `Yes`. | Quando um cliente faz logon, ambos os cookies são aplicados. Quando um cliente faz logoff, ambos os cookies são excluídos. Se um cliente não fizer logon, mas o cookie da sessão expirar, o cookie persistente ainda será usado. Além de fazer logoff, o cookie persistente é excluído quando sua duração se esgota ou quando o cliente clica no link `Not Jane Smith`. |
| **[!UICONTROL Enable Remember Me]** está definido como `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**está definido como `No`.<br/><br/>** Lembre-se de Mim **está definido como `Yes` | Quando um cliente faz logon, ambos os cookies são aplicados. Quando um cliente faz logoff, o cookie da sessão é excluído e a sessão persistente continua. O cookie persistente é excluído quando sua vida útil termina ou quando o cliente clica no link `Not Jane Smith`. |

{style="table-layout:auto"}

## Configurar um carrinho persistente

Durante a configuração de um carrinho de compras persistente, você pode especificar o tempo de vida dos cookies e quais opções deseja disponibilizar para várias atividades do cliente.

Para obter mais informações sobre como o fluxo de trabalho do cliente é determinado por essas configurações, consulte [Fluxo de trabalho persistente do carrinho](#persistent-cart-workflow).

>[!NOTE]
>
>Se o cookie da sessão expirar enquanto o cliente estiver conectado, o cookie persistente permanecerá ativo.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Persistent Shopping Cart]**.

1. Para habilitar o carrinho de compras persistentes e exibir opções adicionais, defina **[!UICONTROL Enable Persistence]** como `Yes`.

   ![Habilitando e configurando a persistência do carrinho](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   Para obter mais informações sobre cada uma dessas definições de configuração, consulte a [_Referência de Configuração_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >Se necessário, desmarque a caixa de seleção **[!UICONTROL Use system value]** para modificar essas configurações.

1. Para **[!UICONTROL Persistence Lifetime (seconds)]**, insira o período, em segundos, durante o qual você deseja que o cookie persistente dure.

   O valor padrão de 31.536.000 segundos é igual a um ano. O tempo máximo permitido é de 100 anos.

1. Defina **[!UICONTROL Enable "Remember Me"]** como um dos seguintes:

   - `Yes` - Exibe a caixa de seleção _Lembrar-se de mim_ na página Logon da sua loja, para que os clientes possam optar por salvar as informações do carrinho de compras.

   - `No` - A persistência ainda pode ser habilitada, mas os clientes não têm a opção de escolher se desejam salvar suas informações.

1. Para pré-marcar a caixa de seleção _Lembre-se de mim_ para o cliente, defina **[!UICONTROL Remember Me Default Value]** como `Yes`.

   O cliente pode desmarcar essa opção se desejar.

1. Defina **[!UICONTROL Clear Persistence on Log Out]** como um dos seguintes:

   - `Yes` - O carrinho de compras é limpo quando um cliente registrado faz logoff.

   - `No` - O carrinho de compras é salvo quando um cliente registrado faz logoff.

   >[!NOTE]
   >
   >Se o cookie da sessão expirar enquanto o cliente ainda estiver conectado, o cookie persistente permanecerá em uso.

1. Defina **[!UICONTROL Persist Shopping Cart]** como um dos seguintes:

   - `Yes` - Se o cookie da sessão expirar, o cookie persistente será preservado. Se um comprador convidado fizer logon posteriormente ou criar uma conta, o carrinho de compras será restaurado.

   - `No` - O carrinho de compras não é preservado para convidados depois que o cookie da sessão expira.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Defina **[!UICONTROL Persist Wish List]** para determinar se o estado das listas de desejos do cliente é mantido quando a sessão termina:

   - `Yes` - O conteúdo da lista de desejos é salvo quando a sessão termina.

   - `No` - A lista de desejos não é salva quando a sessão termina.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Defina **[!UICONTROL Persist Recently Ordered Items]** para determinar se o estado dos itens encomendados recentemente é mantido quando a sessão termina:

   - `Yes` - O estado dos Itens Recentemente Solicitados é salvo quando a sessão termina.

   - `No` - O estado dos Itens Recentemente Solicitados não é salvo quando a sessão termina.

1. Defina **[!UICONTROL Persist Currently Compared Products]** como `Yes` ou `No`.

1. Defina **[!UICONTROL Persist Comparison History]** como `Yes` ou `No`.

1. Defina **[!UICONTROL Persist Recently Viewed Products]** como `Yes` ou `No`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (somente Adobe Commerce) Defina **[!UICONTROL Persist Customer Group Membership and Segmentation]** para determinar se o estado dos critérios de associação de grupo e segmentação do cliente será mantido quando a sessão terminar:

   - `Yes` - O estado dos dados de segmentação e associação de grupo do cliente é salvo quando a sessão termina.

   - `No` - O estado dos dados de segmentação e associação de grupo do cliente não é salvo quando a sessão termina.

1. Clique em **[!UICONTROL Save Config]**.
