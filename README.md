# 🔐 Google Cloud Security: Use Reports to Remediate Findings  
Hands-on security lab where I used **Google Cloud Security Command Center (SCC)** to identify, analyze, and remediate vulnerabilities in cloud resources.

This project demonstrates real-world **Cloud Security Engineer** workflows:
- Reviewing SCC findings  
- IAM analysis  
- Identifying over-permissions  
- Misconfiguration review  
- Applying remediation steps  
- Verifying security posture improvement  

---

## 🧭 Lab Objectives

✔ Understand the purpose of Security Command Center (SCC)  
✔ Detect misconfigurations using built-in security reports  
✔ Identify IAM over-permissions  
✔ Review VM security findings  
✔ Apply remediation actions  
✔ Validate that findings are resolved  

---

## 🛠 Tools & Services Used

- **Google Cloud Security Command Center**
- **IAM Analyzer**
- **VM Instance Security Reports**
- **BigQuery (underlying report queries)**
- **Compute Engine**
- **Cloud Storage (optional logs)**
- **Google Cloud Console**

---

## 📊 What Was Reviewed

### 1️⃣ **IAM Over-Permission Analysis**
- Detected identities with *excessive roles*  
- Found broad roles such as:
  - `Editor`
  - `Owner`
  - `Compute Admin`
- Applied Principle of Least Privilege

### 2️⃣ **VM Security Findings**
- Public IP exposure check  
- Firewall rule misconfigurations  
- OS security recommendations  
- Shielded VM evaluation  

### 3️⃣ **Security Command Center Findings**
Common finding categories:

- **High** → Public access, risky secrets, misconfigured IAM  
- **Medium** → Outdated VM images, missing OS patches  
- **Low** → Informational notices

---

## 🛡 Remediation Steps Performed

✔ Removed overly permissive IAM roles  
✔ Replaced broad roles → specific roles  
✔ Disabled unnecessary public access  
✔ Applied firewall rule restrictions  
✔ Reviewed exposed service accounts  
✔ Enabled missing security features  

---

## 📁 Folder Structure


