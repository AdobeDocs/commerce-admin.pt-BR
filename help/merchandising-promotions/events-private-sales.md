---
title: Vendas e eventos privados
description: Saiba mais sobre como usar vendas privadas e outros eventos de catálogo para aumentar as vendas para sua base de clientes existente e gerar burburinho e novos leads.
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
badgePaas: label="Somente PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Aplica-se somente a projetos do Adobe Commerce na nuvem (infraestrutura do PaaS gerenciada pela Adobe) e a projetos locais."
TQID: https://experienceleague.adobe.com/8MvnlOp5muOQbx3b7dSKguc4wf-k47v9AtaHXu7b9pU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2: id: bd0aa680-a881-4f35-9dcf-843b0574bc5f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# Vendas e eventos privados

{{ee-feature}}

Vendas privadas e outros eventos de catálogo são uma ótima maneira de usar sua base de clientes existente para gerar burburinho e novos leads ou para descarregar o inventário excedente. Você pode criar vendas por tempo limitado, limitar vendas a membros específicos ou criar uma página de venda privada independente. Você também pode definir convites e detalhes do evento. Aumente a fidelidade da marca e gere um burburinho ao oferecer aos melhores clientes o tratamento para VIP. Ofereça acesso exclusivo a vendas somente para membros ou vendas privadas para aumentar a fidelidade à marca. Você também pode usar essas vendas para liquidar mercadorias em excesso. Os grupos de clientes são úteis na configuração desses tipos de membros apenas e nas vendas do VIP.

![Exemplo de vitrine - evento na página inicial](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## Componentes de gerenciamento de eventos

- **Categorias** - Cada evento está associado a uma [categoria](../catalog/category-create.md) do seu catálogo.

- **Eventos** - As vendas de eventos são baseadas em uma data de início e término. Você pode usar um [ticker de contagem regressiva](#event-ticker) para mostrar o tempo restante.

- **Carrossel de eventos do catálogo** - Quando o [widget de Evento do catálogo](../content-design/widget-event-carousel.md) está habilitado na configuração, ele pode ser colocado nas páginas de armazenamento como uma lista de eventos abertos e futuros, classificados por data de término. Se dois ou mais eventos tiverem a mesma data de término, eles serão classificados com base na ordem especificada na configuração.

- **[!UICONTROL Websites]** - Permissões de categoria baseadas principalmente em [grupos de clientes](../customers/customer-groups.md).

- **Permissões de categoria** - [Permissões de categoria](../catalog/category-permissions.md) oferecem controle total sobre as atividades específicas que podem ocorrer em uma determinada categoria.

- **Restrições de acesso** - Impede o [acesso](event-configure.md#restrict-access) público ao site, redirecionando para uma página de aterrissagem, página de logon ou página de registro.

- **Convites** - As mensagens de email são enviadas com um link para criar uma conta no armazenamento. Você pode restringir a capacidade de criar uma conta apenas àqueles que recebem um [convite](invitations.md).

- **Relatórios de vendas particulares** - Os [Relatórios de Vendas Particulares](../getting-started/private-sales-reports.md) fornecem informações sobre convites enviados, clientes convidados e conversões.

## ticker de evento

O bloco de ticker exibe uma contagem regressiva para eventos abertos, com as datas de início e término para eventos futuros. Se um evento tiver sido fechado, o ticker mostrará as datas de início e término.

![Exemplo de vitrine - carrossel de eventos](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

Se o ticker da página de categoria estiver ativado para um evento, o bloco de ticker aparecerá na parte superior da listagem de categorias. Se o ticker da página do produto estiver ativado, o bloco de ticker também aparecerá na parte superior da página do produto de qualquer produto associado à categoria.

O ticker de evento pode ser habilitado ao [criar eventos](event-create.md).

![Exemplo de vitrine - barra lateral do evento](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}
