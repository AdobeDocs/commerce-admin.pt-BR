---
title: Personalizar modelos de email
description: Saiba como personalizar modelos de email para cada visualização de site, loja ou loja.
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# Personalizar modelos de email

O Commerce inclui um modelo de email padrão para a seção do corpo de cada mensagem enviada pelo sistema. O modelo para o conteúdo do corpo é combinado com os modelos de cabeçalho e rodapé para criar a mensagem completa. O conteúdo é formatado com HTML e CSS e pode ser facilmente editado e personalizado adicionando [variáveis](variables-predefined.md) e [widgets](../content-design/widgets.md). Os modelos de email podem ser personalizados para cada visualização de site, loja ou loja. Se estiver usando modelos personalizados, atualize o [configuração do sistema](email-templates.md#configure-email-templates) para garantir que o modelo correto seja usado.

![Exemplo - visualização do email de boas-vindas](./assets/email-template-preview.png){width="500" zoomable="yes"}

Os templates padrão incluem o logotipo e informações da loja e podem ser usados sem mais personalizações. No entanto, como prática recomendada, você deve visualizar cada modelo e fazer as alterações necessárias antes de enviá-los aos clientes.

- [Modelo do cabeçalho](email-template-custom.md#header-template)
- [Modelo de rodapé](email-template-custom.md#footer-template)
- [Modelos de mensagem](email-template-custom.md#message-templates)

![Modelos de email](./assets/email-templates.png){width="700" zoomable="yes"}

## Informações do modelo

| Campo | Descrição |
| ----- | ----------- |
| [!UICONTROL Template Name] | O nome do seu modelo personalizado. |
| [!UICONTROL Insert Variable] | Insere uma variável no modelo na posição do cursor. |
| [!UICONTROL Template Subject] | O Assunto do modelo aparece na coluna Assunto e pode ser usado para classificar e filtrar os modelos na lista. |
| [!UICONTROL Template Content] | O conteúdo do template no HTML. |
| [!UICONTROL Template Styles] | Quaisquer declarações de estilo CSS necessárias para formatar o modelo podem ser inseridas no campo _[!UICONTROL Template Styles]_caixa. |

{style="table-layout:auto"}

## Modelo do cabeçalho

Após concluir o [configuração](email-templates.md#configure-email-templates), o template do cabeçalho de email inclui o logotipo vinculado à loja. Se você tem um conhecimento básico de HTML, você pode facilmente usar [variáveis predefinidas](variables-predefined.md) para adicionar informações de contato da loja ao cabeçalho.

### Etapa 1. Carregar o modelo padrão

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Clique em **[!UICONTROL Add New Template]**.

1. No **[!UICONTROL Load default template]** clique na guia **[!UICONTROL Template]** seletor e escolha `Magento_Email` > `Header`.

   ![Cabeçalho do modelo de email - carregar modelo padrão](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. Clique em **[!UICONTROL Load Template]**.

   O código HTML e as variáveis do modelo aparecem no formulário.

### Etapa 2. Personalizar o modelo

1. Insira o **[!UICONTROL Template Name]** para o cabeçalho personalizado.

1. Insira um **[!UICONTROL Template Subject]** para ajudar a organizar os modelos.

   Na grade, a lista de modelos pode ser classificada e filtrada pela variável _[!UICONTROL Subject]_coluna.

   ![Informações de cabeçalho do modelo de email](./assets/email-template-information.png){width="600" zoomable="yes"}

1. No **[!UICONTROL Template Content]** , modifique o HTML conforme necessário.

   >[!NOTE]
   >
   >Ao trabalhar no código do modelo, tenha cuidado para não substituir nada que esteja entre chaves duplas.

1. Para inserir um [variável](variables-reference.md), posicione o cursor no código em que deseja colocar a variável e clique em **[!UICONTROL Insert Variable]**.

1. Escolha a variável que deseja inserir.

   ![Modelo de cabeçalho - Inserir variável](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   Quando uma variável é selecionada, uma variável [tag de marcação](markup-tags.md) para a variável é inserido no código.

   Embora as variáveis de armazenamento de endereço de email sejam as mais frequentemente incluídas no cabeçalho, você pode inserir o código para qualquer sistema ou [variável personalizada](variables-custom.md) diretamente no modelo.

1. Se você precisar fazer qualquer declaração CSS, insira os estilos no campo **[!UICONTROL Template Styles]** caixa.

1. Quando estiver pronto para revisar seu trabalho, clique em **[!UICONTROL Preview Template]**.

   Faça as alterações necessárias no modelo.

1. Quando terminar, clique em **[!UICONTROL Save Template]**.

   O cabeçalho personalizado agora aparece na lista de modelos de email disponíveis.

### Etapa 3. Atualizar a configuração

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Na grade, localize a exibição de armazenamento que deseja configurar e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Transactional Emails]** seção.

1. Escolha o **[!UICONTROL Header Template]** que é usado como padrão para notificações por email.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

![Configuração de design de email transacional - modelo de cabeçalho](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Modelo de rodapé

O rodapé do modelo de email contém a linha de fechamento e assinatura da mensagem de email. Você pode alterar o fechamento para ajustá-lo ao seu estilo e adicionar outras informações, como o nome da empresa e o endereço abaixo do seu nome.

### Etapa 1. Carregar o modelo padrão

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Clique em **[!UICONTROL Add New Template]**.

1. No **[!UICONTROL Load default template]** clique na guia **[!UICONTROL Template]** seletor e escolha `Magento_Email` > `Footer`.

1. Clique em **[!UICONTROL Load Template]**.

   O código HTML e as variáveis do modelo aparecem no formulário.

### Etapa 2. Personalizar e visualizar o modelo

1. Insira o **[!UICONTROL Template Name]** para seu rodapé personalizado.

1. Insira um **[!UICONTROL Template Subject]** para ajudar a organizar os modelos.

   Na grade, os templates podem ser classificados e filtrados pelo _[!UICONTROL Subject]_coluna.

   ![Rodapé do modelo de email - informações](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. No **[!UICONTROL Template Content]** , modifique o HTML conforme necessário.

   >[!NOTE]
   >
   >Ao trabalhar no código do modelo, tenha cuidado para não substituir nada que esteja entre chaves duplas.

1. Para inserir um [variável](variables-reference.md), posicione o cursor no código em que deseja colocar a variável e clique em **[!UICONTROL Insert Variable]**.

1. Escolha a variável que deseja inserir.

   Quando uma variável é selecionada, uma variável [tag de marcação](markup-tags.md) para a variável é inserido no código.

   Embora as variáveis de Contato da Loja sejam as mais frequentemente incluídas no rodapé, você pode inserir o código de qualquer sistema ou [variável personalizada](variables-custom.md) diretamente no modelo.

1. Se você precisar fazer qualquer declaração CSS, insira os estilos no campo **[!UICONTROL Template Styles]** caixa.

### Etapa 3. Atualizar a configuração

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Na grade, localize a exibição de armazenamento que deseja configurar e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Rolar para baixo e expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Transactional Emails]** seção.

1. Escolha o **[!UICONTROL Footer Template]** que é usado como rodapé padrão nas notificações por email.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

![Configuração de design de email transacional - modelo de rodapé](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Modelos de mensagem

O processo de personalização do corpo de cada mensagem é o mesmo que personalizar o cabeçalho ou rodapé. A única diferença é o modelo de mensagem para cada atividade ou evento que aciona uma notificação. Você pode usar os modelos como estão ou personalizá-los para corresponder à sua voz e marca. Além do texto do modelo, há uma grande variedade de opções [predefinido](variables-predefined.md) variáveis e [personalizado](variables-custom.md) variáveis que podem ser criadas e incorporadas ao modelo.

### Etapa 1. Carregar o modelo padrão

1. No _Admin_ barra lateral, vá para **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Clique em **[!UICONTROL Add New Template]**.

   ![Modelos de email - carregar modelo padrão](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. Faça o seguinte:

   - Em **[!UICONTROL Load default template]**, escolha o **[!UICONTROL Template]** que deseja personalizar.

   - Clique em **[!UICONTROL Load Template]**.

### Etapa 2. Personalizar o modelo

1. Para **[!UICONTROL Template Name]**, digite um nome para o modelo personalizado.

1. Se necessário, altere o **[!UICONTROL Template Subject]**.

   Esta é a primeira linha da mensagem, que é a saudação por padrão. Você pode deixá-la como está ou pode inserir algo mais descritivo.

1. Anote as **[!UICONTROL Currently Used For]** caminho para o modelo, que é o caminho usado para atualizar a configuração.

   ![Modelos de email - informações do modelo](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. No **[!UICONTROL Template Content]** , modifique o HTML conforme necessário.

   O conteúdo consiste em uma combinação de tags HTML, diretivas CSS, variáveis e texto.

   >[!NOTE]
   >
   >Ao trabalhar no código do modelo, tenha cuidado para não digitar acidentalmente sobre o código delimitado por chaves duplas.

1. Para inserir uma variável, posicione o cursor no código onde deseja que a variável apareça.

   A seleção de variáveis varia de acordo com o modelo e inclui as variáveis permitidas [predefinido](variables-predefined.md) e [personalizado](variables-custom.md) variáveis, se disponíveis.

1. Clique em **[!UICONTROL Insert Variable]** e escolha a variável que deseja inserir.

   Um comando para inserir a variável é delimitado por chaves e adicionado ao código no local do cursor. Por exemplo:

   `customVar code=my_custom_variable`

1. Para fazer declarações CSS, insira os estilos em **[!UICONTROL Template Styles]**.

   ![Modelos de email - adicionar estilos personalizados](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Os estilos personalizados são aplicados ao email somente se `{{template config_path="design/email/header_template"}}` está presente no _[!UICONTROL Template Styles]_. Para usar CSS personalizado sem um modelo de cabeçalho padrão, você deve fornecê-los aqui dentro do `<style>` tag HTML.

### Etapa 3. Atualizar a configuração

A variável _[!UICONTROL Currently Used For]_a trilha de navegação estrutural mostra onde o modelo é usado. Neste exemplo, a configuração do template está no estado_[!UICONTROL Customer Configuration]_ página, no campo _[!UICONTROL Create New Account Options]_e na seção_[!UICONTROL Default Welcome Email]_ campo.

- Página - [!UICONTROL Customer Configuration]
- Seção - [!UICONTROL Create New Account Options]
- Campo - [!UICONTROL Default Welcome Email]

1. No **[!UICONTROL Currently Used For]** caminho da navegação estrutural, clique no link para abrir a página de configuração do modelo.

   ![Modelo de email atual](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) seção e localize o campo referente ao modelo de email que você personalizou.

1. Limpe a **[!UICONTROL Use system value]** e clique no nome do seu modelo personalizado.

   ![Configuração de clientes - modelo de email de boas-vindas padrão](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Na mensagem localizada na parte superior do espaço de trabalho, clique em **[!UICONTROL Cache Management]** e limpe qualquer cache inválido.

### Etapa 4. Pré-visualizar e salvar o modelo

1. Quando estiver pronto para revisar seu trabalho, clique em **[!UICONTROL Preview Template]**.

1. Atualize o modelo conforme necessário.

1. Quando terminar, clique em **[!UICONTROL Save Template]**.

   Seu modelo personalizado agora está disponível na lista de modelos de email.
