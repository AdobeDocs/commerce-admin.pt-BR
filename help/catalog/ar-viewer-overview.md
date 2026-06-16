---
title: '[!DNL AR Viewer] para Adobe Commerce'
description: Saiba como o [!DNL AR Viewer] pode beneficiar sua instância do Adobe Commerce e como integrar e configurar a extensão com êxito.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
TQID: https://experienceleague.adobe.com/ofebqdDS0exPDKJMLB-mpE0eVjRKT5ck91Fm2-7CVjA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a09a5a04-e30b-4d55-b031-38e6f5ec86dbid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# [!DNL AR Viewer] para Adobe Commerce

A realidade aumentada (RA) descreve as experiências do usuário que adicionam elementos 2D ou 3D à visualização ao vivo da câmera de um dispositivo de forma que esses elementos pareçam habitar o mundo real.

A extensão do [!DNL AR Viewer] para Adobe Commerce capacita uma experiência perfeita projetada para exibir gráficos 3D renderizados para o usuário.

As informações neste guia fornecem uma visão geral da experiência de integração do [!DNL AR Viewer] no Adobe Commerce e de como o [!DNL AR Viewer] beneficia o usuário, bem como as práticas recomendadas para seguir essa jornada.

Desenvolvido pela Pixar, o [Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} é o primeiro software de código aberto que pode trocar cenas 3D de forma robusta e escalonável, podendo ser composto por vários ativos, fontes e animações diferentes, além de promover fluxos de trabalho altamente colaborativos. Este USD é usado em `.USDZ` arquivos. Este arquivo `.USDZ` fornece conteúdo de AR e 3D para os dispositivos do usuário.

>[!NOTE]
>
> O [!DNL AR Viewer] dá suporte apenas a `.USDZ` arquivos.

## [!DNL AR Viewer] requisitos

O [!DNL AR Viewer] é compatível com o [!DNL Magento Open Source] e o Adobe Commerce. Consulte a [Política de Ciclo de Vida](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} para obter mais informações sobre as versões com suporte.

Consulte [Instalar a [!DNL AR Viewer] extensão](../catalog/ar-viewer-setup.md) para obter mais informações.

Para usar [!DNL AR Viewer], você deve ter o seguinte disponível para sua instância:

* PHP 8.1.0
* Adobe Commerce versão 2.4.4 e mais recente
* Magento Open Source (CE) versão 2.4.x

## Limitações de compatibilidade

[!DNL AR Viewer] limitações de compatibilidade existentes:

* Somente `.USDZ`: este recurso dá suporte apenas a `.USDZ` arquivos.
* `qr-code`: Exige `endroid/qr-code` versão 4.5.
* `Catalog module`: Exige `magento/module-catalog` versão 104.0.0.
