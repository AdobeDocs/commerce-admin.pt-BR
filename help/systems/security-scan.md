---
title: Verificação de segurança
description: Saiba como executar uma verificação de segurança aprimorada e monitorar cada um dos sites Adobe Commerce e Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 1f3173d17cc43227f7d44637f1ef0b62606cd0fd
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Verificação de segurança

A varredura de segurança aprimorada permite monitorar cada um dos sites do Adobe Commerce e do Magento Open Source, incluindo o PWA, quanto a riscos de segurança conhecidos e malware, e receber atualizações de patches e notificações de segurança.

- Obter informações sobre o status de segurança em tempo real da sua loja.
- Receba sugestões com base nas práticas recomendadas para ajudar a resolver problemas.
- Programar verificação de segurança para execução semanal, diária ou sob demanda.
- Executar mais de 21.000 testes de segurança para ajudar a identificar malware em potencial.
- Acesse relatórios históricos de segurança que rastreiam e monitoram o progresso de seus sites.
- Acesse o relatório de varredura que mostra verificações bem-sucedidas e falhas, com qualquer ação recomendada.

A ferramenta Security scan está disponível gratuitamente no painel do [Conta do Commerce/Magento](../getting-started/commerce-account-create.md). Para obter informações técnicas, consulte [Configurar a ferramenta Verificação de segurança](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) no _Guia da infraestrutura do Commerce na nuvem_.

![Ferramenta de verificação de segurança](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Executar uma verificação de segurança

1. Na página inicial da Commerce, faça logon no [Conta do Commerce/Magento](../getting-started/commerce-account-create.md).

1. Revise e aceite os termos para usar a ferramenta de verificação de segurança.

   - No painel esquerdo, escolha **[!UICONTROL Security Scan]**.
   - Clique em **[!UICONTROL Go to Security Scan]**.
   - Leia o **[!UICONTROL Terms and Conditions]**.
   - Clique em **[!UICONTROL Agree]** para continuar.

1. No _[!UICONTROL Monitored Websites]_clique em **[!UICONTROL +Add Site]**.

   Se você tiver vários sites com domínios diferentes, configure uma verificação separada para cada domínio.

   ![Sites Monitorados](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Para verificar a propriedade do domínio do site adicionando um código de confirmação, siga um destes procedimentos:

   **vitrine da Commerce**:

   - Insira o **[!UICONTROL Site URL]** e **[!UICONTROL Site Name]**.
   - Clique em **[!UICONTROL Generate Confirmation Code]**.
   - Clique em **Copiar** para copiar o código de confirmação para a área de transferência.

     ![Gerar código de confirmação](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Faça logon no Admin da loja como um usuário com privilégios totais de administrador e faça o seguinte:

      - No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Localize seu site na lista e clique em **[!UICONTROL Edit]**.
      - Expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL HTML Head]** seção.
      - Role para baixo até **[!UICONTROL Scripts and Style Sheets]** e clique na caixa de texto ao final de qualquer código existente e cole o código de confirmação na caixa de texto.

        ![Scripts e Folhas de Estilo](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Quando terminar, clique em **[!UICONTROL Save Configuration]**.

   **vitrine do PWA**:

   - Insira o **[!UICONTROL Site URL]** e **[!UICONTROL Site Name]**.

   - Para **[!UICONTROL Confirmation Code]**, escolha o `META Tag` e clique em **[!UICONTROL Generate Code]**.

   - Clique em **[!UICONTROL Copy]** para copiar a META Tag do código de confirmação gerado para a área de transferência.

     ![Gerar código de confirmação](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Vá para o diretório do projeto da loja de PWA Studio e faça o seguinte:

      - No diretório do projeto PWA Studio, vá para `packages > venia-concept > template.html`.
      - Adicione o código de confirmação copiado (a tag META gerada) ao cabeçalho de HTML e salve as alterações.

        ![Copiar código de confirmação](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Volte para a CLI do PWA Studio e use o fio para instalar dependências de projeto e executar o comando build de projeto.

        ```sh
        yarn install &&
        yarn build
        ```

      - *No seu projeto na nuvem*, criar um `pwa` e copie o conteúdo dentro do diretório do projeto da loja `dist` pasta.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Use a ferramenta Git CLI para preparar, confirmar e enviar essas alterações para o projeto na nuvem.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Depois que o processo de criação for concluído, as alterações serão implantadas no front da loja de PWA.

1. Retorne para a _[!UICONTROL Security Scan]_na sua conta da Commerce e clique em **[!UICONTROL Verify Confirmation Code]**para estabelecer a propriedade do domínio.

1. Após uma confirmação bem-sucedida, configure o **[!UICONTROL Set Automatic Security Scan]** para um dos seguintes tipos:

   **Verificar semanalmente (recomendado)**:

   - Escolha o **[!UICONTROL Week Day]**, **[!UICONTROL Time]**, e **[!UICONTROL Time Zone]** que a verificação deve ocorrer todas as semanas.
   - Por padrão, a verificação é programada para começar toda semana à meia-noite de sábado, UTC, e continuar até a madrugada de domingo.

     ![Verificar semanalmente](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Verificar diariamente**:

   - Escolha o **[!UICONTROL Time]**, e **[!UICONTROL Time Zone]** que a verificação deve ocorrer todos os dias.
   - Por padrão, a verificação é agendada para começar todos os dias à meia-noite, UTC.

     ![Verificar diariamente](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Insira o **[!UICONTROL Email Address]** onde deseja receber notificações de verificações concluídas e atualizações de segurança.

   ![Endereço de e-mail](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Submit]**.

   Após verificar a propriedade do domínio, o site é exibido na lista Sites monitorados da sua conta da Commerce.

1. Se você tiver vários sites com domínios diferentes, repita esse processo para configurar uma verificação de segurança para cada um.
