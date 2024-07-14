---
title: Conformidade com a CCPA
description: Saiba mais sobre a California Consumer Privacy Act (CCPA), que amplia os direitos dos consumidores na Califórnia para determinar como suas informações pessoais são coletadas, armazenadas e usadas.
exl-id: 165c8b78-683e-4015-b3c4-d3211750799e
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '2256'
ht-degree: 0%

---

# Conformidade com a CCPA

>[!NOTE]
>
>Essas informações são um tópico de uma série para ajudar os comerciantes e desenvolvedores da Adobe Commerce a entender as implicações da California Consumer Privacy Act. As informações baseiam-se no texto do estatuto. Para confirmar se a CCPA se aplica à sua empresa, consulte seu advogado.

A [California Consumer Privacy Act][5] (CCPA) amplia os direitos dos consumidores da Califórnia de determinar como suas informações pessoais são coletadas, armazenadas e usadas. A ênfase é a proteção dos consumidores contra a venda ou troca não autorizadas ou suas informações pessoais. A CCPA foi promulgada em 2018 e entrou em vigor em 1º de janeiro de 2020.

A CCPA concede os seguintes novos direitos aos consumidores:

- **Direito de saber** as categorias de informações pessoais sobre eles coletadas, usadas, compartilhadas ou vendidas nos últimos 12 meses.
- **Direito de excluir** determinados tipos de informações pessoais mantidas por uma empresa e/ou seus provedores de serviços.
- **Direito de recusar** a venda de suas informações pessoais.
- **Direito à não discriminação** em termos de preço ou serviço por ter exercido um direito de privacidade sob a CCPA.

Para fins da CCPA, as informações pessoais neste contexto são definidas como:

>As informações que identifiquem, estejam relacionadas com, descrevam, sejam susceptíveis de ser associadas a, ou possam razoavelmente estar ligadas, direta ou indiretamente, a um determinado consumidor ou residência. (Seção 1798.140)

A este respeito, abrange determinados elementos de dados que não podem ser considerados dados pessoais no contexto de outras leis ou regulamentos. Os comerciantes devem ter isso em mente ao determinar se e como eles devem cumprir a lei.

A CCPA também exige que as empresas forneçam _segurança razoável_ e inclui disposições ampliadas de proteção de dados para os consumidores, incluindo o direito de prosseguir com ações legais em caso de violação de dados.

Consulte seu advogado para determinar se e como você deve cumprir os requisitos da CCPA que podem ser aplicáveis a você e a sua empresa. Isso inclui os novos requisitos de aviso, recusa e manutenção de registros que as empresas devem implementar de acordo com a lei.

## Requisitos comerciais

A CCPA se aplica a empresas com fins lucrativos que realizam negócios na Califórnia e atendem a qualquer um dos seguintes itens:

- Têm uma receita anual bruta de mais de US$ 25 milhões
- Comprar, receber ou vender as informações pessoais de 100.000 ou mais residentes, residências ou dispositivos da Califórnia
- Obter 50% ou mais de sua receita anual com a venda de informações pessoais de residentes da Califórnia.

## Guia de conformidade da CCPA

Esta seção fornece uma descrição de alto nível das etapas necessárias para que os comerciantes cumpram com as regulamentações de privacidade, como a California Consumer Privacy Act (CCPA).

### GDPR e CCPA

Se for necessário que sua empresa esteja em conformidade com o [Regulamento Geral sobre a Proteção de Dados](compliance-gdpr.md) (GDPR) e a CCPA, você poderá usar parte do trabalho do seu programa de conformidade com o GDPR para a CCPA. Embora os regulamentos tenham algumas semelhanças, algumas diferenças incluem:

- A definição de informações pessoais difere para cada regulamento.
- O GDPR exige que os consumidores aceitem participar, antes que seus dados pessoais possam ser usados para determinados fins; a CCPA dá aos consumidores o direito de opt out.
- A CCPA tem requisitos adicionais de inventário e mapeamento de dados.
- Os regulamentos têm requisitos de política de privacidade diferentes.

As empresas que estiverem em conformidade com o GDPR podem ter obrigações adicionais nos termos da CCPA. Para saber mais, consulte a [Planilha da CCPA][3]{:target=&quot;_blank&quot;}.

### Roteiro de conformidade

É necessário um esforço coordenado para desenvolver e implementar um plano para abordar a conformidade. Use esse roteiro como um guia para mobilizar recursos e priorizar tarefas para que você possa seguir em várias frentes. O processo é essencialmente o mesmo para todas as instalações do [!DNL Commerce], com a seguinte exceção:

- **Adobe Commerce na infraestrutura em nuvem**: os comerciantes com lojas hospedadas no Adobe [infraestrutura em nuvem][4]{:target=&quot;_blank&quot;} podem solicitar ajuda ao gerente técnico de conta da Adobe Commerce ou ao Suporte ao cliente para responder às solicitações dos consumidores.

- **No local**: os comerciantes com instalações no local do Adobe Commerce ou Magento Open Source devem desenvolver seus próprios processos e ferramentas para responder e gerenciar solicitações de consumidores relacionadas a regulamentos de privacidade.

#### Etapa 1: Montar uma equipe multifuncional para lidar com a conformidade regulamentar

Monte uma equipe que represente as seguintes funções funcionais no seu negócio e agende uma sessão de treinamento para atualizá-las sobre a legislação. Em seguida, atribua as tarefas necessárias aos participantes por função.

- Estratégia e operações de negócios
- Legal
- Tecnologia da informação
- Experiência do usuário
- Atendimento ao cliente
- Suporte administrativo

De uma perspectiva comercial, você deve determinar se sua empresa estende essas medidas de proteção da privacidade somente aos consumidores da Califórnia ou se as disponibiliza para todos os consumidores, independentemente da localização.

#### Etapa 2: faça o inventário de suas propriedades digitais

**Partes Interessadas:** Tecnologia da Informação, Suporte Jurídico e Administrativo

Faça o inventário de suas propriedades digitais, incluindo todas as integrações e quem tem acesso aos dados do consumidor.

1. Determine quais informações pessoais públicas e privadas são coletadas por meio de seus sites e aplicativos móveis. Por exemplo, um banco de dados padrão do Commerce armazena os seguintes tipos de informações pessoais públicas e privadas:

   - **Público**: listas de desejos, análises de produtos

   - **Particular**: Informações Do Cliente, Informações Sobre Pedidos, Pontos De Recompensa, Registro De Presentes, Catálogo De Endereços, Crédito Da Loja, Métodos De Pagamento, Contratos De Cobrança, Assinaturas De Boletins Informativos, Convites.

     Se a instalação do [!DNL Commerce] tiver sido personalizada, informações pessoais adicionais poderão ser coletadas. As informações pessoais também podem residir em [cookies](./compliance-cookie-law.md), tags e outras tecnologias que coletam informações.

1. Identifique as partes com as quais você compartilha dados. A lista deve incluir prestadores de serviços e terceiros. Terceiros incluem redes de publicidade, provedores de serviços de internet, provedores de análise de dados, entidades governamentais, sistemas operacionais e plataformas, redes sociais e revendedores de dados do consumidor que não coletam informações pessoais diretamente de seus consumidores.

   - **Provedores de Serviços**: entidades que têm acesso aos dados de seus consumidores para fins comerciais e fornecem serviços em seu nome. Por exemplo, o Adobe é um provedor de serviços, assim como alguns desenvolvedores de personalizações, extensões e serviços.

     Verifique as configurações padrão do Google Universal Analytics, do Google Tag Manager e de quaisquer outros serviços de dados usados e faça as alterações necessárias para estar em conformidade com a regulamentação. Para saber mais, consulte [Configurações de Privacidade do Google](../merchandising-promotions/google-tools.md#google-privacy-settings).

   - **Outros Terceiros**: entidades com as quais você compartilha ou vende dados do consumidor. Por exemplo, você pode compartilhar dados do consumidor com uma rede de publicidade em troca de publicidade.

#### Etapa 3: Mapear a jornada do cliente e o processo de coleta de dados em suas lojas

**Partes Interessadas:** Experiência do Usuário, Tecnologia da Informação, Suporte Administrativo

1. Identifique cada ponto na [jornada do cliente] onde as informações pessoais são coletadas e o tipo de informações coletadas em cada etapa.

   Os visitantes do site devem ser notificados antecipadamente ou no ponto de coleta de dados. Por exemplo, uma loja sem integrações personalizadas coleta informações pessoais quando uma conta do cliente é criada e durante a finalização da compra. Se sua loja tiver integrações personalizadas, pode haver itens de dados e atributos adicionais para identificar.

1. Consulte os seguintes tópicos para obter diagramas de fluxo de dados aplicáveis e mapeamentos de entidade de banco de dados para cada versão:

   - [Referência de informações pessoais (2.x)][1]
   - [Referência de informações pessoais (1.x)][2]

   ![diagrama](./assets/privacy-frontend-diagram.svg)

#### Etapa 4: estabelecer procedimentos e mecanismos para responder às solicitações do cliente

**Partes Interessadas:** Atendimento Ao Cliente, Tecnologia Da Informação, Experiência Do Usuário, Suporte Administrativo

De uma perspectiva de gestão de dados, cada solicitação de informações pessoais envolve as seguintes partes:

- **Titulares dos dados** (Consumidores): na CCPA, qualquer pessoa na Califórnia que forneça informações pessoais para fazer uma compra e/ou manter uma conta de cliente pode enviar uma solicitação para acessar ou excluir seus dados pessoais.

- **Entidades agindo como Empresas no escopo da CCPA** (Marcas): [!DNL Commerce] comerciantes coletam e armazenam informações pessoais de seus clientes e convidados que fazem compras em suas lojas.

- **Processador de dados** (Fornecedores de tecnologia): a Adobe Commerce e a Magento Open Source atuam como processadores de dados pessoais armazenados como parte dos serviços fornecidos aos comerciantes. Como processador, a Adobe processa dados pessoais de acordo com a permissão e as instruções do comerciante, de acordo com o contrato de licença.

Os comerciantes são responsáveis por fazer o seguinte:

1. Identifique as partes envolvidas na Solicitação de acesso do titular de dados (DSAR) e verifique a identidade de qualquer pessoa que solicite conhecimento, recusa ou exclusão. Isso se aplica a uma pessoa que tem uma conta de cliente protegida por senha ou que faz compras em sua loja como convidado.

1. Divulgar e fornecer informações a um consumidor em resposta ao seu pedido de direitos no prazo de 45 dias a contar da recepção de um pedido do consumidor verificável, a menos que tal não seja possível. (A lei contém outros requisitos para que uma empresa mantenha a conformidade por atrasos de até 45 dias extras).

   Os comerciantes devem responder a cada DSAR dentro de 45 dias, a partir do dia em que a solicitação for recebida. Se necessário, os comerciantes podem levar até 45 dias a mais para responder, para um total máximo de 90 dias a partir do dia em que a solicitação é recebida. Isso exige que o comerciante notifique o cliente para explicar o motivo do atraso.

1. Desenvolva um mecanismo para apresentar as notificações necessárias na loja e coletar a resposta do consumidor.

1. Estabeleça procedimentos de resposta e documente cada uma das seguintes solicitações:

   - **Solicitações a Saber** - Os visitantes da sua loja devem ser informados sobre quaisquer acordos que você tenha para vender ou compartilhar suas informações pessoais com terceiros, e podem recusar. Os detalhes do uso de informações pessoais e as partes com as quais você compartilha ou vende dados podem ser mantidos em sua política de privacidade.

   - **Solicitações de recusa** - Se os dados pessoais forem vendidos ou transferidos para terceiros em troca de uma consideração valiosa, a CCPA exigirá um link _Não vender minhas informações_ em cada ponto em que forem coletados. Controles de entrada adicionais ativados pelo usuário, como caixas de seleção e botões, podem ser usados em comunicações por email, configurações de preferência de sites ou em formulários de sites no ponto de coleta de dados para que os indivíduos enviem uma solicitação de recusa válida.

   - **Solicitações para excluir**

      - Os comerciantes cujas lojas estão hospedadas na Adobe Commerce Cloud devem entrar em contato com o Suporte da Adobe para obter assistência na exclusão de informações pessoais. Entre em contato com o Gerente técnico de conta do Adobe ou com o Suporte ao cliente para obter mais informações.
      - Os comerciantes que executam instalações do Adobe Commerce ou Magento Open Source no local devem implementar seu próprio processo e script para excluir informações pessoais, mediante solicitação.

#### Etapa 5: gravar o conteúdo para as notificações do cliente necessárias

**Partes Interessadas:** Jurídico, Atendimento ao Cliente, Experiência do Usuário, Tecnologia da Informação, Suporte Administrativo

1. Em parceria com seu serviço jurídico, determine os tipos de avisos que devem ser adicionados ao seu site para atender às obrigações da CCPA.

   - **Aviso de coleta**: um aviso dado no momento ou antes do momento em que as informações pessoais são coletadas do consumidor. O aviso deve ser redigido em linguagem simples e de fácil compreensão para uma pessoa comum. O aviso deve ser visível e fornecido em um ou mais idiomas como o conteúdo do site.

   - **Aviso de Direito de Recusa**: um aviso que informa os consumidores sobre seu direito de recusar a venda de suas informações pessoais.

   - **Aviso de Incentivo Financeiro**: um aviso que explica cada incentivo financeiro, preço ou diferença de serviço que sua empresa recebe em troca de informações pessoais.

   - **Como Enviar uma Solicitação para Coleta e Uso de Informações Pessoais**: instruções para pessoas físicas enviarem uma solicitação para que você divulgue as informações pessoais coletadas sobre elas, incluindo:

      - Partes específicas de informações pessoais que você coletou sobre o consumidor
      - Categorias de informações pessoais que você coletou sobre o consumidor
      - Categorias de fontes de onde as informações pessoais são coletadas
      - Categorias de informações pessoais sobre o consumidor que você vendeu ou divulgou para um objetivo comercial
      - Categorias de terceiros a quem as informações pessoais foram vendidas ou divulgadas para fins comerciais
      - Os motivos pelos quais sua empresa coleta e/ou vende informações pessoais

1. Envie o conteúdo para a equipe e, se possível, seu advogado para análise.

1. Determine onde os avisos são exibidos, como eles funcionam (para cada visita, na autenticação ou por click-through) e sua posição e formato em relação a outro conteúdo.

1. Transmita o conteúdo aprovado para sua equipe de desenvolvimento.

#### Etapa 6: analisar seus contratos com os provedores de serviços

**Partes Interessadas:** Assistência Jurídica E Administrativa

Revise e, se necessário, atualize todos os contratos de provedor de serviços para refletir os requisitos da CCPA.

#### Etapa 7: atualizar sua política de privacidade

**Partes Interessadas:** Assistência Jurídica E Administrativa

Analise sua política de privacidade atual e considere se alguma divulgação adicional é necessária.

- **Uso de Informações Pessoais**: Você deve divulgar quais informações pessoais foram coletadas e quaisquer incentivos financeiros que receber em troca da venda de informações pessoais. Também é necessário explicar como o incentivo é permitido sob a CCPA e como o valor das informações pessoais é calculado.

- **Idade de Consentimento**: se você coletar ou usar informações pessoais sobre menores, poderá estar sujeito aos seguintes requisitos:

   - **Menores &lt; 13**: é necessária autorização dos pais para que menores de 13 anos aceitem a venda de suas informações pessoais.

   - **Menores de 13 anos a &lt; 16**: menores de 13 anos e menos de 16 anos podem optar pela venda de suas informações pessoais, desde que a empresa estabeleça um processo razoável para documentar a ação. O processo deve ser descrito na [política de privacidade](privacy-policy.md) da empresa. Quando uma empresa recebe pedidos de menores nesta faixa etária, deve informá-los do seu direito de opt out posteriormente e explicar como fazê-lo.

  >[!IMPORTANT]
  >
  >Os comerciantes estão proibidos de armazenar os dados pessoais de crianças na plataforma ou nos sistemas [!DNL Commerce]. Se houver motivos para acreditar que os dados coletados pertencem a uma plataforma menor, eles devem ser removidos de uma plataforma [!DNL Commerce] imediatamente para evitar a violação dos termos da licença do Adobe.

#### Etapa 8: documentar todos os procedimentos relacionados e manter registros

**Partes Interessadas:** Atendimento Ao Cliente, Suporte Administrativo

Por 24 meses após cada solicitação de direitos individual ser recebida, mantenha um registro da solicitação e da resposta da sua empresa.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m2.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m1.html
[3]: https://oag.ca.gov/system/files/attachments/press_releases/CCPA%20Fact%20Sheet%20%2800000002%29.pdf
[4]: https://www.adobe.com/commerce/magento.html
[5]: https://oag.ca.gov/privacy/ccpa
