---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Revise as configurações no [!UICONTROL General] &gt; [!UICONTROL Content Management] página do Administrador do Commerce.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![Opções WYSIWYG](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Exibição da loja | Determina se o editor está habilitado para o armazenamento. Opções: Ativado por padrão/Desativado por padrão/Desativado completamente |
| [!UICONTROL WYSIWYG Editor] | Site | Determina a versão do editor TinyMCE usada para o editor WYSIWYG. Opções: <br/>**`TinyMCE 5`**- (Padrão) Usa o TinyMCE versão 5 como o editor WYSIWYG padrão.<br><br>_** Nota:**_Uma atualização para a biblioteca TinyMCE 5.10 no Adobe Commerce e no Magento Open Source 2.4.5 resolve uma vulnerabilidade que permitia a execução arbitrária do JavaScript ao atualizar uma imagem ou link usando alguns tipos de URLs. O TinyMCE 3 foi descontinuado na versão 2.4.0 e removido na versão 2.4.3. O TinyMCE 4 foi removido na versão 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Global | Determina se [URLs estáticos](../../content-design/catalog-urls-dynamic-media.md) são usados para conteúdo de mídia referenciado do editor WYSIWYG. A configuração se aplica a todos os locais onde o editor WYSIWYG está disponível, incluindo produtos, categorias, páginas e blocos. Opções: <br/>**`Yes`**- Usa URLs estáticos para conteúdo de mídia inserido com o editor WYSIWYG. Os URLs estáticos são absolutos e quebrados se a variável [URL base](../../stores-purchase/store-urls.md) das alterações no armazenamento.<br/>**`No`** (Padrão) - Usa URLs dinâmicos para conteúdo de mídia inserido com o editor WYSIWYG, com base no  `{{media url="..."}}` diretiva. Os URLs dinâmicos são relativos e não se quebram se o URL de base do armazenamento for alterado. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![Hierarquia de página CMS](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Global | Ativa o uso da hierarquia de páginas para suas páginas de conteúdo. Opções: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Global | Oferece a capacidade de associar metadados a páginas na hierarquia. Opções: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Global | Determina o estilo de menu padrão. Opções: `Content` / `Left Column` / `Right Column` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Content Tools]

![Ferramentas de conteúdo avançadas](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Global | Determina se a variável [!DNL Page Builder] ferramentas avançadas de conteúdo estão disponíveis. Opções: <br/>**`Yes`**- A [!DNL Page Builder] O espaço de trabalho é exibido na seção Conteúdo de páginas, blocos, produtos e categorias.<br/>**`No`** - As ferramentas de edição CMS padrão aparecem no _[!UICONTROL Content]_seção de páginas, blocos, produtos e categorias. |
| [!UICONTROL Enable Page Builder Content Preview] | Global | Determina se a variável [!DNL Page Builder] as visualizações de conteúdo são ativadas para produtos e categorias. Opções: `Yes` / `No` <br/>**_Nota:_**Isso é definido como `Yes` por padrão, mas desativar a visualização pode impedir quaisquer problemas de desempenho resultantes do carregamento de visualizações em um formulário de produto ou categoria. |
| [!UICONTROL Google Maps API Key] | Global | A variável [!DNL Google Maps] Chave de API da sua conta Google. |
| [!UICONTROL Test Key] |  | Valida o [!DNL Google Maps] Chave da API. |
| [!UICONTROL Google Maps Style] | Global | Cole o [!DNL Google Maps] Estilize o código JSON aqui para alterar a aparência do tipo de conteúdo do Mapa. |
| [!UICONTROL Default Column Grid Size] | Global | Determina o número padrão de colunas na variável [!DNL Page Builder] grade. |
| [!UICONTROL Maximum Column Grid Size] | Global | Determina o número máximo de colunas na variável [!DNL Page Builder] grade. |

{:style=&quot;table-layout:auto&quot;}

>[!TIP]
>
>O Page Builder facilita a criação de páginas ricas em conteúdo com layouts personalizados que aprimoram a sua narrativa visual e impulsionam a participação e a fidelidade do cliente. Esses recursos foram projetados para melhorar a qualidade e reduzir o tempo e o custo de produção de páginas personalizadas. Para obter mais informações sobre esses recursos e como você pode usá-los para criar conteúdo envolvente para sua Adobe Commerce ou loja de Magento Open Source, consulte a [_Guia do usuário do Page Builder_](../../page-builder/guide-overview.md).

{:style=&quot;table-layout:auto&quot;}
