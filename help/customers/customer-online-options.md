---
title: Tempo de vida da sessão do cliente
description: O tempo de vida da sessão do cliente determina o tempo de vida de uma sessão de compras do cliente.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/cJ8Rv5zMkTvZMfrl-nj-3xy3guSPDlxa7HZ-ZG7kLFw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Tempo de vida da sessão do cliente

A duração de uma sessão de compras do cliente é determinada por vários fatores, incluindo a duração da sessão do servidor, o uso de um [carrinho persistente](../stores-purchase/cart-persistent.md) e a duração das informações armazenadas no navegador. Embora estejam relacionados à mesma experiência do cliente, eles são processos separados com diferentes eventos de expiração e durações.

| Processo | Descrição |
| --- | --- |
| Session | Informações armazenadas no servidor, como o conteúdo do carrinho de compras. Se a sessão do servidor expirar antes do cookie expirar, os clientes podem perder o conteúdo do carrinho e reduzir o risco de segurança. |
| Cookie da sessão | Informações armazenadas no navegador como um número ou uma sequência de caracteres. Se o cookie da sessão expirar antes da sessão do servidor, o cliente será desconectado. O cookie de sessão é excluído quando o cliente fecha a janela do navegador. Por padrão, a duração do cookie é definida como 3600 segundos ou uma hora. Se não houver atividade do teclado durante esse tempo, a sessão atual terminará e os clientes deverão fazer logon novamente em suas contas para continuar comprando. |

{style="table-layout:auto"}

Se o [Carrinho persistente](../stores-purchase/cart-persistent.md) estiver habilitado, o conteúdo do carrinho será salvo para a próxima vez que os clientes entrarem em suas contas. Ao usar um carrinho persistente, é recomendável definir a duração da sessão do servidor e o cookie da sessão para um período longo.

No servidor, a duração da sessão é controlada pelo arquivo `php.ini` e por várias variáveis. Atualmente, o Adobe Commerce não tem uma definição de configuração de Administrador que controle a duração da sessão do servidor.

## Configurar o tempo de vida do cookie

1. Na barra lateral _Admin_, vá para [!UICONTROL **Lojas**] > _[!UICONTROL Settings]_>[!UICONTROL **Configuração**].

1. Se você tiver vários armazenamentos, defina o seletor de **[!UICONTROL Store View]** no canto superior direito para o armazenamento onde a configuração se aplica.

1. No painel esquerdo, em **[!UICONTROL General]**, escolha **[!UICONTROL Web]**.

1. Expanda a seção **[!UICONTROL Default Cookie Settings]**.

   ![Configurações de cookie padrão](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Para alterar o padrão, desmarque a caixa de seleção **[!UICONTROL Use system value]** e insira o novo valor em segundos.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar a funcionalidade _Lembre-se de Mim_

Para facilitar o logon, a função **[!UICONTROL Remember Me]** permite que os titulares de contas de usuários evitem inserir suas credenciais sempre que entrarem na loja. Por motivos de segurança, o recurso de persistência é desativado por padrão.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Persistent Shopping Cart]**.

1. Expanda a seção **[!UICONTROL General Options]**.

1. Para **[!UICONTROL Enable Persistence]**, defina como `Yes`. (Desmarque a caixa de seleção **[!UICONTROL Use system value]** para permitir a alteração da configuração padrão.)

1. Para **[!UICONTROL Enable "Remember Me"]**, defina como `Yes` ou `No` de acordo com suas necessidades.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
