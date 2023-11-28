---
title: conformidade com o PSD2
description: Saiba mais sobre os requisitos da Diretiva Serviços de Pagamento (PSD 2) que podem afetar sua loja.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# conformidade com o PSD2

A partir de 14 de setembro de 2019, a União Europeia exige que todos os comerciantes da UE e do Reino Unido cumpram as [Autenticação forte do cliente](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) da Diretiva Serviços de Pagamento (PSD 2). Os comerciantes de todos os outros países são incentivados a cumprir a PSD 2 como prática recomendada.

>[!NOTE]
>
>Este tópico destina-se apenas a fins informativos e não deve ser interpretado como aconselhamento jurídico. Para determinar se e como sua empresa deve cumprir quaisquer obrigações legais, consulte seu advogado.

A autenticação forte do cliente é um componente essencial do PSD2 e requer dois dos seguintes itens:

- Algo que somente o cliente tem (senha ou PIN)
- Algo que somente o cliente sabe (token de segurança exclusivo gerado por telefone ou fob de chave)
- Algo que somente o cliente é (autenticação biométrica, como impressão digital ou reconhecimento facial)

Os bancos europeus podem recusar pagamentos que não cumpram os requisitos. No entanto, transações de baixo risco e baixo valor ainda podem ser aceitas e pagamentos subsequentes em uma assinatura recorrente.

Devido a essa mudança significativa e para garantir que os pagamentos de clientes não sejam recusados, o Adobe introduziu as seguintes alterações e recomendações para clientes nativos [!DNL Commerce] integrações de pagamento.

| Método de pagamento | Requisitos de conformidade |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Para a maioria das soluções PayPal, nenhuma ação é necessária para cumprir com o PSD2, porque os requisitos são tratados pelo PayPal. Para obter informações sobre soluções específicas, consulte a nota na parte superior de cada tópico do PayPal. |
| [Braintree](../stores-purchase/braintree.md) | A partir da mudança para a extensão instalada na versão 2.4.0, os requisitos são tratados dentro do módulo de Pagamentos por Braintree incluído e nenhuma ação é necessária para estar em conformidade com a PSD 2. <br /><br />**_Nota:_**Para estar em conformidade com o PSD 2 usando a integração de núcleo das versões anteriores, execute um dos procedimentos a seguir:<br/>- (Recomendado) Instale a extensão oficial de integração de pagamento Braintree de [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target=&quot;_blank&quot;}.<br/>- Ative e configure o método de pagamento Braintree no [!DNL Commerce] configuração.<br/><br/>Essas integrações principais anteriores suportam a verificação 3D Secure 2.0. No entanto, as implementações de Braintree que são executadas no SDK v2 do JavaScript não são compatíveis com o 3D Secure 2.0. |
| Outro | Para todas as outras integrações de pagamento, verifique as extensões disponíveis em [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}. Solicite ao seu provedor de serviços de pagamento que recomende uma solução para dar suporte aos requisitos de PSD2. |

{style="table-layout:auto"}
