---
title: Configuração da página
description: Saiba como configurar os padrões para as partes principais de uma página de loja.
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Configuração da página

As seções principais da página são controladas, em parte, por um conjunto de tags padrão do HTML. Algumas dessas tags podem ser usadas para determinar a seleção de fontes, cor, tamanho, cores de fundo e imagens usadas em cada seção da página. Outras configurações controlam elementos da página, como o logotipo no cabeçalho e o aviso de copyright no rodapé. Essas seções correspondem à estrutura subjacente da página do HTML e muitas das propriedades básicas podem ser definidas pelo administrador.

- [HTML Head](#html-head)
- [Cabeçalho](#header)
- [Rodapé](#footer)

![seções de página do HTML](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## HTML Head

As configurações na seção HTML Head correspondem à tag `<head>` de uma página do HTML e podem ser definidas para cada exibição de loja. Além de metadados para o título da página, descrição e palavras-chave, a seção inclui um link para o favicon e scripts diversos. As instruções para robôs de mecanismo de pesquisa e a exibição do aviso de demonstração da loja também são configuradas nesta seção.

### Configurar o HTML Head

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de armazenamento que você deseja configurar e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Em _Outras Configurações_, expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL HTML Head]**.

   ![configurações do HTML Head](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. Atualize o [favicon](../getting-started/storefront-branding.md#add-a-favicon), se necessário.

1. Atualize as configurações de título da página de acordo com suas necessidades:

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   Você pode usar um sufixo e/ou prefixo com o título padrão para criar um título de duas ou três partes. Você pode adicionar uma barra vertical ou dois pontos como separador entre o prefixo ou sufixo e o título padrão.

1. Adicione ou modifique metadados compatíveis com a Otimização do mecanismo de pesquisa (SEO) e que ajudem a orientar os clientes para a sua loja a partir dos resultados da pesquisa:

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. Insira qualquer **[!UICONTROL Scripts and Style Sheets]**, conforme necessário.

   >[!NOTE]
   >
   >Todas as JavaScript inseridas no campo [!UICONTROL Scripts and Style Sheets] devem estar na lista de permissões nas configurações da Política de segurança de conteúdo (CSP), caso contrário, elas não serão executadas nas páginas de Check-out. Para obter mais informações, consulte [Política de Segurança de Conteúdo](https://developer.adobe.com/commerce/php/development/security/content-security-policies).


1. Habilite ou desabilite o [aviso de loja de demonstração](../getting-started/storefront-branding.md#set-the-store-demo-notice), se necessário.

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.

### Descrições do campo HTML Head

| Campo | Escopo | Descrição |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | Exibição da loja | Carrega a imagem gráfica pequena que aparece na barra de endereços e na guia do navegador. Tipos de arquivo permitidos: ICO, PNG, APNG, GIF e JPG (JPEG). Nem todos os navegadores suportam esses formatos. |
| [!UICONTROL Default Page Title] | Exibição da loja | O título que aparece na barra de título de cada página quando visualizado em um navegador. O título padrão é usado para todas as páginas, a menos que outro título seja especificado para páginas individuais. |
| [!UICONTROL Page Title Prefix] | Exibição da loja | Um prefixo pode ser adicionado antes do título para criar um título de duas ou três partes. Uma barra vertical ou dois pontos pode ser usada como separador no final do prefixo para diferenciá-lo do texto do título principal. |
| [!UICONTROL Page Title Suffix] | Exibição da loja | Um sufixo pode ser adicionado após o título para criar um título de duas ou três partes. Uma barra vertical ou dois pontos pode ser usada como separador no final do prefixo para diferenciá-lo do texto do título principal. |
| [!UICONTROL Default Meta Description] | Exibição da loja | A descrição fornece um resumo do site para listagens de mecanismos de pesquisa e não deve ter mais de 160 caracteres. |
| [!UICONTROL Default Meta Keywords] | Exibição da loja | Uma série de palavras-chave que descrevem sua loja, cada uma separada por vírgula. |
| [!UICONTROL Scripts and Style Sheets] | Exibição da loja | Contém scripts que devem ser incluídos na HTML antes da marca `<head>` de fechamento. Por exemplo, qualquer JavaScript de terceiros que deve ser colocada antes que a tag `<body>` possa ser inserida aqui. |
| [!UICONTROL Display Demo Store Notice] | Exibição da loja | Controla a exibição do aviso da loja de demonstração na parte superior da página. Opções: `Yes` / `No` |

{style="table-layout:auto"}

## Cabeçalho

A configuração de cabeçalho identifica o caminho para o logotipo da loja e especifica o texto alternativo do logotipo e a mensagem de boas-vindas.

![Configurações de cabeçalho](./assets/configuration-header.png){width="400" zoomable="yes"}

### Configurar o cabeçalho

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de armazenamento que você deseja configurar e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Em _Outras Configurações_, expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Header]**.

1. Faça as alterações necessárias para a exibição da loja:

   - Configurações do [Logotipo](../getting-started/storefront-branding.md#upload-your-logo)
   - Configurações de [Mensagem de boas-vindas](../getting-started/storefront-branding.md#change-the-welcome-message)

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.

### Descrições do campo de cabeçalho

| Campo | Escopo | Descrição |
|--- |--- |--- |
| [!UICONTROL Logo Image] | Exibição da loja | Identifica o caminho para o logotipo que aparece no cabeçalho. Tipos de arquivo compatíveis: PNG, GIF, JPG (JPEG) |
| [!UICONTROL Logo Attribute Width] | Exibição da loja | A largura da imagem do logotipo em pixels. |
| [!UICONTROL Logo Attribute Height] | Exibição da loja | A altura da imagem do logotipo em pixels. |
| [!UICONTROL Welcome Text] | Exibição da loja | A mensagem de boas-vindas é exibida no cabeçalho da página e inclui o nome dos clientes que estão conectados. |
| [!UICONTROL Logo Image Alt] | Exibição da loja | O texto Alt associado ao logotipo. |
| [!UICONTROL Translate Title] | Exibição da loja | Determina se o `Page Title` ou `Meta Title` deve ser traduzido. |

{style="table-layout:auto"}

## Rodapé

A seção Configuração do rodapé é onde você pode atualizar o [aviso de direitos autorais](../getting-started/storefront-branding.md#change-the-copyright-notice) que aparece na parte inferior da página e inserir scripts diversos que devem ser posicionados antes da marca `<body>` de fechamento.

![Configurações de rodapé](./assets/configuration-footer.png){width="400" zoomable="yes"}

### Configurar o rodapé

1. Na barra lateral _Admin_, vá para **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Localize a exibição de armazenamento que você deseja configurar e clique em **[!UICONTROL Edit]** na coluna _[!UICONTROL Action]_.

1. Em _Outras Configurações_, expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Footer]**.

1. Faça as alterações necessárias nas configurações de **[!UICONTROL Copyright]** e **[!UICONTROL Miscellaneous HTML]**.

   >[!NOTE]
   >
   >Todas as JavaScript inseridas no campo [!UICONTROL Miscellaneous HTML] devem estar na lista de permissões nas configurações da Política de segurança de conteúdo (CSP), caso contrário, elas não serão executadas nas páginas de Check-out. Para obter mais informações, consulte [Política de Segurança de Conteúdo](https://developer.adobe.com/commerce/php/development/security/content-security-policies).

1. Quando terminar, clique em **[!UICONTROL Save Configuration]**.

## Descrições do campo de rodapé

| Campo | Escopo | Descrição |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | Exibição da loja | Uma caixa de entrada na qual você pode carregar scripts diversos no servidor que devem ser colocados antes da marca `<body>` de fechamento. |
| [!UICONTROL Copyright] | Exibição da loja | A declaração de direitos autorais que aparece na parte inferior de cada página. Para incluir o símbolo de direitos autorais, use a entidade de caractere do HTML `\&copy;` como a seguir: `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` Substitua o exemplo de aviso de direitos autorais pelo seu próprio aviso. |
| [!UICONTROL Display Report Bugs Link] | Exibição da loja | Determina se o link do relatório de erros (suportado para alguns temas) está ativo ou desativado. |

{style="table-layout:auto"}
