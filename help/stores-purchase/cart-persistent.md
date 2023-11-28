---
title: Persistência do carrinho
description: Saiba como um carrinho de compras persistente rastreia itens de carrinho não comprados e salva as informações da próxima visita do cliente.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 0%

---

# Persistência do carrinho

Um carrinho de compras persistente rastreia itens não comprados que são deixados no carrinho e salva as informações para a próxima visita do cliente. Clientes que são _lembrado_ podem ter o conteúdo de seus carrinhos de compras restaurado na próxima vez que visitarem sua loja.

Usar um carrinho de compras persistente pode ajudar a reduzir o número de carrinhos de compras abandonados e aumentar as vendas. É importante entender que o carrinho de compras persistente não expõe informações confidenciais da conta a qualquer momento. Enquanto o carrinho de compras persistente estiver em uso, os clientes registrados e os compradores convidados precisam fazer logon em uma conta existente ou criar uma conta antes de passar pelo checkout. Para os compradores convidados, um carrinho de compras persistente é a única maneira de recuperar informações de uma sessão anterior.

Para gerenciar o uso da persistência do carrinho para o seu site ou em exibições de loja específicas, você pode [configurar o carrinho de compras persistente](#configure-a-persistent-cart) configurações. Para obter mais informações sobre como essas configurações afetam a experiência do comprador em sua loja, consulte [Fluxo de trabalho persistente do carrinho](#persistent-cart-workflow).

>[!NOTE]
>
>Ao usar um carrinho persistente, é recomendável definir a duração da sessão do servidor e o cookie da sessão para um período longo. Consulte [Duração da sessão](../customers/customer-online-options.md) para obter mais informações.

Para usar o carrinho de compras persistentes, o navegador do cliente deve ser definido para permitir cookies. Há dois tipos de cookies usados para operações do carrinho de compras:

- **Cookie de sessão** - Existe um cookie de sessão de curto prazo durante uma única visita ao seu site e ele expira quando o cliente sai ou após um período definido.

- **Cookie persistente** - Um cookie persistente de longo prazo continua existindo após o final da sessão e salva um registro do conteúdo do carrinho de compras do cliente para referência futura.

## Fluxo de trabalho persistente do carrinho

Quando o carrinho de compras persistente for [habilitado](#configure-a-persistent-cart), o workflow depende de:

- Os valores de _Ativar Lembrar-me_ e _Limpar Persistência ao Fazer Logoff_ configurações
- A decisão do cliente de selecionar ou limpar o _Lembrar-me_ caixa de seleção
- Quando o cookie persistente é limpo

Quando um cookie persistente é aplicado, uma variável `Not Jane Smith?` será exibido no cabeçalho da página. Esse prompt oferece ao cliente a capacidade de encerrar a sessão persistente e começar a trabalhar como convidado ou fazer logon como um cliente diferente. O sistema retém um registro do conteúdo do carrinho de compras, mesmo que o cliente use dispositivos diferentes para comprar em sua loja. Por exemplo, um cliente pode adicionar um item ao carrinho de um laptop, adicionar mais itens de um dispositivo móvel e concluir o processo de finalização de um tablet.

Há um cookie independente e persistente separado para cada navegador. Se o cliente usar vários navegadores ao visitar sua loja durante uma única sessão contínua, as alterações feitas em um navegador serão refletidas em qualquer outro navegador após a atualização da página. Enquanto o carrinho de compras persistentes estiver habilitado, sua loja criará e manterá um cookie persistente separado para cada navegador usado por um cliente para fazer logon ou criar uma conta.

### Exemplo: uma sessão aberta em um computador compartilhado

Jane está terminando suas compras de fim de ano com uma sessão persistente. Ela adiciona um presente para John ao carrinho, e algo para sua mãe. Então ela vai para a cozinha fazer um lanche.

John senta-se no computador para fazer umas compras rápidas enquanto Jane está na cozinha. Sem notar o `Not Jane Smith?` na parte superior da página, ele encontra um belo presente para Jane e o adiciona ao carrinho. Quando ele vai para o check-out e faz logon como ele mesmo, ambos os itens no carrinho de Jane são adicionados ao carrinho. João está com tanta pressa que não nota os itens adicionais durante _Revisão do pedido_ e apresenta o pedido. O carrinho de Jane agora está vazio, e John comprou todos os presentes.

### Lembrar-me

Os clientes podem selecionar o _Lembrar-me_ caixa de seleção na página de logon para salvar o conteúdo de seus carrinhos de compras.

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
| **[!UICONTROL Enable Remember Me]** está definida como `No`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**tem qualquer valor.<br/><br/>A variável** Lembrar-me **não está disponível na página de logon e registro. | O cookie persistente não é usado. |
| **[!UICONTROL Enable Remember Me]** está definida como `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**tem qualquer valor.<br/><br/>** Lembrar-me **não está selecionado. | O cookie de sessão é aplicado como de costume; o cookie persistente não é usado. |
| **[!UICONTROL Enable Remember Me]** está definida como `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**está definida como `Yes`.<br/><br/>** Lembrar-me **está definida como `Yes`. | Quando um cliente faz logon, ambos os cookies são aplicados. Quando um cliente faz logoff, ambos os cookies são excluídos. Se um cliente não fizer logon, mas o cookie da sessão expirar, o cookie persistente ainda será usado. Além de fazer logout, o cookie persistente é excluído quando sua duração se esgota ou quando o cliente clica em `Not Jane Smith` link. |
| **[!UICONTROL Enable Remember Me]** está definida como `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**está definida como `No`.<br/><br/>** Lembrar-me **está definida como `Yes` | Quando um cliente faz logon, ambos os cookies são aplicados. Quando um cliente faz logoff, o cookie da sessão é excluído e a sessão persistente continua. O cookie persistente é excluído quando sua vida útil termina ou quando o cliente clica em `Not Jane Smith` link. |

{style="table-layout:auto"}

## Configurar um carrinho persistente

Durante a configuração de um carrinho de compras persistente, você pode especificar o tempo de vida dos cookies e quais opções deseja disponibilizar para várias atividades do cliente.

Para obter mais informações sobre como o workflow do cliente é determinado por essas configurações, consulte [Fluxo de trabalho persistente do carrinho](#persistent-cart-workflow).

>[!NOTE]
>
>Se o cookie da sessão expirar enquanto o cliente estiver conectado, o cookie persistente permanecerá ativo.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Persistent Shopping Cart]**.

1. Para ativar o carrinho de compras persistentes e exibir opções adicionais, defina **[!UICONTROL Enable Persistence]** para `Yes`.

   ![Ativação e configuração da persistência do carrinho](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   Para obter mais informações sobre cada uma dessas definições de configuração, consulte [_Referência de configuração_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >Se necessário, limpe a caixa de seleção **[!UICONTROL Use system value]** para modificar essas configurações.

1. Para **[!UICONTROL Persistence Lifetime (seconds)]**, insira o tempo, em segundos, durante o qual você deseja que o cookie persistente dure.

   O valor padrão de 31.536.000 segundos é igual a um ano. O tempo máximo permitido é de 100 anos.

1. Definir **[!UICONTROL Enable "Remember Me"]** a um dos seguintes:

   - `Yes` - Exibe o _Lembrar-me_ na página de Logon da sua loja, para que os clientes possam optar por salvar as informações do carrinho de compras.

   - `No` - A persistência ainda pode ser ativada, mas os clientes não têm a opção de escolher se desejam salvar suas informações.

1. Para pré-selecionar a variável _Lembrar-me_ caixa de seleção do cliente, definir **[!UICONTROL Remember Me Default Value]** para `Yes`.

   O cliente pode desmarcar essa opção se desejar.

1. Definir **[!UICONTROL Clear Persistence on Log Out]** a um dos seguintes:

   - `Yes` - O carrinho de compras é limpo quando um cliente registrado faz logoff.

   - `No` - O carrinho de compras é salvo quando um cliente registrado faz logoff.

   >[!NOTE]
   >
   >Se o cookie da sessão expirar enquanto o cliente ainda estiver conectado, o cookie persistente permanecerá em uso.

1. Definir **[!UICONTROL Persist Shopping Cart]** a um dos seguintes:

   - `Yes` - Se o cookie da sessão expirar, o cookie persistente será preservado. Se um comprador convidado fizer logon posteriormente ou criar uma conta, o carrinho de compras será restaurado.

   - `No` - O carrinho de compras não é preservado para convidados depois que o cookie da sessão expira.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Definir **[!UICONTROL Persist Wish List]** para determinar se o estado das listas de desejos do cliente é retido quando a sessão termina:

   - `Yes` - O conteúdo da lista de desejos é salvo quando a sessão termina.

   - `No` - A lista de desejos não é salva quando a sessão termina.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Definir **[!UICONTROL Persist Recently Ordered Items]** para determinar se o estado dos itens solicitados recentemente é retido quando a sessão termina:

   - `Yes` - O estado dos Itens solicitados recentemente é salvo quando a sessão termina.

   - `No` - O estado dos Itens solicitados recentemente não é salvo quando a sessão termina.

1. Definir **[!UICONTROL Persist Currently Compared Products]** para `Yes` ou `No`.

1. Definir **[!UICONTROL Persist Comparison History]** para `Yes` ou `No`.

1. Definir **[!UICONTROL Persist Recently Viewed Products]** para `Yes` ou `No`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Somente Adobe Commerce) Definir **[!UICONTROL Persist Customer Group Membership and Segmentation]** para determinar se o estado dos critérios de associação e segmentação de grupo do cliente é mantido quando a sessão termina:

   - `Yes` - O estado dos dados de associação de grupo e segmentação do cliente é salvo quando a sessão termina.

   - `No` - O estado da associação de grupo do cliente e os dados de segmentação não são salvos quando a sessão termina.

1. Clique em **[!UICONTROL Save Config]**.
