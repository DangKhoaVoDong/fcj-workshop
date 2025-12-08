---
title: "Event 5"
date: ""
weight: 5
chapter: false
pre: " <b> 4.5. </b> "
---
# Event Report: “Workshop: AWS Well-Architected Security Pillar”

### Event Objectives

- Understand the importance of the Security Pillar within the AWS Well-Architected Framework.
- Master the Shared Responsibility Model and core principles: Least Privilege, Zero Trust, Defense in Depth.
- Learn how to apply the 5 key security domains: IAM, Detection, Infrastructure Protection, Data Protection, and Incident Response.
- Identify common security threats in Vietnam and how to prevent them.

### List of Speakers

- **AWS Security Specialists Team.**

### Key Highlights

The workshop focused deeply on the 5 main domains (5 Pillars) of Cloud security:

#### 1. Identity & Access Management (IAM)
- **Principle:** Avoid using long-term credentials for users.
- **Solutions:**
    - Use **IAM Roles** instead of fixed Access Keys.
    - **IAM Identity Center:** Centralized Single Sign-On (SSO) management.
    - **SCP (Service Control Policies):** Establish security guardrails for multi-account environments.
    - Enforce **MFA** and periodic credential rotation.

#### 2. Detection
- **Comprehensive Logging:** Enable CloudTrail (organization-level), VPC Flow Logs, and S3 access logs.
- **Detection Tools:**
    - **Amazon GuardDuty:** Detect anomalous behavior using Machine Learning.
    - **AWS Security Hub:** Centralized security posture management.
- **Detection-as-Code:** Automate alert rule creation via infrastructure code.

#### 3. Infrastructure Protection
- **Network Security:** VPC segmentation, placing resources in private subnets if public access is not required.
- **Defense in Depth:** Combine Security Groups (instance-level firewall), NACLs (subnet-level firewall), AWS WAF (Web App Firewall), and AWS Shield (DDoS protection).

#### 4. Data Protection
- **Encryption:** Encrypt data both at-rest and in-transit.
- **Key Management:** Use **AWS KMS** to manage encryption keys and establish key rotation policies.
- **Secrets Management:** Do not hard-code passwords in code; use **AWS Secrets Manager** to store and automatically rotate DB credentials.

#### 5. Incident Response (IR)
- **IR Lifecycle:** Preparation -> Detection -> Containment -> Investigation -> Recovery.
- **Automation:** Use AWS Lambda and Step Functions to automate response actions (e.g., automatically revoking permissions of exposed IAM users, isolating infected EC2 instances).

### Key Learnings

#### Security Mindset
- **Security is Day 0:** Security is not the final step before deployment but must be integrated from the design phase (Shift Left Security).
- **Zero Trust:** Do not trust any user or device; always authenticate and authorize every request.
- **Automate Security:** Humans can make mistakes, but code is consistent. Automate as many security processes as possible.

#### Technical Knowledge
- Clearly distinguished the difference and coordination between **Security Groups** (stateful) and **NACLs** (stateless).
- Understood how **KMS Envelope Encryption** works to protect data effectively.

### Application to Work

- **Project Audit:** Immediately check Security Groups in the internship project to remove unnecessary `0.0.0.0/0` rules (especially for SSH/RDP ports).
- **Protect Secrets:** Move all database credentials currently in configuration files to **AWS Secrets Manager**.
- **Enable GuardDuty:** Propose enabling GuardDuty to monitor suspicious behaviors in the team's AWS account.

### Event Experience

The **Well-Architected Security Pillar** workshop completely changed my perspective on security.

#### "Startled" by Real-world Threats
- The sharing session on **Top threats** in Vietnam made me realize that exposing Access Keys or leaving S3 buckets public are elementary mistakes but have extremely serious consequences.

#### Visual Demos
- Watching a live demo of how a hacker exploits an IAM vulnerability and how the system automatically detects and blocks it using Lambda was truly convincing. It proved the power of **Automated Incident Response**.

#### Standardized Process
- I learned that incident response is not about "struggling" to fix errors but requires a clear **Playbook**: isolate, collect evidence (forensics), and then recover.

#### Key Takeaways
- Security is everyone's responsibility (Shared Responsibility), not just the Security team's. As a Developer, writing secure code and configuring infrastructure correctly is the biggest contribution to the organization's security.

#### Event Photos
* Insert photos of slides about the Shared Responsibility Model, GuardDuty demo, or the workshop space here *

> Overall: The event helped me build a solid foundation to become an engineer who is not only skilled in features but also trustworthy in security (Security-first Engineer).