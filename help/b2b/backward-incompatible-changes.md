---
title: Alterações incompatíveis com versões anteriores do Adobe Commerce B2B
description: Saiba mais sobre as alterações nas versões B2B do Adobe Commerce que podem exigir a atualização do código personalizado.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Alterações incompatíveis com versões anteriores do Adobe Commerce B2B

Revise as informações de referência de alto nível para todas as alterações incompatíveis com versões anteriores em B2B para versões do Adobe Commerce. Consulte a seção de destaques para conhecer as alterações incompatíveis que têm grande impacto e exigem explicação detalhada e instruções especiais.

## Destaques

### 1.4.2 a 1.5.0

Com a adição da atribuição multiempresa, as contas de usuário da empresa agora podem ter vários valores `company_id`. O `Magento\Company\Api\Data\CompanyCustomerInterface` foi atualizado para definir o `company_id` padrão para um usuário. O padrão é definido para a primeira empresa atribuída à conta de usuário da empresa.

Se você estiver atualizando de uma versão anterior, o Adobe recomenda implementar os seguintes métodos nas classes que usam o `Magento\Company\Api\Data\CompanyCustomerInterface`.

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## Referência

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
