# Joiner Mover Leaver (JML) Identity Lifecycle Framework  
A complete enterprise-ready identity lifecycle framework for Microsoft Entra ID.

---

## 🔹 Purpose
The JML lifecycle defines how identities are created, updated and deprovisioned.  
It ensures:

• Timely access on day one  
• Role based access changes during employment  
• Secure and complete removal of access when a user leaves  
• Governance, auditing and compliance  

---

# 1. JOINER PROCESS

## 🎯 Objectives:
• Provision a new identity  
• Assign correct access based on job role  
• Enable authentication methods  
• Ensure onboarding readiness  

## 🧩 Workflow:
1. HR raises new starter record  
2. Identity is created in Entra ID (automatic or manual)  
3. User is assigned to:
   - Department group  
   - Job role group  
   - Dynamic group memberships  
4. Access packages automatically grant:
   - M365 licence  
   - Required apps  
   - Shared folders, Teams, SharePoint  
5. MFA onboarding email sent  
6. Authentication methods registered  
7. Manager notified that account is ready  

## 🛠 Optional Automation:
• Auto-provision via HR system  
• PowerShell automation for account creation  
• Access packages for team access  

---

# 2. MOVER PROCESS

## 🎯 Objectives:
• Update access based on job changes  
• Remove old access that should no longer apply  
• Maintain least privilege through role changes  

## 🧩 Workflow:
1. HR updates user’s job title or department  
2. Dynamic group membership updates  
3. Role-based access automatically adjusts  
4. Old group memberships removed  
5. Access packages reassigned  
6. Manager notified of access changes  

## 🔍 Key Controls:
• Access removal validation  
• Audit log review  
• No lingering group memberships  

---

# 3. LEAVER PROCESS

## 🎯 Objectives:
• Disable identity quickly  
• Revoke all access immediately  
• Retain or transfer data depending on policy  

## 🧩 Workflow:
1. HR submits termination  
2. Account automatically disabled or blocked  
3. PIM roles removed  
4. Access packages revoked  
5. Licences removed  
6. Mailbox converted to shared mailbox  
7. Data archived and transferred  
8. Manager confirmation  

## 🛡 Security Controls:
• Immediate MFA revocation  
• Sign-in block  
• Token revocation  
• Removal from all groups  

---

# 4. GOVERNANCE & COMPLIANCE

## 📌 Mandatory Controls:
• Quarterly access recertification  
• Audit logs for joiners, movers and leavers  
• Orphaned accounts report  
• Service accounts review  
• Privileged role monitoring  

---

# 5. DOCUMENTATION

This framework should be paired with:

• Access Packages documentation  
• PIM governance policy  
• Dynamic group rules  
• HR to IT integration workflow  
• Conditional Access baseline policies  

---

# ✔ Summary

This JML lifecycle provides full identity governance for Microsoft Entra ID and ensures secure, compliant and consistent handling of every identity event.

