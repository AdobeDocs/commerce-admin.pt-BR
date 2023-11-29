---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Revise as configurações no [!UICONTROL Security] &gt; [!UICONTROL Security.txt] página do Administrador do Commerce.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Para obter mais informações sobre a alteração dessas definições de configuração, consulte [Relatórios de problemas de segurança](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Geral](./assets/txt-general.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Enable] | Site | Quando ativado, um `security.txt` O arquivo salvo contém as informações necessárias aos pesquisadores de segurança para relatar possíveis vulnerabilidades a você. Opções:<br />**`Yes`**- Cria o `security.txt` arquivo com base nas informações inseridas na variável _Informações de contato_ e _Outras informações_ seções.<br />**`No`** - (padrão) Não cria a variável `security.txt` arquivo. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Informações de contato](./assets/txt-contact-info.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Email] | Site | O endereço de email para o qual os relatórios de segurança podem ser enviados. |
| [!UICONTROL Phone] | Site | Um número de telefone que pode ser usado para relatar problemas de segurança. |
| [!UICONTROL Contact Page] | Site | A URL de uma página do site que lista contatos de segurança ou seus _Entre em contato_ página. Exemplos: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Outras informações](./assets/txt-other-info.png)<!-- zoom -->

| Campo | [Escopo](../../getting-started/websites-stores-views.md#scope-settings) | Descrição |
|--- |--- |--- |
| [!UICONTROL Encryption] | Site | Um URL que aponta para o local de uma chave de criptografia que os pesquisadores de segurança podem usar para enviar comunicações criptografadas. _**Não insira a chave de criptografia neste campo.**_ <br/><br/>Cabe ao pesquisador verificar se a chave é de uma fonte confiável. Os pesquisadores não devem supor que a chave seja a mesma usada para gerar a assinatura digital. Exemplo:<br />Chave OpenPGP do servidor Web - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Site | Um URL que aponte para uma página em sua loja onde os pesquisadores de segurança são reconhecidos, como`https://mystore.com/hall-of-fame.html`. Para evitar ataques futuros, inclua apenas uma descrição geral sem revelar informações específicas sobre problemas de vulnerabilidade. Exemplo:<br />Gostaríamos de agradecer aos seguintes pesquisadores:<br />(aaaa/mm/dd) Justin Thyme - injeção de SQL |
| [!UICONTROL Preferred Languages] | Site | Especifica pelo menos um idioma preferencial do relatório de segurança. Separar vários caracteres [códigos de idioma](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) com vírgula. Todos os idiomas especificados têm a mesma prioridade. Por exemplo, para especificar inglês, espanhol e francês, digite `en, es, fr`. |
| [!UICONTROL Hiring] | Site | A URL de uma página no site que lista cargos relacionados à segurança. Exemplo: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Site | O URL da página que descreve sua política de segurança e as práticas de relatório de vulnerabilidade. Exemplo: `https://mystore.com/security-reporting.html` Padrão: `https://mystore.com/security` |
| [!UICONTROL Signature] | Site | Um link para seu arquivo de assinatura digital. A assinatura digital deve ser gerada a partir da linha de comando e é salva no `.well-known` no servidor. Para obter mais informações, consulte [Segurança.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) no GitHub. Exemplo: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
