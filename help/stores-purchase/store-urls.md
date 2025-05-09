---
title: Armazenar URLs
description: Saiba mais sobre URLs de loja e como configurar a URL base e os códigos de loja.
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/pt-br/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# Armazenar URLs

Cada site em uma instalação do Adobe Commerce ou do Magento Open Source tem um URL base atribuído à loja e outro URL atribuído ao administrador. O Adobe usa variáveis para definir links internos em relação ao URL base, o que permite mover toda uma loja de um local para outro sem atualizar os links. URLs base padrão começam com `http` e URLs base seguras começam com `https`.

- **URL Base** — `http://www.yourdomain.com/magento/`
- **URL de Base Segura** — `https://www.yourdomain.com/magento/`
- **URL com endereço IP** — `http://###.###.###.###/magento/` ou `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>Não altere o URL de administração da configuração de URL base padrão. Para alterar o caminho ou a URL do Administrador, consulte [Usar uma URL de Administrador personalizada](#use-a-custom-admin-url).

## Usar um protocolo seguro

Os URLs de base da sua loja foram inicialmente configurados durante a instalação do Adobe Commerce. Se um certificado de segurança estava disponível no momento, você poderia especificar `HTTPS` URLs para serem usadas para o armazenamento, Admin ou ambos. Se a instalação do Adobe Commerce incluir várias lojas ou se você planejar adicionar mais lojas posteriormente, poderá incluir o código da loja no URL. Todos os recursos e operações do Adobe podem ser usados com protocolo seguro.

Se um certificado de segurança não estava disponível para o domínio no momento da instalação, atualize a configuração antes de iniciar o armazenamento. Depois que um certificado de segurança for estabelecido para o seu domínio, você poderá configurar uma ou ambas as URLs de base para operar com o protocolo SSL e o protocolo TLS [Transport Layer Security][1].

>[!IMPORTANT]
>
>A Adobe recomenda transmitir todas as páginas de um site de produção, incluindo páginas de conteúdo e de produtos, usando um protocolo seguro.

O Adobe Commerce e o Magento Open Source podem ser configurados para entregar todas as páginas em `HTTPS` por padrão. Se o armazenamento estiver funcionando com o protocolo padrão, você poderá melhorar a segurança habilitando o [HTTP Strict Transport Security][2] (HSTS) e atualizando todas as solicitações de página não seguras. HSTS é um protocolo de aceitação que impede que os navegadores renderizem páginas `HTTP` padrão que são transmitidas com protocolo não seguro para o domínio especificado. Como os mecanismos de pesquisa podem já ter indexado cada página do seu armazenamento com URLs `HTTP` padrão, você pode configurar o Commerce para atualizar automaticamente todas as solicitações de página não seguras para `HTTPS`, de modo que não perca tráfego. Quando o Commerce é configurado para usar URLs seguras para a loja e o Administrador, dois campos adicionais são exibidos para permitir que você habilite o `HSTS`.

## Configurar o URL de base

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Em _Geral_, no painel esquerdo, escolha **[!UICONTROL Web]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Base URL]**.

   - **[!UICONTROL Base URL]** — Insira a URL de base totalmente qualificada para sua loja. Certifique-se de finalizar o URL com uma barra, para que ele possa ser estendido com Chaves de URL adicionais de sua loja. Por exemplo: `http://yourdomain.com/`

     >[!NOTE]
     >
     >Não altere o espaço reservado no campo _[!UICONTROL Base Link URL]_. É um espaço reservado usado para criar links relativos ao URL de base.

   - **[!UICONTROL Base URL for Static View Files]** — (Opcional) Especifique um local alternativo para a URL base dos arquivos de exibição estáticos inserindo o caminho que começa com o seguinte espaço reservado:

     \{\{unsecure_base_url}}

   - **[!UICONTROL Base URL for User Media Files]** — (Opcional) Especifique um local alternativo para a URL base dos arquivos de mídia do usuário inserindo o caminho que começa com o seguinte espaço reservado:

     \{\{unsecure_base_url}}

     Para uma instalação típica, não há necessidade de atualizar os caminhos para os arquivos de visualização estáticos ou arquivos de mídia, pois eles são relativos ao URL base.

   ![Configuração geral - URLs de base Web](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Os espaços reservados entre chaves duplas são tags de marcação para variáveis.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Configurar o URL básico seguro

Se o domínio tiver um certificado de segurança válido, você poderá configurar os URLs da loja e do administrador para transmitir dados por um canal seguro (https). Sem um certificado de segurança válido, seu armazenamento não pode operar com o protocolo seguro (SSL/TLS).

1. Expanda ![Seletor de expansão](../assets/icon-display-expand.png) a seção _[!UICONTROL Base URLs (Secure])_ e faça o seguinte:

   ![Configuração geral - URLs de base segura](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]** — Insira o URL base seguro completo, seguido por uma barra. Por exemplo: `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]** — Não altere o espaço reservado no campo de URL do link base seguro. É usado para criar links relativos ao URL base seguro.

   - **[!UICONTROL Secure Base URL for Static View Files]** — (Opcional) Especifique um local alternativo para a URL base segura para arquivos de exibição estáticos inserindo o caminho que começa com o seguinte espaço reservado:

     \{\{secure_base_url}}

   - **[!UICONTROL Secure Base URL for User Media Files]** — (Opcional) Especifique um local alternativo para a URL de base segura dos arquivos de mídia do usuário inserindo o caminho que começa com o seguinte espaço reservado:

     \{\{secure_base_url}}

1. Para melhorar a segurança, defina as duas opções a seguir como `Yes`.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. Para _[!UICONTROL Enhanced Security Settings]_, faça o seguinte:

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]** — Se você quiser que seu armazenamento exiba apenas solicitações de página HTTPS seguras, defina como `Yes`.

   - **[!UICONTROL Upgrade Insecure Requests]** — Para atualizar qualquer solicitação de páginas HTTP não seguras padrão para proteger HTTPS, defina como `Yes`.

1. Defina o **[!UICONTROL Offloader Header]** para o seu servidor.

   A maioria das instalações do Commerce usa o `X-Forward-Proto` padrão para identificar o protocolo como `HTTP` ou `HTTPS`. Se a configuração do servidor usar um offloader_header diferente, insira-o aqui.

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

## Incluir o código de armazenamento em URLs

>[!NOTE]
>
>Quando a opção _Adicionar código de armazenamento a URLs_ estiver definida como `Yes`, você deverá incluir códigos de armazenamento nas URLs do navegador. Essa configuração garante que as regravações de URL sejam mapeadas corretamente e que todas as páginas sejam abertas com êxito, sem erros _&quot;Página 404 Não Encontrada&quot;_.

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Em _[!UICONTROL General]_, no painel esquerdo, escolha **[!UICONTROL Web]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL URL Options]**.

1. Defina **[!UICONTROL Add Store Code]** de acordo com sua preferência:

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![Configuração geral - Opções de URL da Web](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Clique no link **[!UICONTROL Cache Management]** na mensagem, na parte superior do espaço de trabalho. Em seguida, siga as instruções para atualizar o cache.

   ![Mensagem de gerenciamento de cache](./assets/msg-cache-management.png)

## Solução de problemas de URL

Se, após seguir as instruções de configuração, algumas páginas continuarem a ser fornecidas com a URL insegura (`http://`), faça o seguinte:

- Altere o URL de base (não seguro) para o URL HTTPS seguro.
- No servidor, edite o arquivo `.htaccess` (ou balanceador de carga) para que a URL não segura seja redirecionada para a URL segura.

## Usar um URL de administração personalizado

Como uma [prática recomendada de segurança](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=pt-BR), a Adobe recomenda que você use uma URL de Administrador exclusiva em vez do _admin_ padrão ou um termo comum, como _backend_. Embora não proteja diretamente o site contra um determinado mau ator, pode reduzir a exposição a scripts que tentam obter acesso não autorizado.

>[!NOTE]
>
>Verifique com seu provedor de hospedagem antes de implementar um URL de administrador personalizado. Alguns provedores de hospedagem exigem um URL padrão para atender às regras de proteção por firewall.

Em uma instalação típica, o URL e o caminho do administrador seguem imediatamente o URL de base. O caminho do Administrador é um diretório abaixo da raiz.

- **URL Base Padrão**: `http://yourdomain.com/magento/`
- **Caminho Padrão do Administrador**: `admin`
- **URL e Caminho Padrão do Administrador**: `http://yourdomain.com/magento/admin`

Embora seja possível alterar o URL do administrador e o caminho para outro local, qualquer erro remove o acesso ao administrador e deve ser corrigido do servidor.

>[!NOTE]
>
>Como precaução, não tente alterar o URL do administrador sozinho, a menos que você saiba como editar arquivos de configuração no servidor. Para projetos do Adobe Commerce implantados na infraestrutura em nuvem, altere a URL do Administrador seguindo as [instruções](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=pt-BR#admin-url) no *Guia do Adobe Commerce na Infraestrutura em Nuvem*.

### Método 1: alterar do Administrador

1. Na barra lateral _Admin_, vá para **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. No painel esquerdo, expanda **[!UICONTROL Advanced]** e escolha **[!UICONTROL Admin]**.

1. Expandir ![Seletor de expansão](../assets/icon-display-expand.png) a seção **[!UICONTROL Admin Base URL]**.

1. Defina as opções de configuração para o URL personalizado:

   ![Configuração avançada - URL de base do administrador](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   Se necessário, desmarque a caixa de seleção **[!UICONTROL Use system value]** para alterar a configuração.

   - Defina **[!UICONTROL Use Custom Admin URL]** como `Yes`.

   - Digite o **[!UICONTROL Custom Admin URL]**: `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >O URL do administrador deve estar na mesma instalação do Commerce e ter a mesma raiz do documento que a loja.

   - Defina **[!UICONTROL Custom Admin Path]** como `Yes`.

   - Para **[!UICONTROL Custom Admin Path]**, insira o caminho a ser usado como o nome da pasta de administração personalizada.

     Exemplo: `sample_custom_admin`

1. Quando terminar, clique em **[!UICONTROL Save Config]**.

1. Depois que as alterações forem salvas, saia do Administrador e faça logon novamente usando o novo URL e caminho do Administrador.

### Método 2: alterar o caminho Admin a partir da linha de comando do servidor

1. Abra o arquivo `app/etc/env.php` em um editor de texto e altere o valor do parâmetro `frontName` da seção `backend`. Em seguida, salve o arquivo.

   Use somente caracteres minúsculos.

   >[!NOTE]
   >
   >   Esse método permite alterar o Caminho do administrador, mas não o URL do administrador.

   >[!TIP]
   >
   >Para o Adobe Commerce na infraestrutura em nuvem, você pode configurar um caminho de administrador personalizado usando a variável `ADMIN_URL` na interface de usuário da nuvem. Consulte o [tópico sobre variáveis de administrador](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=pt-BR) no _Guia do Commerce na Infraestrutura da Nuvem_.

   - **Caminho Padrão do Administrador**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **Novo Caminho do Administrador**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. Use um dos seguintes métodos para limpar o cache:

   - Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Em seguida, clique em **[!UICONTROL Flush Magento Cache]**.
   - No servidor, execute o seguinte:

     ```bash
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >As alterações feitas usando o Método 1 têm prioridade sobre as alterações feitas no arquivo `app/etc/env.php`.

### Método 3: alterar o caminho do administrador usando a CLI do Commerce

Você pode usar o comando `setup:config:set` da CLI para alterar o Caminho do Administrador. O exemplo a seguir usa a opção `--backend-frontname` para alterar o caminho da raiz do Commerce para um novo caminho de Administrador:

```bash
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

Este comando atualiza a opção de configuração `backend` > `frontName` no arquivo `app/etc/env.php`.

## Restaurar o URL e o caminho do administrador padrão

Caso tenha definido um URL de administrador inválido ou um Caminho do administrador e tenha perdido o acesso ao back-end, há uma maneira de corrigi-lo na linha de comando.

1. Para reverter para o URL padrão do Administrador, execute este comando:

   ```bash
   php bin/magento config:set admin/url/use_custom 0
   ```

1. Para reverter para o Caminho do Administrador padrão (definido em `app/etc/env.php`, conforme descrito no Método 2), execute este comando:

   ```bash
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. Use um dos seguintes métodos para limpar o cache:

   - Na barra lateral _Admin_, vá para **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Em seguida, clique em **[!UICONTROL Flush Magento Cache]**.
   - No servidor, execute o seguinte:

     ```bash
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
