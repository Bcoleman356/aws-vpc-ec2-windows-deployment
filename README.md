# 🌐 AWS VPC & EC2 Windows Instance Deployment

![AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![EC2](https://img.shields.io/badge/Amazon_EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white)
![VPC](https://img.shields.io/badge/Amazon_VPC-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

## 📋 Overview

This project demonstrates building a complete private cloud network architecture on AWS from scratch — provisioning a custom Virtual Private Cloud (VPC), configuring subnets, defining network routing rules, and deploying a Windows EC2 instance inside the private network environment.

This is not a basic "launch an instance" tutorial. This project builds the full network foundation first — VPC, subnet, security groups, and routing — then provisions compute inside a properly secured private network. That's how enterprise cloud environments are actually built.

---

## 🎯 What I Built

A fully functional private AWS network environment with a Windows EC2 instance deployed inside a custom VPC — simulating a real enterprise cloud infrastructure deployment from the network layer up.

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────┐
│                  AWS Cloud                          │
│                                                     │
│  ┌─────────────────────────────────────────────┐   │
│  │           Custom VPC                        │   │
│  │        (Private Network)                    │   │
│  │                                             │   │
│  │  ┌─────────────────────────────────────┐   │   │
│  │  │            Subnet                   │   │   │
│  │  │       (Network Segment)             │   │   │
│  │  │                                     │   │   │
│  │  │  ┌──────────┐   ┌───────────────┐  │   │   │
│  │  │  │  Windows  │   │   Security    │  │   │   │
│  │  │  │ EC2       │   │   Group       │  │   │   │
│  │  │  │ Instance  │   │   (Firewall   │  │   │   │
│  │  │  │           │   │    Rules)     │  │   │   │
│  │  │  └──────────┘   └───────────────┘  │   │   │
│  │  └─────────────────────────────────────┘   │   │
│  │                                             │   │
│  │  ┌─────────────┐   ┌─────────────────┐    │   │
│  │  │  Internet   │   │  Route Table    │    │   │
│  │  │  Gateway    │   │  (Traffic       │    │   │
│  │  │             │   │   Rules)        │    │   │
│  │  └─────────────┘   └─────────────────┘    │   │
│  └─────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────┘
```

---

## 🛠️ Skills & Technologies Applied

| Category | Tools & Concepts |
|---|---|
| **Cloud Platform** | Amazon Web Services (AWS) |
| **Networking** | Virtual Private Cloud (VPC), Custom Subnet, CIDR configuration |
| **Security** | Security Groups, inbound/outbound rules, least-privilege access |
| **Routing** | Route Tables, Internet Gateway, traffic flow control |
| **Compute** | Amazon EC2, Windows Server instance, key pair authentication |
| **Access** | Remote Desktop Protocol (RDP), port 3389 security configuration |
| **Resource Management** | AWS Console, resource tagging, cost management |

---

## 📋 Key Steps Completed

### Step 1 — Custom VPC Creation
- Created a custom Virtual Private Cloud (VPC) with a defined CIDR block
- Established a fully isolated private network environment separate from the AWS default VPC
- Named and tagged all resources for governance and cost tracking

### Step 2 — Subnet Configuration
- Created a custom subnet within the VPC with a specific IP address range
- Configured subnet availability zone placement for the target region
- Enabled auto-assign public IP for instances deployed within the subnet

### Step 3 — Internet Gateway & Route Table
- Created and attached an Internet Gateway to the VPC for external connectivity
- Configured Route Table with routing rules directing internet-bound traffic through the gateway
- Associated Route Table with the custom subnet

### Step 4 — Security Group Configuration (Networking Rules)
- Created a custom Security Group defining inbound and outbound traffic rules
- Configured inbound rule allowing RDP access (port 3389) from authorized IP only
- Set outbound rules controlling traffic leaving the instance
- Applied least-privilege principles — only required ports open, all others denied by default

### Step 5 — Windows EC2 Instance Provisioning
- Selected Windows Server AMI for the EC2 instance
- Chose appropriate instance type (t2.micro) for the lab environment
- Attached the instance to the custom VPC, subnet, and security group
- Generated and downloaded key pair for secure authentication
- Launched instance and validated successful deployment

### Step 6 — Remote Access Validation
- Decrypted Windows administrator password using the key pair
- Connected via Remote Desktop Protocol (RDP) to the running Windows instance
- Validated full network connectivity and instance operation within the private VPC environment

---

## 🔐 Security Concepts Demonstrated

| Concept | Implementation |
|---|---|
| **Network Isolation** | Custom VPC provides full isolation from other AWS accounts and default networking |
| **Subnet Segmentation** | Private subnet segments the network — resources grouped by function and security zone |
| **Least Privilege Access** | Security Group rules open only port 3389 — all other inbound traffic denied by default |
| **Defense in Depth** | Multiple security layers — VPC isolation + Security Group rules + key pair authentication |
| **Traffic Control** | Route Table rules explicitly define allowed traffic paths — no implicit routing |
| **Key Pair Authentication** | RDP access secured with key pair — stronger than password-only access |

---

## 💡 AWS vs Azure — Architecture Comparison

| Concept | AWS | Azure Equivalent |
|---|---|---|
| Private Network | VPC | Virtual Network (VNet) |
| Network Segment | Subnet | Subnet |
| Firewall Rules | Security Group | Network Security Group (NSG) |
| Traffic Routing | Route Table | Route Table |
| Internet Access | Internet Gateway | Internet Gateway / Public IP |
| Virtual Machine | EC2 Instance | Azure Virtual Machine |

Understanding both platforms makes you a genuine multi-cloud candidate. You've now built equivalent network + compute architectures on both Azure and AWS.

---

## 🎓 Certifications This Supports

| Certification | Relevant Concepts |
|---|---|
| **CompTIA Security+** *(In Progress)* | Network segmentation, firewall rules, least privilege, defense in depth |
| **Microsoft AZ-104** *(In Progress)* | VNet/VPC concepts, subnetting, NSG/Security Group equivalency |
| **AWS Cloud Practitioner** *(Future)* | VPC, EC2, Security Groups, Route Tables — direct exam content |

---

## 🗂️ Full Project Portfolio

| # | Project | Platform | Key Skills |
|---|---|---|---|
| 1 | Windows VM Deployment | Azure | NSG, RBAC, RDP |
| 2 | Linux VM Deployment | Azure | SSH, NSG, Linux |
| 3 | Cloud Storage Website | Azure | Blob Storage, SAS |
| 4 | Automate Cloud Deployments | Azure | CLI, ARM, IaC |
| 5 | Automate Azure VM with Terraform | Azure + Terraform | IaC, Terraform |
| 6 | Automate Azure Website with Terraform | Azure + Terraform | IaC, Blob Storage |
| 7 | Basic Azure VM Lab | Azure | AZ-900, AZ-104 |
| 8 | AWS S3 Lab | AWS | Multi-Cloud Storage |
| 9 | **AWS VPC & EC2 Windows Deployment** | **AWS** | **VPC, Subnet, Security Groups, EC2** |
| 10 | Active Directory Manager — CyberSec | Full-Stack App | IAM, RBAC, TypeScript |

---

## 👤 Author

**Brandon Coleman**
IT Systems Analyst | Cybersecurity · Azure Cloud · Data Analytics

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/Bcoleman356/cybersecurity-cloud-projects)

📍 Mansfield, TX
