Here’s a clear side‑by‑side comparison in table format to highlight the difference between **Prompt Injection** and **Sensitive Information Disclosure**:

| Aspect | Prompt Injection | Sensitive Information Disclosure |
|--------|------------------|----------------------------------|
| **Definition** | A malicious attempt to manipulate an AI system by inserting crafted instructions into its input. | The unintended exposure of confidential or private data by the AI system. |
| **Primary Goal of Attacker** | To change the AI’s behavior, override safeguards, or force unintended actions. | To obtain sensitive data such as PII, credentials, financial details, or proprietary information. |
| **Attack Vector** | Crafted prompts in chat, poisoned documents, hidden instructions in websites, images, or other external sources. | Exploiting weak safeguards, misconfigured access, or successful prompt injection leading to data leakage. |
| **Impact** | AI may execute unauthorized tasks, generate harmful outputs, or bypass restrictions. | Loss of confidentiality, privacy breaches, regulatory violations, reputational damage. |
| **Example** | An attacker embeds hidden instructions in a PDF that makes the AI reveal internal system prompts. | The AI unintentionally outputs a customer’s credit card number or internal company secrets. |
| **Mitigation** | Input sanitization, isolation of untrusted sources, monitoring, and strict guardrails. | Data classification, access controls, redaction, encryption, and compliance frameworks. |

👉 Think of **prompt injection** as the *method of attack* (how the system is tricked), while **sensitive information disclosure** is often the *consequence* (what gets leaked).  

LLM02:2025 Sensitive Information Disclosure -
THREATS
Sensitive Information Disclosure refers to the unintended exposure of
confidential data—such as personal identifiable information (Pll), financial
records, health documents, business secrets, security credentials, and legal
materials—by large language models (LLMs), which can lead to
unauthorized access, privacy violations, and intellectual property breaches.
Return sensitive information
(Pll, PHI, Financial data, employee data, HR info, IP)
Return sensitive information from other the LLM itself, other internal
systems / applications
Return sensitive information from RAG storage or connected databases
Return sensitive training data
Return admin related information
