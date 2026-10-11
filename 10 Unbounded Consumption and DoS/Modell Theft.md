# Model Theft

## What is Model Theft?

**Model Theft** occurs when an attacker illegally copies, extracts, or replicates an AI model. This can be achieved through reverse engineering, excessive querying, or exploiting vulnerabilities to gain access to the model, its code, or its parameters.

**Example:**
- An attacker crafts inputs to infer how the model works based on its outputs.
- Vulnerabilities expose model files, source code, or model weights.

## How Does Model Theft Happen?

Model theft commonly occurs when organizations fail to implement adequate security controls, including:

- Weak or missing access controls and authentication mechanisms.
- Inadequate protection of model code, weights, and parameters.
- Lack of encryption, obfuscation, or secure execution environments.
- Exposure of model repositories, APIs, or backend infrastructure.

## Common Model Theft Techniques

#### 1. Model Replication: Attackers interact with a model at scale and use the generated outputs to train a duplicate model that mimics the original system's behavior.
#### 2. Code Access: If a model has direct or indirect access to code repositories, attackers may exploit vulnerabilities or prompt-based weaknesses to obtain source code and proprietary logic.
#### 3. Model Extraction: By submitting a large volume of carefully crafted queries, attackers can analyze responses and gradually recreate parts of the model's functionality and behavior.

## Impact

- Loss of intellectual property (IP)
- Unauthorized model usage and monetization
- Exposure of proprietary algorithms and training methods
- Competitive and financial losses
- Increased risk of further attacks against AI systems

## How to Prevent Model Theft

### Access Control & Authentication
- Enforce strong authentication mechanisms.
- Implement role-based access control (RBAC).
- Restrict access to authorized users only.

### Model Protection
- Encrypt model files, weights, and parameters.
- Use code obfuscation where appropriate.
- Store and run models in secure enclaves or trusted execution environments.

### API Security
- Apply rate limiting and usage quotas.
- Monitor for excessive or suspicious query patterns.
- Detect and block automated extraction attempts.

### Monitoring & Auditing
- Continuously monitor model access and usage.
- Log and review security events.
- Alert on abnormal model interaction patterns.

### Infrastructure Security
- Secure code repositories and model storage locations.
- Regularly patch vulnerabilities.
- Follow secure deployment and configuration practices.

1. Agent Denial of Service (Demo 1): 
<img width="1756" height="884" alt="image" src="https://github.com/user-attachments/assets/201cd77d-d73a-4e87-8671-a2d5c4746dbb" />

2. Claude Magic String DoS Scenario
<img width="1539" height="963" alt="image" src="https://github.com/user-attachments/assets/b9eaaf84-99f4-48e9-85d5-73f65a718139" />
<img width="1745" height="799" alt="image" src="https://github.com/user-attachments/assets/66b2c792-6274-4050-8ecc-75773f8bb523" />

3. DoS in Claude Opus 4.6
<img width="1372" height="695" alt="image" src="https://github.com/user-attachments/assets/8eaf780d-4b88-4c31-9302-32f877b39ddb" />
<img width="1751" height="639" alt="image" src="https://github.com/user-attachments/assets/34701b1a-1670-47dd-a5d4-cf77d1e8de8c" />
<img width="1748" height="950" alt="image" src="https://github.com/user-attachments/assets/9ea9fc1f-6f49-4d98-86c7-216feb1ef2b1" />

