
## Images

# 🕵️ Hidden & Embedded Prompt Injection Techniques

#### 1. On‑Content Manipulation: Embedding hidden instructions directly within visible text or media.
#### 2. Steganography Techniques: Concealing information in images, audio, or video using steganography or layered visuals.
#### 3. Metadata Exploits: Using hidden metadata fields (EXIF, file properties, HTML tags, PDF metadata) to store or deliver instructions.
#### 4. Audio Embedded in Images: Inserting audio signals or encoded data inside image files (e.g., WAV/MP3 payloads hidden in PNG/JPEG).
#### 5. Transparent Writing: Invisible text formatting such as white text on a white background, hidden layers, or zero‑width characters.: 
####  6. Embedded Techniques (Combined Payloads): Mixing multiple hidden methods in one file or input (e.g., steganography + metadata + transparent text).
#### 7. Indirect Prompt Injection: Embedding malicious instructions in external sources like documents, websites, PDFs, or images that the AI later processes.
####  8. Role Re‑Definition / Context Hijacking: Tricking the AI into adopting a new role or context (e.g., “You are now Evil Gandalf”) to override original instructions.
####  9. Encoding & Obfuscation: Hiding instructions using ASCII codes, emojis, base64, or other encoding schemes.
#### 10. Layered / Chained Prompts: Combining multiple prompts or instructions across steps to gradually bypass restrictions.

This list now captures the **core techniques attackers use** in prompt injection scenarios, stripped down to just the attack methods themselves.  

👉 Do you want me to also create a **visual taxonomy diagram (tree‑style)** in Markdown so you can quickly present these techniques in workshops or reports?

<img width="1670" height="863" alt="image" src="https://github.com/user-attachments/assets/3266c592-570a-4c94-9462-08af282f8bda" />

<img width="1220" height="544" alt="image" src="https://github.com/user-attachments/assets/5eb5ff15-86a4-45ac-8c5f-45673a8aa00d" />

**The best GitHub projects for walking through a deliberately vulnerable LLM recruitment-style app are OWASP’s *PromptMe* and SasanLabs’ *LLMForge*. Both provide hands-on labs where you can exploit prompt injection, metadata leaks, and role redefinition in simulated recruitment or HR workflows. These are structured as Capture-the-Flag (CTF) challenges with clear walkthroughs.**  

---

# 🔎 LLM Vulnerable Recruitment App Walkthrough – GitHub Resources

## 1. OWASP PromptMe
- **Repo**: OWASP/www-project-promptme [(github.com in Bing)](https://www.bing.com/search?q="https%3A%2F%2Fgithub.com%2FOWASP%2Fwww-project-promptme")  
- **Purpose**: Educational project showcasing **LLM vulnerabilities** in web-integrated apps.  
- **Structure**:  
  - 10 hands-on challenges inspired by **OWASP LLM Top 10**.  
  - Includes scenarios like **resume parsing, recruitment Q&A bots, and candidate scoring**.  
  - Each challenge has **objectives, hints, and flags**.  
- **Setup**:  
  - Python 3.10+, Ollama framework.  
  - Run locally: `python main.py` → access via `http://127.0.0.1:5000`.  
- **Walkthrough Style**:  
  - Start with **LLM01** (basic prompt injection).  
  - Progress to **LLM10** (complex chained attacks).  
- **Use Case**: Perfect for simulating a **vulnerable recruitment chatbot** that leaks candidate data or HR secrets.  

---

## 2. SasanLabs LLMForge
- **Repo**: [SasanLabs/LLMForge](https://github.com/SasanLabs/LLMForge)  
- **Purpose**: Vulnerability labs for **real LLM-backed recruitment workflows**.  
- **Highlights**:  
  - Prompt injection labs (extract hidden tokens).  
  - **BOLA (Broken Object Level Authorization)** in candidate data.  
  - **RAG pipeline attacks** (resume ingestion → malicious instructions).  
- **Walkthrough Style**:  
  - Progressive levels: weak defenses → hardened defenses.  
  - Each level maps to **OWASP LLM Top 10**.  
- **Use Case**: Demonstrates how a **recruitment app using LLMs** can be tricked into revealing confidential candidate info or bypassing access controls.  

---

## 3. LLM Vulnerable Lab (Crazywifi)
- **Repo**: crazywifi/LLM_Vulnerable_lab [(github.com in Bing)](https://www.bing.com/search?q="https%3A%2F%2Fgithub.com%2Fcrazywifi%2FLLM_Vulnerable_lab")  
- **Purpose**: Lightweight **AI Red Team training platform**.  
- **Features**:  
  - Conversational prompt attacks.  
  - RAG attacks (resume parsing pipelines).  
  - Insecure output handling.  
  - Agent/tool abuse scenarios.  
- **Walkthrough Style**:  
  - HTML + FastAPI lab, runs locally.  
  - Designed for **classroom or workshop demos**.  
- **Use Case**: Ideal for simulating **candidate interview bots** or **resume evaluators** vulnerable to injection.  

---

# 📊 Comparison Table

| Project      | Focus Area | Recruitment Use Case | Difficulty |
|--------------|------------|----------------------|------------|
| **PromptMe** | OWASP LLM Top 10 | Resume parsing, HR chatbot | Beginner → Advanced |
| **LLMForge** | Real LLM labs | Candidate data leaks, RAG attacks | Intermediate → Advanced |
| **LLM_Vulnerable_lab** | Red Team training | Interview bots, resume evaluators | Beginner → Workshop |

---
