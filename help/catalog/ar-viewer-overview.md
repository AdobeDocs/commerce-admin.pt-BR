---
title: '[!DNL AR Viewer] para Adobe Commerce'
description: Saiba como o [!DNL AR Viewer] pode beneficiar sua instância do Adobe Commerce e como integrar e configurar a extensão com êxito.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# [!DNL AR Viewer] para Adobe Commerce

A realidade aumentada (RA) descreve as experiências do usuário que adicionam elementos 2D ou 3D à visualização ao vivo da câmera de um dispositivo de forma que esses elementos pareçam habitar o mundo real.

A extensão do [!DNL AR Viewer] para Adobe Commerce capacita uma experiência perfeita projetada para exibir gráficos 3D renderizados para o usuário.

As informações neste guia fornecem uma visão geral da experiência de integração do [!DNL AR Viewer] no Adobe Commerce e de como o [!DNL AR Viewer] beneficia o usuário, bem como as práticas recomendadas para seguir essa jornada.

Desenvolvido pela Pixar, o [Universal Scene Description (USD)](https://www.pixar.com/usd){target=_blank} é o primeiro software de código aberto que pode trocar cenas 3D de forma robusta e escalonável, que podem ser compostas por vários ativos, fontes e animações diferentes, ao mesmo tempo em que promove fluxos de trabalho altamente colaborativos. Este USD é usado em `.USDZ` arquivos. Este arquivo `.USDZ` fornece conteúdo de AR e 3D para os dispositivos do usuário.

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
