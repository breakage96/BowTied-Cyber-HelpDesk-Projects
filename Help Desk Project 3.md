
# 👥 Active Directory: Create a User + Security Group

## 🧰 Tools Used
- Windows Server (Domain Controller)
- Active Directory Users and Computers (ADUC)
- Optional: PowerShell for CLI practice
- Screenshot tool (Ubuntu + Remmina + Imgur)

---

## 🎯 Objective

Simulate two common Helpdesk tasks in a Windows domain environment:

1. Create a new user account  
2. Create a security group and assign the user

---

## 🪜 Steps Performed

### 1. 👤 Create New User (Sam Johnson)
- Opened **Active Directory Users and Computers**
- Navigated to: `corp.local > Users`
- Right-clicked **Users** → **New → User**
- Entered:
  - **First Name:** Sam  
  - **Last Name:** Johnson  
  - **Username (sAMAccountName):** sjohnson
- Set password to `TempP@ss123!`
  - Enabled: ✅ **User must change password at next logon**

---

### 2. 🏢 Create Security Group (Support Team)
- In ADUC under `corp.local > Users`
- Right-clicked → **New → Group**
- Entered:
  - **Group Name:** Support Team  
  - **Scope:** Global  
  - **Type:** Security

---

### 3. ➕ Add User to Group
- Right-clicked **Support Team** → **Properties → Members → Add**
- Searched for **sjohnson**, clicked **OK**
- Verified Sam Johnson was listed as a group member

---

## 📝 Reflection

> “This project helped me practice a core Tier 1 task — user and group creation.  
> It gave me confidence navigating ADUC and understanding group permissions.”

---

## 📎 Attachments
- ✅ PDF Lab Report  
- ✅ [Screenshots Album on Imgur](https://imgur.com/gallery/help-desk-project-3-xBBBGv3)
