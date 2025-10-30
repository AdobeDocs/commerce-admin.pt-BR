---
title: Configuração da transportadora da remessa
description: Saiba mais sobre o suporte para contas de remessa comercial disponível para sua loja.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Configuração da transportadora da remessa

Se você tiver uma conta comercial com uma operadora compatível, poderá oferecer aos clientes a conveniência de escolher essa operadora durante o check-out. As taxas são baixadas automaticamente para que você não precise pesquisar as informações.

>[!NOTE]
>
>Consulte o [Commerce Marketplace](../getting-started/commerce-marketplace.md) para obter serviços de envio adicionais para a sua instalação do Commerce.

Antes de oferecer aos clientes uma seleção de transportadoras, você deve concluir as seguintes etapas:

- Defina as [configurações de envio](shipping-settings.md) para estabelecer o ponto de origem do seu armazenamento.

- Defina as configurações para cada serviço de operadora que deseja oferecer.

   - [**UPS**](ups.md) - O United Parcel Service (UPS) oferece serviços de envio doméstico e internacional por terra e ar para mais de 220 países.
   - [**USPS**](usps.md) - O Serviço Postal dos Estados Unidos (USPS) é o serviço postal independente do governo dos Estados Unidos. O USPS oferece serviços de transporte nacional e internacional por terra e ar.
   - [**FedEx**](fedex.md) - A FedEx oferece serviços de envio doméstico e internacional por terra e ar para mais de 220 países.
   - [**DHL**](dhl.md) - A DHL oferece serviços internacionais integrados e soluções personalizadas voltadas para o cliente, para gerenciamento e transporte de cartas, mercadorias e informações.

## Peso dimensional

O peso dimensional, às vezes chamado de peso volumétrico, é uma prática comum do setor que baseia o preço do transporte em uma combinação de peso e volume do pacote. Em termos simples, o peso dimensional determina a taxa de envio com base na quantidade de espaço que um pacote ocupa na área de carga da transportadora. O peso dimensional é normalmente usado quando um pacote é relativamente leve em comparação ao seu volume.

Todas as principais transportadoras aplicam peso dimensional a algumas entregas. No entanto, a maneira como a precificação de peso dimensional é aplicada varia de uma transportadora para outra. Se sua empresa tem um alto volume de remessas, mesmo uma pequena diferença no preço de envio pode se traduzir em milhares de dólares ao longo de um ano.

## Configuração

As opções de configuração variam para cada operadora. No entanto, todos exigem as seguintes etapas:

1. Abra uma conta de remessa com a transportadora.

1. Insira o número da conta ou a ID de usuário e o URL do gateway do sistema na configuração da loja.

### Descontinuação da API de ferramentas da Web do USPS

As versões 2.4.6, 2.4.7 e 2.4.8 do Adobe Commerce usam as APIs de ferramentas herdadas da Web para integração de envio pronta para uso com o USPS. A USPS introduziu as APIs USPS, uma plataforma baseada em REST para substituir as APIs herdadas das ferramentas da Web.

Em 25 de janeiro de 2026, o USPS desativará as APIs de ferramentas herdadas da Web. Após essa data, todas as solicitações para as APIs de ferramentas da Web falharão.

Para evitar a interrupção dos serviços de envio do USPS, execute as seguintes ações antes de 25 de janeiro de 2026:

- Aplique o [patch de qualidade da migração da API REST do USPS](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/usps-rest-api-migration-patch.html)&#x200B;(AC-1520) para adicionar suporte à integração com as APIs REST do USPS.

- Atualize a configuração do Commerce USPS para usar as APIs REST:

   - [Configuração da Transportadora de Remessa USPS](usps.md)

   - [Configuração da etiqueta de remessa](shipping-label-create.md)

