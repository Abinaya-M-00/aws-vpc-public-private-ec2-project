# 🌐 AWS VPC Public and Private EC2 Project

## 📌 Project Overview

This project demonstrates how to build a custom AWS network infrastructure using a Virtual Private Cloud (VPC). The architecture includes public and private subnets, route tables, an Internet Gateway, security groups, and EC2 instances.

The main goal of this project is to understand how AWS networking works and how public and private resources can be deployed securely inside a VPC.

---

## 🏗️ Architecture

```text
                    Internet
                       │
                       ▼
                Internet Gateway
                       │
                       ▼
                Public Route Table
                       │
                       ▼
        ┌───────────────────────────┐
        │      Public Subnet        │
        │       10.0.1.0/24         │
        │                           │
        │      Public EC2           │
        │      (Bastion Host)       │
        └───────────────────────────┘
                       │
                       │ Private Network
                       ▼
        ┌───────────────────────────┐
        │      Private Subnet       │
        │       10.0.2.0/24         │
        │                           │
        │      Private EC2          │
        │     No Public IP          │
        └───────────────────────────┘
```

---

## 🛠️ AWS Services Used

* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Tables
* Security Groups

---

## ⚙️ Project Configuration

### VPC

* **VPC Name:** `my-project-vpc`
* **CIDR Block:** `10.0.0.0/16`

### Public Subnet

* **Subnet Name:** `public-subnet`
* **CIDR Block:** `10.0.1.0/24`

### Private Subnet

* **Subnet Name:** `private-subnet`
* **CIDR Block:** `10.0.2.0/24`

---

## 🔐 Security Configuration

### Public EC2 Security Group

* SSH (Port 22)
* Used for administrative access to the Public EC2 instance.

### Private EC2 Security Group

* SSH (Port 22)
* Access allowed from the Public EC2 security group.

---

## 🚀 Project Implementation Steps

1. Created a custom VPC.
2. Created a public subnet.
3. Created a private subnet.
4. Created and attached an Internet Gateway.
5. Created a public route table and configured internet access.
6. Created a private route table.
7. Associated the public and private subnets with their respective route tables.
8. Created security groups for both EC2 instances.
9. Launched a Public EC2 instance with a public IP address.
10. Launched a Private EC2 instance without a public IP address.
11. Successfully connected to the Public EC2 instance.

---

## 🎯 Key Learning Outcomes

* Understanding AWS VPC networking.
* Difference between public and private subnets.
* Configuring Internet Gateway and Route Tables.
* Using Security Groups as virtual firewalls.
* Deploying EC2 instances inside different subnets.
* Understanding public and private IP addressing.
* Basic Bastion Host architecture.

---

## 👩‍💻 Author

**Abinaya M**

Aspiring Cloud and Engineer

---

⭐ If you found this project useful, feel free to star the repository!
