# 🛡️ Estratégias de Defesa e Mitigação

Como analistas de segurança, nosso objetivo é impedir que este ataque tenha sucesso. Abaixo estão as medidas recomendadas contra ataques baseados em formulários SaaS.

## 1. Treinamento e Conscientização (Camada Humana)
* **Regra de Ouro:** Nunca insira senhas em formulários do Google Forms, Microsoft Forms ou Typeform. Provedores de identidade legítimos (Okta, Azure AD, Google Auth) nunca usam formulários padrão para login.
* **Verificação de URL:** Treinar usuários para verificar se a URL de login corresponde exatamente ao domínio da empresa ou ao provedor de SSO oficial.

## 2. Implementação Técnica (Camada Lógica)
* **FIDO2 / WebAuthn:** A solução definitiva.
    * Chaves de segurança físicas (YubiKey, Titan) ou biométricas (TouchID/Windows Hello) vinculam o login ao domínio correto.
    * Se o usuário estiver em um site falso (ex: `docs.google.com` tentando passar por login corporativo), a chave de segurança **não funcionará**, impedindo o ataque mesmo que o usuário tente ceder seus dados.

## 3. Monitoramento e DLP
* **Bloqueio de Categorias:** Se possível, bloquear categorias de "Personal Cloud Storage" ou "Online Forms" para usuários que não necessitam dessas ferramentas.
* **Inspeção de Logs:** Monitorar tráfego de saída para domínios de formulários genéricos contendo padrões de POST suspeitos (embora difícil devido à criptografia HTTPS).

## 4. Branding Defensivo
* Personalizar a página de login real da empresa com uma imagem ou frase secreta que formulários genéricos não conseguem replicar facilmente.
