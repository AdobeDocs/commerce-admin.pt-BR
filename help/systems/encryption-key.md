---
title: Chave de criptografia
description: Saiba como gerar automaticamente ou adicionar sua própria chave de criptografia, que deve ser alterada regularmente para melhorar a segurança.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Chave de criptografia

O Adobe Commerce e o Magento Open Source usam uma chave de criptografia para proteger senhas e outros dados confidenciais. Um padrão do setor [!DNL ChaCha20-Poly1305] O algoritmo é usado com uma chave de 256 bits para criptografar todos os dados que exigem criptografia. Isso inclui dados de cartão de crédito e senhas de integração (módulo de pagamento e envio). Além disso, um algoritmo de hash seguro forte (SHA-256) é usado para executar o hash de todos os dados que não exigem descriptografia.

Durante a instalação inicial, você será solicitado a permitir que o Commerce gere uma chave de criptografia ou insira uma de sua preferência. A ferramenta encryption key permite alterar a chave conforme necessário. A chave de criptografia deve ser alterada regularmente para melhorar a segurança e, a qualquer momento, a chave original pode ser comprometida. Sempre que a chave é alterada, todos os dados herdados são recodificados usando a nova chave.

Para obter informações técnicas, consulte [Instalação avançada local](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) no _Guia de instalação_.

## Etapa 1: tornar o arquivo gravável

Para alterar a chave de criptografia, verifique se o seguinte arquivo é gravável: `[your store]/app/etc/env.php`

## Etapa 2: Alterar a chave de criptografia

1. No _Admin_ barra lateral, vá para **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Chave de criptografia do sistema](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Siga um destes procedimentos:

   - Para gerar uma nova chave, defina **[!UICONTROL Auto-generate Key]** para `Yes`.
   - Para usar uma chave diferente, defina **[!UICONTROL Auto-generate Key]** para `No`. Em seguida, no **[!UICONTROL New Key]** insira ou cole a chave que deseja usar.

1. Clique em **[!UICONTROL Change Encryption Key]**.

1. Mantenha um registro da nova chave em um local seguro.

   É necessário descriptografar os dados, se ocorrer algum problema com seus arquivos.
