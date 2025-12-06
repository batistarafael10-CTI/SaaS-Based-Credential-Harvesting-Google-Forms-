# ⚙️ Workflow Técnico: Execução da Simulação

Este documento detalha o passo a passo demonstrado na vídeo-aula para a criação da campanha de conscientização.

## Fase 1: Inteligência (OSINT)
Antes de criar o formulário, é necessário validar se a empresa alvo utiliza o ecossistema Google Workspace.
* **Verificação MX:** Checar registros MX do domínio (ex: `ASPMX.L.GOOGLE.COM`).
* **Motivo:** Enviar um link do Google para uma empresa que usa Office 365 gera desconfiança imediata.

## Fase 2: Construção do Payload (Google Forms)
A eficácia deste ataque reside na **Familiaridade Visual**.

### Configurações do Formulário:
1.  **Título:** Deve soar burocrático e urgente.
    * *Ex:* `Chamado #9921 - Validação de Acesso Corporativo`
2.  **Identidade Visual:** Upload do logo da empresa alvo no cabeçalho (Header).
3.  **Campos (Inputs):**
    * E-mail Corporativo (Texto)
    * Setor/Departamento (Dropdown - aumenta a legitimidade)
    * **Credencial de Acesso** (Texto)
        * *Obs:* Evitar a palavra "Senha" explicitamente para não ativar gatilhos de *phishing* automáticos do Google. Usar "Chave de Acesso", "PIN" ou "Validação".

### Configurações de Privacidade:
* [ ] Coletar e-mails automaticamente (DESMARCAR - para tornar o form público).
* [x] Restringir aos usuários da organização (DESMARCAR - necessário para acesso externo).

## Fase 3: Ofuscação do Link
O link cru do Google Forms é longo e suspeito para usuários atentos.

1.  Gerar link no Forms: `https://docs.google.com/forms/d/e/1FAIpQLS...`
2.  Utilizar encurtador (Bitly/Is.gd) com alias personalizado.
    * *Payload Final:* `is.gd/validacao-rh-interno`

## Fase 4: Exfiltração
Configurar a aba "Respostas" para enviar dados para uma nova planilha (**Google Sheets**). Isso atua como um painel de controle (C2) que não exige infraestrutura própria do atacante.
