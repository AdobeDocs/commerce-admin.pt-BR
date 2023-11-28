---
title: Vendas e eventos privados
description: Saiba mais sobre como usar vendas privadas e outros eventos de catálogo para aumentar as vendas para sua base de clientes existente e gerar burburinho e novos leads.
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Vendas e eventos privados

{{ee-feature}}

Vendas privadas e outros eventos de catálogo são uma ótima maneira de usar sua base de clientes existente para gerar burburinho e novos leads ou para descarregar o inventário excedente. Você pode criar vendas por tempo limitado, limitar vendas a membros específicos ou criar uma página de venda privada independente. Você também pode definir convites e detalhes do evento. Aumente a fidelidade da marca e gere um burburinho ao oferecer aos melhores clientes o tratamento contra VIP. Ofereça acesso exclusivo a vendas somente para membros ou vendas privadas para aumentar a fidelidade à marca. Você também pode usar essas vendas para liquidar mercadorias em excesso. Grupos de clientes são úteis na configuração desses tipos de membros apenas e vendas de VIP.

![Exemplo de vitrine - evento na página inicial](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## Componentes de gerenciamento de eventos

- **Categorias** - Cada evento está associado a um [categoria](../catalog/category-create.md) do catálogo.

- **Eventos** - As vendas do evento são baseadas em uma data de início e término. Você pode usar um [contagem regressiva](#event-ticker) para mostrar o tempo restante.

- **Carrossel de eventos do catálogo** - Quando a variável [Widget de Evento de catálogo](../content-design/widget-event-carousel.md) estiver ativado na configuração, ele pode ser colocado nas páginas de armazenamento como uma lista de eventos abertos e futuros, classificados por data de término. Se dois ou mais eventos tiverem a mesma data de término, eles serão classificados com base na ordem especificada na configuração.

- **[!UICONTROL Websites]** - As permissões de categoria se baseiam principalmente no [grupos de clientes](../customers/customer-groups.md).

- **Permissões de categoria** - [Permissões de categoria](../catalog/category-permissions.md) O oferece controle total sobre as atividades específicas que podem ocorrer em determinada categoria.

- **Restrições de acesso** - Impede que [acesso](event-configure.md#restrict-access) para o site, redirecionando para uma página de aterrissagem, página de logon ou página de registro.

- **Convites** - Mensagens de email são enviadas com um link para criar uma conta na loja. É possível restringir a capacidade de criar uma conta somente àqueles que recebem uma [convite](invitations.md).

- **Relatórios de vendas privadas** - A [Relatórios de Vendas Privadas](../getting-started/private-sales-reports.md) forneça informações sobre convites enviados, clientes convidados e conversões.

## ticker de evento

O bloco de ticker exibe uma contagem regressiva para eventos abertos, com as datas de início e término para eventos futuros. Se um evento tiver sido fechado, o ticker mostrará as datas de início e término.

![Exemplo de vitrine - carrossel de eventos](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

Se o ticker da página de categoria estiver ativado para um evento, o bloco de ticker aparecerá na parte superior da listagem de categorias. Se o ticker da página do produto estiver ativado, o bloco de ticker também aparecerá na parte superior da página do produto de qualquer produto associado à categoria.

O ticker do evento pode ser ativado quando você [criação de eventos](event-create.md).

![Exemplo da loja - barra lateral do evento](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}
