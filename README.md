# ModelArmor  

**ModelArmor** uses **KubeArmor** as a sandboxing engine to ensure secure execution of untrusted AI/ML models. AI/ML models function as processes, and allowing untrusted models to execute in AI environments poses significant risks, such as cryptomining attacks leveraging GPUs and remote command injections. KubeArmor's preemptive mitigation mechanism constrains models' execution environments, enhancing security.  

---

## **General Introduction**  

**What is ModelArmor?**  
ModelArmor leverages KubeArmor as a sandboxing engine to securely constrain the execution of untrusted models within predefined boundaries. Since AI/ML models essentially run as processes, allowing untrusted models in AI environments poses significant risks, such as cryptomining attacks exploiting GPUs or remote command injection vulnerabilities. The gathered telemetry allows identifying issues such as cryptojacking and other exploits in the model. Furthermore, it can prevent exploitation by enforcing preemptive policies, offering an effective framework to safeguard and enforce constraints on the models' execution environment.

---

## **Problems It Solves**  

ModelArmor addresses several critical challenges in executing untrusted AI/ML models, reducing risks and strengthening the overall security posture of AI environments:

1. **Mitigation of Cryptomining Attacks**  
   Prevents unauthorized use of GPUs for cryptomining by restricting model processes to only execute authorized computations.

2. **Defense Against Remote Command Injection**  
   Blocks untrusted models from executing malicious commands that could compromise the system or network.

3. **Containment of Untrusted Code**  
   Ensures untrusted models are isolated within a secure environment, preventing them from accessing unauthorized resources or data.

4. **Prevention of Resource Abuse**  
   Controls resource usage (CPU, memory, disk) to prevent models from overwhelming the system and affecting other workloads.

5. **Reduced Risk of Data Breaches**  
   Constrains the model's execution to prevent unauthorized access or exfiltration of sensitive data.

6. **Proactive Threat Mitigation**  
   Detects and stops potential security violations before they can cause harm via KubeArmor's preemptive policies.

7. **Regulatory Compliance**  
   Helps meet security and compliance requirements by ensuring models are executed within strict operational boundaries.

8. **Securing CUDA Libraries**  
   Helps in whitelisting specific processes or binaries to access CUDA libraries and denying access to unauthorized attempts to exploit CUDA libraries.

---

## **Why It’s Needed**  

In today’s AI-driven world, as the mundane becomes automated, it is crucial to consider the security of data being used by models. AI systems often have access to sensitive information such as intellectual property, PII, or insider data that could lead to significant losses if leaked. Without proper security, models could be misused for data exfiltration or ransomware attacks. Protecting models ensures they work safely, reliably, and follow rules, keeping systems and data secure. Hence, AI model security is an essential part of an AI-driven landscape to safeguard against these issues.

---

## **Origin Story and System Design**  

As AI began to permeate every vertical for task automation, AccuKnox implemented an AI chatbot to enhance security. However, feedback from clients revealed widespread concerns about data security as AI analyzed sensitive information for insights.  
ModelArmor was created to address these concerns, offering security for AI models by leveraging the powerful detection and prevention capabilities of KubeArmor. Its architecture emphasizes proactive prevention of attacks through policy enforcement using eBPF and LSMs.

---

## **Use Cases**  

### **PyTorch-Based Use Cases**  

1. **[Pickle Code Injection PoC](https://help.accuknox.com/use-cases/modelarmor-pickle-code/)**  
   Demonstrates a Proof of Concept for pickle-based code injection attacks in PyTorch models and how KubeArmor can prevent them.  

2. **[Adversarial Attacks on Deep Learning Models](https://help.accuknox.com/use-cases/modelarmor-adverserial-attacks/)**  
   Shows how to mitigate adversarial attacks targeting PyTorch models by applying security policies.  

3. **[PyTorch App Deployment with KubeArmor](https://help.accuknox.com/use-cases/modelarmor-deploy-pytorch/)**  
   A comprehensive guide on securely deploying PyTorch applications using KubeArmor.  

### **TensorFlow-Based Use Cases**  

1. **[FGSM Attack on a TensorFlow Model](https://drive.google.com/file/d/1EnmsIiR4G4bYmoxBIHTk1bDkW2XatM4N/preview)**  
   Learn about FGSM attacks targeting TensorFlow models and how to mitigate them with KubeArmor policies.  

2. **[Keras Inject Attack and Apply Policies](https://drive.google.com/file/d/1olGBz3WUoJqmcAVdRY7uImKTHggRX6nK/preview)**  
   Demonstrates Keras-based injection attacks and applying protective security policies.  

### **Securing NVIDIA NIM**  

**[Securing NVIDIA NIM (PDF Guide)](https://help.accuknox.com/resources/Securing_NVIDIA_NIM.pdf)**  
Explore how KubeArmor secures NVIDIA NIM deployments against potential threats using model-aware policies.  


---

## **Benefits/Advantages/Differentiators**  

- **Ease of Integration**: Leverages Linux kernel capabilities (eBPF and LSMs) for policy enforcement with negligible process overhead.  
- **Scalability**: Scales seamlessly in distributed environments, reducing maintenance complexity.  
- **Granular Policies**: Provides inline mitigation through fine-grained policies, standing out compared to alternatives focused only on detection.  
- **Cost-Effectiveness**: Combines security and operational efficiency without added complexity.  


### For more use cases refer [Help Documentation](https://help.accuknox.com/use-cases/modelarmor/)
