# SaaS-Based-Credential-Harvesting-Google-Forms-

# 🛡️ PoC: SaaS-Based Credential Harvesting (Google Forms)

> ⚠️ **DISCLAIMER (AVISO LEGAL):**
> Este repositório contém material desenvolvido estritamente para fins educacionais e de conscientização em Segurança da Informação. O objetivo é demonstrar como plataformas legítimas (SaaS) podem ser abusadas por atacantes para contornar filtros de segurança tradicionais. O autor não se responsabiliza pelo uso indevido destas informações. **Nunca realize testes de penetração sem autorização explícita.**

## 📖 Sobre o Projeto
Este projeto é material de apoio para a aula sobre **"Criação e Impersonamento para Estratégias de Captura de Dados"**.

Diferente de ataques que utilizam malwares complexos ou ferramentas baseadas em Linux, este cenário explora o conceito de **Living off the Land (LotL)** aplicado a plataformas SaaS, combinado com automação de análise de dados via Python.

### 🎯 Cenário
- **Vetor de Ataque:** Google Forms (domínio legítimo e confiável).
- **Alvo Simulado:** Usuário corporativo ("Carlos") acostumado com o ecossistema G-Suite.
- **Técnica:** Engenharia Social + Abuso de Reputação de Domínio.
- **Análise:** Processamento automatizado de dados exfiltrados via Google Colab.

## 🚀 Estrutura do Ataque

1.  **OSINT:** Identificação do uso de G-Suite pela empresa alvo.
2.  **Setup:** Criação de formulário "oficial" mimetizando o RH/TI.
3.  **Bypass:** Utilização de domínios `docs.google.com` para evadir Secure Email Gateways (SEG).
4.  **Coleta:** Exfiltração de credenciais via Google Sheets em tempo real.
5.  **Processamento (C2 Simulado):** Uso de Python no Google Colab para triagem automática de alvos de alto valor (High Value Targets).

## 📊 Análise de Dados (Google Colab)
Este repositório inclui um **Jupyter Notebook** (`.ipynb`) executado no Google Colab que simula o painel de controle do atacante. O script realiza:

* **Simulação de Dataset:** Geração de massa de dados fake para testar o cenário.
* **Filtragem Inteligente:** Identificação automática de credenciais pertencentes a setores críticos (Diretoria, Financeiro).
* **Visualização:** Geração de gráficos (Matplotlib/Seaborn) para medir a eficácia da campanha por departamento.

Você pode visualizar ou executar o notebook clicando no botão "Open in Colab" no topo deste arquivo.

## 🛠️ Ferramentas Utilizadas
- **Coleta:** Google Forms
- **Armazenamento:** Google Sheets
- **Análise & Automação:** Google Colab (Python, Pandas, Seaborn)
- **Ofuscação:** Encurtadores de URL

## 🤝 Contribuição
Sinta-se à vontade para enviar PRs com novas estratégias de mitigação ou exemplos de *branding* defensivo.

