---
title: Etiquetas de remessa
description: Saiba mais sobre o fluxo de trabalho de etiquetas de remessa para remessas regulares e produtos com autorização para devolução de mercadoria.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
TQID: https://experienceleague.adobe.com/Cjf9-372TRGIfWXpWR20OUII5XorPdfO1qgG-b2yPYI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 0%

---

# Etiquetas de remessa

O Commerce inclui um alto nível de integração com as principais transportadoras, o que dá a você acesso aos sistemas de transporte de transportadoras para rastrear pedidos, criar etiquetas de remessa e muito mais. As etiquetas de remessa podem ser criadas para remessas regulares e produtos com autorização para devolução de mercadoria. Além das informações fornecidas pela transportadora, a etiqueta também inclui o número do pedido Commerce, o número do pacote e a quantidade total de pacotes para a remessa.

![Rótulo de Remessa de Prioridade USPS](./assets/shipping-usps-priority-label.png){width="300"}

- [Configurar etiquetas de remessa](shipping-label-configure.md)
- [Criar etiquetas e pacotes de remessa](shipping-label-create.md)

## Fluxo de trabalho de etiqueta de remessa

As etiquetas de remessa podem ser produzidas no momento em que a remessa é criada ou posteriormente. As etiquetas de remessa são armazenadas no formato PDF e são baixadas no computador.

### Etapa 1: o comerciante envia a solicitação de etiqueta de remessa

O comerciante/gerente da loja conclui as informações necessárias para gerar as etiquetas e envia a solicitação.

### Etapa 2: Solicitação enviada à transportadora

A Commerce entra em contato com a transportadora e cria um pedido no sistema da transportadora. Uma ordem separada é criada para cada pacote enviado.

### Etapa 3: a operadora envia o rótulo e o número de rastreamento

A transportadora envia o rótulo da remessa e o número de rastreamento da remessa.

- Uma única entrega com vários pacotes recebe várias etiquetas de entrega.

- Se você gerar os mesmos rótulos de remessa várias vezes, os números de rastreamento originais serão preservados.

- Para produtos devolvidos com números RMA, os números de rastreamento antigos são substituídos por novos.

### Etapa 4: o comerciante baixa e imprime a etiqueta

Depois que a etiqueta de remessa é gerada, a nova remessa é salva e a etiqueta pode ser impressa. Se a etiqueta da entrega não puder ser criada devido a problemas com a conexão ou por qualquer outro motivo, a entrega não será criada. Dependendo das configurações do navegador, o arquivo PDF pode ser aberto e impresso. Cada rótulo aparece em uma página separada na PDF.
