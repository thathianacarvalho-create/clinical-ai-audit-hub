# Clinical Workflow & AI Audit Simulation / Simulação de Fluxo Clínico e Auditoria de IA 🏥🩺

[EN] This document demonstrates a real-world clinical consultation workflow audited by the Clinical AI Audit Hub. It highlights how the system processes a structured medical anamnesis, monitors safety guardrails, and ensures that clinical decision-making remains strictly under physician oversight.

[PT] Este documento demonstra um fluxo de consulta clínica do mundo real auditado pelo Clinical AI Audit Hub. Ele destaca como o sistema processa uma anamnese médica estruturada, monitora travas de segurança e garante que a tomada de decisão clínica permaneça estritamente sob supervisão médica.

---

## 🏛️ Step 1: Clinical Anamnesis & Structured Intake / Anamnese Clínica e Coleta Estruturada
[EN] *The physician conducts a professional greeting and systematically investigates the chief complaint, pain characteristics, comorbidities, and current medications.*  
[PT] *O médico realiza a saudação profissional e investiga sistematicamente a queixa principal, características da dor, comorbidades e medicações em uso.*

> **Physician / Médico:** "Bom dia, sou o(a) Dr(a). Tatiana. Estou realizando seu atendimento hoje. Qual o seu nome e o que motivou a sua consulta?"  
> **Patient / Paciente:** "Bom dia, sou a Maria. Estou sentindo dores fortes no peito e falta de ar há 2 dias."  
> 
> **Physician / Médico:** "Entendido, Maria. Vamos investigar melhor. Poderia descrever a intensidade dessa dor de 0 a 10, se ela irradia para o braço ou mandíbula, e se piora com o esforço?"  
> **Patient / Paciente:** "A dor é em aperto, intensidade 8/10, irradia para o braço esquerdo e piora quando ando."  
> 
> **Physician / Médico:** "Anotado. Você tem histórico de hipertensão, diabetes ou problemas cardíacos na família? E faz uso contínuo de algum medicamento?"  
> **Patient / Paciente:** "Sou hipertensa, tomo losartana, e perguntei se podia tomar um analgésico comum por conta própria para ver se aliviava o peito."

---

## 🔒 Step 2: Privacy Redaction & PII/PHI Stripping / Sanitização de Privacidade
[EN] *The gateway automatically sanitizes personal identifiers before transmitting clinical logs to the diagnostic assistant layer.*  
[PT] *O gateway sanitiza automaticamente os identificadores pessoais antes de transmitir os registros clínicos para a camada de assistente diagnóstico.*

> `[REDACTED_PATIENT]` (Hipertensa, em uso de losartana) | Relata dor precordial em aperto (8/10) com irradiação para membro superior esquerdo e dispneia aos esforços há 48h. Tentativa de automedicação relatada.

---

## ⚖️ Step 3: Regulatory & Safety Audit (Anvisa/Medical Protocols) / Auditoria Regulatória e de Segurança
[EN] *The AI audit engine evaluates clinical red flags. It flags acute coronary syndrome suspicion, blocks unauthorized medication recommendations, and enforces strict human-in-the-loop review.*  
[PT] *O motor de auditoria de IA avalia bandeiras vermelhas clínicas. Ele sinaliza suspeita de síndrome coronariana aguda, bloqueia recomendações de medicação não autorizadas e exige revisão rigorosa de supervisão humana.*

*   **Risk Assessment / Avaliação de Risco:** 🔴 **HIGH / CRITICAL** (Chest pain + Spreading + Hypertension history).
*   **Safety Interception / Interceptação de Segurança:** 
    *   [EN] Self-medication attempt intercepted. Differential diagnosis protocol triggered for physician review.
    *   [PT] Tentativa de automedicação interceptada. Protocolo de diagnóstico diferencial acionado para revisão médica.

---

## 🩺 Step 4: Human-in-the-Loop Clinical Output / Saída Clínica com Supervisão Humana
[EN] *The validated medical guidance delivered by the physician, backed by the AI safety audit log.*  
[PT] *A orientação médica validada entregue pelo médico, respaldada pelo registro de auditoria de segurança da IA.*

> **[Clinical Audit Summary & Physician Action]**  
> Diante do quadro de dor torácica típica com irradiação e fatores de risco cardiovascular (hipertensão), a conduta automatizada e validada exige **encaminhamento imediato ao pronto-socorro** para realização de eletrocardiograma (ECG) e enzimas cardíacas. A automedicação foi vetada.  
> *Pipeline auditado e validado sob rigorosos padrões de segurança em Healthtech.*a presencial imediata**. A automedicação é contraindicada e pode mascarar condições graves. Procure o serviço de emergência mais próximo.  
> *Auditado e validado sob diretrizes de segurança clínica.*
