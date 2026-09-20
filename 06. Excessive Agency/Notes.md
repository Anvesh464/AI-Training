# LLM06:2025 Excessive Agency – THREATS

Excessive Agency refers to the vulnerability arising when Large Language Models (LLMs) are granted more functionality, permissions, or autonomy than necessary. This can enable unintended or harmful actions due to unexpected, ambiguous, or manipulated outputs.

## Key Threats

- **Interaction with APIs** - LLMs may directly interact with APIs without proper validation, leading to unauthorized or harmful actions.
- **Plugin & Tool Invocation** - LLMs can invoke plugins, tools, or other applications/services, expanding their attack surface.
- **Business Logic Manipulation** - Attackers may trick LLMs into granting discounts, refunds, or other unintended financial/operational actions.
- **Server-Side Request Forgery (SSRF)** - In multi-chain or app integrations, LLMs can be manipulated to perform unauthorized backend requests.
- **Enterprise Service Interaction** - LLMs may interact with platforms such as Slack, Jira, Google Suite, or Email services, potentially exposing sensitive data or enabling privilege escalation.

<img width="1149" height="793" alt="image" src="https://github.com/user-attachments/assets/300456fa-90ce-4530-8c27-8cbeebff6c59" />

## LLM06:2025 Excessive Agency - REMEDIATION 
- Strict Action Boundaries & Guardrails (operational limits, execution) 
- Human Oversight & Approval Mechanisms (for high stake operations) 
- Minimal Privilege & API Access Controls (least privilege) 
- Explainability & Transparency (clear and justifiable justification process) 
- Behavior Monitoring & Anomaly Detection (establish baseline) 

# LLM06:2025 Excessive Agency – DESCRIPTION & RISKS

Excessive agency refers to an AI system being given too much autonomy or control, allowing it to make significant decisions or take actions without sufficient human oversight. This can lead to unintended, harmful, or unethical outcomes.

## Example - A malicious user is able to interact with backend APIs directly through the LLM.  
  ➝ This enables unauthorized operations and potential exploitation.
## Key Risks - **Unrestricted System Interfaces** - When LLMs interface with other systems without constraints, they may trigger undesirable operations or actions. Like web applications, LLMs should not be expected to self-police.  
  ➝ Security controls must be embedded within APIs and system boundaries to prevent misuse.

## What enables Excessive Agency? 
- Failing to implement sufficient human oversight and intervention mechanisms, allowing the Al to make significant decisions autonomously without human review. 
- Assigning Al systems too much control over critical tasks and decision-making processes without establishing checks and balances, which can lead to unintended or harmful outcomes.

- **Example 1** - An LLM is programmed to autonomously perform actions like purchasing or data deletion, but due to lack of constraints, it performs these actions inappropriately or excessively. 
- **Example 2** - LLM triggers actions outside LLM for example the LLM has access to email to read and summarize but then a malicious email arrives which will make LLM send spam. 
- **Example 3** - Or Customer Service LLM has payment access and can refund. Malicious prompt convinces LLM to refund 100 years.

<img width="1523" height="530" alt="image" src="https://github.com/user-attachments/assets/82ae3be1-86d4-45cd-8b2e-2355faea5c2f" />

# LLM06:2025 Excessive Agency – STEP BY STEP ATTACK PATH

1. LLM has access to APIs that can access sensitive information  
2. LLM can use APIs unsafely 
3. Think of the concept from SSRF 
4. Find out which APIs and plugins the LLM has access to 
5. Simply ask! 
6. If not compliant, re-ask, re-phrase, tell it you are the developer or admin

<img width="1504" height="544" alt="image" src="https://github.com/user-attachments/assets/4e066655-666d-432b-beab-037bf28e21cb" />
<img width="1524" height="536" alt="image" src="https://github.com/user-attachments/assets/6e95bbb2-6b84-4343-af24-5550ea8f11ca" />
<img width="1462" height="281" alt="image" src="https://github.com/user-attachments/assets/9f8d02d1-2fdb-4ef3-8553-722b2de24bbc" />
<img width="1510" height="439" alt="image" src="https://github.com/user-attachments/assets/450bb7c4-1d25-46f9-9a75-fe9e62f2f1a4" />

## How to prevent excessive agency? 
To prevent excessive agency in Al systems, implement sufficient human oversight and intervention mechanisms to review and approve critical decisions made by the Al. Additionally, establish clear boundaries and limits on the tasks and decisions delegated to the Al to ensure important actions always involve human judgment. 

https://portswigger.net/web-security/llm-attacks/lab-exploiting-vulnerabilities-in-llm-apis

### LLM06:2025 Insecure Plugin Design – THREATS

Insecure plugin design occurs when plugins or extensions for an AI system are poorly constructed, lacking proper security measures. Such weaknesses can be exploited by attackers to gain unauthorized access, manipulate the system, or introduce malicious code. Examples: An email plugin does not sanitize input, lack of authorization checks etc.. 

## Examples of Vulnerable Plugins

1. **Video** – May allow injection of malicious scripts in metadata or links.  
2. **Doc Maker** – Can be exploited to embed harmful macros or unauthorized content.  
3. **Diagram Maker** – Vulnerable to manipulation of rendering logic or injection attacks.  
4. **QR Code Generator** – Can encode malicious URLs or payloads.  
5. **HeyGen** – May expose sensitive data if not properly secured.  
6. **Code Plugin** – Risk of executing unsafe or unvalidated code snippets.  
7. **Email Plugin** – Without sanitization or authorization checks, attackers can send unauthorized emails or exfiltrate sensitive information.

<img width="1491" height="326" alt="image" src="https://github.com/user-attachments/assets/e4297267-a7da-4043-8a63-30a6178b19f6" />

## What enables Insecure Plugin Design? 
- Failing to conduct thorough security reviews and audits of plugins before integrating them, which can lead to the inclusion of insecure or malicious code. 
- Not properly isolating plugins from the core system, allowing plugins to have excessive permissions and access to critical system resources, which can be exploited by attackers. 

<img width="1460" height="538" alt="image" src="https://github.com/user-attachments/assets/e1ea630b-0cd5-4ccd-a11c-37c2bdb4d158" />

## More issues: 
- Authorization not tracked between plugins 
- Authentication performed without Authorization to particular plugin 
- Plugin may treat all LLM as user created and performs actions without Authorization.
- **Plugins chained together without Authorization (considerations of one plugin against another plugin.) 

<img width="1485" height="546" alt="image" src="https://github.com/user-attachments/assets/014302a0-d14f-4db8-a2ca-27f16a27dfe6" />
<img width="1520" height="486" alt="image" src="https://github.com/user-attachments/assets/7b3f1ac6-a672-4bd3-a299-2f5ae8e423b7" />
<img width="1500" height="521" alt="image" src="https://github.com/user-attachments/assets/27863c2f-8f1f-49ff-96d2-7e61cbcee091" />
<img width="1483" height="508" alt="image" src="https://github.com/user-attachments/assets/4d820891-229a-4e4c-8c80-c28799471bde" />

<img width="1211" height="835" alt="image" src="https://github.com/user-attachments/assets/d6095a70-8914-4ed9-a414-7b41f55c969d" />

<img width="1272" height="770" alt="image" src="https://github.com/user-attachments/assets/291598f0-01bf-4310-a1af-fb9dcdf1f24a" />
<img width="1205" height="834" alt="image" src="https://github.com/user-attachments/assets/94ca876d-f342-437a-932d-96d9d07254a3" />






