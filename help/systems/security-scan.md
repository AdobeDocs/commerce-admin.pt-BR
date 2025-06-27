---
title: Verificação de segurança
description: Saiba como executar uma verificação de segurança aprimorada e monitorar cada um dos sites do Adobe Commerce e do Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 8e634311cd84a9e797a36218c29abb4699d72835
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Verificação de segurança

A verificação de segurança aprimorada permite monitorar cada um dos sites da Adobe Commerce e da Magento Open Source, incluindo o PWA, quanto a riscos de segurança conhecidos e malware, e receber atualizações de patches e notificações de segurança.

- Obtenha o insight no status de segurança em tempo real de sua loja.
- Receba sugestões com base nas práticas recomendadas para ajudar a resolver problemas.
- Programar verificação de segurança para execução semanal, diária ou sob demanda.
- Executar mais de 21.000 testes de segurança para ajudar a identificar malware em potencial.
- Acesse relatórios históricos de segurança que rastreiam e monitoram o progresso de seus sites.
- Acesse o relatório de varredura que mostra verificações bem-sucedidas e falhas, com qualquer ação recomendada.

A ferramenta Security scan está disponível gratuitamente no painel da sua [conta do Commerce/Magento](../getting-started/commerce-account-create.md). Para obter informações técnicas, consulte [Configurar a Ferramenta de Verificação de Segurança](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) no _Guia de Infraestrutura do Commerce na Nuvem_.

![Ferramenta de verificação de segurança](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Executar uma verificação de segurança

1. Entre na sua [conta Commerce/Magento](../getting-started/commerce-account-create.md).

1. No painel esquerdo, clique na guia [!UICONTROL Security Scan]. (Se necessário, revise e aceite quaisquer termos atualizados para usar a ferramenta de verificação de segurança.)

   - No painel esquerdo, escolha **[!UICONTROL Security Scan]**.
   - Clique em **[!UICONTROL Go to Security Scan]**.
   - Leia o **[!UICONTROL Terms and Conditions]**.
   - Clique em **[!UICONTROL Agree]** para continuar.

1. Na página _[!UICONTROL Monitored Websites]_, clique em **[!UICONTROL +Add Site]**.

   Se você tiver vários sites com domínios diferentes, configure uma verificação separada para cada domínio.

   ![Sites Monitorados](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Para verificar a propriedade do domínio do site adicionando um código de confirmação, siga um destes procedimentos:

   **vitrine da Commerce**:

   - Insira o **[!UICONTROL Site URL]** e **[!UICONTROL Site Name]**.
   - Clique em **[!UICONTROL Generate Confirmation Code]**.
   - Clique em **Copiar** para copiar seu código de confirmação para a área de transferência.

     ![Gerar Código de Confirmação](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Faça logon no Admin da loja como um usuário com privilégios totais de administrador e faça o seguinte:

      - Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Localize seu site na lista e clique em **[!UICONTROL Edit]**.
      - Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL HTML Head]**.
      - Role para baixo até **[!UICONTROL Scripts and Style Sheets]**, clique na caixa de texto ao final de qualquer código existente e cole o código de confirmação na caixa de texto.

        ![Scripts e Folhas de Estilo](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Quando terminar, clique em **[!UICONTROL Save Configuration]**.

   **vitrine da PWA**:

   - Insira o **[!UICONTROL Site URL]** e **[!UICONTROL Site Name]**.

   - Para **[!UICONTROL Confirmation Code]**, escolha a opção `META Tag` e clique em **[!UICONTROL Generate Code]**.

   - Clique em **[!UICONTROL Copy]** para copiar a marca META do código de confirmação gerado para a área de transferência.

     ![Gerar Código de Confirmação](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Vá para o diretório do projeto da loja PWA Studio e faça o seguinte:

      - No diretório do projeto PWA Studio, vá para `packages > venia-concept > template.html`.
      - Adicione o código de confirmação copiado (a tag META gerada) ao cabeçalho do HTML e salve as alterações.

        ![Copiar Código de Confirmação](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Volte para a CLI do PWA Studio e use o fio para instalar dependências de projeto e executar o comando build de projeto.

        ```sh
        yarn install &&
        yarn build
        ```

      - *No seu projeto na nuvem*, crie uma pasta `pwa` e copie o conteúdo dentro da pasta `dist` do projeto da vitrine.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Use a ferramenta Git CLI para preparar, confirmar e enviar essas alterações para o projeto na nuvem.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Depois que o processo de criação for concluído, as alterações serão implantadas na loja da PWA.

1. Retorne à página _[!UICONTROL Security Scan]_na sua conta do Commerce e clique em **[!UICONTROL Verify Confirmation Code]**para estabelecer a propriedade do domínio.

1. Após uma confirmação bem-sucedida, configure as opções do **[!UICONTROL Set Automatic Security Scan]** para um dos seguintes tipos:

   **Verificar Semanalmente (recomendado)**:

   - Escolha os **[!UICONTROL Week Day]**, **[!UICONTROL Time]** e **[!UICONTROL Time Zone]** nos quais a verificação deve ocorrer todas as semanas.
   - Por padrão, a verificação é programada para começar toda semana à meia-noite de sábado, UTC, e continuar até a madrugada de domingo.

     ![Verificar Semanalmente](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Verificar Diariamente**:

   - Escolha as **[!UICONTROL Time]** e **[!UICONTROL Time Zone]** em que a verificação deve ocorrer todos os dias.
   - Por padrão, a verificação é agendada para começar todos os dias à meia-noite, UTC.

     ![Verificação Diária](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Digite o **[!UICONTROL Email Address]** onde deseja receber notificações de verificações concluídas e atualizações de segurança.

   ![Endereço de email](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Submit]**.

   Após verificar a propriedade do domínio, o site é exibido na lista Sites monitorados da sua conta da Commerce.

1. Se você tiver vários sites com domínios diferentes, repita esse processo para configurar uma verificação de segurança para cada um.

## Excluir uma verificação de segurança

>[!NOTE]
>
>Somente a pessoa que configurou originalmente a verificação pode excluí-la da conta. Se eles não tiverem feito logon em sua [conta](https://account.magento.com) desde agosto de 2022, eles devem primeiro verificar se têm [registrado para uma Adobe ID](https://account.magento.com).

**Excluir uma verificação**

1. Entre na [conta da Commerce/Magento](../getting-started/commerce-account-create.md).

1. No painel esquerdo, clique na guia [!UICONTROL Security Scan]. (Se necessário, revise e aceite quaisquer termos atualizados para usar a ferramenta de verificação de segurança.)

   - Clique em **[!UICONTROL Go to Security Scan]**.
   - Leia o **[!UICONTROL Terms and Conditions]**.
   - Clique em **[!UICONTROL Agree]** para continuar.

1. Na página _[!UICONTROL Monitored Websites]_, localize a lista suspensa na coluna [!UICONTROL Actions] e selecione **[!UICONTROL Delete]**para o(s) site(s) apropriado(s).
