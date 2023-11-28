---
title: '[!DNL AR Viewer] para Adobe Commerce'
description: Saiba como o [!DNL AR Viewer] O pode beneficiar sua instância do Adobe Commerce e aprender a integrar e configurar a extensão com êxito.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] para Adobe Commerce

A realidade aumentada (RA) descreve as experiências do usuário que adicionam elementos 2D ou 3D à visualização ao vivo da câmera de um dispositivo de forma que esses elementos pareçam habitar o mundo real.

A variável [!DNL AR Viewer] A extensão para Adobe Commerce capacita uma experiência perfeita projetada para exibir gráficos 3D renderizados para o usuário.

As informações neste guia fornecem uma visão geral da experiência de integração para o [!DNL AR Viewer] no Adobe Commerce e como o [!DNL AR Viewer] O beneficia o usuário, bem como as práticas recomendadas que devem ser seguidas ao longo dessa jornada.

Desenvolvido pela Pixar, [Descrição da cena universal (USD)](https://www.pixar.com/usd){target=_blank} O é o primeiro software de código aberto que pode intercambiar cenas 3D de maneira robusta e escalável, que podem ser compostas por vários ativos, fontes e animações diferentes, enquanto promove fluxos de trabalho altamente colaborativos. Este USD é usado em `.USDZ` arquivos. Este `.USDZ` O arquivo fornece conteúdo AR e 3D para os dispositivos do usuário.

>[!NOTE]
>
> A variável [!DNL AR Viewer] suporta somente `.USDZ` arquivos.

## [!DNL AR Viewer] requisitos

A variável [!DNL AR Viewer] é compatível com ambos [!DNL Magento Open Source] e Adobe Commerce. Consulte [Política de ciclo de vida](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} para obter mais informações sobre as versões compatíveis.

Consulte [Instale o [!DNL AR Viewer] extensão](../catalog/ar-viewer-setup.md) para obter mais informações.

Para utilizar [!DNL AR Viewer], você deve ter o seguinte disponível para sua instância:

* PHP 8.1.0
* Adobe Commerce versão 2.4.4 e mais recente
* Magento Open Source (CE) versão 2.4.x

## Limitações de compatibilidade

[!DNL AR Viewer] limitações de compatibilidade existentes:

* `.USDZ` only: este recurso só oferece suporte `.USDZ` arquivos.
* `qr-code`: Exige `endroid/qr-code` versão 4.5.
* `Catalog module`: Exige `magento/module-catalog` versão 104.0.0.
