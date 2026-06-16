---
title: Segurança
description: Saiba mais sobre as ferramentas disponíveis para proteger seus armazenamentos e dados e as diretrizes para um plano de ação de segurança se você detectar um comprometimento.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
TQID: https://experienceleague.adobe.com/9aJ-ZVqwaIr2IJTY6e2hp3eoZe2v6sxz6WdqP2FiPTc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2: id: f8ddfd3b-6194-46e8-a176-0e918039be56
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 0%

---

# Segurança

Há várias maneiras de proteger seu armazenamento e manter sua segurança de dados:

- Configurar [autenticação de dois fatores](security-two-factor-authentication.md)
- Implementar o [CAPTCHA](security-captcha.md) ou o [reCAPTCHA](security-google-recaptcha.md)
- Configure uma [Verificação de Segurança](security-scan.md) para cada domínio na sua instalação do Adobe Commerce ou do Magento Open Source.

>[!NOTE]
>
>Os armazenamentos que habilitaram a autenticação [!DNL Adobe Identity Management Services] (IMS) têm o Adobe Commerce nativo e o Magento Open Source 2FA desabilitados. Os usuários administradores que estão conectados à instância do Commerce com suas credenciais do Adobe não precisam se autenticar novamente para muitas tarefas administrativas. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [[!DNL Adobe Identity Management Service] (IMS) Visão geral da integração](../getting-started/adobe-ims-integration-overview.md).

Visite a [Central de Segurança](https://helpx.adobe.com/security.html){:target="_blank"} para obter as últimas notícias sobre vulnerabilidades potenciais, registrar-se para receber notificações de Segurança do Adobe e acessar a Central de Confiabilidade da Adobe.

![Central de segurança](./assets/product-security-home.png){width="700" zoomable="yes"}

Para obter informações sobre as práticas recomendadas de segurança, consulte [Proteger o site e a infraestrutura do Commerce](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) no _Manual de implementação_.

## Plano de ação de segurança

Se você suspeitar que o site do Adobe Commerce ou do Magento Open Source está comprometido, siga este plano de ação sem demora.

1. **Diagnóstico**: execute uma verificação para estabelecer o status de segurança do repositório do Commerce. A [Verificação de Segurança](security-scan.md) do Commerce é um serviço gratuito oferecido pela Adobe que permite monitorar os sites da Commerce quanto a riscos de segurança e malware conhecidos e receber notificações de segurança.

1. **Limpar**: contrate um [consultor qualificado](https://solutionpartners.adobe.com/s/directory/?partner_type=1) ou serviço online para limpar todo o código mal-intencionado do seu site. Alguns membros da comunidade do Commerce recomendam [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Verifique se há código executável restante na pasta `/media`. Remova todos os usuários administradores desconhecidos e redefina todas as senhas de administradores.

1. **Proteger**: mantenha sua instalação do Commerce atualizada com a versão mais recente. Se você estiver usando uma versão mais antiga, aplique todos os patches de segurança à medida que estiverem disponíveis. Revise e siga as [práticas recomendadas de segurança da Commerce](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Assinar os [Alertas de Segurança do Commerce](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Relatório**: se você acha que encontrou uma vulnerabilidade específica no Commerce, [abra um problema com o Adobe](https://hackerone.com/adobe?type=team) e inclua detalhes técnicos.

1. **Atualização**: para obter mais tranquilidade do suporte 24 horas por dia, 7 dias por semana, planeje sua atualização para o [Adobe Commerce em nossa Arquitetura de Nuvem](https://business.adobe.com/products/magento/cloud-delivery.html) agora.
