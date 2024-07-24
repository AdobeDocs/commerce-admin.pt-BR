---
title: Persistência do carrinho
description: Saiba como um carrinho de compras persistente rastreia itens de carrinho não comprados e salva as informações da próxima visita do cliente.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: ea3aae3fce7f5e18155138b2bb9e7df0b3831fdd
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---

# Persistência do carrinho

Um carrinho de compras persistente rastreia itens não comprados no carrinho e salva as informações. Esse processo garante que o conteúdo do carrinho de compras permaneça acessível quando a sessão conectada expirar.

Se um cliente for _lembrado_, o conteúdo de seu carrinho de compras permanecerá acessível no dispositivo atual quando a sessão conectada expirar. Depois que a sessão expira, o carrinho de compras do cliente é acessado usando a sessão persistente do carrinho. Se o mesmo cliente fizer logon em outro dispositivo ou navegador, adicionar algo ao carrinho de compras e retornar ao dispositivo com uma sessão persistente ativa, o carrinho de compras será atualizado com os itens adicionados.

Usar um carrinho de compras persistente pode reduzir o número de carrinhos de compras abandonados e aumentar as vendas. O carrinho de compras persistente **não** expõe informações confidenciais da conta a qualquer momento.

Para gerenciar o uso da persistência do carrinho de compras para o seu site ou em visualizações de loja específicas, você pode [definir configurações de persistência do carrinho de compras](#configure-a-persistent-cart). Para obter mais informações sobre como essas configurações afetam a experiência do comprador em sua vitrine, consulte [Fluxo de trabalho persistente do carrinho](#persistent-cart-workflow).

>[!NOTE]
>
>O recurso de carrinho de compras persistente está disponível somente para clientes registrados e conectados. Os compradores convidados não podem usar o recurso de carrinho de compras persistente.

## Fluxo de trabalho persistente do carrinho

Quando o carrinho de compras persistente está [habilitado](#configure-a-persistent-cart), o fluxo de trabalho depende:

- Os valores das configurações _[!UICONTROL Enable Remember Me]_e_[!UICONTROL Clear Persistence on Log Out]_
- A decisão do cliente de marcar ou desmarcar a caixa de seleção _[!UICONTROL Remember Me]_
- Quando o cookie persistente é limpo

Quando a sessão do cliente expirar, um link `Not Jane Smith?` será exibido no cabeçalho da página sob as seguintes condições:
- o cliente conectado selecionou a opção _[!UICONTROL Remember Me]_e um cookie persistente foi aplicado
- o cliente faz logoff quando o sistema está configurado com _[!UICONTROL Clear Persistence on Sign Out]_definido como `No`.

O sistema retém um registro do conteúdo do carrinho de compras no dispositivo atual, mesmo se a sessão conectada expirar. O link `Not Jane Smith?` permite que o cliente encerre a sessão persistente e comece a trabalhar como convidado, ou faça logon como um cliente diferente ou igual.

Se o cliente marcou a caixa de seleção _[!UICONTROL Remember Me]_ao fazer logon, seu armazenamento cria e mantém um cookie persistente separado. Este cookie ajuda a manter o carrinho de compras do cliente acessível, mesmo depois que ele fecha o navegador ou navega para um site diferente e sua sessão conectada expira.

Se esse mesmo cliente visitar sua loja usando vários navegadores enquanto estiver conectado ou enquanto uma sessão persistente estiver ativa, as alterações que o cliente fizer no conteúdo do carrinho de compras em um navegador serão refletidas em outros navegadores quando a página for atualizada.

>[!NOTE]
>
>Para garantir a sincronização do carrinho em vários dispositivos ou navegadores, os clientes devem fazer logon em cada novo dispositivo que usam para comprar. Para clientes conectados, o conteúdo do carrinho de compras é sincronizado em vários dispositivos e navegadores, desde que eles estejam conectados na mesma conta, independentemente da configuração de Carrinho persistente.

### Comportamento da caixa de seleção &quot;Lembrar-se de mim&quot;

Os clientes podem marcar a caixa de seleção _[!UICONTROL Remember Me]_na página de logon ou ao criar uma nova conta para manter o conteúdo do carrinho de compras acessível no dispositivo atual quando a sessão conectada expirar.

| Lembra de Mim? | Resultado |
| ------------ |  ------ |
| Selecionado | Cria um cookie persistente e mantém o conteúdo do carrinho de compras acessível no dispositivo atual quando a sessão de logon do cliente expira. |
| Não selecionado | Não cria um cookie persistente e não mantém o conteúdo do carrinho de compras acessível no dispositivo atual quando a sessão de logon expira. Observe que o conteúdo do carrinho de compras ainda é salvo na conta do cliente e recarregado na próxima vez que o cliente fizer logon. |

{style="table-layout:auto"}

### Limpar Persistência no Comportamento de Saída

Quando o cliente faz logon ou se registra com a opção _Lembre-se de mim_ selecionada, a configuração da opção _Limpar persistência ao sair_ determina o comportamento persistente do carrinho.

|  | Limpar Persistência na Saída definida como Sim | Limpar Persistência ao Sair definida como Não |
| ------ | ------ | ------ |
| _Lembrado_ cliente faz logoff | Exclui cookies persistentes e de sessão para que o conteúdo do carrinho de compras desapareça no dispositivo atual até que o mesmo cliente faça logon novamente. | Exclui o cookie da sessão, mas o cookie persistente permanece em vigor. O conteúdo do carrinho de compras permanece acessível no dispositivo atual. |
| _Lembrado_ cliente não faz logoff, mas o cookie da sessão expira | O cookie persistente permanece em vigor e o conteúdo do carrinho de compras é acessível no dispositivo atual. | O cookie persistente permanece em vigor e o conteúdo do carrinho de compras é acessível no dispositivo atual. |

### Exemplo de uma sessão aberta em um computador compartilhado

Jane está terminando suas compras de fim de ano como um _Lembrado_ cliente conectado. Ela adiciona um presente para John ao carrinho, e algo para sua mãe. Em seguida, ela vai à cozinha para um lanche e sua sessão de login expira.

John senta-se no computador para fazer umas compras rápidas enquanto Jane está na cozinha. Sem notar o link `Not Jane Smith?` na parte superior da página, John encontra um belo presente para Jane e o adiciona ao carrinho. Ao fazer o check-out, ele percebe que os endereços de envio e de cobrança estão pré-preenchidos e acha que está conectado. John está com tanta pressa que não nota os itens adicionais durante a _Revisão do pedido_ e envia o pedido. O carrinho de Jane agora está vazio, e John comprou todos os presentes.

## Configurar um carrinho persistente

Durante a configuração de um carrinho de compras persistente, você pode especificar o tempo de vida dos cookies e quais opções deseja disponibilizar para várias atividades do cliente.

Para usar o carrinho de compras persistentes, o navegador do cliente deve ser definido para permitir cookies. Há dois tipos de cookies usados para operações do carrinho de compras:

- **Cookie de sessão** - Existe um cookie de sessão de curto prazo durante uma única visita ao seu site. Este cookie expira quando o cliente faz logoff ou quando a sessão expira.

- **Cookie Persistente** - Um cookie persistente de longo prazo continua a existir após o término da sessão conectada. Esse cookie garante que o conteúdo do carrinho de compras de um cliente permaneça acessível quando o cliente fizer logoff ou a sessão expirar.

Para obter mais informações sobre como essas configurações afetam o fluxo de trabalho do cliente, consulte [Fluxo de trabalho persistente do carrinho](#persistent-cart-workflow).

{{$include /help/_includes/persistent-cart-configuration.md}}
