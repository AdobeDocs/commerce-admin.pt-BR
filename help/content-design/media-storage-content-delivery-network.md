---
title: Usar uma rede de entrega de conteúdo
description: Saiba como usar uma Rede de entrega de conteúdo (CDN) para armazenar arquivos de mídia.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/c-Aw3S5unZlMdDG1k080D4CIMcILglNa4ymZxPt6HBk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 0%

---

# Usar uma rede de entrega de conteúdo

Uma rede de entrega de conteúdo (CDN) pode ser usada para armazenar arquivos de mídia. O Adobe Commerce na infraestrutura em nuvem inclui a CDN Fastly (consulte [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) no _Guia do Commerce na Infraestrutura da Nuvem_). Uma instância do Commerce que esteja instalada _no local_ não inclui uma integração com qualquer CDN específica. Você pode usar a CDN de sua escolha.

Após configurar o CDN, você deve concluir a configuração no Admin. As alterações podem ser feitas no nível global ou do site. Quando um CDN é usado para armazenamento de mídia, todos os caminhos para mídia nas páginas de armazenamento do Commerce são alterados para os caminhos CDN especificados na configuração.

## Fluxo de trabalho CDN

1. **Mídia de solicitações do navegador** - Uma página da loja é aberta no navegador do cliente e o navegador solicita a mídia especificada na HTML.
1. **Solicitação enviada para a CDN; imagens encontradas e veiculadas** - A solicitação é enviada primeiro para a CDN. Se o CDN tiver as imagens armazenadas, ele fornecerá os arquivos de mídia ao navegador do cliente.
1. **Mídia não encontrada, solicitação enviada para o [!DNL Commerce] servidor Web** - Se a CDN não tiver os arquivos de mídia, a solicitação será enviada para o servidor Web [!DNL Commerce]. Se os arquivos de mídia forem encontrados no sistema de arquivos, o servidor da Web os enviará ao navegador do cliente.

>[!IMPORTANT]
>
>Por questões de segurança, quando um CDN é usado como armazenamento de mídia, o JavaScript pode não funcionar corretamente se o CDN estiver localizado fora do seu subdomínio.

## Configurar uma rede de entrega de conteúdo

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Web]**.

1. No canto superior esquerdo, defina **[!UICONTROL Store View]** conforme necessário.

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Base URLs]** e faça o seguinte:

   ![Configuração geral - URLs de base Web](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Atualize o **[!UICONTROL Base URL for Static View Files]** com a URL do local no CDN onde os arquivos de exibição estáticos estão armazenados.

   - Atualize o **[!UICONTROL Base URL for User Media Files]** com a URL dos arquivos JavaScript no CDN.

     Ambos os campos podem ser deixados em branco ou podem começar com o espaço reservado: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Base URLs (Secure)]** e faça o seguinte:

   ![Configuração geral - URLs de base da Web (seguro)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Atualize o **[!UICONTROL Secure Base URL for Static View Files]** com a URL do local no CDN onde os arquivos de exibição estáticos estão armazenados.

   - Atualize o **[!UICONTROL Secure Base URL for User Media Files]** com a URL dos arquivos JavaScript no CDN.

     Ambos os campos podem ser deixados em branco ou podem começar com o espaço reservado: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
