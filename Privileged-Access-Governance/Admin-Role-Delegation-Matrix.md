# Admin Role Delegation Matrix  
A comprehensive matrix defining privileged roles, responsibilities, owners, approval flows and governance controls for secure administration in Microsoft Entra ID.

---

# 1. Purpose

The Admin Role Delegation Matrix provides a clear mapping of:

• Who can administer what  
• Which roles are allowed or restricted  
• What level of privilege each role permits  
• Who approves assignments  
• What governance controls apply  

This prevents privilege creep, enhances operational clarity and enforces least privilege across the organisation.

---

# 2. Role Categories

Roles are grouped into **six privilege tiers** to simplify governance.

| Tier | Name | Risk Level | Description |
|------|------|-------------|--------------|
| T0 | Global Administrators | Critical | Full authority across tenant, full impact risk |
| T1 | Security & Identity Admins | High | Identity, authentication, CA, PIM, MFA |
| T2 | Platform Admins | High | Exchange, SharePoint, Teams, Apps |
| T3 | IT Operations Admins | Medium | Helpdesk, Groups, User Management |
| T4 | Low-Risk Admin Roles | Low | Reporting, Read-only roles |
| T5 | Custom Admin Roles | Variable | Limited-scope or custom RBAC |

---

# 3. Admin Role Delegation Matrix

## Role Assignment Matrix

| Role | Tier | Allowed Assignees | Approval Required | Activation Type | Maximum Duration | Notes |
|------|------|-------------------|-------------------|------------------|------------------|--------|
| Global Administrator | T0 | Identity Architect, Senior IAM Lead | CISO / Security Director | Eligible via PIM | 1 hour | No permanent assignments except break glass |
| Privileged Role Administrator | T1 | IAM Team | Security Manager | Eligible | 2 hours | Cannot approve own requests |
| Security Administrator | T1 | Security Operations, IAM | Security Manager | Eligible | 8 hours | High-risk role; justification mandatory |
| Conditional Access Administrator | T1 | IAM / Security Engineers | IAM Lead | Eligible | 4 hours | Must have MFA + compliant device |
| Authentication Admin | T1 | IAM Team | IAM Lead | Eligible | 4 hours | MFA reset access; monitored |
| Exchange Administrator | T2 | Messaging Team | Messaging Manager | Eligible | 8 hours | Risky role; logs monitored |
| SharePoint Administrator | T2 | Collaboration Team | Collaboration Lead | Eligible | 8 hours | Must review SPO sharing risks |
| Teams Administrator | T2 | Collaboration Team | Collaboration Lead | Eligible | 8 hours | Lower risk, operational role |
| User Administrator | T3 | IT Support, Service Desk | Service Delivery Manager | Eligible or Active | 16 hours | Allowed active assignment for support |
| Groups Administrator | T3 | IT Support | None | Eligible | 8 hours | Group modification monitored |
| Helpdesk Administrator | T3 | Support Tier 1–2 | None | Active | Permanent | Limited-risk role |
| Reports Reader | T4 | Security Analysts, IT | None | Active | Permanent | Read-only role |
| Insights Administrator | T4 | IT Operations | None | Active | Permanent | Low risk |
| Custom RBAC Roles | T5 | Based on scope | Application Owner | Case-by-case | Case-by-case | Must follow least privilege |

---

# 4. Assignment Rules

### 1. No permanent assignments for T0 or T1 roles  
Only break-glass accounts may be permanently privileged.

### 2. All sensitive roles must be **eligible** via PIM  
Except support roles requiring continuous access (e.g. Helpdesk Admin).

### 3. Approval required for high-risk activations  
• Global Admin  
• Security Admin  
• Conditional Access Admin  
• Privileged Role Admin  

### 4. All assignments require justification  
Including:  
• Ticket number  
• Business justification  
• Time-bound duration  

---

# 5. Privileged Role Ownership

| Role | Owner | Responsibilities |
|------|--------|---------------------------|
| Global Admin | CISO / IAM Director | Oversees critical access, break-glass governance |
| PIM Admin | IAM Lead | Manages privileged access workflows |
| Security Admin | Security Manager | Oversees CA, identity protection, threat mitigation |
| Exchange/SharePoint Admin | Platform Leads | Oversees app-specific security boundaries |
| User & Groups Admin | Service Delivery Manager | Manages operational identity tasks |

---

# 6. Governance Controls

### Required Controls:

✔ Quarterly access reviews  
✔ Time-bound assignments  
✔ No standing privilege for admin roles  
✔ PIM activation alerts enabled  
✔ Justification + ticket required  
✔ Break-glass accounts tested monthly  
✔ Privileged activity logs sent to SIEM  
✔ Locked-down access to privileged portals  

---

# 7. Forbidden Assignments

The following are **not allowed**:

❌ Permanent Global Administrator  
❌ Permanent Privileged Role Administrator  
❌ MFA-bypass admin roles  
❌ Assigning admin roles to guest users  
❌ Assigning admin roles to personal devices  
❌ Admin roles without Conditional Access protection  
❌ Assigning roles without owner approval  

---

# 8. Role Escalation Workflow

### Step-by-step process:

1. User submits role request  
2. IAM team validates request and justification  
3. Owner approves or denies  
4. Assignment set to **Eligible**  
5. Activation requires MFA + justification  
6. PIM logs activation  
7. Approver notified (for sensitive roles)  
8. Role expires automatically after time limit  

---

# 9. Monitoring & Reporting

PIM must be configured to send reports to:

• Azure AD Audit Logs  
• Azure AD Sign-in Logs  
• Microsoft Defender for Cloud Apps  
• Security Information & Event Management (Sentinel)  

Reports to be reviewed weekly:

• Privileged activation attempts  
• Failed activations  
• Assignments outside policy  
• Risky user escalations  
• Permanent assignments flagged  

---

# ✔ Summary

This Admin Role Delegation Matrix provides a clear, structured and secure framework for managing privileged access in Microsoft Entra ID.  
It supports least privilege, eliminates excess admin access and provides strong governance controls aligned with enterprise best practices.


