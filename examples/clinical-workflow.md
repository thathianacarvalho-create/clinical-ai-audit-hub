# Clinical Workflow Audit Simulation / Simulação de Auditoria de Fluxo Clínico 🏥🔍

[EN] This document simulates a real-world audit scenario using the Clinical AI Audit Hub framework. It demonstrates how the system intercepts a raw, unverified clinical query, strips out PII/PHI, applies regulatory and safety constraints, and produces an audited, human-in-the-loop output.

[PT] Este documento simula um cenário de auditoria do mundo real usando o framework do Clinical AI Audit Hub. Ele demonstra como o sistema intercepta uma consulta clínica bruta e não verificada, remove dados de identificação (PII/PHI), aplica restrições regulatórias e de segurança, e produz um resultado auditado com supervisão humana.

---

## 🛑 Step 1: Raw Input (Unsanitized) / Entrada Bruta (Não Sanitizada)
[EN] *Patient provides a raw prompt containing personal data and an ambiguous clinical request.*  
[PT] *O paciente fornece um prompt bruto contendo dados pessoais e uma solicitação clínica ambígua.*

> "Olá, meu nome é Maria Silva, CPF 123.456.789-00, moradora de São Paulo. Estou sentindo dores fortes no peito e falta de ar há 2 dias. Posso tomar o remédio X por conta própria para aliviar?"

---

## 🔒 Step 2: Privacy Redaction & PII/PHI Stripping / Sanitização de Privacidade
[EN] *The gateway pipeline automatically detects and masks all sensitive identifiers before it reaches the AI core.*  
[PT] *O pipeline de gateway detecta e mascara automaticamente todos os identificadores sensíveis antes que cheguem ao núcleo da IA.*

> `[REDACTED_NAME]`, `[REDACTED_ID]`, `[REDACTED_LOCATION]` relata dor precordial e dispneia há 48 horas. Pergunta sobre automedicação.

---

## ⚖️ Step 3: Regulatory & Safety Audit (Anvisa/LGPD Guardrails) / Auditoria Regulatória e de Segurança
[EN] *The AI core applies strict safety guardrails: it refuses autonomous diagnosis, flags severe red flags (chest pain), and enforces mandatory human medical review.*  
[PT] *O núcleo da IA aplica travas rígidas de segurança: recusa diagnóstico autônomo, sinaliza bandeiras vermelhas graves (dor no peito) e exige revisão médica humana obrigatória.*

*   **Risk Level / Nível de Risco:** 🔴 **HIGH (CRITICAL)** / ALTO (CRÍTICO)
*   **Red Flags Identified / Bandeiras Vermelhas Identificadas:** Chest pain + Shortness of breath (Potential Acute Coronary Syndrome).
*   **Action Protocol / Protocolo de Ação:** 
    *   [EN] Immediate referral to emergency medical care. Autonomous medication advice strictly blocked.
    *   [PT] Encaminhamento imediato para atendimento médico de emergência. Conselho de automedicação estritamente bloqueado.

---

## 🩺 Step 4: Human-in-the-Loop Final Output / Saída Final com Supervisão Humana
[EN] *The final validated response delivered to the healthcare professional/patient portal under strict medical oversight.*  
[PT] *A resposta final validada entregue ao profissional de saúde / portal do paciente sob rigorosa supervisão médica.*

> **[Clinical AI Auditor Safeguard Notice]**  
> Os sintomas relatados (dor no peito e falta de ar) constituem sinais de alerta clínico que exigem **avaliação médica presencial imediata**. A automedicação é contraindicada e pode mascarar condições graves. Procure o serviço de emergência mais próximo.  
> *Auditado e validado sob diretrizes de segurança clínica.*
