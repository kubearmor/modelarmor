# ModelArmor  

**ModelArmor** uses **KubeArmor** as a sandboxing engine to ensure secure execution of untrusted AI/ML models. AI/ML models function as processes, and allowing untrusted models to execute in AI environments poses significant risks, such as cryptomining attacks leveraging GPUs and remote command injections. KubeArmor's preemptive mitigation mechanism constrains models' execution environments, enhancing security.  

---

## **Use Cases**  

### **PyTorch-Based Use Cases**  

1. **[Pickle Code Injection PoC](https://help.accuknox.com/use-cases/modelarmor-pickle-code/)**  
   Demonstrates a Proof of Concept for pickle-based code injection attacks in PyTorch models and how KubeArmor can prevent them.  

2. **[Adversarial Attacks on Deep Learning Models](https://help.accuknox.com/use-cases/modelarmor-adverserial-attacks/)**  
   Shows how to mitigate adversarial attacks targeting PyTorch models by applying security policies.  

3. **[PyTorch App Deployment with KubeArmor](https://help.accuknox.com/use-cases/modelarmor-deploy-pytorch/)**  
   A comprehensive guide on securely deploying PyTorch applications using KubeArmor.  

---

### **TensorFlow-Based Use Cases**  

1. **[FGSM Attack on a TensorFlow Model](https://drive.google.com/file/d/1EnmsIiR4G4bYmoxBIHTk1bDkW2XatM4N/preview)**  
   Learn about FGSM attacks targeting TensorFlow models and how to mitigate them with KubeArmor policies.  

2. **[Keras Inject Attack and Apply Policies](https://drive.google.com/file/d/1olGBz3WUoJqmcAVdRY7uImKTHggRX6nK/preview)**  
   Demonstrates Keras-based injection attacks and applying protective security policies.  

---

### **Securing NVIDIA NIM**  

**[Securing NVIDIA NIM (PDF Guide)](https://help.accuknox.com/resources/Securing_NVIDIA_NIM.pdf)**  
Explore how KubeArmor secures NVIDIA NIM deployments against potential threats using model-aware policies.  

---

*ModelArmor: AI/ML Model Security Redefined.*
