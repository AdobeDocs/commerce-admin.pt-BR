---
title: Tempo de vida da sessão do cliente
description: O tempo de vida da sessão do cliente determina o tempo de vida de uma sessão de compras do cliente.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Tempo de vida da sessão do cliente

O tempo de vida de uma sessão de compras do cliente é determinado por vários fatores, incluindo a duração da sessão do servidor, o uso de um [carrinho persistente](../stores-purchase/cart-persistent.md)e a duração das informações armazenadas no navegador. Embora estejam relacionados à mesma experiência do cliente, eles são processos separados com diferentes eventos de expiração e durações.

| Processo | Descrição |
| --- | --- |
| Session | Informações armazenadas no servidor, como o conteúdo do carrinho de compras. Se a sessão do servidor expirar antes do cookie expirar, os clientes podem perder o conteúdo do carrinho e reduzir o risco de segurança. |
| Cookie da sessão | Informações armazenadas no navegador como um número ou uma sequência de caracteres. Se o cookie da sessão expirar antes da sessão do servidor, o cliente será desconectado. O cookie de sessão é excluído quando o cliente fecha a janela do navegador. Por padrão, a duração do cookie é definida como 3600 segundos ou uma hora. Se não houver atividade do teclado durante esse tempo, a sessão atual terminará e os clientes deverão fazer logon novamente em suas contas para continuar comprando. |

{style="table-layout:auto"}

Se [Carrinho persistente](../stores-purchase/cart-persistent.md) estiver ativado, o conteúdo do carrinho será salvo na próxima vez que os clientes entrarem em suas contas. Ao usar um carrinho persistente, é recomendável definir a duração da sessão do servidor e o cookie da sessão para um período longo.

No servidor, a duração da sessão é controlada pelo `php.ini` arquivo e várias variáveis. Atualmente, o Adobe Commerce não tem uma definição de configuração de Administrador que controle a duração da sessão do servidor.

## Configurar o tempo de vida do cookie

1. No _Admin_ barra lateral, vá para [!UICONTROL **Lojas**] > _[!UICONTROL Settings]_>[!UICONTROL **Configuração**].

1. Se você tiver vários armazenamentos, defina a variável **[!UICONTROL Store View]** no canto superior direito, escolha a loja onde a configuração se aplica.

1. No painel esquerdo, em **[!UICONTROL General]**, escolha **[!UICONTROL Web]**.

1. Expanda a **[!UICONTROL Default Cookie Settings]** seção.

   ![Configurações de cookie padrão](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Para alterar o padrão, desmarque a caixa **[!UICONTROL Use system value]** e insira o novo valor em segundos.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar _Lembrar-me_ funcionalidade

Para facilitar o logon, a variável **[!UICONTROL Remember Me]** permite que os titulares de contas de usuários evitem inserir suas credenciais sempre que entrarem na loja. Por motivos de segurança, o recurso de persistência é desativado por padrão.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Persistent Shopping Cart]**.

1. Expanda a **[!UICONTROL General Options]** seção.

1. Para **[!UICONTROL Enable Persistence]**, defina como `Yes`. (Limpe a caixa **[!UICONTROL Use system value]** para permitir a alteração da configuração padrão.)

1. Para **[!UICONTROL Enable "Remember Me"]**, defina como `Yes` ou `No` de acordo com suas necessidades.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
