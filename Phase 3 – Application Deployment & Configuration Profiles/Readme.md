# 🧱 Intune Administration: Phase 3 – Application Deployment & Configuration Profiles

## 📌 Overview

This phase of the Intune Administration Lab Series focuses on deploying applications and configuration profiles to managed Windows devices using Microsoft Intune.

Building upon the enrollment and compliance framework established in Phase 2, this phase demonstrates how Intune enforces enterprise security settings and automates software deployment across endpoints.

Through app deployment, BitLocker configuration, and baseline enforcement, this phase highlights how device protection and configuration consistency are maintained at scale.

## 🎯 Objectives

- Deploy Microsoft 365 Apps for Enterprise using Intune  
- Configure and apply the Windows Security Baseline (24H2)  
- Enforce BitLocker Drive Encryption via configuration profiles  
- Validate successful deployment and compliance reporting in Intune  

## 🧠 Key Concepts Reinforced

| Concept | Description |
|----------|-------------|
| Application Deployment | Automates the delivery of approved software packages to Intune-managed devices. |
| Configuration Profile | Defines and applies device-level settings for security, updates, and user experience. |
| Security Baseline | Microsoft-recommended configuration template aligning endpoints with enterprise security standards. |
| BitLocker Encryption | Protects data-at-rest by encrypting storage drives and enforcing TPM-based security. |
| Compliance Reporting | Monitors device posture and confirms adherence to assigned policies. |

## 🧪 Lab Environment & Tools

**Platform:** Microsoft Intune & Microsoft Entra ID  
**Tenant:** micoopergmail.onmicrosoft.com (Cumulus Labs)  
**Virtual Machine:** Windows 11 Pro – IntuneClient01  
**Primary Admin:** MCooper@micoopergmail.onmicrosoft.com  

**Tools Used:**  
- Intune Admin Center (https://intune.microsoft.com)  
- Microsoft 365 Security Baseline (24H2)  
- BitLocker Configuration Profile  
- PowerShell (`Get-BitLockerVolume` validation)

## 🗂 Project Structure & Labs

### ✅ Labs Completed

| Lab # | Title | Focus Area |
|-------|-------|------------|
| 01 | Intune Management Extension Verification | Confirming agent installation on enrolled devices |
| 02 | BitLocker Policy Configuration | Enforcing encryption and TPM + PIN requirements |
| 03 | Windows Security Baseline Deployment | Applying Microsoft’s 24H2 security settings |
| 04 | Microsoft 365 Apps Deployment | Automating enterprise app installation |
| 05 | Compliance Validation | Verifying deployment and encryption success |

Each lab directory includes:  
- **README.md:** Detailed walkthrough and results  
- **screenshots/**: Visual verification of each step  

## 📸 Screenshots

### Step 1: Intune Pilot Group Membership  
Confirmed that **IntuneClient01** was successfully added to the **Intune-Pilot-Devices** group, ensuring proper targeting for all deployment and configuration policies in this phase.  
![Intune Pilot Group Membership](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%203%20%E2%80%93%20Application%20Deployment%20%26%20Configuration%20Profiles/Screenshots/phase3-step1-intune-pilot-group-membership.png)

---

### Step 2: BitLocker Policy Configuration  
Created and assigned a **Disk Encryption Policy** under *Endpoint Security → Disk encryption*. Configured encryption settings (TPM + PIN) and assigned the policy to the **Intune-Pilot-Devices** group.  
![BitLocker Policy Configuration](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%203%20%E2%80%93%20Application%20Deployment%20%26%20Configuration%20Profiles/Screenshots/phase3-step2-bitlocker-policy-creation.png)

---

### Step 3: Microsoft 365 Apps Deployment  
Deployed **Microsoft 365 Apps for Enterprise** as a required application for managed devices. Selected 64-bit installation, enabled automatic updates, and assigned to the **Intune-Pilot-Devices** group.  
![Microsoft 365 Apps Deployment](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%203%20%E2%80%93%20Application%20Deployment%20%26%20Configuration%20Profiles/Screenshots/phase3-step3-m365-apps-deployment.png)

---

### Step 4: Windows Security Baseline (24H2) Deployment  
Deployed and assigned the **Cumulus Labs – Windows Security Baseline (24H2)** to ensure consistent enterprise-grade security configurations. Confirmed policy synchronization with Intune.  
![Windows Security Baseline Deployment](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%203%20%E2%80%93%20Application%20Deployment%20%26%20Configuration%20Profiles/Screenshots/phase3-step4-security-baseline-deployment.png)

---

### Step 5: BitLocker Encryption Validation  
Validated BitLocker encryption using PowerShell command `Get-BitLockerVolume`. Output confirmed **FullyEncrypted** status with protection **On**, ensuring successful enforcement of encryption policy.  
![BitLocker Encryption Validation](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%203%20%E2%80%93%20Application%20Deployment%20%26%20Configuration%20Profiles/Screenshots/phase3-step5-get-bitlockervolume-status.png)

---

### Step 6: Device Compliance Results  
Reviewed compliance posture of **IntuneClient01** in Intune Admin Center. Device reported as compliant across all key indicators. The **65001 (Not applicable)** message appeared because no dedicated compliance policy was assigned — a known Intune reporting limitation that does not impact overall compliance.  
![Device Compliance Results](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%203%20%E2%80%93%20Application%20Deployment%20%26%20Configuration%20Profiles/Screenshots/phase3-step6-compliance-results.png)

## 📈 Outcomes Summary

✅ Successfully deployed Microsoft 365 Apps for Enterprise  
✅ Applied Windows Security Baseline (24H2) without conflicts  
✅ Enforced BitLocker encryption with verified TPM + PIN  
✅ Confirmed compliance and policy reporting within Intune  
✅ Established foundation for Conditional Access and Defender integration in Phase 4  

## 💼 Business Relevance

This phase mirrors how organizations streamline endpoint management through centralized policy control and automation.  

By standardizing application deployment and enforcing encryption requirements, administrators reduce manual workload and strengthen data security at scale.  
Consistent configuration management through Intune also simplifies audit readiness and supports Zero Trust objectives across Microsoft 365 environments.  

## 🙏 Acknowledgments

- Microsoft Learn: [Deploy apps with Microsoft Intune](https://learn.microsoft.com/mem/intune/apps/apps-add)  
- Microsoft Learn: [Configure BitLocker settings in Intune](https://learn.microsoft.com/mem/intune/protect/encrypt-devices)  
- AI-Supported Documentation: README structure and content refined using ChatGPT (OpenAI) for consistency and technical accuracy.  
