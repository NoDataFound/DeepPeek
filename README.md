# SecurityScorecard STRIKE Research: A DeepPeek @ DeepSeek Analysis
```
                                                                                                         
                                         
         ░░░░░░░▒▒▒░░  ░▒░             
        ░▒▓▓▓▓▓▓▓▓▓▓▒    ░▓▓▓░   ░▒▒     
      ░▒▓▓▓▓▓▓▓▓▓▓▓▓▓▓▒░ ░▓▓▓▓▓▓▓▓▓░     
     ░▒▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▒░░▒▓▓▓▓▓▒░      
     ░▓▒░░░▒▒▓▓▓▓▓▓▓▓▓▓▓▓▓▒▒▓▓▓░░        
     ▒▓░      ░▒▓▓▓▓▓▒X▒▓▓▓▓▓▒          
     ░▓▓░       ░▒▓▓▓▓▒░░▒▓▓▓▓░          
     ░▓▓▒░        ░▓▓▓▓▓▓▓▓▓▓░░          
     ░░▓▓▒     ░  ░░▓▓▓▓▓▓▓▓░░           
       ░▒▓▓▒░  ▒▓▒░░ ▒▓▓▓▓▒░             
        ░░▓▓▓▓▓▓▓▓▓▓▒░░▒▓▓▓▓▓░           
          ░░▒▒▓▓▓▓▓▓▒▒░░                 
                                         
                                                                         

```

![Security](https://img.shields.io/badge/Security-Research-red) 
![Status](https://img.shields.io/badge/Status-Active-green) 
![Version](https://img.shields.io/badge/Version-1.0.8-blue) 
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## 📌 Overview
This repository contains research, analysis, and resources from the **SecurityScorecard STRIKE** team research regarding **DeepSeek** (https://securityscorecard.com/blog/a-deep-peek-at-deepseek), an AI-powered application with significant security and privacy concerns. This research highlights potential risks, data exfiltration methods, and security weaknesses, as well as technical methodologies for static and dynamic analysis.

---

## 🔥 Key Findings
- **Security Vulnerabilities**: Weak encryption, SQL injection risks, hardcoded keys.
- **Data Collection Concerns**: Captures user inputs, device data, and keystroke patterns.
- **Data Transmission to China**: Stored on **Chinese state-owned infrastructure** with **ByteDance ties**.
- **Anti-Debugging Mechanisms**: Prevents security analysis by detecting Frida and debugging attempts.
- **Regulatory Scrutiny**: Banned in **Italy, Australia, and by the U.S. Navy** due to security concerns.
- **Code Analysis**: Direct integration with **ByteDance** analytics, **risking unauthorized data access**.
- **Network Security Risks**: Third-party servers with **low security scores** and **questionable reliability**.

---

## 🛠 Research Methodology

### 🔍 1. APK Extraction
- Identify and extract the **DeepSeek APK** using `adb`
- Retrieve the installed package path
- Pull APK from the device

### 🏗 2. Static Analysis
- **Decompile APK** using `apktool`
- Inspect `AndroidManifest.xml` for overreaching permissions
- Analyze `smali` code and embedded resources

### 🌐 3. Dynamic Analysis
- **Intercept HTTP/S traffic** using **Burp Suite**
- **Bypass SSL pinning** with **Frida** for deeper inspection
- Monitor **network requests and data leakage patterns**

### 🔑 4. Security Vulnerabilities (CWE Mappings)
| CWE | Risk Level | Description |
|------|------------|-------------|
| **CWE-327** | High | Weak encryption (DES) can be cracked easily. |
| **CWE-89** | High | SQL Injection risks allow data exfiltration. |
| **CWE-321** | High | Hardcoded encryption keys expose sensitive data. |
| **CWE-502** | Medium | Unsafe deserialization leads to remote execution. |
| **CWE-78** | Moderate | Injection risks in system commands. |

---

## 🔬 Tools Used
- **Apktool** – Decompile & analyze the APK structure.
- **Burp Suite** – Capture and inspect HTTP/S requests.
- **Frida** – Dynamic hooking & bypassing SSL pinning.
- **MITM Proxy** – Analyze encrypted data transmission.
- **Android Studio AVD** – Emulated environment for testing.

---

## 📁 Repository Contents
- `/apk/` – Extracted and decompiled APK components.
- `/scripts/` – **Frida** scripts for runtime analysis.
- `/network/` – Captured HTTP/S traffic logs.
- `/reports/` – Full STRIKE **DeepSeek security report**.
- `/STIX/` – Structured **threat intelligence data (STIX format)**.


