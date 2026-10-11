# LLMIO:2025 Unbounded Consumption

## Threats

**Unbounded Consumption** occurs when Large Language Models (LLMs) are exposed to excessive, uncontrolled, or malicious usage, resulting in resource exhaustion, service disruption, financial impact, or intellectual property theft.

### Common Threats

- **Denial of Service (DoS)**
  - Memory exhaustion attacks
  - Resource-intensive requests
  - Unfinishable or recursive tasks
  - Infinite loops and excessive token consumption

- **Model Infrastructure Attacks**
  - Deletion or corruption of model files on the server
  - Disruption of model availability

- **Model Theft**
  - Model replication or cloning
  - Unauthorized access to model code or weights
  - Model extraction through repeated querying

- **Traditional DoS Attacks**
  - API flooding
  - Application and server infrastructure attacks
  - Network-level resource exhaustion

- **Model Reverse Engineering**
  - Crafting inputs to infer model behavior
  - Extracting proprietary information from model outputs
---
<img width="1240" height="793" alt="image" src="https://github.com/user-attachments/assets/51789c58-9e6a-48a8-98b5-bc210315b891" />

# LLMIO:2025 Unbounded Consumption

## Remediation

### 1. Rate Limiting & Quotas - Control and restrict resource usage through:
- API rate limits
- Token consumption limits
- User interaction quotas
- Request throttling

### 2. Memory & Context Size Constraints -Prevent resource abuse by limiting:
- Prompt input length
- Context window size
- Response output length
- Conversation history retention

### 3. Usage Monitoring & Anomaly Detection - Continuously monitor and identify:
- Unusual usage patterns
- Excessive token consumption
- Suspicious user behavior
- Real-time abuse indicators

### 4. Prioritization & Resource Allocation - Ensure service availability through:
- Role-based access controls
- Resource quotas per user or tenant
- Priority processing for mission-critical workloads
- Workload isolation

### 5. Session Expiry & Garbage Collection - Optimize resource utilization with:
- Session expiration policies
- Cache cleanup mechanisms
- Memory reclamation processes
- Automated resource lifecycle management


Model Denial of Service (DOS) is an attack where an attacker overwhelms an Al model with excessive 
or specially crafted requests, causing it to become unresponsive or significantly degrade its 
performance, thereby disrupting its normal operations. 

## Example 1: 
LLM acts on user requested tasks which result in high CPU/memory usage of difficult to solve or 
recurring tasks which impact availability. 

## Example 2: 
An attacker continuously prompts an LLM with complex and resource-intensive queries, overloading the 
system and preventing legitimate users from accessing the service. 

## Example 3: 
Sending long queries, queries for recurring resource usage of high volume tasks like LangChain, AutoGPT. 
Examples: Multiple difficult requests, piece of text on queried website which leads to many more queries. 

### **Attack vectors: **
- Resource intensive requests 
- DOS by deleting model files on server 
- Traditional DOS against APIs and application / server infrastructure 
- Loops via indirect prompt injections 
- Loops via evaluated code via indirect prompt injection

<img width="1457" height="576" alt="image" src="https://github.com/user-attachments/assets/76754bfe-2d74-420a-8f76-12f484d2515a" />

#### How to prevent denial of service? 

To prevent Model Denial of Service (DOS) attacks, implement rate limiting on API endpoints to  control the number of requests and prevent system overload. Additionally, ensure proper resource 
management and allocation to handle high traffic loads and mitigate the impact of excessive or 
specially crafted requests. 
