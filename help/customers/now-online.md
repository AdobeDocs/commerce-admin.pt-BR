---
title: Clientes agora online
description: A opção _Agora Online_ no menu [!UICONTROL Customers ] lista todos os clientes e visitantes que estão online na sua loja.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
TQID: https://experienceleague.adobe.com/jtyDgy3jFmn0XymAYcpc2AOLLWSTDw-3OGkvG9a1SDc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 0%

---

# Clientes agora online

A opção **[!UICONTROL Now Online]** no menu [!DNL Customers] lista todos os clientes e visitantes que estão online na sua loja. O intervalo de tempo em que os clientes são mostrados como online no momento é definido na configuração e determina por quanto tempo a atividade [!DNL Customer's] fica visível do Administrador. Por padrão, o intervalo é de 15 minutos. A sessão termina se o teclado não for usado durante esse período, e os clientes deverão entrar em suas contas novamente para continuar comprando. É importante observar que o conteúdo dos carrinhos é salvo para acesso posterior.

![Clientes Online](assets/customers-now-online.png){width="700" zoomable="yes"}

O status online dos clientes é atualizado somente após o logon, o registro ou qualquer outro evento que mude o estado do cliente. Ele inclui eventos relacionados ao carrinho, como adicionar, remover e modificar produtos.

>[!NOTE]
>
>Visitas a páginas por si só não atualizam o status online do cliente. Para coletar essas informações, é recomendável [configurar o Google Analytics](../merchandising-promotions/google-analytics.md) (sozinho ou com o [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) ou usar outro software de análise com o Adobe Commerce.

## Ver todos os clientes atualmente online

Na barra lateral _Admin_, vá para **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Para obter informações sobre como ajudar um cliente online a concluir uma compra, consulte [Assistência para compras](../stores-purchase/introduction.md#shopping-assistance).

## Configurar o intervalo de tempo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Customers]** e escolha **[!UICONTROL Customer Configuration]**.

1. Expanda a seção **[!UICONTROL Online Customers Options]** e faça o seguinte:

   ![Opções de Cliente Online](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Para **[!UICONTROL Online Minutes Interval]**, insira o número de minutos para que a sessão do cliente fique visível do Administrador. Deixe o campo vazio para aceitar o intervalo padrão de 15 minutos.

   - Para **[!UICONTROL Customer Data Lifetime]**, insira o número de minutos antes que quaisquer dados não salvos inseridos pelo cliente expirem.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Descrições da coluna

| Coluna | Descrição |
| --- | --- |
| **[!UICONTROL ID]** | A ID de um cliente registrado. |
| **[!UICONTROL First Name]** | O nome de um cliente registrado. |
| **[!UICONTROL Last Name]** | O sobrenome de um cliente registrado. |
| **[!UICONTROL Email]** | O endereço de email de um cliente registrado. |
| **[!UICONTROL Last Activity]** | A data e a hora da última atividade do cliente em sua loja. |
| **[!UICONTROL Type]** | Opções: `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | O último URL que o cliente visitou. |
| **[!UICONTROL Company]** | O nome da empresa à qual o usuário pertence. |

{style="table-layout:auto"}
