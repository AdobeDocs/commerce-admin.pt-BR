---
title: Credenciais de logon e URLs
description: Saiba mais sobre os URLs do Commerce e as credenciais da conta usadas para obter acesso ao administrador e à loja.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# Credenciais de logon e URLs

Antes de prosseguir com a instalação e configuração, verifique se você tem as informações necessárias para acessar o administrador da loja e a conta do Commerce.

## URL da vitrine

O endereço do seu [vitrine](storefront.md) geralmente, é o domínio atribuído ao seu endereço IP. Alguns armazenamentos são instalados na raiz ou no diretório mais acima. Outros são instalados em um diretório abaixo da raiz. O armazenamento pode residir em um subdomínio associado a um domínio primário. O URL da loja pode ser semelhante a um dos seguintes:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

Se você ainda não tiver um domínio, o URL de loja incluirá uma série de quatro números, cada um separado por um ponto em _quad pontilhado_ notação.

## URL do administrador

O endereço da loja [Admin](admin.md) é configurado durante a instalação. O endereço padrão é o mesmo da loja, mas com `/admin` no final. Embora os exemplos neste guia usem o diretório padrão, é uma prática recomendada executar seu Administrador de um local exclusivo da sua loja.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] account

Seu [Conta do Commerce](commerce-account-create.md) O fornece acesso a informações sobre seus produtos e serviços, configurações da conta, histórico de faturamento e recursos de suporte. Para acessar sua conta, acesse o site principal do Commerce e clique em **[!UICONTROL My Account]** no canto superior direito.

## Conta do cliente

Enquanto estiver aprendendo sobre a loja, certifique-se de configurar um teste [conta do cliente](../customers/account-dashboard.md), para que você possa experimentar o processo de armazenamento e finalização da perspectiva do cliente.

## Dados de exemplo

O Adobe fornece um conjunto de dados de exemplo que inclui uma loja de exemplo com mais de 250 produtos (cerca de 200 deles são produtos configuráveis), categorias, regras de preços promocionais, páginas CMS, banners e assim por diante. Os dados de amostra usam o _Luma_ tema na loja. [Instalar estes dados de exemplo](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) O é opcional, mas pode ser útil para testar e desenvolver personalizações para seus negócios de comércio eletrônico.
