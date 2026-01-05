# AWS Security Hub: Cloud Security Posture Management in Practice  
> Centralised Visibility, Continuous Compliance & Automated Response in AWS

This project explores **AWS Security Hub**, AWS’s native **Cloud Security Posture Management (CSPM)** service. It focuses on understanding how Security Hub provides a **centralised view of security findings across multiple AWS services and accounts**, and how it can be used as the foundation for a scalable cloud security strategy.

AWS Security Hub was one of the first native AWS security tools many cloud security engineers encounter — and for good reason. It integrates deeply with the AWS ecosystem and allows you to start assessing your security posture almost immediately.

---

## 🎯 Project Objectives

By completing this project, you will:

- Understand what **AWS Security Hub** is and where it fits in cloud security
- Learn how Security Hub aggregates findings across AWS services
- Interpret **Cloud Security Posture reports**
- Explore security automation and response workflows
- Identify real-world challenges in operating CSPM tools at scale
- Understand how Security Hub aligns with organisational security controls

---

## 🧠 Key Concepts Covered

- Cloud Security Posture Management (CSPM)
- Security standards and benchmarks (CIS, AWS Best Practices, PCI DSS)
- Centralised security monitoring
- Security automation and remediation
- Multi-account AWS security strategy

---

## 🖼️ High-Level Architecture

<!-- IMAGE PLACEHOLDER -->
<!-- Diagram: AWS Accounts → Security Services → Security Hub → Dashboard / Automation -->
![AWS Security Hub Architecture](images/security-hub-architecture.png)

---

## 🔐 What is AWS Security Hub?

**AWS Security Hub** is a native AWS security service that provides a **comprehensive view of your security posture** across your AWS environment.

It:
- Aggregates findings from multiple AWS security services
- Correlates and prioritises issues
- Continuously evaluates your environment against industry standards
- Centralises visibility across **multiple AWS accounts**

Because it is native to AWS, you don’t need to configure third-party integrations, external identities, or complex IAM trust relationships to get started.

---

## ✨ Key Features

### 1️⃣ Cloud Security Posture Reports

AWS Security Hub continuously evaluates your AWS environment against:

- **AWS Foundational Security Best Practices**
- **CIS Benchmarks**
- **PCI DSS** (where applicable)

It generates posture reports that:
- Highlight misconfigurations
- Show compliance gaps
- Help track security improvements over time

<!-- IMAGE PLACEHOLDER -->
![Security Posture Report](images/security-posture.png)

---

### 2️⃣ Security Automation and Response

Security Hub supports automated responses to findings through integrations with:

- **AWS Lambda**
- **EventBridge**
- **Step Functions**

This allows teams to:
- Automatically remediate common issues
- Reduce mean time to response (MTTR)
- Enforce security controls consistently

<!-- IMAGE PLACEHOLDER -->
![Security Automation](images/security-automation.png)

---

### 3️⃣ Correlated Security Findings

Security Hub aggregates and correlates findings from AWS services such as:

- Amazon GuardDuty
- AWS Inspector
- Amazon Macie
- Third-party security products

By correlating these findings, Security Hub provides a **prioritised view of risk**, helping security teams focus on what matters most.

<!-- IMAGE PLACEHOLDER -->
![Correlated Findings](images/correlated-findings.png)

---

## 🧾 TL;DR

AWS Security Hub:
- Gathers findings from AWS and third-party tools
- Compares them against security standards
- Displays everything in a central dashboard
- Helps teams prioritise, remediate, and track security issues

---

## 🛠️ Hands-On Walkthrough

### 1️⃣ Enable AWS Security Hub

1. Open the **AWS Management Console**
2. Navigate to **Security Hub**
3. Enable the service

<!-- IMAGE PLACEHOLDER -->
![Enable Security Hub](images/enable-security-hub.png)

---

### 2️⃣ Enable a Security Standard

For this project, enable:

**AWS Foundational Security Best Practices v1.0.0**

AWS provides a **30-day free trial**, making it ideal for learning and experimentation.

<!-- IMAGE PLACEHOLDER -->
![Enable Standards](images/enable-standards.png)

---

### 3️⃣ Review Findings

From the main Security Hub dashboard, you can view:
- All benchmark findings
- Severity levels
- Affected resources
- Compliance status

<!-- IMAGE PLACEHOLDER -->
![Security Hub Dashboard](images/security-hub-dashboard.png)

---

### 4️⃣ Explore the Console

Key areas to explore:
- Findings
- Insights
- Standards
- Settings

This helps build intuition for how Security Hub is used in real environments.

---

## ⚠️ The Real Challenge: Operating CSPM at Scale

Turning on Security Hub is easy. **Operating it effectively is not.**

Key challenges include:

- Designing a **centralised security account**
- Filtering and suppressing noisy findings
- Customising rules to match real risk
- Integrating findings into:
  - Ticketing systems
  - SIEMs
  - ChatOps tools
- Automating remediation without breaking workloads

Out-of-the-box, Security Hub can generate **a large volume of findings**. Without a clear plan, alerts risk being ignored.

---

## 🏗️ Best Practice Considerations

- Deploy Security Hub using **Infrastructure as Code**
- Centralise findings across AWS accounts
- Align findings with organisational security objectives
- Use automation selectively and intentionally
- Regularly review and tune controls

---

## 🧯 Disable When Finished

To avoid ongoing costs:

```text
Security Hub → Settings → General → Disable
