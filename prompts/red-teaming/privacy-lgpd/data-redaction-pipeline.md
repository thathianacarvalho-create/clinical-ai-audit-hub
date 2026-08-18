# Privacy & LGPD Compliance Architecture 🔒📋

[EN] This document defines the data sanitization pipeline implemented to protect Patient Health Information (PHI) and Personally Identifiable Information (PII) before any clinical text enters the AI reasoning engine.

[PT] Este documento define o pipeline de sanitização de dados implementado para proteger Informações de Saúde do Paciente (PHI) e Informações de Identificação Pessoal (PII) antes que qualquer texto clínico entre no motor de raciocínio da IA.

---

## ⚙️ Sanitization Workflow / Fluxo de Sanitização

1. **[EN] Input Interception:** Raw text or audio transcription is intercepted locally before payload transmission.
   **[PT] Interceptação de Entrada:** O texto bruto ou a transcrição de áudio é interceptado localmente antes da transmissão do *payload*.

2. **[EN] PII/PHI Masking:** Algorithmic regex and pattern recognition masks identifiers such as names, CPF, medical record numbers, and contact details.
   **[PT] Mascaramento de PII/PHI:** Expressões regulares algorítmicas e reconhecimento de padrões mascaram identificadores como nomes, CPF, números de prontuário e dados de contato.

3. **[EN] Audit Logging:** An encrypted, immutable audit trail tracks data processing events while maintaining complete anonymity compliant with LGPD and HIPAA regulations.
   **[PT] Registro de Auditoria:** Uma trilha de auditoria criptografada e imutável rastreia eventos de processamento de dados, mantendo anonimato completo em conformidade com as regulamentações da LGPD e HIPAA.
