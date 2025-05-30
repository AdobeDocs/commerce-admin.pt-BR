---
title: Credenciais de logon e URLs
description: Saiba mais sobre os URLs da Commerce e as credenciais de conta usadas para obter acesso ao administrador e à loja.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '351'
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
