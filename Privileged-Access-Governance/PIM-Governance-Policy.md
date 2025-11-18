# Privileged Identity Management (PIM) Governance Policy  
A complete framework for managing, controlling and auditing privileged access in Microsoft Entra ID.

---

# 1. Purpose

This policy defines how privileged roles are assigned, activated, monitored and governed in Microsoft Entra ID.  
It ensures:

• Least privilege  
• Controlled admin access  
• Separation of duties  
• Auditable and compliant processes  
• Protection against misuse of admin roles  

This policy applies to all privileged roles, including Global Administrator, Privileged Role Administrator and custom roles.

---

# 2. Scope

This governance policy covers:

• Eligible and active administrator roles  
• PIM access management  
• Activation requirements  
• Approval workflows  
• Notifications  
• Monitoring and reporting  
• Recertification  
• Removal of privileges  

It applies to internal staff, contractors, and third-party administrators.

---

# 3. Privileged Role Principles

All privileged access must follow these principles:

### 1. Least Privilege  
Users should receive the minimum level of access required for their job.

### 2. Just-in-Time Access  
Admin roles should be eligible, not permanently active.

### 3. Approval-Based Elevation  
Sensitive roles must require approval from a security or department owner.

### 4. Full Auditing  
All activations, escalations, and privileged tasks must be logged.

### 5. Zero Standing Privilege (ZSP)  
Permanent admin access should be eliminated unless justified.

---

# 4. Role Assignment Rules

### Role Assignment Types  
Roles must be assigned as:

• **Eligible** (preferred)  
• **Active** (only with written business justification)  

### Permanent Active Roles Allowed For:  
• Break glass accounts  
• Service accounts (with strict controls)  
• Specific automation requirements  

### Not Allowed:  
• Permanent Global Administrator  
• Permanent Privileged Role Administrator  
• Permanent Cloud Application Administrator  
• Permanent SharePoint Administrator  

---

# 5. Role Activation Requirements

### Activation Conditions  
PIM role activation requires:

• MFA  
• Justification  
• Ticket or change request reference  
• Approval (for sensitive roles)  
• Conditional Access compliance  
• Device compliance (if enforced)  

### Sensitive Roles (Require Approval):  
• Global Administrator  
• Privileged Role Administrator  
• User Administrator  
• Exchange Administrator  
• Security Administrator  

### Low-Risk Roles (No Approval Required):  
• Reports Reader  
• Helpdesk Administrator  
• Groups Administrator  

---

# 6. Activation Settings

### Required settings for all PIM roles:

| Setting | Requirement |
|---------|-------------|
| Maximum activation duration | 1–4 hours |
| Require MFA | Yes |
| Require justification | Yes |
| Require ticket ID | Recommended |
| Require approval | For sensitive roles |
| Send activation notifications | To approvers & auditors |
| Assignment review frequency | Quarterly |

---

# 7. Monitoring & Alerts

### PIM must have alerts enabled for:

• Permanent role assignment added  
• Role assigned to a risky user  
• Activation outside business hours  
• High-risk sign-in during activation  
• Failed activation attempts  
• Multiple activations in short period  

### Logging  
All PIM activities must be logged in:

• Azure AD Audit Logs  
• Azure AD Sign-in Logs  
• Microsoft Defender for Cloud Apps (optional)  
• SIEM (Sentinel recommended)

---

# 8. Privileged Access Reviews

Quarterly access reviews must be performed for:

• Eligible role assignments  
• Active role assignments  
• Break glass accounts  
• Service accounts with privileges  

Reviews must check:

• Role necessity  
• Recent role activity  
• User employment status  
• Risk detections  
• Inactivity or misuse  

All decisions must be logged.

---

# 9. Break Glass Account Policy

Break glass accounts must:

• Be cloud-only  
• Have long, randomly generated passwords  
• Be excluded from Conditional Access  
• Be protected in a secure password vault  
• Have regular access reviews  
• Have monitored sign-ins  

Only two break glass accounts are allowed.

---

# 10. Removal of Privileges

Admin privileges must be removed when:

• User changes role  
• User leaves the company  
• User has not activated role in 90+ days  
• User fails access review  
• Security risk detected  

Removal actions must be logged and reported.

---

# 11. Service Account Governance

Privileged service accounts must:

• Use certificate-based authentication  
• Never use interactive login  
• Be assigned least privilege RBAC roles  
• Have documented owners  
• Have rotation schedules  
• Be reviewed quarterly  

---

# 12. Compliance & Auditing

This PIM governance policy supports:

• ISO 27001  
• SOC 1 / SOC 2  
• NIST 800-53  
• Cyber Essentials Plus  
• Microsoft Zero Trust architecture  

All audit evidence must be archived for compliance.

---

# ✔ Summary

This PIM Governance Policy provides strong controls for managing privileged access using Microsoft Entra ID and ensures adherence to least privilege, zero standing privilege and security best practices.

It supports secure and compliant operations across enterprise environments.

