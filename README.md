# CST8919 – Cloud Service Alternatives Report

**Author:** Ololade Akinrinsola  
**Course:** DevOps Security and Compliance (Summer 2025)  
**Assignment:** Cloud Service Alternatives Report (10% Final Grade)  
**Due Date:** Week 15 (August 15, 2025)

---

## Table of Contents

- [1. Introduction](#1-introduction)  
- [2. Summary Comparison Table](#2-summary-comparison-table)  
- [3. Service-by-Service Detailed Comparison](#3-service-by-service-detailed-comparison)  
  - [3.1 Azure Active Directory (AAD)](#31-azure-active-directory-aad)  
  - [3.2 Azure Monitor & Log Analytics](#32-azure-monitor--log-analytics)  
  - [3.3 Azure Policy](#33-azure-policy)  
  - [3.4 Defender for Cloud](#34-defender-for-cloud)  
  - [3.5 Azure Sentinel (SIEM/SOAR)](#35-azure-sentinel-siemssoar)  
- [4. Pricing Comparison](#4-Pricing Comparison)
- [5. References](#5-references)

---

## 1. Introduction

This report identifies Amazon Web Services (AWS) and Google Cloud Platform (GCP) equivalents to key Azure services studied during the CST8919 course. The comparison covers service overviews, core features, security and compliance capabilities, pricing models, and DevSecOps integration, helping expand cloud security knowledge beyond Azure.

---

## 2. Summary Comparison Table

| Azure Service           | AWS Equivalent                  | GCP Equivalent                         | Notes                            |
|------------------------|--------------------------------|---------------------------------------|---------------------------------|
| Azure Active Directory (SSO, IAM) | AWS IAM & AWS Cognito             | Google Cloud IAM & Identity Platform  | Identity and access management  |
| Azure Monitor & Log Analytics | Amazon CloudWatch & AWS CloudTrail | Google Cloud Operations Suite (formerly Stackdriver) | Monitoring and log analysis      |
| Azure Policy           | AWS Config & Service Control Policies (SCPs) | Google Cloud Policy Intelligence & Organization Policy | Governance and compliance       |
| Defender for Cloud     | AWS Security Hub & GuardDuty    | Google Cloud Security Command Center  | Threat detection and posture    |
| Azure Sentinel (SIEM/SOAR) | AWS Security Hub + GuardDuty + Detective | Google Chronicle                      | Security information & event management |

---

## 3. Service-by-Service Detailed Comparison

### 3.1 Azure Active Directory (AAD)

- **Overview:**  
  Cloud-based identity and access management service with single sign-on (SSO), multifactor authentication, and conditional access.

- **AWS Equivalent:**  
  - **AWS IAM:** User and permission management for AWS resources.  
  - **AWS Cognito:** User sign-up, sign-in, and access control for web and mobile apps, supports SSO and federation.

- **GCP Equivalent:**  
  - **Google Cloud IAM:** Fine-grained access control for GCP resources.  
  - **Identity Platform:** Provides user authentication and identity management including SSO.

- **Core Features:**  
  - Role-based access control (RBAC)  
  - Multi-factor authentication (MFA)  
  - Conditional access policies  
  - User and group management

- **Security & Compliance:**  
  - Certifications include ISO 27001, SOC 1/2/3, HIPAA, GDPR for all providers.

- **Pricing Model:**  
  Usually free tier available; charges based on number of users, authentication events, and advanced features.

- **DevSecOps Integration:**  
  Integrates with CI/CD pipelines for automated user provisioning, supports APIs and SDKs.

---

### 3.2 Azure Monitor & Log Analytics

- **Overview:**  
  Full-stack monitoring service including metrics, logs, alerts, and dashboards.

- **AWS Equivalent:**  
  - **Amazon CloudWatch:** Metrics, logs, alarms, dashboards.  
  - **AWS CloudTrail:** Auditing API activity and account events.

- **GCP Equivalent:**  
  - **Google Cloud Operations Suite:** Includes Monitoring, Logging, Trace, Debugger.

- **Core Features:**  
  - Real-time monitoring & alerting  
  - Log aggregation and analytics  
  - Custom dashboards and Kusto Query Language (KQL) on Azure  
  - Integration with incident management tools

- **Security & Compliance:**  
  Data encryption in transit and at rest, compliance with major standards.

- **Pricing Model:**  
  Charges based on data volume ingested, retention period, and custom metrics.

- **DevSecOps Integration:**  
  Supports integration with CI/CD workflows, alert automation, and third-party tools.

---

### 3.3 Azure Policy

- **Overview:**  
  Governance tool that enforces organizational rules on resources via policies and initiatives.

- **AWS Equivalent:**  
  - **AWS Config:** Tracks resource compliance and changes.  
  - **Service Control Policies (SCPs):** Enforce governance across accounts in AWS Organizations.

- **GCP Equivalent:**  
  - **Google Cloud Policy Intelligence:** Analyzes IAM policies.  
  - **Organization Policy Service:** Enforces constraints across resources.

- **Core Features:**  
  - Policy definitions and assignments  
  - Compliance evaluation  
  - Remediation tasks  
  - Initiatives to group policies

- **Security & Compliance:**  
  Helps meet compliance by ensuring resource configurations comply with standards.

- **Pricing Model:**  
  Generally pay-per-evaluation or free with included resource limits.

- **DevSecOps Integration:**  
  Policy-as-code can be integrated in CI/CD pipelines for automated governance.

---

### 3.4 Defender for Cloud

- **Overview:**  
  Cloud security posture management and threat protection.

- **AWS Equivalent:**  
  - **AWS Security Hub:** Centralizes security findings.  
  - **Amazon GuardDuty:** Threat detection service.

- **GCP Equivalent:**  
  - **Google Cloud Security Command Center:** Unified security and risk platform.

- **Core Features:**  
  - Continuous security assessment  
  - Threat detection  
  - Recommendations and remediation guidance

- **Security & Compliance:**  
  Complies with major certifications; improves overall cloud security posture.

- **Pricing Model:**  
  Based on resource counts and data analyzed.

- **DevSecOps Integration:**  
  Integrates with security automation, alerts, and workflow orchestration.

---

### 3.5 Azure Sentinel (SIEM/SOAR)

- **Overview:**  
  Cloud-native Security Information and Event Management (SIEM) and Security Orchestration Automated Response (SOAR).

- **AWS Equivalent:**  
  Combination of **AWS Security Hub**, **Amazon GuardDuty**, and **Amazon Detective**.

- **GCP Equivalent:**  
  - **Google Chronicle:** Security analytics and threat hunting.

- **Core Features:**  
  - Aggregates security data  
  - Real-time threat detection  
  - Automated response playbooks  
  - Integration with third-party security tools

- **Security & Compliance:**  
  Helps meet regulatory requirements via comprehensive event logging and incident response.

- **Pricing Model:**  
  Based on volume of data ingested and retention.

- **DevSecOps Integration:**  
  Supports automated workflows for incident handling and remediation.

---
## 4. Pricing Comparison

| Service                  | Azure Pricing Summary                                           | AWS Pricing Summary                                           | GCP Pricing Summary                                            |
|--------------------------|----------------------------------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------|
| **Azure Active Directory (AAD)** | Free tier for basic features; Premium P1 $6/user/month, Premium P2 $9/user/month | IAM is free; AWS Cognito charges ~$0.0055 per monthly active user (MAU) | IAM free; Identity Platform charges ~$0.0055 per MAU            |
| **Azure Monitor & Log Analytics** | Charges based on data ingested (~$2.30 per GB) and retention | CloudWatch charges per custom metric (~$0.30 per metric/month), logs ingestion (~$0.50 per GB) | Operations Suite charges per GB ingested (logs ~$0.50/GB), metrics free up to limits |
| **Azure Policy**          | Generally free; charges may apply for advanced features or high volume | AWS Config charges ~$0.003 per configuration item recorded; SCPs free | Organization Policy free; Policy Intelligence free; charges apply for related logging |
| **Defender for Cloud**    | Charges per resource protected (e.g., $15 per node per month) | AWS Security Hub charges $0.001 per security finding; GuardDuty ~$4 per million events | Security Command Center standard tier is free; premium tier pricing upon request |
| **Azure Sentinel**        | Charges based on data ingested (starting at ~$2.46 per GB) and retention | AWS Security Hub free for first 10,000 events, then $0.001 per event; Detective and GuardDuty priced separately | Chronicle pricing based on ingestion volume; pricing available upon request |

---

### Notes:

- Pricing varies significantly by region, volume, and usage pattern.  
- Most services offer free tiers with limited usage.  
- Detailed pricing is available on each provider's official pricing pages (links below).

---

## 5. References

- [Microsoft Azure Documentation](https://docs.microsoft.com/en-us/azure/)  
- [AWS Documentation](https://docs.aws.amazon.com/)  
- [Google Cloud Documentation](https://cloud.google.com/docs)  
- [Azure Policy Overview](https://docs.microsoft.com/en-us/azure/governance/policy/overview)  
- [Azure Sentinel](https://azure.microsoft.com/en-us/services/azure-sentinel/)  
- [Kusto Query Language (KQL)](https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/)  
- [Auth0 Flask Integration](https://auth0.com/docs/quickstart/webapp/python)

- [Azure Active Directory Pricing](https://azure.microsoft.com/en-us/pricing/details/active-directory/)  
- [AWS IAM Pricing](https://aws.amazon.com/iam/pricing/) & [AWS Cognito Pricing](https://aws.amazon.com/cognito/pricing/)  
- [Google Cloud IAM Pricing](https://cloud.google.com/identity/pricing) & [Identity Platform Pricing](https://cloud.google.com/identity-platform/pricing)  

- [Azure Monitor Pricing](https://azure.microsoft.com/en-us/pricing/details/monitor/)  
- [AWS CloudWatch Pricing](https://aws.amazon.com/cloudwatch/pricing/)  
- [Google Cloud Operations Suite Pricing](https://cloud.google.com/stackdriver/pricing)  

- [Azure Policy Pricing](https://azure.microsoft.com/en-us/pricing/details/azure-policy/)  
- [AWS Config Pricing](https://aws.amazon.com/config/pricing/)  
- [Google Cloud Organization Policy Pricing](https://cloud.google.com/resource-manager/docs/organization-policy/overview)  

- [Defender for Cloud Pricing](https://azure.microsoft.com/en-us/pricing/details/defender-for-cloud/)  
- [AWS Security Hub Pricing](https://aws.amazon.com/security-hub/pricing/)  
- [Google Cloud Security Command Center Pricing](https://cloud.google.com/security-command-center/pricing)  

- [Azure Sentinel Pricing](https://azure.microsoft.com/en-us/pricing/details/azure-sentinel/)  
- [AWS GuardDuty Pricing](https://aws.amazon.com/guardduty/pricing/)  
- [Google Chronicle Pricing](https://cloud.google.com/chronicle/pricing)  


---


