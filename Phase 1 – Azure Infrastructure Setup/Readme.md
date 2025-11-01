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

## 📸 Screenshots

| Step | Screenshot | Description |
|------|-------------|--------------|
| **1** | ![Resource Group Creation](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%201%20%E2%80%93%20Azure%20Infrastructure%20Setup/screenshots/phase1-step1-resourcegroup-creation.png) | Created the **Intune-Lab** resource group using PowerShell. This serves as the parent container for all Azure resources in the lab environment. |
| **2** | ![VNet and Subnet Creation](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%201%20%E2%80%93%20Azure%20Infrastructure%20Setup/screenshots/phase1-step2-vnet-subnet-creation.png) | Deployed **Intune-VNet** (10.0.0.0/16) and **Intune-Subnet** (10.0.1.0/24) using PowerShell to define the virtual network structure and address space. |
| **3a** | ![AzureBastionSubnet Creation](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%201%20%E2%80%93%20Azure%20Infrastructure%20Setup/screenshots/phase1-step3a-azurebastionsubnet-creation.png) | Configured a dedicated **AzureBastionSubnet** (10.0.0.192/26) to support Bastion deployment and secure private RDP access. |
| **3b** | ![Bastion Configuration Review](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%201%20%E2%80%93%20Azure%20Infrastructure%20Setup/screenshots/phase1-step3b-bastion-configuration-review.png) | Reviewed Bastion configuration prior to deployment. Confirmed association with *Intune-VNet* and *Intune-Lab* resource group. |
| **3c** | ![Bastion Deployment Success](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%201%20%E2%80%93%20Azure%20Infrastructure%20Setup/screenshots/phase1-step3c-bastion-deployment-success.png) | Verified successful deployment of **Intune-Bastion03** in *West US 2*. The Bastion host is now operational for secure connectivity. |
| **4a** | ![VM Deployment Success](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%201%20%E2%80%93%20Azure%20Infrastructure%20Setup/screenshots/phase1-step4a-vm-deployment-success.png) | Created **IntuneClient01** (Windows 11) in *Intune-Subnet*. This VM acts as the managed client for Intune and policy testing. |
| **4b** | ![Bastion RDP Connection](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%201%20%E2%80%93%20Azure%20Infrastructure%20Setup/screenshots/phase1-step4b-bastion-rdp-connection.png) | Connected to **IntuneClient01** using Azure Bastion via web-based RDP—no public IP required, enhancing network security. |
| **4c** | ![Windows 11 OOBE Setup](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%201%20%E2%80%93%20Azure%20Infrastructure%20Setup/screenshots/phase1-step4c-windows11-oobe-setup.png) | Completed the **Windows 11 Out-of-Box Experience (OOBE)**, confirming successful VM initialization within the private network. |
| **4d** | ![Windows 11 Desktop](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%201%20%E2%80%93%20Azure%20Infrastructure%20Setup/screenshots/phase1-step4d-windows11-desktop.png) | Reached the Windows 11 desktop through Bastion RDP, validating full end-to-end connectivity and lab readiness. |


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
