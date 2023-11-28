---
title: Segurança
description: Saiba mais sobre as ferramentas disponíveis para proteger seus armazenamentos e dados e as diretrizes para um plano de ação de segurança se você detectar um comprometimento.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: 671ec7015c37b24ca0acc615ae3715b8b870a453
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Segurança

Há várias maneiras de proteger seu armazenamento e manter sua segurança de dados:

- Configurar [autenticação de dois fatores](security-two-factor-authentication.md)
- Implementar [CAPTCHA](security-captcha.md) ou [reCAPTCHA](security-google-recaptcha.md)
- Configurar um [Verificação de segurança](security-scan.md) para cada domínio na instalação do Adobe Commerce ou Magento Open Source.

Visite o [Central de segurança](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;} e ingresse no Registro de alertas de segurança para receber as últimas notícias sobre vulnerabilidades em potencial. Para obter informações sobre as práticas recomendadas de segurança, consulte [Proteger o site e a infraestrutura do Commerce](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) no _Manual de implementação_.

>[!NOTE]
>
>Lojas que foram habilitadas [!DNL Adobe Identity Management Services] (IMS) têm o Adobe Commerce nativo e o Magento Open Source 2FA desabilitado. Os usuários administradores que estão conectados à instância do Commerce com suas credenciais de Adobe não precisam se autenticar novamente para muitas tarefas de administrador. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [[!DNL Adobe Identity Management Service] Visão geral da integração do (IMS)](../getting-started/adobe-ims-integration-overview.md).

![Central de segurança](./assets/product-security-home.png){width="700" zoomable="yes"}

## Plano de ação de segurança

Se você suspeitar que o site do Adobe Commerce ou do Magento Open Source está comprometido, siga este plano de ação sem demora.

1. **Diagnosticar**: execute uma verificação para estabelecer o status de segurança da sua loja do Commerce. Commerce [Verificação de segurança](security-scan.md) O é um serviço gratuito oferecido pela Adobe que permite monitorar os sites do Commerce em busca de riscos de segurança e malware conhecidos e receber notificações de segurança.

1. **Limpar**: Contratar um [consultor qualificado](https://solutionpartners.adobe.com/s/directory/?partner_type=1) ou serviço online para limpar seu site de todos os códigos mal-intencionados. Alguns membros da comunidade do Commerce recomendam [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Verifique a `/media` pasta para código executável restante. Remova todos os usuários administradores desconhecidos e redefina todas as senhas de administradores.

1. **Protect**: mantenha sua instalação do Commerce atualizada com a versão mais recente. Se você estiver usando uma versão mais antiga, aplique todos os patches de segurança à medida que estiverem disponíveis. Revisar e acompanhar [Práticas recomendadas de segurança do Commerce](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Assinar o [Alertas de segurança do Commerce](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Relatório**: se você acha que encontrou uma vulnerabilidade específica no Commerce, [abra um problema com o Adobe](https://hackerone.com/adobe?type=team) e incluir detalhes técnicos.

1. **Atualizar**: para obter mais tranquilidade com o suporte 24 horas por dia, 7 dias por semana, planeje sua atualização para [Adobe Commerce em nossa arquitetura em nuvem](https://business.adobe.com/products/magento/cloud-delivery.html) agora.
