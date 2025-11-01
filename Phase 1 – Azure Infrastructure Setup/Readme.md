# 🧱 Intune Administration: Phase 1 – Azure Infrastructure Setup  

📌 **Overview**  
This repository documents the first phase of the Intune Administration Lab Series — building a secure Azure foundation for endpoint management.  
Each step mirrors the process of designing a real enterprise environment where Intune and Microsoft Entra ID (Azure AD) integrate for device management, access control, and compliance.  

By documenting each stage with screenshots and detailed explanations, this lab demonstrates the cloud infrastructure preparation required before enrolling and managing Windows devices in Intune.  

---

### 🎯 **Objectives**
- Create a dedicated Azure Resource Group for Intune lab resources  
- Deploy a Virtual Network (VNet) and subnets for private connectivity  
- Configure Azure Bastion for secure RDP access without public exposure  
- Deploy a Windows 11 virtual machine within a private subnet  
- Validate end-to-end connectivity and secure access through Bastion  

---

### 🧠 **Key Concepts Reinforced**
| Concept | Description |
|----------|--------------|
| **Virtual Networking** | Designing VNets and subnets to isolate and segment Azure resources securely |
| **Azure Bastion** | Providing secure, browser-based RDP connectivity without exposing VM public IPs |
| **Resource Organization** | Structuring resources logically under a single resource group for ease of management |
| **Compute Deployment** | Deploying and configuring a Windows 11 virtual machine using the Azure Portal |
| **Security Principles** | Implementing least privilege and zero-trust access design through Bastion |
| **Connectivity Verification** | Testing private VM access within Azure using Bastion to ensure proper network routing |

---

### 🧪 **Lab Environment & Tools**
**Platform:** Microsoft Azure  
**Tenant:** Microsoft Entra ID (`micoocopergmail.onmicrosoft.com`)  
**Tools Used:**  
- Azure Portal  
- Microsoft Entra Admin Center  
- PowerShell  
- Azure Bastion  
- Windows 11 Pro (VM)  

---

### 🗂 **Project Structure & Labs**
✅ **Labs Completed**

| Lab # | Title | Focus Area |
|-------|--------|-------------|
| 01 | Build Azure Resource Group and Virtual Network | Resource Organization & Networking |
| 02 | Deploy Azure Bastion Host for Secure Access | Network Security & Access Control |
| 03 | Create Windows 11 Virtual Machine (No Public IP) | Private Compute Deployment |
| 04 | Validate RDP Connectivity via Bastion | Secure Access Verification |

Each lab directory includes:
- **README.md:** Step-by-step walkthrough with explanations  
- **screenshots/:** Visual documentation of configurations and successful deployments  

---

### 📸 **Screenshot Documentation**
| Step | Filename | Description |
|------|-----------|-------------|
| 1 | `phase1-step1-resourcegroup-creation.png` | Resource group `Intune-Lab` successfully created in West US 2 |
| 2 | `phase1-step2-vnet-subnet-creation.png` | Virtual network `Intune-VNet` and `Intune-Subnet` configured |
| 3 | `phase1-step3a-azurebastionsubnet-creation.png` | Added `AzureBastionSubnet` to VNet |
| 4 | `phase1-step3b-bastion-configuration-review.png` | Final Bastion setup screen before deployment |
| 5 | `phase1-step3c-bastion-deployment-success.png` | `Intune-Bastion03` deployed successfully |
| 6 | `phase1-step4a-vm-networking-no-public-ip.png` | VM networking configuration without public IP |
| 7 | `phase1-step4b-vm-deployment-success.png` | Windows 11 VM `IntuneClient01` running in private subnet |
| 8 | `phase1-step4c-bastion-rdp-connection.png` | Connecting to VM using Bastion via browser-based RDP |
| 9 | `phase1-step4d-windows11-oobe-setup.png` | Initial Windows 11 out-of-box setup screen |
| 10 | `phase1-step4e-windows11-desktop.png` | Windows 11 desktop confirmed accessible via Bastion |
| 11 | `phase1-summary-lab-complete.png` | Overview of completed Phase 1 resources and success confirmation |

---

### 📈 **Outcomes Summary**
✅ Deployed a secure, isolated Azure environment for Intune management  
✅ Implemented private VM connectivity using Bastion  
✅ Verified end-to-end remote access without public exposure  
✅ Established a foundation for future Intune and Entra ID integration labs  

---

### 💼 **Business Relevance**
These foundational configurations replicate real-world enterprise practices, ensuring:
- Secure device management within a controlled Azure environment  
- Compliance with zero-trust principles (no public exposure)  
- Readiness for device enrollment and policy application via Microsoft Intune  
- Scalable, repeatable design for hybrid IT infrastructure  

---

### 🙏 **Acknowledgments**
- Microsoft Learn – Endpoint Management & Intune Administration Modules  
- Microsoft Documentation – Azure Bastion and Virtual Network Setup  
- AI-Supported Documentation: Lab writeups were structured and refined with the assistance of **ChatGPT (OpenAI)** for accuracy, formatting, and clarity.  
