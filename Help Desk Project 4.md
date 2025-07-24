
# 🧾 Mock Ticketing Journal – Helpdesk Simulation

## 🧰 Tools Simulated
- Windows Server 2022 (Active Directory)
- ADUC (Active Directory Users and Computers)
- VPN Client (e.g., Fortinet / Cisco AnyConnect)
- Authenticator Apps (Microsoft / Google)
- Printer & IP troubleshooting via CMD
- Ticketing format based on ITIL standards

---

## 🎯 Objective

Simulate a week in a helpdesk queue by documenting 5 mock Tier 1 support tickets.

This journal demonstrates:

- Common issues faced by end-users
- Technical troubleshooting steps
- Communication and escalation
- Reflection and learning

---

## 📋 Ticket 1: Password Reset & Account Lockout

**Issue Summary:**
User unable to log into their computer after multiple failed attempts.

**Diagnosis:**
Checked ADUC — account `jdoe` was locked due to failed login policy.

**Resolution Steps:**
- Unlocked the account in ADUC  
- Reset password to `SecureWelcome!99`  
- Confirmed access via user test login

**Reflection:**
This was my first experience unlocking a domain user. I gained confidence using ADUC and now understand account policies better.

---

## 📋 Ticket 2: VPN Not Connecting

**Issue Summary:**
Remote user reported VPN hanging at 80%.

**Diagnosis:**
User entered outdated cached credentials. VPN logs showed failed SSO handshake.

**Resolution Steps:**
- Instructed user to clear saved credentials  
- Flushed DNS cache with `ipconfig /flushdns`  
- Re-entered login info manually — VPN connected

**Reflection:**
Learned how cached credentials can cause VPN issues and how to use basic CMD tools to assist.

---

## 📋 Ticket 3: MFA Setup Issue

**Issue Summary:**
User could not finish MFA setup on new phone.

**Diagnosis:**
Previous device still linked to Microsoft Authenticator — sync error triggered.

**Resolution Steps:**
- Reset MFA configuration in admin portal  
- Guided user through setting up new device  
- Confirmed 2FA prompt on login

**Reflection:**
This taught me the importance of clear step-by-step communication and user patience during onboarding issues.

---

## 📋 Ticket 4: Printer Offline Error

**Issue Summary:**
User unable to print; system reported “offline” error.

**Diagnosis:**
Pinged printer IP — unresponsive. Device was found powered off.

**Resolution Steps:**
- Powered on printer  
- Reconfirmed IP address via printer screen  
- Re-added printer on the workstation using correct IP

**Reflection:**
Reinforced how physical checks and basic ping tests can quickly solve user-reported network issues.

---

## 📋 Ticket 5: App Install Request Denied

**Issue Summary:**
User requested installation of unapproved software.

**Diagnosis:**
App not on company whitelist — required admin-level exception.

**Resolution Steps:**
- Politely informed user of software policy  
- Escalated request to supervisor  
- Logged all actions for compliance

**Reflection:**
Helped me understand how to balance policy enforcement with user needs, and how to escalate professionally.

---

## 📝 Final Reflection

> This project simulated a real helpdesk queue and helped me build confidence in both technical troubleshooting and soft skills like communication, documentation, and knowing when to escalate.

---

