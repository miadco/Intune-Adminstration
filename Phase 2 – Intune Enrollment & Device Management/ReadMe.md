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

| Step | Screenshot | Description |
|------|-------------|--------------|
| **1** | ![phase2-step1-device-enrollment.png](screenshots/phase2-step1-device-enrollment.png) | Initiated Windows device enrollment via “Access work or school,” connecting to Cumulus Labs Entra ID. |
| **2** | ![phase2-step2-compliance-baseline.png](screenshots/phase2-step2-compliance-baseline.png) | Created the *Windows Compliance Baseline – Tier 1* policy to enforce Defender and encryption standards. |
| **3a** | ![phase2-step3a-noncompliance-action.png](screenshots/phase2-step3a-noncompliance-action.png) | Configured action to mark noncompliant devices immediately for real-time enforcement. |
| **3b** | ![phase2-step3b-m365-baseline.png](screenshots/phase2-step3b-m365-baseline.png) | Deployed *M365 Security Baseline – Tier 1* for enterprise-grade configuration consistency. |
| **4** | ![phase2-step4-dsregcmd-status.png](screenshots/phase2-step4-dsregcmd-status.png) | Verified successful MDM registration via PowerShell showing `Managed by MDM` and `KeySignTest : PASSED`. |
| **5** | ![phase2-step5-device-compliant.png](screenshots/phase2-step5-device-compliant.png) | Intune Admin Center confirming `IntuneClient01` is enrolled, compliant, and managed by Intune. |

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
