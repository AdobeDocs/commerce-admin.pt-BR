---
title: Configurações de enriquecimento
description: Configure a entrega, tarefas mensais de tráfego agencial e agentes de IA qualificados compartilhados por Enriquecimento de catálogo e Enriquecimento de PDP na Descoberta de produto de IA.
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# Configurações de enriquecimento

Use a guia **[!UICONTROL Settings]** no espaço de trabalho Descoberta de Produtos de IA para configurar sua instância do Adobe Commerce. Quando configurados, os enriquecimentos de catálogo e PDP são exibidos no espaço de trabalho Descoberta de produto de IA.

Os campos nesta guia identificam o ambiente [!DNL Adobe Commerce] e a exibição de loja à qual a Descoberta de Produto da IA se conecta. Para obter os requisitos de entrada e organização do IMS, consulte os [pré-requisitos de Descoberta de Produto de IA](prerequisites.md).

1. No Administrador, vá para **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** ou **[!UICONTROL Product Details Page Enrichment]**.
1. Na lista **[!UICONTROL Scope]** na parte superior da página, selecione o modo de exibição de loja que deseja configurar ou deixe **[!UICONTROL All Store Views]** para gerenciar as configurações entre os modos de exibição de loja.
1. Abra a guia **[!UICONTROL Settings]**.
1. Em **[!UICONTROL Commerce Configuration]**, expanda o painel de exibição de loja rotulado com sua URL.

   Forneça os detalhes do ambiente [!DNL Adobe Commerce] para habilitar o serviço de Descoberta de Produtos de IA e os fluxos de trabalho de auditoria.

   ![Configuração do Commerce na guia Configurações de Enriquecimento do Catálogo](./assets/catalog-enrichment-commerce-config.png){zoomable="yes"}

1. Insira os detalhes da conexão necessários para a exibição da loja.

   - **[!UICONTROL Store View URL]**: URL correspondente à exibição de armazenamento (por exemplo, `https://brand.example.com/fr/`).
   - **[!UICONTROL Environment ID]**: Identificador exclusivo do ambiente [!DNL Adobe Commerce] que a conexão acessa.
   - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]** e **[!UICONTROL Store View Code]**: Códigos de exibição de site, loja e loja do site da Commerce. Esses valores devem corresponder aos códigos no Administrador do Commerce.
   - **[!UICONTROL Host Name]**: Nome do host da sua instância [!DNL Adobe Commerce].
   - **(Opcional - somente para enriquecimento do catálogo)** Em **[!UICONTROL Catalog field limits]**, selecione **[!UICONTROL Limit maximum characters for product name]** e especifique o limite de caracteres para qualquer nome de produto gerado. Selecione **[!UICONTROL Limit maximum characters for product description]** e especifique o limite de caracteres para qualquer descrição de produto gerada.

1. Clique em **[!UICONTROL Save]**.

Depois de salvar, aguarde a conclusão de qualquer trabalho de sincronização ou validação inicial antes de depender dos resultados do catálogo ou da auditoria para essa exibição de armazenamento. Pode levar até 24 horas para que as sugestões de produtos sejam exibidas na página **[!UICONTROL Catalog Enrichment]**.

Para remover uma configuração de exibição de repositório, expanda essa entrada e clique em **[!UICONTROL Delete]**.

## Descrições dos campos {#commerce-connection-fields}

Os campos obrigatórios estão marcados com um asterisco (*) no formulário **[!UICONTROL Commerce Configuration]**.

| Campo | Obrigatório | Descrição |
| --- | --- | --- |
| Armazenar URL de exibição | Sim | URL correspondente à exibição de armazenamento (por exemplo, `https://brand.example.com/fr/`). |
| ID do ambiente | Sim | Identificador exclusivo do ambiente [!DNL Adobe Commerce] que a conexão acessa. |
| Código do site | Sim | Código do site da Commerce. |
| Armazenar código | Sim | Código de armazenamento do site da Commerce. |
| Código de exibição da loja | Sim | Exibição de loja do site da Commerce. |
| Nome do host | Sim | Nome do host da instância [!DNL Adobe Commerce]. |
| Limites de campo de catálogo (somente enriquecimento do catálogo) | Não | Defina limites de caracteres para quaisquer nomes e descrições de produtos gerados. |
