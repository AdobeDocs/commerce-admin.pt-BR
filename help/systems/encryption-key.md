---
title: Chave de criptografia
description: Saiba como alterar sua própria chave de criptografia, o que deve ser feito regularmente para melhorar a segurança.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Chave de criptografia

>[!NOTE]
>
>Se você tentou concluir essas etapas e está com problemas, consulte o artigo da Base de Dados de Conhecimento [Solução de Problemas de Rotação de Chaves de Criptografia: CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102).

A Adobe Commerce e a Magento Open Source usam uma chave de criptografia para proteger senhas e outros dados confidenciais. Um algoritmo [!DNL ChaCha20-Poly1305] padrão do setor é usado com uma chave de 256 bits para criptografar todos os dados que exigem criptografia. Isso inclui dados de cartão de crédito e senhas de integração (módulo de pagamento e envio). Além disso, um algoritmo de hash seguro forte (SHA-256) é usado para executar o hash de todos os dados que não exigem descriptografia.

Durante a instalação inicial, você será solicitado a permitir que o Commerce gere uma chave de criptografia ou a inserir uma de sua preferência. A ferramenta encryption key permite alterar a chave conforme necessário. A chave de criptografia deve ser alterada regularmente para melhorar a segurança e, a qualquer momento, a chave original pode ser comprometida.

Para obter informações técnicas, consulte [Instalação avançada local](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) no _Guia de Instalação_ e [Nova criptografia de dados](https://developer.adobe.com/commerce/php/development/security/data-encryption/) no _Guia do Desenvolvedor do PHP_.

>[!IMPORTANT]
>
>- Antes de seguir estas instruções para alterar a chave de criptografia, verifique se o seguinte arquivo é gravável: `[your store]/app/etc/env.php`
>- O recurso de alteração da chave de criptografia nas configurações de Administrador está obsoleto e foi removido na versão 2.4.8. Você deve usar o comando da CLI descrito nesta página para alterar a chave de criptografia após o upgrade para a versão 2.4.8.

**Para alterar uma chave de criptografia:**

As instruções a seguir exigem acesso a um terminal.

1. Habilitar [modo de manutenção](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode).

   ```bash
   bin/magento maintenance:enable
   ```

1. Desabilitar trabalhos cron.

   _Projetos de infraestrutura em nuvem:_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _Projetos locais_

   ```bash
   crontab -e
   ```

1. Altere a chave de criptografia usando um dos métodos a seguir.

   +++comando CLI

   Execute o seguinte comando da CLI e verifique se ele foi concluído sem erros. Se você precisar criptografar novamente determinados valores de configuração do sistema ou campos de pagamento, consulte o [guia detalhado sobre criptografia](https://developer.adobe.com/commerce/php/development/security/data-encryption/) no _Guia de Desenvolvimento do PHP_.

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++Configurações do administrador

   >[!IMPORTANT]
   >
   >Este recurso foi descontinuado e removido na versão 2.4.8. A Adobe recomenda alterar as chaves de criptografia com a CLI.

   1. Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

      ![Chave de criptografia do sistema](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. Siga um destes procedimentos:

      - Para gerar uma nova chave, defina **[!UICONTROL Auto-generate Key]** como `Yes`.
      - Para usar uma chave diferente, defina **[!UICONTROL Auto-generate Key]** como `No`. Em seguida, no campo **[!UICONTROL New Key]**, insira ou cole a chave que deseja usar.

   1. Clique em **[!UICONTROL Change Encryption Key]**.

      >[!NOTE]
      >
      >Mantenha um registro da nova chave em um local seguro. É necessário descriptografar os dados, se ocorrer algum problema com seus arquivos.

   +++

1. Limpe o cache.

   _Projetos de infraestrutura em nuvem:_

   ```bash
   magento-cloud cc
   ```

   _Projetos locais:_

   ```bash
   bin/magento cache:flush
   ```

1. Habilitar trabalhos cron.

   _Projetos de infraestrutura em nuvem:_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _Projetos locais:_

   ```bash
   crontab -e
   ```

1. Desabilitar modo de manutenção.

   ```bash
   bin/magento maintenance:disable
   ```
