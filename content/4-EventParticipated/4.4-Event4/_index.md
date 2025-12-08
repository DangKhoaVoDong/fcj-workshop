---
title: "Event 4"
date: ""
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

# Event Report: “Workshop: DevOps on AWS”

### Event Objectives

- Understand the true DevOps Mindset and Culture.
- Master the AWS CI/CD toolset to automate the software development process.
- Learn how to manage Infrastructure as Code (IaC).
- Get familiar with Container technology and modern application deployment strategies.
- Establish comprehensive Monitoring and Observability systems.

### List of Speakers

- **AWS Technical Experts Team.**

### Key Highlights

This was a full-day workshop with in-depth knowledge, consisting of two main sessions:

#### 1. Morning Session: CI/CD & Infrastructure as Code
- **DevOps Mindset:** DevOps is not just about tools but a combination of culture, processes, and tools. Introduction to efficiency metrics (DORA metrics) such as deployment frequency and Mean Time to Recovery (MTTR).
- **AWS CI/CD Pipeline:**
    - **Source Control:** Source code management with AWS CodeCommit and Git strategies (GitFlow, Trunk-based).
    - **Build & Test:** Automating code building and testing with AWS CodeBuild.
    - **Deployment:** Automating application deployment with AWS CodeDeploy (supporting Blue/Green, Canary).
    - **Orchestration:** Coordinating the entire process using AWS CodePipeline.
- **Infrastructure as Code (IaC)::**
    - **CloudFormation:** Creating and managing AWS resources using JSON/YAML templates, drift detection.
    - **AWS CDK:** Defining infrastructure using familiar programming languages (Python, TypeScript, Java), making code reuse easier.

#### 2. Afternoon Session: Containers & Observability
- **Container Services:**
    - **Amazon ECR:** Secure Docker image storage.
    - **Amazon ECS & EKS:** Comparison of container orchestration services, scaling strategies.
    - **AWS App Runner:** Simplified container deployment solution for developers.
- **Monitoring & Observability:**
    - **CloudWatch:** Collecting metrics, logs, creating dashboards, and alarms.
    - **AWS X-Ray:** Tracing requests through distributed systems to find bottlenecks.
- **DevOps Best Practices:** Safe deployment strategies (Feature flags, A/B testing) and Incident management.

### Key Learnings

#### Technical Knowledge
- **Automation is King:** Understood the power of automating everything, from committing code to deploying to production, helping to minimize human error.
- **IaC vs. Click-ops:** Clearly recognized the superiority of using code to manage infrastructure (CDK/CloudFormation) versus manual operations on the Console (Click-ops), especially regarding environment reproducibility.
- **Observability:** Distinguished between Monitoring (Is the system working?) and Observability (Why is the system working that way?), and the crucial role of X-Ray in microservices.

#### Practical Skills
- Learned how to set up a basic CI/CD pipeline.
- Learned how to write a simple CDK script to create an S3 bucket or EC2 instance.

### Application to Work

- **Project Improvement:** Immediately apply AWS CodePipeline to the current internship project to automate code deployment whenever there is a new update.
- **Switch to IaC:** Start writing CloudFormation/CDK for currently used resources instead of creating them manually, facilitating configuration sharing with other team members.
- **Optimize Monitoring:** Set up CloudWatch Alarms to receive alerts via email/Slack when server CPU or Memory increases abnormally.

### Event Experience

The **DevOps on AWS** workshop was a high-intensity learning day but extremely valuable.

#### Depth and Flow
- The program went from Mindset to Tools and Practice, creating a very logical flow of knowledge.
- The **Blue/Green Deployment** demos helped me "see and hear" how to update applications with zero downtime - something I had only read about in theory before.

#### Career Orientation Opportunity
- The Q&A session at the end regarding **DevOps career pathways** and the AWS certification roadmap helped me visualize the career ladder of a DevOps Engineer more clearly.

#### Learning Environment
- Studying at the AWS office with full facilities and direct support from experts made absorbing difficult concepts like Kubernetes (EKS) or Tracing much easier.

#### Key Takeaways
- DevOps is a journey of Continuous Improvement. Learning tools is necessary, but the mindset of automation and measurement is the core.

#### Event Photos
* Insert screenshots of the CI/CD pipeline, architecture diagrams on the board, or photos with speakers here *

> Overall: The event helped me "upgrade" from a simple programmer mindset to that of a modern system engineer who knows how to master the product operation process.