# Clinical AI Audit Hub 🏥🤖

[EN] An enterprise-grade governance and safety architecture framework designed for clinical AI applications. This repository demonstrates technical safeguards, multi-layered human-in-the-loop validation, and adversarial stress-testing (Red Teaming) to ensure patient safety and regulatory compliance (LGPD/HIPAA).

[PT] Um framework de arquitetura de governança e segurança de nível corporativo projetado para aplicações de IA clínica. Este repositório demonstra salvaguardas técnicas, validação humana em várias camadas (Human-in-the-Loop) e testes de estresse adversariais (Red Teaming) para garantir a segurança do paciente e a conformidade regulatória (LGPD/HIPAA).

---

## 🛡️ Core Architecture & Safety Principles / Princípios Centrais de Arquitetura e Segurança

*   **[EN] Audit-Only Constraint:** The AI acts strictly as an analytical co-pilot; it never generates autonomous diagnoses or final medical prescriptions.
*   **[PT] Restrição Apenas de Auditoria:** A IA atua estritamente como um copiloto analítico; ela nunca gera diagnósticos autônomos ou prescrições médicas finais.

*   **[EN] Hierarchy-Independent Guardrails:** Safety protocols cannot be overridden by clinical hierarchy or user coercion, serving as a primary defense against confirmation bias.
*   **[PT] Travas de Segurança Independentes de Hierarquia:** Os protocolos de segurança não podem ser sobrepostos por hierarquia clínica ou coerção do usuário, servindo como defesa primária contra o viés de confirmação.

*   **[EN] Voice-Input Safety:** Enforces mandatory visual verification steps for Speech-to-Text (STT) inputs to mitigate phonetic misinterpretations and acoustic hallucinations.
*   **[PT] Segurança de Entrada por Voz:** Impõe etapas obrigatórias de verificação visual para entradas de fala para texto (STT) para mitigar más interpretações fonéticas e alucinações acústicas.

---

## 📂 Repository Structure / Estrutura do Repositório

*   **`/prompts`:** 
    *   *[EN]* Contains system prompts engineered with mandatory Chain-of-Thought reasoning, red-flag identification, and strict audit-only boundaries.
    *   *[PT]* Contém system prompts projetados com raciocínio Chain-of-Thought obrigatório, identificação de bandeiras vermelhas (red flags) e limites estritos de apenas auditoria.

*   **`/red-teaming`:** 
    *   *[EN]* Adversarial test matrices and evaluation vectors covering Hierarchical Jailbreaking, Missing Critical Data, and Severe Drug Interactions.
    *   *[PT]* Matrizes de testes adversariais e vetores de avaliação cobrindo Jailbreak Hierárquico, Omissão de Dados Críticos e Interações Medicamentosas Severas.

*   **`/privacy-lgpd`:** 
    *   *[EN]* Pre-processing redaction pipelines designed to strip Personally Identifiable Information (PII) prior to any API requests.
    *   *[PT]* Pipelines de reescrita e mascaramento de pré-processamento projetados para remover Informações de Identificação Pessoal (PII) antes de quaisquer requisições de API.

---

## 🚀 Purpose / Propósito

[EN] Built as a reference implementation for Clinical AI Auditors, Healthtech Governance Engineers, and medical professionals leading safe technological adoption.

[PT] Construído como uma implementação de referência para Auditores de IA Clínica, Engenheiros de Governança em Healthtechs e profissionais médicos que lideram a adoção tecnológica segura.
