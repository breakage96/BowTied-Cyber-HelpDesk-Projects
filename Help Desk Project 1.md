# 🚀 Deploying a Windows Domain Controller in AWS from Ubuntu

## 🧠 Objective
Simulate a realistic enterprise environment by deploying a Windows Server 2019 Domain Controller in AWS. The project includes Active Directory setup, secure remote access from Ubuntu, and Group Policy capabilities — all from scratch.

## 🛠 Tools Used
- AWS EC2
- Windows Server 2019
- Active Directory Domain Services (AD DS)
- Ubuntu (Remmina, FreeRDP, AWS CLI)
- Group Policy Management Console (GPMC)

## 🗺 Architecture
```
[Ubuntu Host] -> RDP -> [AWS EC2: Windows Server 2019]
                            |
                            -> Active Directory Domain: lab.local
```

## ⚙ Implementation Steps

1. **Launched EC2 Instance**
   - Selected Windows Server 2019 Base AMI
   - Allowed only my IP over RDP (port 3389)
   - Used a `.pem` key pair for password retrieval

2. **Connected via RDP from Ubuntu**
   - Installed `xfreerdp` and Remmina
   - Used AWS CLI to decrypt the Windows Administrator password

3. **Installed Active Directory**
   - Added AD DS role via Server Manager
   - Promoted server to domain controller (domain: `lab.local`)

4. **Created Domain User Accounts**
   - Opened Active Directory Users and Computers
   - Created user: `VIP@lab.local`

## 🔐 Security Measures
- RDP access restricted to a trusted IP
- Password policy enforced via Group Policy
- IAM credentials secured with least privilege

## 📈 Future Improvements
- Join additional Windows/Linux clients to the domain
- Implement custom Group Policy Objects (GPOs)
- Set up centralized logging (e.g., ELK stack)
- Simulate attacks like pass-the-hash in a safe lab

## 📸 Screenshots

### Active Directory Initialized (lab.local domain)
![AD Screenshot](remmina_54.210.118.92_54.210.118.92_20250716-020140.png)

### Creating a New Domain User (VIP@lab.local)
![User Creation Screenshot](remmina_54.210.118.92_54.210.118.92_20250716-020258.png)
