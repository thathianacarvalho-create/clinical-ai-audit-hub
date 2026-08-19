# Clinical Workflow & AI Audit Simulation / Simulação de Fluxo Clínico e Auditoria de IA 🏥🩺

[EN] This document demonstrates a real-world clinical consultation workflow audited by the Clinical AI Audit Hub. It highlights how the system processes a structured medical anamnesis, monitors safety guardrails, and ensures that clinical decision-making remains strictly under physician oversight.

[PT] Este documento demonstra um fluxo de consulta clínica do mundo real auditado pelo Clinical AI Audit Hub. Ele destaca como o sistema processa uma anamnese médica estruturada, monitora travas de segurança e garante que a tomada de decisão clínica permaneça estritamente sob supervisão médica.

---

## 🏛️ Step 1: Clinical Anamnesis & Structured Intake / Anamnese Clínica e Coleta Estruturada
[EN] *The physician conducts a professional greeting and systematically investigates the chief complaint, pain characteristics, comorbidities, and current medications.*  
[PT] *O médico realiza a saudação profissional e investiga sistematicamente a queixa principal, características da dor, comorbidades e medicações em uso.*

> **Physician / Médico:** "Bom dia, sou a Dra. Tatiana. Estou realizando seu atendimento hoje nessa unidade de saúde. Qual o seu nome, idade, profissão e o que motivou a sua consulta?"  
> **Patient / Paciente:** "Bom dia, sou o Marcos, tenho 50 anos, sou motorista de aplicativo. Estou sentindo dores fortes no peito e falta de ar há 2 dias."  
> 
> **Physician / Médico:** "Entendido, Sr. Marcos. Vamos investigar melhor. Poderia descrever o tipo da dor, a intensidade dessa dor de 0 a 10, se ela irradia para o braço ou mandíbula, e se piora com o esforço?"  
> **Patient / Paciente:** "A dor é em aperto, intensidade 8/10, irradia para o braço esquerdo e piora quando ando."  
> 
> **Physician / Médico:** "Anotado. O senhor tem histórico de hipertensão, diabetes ou problemas cardíacos na família? faz uso contínuo de algum medicamento? fuma, faz uso de bebida alccólica, faz uso de drogras ilícitas"  
> **Patient / Paciente:** "Sou hipertenso, tomo losartana 50mg 1x ao dia. Minha mãe era hipertensa e diabética. Eu perguntei se podia tomar um Dipirona por conta própria para ver se aliviava o peito."

---

## 🔒 Step 2: Privacy Redaction & PII/PHI Stripping / Sanitização de Privacidade
[EN] *The gateway automatically sanitizes personal identifiers before transmitting clinical logs to the diagnostic assistant layer.*  
[PT] *O gateway sanitiza automaticamente os identificadores pessoais antes de transmitir os registros clínicos para a camada de assistente diagnóstico.*

> `[REDACTED_MALE_PATIENT]`, 50 anos. (Hipertenso, uso de losartana 50mg/dia. Histórico familiar: mãe HAS/DM). Relata dor precordial em aperto (8/10) com irradiação para membro superior esquerdo e dispneia aos esforços há 48h. Tentativa de automedicação relatada.

---

## 🔎 Step 3: RAG Query Generation (Clinical Knowledge Retrieval) / Geração de Consultas RAG
[EN] *Based on the sanitized data, the AI generates technical queries to securely fetch evidence-based medical guidelines, assisting the physician's diagnostic process.*  
[PT] *Com base nos dados sanitizados, a IA gera consultas técnicas para buscar de forma segura diretrizes médicas baseadas em evidências, auxiliando o processo diagnóstico do médico.*

> **Internal Search Queries Generated / Consultas Internas Geradas:**
> 1. "Protocolos de triagem para Síndrome Coronariana Aguda (SCA) em homem, 50 anos, com HAS e dor precordial aos esforços."
> 2. "Contraindicações de AINEs/analgésicos em suspeita de infarto agudo do miocárdio."

---

## ⚖️ Step 4: Regulatory & Safety Audit / Auditoria Regulatória e de Segurança
[EN] *The AI audit engine evaluates clinical red flags, blocks unauthorized medication recommendations, and enforces strict human-in-the-loop review.*  
[PT] *O motor de auditoria de IA avalia bandeiras vermelhas clínicas, bloqueia recomendações de medicação não autorizadas e exige revisão rigorosa de supervisão humana.*

*   **Risk Assessment / Avaliação de Risco:** 🔴 **HIGH / CRITICAL** (Chest pain + Spreading + Hypertension).
*   **Safety Interception / Interceptação de Segurança:** 
    *   [EN] Self-medication attempt intercepted. Differential diagnosis protocol triggered for physician review.
    *   [PT] Tentativa de automedicação (analgésico) estritamente interceptada devido ao risco mascaramento de isquemia.

---

## 🩺 Step 5: Human-in-the-Loop Clinical Output / Saída Clínica com Supervisão Humana
[EN] *The validated medical guidance delivered by the physician, backed by the AI safety audit log.*  
[PT] *A orientação médica validada entregue pelo médico, respaldada pelo registro de auditoria de segurança da IA.*

> **[Clinical Audit Summary & Physician Action]**  
> Diante do quadro de dor torácica típica com irradiação e fatores de risco (HAS familiar e pessoal), a conduta validada exige **encaminhamento imediato à sala de emergência** para realização de Eletrocardiograma (ECG) em até 10 minutos e dosagem de troponina. A automedicação foi vetada.  
> *Pipeline auditado e validado sob rigorosos padrões de segurança médica.*
