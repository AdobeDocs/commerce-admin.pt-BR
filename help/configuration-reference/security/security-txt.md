---
title: '[!UICONTROL Security] > [!UICONTROL Security.txt]'
description: Revise as configurações na página [!UICONTROL Security] > [!UICONTROL Security.txt] do Administrador do Commerce.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
TQID: https://experienceleague.adobe.com/fXStEab1k6GKC5Tj7CStSGou3uNB-wJk5rZ-7EiFkcg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 360
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Para obter mais informações sobre como alterar essas configurações, consulte [Relatórios de problemas de segurança](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Geral](./assets/txt-general.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable] | Site | Quando habilitado, um arquivo `security.txt` é salvo e contém as informações necessárias aos pesquisadores de segurança para relatar possíveis vulnerabilidades a você. Opções:<br />**`Yes`**- Cria o arquivo `security.txt` com base nas informações inseridas nas seções _Informações de contato_ e _Outras informações_.<br />**`No`** - (padrão) Não cria o arquivo `security.txt`. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Informações de contato](./assets/txt-contact-info.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Email] | Site | O endereço de email para o qual os relatórios de segurança podem ser enviados. |
| [!UICONTROL Phone] | Site | Um número de telefone que pode ser usado para relatar problemas de segurança. |
| [!UICONTROL Contact Page] | Site | A URL de uma página do site que lista contatos de segurança ou a sua página _Fale Conosco_. Exemplos: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Outras informações](./assets/txt-other-info.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Encryption] | Site | Um URL que aponta para o local de uma chave de criptografia que os pesquisadores de segurança podem usar para enviar comunicações criptografadas. _**Não insira a chave de criptografia neste campo.**_ <br/><br/>É responsabilidade do pesquisador verificar se a chave é de uma fonte confiável. Os pesquisadores não devem supor que a chave seja a mesma usada para gerar a assinatura digital. Exemplo:<br />Chave OpenPGP do servidor Web - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Site | Uma URL que aponte para uma página em seu armazenamento onde pesquisadores de segurança são reconhecidos, como `https://mystore.com/hall-of-fame.html`. Para evitar ataques futuros, inclua apenas uma descrição geral sem revelar informações específicas sobre problemas de vulnerabilidade. Exemplo:<br />Gostaríamos de agradecer aos seguintes pesquisadores:<br />(aaaa/mm/dd) Justin Thyme - injeção de SQL |
| [!UICONTROL Preferred Languages] | Site | Especifica pelo menos um idioma preferencial do relatório de segurança. Separe vários [códigos de idioma](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) de dois caracteres com uma vírgula. Todos os idiomas especificados têm a mesma prioridade. Por exemplo, para especificar inglês, espanhol e francês, digite `en, es, fr`. |
| [!UICONTROL Hiring] | Site | A URL de uma página no site que lista cargos relacionados à segurança. Exemplo: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Site | O URL da página que descreve sua política de segurança e as práticas de relatório de vulnerabilidade. Exemplo: `https://mystore.com/security-reporting.html` Padrão: `https://mystore.com/security` |
| [!UICONTROL Signature] | Site | Um link para seu arquivo de assinatura digital. A assinatura digital deve ser gerada na linha de comando e é salva na pasta `.well-known` no servidor. Para obter mais informações, consulte [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) no GitHub. Exemplo: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
