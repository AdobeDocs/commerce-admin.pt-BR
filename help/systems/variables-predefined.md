---
title: Usar variáveis predefinidas
description: Saiba mais sobre as variáveis predefinidas e como adicioná-las em um modelo de email.
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Usar variáveis predefinidas

[Predefinido](variables-predefined.md) facilitam a personalização [email](email-templates.md) e [informativo](../merchandising-promotions/newsletters.md) modelos e outros tipos de conteúdo. A lista de permissões [predefinido](variables-predefined.md) são exibidas quando você clica no botão Inserir variável. Como mostrado na imagem a seguir, a lista de variáveis disponíveis para um template de email específico é determinada pelos dados associados ao template. Consulte a [Referência da variável](variables-reference.md) para obter uma lista de modelos de email usados com frequência e suas variáveis associadas.

![Variáveis predefinidas para o modelo de email](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## Adicionar uma variável a um modelo de email

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Siga um destes procedimentos:

   - Para adicionar a variável a um modelo existente, clique no modelo na lista para abrir o no modo de edição.

   - Para usar a variável em um novo modelo, clique em **[!UICONTROL Add New Template]** e personalize o código do template padrão. Consulte [Modelos de mensagem](email-template-custom.md#message-templates).

1. Em _[!UICONTROL Load default template]_, escolha o **[!UICONTROL Template]**que deseja personalizar.

1. Para aplicar um modelo, clique em **[!UICONTROL Load Template]**.

   A variável _[!UICONTROL Currently used for]_exibe o caminho de configuração do modelo. A variável_[!UICONTROL Template Subject]_ e _[!UICONTROL Template Content]_são gerados automaticamente em relação ao modelo selecionado.

   - **[!UICONTROL Template Subject]** - Esse texto é exibido na linha de assunto de um email.

   - **[!UICONTROL Template Content]** - Esse texto é exibido no conteúdo completo do email enviado.

   ![Conteúdo do modelo de email](./assets/email-template-content.png){width="600" zoomable="yes"}

1. Insira um **[!UICONTROL Template Name]**.

1. Para obter uma lista das [predefinido](variables-predefined.md) que podem ser usadas com esse modelo de email, clique em **[!UICONTROL Insert Variable]**.

   Determine qual variável você deseja inserir no modelo. Em seguida, clique em _Fechar_ (X) no canto superior direito. (Você voltará a isso mais tarde.)

1. Para ver um modelo do modelo, clique em **[!UICONTROL Preview Template]** na barra de botões.

   Quando a visualização for aberta em uma nova guia, determine onde deseja colocar a variável em relação ao outro conteúdo. Em seguida, retorne à guia original para continuar.

   ![Visualizar modelo](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. No **[!UICONTROL Template Content]** posicione o ponto de inserção onde deseja que a variável apareça e clique em **[!UICONTROL Insert Variable...]**.

1. Na lista de variáveis disponíveis, clique na que deseja inserir no modelo.

1. Quando terminar, clique em **[!UICONTROL Save Template]**.

## Converter o modelo em texto simples

1. Abra um modelo no modo de edição.

1. Na parte superior da página, clique em **[!UICONTROL Convert to Plain Text]**.

1. Quando solicitado a retirar as tags, clique em **[!UICONTROL OK]**.

1. Para salvar a versão de texto simples, clique em **[!UICONTROL Save Template]**.

## Restaurar a versão do HTML

1. Na parte superior da página, clique em **[!UICONTROL Return HTML Version]**.

1. Para salvar a versão do HTML do modelo, clique em **[!UICONTROL Save Template]**.
