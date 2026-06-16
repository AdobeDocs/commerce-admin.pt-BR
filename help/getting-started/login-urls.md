---
title: Credenciais de logon e URLs
description: Saiba mais sobre os URLs da Commerce e as credenciais de conta usadas para obter acesso ao administrador e à loja.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
TQID: https://experienceleague.adobe.com/8IGacP581jwpVtFnCFXRrG5vuIwCJaAUnbliitMHuf8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: d41d3a54-9721-475c-abd6-295bebfba9e4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 373
ht-degree: 0%

---

# Credenciais de logon e URLs

Antes de prosseguir com a instalação e configuração, verifique se você tem as informações necessárias para acessar o administrador da loja e a conta da Commerce.

## URL da vitrine

O endereço da sua [loja](storefront.md) é geralmente o domínio atribuído ao seu endereço IP. Alguns armazenamentos são instalados na raiz ou no diretório mais acima. Outros são instalados em um diretório abaixo da raiz. O armazenamento pode residir em um subdomínio associado a um domínio primário. O URL da loja pode ser semelhante a um dos seguintes:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

Se você ainda não tiver um domínio, a URL de armazenamento incluirá uma série de quatro números, cada um separado por um ponto na notação _pontilhado quad_.

## URL do administrador

O endereço do [Administrador](admin.md) do armazenamento é configurado durante a instalação. O endereço padrão é o mesmo do armazenamento, mas com `/admin` no final. Embora os exemplos neste guia usem o diretório padrão, é uma prática recomendada executar seu Administrador de um local exclusivo da sua loja.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## Conta [!DNL Commerce]

Sua [conta da Commerce](commerce-account-create.md) fornece acesso a informações sobre seus produtos e serviços, configurações da conta, histórico de cobrança e recursos de suporte. Para acessar sua conta, vá para o site principal do Commerce e clique em **[!UICONTROL My Account]** no canto superior direito.

## Conta do cliente

Enquanto você está aprendendo sobre a loja, certifique-se de configurar uma [conta de cliente](../customers/account-dashboard.md) de teste, para que possa experimentar o processo de armazenamento e finalização da perspectiva do cliente.

## Dados de exemplo

[!BADGE Somente PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."}

O Adobe fornece um conjunto de dados de exemplo que inclui uma loja de exemplo com mais de 250 produtos (cerca de 200 deles são produtos configuráveis), categorias, regras de preços promocionais, páginas do CMS, banners e assim por diante. Os dados de exemplo usam o tema _Luma_ na vitrine. [A instalação destes dados de exemplo](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) é opcional, mas pode ser útil para testar e desenvolver personalizações para seus negócios de comércio eletrônico.
