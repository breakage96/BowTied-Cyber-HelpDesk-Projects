
# 🔐 Password Reset + Account Lockout Lab

## 🧰 Tools Used
- Windows Server 2022 (Domain Controller)
- Active Directory Users and Computers (ADUC)
- Event Viewer
- PowerShell
- RDP Client (Remmina on Ubuntu)

---

## 🎯 Objective

Simulate a Tier 1 Helpdesk task:

- Reset a user’s password
- Unlock their account
- Document the process using screenshots, CLI commands, and system logs

---

## 🪜 Steps Performed

### 1. 🔍 Created a Test User
- Opened **Active Directory Users and Computers (ADUC)**
- Created user: `John Doe` / `jdoe`
- Enabled “User must change password at next logon”

📸 Screenshot:
Refer to Link at bottom

---

### 2. 🚫 Simulated Lockout
- Attempted login with incorrect passwords
- Received lockout message:
  > `"Account locked out"`

📸 Screenshot:
Refer to Link at bottom

---

### 3. ✅ Reset Password
- Reset via ADUC: New password `SecureWelcome!99`
- Unchecked “User must change password at next logon”

📸 Screenshot:
Refer to Link at bottom

**Optional PowerShell Command:**
```powershell
Set-ADAccountPassword -Identity "jdoe" -NewPassword (ConvertTo-SecureString -AsPlainText "SecureWelcome!99" -Force)
Unlock-ADAccount -Identity "jdoe"
```

---

### 4. 🔓 Unlocked the Account
- Navigated to user’s **Account** tab in ADUC
- Checked "Unlock account" if it was still locked

📸 Screenshot:
Refer to Link at bottom

---

### 5. 🔎 Event Viewer Logs
- Viewed `Windows Logs > Security`
- Filtered for:
  - `4625` = Failed logins
  - `4724` = Password reset

📸 Screenshot:
Refer to Link at bottom

---

## 📝 Reflection

> This lab gave me hands-on experience with common Helpdesk tasks. I gained confidence resetting passwords, unlocking accounts, and validating logs using Event Viewer. It helped reinforce my understanding of Windows authentication and domain security practices.

---

## 📎 Attachments
- ✅ [PDF Lab Report](Password_Reset_Account_Lockout_Lab.pdf)
- ✅ Screenshots hosted on [Imgur Album](https://imgur.com/a/aanj7GU)
