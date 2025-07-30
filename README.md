# Terraform EC2 Instance Setup on AWS

## 📌 Overview
This project uses **Terraform** to automate the provisioning of an EC2 instance on **AWS**. It includes key pair creation, security group setup, and instance deployment using the default VPC.

## 📁 Files and Structure
- `main.tf`: Contains resources for EC2, key pair, security group, and default VPC.
- `provider.tf`: Specifies AWS region.
- `terraform.tf`: Declares required provider and version.

## 🧰 Technologies Used
- Terraform
- AWS EC2
- AWS VPC and Security Groups
- SSH Key Authentication

## 🚀 How to Use

### 1. Clone the Repository
```bash
git clone <repo-url>
cd <repo-directory>
```

### 2. Set Up AWS Credentials

Ensure AWS CLI is configured with IAM credentials:

```bash
aws configure
```

### 3. Initialize Terraform

```bash
terraform init
```

### 4. Review the Plan

```bash
terraform plan
```

### 5. Apply the Configuration

```bash
terraform apply
```

### 6. SSH into the EC2 Instance

```bash
ssh -i ~/.ssh/id_rsa ec2-user@<public-ip>
```

---

## 🔐 Security Group Rules

- **Port 22 (SSH)** — open to all IPs
- **Port 80 (HTTP)** — open to all IPs
- **All outbound traffic allowed**

---

## 📝 Notes

- Ensure your SSH key exists at `~/.ssh/id_rsa.pub`.
- You can update the AMI ID and instance type based on your AWS region.
- This setup uses the default VPC in the selected region.

---

## 📦 License

This project is licensed under the MIT License.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you would like to change.
