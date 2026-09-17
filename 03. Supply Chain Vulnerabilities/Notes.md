# LLM03:2025 Supply Chain – THREATS

Supply Chain refers to vulnerabilities in the development and deployment processes of Large Language Models (LLMs), where compromised third‑party components—such as pre‑trained models, datasets, or plugins—can introduce security risks like backdoors, biases, or system failures, potentially leading to unauthorized access or malicious behavior.

## Key Threats
- Vulnerable models used  
- 3rd party package vulnerabilities  
- Out‑of‑date or vulnerable software, libraries, or repositories  
- Plugin exploits  
- Poisoned PyPi package  

<img width="1025" height="337" alt="image" src="https://github.com/user-attachments/assets/41b1a0d4-d842-4456-b304-0fe64744a156" />

# LLM03:2025 Supply Chain – REMEDIATION

## Key Remediation Strategies
- **Vendor Security Assessment & Audits** - Regular audits of third‑party vendors to ensure compliance and detect vulnerabilities.  
- **Secure Model & Data Provenance** - Comprehensive analysis of the entire supply chain to verify authenticity and integrity.  
- **Dependency Management & SBOM (Software Bill of Materials)** - Maintain visibility into all dependencies with SBOM to track and manage risks effectively.  
- **Zero Trust & Access Controls** - Enforce strict access policies and adopt Zero Trust principles to minimize exposure.  
- **Resilience & Redundancy Planning** - Establish fallback mechanisms and alternative suppliers to ensure continuity and reduce risk.  

# Supply Chain Vulnerabilities

Supply chain vulnerabilities occur when attackers exploit weaknesses in the third‑party components, software, or services that an AI system depends on, potentially introducing malicious elements or compromising the integrity and security of the entire system.

- **Examples** -  - Out‑of‑date or vulnerable software, libraries, or repositories  
- LLM supply chains risk integrity due to vulnerabilities leading to biases, security breaches, or system failures Issues arising from pre‑trained models, crowdsourced data, and plugin extensions.

# What Enables Supply Chain Vulnerabilities?

Supply chain vulnerabilities are often enabled by weak practices in managing third‑party components and dependencies. Key enablers include:

- **Lack of Thorough Vetting & Audits** - Failing to thoroughly vet and audit third‑party libraries, frameworks, and services for security risks before integrating them into systems.  
- **Insufficient Monitoring & Updating** - Not continuously monitoring and updating third‑party components to ensure they remain secure and up‑to‑date with the latest patches and security fixes.  

# Supply Chain Vulnerability Examples

- **Example 1** - A compromised dataset, which is part of the LLM's supply chain, is used for training, leading the model to unintentionally generate outputs that include malware or phishing links.  

- **Example 2** - Vulnerable model used for transfer learning, poisoned crowd‑sourced data, tampered model or data, third‑party package vulnerabilities.  

- **Examples in Practice**  
  - OpenGPT  
  - 3rd Party Package exploit  
  - Plugin exploits  
  - Poisoned PyPi package (tricking developers into installation)  
  - Trojan / backdoor in model zoo models
  - 
# Preventing Supply Chain Vulnerabilities

To prevent supply chain vulnerabilities, organizations must adopt proactive security practices when integrating third‑party components, libraries, and services.

## Key Prevention Strategies
- **Thorough Vetting & Audits** - Carefully vet and audit all third‑party components, libraries, and services for security risks before integration.  
- **Continuous Monitoring & Updates** - Continuously monitor and promptly update third‑party components to ensure they remain secure and up‑to‑date with the latest patches and security fixes.  

