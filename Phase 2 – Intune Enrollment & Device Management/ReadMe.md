# 🧱 Intune Administration: Phase 2 – Intune Enrollment & Device Management

## 📌 Overview  
This phase of the **Intune Administration Lab Series** focuses on enrolling a Windows 10/11 device into Microsoft Intune, applying compliance and security baselines, and validating full device management.  

Building upon the Azure infrastructure established in Phase 1, this lab simulates a real enterprise environment where devices are registered, secured, and governed using **Microsoft Intune** and **Microsoft Entra ID**.  

Through step-by-step enrollment, policy creation, and verification, this phase demonstrates the complete lifecycle of an Intune-managed device — from initial registration to compliance validation.

---

## 🎯 Objectives  
- Enroll a Windows 10/11 virtual machine into Microsoft Intune using Azure AD join  
- Apply a Windows compliance baseline to enforce security posture  
- Deploy the Microsoft 365 Security Baseline for enhanced protection  
- Verify MDM enrollment and synchronization between Entra ID and Intune  
- Confirm device compliance and management visibility in Intune Admin Center  

---

## 🧠 Key Concepts Reinforced  

| Concept | Description |
|----------|--------------|
| **Device Enrollment** | Connects a Windows device to Microsoft Intune via Entra ID, enabling centralized management and policy delivery. |
| **Compliance Policy** | Establishes minimum security requirements for devices, such as Defender status, BitLocker, and Secure Boot. |
| **Security Baseline** | A preconfigured set of Microsoft-recommended settings for consistent enterprise security. |
| **MDM Check-in** | The synchronization process between the device and Intune to apply and report policies. |

---

## 🧪 Lab Environment & Tools  

**Platform:** Microsoft Intune & Microsoft Entra ID  
**Tenant:** `micoopergmail.onmicrosoft.com` (Cumulus Labs)  
**Virtual Machine:** Windows 11 Pro – `IntuneClient01`  
**Primary Admin:** `MCooper@micoopergmail.onmicrosoft.com`  
**Tools Used:**
- Intune Admin Center ([https://intune.microsoft.com](https://intune.microsoft.com))  
- Microsoft Entra Admin Center  
- Windows 11 Settings → Accounts → Access Work or School  
- PowerShell (`dsregcmd /status` for verification)  

---

## 🗂 Project Structure & Labs  

### ✅ Labs Completed  

| Lab # | Title | Focus Area |
|-------|--------|-------------|
| 01 | Device Enrollment & Azure AD Join | Registering Windows device with Intune and Entra ID |
| 02 | Windows 10/11 Compliance Policy Creation | Applying baseline compliance controls |
| 03 | Microsoft 365 Security Baseline Deployment | Implementing Defender, BitLocker, and Firewall settings |
| 04 | Device Check-in and Compliance Verification | Confirming device management and policy enforcement |

Each lab directory includes:  
- **README.md:** Detailed walkthrough and key explanations  
- **screenshots/:** Visual verification of enrollment, policy creation, and compliance  

---

## 📸 Screenshots  

### Step 1: Device Enrollment Confirmation  
![Device Enrollment Confirmation](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%202%20%E2%80%93%20Intune%20Enrollment%20%26%20Device%20Management/Screenshots/phase2-step1-device-enrollment.png)  
The Windows 11 VM (**IntuneClient01**) successfully enrolled into Microsoft Intune, showing a connection to Cumulus Labs’s Entra ID for MDM management.  

---

### Step 2: Windows Compliance Baseline Creation  
![Windows Compliance Baseline Creation](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%202%20%E2%80%93%20Intune%20Enrollment%20%26%20Device%20Management/Screenshots/phase2-step2-windows-compliance-baseline.png)  
Created a custom **Windows Compliance Baseline – Tier 1** to define compliance rules for Windows 10/11 devices and monitor posture.  

---

### Step 3: Microsoft 365 Security Baseline Profile  
![Microsoft 365 Security Baseline Profile](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%202%20%E2%80%93%20Intune%20Enrollment%20%26%20Device%20Management/Screenshots/phase2-step3-m365-security-baseline.png)  
Configured the **Microsoft 365 Apps for Enterprise Security Baseline – Tier 1** profile to apply secure configuration standards across Office apps.  

---

### Step 4: MDM Diagnostic Verification  
![MDM Diagnostic Verification](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%202%20%E2%80%93%20Intune%20Enrollment%20%26%20Device%20Management/Screenshots/phase2-step4-mdm-diagnostic-data.png)  
Validated successful MDM registration of **IntuneClient01** via diagnostic data — confirming configuration settings were successfully managed by Intune.  

---

### Step 5: Device Compliance Status  
![Device Compliance Status](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%202%20%E2%80%93%20Intune%20Enrollment%20%26%20Device%20Management/Screenshots/phase2-step5-device-compliance-confirmation.png)  
Confirmed **IntuneClient01** is managed by Intune and compliant with all applied baselines and security policies.  


---

## 📈 Outcomes Summary  

✅ Successfully enrolled Windows 11 device into Microsoft Intune  
✅ Applied Windows compliance and Microsoft 365 security baselines  
✅ Verified policy synchronization between Entra ID and Intune  
✅ Confirmed device reporting as “Compliant” in Intune Admin Center  
✅ Established foundation for advanced Intune management and configuration policies  

---

## 💼 Business Relevance  
This phase mirrors real enterprise operations where IT administrators manage and secure devices through centralized MDM solutions.  
By enforcing compliance and deploying security baselines, organizations can:  
- Maintain consistent device security configurations  
- Ensure endpoint compliance with internal and external regulations  
- Strengthen their Zero Trust posture  
- Automate reporting and remediation within Microsoft 365 environments  

---

## 🙏 Acknowledgments  
- **Microsoft Learn:** [Set up enrollment for Windows devices in Intune](https://learn.microsoft.com/mem/intune/enrollment/windows-enrollment-methods)  
- **Microsoft Learn:** [Apply security baselines in Intune](https://learn.microsoft.com/mem/intune/protect/security-baselines)  
- **AI-Supported Documentation:** README structure and content refined using ChatGPT (OpenAI) for consistency and technical accuracy.  
