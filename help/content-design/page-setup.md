---
title: Configuração da página
description: Saiba como configurar os padrões para as partes principais de uma página de loja.
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configuração da página

As seções principais da página são controladas, em parte, por um conjunto de tags HTML padrão. Algumas dessas tags podem ser usadas para determinar a seleção de fontes, cor, tamanho, cores de fundo e imagens usadas em cada seção da página. Outras configurações controlam elementos da página, como o logotipo no cabeçalho e o aviso de copyright no rodapé. Essas seções correspondem à estrutura subjacente da página do HTML e muitas das propriedades básicas podem ser definidas pelo administrador.

- [Cabeçalho do HTML](#html-head)
- [Cabeçalho](#header)
- [Rodapé](#footer)

![seções da página HTML](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## Cabeçalho do HTML

As configurações na seção Cabeçalho do HTML correspondem à variável `<head>` tag de uma página de HTML e pode ser configurada para cada visualização de loja. Além de metadados para o título da página, descrição e palavras-chave, a seção inclui um link para o favicon e scripts diversos. As instruções para robôs de mecanismo de pesquisa e a exibição do aviso de demonstração da loja também são configuradas nesta seção.

### Configure o HTML Head

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de loja que deseja configurar e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Em _Outras configurações_, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL HTML Head]** seção.

   ![Definições de configuração do HTML Head](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. Atualize o [favicon](../getting-started/storefront-branding.md#add-a-favicon) se necessário.

1. Atualize as configurações de título da página de acordo com suas necessidades:

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   Você pode usar um sufixo e/ou prefixo com o título padrão para criar um título de duas ou três partes. Você pode adicionar uma barra vertical ou dois pontos como separador entre o prefixo ou sufixo e o título padrão.

1. Adicione ou modifique metadados compatíveis com a Otimização do mecanismo de pesquisa (SEO) e que ajudem a orientar os clientes para a sua loja a partir dos resultados da pesquisa:

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. Insira qualquer **[!UICONTROL Scripts and Style Sheets]** conforme necessário.

1. Ative ou desative o [aviso da loja de demonstração](../getting-started/storefront-branding.md#set-the-store-demo-notice) se necessário.

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.

### Descrições do campo Cabeçalho do HTML

| Campo | Escopo | Descrição |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | Exibição da loja | Carrega a imagem gráfica pequena que aparece na barra de endereços e na guia do navegador. Tipos de arquivo permitidos: ICO, PNG, APNG, GIF e JPG (JPEG). Nem todos os navegadores suportam esses formatos. |
| [!UICONTROL Default Page Title] | Exibição da loja | O título que aparece na barra de título de cada página quando visualizado em um navegador. O título padrão é usado para todas as páginas, a menos que outro título seja especificado para páginas individuais. |
| [!UICONTROL Page Title Prefix] | Exibição da loja | Um prefixo pode ser adicionado antes do título para criar um título de duas ou três partes. Uma barra vertical ou dois pontos pode ser usada como separador no final do prefixo para diferenciá-lo do texto do título principal. |
| [!UICONTROL Page Title Suffix] | Exibição da loja | Um sufixo pode ser adicionado após o título para criar um título de duas ou três partes. Uma barra vertical ou dois pontos pode ser usada como separador no final do prefixo para diferenciá-lo do texto do título principal. |
| [!UICONTROL Default Meta Description] | Exibição da loja | A descrição fornece um resumo do site para listagens de mecanismos de pesquisa e não deve ter mais de 160 caracteres. |
| [!UICONTROL Default Meta Keywords] | Exibição da loja | Uma série de palavras-chave que descrevem sua loja, cada uma separada por vírgula. |
| [!UICONTROL Scripts and Style Sheets] | Exibição da loja | Contém scripts que devem ser incluídos no HTML antes do fechamento `<head>` tag. Por exemplo, qualquer JavaScript de terceiros que deve ser colocado antes da variável `<body>` tag pode ser inserida aqui. |
| [!UICONTROL Display Demo Store Notice] | Exibição da loja | Controla a exibição do aviso da loja de demonstração na parte superior da página. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## Cabeçalho

A configuração de cabeçalho identifica o caminho para o logotipo da loja e especifica o texto alternativo do logotipo e a mensagem de boas-vindas.

![Configurações do cabeçalho](./assets/configuration-header.png){width="400" zoomable="yes"}

### Configurar o cabeçalho

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de loja que deseja configurar e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Em _Outras configurações_, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Header]** seção.

1. Faça as alterações necessárias para a exibição da loja:

   - [Logotipo](../getting-started/storefront-branding.md#upload-your-logo) configurações
   - [Mensagem de boas-vindas](../getting-started/storefront-branding.md#change-the-welcome-message) configurações

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.

### Descrições do campo de cabeçalho

| Campo | Escopo | Descrição |
|--- |--- |--- |
| [!UICONTROL Logo Image] | Exibição da loja | Identifica o caminho para o logotipo que aparece no cabeçalho. Tipos de arquivos suportados: PNG, GIF, JPG (JPEG) |
| [!UICONTROL Logo Attribute Width] | Exibição da loja | A largura da imagem do logotipo em pixels. |
| [!UICONTROL Logo Attribute Height] | Exibição da loja | A altura da imagem do logotipo em pixels. |
| [!UICONTROL Welcome Text] | Exibição da loja | A mensagem de boas-vindas é exibida no cabeçalho da página e inclui o nome dos clientes que estão conectados. |
| [!UICONTROL Logo Image Alt] | Exibição da loja | O texto Alt associado ao logotipo. |
| [!UICONTROL Translate Title] | Exibição da loja | Determina se a variável `Page Title` ou `Meta Title` deve ser traduzida. |

{style="table-layout:auto"}

## Rodapé

A seção Configuração do rodapé é onde você pode atualizar o [aviso de copyright](../getting-started/storefront-branding.md#change-the-copyright-notice) que aparece na parte inferior da página e insira scripts diversos que devem ser posicionados antes de fechar `<body>` tag.

![Configurações do rodapé](./assets/configuration-footer.png){width="400" zoomable="yes"}

### Configurar o rodapé

1. No _Admin_ barra lateral, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de loja que deseja configurar e clique em **[!UICONTROL Edit]** no _[!UICONTROL Action]_coluna.

1. Em _Outras configurações_, expandir ![Seletor de expansão](../assets/icon-display-expand.png) o **[!UICONTROL Footer]** seção.

1. Faça as alterações necessárias no **[!UICONTROL Copyright]** e **[!UICONTROL Miscellaneous HTML]** configurações.

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.

## Descrições do campo de rodapé

| Campo | Escopo | Descrição |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | Exibição da loja | Uma caixa de entrada onde você pode carregar diversos scripts para o servidor, que deve ser colocada antes do fechamento `<body>` tag. |
| [!UICONTROL Copyright] | Exibição da loja | A declaração de direitos autorais que aparece na parte inferior de cada página. Para incluir o símbolo de copyright, use a entidade de caractere HTML `\&copy;` como no seguinte: `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` Substitua o exemplo de aviso de copyright pelo seu próprio aviso. |
| [!UICONTROL Display Report Bugs Link] | Exibição da loja | Determina se o link do relatório de erros (suportado para alguns temas) está ativo ou desativado. |

{style="table-layout:auto"}
