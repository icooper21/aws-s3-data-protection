# aws-s3-data-protection
Hands-on AWS lab demonstrating how S3 misconfigurations can expose data publicly, and how to secure it using proper access controls and encryption.

# 🔐 AWS S3 Data Protection & Encryption Lab

## 📌 Project Overview
This project demonstrates secure data storage in AWS by configuring S3 encryption, intentionally introducing a public access misconfiguration, and remediating the issue to restore a secure state.

## 🎯 Objectives
- Configure secure S3 bucket with encryption enabled
- Simulate public data exposure through misconfiguration
- Validate public accessibility via object URL
- Remediate exposure by removing public access
- Reinforce security using block public access settings

## 🛠️ Technologies Used
- :contentReference[oaicite:0]{index=0}
- :contentReference[oaicite:1]{index=1} (conceptual)


## 🚀 1. Secure Bucket Configuration
- Created S3 bucket with default encryption enabled (SSE-S3)
- Blocked all public access at bucket level
- Configured secure object ownership (ACLs initially disabled)

## ⚠️ 2. Misconfiguration: Public Access Enabled
- Modified permissions to allow public read access at object level
- Uploaded file and configured it to be publicly accessible
- Created intentional data exposure scenario

![Public File Access](file-access.png)

## 🌐 3. Exposure Validation
- Accessed object via public URL in browser
- Confirmed data was publicly accessible without authentication

## 🔐 4. Remediation: Secure Configuration Restored
- Removed public read permissions from object
- Re-enabled bucket-level block public access
- Verified only account owner retains access

![File Secured](file-secured.png)

![Block Public Access](images/block-public-access.png)


## ⚠️ Security Analysis
### Risk Identified
- Publicly accessible S3 objects can expose sensitive data to the internet

### Impact
- Unauthorized data access
- Potential data leakage and compliance violations

## 📚 Key Learnings
- Misconfigured S3 permissions can easily expose data
- Public access must be tightly controlled at both object and bucket levels
- Defense-in-depth (ACL + block public access) strengthens security posture


## 🧠 Conclusion
This lab demonstrates how improper S3 configurations can lead to data exposure and highlights the importance of enforcing secure defaults and validating access controls in cloud environments.
