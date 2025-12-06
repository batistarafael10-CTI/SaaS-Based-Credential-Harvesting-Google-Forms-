# SaaS-Based-Credential-Harvesting-Google-Forms-

# 🛡️ PoC: SaaS-Based Credential Harvesting (Google Forms)

> ⚠️ **DISCLAIMER (AVISO LEGAL):**
> Este repositório contém material desenvolvido estritamente para fins educacionais e de conscientização em Segurança da Informação. O objetivo é demonstrar como plataformas legítimas (SaaS) podem ser abusadas por atacantes para contornar filtros de segurança tradicionais. O autor não se responsabiliza pelo uso indevido destas informações. **Nunca realize testes de penetração sem autorização explícita.**

## 📖 Sobre o Projeto
Este projeto é material de apoio para a aula sobre **"Criação e Impersonamento para Estratégias de Captura de Dados"**. 

Diferente de ataques que utilizam malwares complexos ou ferramentas como *Setoolkit* em Linux, este cenário explora o conceito de **Living off the Land (LotL)** aplicado a plataformas SaaS.

### 🎯 Cenário
- **Vetor de Ataque:** Google Forms (domínio legítimo e confiável).
- **Alvo Simulado:** Usuário corporativo ("Carlos") acostumado com o ecossistema G-Suite.
- **Técnica:** Engenharia Social + Abuso de Reputação de Domínio.
- **Objetivo:** Demonstrar a falha humana e a ineficácia de filtros de e-mail baseados apenas em reputação de domínio.

## 🚀 Estrutura do Ataque
1.  **OSINT:** Identificação do uso de G-Suite pela empresa alvo.
2.  **Setup:** Criação de formulário "oficial" mimetizando o RH/TI.
3.  **Bypass:** Utilização de domínios `docs.google.com` para evadir Secure Email Gateways (SEG).
4.  **Coleta:** Exfiltração de credenciais via Google Sheets em tempo real.

## 🛠️ Ferramentas Utilizadas
- Navegador Web (Chrome/Firefox)
- Google Forms (Coleta)
- Google Sheets (C2 / Armazenamento)
- Encurtadores de URL (Ofuscação)

## 🤝 Contribuição
Sinta-se à vontade para enviar PRs com novas estratégias de mitigação ou exemplos de *branding* defensivo.
