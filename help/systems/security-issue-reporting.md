---
title: Relatórios de problemas de segurança
description: Saiba como configurar as informações de contato e os links relacionados à segurança que podem ser usados por pesquisadores de segurança para relatar problemas de segurança sobre o seu site.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---

# Relatórios de problemas de segurança

A variável `security.txt` O arquivo contém informações de contato e links relacionados à segurança que podem ser usados por pesquisadores de segurança para relatar preocupações de segurança sobre o site. Se suas informações de segurança mudarem com o tempo, verifique se elas estão `security.txt` O arquivo está atualizado.

**_Para configurar o security.txt:_**

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL Security]_, clique em **[!UICONTROL Security.txt]**.

1. No _[!UICONTROL General]_seção, definir **[!UICONTROL Enable]**para `Yes`.

   ![Configuração de segurança geral](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Em _[!UICONTROL Contact Information]_, insira o seguinte:

   - O endereço de email e o número de telefone da pessoa que gerencia problemas de segurança na sua loja.

   - O URL da loja **[!UICONTROL Contact Page]**. Esta página pode ser uma lista de contatos de segurança da loja ou sua _Entre em contato_ página.

   ![Configuração de informações de contato](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Em _[!UICONTROL Other Information]_, insira o seguinte:

   - O URL do público **[!UICONTROL Encryption]** chave. Por exemplo: `https://example.com/pgp-key.txt`

   - O URL de um **[!UICONTROL Acknowledgments]** página na qual os pesquisadores de segurança são reconhecidos por seus esforços em nome de sua loja.

   - Seu **[!UICONTROL Preferred Languages]** para comunicações de segurança. Insira o padrão de dois caracteres [código de idioma](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) para cada idioma suportado, separados por vírgula. Por exemplo, para especificar inglês, espanhol e francês, digite `en, es, fr`. Todos os idiomas especificados têm a mesma prioridade, independentemente da ordem de aparência.

   - O URL de um **[!UICONTROL Hiring]** página que lista oportunidades de emprego relacionadas à segurança na loja.

   - O URL da sua segurança **[!UICONTROL Policy]** página.

   - O URL de um site digital **[!UICONTROL Signature]** que é salvo no servidor. Por exemplo: `https://mystore.com/.well-known/security.txt.sig`

   A assinatura digital deve ser configurada na CLI (Command-Line Interface, interface de linha de comando) do servidor. Para saber mais, consulte [Segurança.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) no GitHub.

   ![Outras informações](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.
