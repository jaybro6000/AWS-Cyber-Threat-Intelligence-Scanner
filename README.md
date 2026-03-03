# AWS Cyber Threat Intelligence Scanner

A serverless security automation tool that scans leaked credential feeds to identify corporate domain exposure. This project demonstrates how to automate threat intelligence using **AWS Lambda**, **S3**, and **CloudWatch Logs**.

---

## Execution Steps

### 1. Ingesting Threat Data
Shows the preparation of `breach_data.txt` containing simulated leaked credentials.
<img width="1366" height="688" alt="Project_The_Cyber_Threat_Intelligence_1" src="https://github.com/user-attachments/assets/eecb1ebd-cf04-451c-ba5b-26d3d13543e4" />


### 2. Secure Data Storage
Shows the S3 bucket `threat-intel-feed-2026` acting as a secure repository for the intelligence feed.
<img width="1920" height="851" alt="Project_The_Cyber_Threat_Intelligence_5" src="https://github.com/user-attachments/assets/0e4cc0c2-f810-4fe5-83cd-9f94f2c97afe" />


### 3. Provisioning the Scanner
Shows the initialization of the Python-based Lambda function `Threat-Intelligence-Scanner`.
<img width="1920" height="861" alt="Project_The_Cyber_Threat_Intelligence_2" src="https://github.com/user-attachments/assets/0e8530f2-07be-4c43-a83d-3d02cae9bc7b" />


### 4. Implementing Least Privilege
Shows the IAM Role configuration, granting the scanner restricted `ReadOnlyAccess` to S3.
<img width="1920" height="858" alt="Project_The_Cyber_Threat_Intelligence_7" src="https://github.com/user-attachments/assets/7555e284-f73a-480f-890a-0371dd7daf30" />


### 5. Developing the Logic
Shows the Python script using `boto3` to parse the feed and search for specific domain matches.
<img width="1920" height="901" alt="Project_The_Cyber_Threat_Intelligence_3" src="https://github.com/user-attachments/assets/d4c65ed2-d825-4d44-8dcb-bb5862aab7ac" />


### 6. Successful Threat Detection
Shows the Lambda execution result returning a "Threat Detected" status after a domain match.
<img width="1920" height="869" alt="Project_The_Cyber_Threat_Intelligence_8" src="https://github.com/user-attachments/assets/70a1f534-f0a3-4809-a5f2-0944d942da70" />


### 7. Security Auditing & Logging
Shows the detailed CloudWatch Log stream capturing the specific "ALERT" for security teams.
![Photo Placeholder: Project_The_Cyber_Threat_Intelligence_9.png]
