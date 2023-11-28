---
title: '[!DNL Google Analytics]'
description: Saiba como usar [!DNL Google Analytics] para coletar métricas úteis para seus sites do Commerce.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] O oferece a capacidade de definir dimensões e métricas personalizadas adicionais para rastreamento, com suporte para interações offline e de aplicativos móveis e acesso a atualizações contínuas. [!DNL Google Analytics] O 4 é a solução de medição de última geração da Google e está substituindo o [!DNL Universal Analytics]. Em 1º de julho de 2023, as propriedades padrão do Universal Analytics deixarão de processar novas ocorrências.

>[!NOTE]
>
>Se sua empresa estiver sujeita a regulamentos de privacidade, como o [Regulamento Geral sobre a Proteção de Dados](../getting-started/compliance-gdpr.md) e/ou a [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), consulte [Configurações de privacidade do Google](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Se você habilitar a opção [Modo de restrição de cookies](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] O não coleta dados sobre visitantes, a menos que tenham aceitado cookies.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Etapa 1: configurar [!UICONTROL Google Analytics] 4

Se você ainda não tiver uma [!DNL Google Analytics] 4 para o seu site, siga um destes métodos:

- [Configurar a coleta de dados do Analytics pela primeira vez](https://support.google.com/analytics/answer/9304153)
- [Adicionar Google Analytics 4 a um site com [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Etapa 2: concluir a configuração do Commerce

1. Faça logon no Administrador da sua loja Commerce.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Google API]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Google GTag]** seção.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Google Analytics4]** subseção e faça o seguinte:

   - Definir **[!UICONTROL Enable]** para `Yes`.

   - Deixe a **[!UICONTROL Account type]** as `Google Analytics4`.

   - Insira seu **[!UICONTROL Measurement ID]**. Para saber mais, consulte [Ajuda do Google Analytics](https://support.google.com/analytics/answer/9539598).

   - Se você quiser realizar testes A/B e outros testes de desempenho no seu conteúdo, defina **Experimentos de conteúdo** para `Yes`.

   ![Configuração de vendas - API do Google para Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>Em 1º de julho de 2023, as propriedades padrão do Universal Analytics não processarão mais os dados. Se você ainda confiar em [!DNL Universal Analytics], recomenda-se que você [prepare-se para usar o Google Analytics 4](https://support.google.com/analytics/answer/10759417) daqui para frente.

### Etapa 1: configurar o Google Universal Analytics

Visite o site da Google e inscreva-se para obter um [Google Universal Analytics][1] conta.

### Etapa 2: concluir a configuração do Commerce

1. Faça logon no Administrador da sua loja Commerce.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Sales]** e escolha **[!UICONTROL Google API]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Google Analytics]** e faça o seguinte:

   - Definir **[!UICONTROL Enable]** para `Yes`.

   - Insira seu [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Se você quiser realizar testes A/B e outros testes de desempenho no seu conteúdo, defina **[!UICONTROL Content Experiments]** para `Yes`.

   ![Configuração de vendas - API do Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Comércio eletrônico aprimorado

O Ecommerce aprimorado é um plug-in para [!DNL Google Universal Analytics] isso fornece informações sobre o comportamento de compra e compra dos clientes. Você pode usar o Ecommerce aprimorado para produzir relatórios sobre as principais atividades do cliente, como quando os clientes adicionam itens ao carrinho, iniciam o processo de finalização ou concluem uma compra. Você também pode identificar e analisar padrões de compradores que abandonam seus carrinhos sem fazer uma compra.

As instruções a seguir mostram como configurar [!DNL Google Tag Manager] com [!DNL Universal Analytics] para produzir dados e relatórios aprimorados de comércio eletrônico.

### Etapa 1. Inscrever-se para contas do Google

1. Inscreva-se para um [Gerenciador de tags da Google](google-tag-manager.md) e conclua a configuração do Commerce.

1. Inscreva-se para um novo [Google Universal Analytics][1] conta.

### Etapa 2. Configurar o Ecommerce aprimorado

1. Faça logon em sua conta do Google Universal Analytics.

1. Crie uma propriedade para a Análise aprimorada de comércio eletrônico com as seguintes configurações:

   - Status: ATIVADO
   - Produtos relacionados: ATIVADO
   - Ativar Relatórios de Comércio Eletrônico Aprimorados: ATIVADO
   - Rotulagem de check-out: (não obrigatório)

1. Quando terminar, clique em **[!UICONTROL Submit]**.

### Etapa 3. Criar tags e acionadores

1. Faça logon no [!DNL Google Tag Manager] e crie os seguintes acionadores:

   | Nome | Tipo de evento | Filtro |
   |--- |--- |--- |
   | `addToCart` | Evento personalizado |  |
   | `checkout` | Evento personalizado |  |
   | `checkout only` | Exibição da página | O URL da página corresponde a RegEx /checkout/.* |
   | `checkoutOption` | Evento personalizado |  |
   | `gtm.dom` | Evento personalizado |  |
   | `productClick` | Evento personalizado |  |
   | `promotionClick` | Evento personalizado |  |
   | `removeFromCart` | Evento personalizado |  |

   >[!NOTE]
   >
   >A variável [!UICONTROL Checkout] evento é acionado apenas para os métodos de pagamento básicos incorporados do Commerce (como `Check / Money Order` e `Cash On Delivery Payment`). Este evento não é executado por `PayPal checkout` e outros métodos de pagamento externo, que usam redirecionamento para o check-out de recursos externos.

1. Crie as seguintes tags do Universal Analytics com a mesma configuração básica.

   - Tags do Universal Analytics

     | Nome | Tipo | Disparar acionadores |
     |--- |--- |--- |
     | `Add to cart tracking` | Universal Analytics | addToCart |
     | `Checkout option tracking` | Universal Analytics | checkoutOption |
     | `Checkout tracking` | Universal Analytics | check-out |
     | `Pageview tracking` | Universal Analytics | gtm.dom |
     | `Product click tracking` | Universal Analytics | productClick |
     | `Promo click tracking` | Universal Analytics | promotionClick |
     | `Remove from cart tracking` | Universal Analytics | removeFromCart |

   - Configuração básica de tag

     | Configuração | Valor |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX (a ID de rastreamento da sua conta do Universal Analytics.) |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | True |
     | [!UICONTROL Use data layer] | True |
     | [!UICONTROL Use Debug version] | True |

1. Conclua as configurações de rastreamento individuais.

   - Insira o seguinte **[!UICONTROL Add to Cart]** configurações de rastreamento:

     | Configuração | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comércio eletrônico |
     | [!UICONTROL Action] | Adicionar ao carrinho |
     | [!UICONTROL Trigger] | addToCart |

   - Insira o seguinte **[!UICONTROL Checkout option]** configurações de rastreamento:

     | Configuração | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comércio eletrônico |
     | [!UICONTROL Action] | Opção de check-out |
     | [!UICONTROL Trigger] | checkoutOption |

   - Insira o seguinte **[!UICONTROL PageView]** configurações de rastreamento:

     | Configuração | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Conclua o seguinte **[!UICONTROL Product Click]** configuração de rastreamento:

     | Configuração | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comércio eletrônico |
     | [!UICONTROL Action] | Clique no produto |
     | [!UICONTROL Trigger] | productClick |

   - Conclua o seguinte **[!UICONTROL Promotion Click]** configuração de rastreamento:

     | Configuração | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comércio eletrônico |
     | [!UICONTROL Action] | Clique na promoção |
     | [!UICONTROL Trigger] | promotionClick |

   - Conclua o seguinte **[!UICONTROL Remove from Cart]** configuração de rastreamento:

     | Configuração | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comércio eletrônico |
     | [!UICONTROL Action] | Remover do carrinho |
     | [!UICONTROL Trigger] | removeFromCart |

1. Quando terminar, clique em **[!UICONTROL Preview]** e verifique se as tags funcionam corretamente.

1. Após verificar as configurações, clique em **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
