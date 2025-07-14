# AWS VPC with Public and Private Subnets

## 🧭 Overview

This project demonstrates a production-style VPC setup in AWS:

- ✅ Public and Private Subnets
- ✅ Internet Gateway (for public subnet)
- ✅ NAT Gateway (for private subnet)
- ✅ Bastion Host for secure SSH
- ✅ EC2 instance in each subnet
- ✅ Route Tables, Security Groups

---

## 🌐 Network Architecture

VPC CIDR: `10.0.0.0/16`

| Component       | Subnet CIDR     | Notes                        |
|----------------|------------------|------------------------------|
| Public Subnet  | `10.0.1.0/24`    | Bastion host, IGW access     |
| Private Subnet | `10.0.2.0/24`    | App server, NAT access only  |

![Architecture](./architecture-diagram.png)

---

## 🚀 Deployment Options

### Option 1: Manual (AWS Console)

Follow this [step-by-step guide](#).

### Option 2: Terraform

In the `terraform/` directory:

```bash
cd terraform
terraform init
terraform apply
