# Secure Private Infrastructure Deployment with Bastion Access and IAM Role-Based Architecture

## 📌 Project Overview
This project demonstrates a secure AWS architecture where:
- Application servers run in private subnets
- No public IP is assigned to backend servers
- Access is controlled via a Bastion Host
- IAM Roles are used instead of static credentials

---

## ⚙️ Tech Stack
- AWS EC2
- AWS VPC
- AWS IAM
- AWS S3
- NAT Gateway
- Internet Gateway
- Nginx

---

## 🔐 Architecture Flow
Local Machine → Bastion Host → Private EC2 → IAM Role → S3

---

## 📸 Screenshots

### 1. Architecture Overview
![Architecture](screenshots/architecture.png)

### 2. EC2 Instances
![EC2 Instances](screenshots/ec2.png)

### 3. Public Subnets Configuration
![Public Subnets](screenshots/PublicSubnets.png)

### 4. Private Subnets Configuration
![Private Subnets](screenshots/PrivateSubnets.png)

### 5. Bastion Security Group
![Bastion Security Group](screenshots/BastionSG.png)

### 6. Application Server Security Group
![Application Security Group](screenshots/AppSG.png)

### 7. Bastion SSH Access
![Bastion SSH](screenshots/bastion-ssh.png)

### 8. Private Server SSH Access via Bastion
![Private SSH](screenshots/private-ssh.png)

### 9. Application Server Setup
![App Server Setup](screenshots/AppServerSetup.png)

### 10. Application Server External Access
![App Server External Access](screenshots/AppServerExternalEccess.png)

### 11. IAM Role Configuration
![IAM Role](screenshots/iam-role.png)

### 12. IAM Role Modification
![IAM Role Modify](screenshots/iam-role-modify.png)

### 13. S3 Bucket
![S3 Bucket](screenshots/S3-Bucket.png)

### 14. S3 Access Verification
![S3 Access](screenshots/s3-access.png)

---

## 🧪 Verification

### S3 Access
```bash
aws s3 ls s3://fintech-secure-bucket
```

### SSH Flow
```bash
ssh -i key.pem ec2-user@bastion-ip
ssh -i key.pem ec2-user@private-ip
```

---

## 🔐 Security Highlights
- ✅ Private subnet isolation for application servers
- ✅ Bastion host as single entry point
- ✅ IAM role-based authentication (no static credentials)
- ✅ Security groups with least privilege access
- ✅ No public IP addresses on backend servers
- ✅ Secure SSH tunneling through bastion

---

## 🚀 Key Features
- **Secure Network Architecture**: VPC with public and private subnets
- **Bastion Host**: Controlled access point to private infrastructure
- **IAM Roles**: Temporary credentials instead of access keys
- **S3 Integration**: Secure bucket access via IAM roles
- **Production-Ready**: Suitable for fintech and compliance-heavy environments

---

## 📁 Project Structure
```
bastion-project/
 ├── README.md                    # Project documentation
 ├── documentation.pdf            # Detailed implementation guide
 ├── architecture.png             # High-level architecture diagram
 └── screenshots/                 # Implementation screenshots
   
```
