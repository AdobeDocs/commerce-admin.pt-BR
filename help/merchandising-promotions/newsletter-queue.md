---
title: Filas de informativo
description: Saiba como gerenciar filas de informativos para enviar vários lotes de informativos.
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Filas de informativo

Para gerenciar a carga no servidor, boletins informativos com muitos assinantes são enviados em uma fila de vários lotes. Você pode verificar a fila de boletins informativos periodicamente para verificar o status e ver quantos foram processados. Quaisquer problemas que ocorrerem durante a transmissão aparecerão no _Problema no informativo_ relatório.

## Enviar informativo

1. No _Admin_ , acesse **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. Na grade, localize o [modelo de informativo](newsletter-template.md) que deve ser enviado e defina o **[!UICONTROL Action]** coluna para `Queue Newsletter`.

1. Para **[!UICONTROL Queue Date Start]**, selecione a data em que a transmissão começará a partir do calendário (![Ícone de calendário](../assets/icon-calendar.png)).

1. Para **[!UICONTROL Subscribers From]**, selecione cada exibição de loja a ser incluída na explosão do email.

1. Preencha as informações do cabeçalho do email:

   - Insira uma breve descrição do informativo para o **[!UICONTROL Subject]** linha do cabeçalho do email.

   - Insira o **[!UICONTROL Sender Name]**.

   - Para **[!UICONTROL Sender Email]**, insira o endereço de email do remetente.

     O nome e o endereço de email padrão do remetente são especificados na configuração.

     ![Informações da fila de informativos](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Se aplicável, insira uma nota no campo **[!UICONTROL Message]** acima das instruções para cancelar a inscrição.

   >[!NOTE]
   >
   >Não remova as instruções, que são exigidas por lei em muitas jurisdições.

1. Para aplicar estilos personalizados a um boletim informativo, adicione-os à **[!UICONTROL Newsletter Styles]** campo.

1. Quando terminar, clique em **[!UICONTROL Save and Resume]**.

   O informativo aparece na fila do aguardando para ser processado.

## Verificar se há problemas

No _Admin_ , acesse **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## Barra de botões

| Botão | Descrição |
|--- |--- |
| **[!UICONTROL Back]** | Retorna à página Modelos de informativo sem salvar as alterações. |
| **[!UICONTROL Reset]** | Redefine todas as alterações não salvas no formulário de informações da fila para seus valores anteriores. |
| **[!UICONTROL Preview Template]** | Abre uma página de visualização em uma guia separada. |
| **[!UICONTROL Save and Resume]** | Salva todas as alterações feitas. Coloca o informativo na fila. |
| **[!UICONTROL Save Newsletter]** | Salva todas as alterações feitas. Coloca o informativo na fila. |

{style="table-layout:auto"}

## Colunas

| Coluna | Descrição |
|--- |--- |
| [!UICONTROL ID] | Um identificador numérico exclusivo atribuído a cada modelo de boletim informativo. |
| [!UICONTROL Queue Start] | A data em que o informativo foi enviado. |
| [!UICONTROL Queue End] | A data em que o informativo terminou de ser enviado. |
| [!UICONTROL Subject] | Assunto do modelo do informativo. |
| [!UICONTROL Status] | Indica o status do correio do informativo. Valores possíveis: `Sent`, `Canceled`, `Not Sent`, `Sending`ou `Paused`. |
| [!UICONTROL Processed] | Indica quantos informativos foram enviados. |
| [!UICONTROL Recipients] | Indica quantos informativos foram recebidos pelos assinantes. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**: abre uma janela separada para visualizar o template. |

{style="table-layout:auto"}
