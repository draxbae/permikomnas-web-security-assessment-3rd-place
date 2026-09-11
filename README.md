# PERMIKOMNAS Web Security Assessment

Sanitized web security assessment case study from the **PERMIKOMNAS RI national competition** in the field of Informatics, Cyber Security, and Bug Bounty.

## 🏆 Achievement

**3rd Place — PERMIKOMNAS RI Bug Bounty Competition**

This project documents my team's web security assessment experience during the national PERMIKOMNAS RI competition.

The assessment focused on identifying and validating web application security issues through reconnaissance, enumeration, manual analysis, vulnerability testing, impact assessment, and security reporting.

> **Note:** This repository is a sanitized portfolio version. Sensitive target information, credentials, personal data, IP addresses, raw competition reports, and detailed exploit information have been intentionally excluded.

---

## 📌 Project Overview

During the competition, our team performed an authorized security assessment within the scope and rules defined by the PERMIKOMNAS RI Bug Bounty competition.

The assessment combined automated reconnaissance and scanning with manual web application analysis.

The workflow included:

* Reconnaissance and scanning
* Web application enumeration
* Endpoint discovery
* HTTP request/response analysis
* Browser Developer Tools inspection
* Client-side source code analysis
* Manual vulnerability testing
* Vulnerability validation
* Impact analysis
* Security reporting

The goal was to identify security weaknesses, validate their impact, and document appropriate remediation recommendations.

---

## 🔎 Assessment Approach

```text
Reconnaissance & Scanning
        ↓
Kali Linux / Windows PowerShell
        ↓
Web Application Enumeration
        ↓
Endpoint & Resource Discovery
        ↓
Browser Developer Tools
        ↓
Source Code & HTTP Analysis
        ↓
Manual Vulnerability Testing
        ↓
Validation & Impact Analysis
        ↓
Security Reporting
```

---

## 🧪 Methodology

### 1. Reconnaissance

Initial reconnaissance was performed to understand the authorized assessment scope and identify publicly accessible application components.

Activities included:

* Domain and asset reconnaissance
* Service discovery
* Basic technology identification
* Identification of accessible web resources
* Collection of information relevant to the authorized scope

### 2. Web Application Enumeration

After reconnaissance, accessible application functionality and resources were enumerated.

Activities included:

* Endpoint discovery
* Web application mapping
* Resource enumeration
* HTTP response analysis
* Identification of interesting application behavior
* Review of accessible client-side assets

### 3. Manual Web Analysis

Automated reconnaissance was followed by manual analysis using the browser and Developer Tools.

Activities included:

* Inspecting application behavior
* Reviewing client-side source code
* Analyzing JavaScript resources
* Reviewing HTTP requests and responses
* Identifying potentially sensitive parameters and application logic
* Investigating abnormal or unexpected responses

### 4. Vulnerability Validation

Potential vulnerabilities identified during reconnaissance and manual analysis were manually validated.

The validation process focused on:

* Reproducing the observed behavior
* Comparing application responses
* Testing relevant parameters and object references
* Confirming whether a suspected issue represented an actual security weakness
* Assessing the security impact while remaining within the authorized scope

### 5. Impact Analysis

Validated findings were analyzed to determine their potential impact.

The assessment considered factors such as:

* Confidentiality
* Integrity
* Availability
* Access control
* Information exposure
* Potential security consequences

Findings were assigned severity according to the observed behavior and potential impact.

### 6. Security Reporting

Validated vulnerabilities were documented in a structured security report.

Each finding included relevant information such as:

* Vulnerability description
* Severity
* Affected functionality
* Technical observation
* Security impact
* Recommended remediation

Sensitive information from the original competition reports has been removed from this portfolio version.

---

## 🛡️ Findings Summary

| Finding                                 | Severity   | Category                         |
| --------------------------------------- | ---------- | -------------------------------- |
| Insecure Direct Object Reference (IDOR) | **High**   | Broken Access Control            |
| HTTP 507 Insufficient Storage           | **Medium** | Availability / Resource Handling |
| `.env` File Existence Disclosure        | **Medium** | Information Disclosure           |
| Directory Listing Enabled               | **Medium** | Security Misconfiguration        |

> The findings listed above are presented in sanitized form for portfolio and educational purposes.

Detailed sanitized findings are documented in [`findings.md`](findings.md).

---

## 🔐 Key Security Areas

The assessment provided practical experience in several areas of web application security.

### Broken Access Control

Analysis of application functionality and object references to identify potential authorization weaknesses.

### Information Disclosure

Investigation of application responses and accessible resources that could reveal information about the underlying application.

### Security Misconfiguration

Identification of configurations that could unnecessarily expose application resources.

### Availability & Resource Handling

Analysis of application behavior related to resource and storage handling.

---

## 🛠️ Tools & Technologies

The assessment involved a combination of security tools and manual analysis techniques.

### Operating Systems

* Kali Linux
* Windows PowerShell

### Security & Analysis

* Web reconnaissance tools
* Network and service discovery tools
* HTTP analysis tools
* Vulnerability scanning tools
* Browser Developer Tools
* Browser Inspect

### Manual Analysis

* HTTP request/response analysis
* Client-side source code inspection
* Manual vulnerability testing

---

## 💻 Skills Demonstrated

Through this assessment, I developed practical experience in:

* Web reconnaissance
* Web application enumeration
* Endpoint discovery
* Manual web penetration testing
* HTTP request/response analysis
* Browser Developer Tools
* Source code inspection
* Broken access control analysis
* IDOR identification and validation
* Information disclosure analysis
* Security misconfiguration analysis
* Availability testing
* Vulnerability validation
* Impact assessment
* Security reporting
* Remediation recommendations

---

## 📚 Learning Outcomes

This competition provided practical experience beyond theoretical cybersecurity concepts.

Key learning outcomes included:

* Understanding the importance of reconnaissance before vulnerability testing
* Combining automated tools with manual analysis
* Understanding how web applications process requests and responses
* Identifying security weaknesses through application behavior
* Validating vulnerabilities rather than relying only on automated scanner results
* Assessing the potential impact of security findings
* Writing structured vulnerability reports
* Working as part of a cybersecurity competition team

---

## 🏆 Competition Experience

**Competition:** PERMIKOMNAS RI Bug Bounty Competition
**Level:** National
**Field:** Informatics / Cyber Security / Bug Bounty
**Result:** **3rd Place**

The competition provided an opportunity to apply web security knowledge in a competitive environment while working within defined rules of engagement and an authorized testing scope.

---

## 👥 Team

This assessment was performed as a team during the PERMIKOMNAS RI competition.

The repository focuses on my team's technical assessment experience while keeping participant information and sensitive competition data private.

---

## 🔒 Ethics & Scope

All security testing was performed within the authorized scope and rules established by the PERMIKOMNAS RI Bug Bounty competition.

The purpose of the assessment was to identify and responsibly report security weaknesses.

No unauthorized systems were intentionally targeted.

---

## ⚠️ Disclaimer

This repository is a **sanitized educational and professional portfolio case study**.

The original competition report contained information that should not be publicly disclosed. Therefore, the following information has intentionally been excluded:

* Sensitive target URLs
* IP addresses
* Credentials
* Personal participant information
* Raw competition reports
* Detailed exploitation instructions
* Sensitive proof-of-concept information

Security testing should only be performed against systems where explicit authorization has been provided.

---

## 📁 Repository Structure

```text
permikomnas-web-security-assessment/
│
├── README.md
├── findings.md
└── methodology.md
```

The repository is intentionally kept limited to sanitized documentation suitable for a professional portfolio.
