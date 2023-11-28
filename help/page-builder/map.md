---
title: Mídia - Mapa
description: Saiba mais sobre o tipo de conteúdo do Mapa, usado para adicionar um mapa do [!DNL Google Maps] Platform para o [!DNL Page Builder] estágio.
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 0%

---

# Mídia - Mapa

Use o _Mapa_ tipo de conteúdo do qual adicionar um mapa [[!DNL Google Maps] Platform][1] para o [[!DNL Page Builder] estágio](workspace.md#stage). Por exemplo, você pode adicionar um mapa a um bloco e, em seguida, adicionar o bloco à [Sobre nós](../content-design/pages.md#about-us) e [Entre em contato](../getting-started/store-details.md#contact-us-form) páginas.

Para aproveitar ao máximo o [!DNL Google Maps] Platform, você pode personalizar o mapa, realçar os locais da loja e usar o Google [Places][2] para adicionar informações avançadas sobre sua loja a todos [!DNL Google Maps].

## Benefícios da incorporação de um mapa do Google

1. Fornece aos compradores um escopo completo de informações sobre sua empresa (número de telefone, site, avaliações, classificações de estrelas e assim por diante) diretamente no seu site.

1. Um mapa do Google geralmente destaca atrações próximas, parques, restaurantes e assim por diante. Essas informações ajudam os clientes a determinar sua localização física e planejar a viagem.

1. Facilita para os clientes encontrar o endereço de sua loja física sem a necessidade de abrir uma nova janela do navegador e sair do site.

1. Se você tiver uma cadeia de lojas físicas, adicionar um Mapa do Google no seu site ajudará a aumentar a percepção e a credibilidade da sua marca na forma de itens destacados.

![Exemplo de vitrine - mapear com localização](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Caixa de ferramentas de mapa

A caixa de ferramentas do mapa é exibida quando você passa o mouse sobre o container do mapa.

| Ferramenta | Ícone | Descrição |
|--- |--- |--- |
| Mover | ![Ícone Mover](./assets/pb-icon-move.png){width="25"} | Move o mapa para outra posição no palco. |
| (rótulo) | [!UICONTROL Map] | Identifica o contêiner de conteúdo atual como um mapa. Passe o mouse sobre o contêiner do mapa para ver a caixa de ferramentas. |
| Configurações | ![Ícone Configurações](./assets/pb-icon-settings.png){width="25"} | Abre a página Editar mapa, onde é possível alterar as propriedades do mapa e do container. |
| Ocultar | ![Ícone Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta o mapa atual. |
| Mostrar | ![Mostrar ícone](./assets/pb-icon-show.png){width="25"} | Mostra o mapa oculto. |
| Duplicar | ![Ícone Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Faz uma cópia do mapa. |
| Remover | ![Ícone Remover](./assets/pb-icon-remove.png){width="25"} | Exclui o mapa do estágio. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Configurar [!DNL Google Maps] para o seu administrador

Antes de adicionar um mapa, primeiro abra um [account][3] para obter uma avaliação gratuita do [!DNL Google Maps] Plataforma. O teste grátis dura 12 meses e inclui um crédito de 300 dólares. Se você consumir seu crédito, a Google não cobrará sua conta sem sua permissão.

### Etapa 1: Obtenha o seu [!DNL Google Maps] Chave de API

Se você já tiver um [!DNL Google Maps] , use um dos seguintes procedimentos para obter a chave de API necessária para a configuração. Para configurar um [!DNL Google Maps] , você deve ser um administrador do site autorizado a habilitar o faturamento de sua conta. Se você não estiver pronto para configurar um [!DNL Google Maps] Conta da Platform, você pode ignorar esta etapa e usar o mapa de espaço reservado por enquanto.

1. Vá para a [Console da Google Cloud Platform](https://cloud.google.com/console/google/maps-apis/overview).

1. Clique na lista suspensa do projeto e selecione ou crie o projeto ao qual deseja adicionar uma chave de API.

1. Para configurar suas credenciais de API, siga o [instruções][4] no [!DNL Google Maps] documentações.

1. Copie sua chave de API na área de transferência.

### Etapa 2: configurar [!DNL Google Maps] in [!DNL Commerce]

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Ferramentas de conteúdo avançadas](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Para obter mais informações sobre as opções de configuração das Ferramentas avançadas de gerenciamento de conteúdo, consulte [Guia de referência de configuração](../configuration-reference/general/content-management.md).

1. Para **[!UICONTROL Google Maps API Key]**, cole a chave copiada na etapa 1.

1. Clique em **[!UICONTROL Test Key]**.

   Se houver um problema com sua chave, volte para a guia [!DNL Google Maps] Site da plataforma para resolver o problema. Em seguida, tente novamente.

1. Após verificar sua chave, clique em **[!UICONTROL Save Config]**.

## Adicionar um mapa ao estágio

1. Abra a página, o bloco ou o bloco dinâmico no [!DNL Page Builder] espaço de trabalho.

1. No [!DNL Page Builder] painel, expandir **[!UICONTROL Media]** e arraste uma **[!UICONTROL Map]** espaço reservado para o estágio.

   ![Arrastar um mapa para o estágio](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Se [!DNL Google Maps] A plataforma está configurada para sua loja, um mapa é exibido para o local da loja.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Se [!DNL Google Maps] A plataforma ainda não está configurada para sua loja, um mapa de espaço reservado é exibido.

   ![[!DNL Google Maps] Espaço reservado](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Adicionar um local de mapa personalizado

1. Passe o mouse sobre o container do mapa para exibir a caixa de ferramentas e escolher o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

1. No canto superior direito da _[!UICONTROL Edit Map]_clique em **[!UICONTROL Add Location]**.

1. Insira o **[!UICONTROL Location Name]** que você deseja associar ao pino no mapa.

1. Colete as coordenadas de localização que deseja usar para a localização personalizada.

   Alternativamente, no **[!UICONTROL Position]** você pode arrastar o pino no mapa exibido.

   Se necessário, acesse [[!DNL Google Maps]][5] em uma nova janela do navegador e use um dos métodos a seguir para obter as coordenadas:

   ![Mapear coordenadas](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Método 1:** Copiar do URL

   - No canto superior esquerdo, digite o endereço no campo **[!UICONTROL Search]** e clique no botão _Pesquisar_ ( ![Ícone de pesquisa](../assets/icon-magnify-search.png){width="20"} ) ícone.

   - Copie as coordenadas no URL e cole-as em um bloco de notas.

   **Método 2:** Copiar de &quot;O que está aqui?&quot;

   - Clique com o botão direito do mouse no pino vermelho que marca o local no mapa e escolha **[!UICONTROL What's here?]** no menu.

   - No rótulo exibido, copie o texto, incluindo as coordenadas, e cole-o em um bloco de notas.

1. Insira os números, sem a vírgula, em cada um dos **[!UICONTROL Coordinates]** caixas.

   Também é possível inserir o máximo de informações restantes que você deseja que estejam disponíveis no mapa.

1. Preencha quaisquer outras informações que deseja associar ao local do mapa:

   | Opção | Descrição |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | O número de telefone do local. |
   | [!UICONTROL Street Address] | O endereço do local. |
   | [!UICONTROL City] | A cidade do local. |
   | [!UICONTROL Region/State] | A região ou o estado da localização. |
   | [!UICONTROL Zip/Postal Code] | O CEP do local. |
   | [!UICONTROL Country] | O país do local. |
   | [!UICONTROL Comment] | Todos os comentários que deseja incluir. |

   {style="table-layout:auto"}

1. Quando terminar, clique em **[!UICONTROL Save]**.

   A nova localização aparece no mapa e na grade de localização do mapa no _[!UICONTROL Edit Map]_página.

   ![[!DNL Page Builder] - mapeia a grade de localização](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## Estilo do mapa {#styling}

Use o [!DNL Google Maps] Assistente de estilo da plataforma para aplicar um dos seis temas predefinidos ou criar um tema personalizado. Você pode gerar um arquivo JSON com as propriedades de estilo do mapa ou um link para o mapa estilizado.

### Alterar o estilo do mapa

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. No **[!UICONTROL Google Maps Style]** caixa de texto, clique [Criar estilo do mapa][6].

   Essa ação abre a variável [[!DNL Google Maps] Assistente de estilo da plataforma][6] em uma guia separada, onde é possível definir um estilo para o [!DNL Google Maps] Projeto de plataforma.

1. Clique em **[!UICONTROL Create a Style]** e siga as instruções fornecidas.

   Quando terminar, clique em **[!UICONTROL Finish]**.

1. Exporte o estilo concluído como código JSON ou como um URL para que você possa adicioná-lo à [!DNL Commerce] configuração.

   - **JSON**: Abaixo da caixa com o código JSON gerado, clique em **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**: Abaixo da caixa com o URL gerado, clique em **[!UICONTROL Copy URL]**.

1. Retorne à guia do navegador Admin e cole o código ou URL gerado na **Estilo do Google Maps** caixa.

   Se você estiver usando um URL, substitua o `YOUR_API_KEY` espaço reservado com seu [!DNL Google Maps] Chave da API. Esse URL é vinculado ao seu Google Map estilizado.

1. No canto superior direito, clique em **[!UICONTROL Save Config]**.

### Alterar as configurações do mapa

1. Passe o mouse sobre o contêiner do mapa para exibir a caixa de ferramentas e escolha o _Configurações_ ( ![Ícone Configurações](./assets/pb-icon-settings.png){width="20"} ) ícone.

1. Altere as configurações básicas conforme necessário:

   | Opção | Descrição |
   | ------ | ----------- |
   | [!UICONTROL Height] | Especifica a altura do mapa exibido em pixels. |
   | [!UICONTROL Show Controls] | Determina se os controles padrão do Google Map são exibidos. |

   {style="table-layout:auto"}

1. Modifique o _[!UICONTROL Advanced]_configurações conforme necessário:

   - Para controlar o posicionamento horizontal do conteúdo do mapa adicionado ao contêiner, escolha um **[!UICONTROL Alignment]**:

     | Opção | Descrição |
     | ------ | ----------- |
     | `Default` | Aplica a configuração padrão de alinhamento especificada na folha de estilos do tema atual. |
     | `Left` | Alinha o conteúdo ao longo da borda esquerda do contêiner do mapa, com permissão para qualquer preenchimento especificado. |
     | `Center` | Alinha o conteúdo no centro do contêiner do mapa, com permissão para qualquer preenchimento especificado. |
     | `Right` | Alinha o conteúdo ao longo da borda direita do contêiner do mapa, com permissão para qualquer preenchimento especificado. |

     {style="table-layout:auto"}

   - Defina o **[!UICONTROL Border]** estilo aplicado aos quatro lados do contêiner de mapa:

     | Opção | Descrição |
     | ------ | ----------- |
     | `Default` | Aplica o estilo de borda padrão especificado pela folha de estilos associada. |
     | `None` | Não fornece nenhuma indicação visível das bordas do contêiner. |
     | `Dotted` | A borda do contêiner aparece como uma linha pontilhada. |
     | `Dashed` | A borda do contêiner aparece como uma linha tracejada. |
     | `Solid` | A borda do contêiner aparece como uma linha sólida. |
     | `Double` | A borda do contêiner aparece como uma linha dupla. |
     | `Groove` | A borda do contêiner é exibida como uma linha com ranhura. |
     | `Ridge` | A borda do contêiner aparece como uma linha estriada. |
     | `Inset` | A borda do contêiner aparece como uma linha interna. |
     | `Outset` | A borda do contêiner aparece como uma linha de saída. |

     {style="table-layout:auto"}

   - Se você definir um estilo de borda diferente de `None`, conclua as opções de exibição da borda:

     ![Cor da borda](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | Opção | Descrição |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Especifique a cor escolhendo uma amostra, clicando no seletor de cores ou inserindo um nome de cor válido ou um valor hexadecimal equivalente. |
     | [!UICONTROL Border Width] | Insira o número de pixels para a largura da linha de borda. |
     | [!UICONTROL Border Radius] | Insira o número de pixels para definir o tamanho do raio usado para arredondar cada canto da borda. |

     {style="table-layout:auto"}

   - (Opcional) Especifique os nomes dos **[!UICONTROL CSS classes]** na folha de estilos atual para aplicar ao contêiner do mapa.

     Separe vários nomes de classe com um espaço.

   - Insira valores, em pixels, para o **[!UICONTROL Margins and Padding]** para especificar as margens externas e o preenchimento interno do contêiner do mapa.

     Insira cada valor correspondente no diagrama do contêiner de mapa.

     | Área de contêiner | Descrição |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | A quantidade de espaço em branco aplicada à borda externa de todos os lados do container. |
     | [!UICONTROL Padding] | A quantidade de espaço em branco aplicada à borda interna de todos os lados do contêiner. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >O preenchimento não está disponível para o tipo de conteúdo do Mapa.

1. Quando terminar, clique em **[!UICONTROL Save]** para aplicar as configurações e retornar ao [!DNL Page Builder] espaço de trabalho.

### Alterar o tamanho da grade

O tamanho da grade determina o tamanho do mapa relacionado a um [coluna](column.md) no [!DNL Page Builder] estágio. Por padrão, o mapa tem 12 colunas de largura, com um máximo de 16 colunas.

1. No _Admin_ barra lateral, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, em _[!UICONTROL General]_, escolha **[!UICONTROL Content Management]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Atualize as opções de grade conforme necessário:

   >[!NOTE]
   >
   >Se necessário, limpe a caixa de seleção **[!UICONTROL Use system value]** para modificar essas configurações.

   - Para **[!UICONTROL Default Column Grid Size]**, insira um novo valor para o tamanho padrão da grade.

   - Para **[!UICONTROL Maximum Column Grid Size]**, insira um novo valor para o tamanho máximo de grade padrão.

   ![Configurações de tamanho da grade da coluna](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
