---
title: Relatórios de problemas de segurança
description: Saiba como configurar as informações de contato e os links relacionados à segurança que podem ser usados por pesquisadores de segurança para relatar problemas de segurança sobre o seu site.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/tXZFSpgx9r2t-tN2Oc7L2aiPDlL6hSZBRC9pHjzcjQk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 0%

---

# Relatórios de problemas de segurança

O arquivo `security.txt` contém informações de contato e links relacionados à segurança que podem ser usados por pesquisadores de segurança para relatar preocupações de segurança sobre o site. Se suas informações de segurança forem alteradas com o tempo, verifique se elas estão atualizadas no arquivo `security.txt`.

**_Para configurar security.txt:_**

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL Security]_, clique em **[!UICONTROL Security.txt]**.

1. Na seção _[!UICONTROL General]_, defina **[!UICONTROL Enable]**&#x200B;como `Yes`.

   ![Configuração de segurança geral](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Em _[!UICONTROL Contact Information]_, digite o seguinte:

   - O endereço de email e o número de telefone da pessoa que gerencia problemas de segurança na sua loja.

   - A URL da sua loja **[!UICONTROL Contact Page]**. Esta página pode ser uma lista de contatos de segurança de armazenamento ou sua página _Fale Conosco_.

   ![Configuração de Informações de Contato](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Em _[!UICONTROL Other Information]_, digite o seguinte:

   - A URL da sua chave pública **[!UICONTROL Encryption]**. Por exemplo: `https://example.com/pgp-key.txt`

   - A URL de uma página **[!UICONTROL Acknowledgments]** na qual os pesquisadores de segurança são reconhecidos por seus esforços em nome de sua loja.

   - Seu **[!UICONTROL Preferred Languages]** para comunicações relacionadas à segurança. Insira o [código de idioma](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) de dois caracteres padrão para cada idioma suportado, separado por vírgula. Por exemplo, para especificar inglês, espanhol e francês, digite `en, es, fr`. Todos os idiomas especificados têm a mesma prioridade, independentemente da ordem de aparência.

   - A URL de uma página **[!UICONTROL Hiring]** que lista oportunidades de emprego relacionadas à segurança na sua loja.

   - A URL da página de segurança **[!UICONTROL Policy]**.

   - A URL de um arquivo digital **[!UICONTROL Signature]** salvo no servidor. Por exemplo: `https://mystore.com/.well-known/security.txt.sig`

   A assinatura digital deve ser configurada na CLI (Command-Line Interface, interface de linha de comando) do servidor. Para saber mais, consulte [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) no GitHub.

   ![Outras Informações](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
