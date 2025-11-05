🧱 Intune Administration: Phase 4 – Monitoring, Reporting & Endpoint Security Remediation

📌 Overview  
This phase of the Intune Administration Lab Series focuses on integrating Microsoft Intune with Microsoft Defender for Endpoint to establish real-time protection, threat detection, and reporting visibility across managed devices.  

Building upon the baseline and encryption framework established in Phase 3, this phase demonstrates how Intune delivers endpoint security at scale by enforcing antivirus policies, monitoring compliance, and validating threat response through Defender telemetry.  

Through Defender policy deployment, EICAR test simulation, and PowerShell-based verification, this phase highlights how Microsoft 365 security ecosystems unify prevention, detection, and remediation.

---

🎯 Objectives
- Deploy and validate Microsoft Defender Antivirus policy through Intune  
- Confirm device compliance and configuration report synchronization  
- Simulate malware detection using the EICAR test file  
- Validate real-time protection and Defender for Endpoint telemetry  
- Configure cloud-delivered protection and MAPS reporting  

---

🧠 Key Concepts Reinforced

| Concept | Description |
|----------|-------------|
| Microsoft Defender Integration | Connects Intune policy management with Defender Antivirus and cloud telemetry for continuous endpoint monitoring. |
| Cloud-Delivered Protection | Extends Defender intelligence through Microsoft cloud services to detect emerging threats faster. |
| EICAR Test File | A safe, industry-standard file used to validate antivirus detection and response without introducing real malware. |
| Compliance & Reporting | Confirms device posture, remediation actions, and security configuration status within Intune. |
| MAPS Telemetry | Microsoft Active Protection Service that submits threat metadata and samples for improved protection analytics. |

---

🧪 Lab Environment & Tools
**Platform:** Microsoft Intune & Microsoft Defender for Endpoint  
**Tenant:** micoopergmail.onmicrosoft.com (Cumulus Labs)  
**Virtual Machine:** Windows 11 Pro – IntuneClient01  
**Primary Admin:** MCooper@micoopergmail.onmicrosoft.com  

**Tools Used**
- Intune Admin Center (https://intune.microsoft.com)  
- Microsoft 365 Defender Portal (https://security.microsoft.com)  
- Windows Security App & PowerShell  
- EICAR Test File for threat simulation  

---

🗂 Project Structure & Labs  

✅ Labs Completed  

| Lab # | Title | Focus Area |
|-------|--------|-------------|
| 01 | Defender Policy Deployment | Create and assign Microsoft Defender Antivirus policy in Intune |
| 02 | Compliance and Configuration Reports | Monitor device check-ins and policy sync status |
| 03 | Threat Simulation (EICAR) | Validate real-time protection and alert generation |
| 04 | Cloud Telemetry Configuration | Enable cloud-delivered protection and MAPS submission |
| 05 | Security Event Verification | Review Defender alerts and reporting status |

Each lab directory includes:
- **README.md:** Detailed walkthrough and results  
- **screenshots/**: Visual verification of each step  

---

## 📸 Screenshots

### Step 1: Defender Antivirus Policy Configuration
Created and configured the **Phase 4 – Defender Antivirus Policy** under *Endpoint security → Antivirus*. Enabled real-time monitoring, cloud protection, automatic sample submission, and set remediation actions.  
![Defender Antivirus Policy Configuration](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%204%20%E2%80%93%20Monitoring%2C%20Reporting%20%26%20Endpoint%20Security%20Remediation/Screenshots/phase4-step1-defender-policy-configuration.png)

### Step 2: PowerShell Verification of Defender Status
Ran `Get-MpComputerStatus` to confirm Defender services are active: RealTimeProtection, Antispyware, IOAV, and NIS.  
![PowerShell Verification of Defender Status](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%204%20%E2%80%93%20Monitoring%2C%20Reporting%20%26%20Endpoint%20Security%20Remediation/Screenshots/phase4-step2-getmpcomputerstatus.png)

### Step 3: Defender for Endpoint Connector Configuration
Validated the Intune ↔ Microsoft 365 Defender connection is **Available** under *Endpoint security → Setup → Microsoft Defender for Endpoint*.  
![Defender for Endpoint Connector Configuration](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%204%20%E2%80%93%20Monitoring%2C%20Reporting%20%26%20Endpoint%20Security%20Remediation/Screenshots/phase4-step3-defender-connector.png)

### Step 4: Device Compliance Overview
Viewed *Reports → Device compliance* to confirm **IntuneClient01** is **Compliant**, indicating policies applied and reporting is working.  
![Device Compliance Overview](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%204%20%E2%80%93%20Monitoring%2C%20Reporting%20%26%20Endpoint%20Security%20Remediation/Screenshots/phase4-step4-compliance-overview.png)

### Step 5: EICAR Threat Detection Notification
Simulated malware with the EICAR test file. Defender immediately detected and quarantined the file, proving real-time protection.  
![EICAR Threat Detection Notification](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%204%20%E2%80%93%20Monitoring%2C%20Reporting%20%26%20Endpoint%20Security%20Remediation/Screenshots/phase4-step5-eicar-alert.png)

### Step 6: PowerShell EICAR Detection Log
Used `Get-MpThreat` to show **Virus:DOS/EICAR_Test_File** was detected and remediated, confirming the AV response pipeline.  
![PowerShell EICAR Detection Log](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%204%20%E2%80%93%20Monitoring%2C%20Reporting%20%26%20Endpoint%20Security%20Remediation/Screenshots/phase4-step6-eicar-detection.png)

### Step 7: Cloud Protection Settings Verification
Checked `Get-MpPreference` to verify MAPS telemetry, sample submission, and cloud-delivered protection configuration.  
![Cloud Protection Settings Verification](https://github.com/miadco/Intune-Adminstration/blob/main/Phase%204%20%E2%80%93%20Monitoring%2C%20Reporting%20%26%20Endpoint%20Security%20Remediation/Screenshots/phase4-step7-cloud-settings.png)
  

---

📈 Outcomes Summary  
✅ Successfully deployed Microsoft Defender Antivirus policy  
✅ Confirmed device compliance and report generation in Intune  
✅ Detected and quarantined EICAR test file via real-time protection  
✅ Configured MAPS and cloud-delivered protection for telemetry sync  
✅ Validated Defender integration within Microsoft 365 Defender portal  

---

💼 Business Relevance  
This phase demonstrates how enterprises unify endpoint protection and compliance reporting within Microsoft Intune and Defender for Endpoint.  

By automating antivirus policy deployment, enforcing cloud protection, and confirming real-time response through simulation, administrators can ensure consistent endpoint security posture and faster incident visibility.  

Centralized telemetry also supports Zero Trust principles by maintaining continuous verification and rapid containment of threats across managed endpoints.  

---

🙏 Acknowledgments  
- **Microsoft Learn:** [Configure Defender Antivirus policy in Intune](https://learn.microsoft.com/en-us/mem/intune/protect/antivirus-microsoft-defender-settings-windows)  
- **Microsoft Learn:** [Microsoft Defender for Endpoint integration with Intune](https://learn.microsoft.com/en-us/mem/intune/protect/advanced-threat-protection)  
- **AI-Supported Documentation:** README structure and content refined using ChatGPT (OpenAI) for consistency and technical accuracy.  



