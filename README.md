# Terraform
![image](https://github.com/user-attachments/assets/8686fa2f-20cc-4687-9f0a-2ac18061dbdb)
# 🚀 Terraform Core Workflow

Terraform's core workflow consists of three key stages: **Write**, **Plan**, and **Apply**. These stages help manage infrastructure as code in a consistent and predictable way.

---

## 📝 1. Write

- Define your **desired infrastructure** using `.tf` files written in HCL (HashiCorp Configuration Language).
- Resources can span **multiple cloud providers** and services.
- This is where you describe what infrastructure should exist.

### 💡 Example:
You might configure:
- A Virtual Private Cloud (VPC)
- Security Groups
- EC2 instances or virtual machines
- A Load Balancer for routing traffic

---

## 🔍 2. Plan

- Terraform reads the current state of your infrastructure.
- It compares that state to the desired configuration and produces an **execution plan**.
- This plan shows:
  - What will be **created**
  - What will be **updated**
  - What will be **destroyed**

### 📌 Command:
```bash
terraform plan

