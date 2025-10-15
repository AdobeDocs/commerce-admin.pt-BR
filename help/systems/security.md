---
title: Segurança
description: Saiba mais sobre as ferramentas disponíveis para proteger seus armazenamentos e dados e as diretrizes para um plano de ação de segurança se você detectar um comprometimento.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: fede05a413428520eec89d46f41a1cdd9c9c3a2e
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Segurança

Há várias maneiras de proteger seu armazenamento e manter sua segurança de dados:

- Configurar [autenticação de dois fatores](security-two-factor-authentication.md)
- Implementar o [CAPTCHA](security-captcha.md) ou o [reCAPTCHA](security-google-recaptcha.md)
- Configure uma [Verificação de Segurança](security-scan.md) para cada domínio em sua instalação do Adobe Commerce ou do Magento Open Source.

>[!NOTE]
>
>Os armazenamentos que habilitaram a autenticação [!DNL Adobe Identity Management Services] (IMS) têm o Adobe Commerce nativo e o Magento Open Source 2FA desabilitado. Os usuários administradores que estão conectados à instância do Commerce com suas credenciais de Adobe não precisam se autenticar novamente para muitas tarefas de administrador. A autenticação é tratada pelo Adobe IMS quando o usuário administrador faz logon em sua sessão atual. Consulte [[!DNL Adobe Identity Management Service] (IMS) Visão geral da integração](../getting-started/adobe-ims-integration-overview.md).

Visite a [Central de segurança](https://helpx.adobe.com/br/security.html){:target=&quot;_blank&quot;} para obter as últimas notícias sobre vulnerabilidades em potencial, registre-se para receber notificações de segurança do Adobe e acesse a Central de Confiabilidade do Adobe.

![Central de segurança](./assets/product-security-home.png){width="700" zoomable="yes"}

Para obter informações sobre as práticas recomendadas de segurança, consulte [Proteger o site e a infraestrutura do Commerce](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=pt-BR) no _Manual de implementação_.

## Plano de ação de segurança

Se você suspeitar que o site do Adobe Commerce ou do Magento Open Source está comprometido, siga este plano de ação sem demora.

1. **Diagnóstico**: execute uma verificação para estabelecer o status de segurança do repositório do Commerce. A [Verificação de Segurança](security-scan.md) do Commerce é um serviço gratuito oferecido pelo Adobe que permite monitorar os sites da Commerce quanto a riscos de segurança e malware conhecidos e receber notificações de segurança.

1. **Limpar**: contrate um [consultor qualificado](https://solutionpartners.adobe.com/s/directory/?partner_type=1) ou serviço online para limpar todo o código mal-intencionado do seu site. Alguns membros da comunidade do Commerce recomendam [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Verifique se há código executável restante na pasta `/media`. Remova todos os usuários administradores desconhecidos e redefina todas as senhas de administradores.

1. **Protect**: mantenha sua instalação do Commerce atualizada com a versão mais recente. Se você estiver usando uma versão mais antiga, aplique todos os patches de segurança à medida que estiverem disponíveis. Revise e siga as [práticas recomendadas de segurança da Commerce](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Assinar os [Alertas de Segurança do Commerce](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Relatório**: se você acha que encontrou uma vulnerabilidade específica no Commerce, [abra um problema com o Adobe](https://hackerone.com/adobe?type=team) e inclua detalhes técnicos.

1. **Atualização**: para obter mais tranquilidade do suporte 24 horas por dia, 7 dias por semana, planeje sua atualização para o [Adobe Commerce em nossa Arquitetura de Nuvem](https://business.adobe.com/br/products/magento/cloud-delivery.html) agora.
