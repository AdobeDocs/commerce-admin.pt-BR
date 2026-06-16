---
title: Conformidade com o PSD2
description: Saiba mais sobre os requisitos da Diretiva de Serviços de Pagamento (PSD2) que podem afetar sua loja.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
TQID: https://experienceleague.adobe.com/paVa-tpYYzrINAPRFs4TOzbp4b4CLJDlxqNlL1gzp2Q
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c32adafa-ed01-4b31-997e-2413013911b0id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f0ca7b10-ef6c-4ee4-b63f-030819bdd1f3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# Conformidade com o PSD2

A partir de 14 de setembro de 2019, a União Europeia exige que todos os comerciantes da UE e do Reino Unido cumpram os requisitos de [Autenticação de Cliente Forte](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) da Diretiva de Serviços de Pagamento (PSD2). Os comerciantes de todos os outros países são incentivados a cumprir a PSD2 como prática recomendada.

>[!NOTE]
>
>Este tópico destina-se apenas a fins informativos e não deve ser interpretado como aconselhamento jurídico. Para determinar se e como sua empresa deve cumprir quaisquer obrigações legais, consulte seu advogado.

A autenticação forte do cliente é um componente essencial da PSD2 e requer dois dos seguintes itens:

- Algo que somente o cliente tem (senha ou PIN)
- Algo que somente o cliente sabe (token de segurança exclusivo gerado por telefone ou fob de chave)
- Algo que somente o cliente é (autenticação biométrica, como impressão digital ou reconhecimento facial)

Os bancos europeus podem recusar pagamentos que não cumpram os requisitos. No entanto, transações de baixo risco e baixo valor ainda podem ser aceitas e pagamentos subsequentes em uma assinatura recorrente.

Devido a essa mudança significativa e para garantir que os pagamentos dos clientes não sejam recusados, a Adobe apresentou as seguintes alterações e recomendações para integrações de pagamento [!DNL Commerce] nativas.

| Método de pagamento | Requisitos de conformidade |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Para a maioria das soluções do PayPal, nenhuma ação é necessária para estar em conformidade com a PSD2, porque os requisitos são tratados pelo PayPal. Para obter informações sobre soluções específicas, consulte a nota na parte superior de cada tópico do PayPal. |
| [Braintree](../stores-purchase/braintree.md) | A partir da mudança para a extensão instalada na versão 2.4.0, os requisitos são tratados no módulo do Braintree Payments incluído e nenhuma ação é necessária para estar em conformidade com o PSD2. <br /><br />**_Nota:_** Para estar em conformidade com a PSD2 usando a integração principal em versões anteriores, siga um destes procedimentos:<br/>- (Recomendado) Instale a extensão de integração de pagamento oficial da Braintree de [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}.<br/>- Habilite e configure o método de pagamento da Braintree na configuração [!DNL Commerce].<br/><br/>Essas integrações principais anteriores oferecem suporte à verificação do 3D Secure 2.0. No entanto, as implementações do Braintree executadas no JavaScript SDK v2 não são compatíveis com o 3D Secure 2.0. |
| Outro | Para todas as outras integrações de pagamento, verifique as extensões disponíveis em [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}. Solicite ao seu provedor de serviços de pagamento que recomende uma solução para dar suporte aos requisitos do PSD2. |

{style="table-layout:auto"}
