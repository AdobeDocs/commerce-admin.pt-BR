---
title: Referência de atributos de dados do cliente
description: Use essa referência de atributos de dados do cliente quando trabalhar com importações e exportações de dados do cliente.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Referência de atributos de dados do cliente

As tabelas a seguir listam os atributos de uma exportação típica do arquivo principal e dos endereços do cliente dos clientes. A instalação usada para exportar esses dados tem dois sites e várias exibições de loja, com os dados de amostra instalados.

Cada atributo, ou campo, é representado no arquivo CSV como uma coluna e os registros do cliente são representados por linhas. As colunas que começam com um sublinhado são entidades de serviço que contêm propriedades ou dados complexos.

## Arquivo principal do cliente

| Atributo | Descrição |
|--- |--- |
| `email` | O endereço de email do cliente. |
| `_website` |  |
| `_store` |  |
| `confirmation` | Sinalizador de confirmação. |
| `created_at` | A data em que a conta do cliente foi criada. |
| `created_in` | A exibição de loja onde a conta foi criada. |
| `disable_auto_group_change` | Determina se os grupos de clientes podem ser atribuídos dinamicamente durante a validação da ID de IVA. |
| `dob` | A data de nascimento do cliente. <br><br>**_Importante:_**De acordo com as práticas recomendadas atuais de segurança e privacidade, analise o armazenamento e o processamento da data de nascimento completa do cliente (mês, dia, ano). Quando coletados com outros identificadores pessoais (como_nome completo _), é um possível risco legal e de segurança. Recomendamos limitar o armazenamento das datas de nascimento completas dos clientes e, em vez disso, sugerimos usar o ano de nascimento do cliente como uma alternativa. |
| `firstname` | O nome do cliente. |
| `gender` | O sexo do cliente. |
| `group_id` | A ID do grupo de clientes ao qual o cliente está atribuído. |
| `lastname` | O sobrenome do cliente. |
| `middlename` | O nome do meio ou a inicial do meio do cliente. |
| `password_hash` | Hash de senha |
| `prefix` | Qualquer prefixo usado com o nome do cliente (como `Mr.`, `Ms.`, `Mrs.`, e `Dr.`). |
| `rp_token` | Redefinir token de senha. |
| `rp_token_created_at` | Data em que a senha foi redefinida. |
| `store_id` | ID da loja |
| `suffix` | Qualquer sufixo usado com o nome do cliente (como `Jr.`, `Sr.`, e `Esquire`). |
| `taxvat` |  |
| `website_id` | A ID do site onde a conta do cliente foi criada. |
| `password` | A senha do cliente. |

{style="table-layout:auto"}

## Endereços de clientes

| Atributo | Descrição |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | A cidade onde o endereço do cliente está localizado. |
| `company` | O nome da empresa, se aplicável para este endereço. |
| `country_id` | A ID do país onde o endereço do cliente está localizado. |
| `fax` | O número de fax do cliente, se aplicável. |
| `firstname` | O nome do cliente. |
| `lastname` | O sobrenome do cliente. |
| `middlename` | O nome do meio ou a inicial do meio do cliente. |
| `postcode` | O CEP onde o endereço do cliente está localizado. |
| `prefix` | Qualquer prefixo usado com o nome do cliente (como `Mr.`, `Ms.`, `Mrs.`, e `Dr.`). |
| `region` | A região onde o endereço do cliente está localizado. |
| `region_id` | ID da região |
| `street` | O endereço do cliente. Uma segunda linha do endereço está disponível, se especificada na configuração. |
| `suffix` | Se usado, o sufixo associado ao nome do cliente (como `Jr.`, `Sr.`ou `III`). |
| `telephone` | O número de telefone do cliente associado ao endereço. |
| `vat_id` | ID de IVA é um identificador interno do Número de IVA do cliente quando usado na Validação de IVA. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | Identifica o endereço de cobrança padrão. Um valor de `1` indica que o endereço é o endereço de faturamento padrão do cliente. Valores: 1 / 0 |
| `_address_default_shipping_` | Identifica o endereço de entrega padrão. Um valor de `1` indica que o endereço é o endereço de entrega padrão do cliente. Valores: `1` / `0` |

{style="table-layout:auto"}
