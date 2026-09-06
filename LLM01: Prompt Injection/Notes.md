## LLM01: Prompt Injection

Prompt Injection refers to a security vulnerability where adversarial inputs manipulate large language models (LLMs) into unintended behaviors, such as revealing confidential information or executing unauthorized actions. 

Direct Prompt Injection: (
Indirect Prompt Injection: (any documents, websites, source code, images, audio, video, emails, invisible prompts, data exfiltration via indirect prompt injection) 

# 🔐 Prompt Injection Types

## ⚡ Direct Prompt Injection
- **Definition**: Mtext in chat, API, invisible prompts ASCII, ANSI, Emojis etc.)  
- **Example**: A user hides a command in emoji text that tricks the LLM into revealing sensitive data.

## 🎯 Indirect Prompt Injection
- **Definition**: Malicious instructions hidden in external sources the LLM processes 📄 Documents, 🌐 Websites, 💻 Source code, 🖼️ Images, 🎧 Audio, 🎥 Video, 📧 Emails, 🕶️ Invisible prompts.  
- **Example**: A poisoned PDF or webpage embeds hidden instructions that cause the LLM to exfiltrate data.

### 🔓 Jailbreaking
- is effectivrly getting information Forcing the model to bypass its built-in safety rules or restrictions.  
- Often done by crafting clever prompts that trick the model into revealing hidden capabilities like making bomb,
- Example: Trick LLM into giving hacking steps despite restrictions.  
   
### 🧠 Memory Manipulation
- Exploiting how AI systems store or recall information (Altering what AI recalls (e.g., injecting false facts so future answers change).
- Attackers may try to insert, alter, or erase memory to influence future outputs.
- Example: Injecting false facts so future answers repeat attacker’s narrative.  

### 🎭 Multi-Modal Prompt Injection - images, audio or video
- Extending prompt injection attacks beyond text, using **images, audio, or other input types**.  
- Example: hiding malicious instructions inside an uploaded image that the AI interprets and Embedding secret text in an image that tells the LLM to leak data.

### 🔗 Multi-Chain Prompt Injection
- A more complex attack where instructions are spread across **multiple prompts or steps**.  
- The AI is manipulated gradually, making detection harder since the malicious intent unfolds over a chain of interactions.
- Chained LLM Workflow → In a corporate environment, multiple LLMs are linked so that the output of LLM‑1 becomes the input of LLM‑2, whose output then feeds LLM‑3, with APIs invoked along the chain (e.g., LLM‑1 extracts data → LLM‑2 transforms it → LLM‑3 calls an API for action).
```markdown
# Corporate LLM Chaining Architecture

## Flow Diagram

LLM-1 ➝ LLM-2 ➝ LLM-3 ➝ API Calls

### Example Workflow
1. **LLM-1** → Extracts structured data from raw input  
   *(e.g., parses customer query)*  

2. **LLM-2** → Transforms or enriches the data  
   *(e.g., converts into SQL or JSON)*  

3. **LLM-3** → Executes logic and triggers external APIs  
   *(e.g., calls CRM or payment gateway)*  

4. **API Response** → Returned to user or system dashboard
```
<img width="1194" height="648" alt="image" src="https://github.com/user-attachments/assets/b8b6e4b0-9e8b-46e3-8e7b-1eb138c7461f" />

<img width="1233" height="417" alt="image" src="https://github.com/user-attachments/assets/cea967bc-db31-47a3-8b4a-c8642f3961dd" />

