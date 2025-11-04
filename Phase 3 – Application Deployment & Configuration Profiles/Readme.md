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

**Step 1: Intune Management Extension Verification**  
Intune Management Extension installed successfully on IntuneClient01, enabling advanced Win32 app deployment.  

**Step 2: BitLocker Policy Configuration**  
Created and assigned a BitLocker configuration profile enforcing TPM + PIN protection.  

**Step 3: Windows Security Baseline (24H2)**  
Deployed Microsoft’s Windows Security Baseline and verified applied settings through local policy results.  

**Step 4: BitLocker Status Validation**  
Confirmed encryption status using PowerShell `Get-BitLockerVolume` – Protection Status displayed as **On**.  

**Step 5: Compliance Results**  
Validated all policies and deployments as successful in Intune Admin Center.  

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
