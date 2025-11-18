# Entitlement Management – Access Package Template  
A structured template for documenting and governing Access Packages in Microsoft Entra ID.

---

# 1. Access Package Overview

**Access Package Name:**  
Example: Finance Team Access Package

**Catalog:**  
• Business Applications  
• Collaboration Access  
• Admin Access  
• HR and Finance  

**Description:**  
Provide a clear description of the purpose of this access package.  
Example: Grants finance team members access to the Finance Teams site, required SaaS applications and department groups.

**Owner(s):**  
List application or department owners responsible for approvals and governance.

---

# 2. Purpose and Business Justification

Explain why this access package exists.

### Examples:
• Centralise access required for a specific job role  
• Automate identity provisioning  
• Reduce manual access requests  
• Improve least privilege and compliance  
• Provide time-bound access for guests  
• Standardise department access  

---

# 3. Resources Included in the Package

## Groups
List all groups included.  
Specify type (security, Microsoft 365 group, dynamic).

Example:
| Group Name | Type | Purpose |
|------------|-------|----------|
| Finance-Staff | Security Group | Core department permissions |
| Finance-App-Users | Security Group | App access |

## Applications
Example:
| Application | Access Level | Notes |
|--------------|--------------|--------|
| Dynamics 365 Finance | User | Finance transactions |
| Power BI | Viewer | Financial dashboards |

## SharePoint / Teams
Example:
| Resource | Access Level |
|----------|---------------|
| Finance Team Site | Member |
| Finance Team Chat | Member |

## Roles (Optional)
Example:
| Role | Scope | Purpose |
|------|---------|---------|
| Reader | Finance Resource Group | View only |

---

# 4. Policies

Access packages rely on **policies** to define how users request access and how long it lasts.

## Policy Name:
Example: Internal Employee Access Policy

---

## Policy Settings:

### 1. **Who can request this access?**
Choose one or more:
• Specific users  
• All users in directory  
• Members of a department  
• Guest users  
• External partner users  

### 2. **Request Access Method**
• Requires approval  
• No approval required  
• Requires justification  
• Requires ticket number  

### 3. **Approval Workflow**
List approvers:

| Stage | Approver | Notes |
|-------|----------|--------|
| Stage 1 | Department Manager | Business validation |
| Stage 2 | App Owner | Technical validation |

### 4. **Assignment Duration**
• Time-bound (e.g. 90 days)  
• Permanent  
• Requires renewal  
• Requires re-approval  

### 5. **Access Expiration Settings**
• Automatically remove user  
• Notify user before removal  
• Manager must reapprove  

---

# 5. Lifecycle Controls & Governance

Explain how access is reviewed and controlled over time.

### ⭐ Mandatory Governance Controls:
• Quarterly access reviews  
• Owner attestation  
• Automatic access expiration  
• Guest access restricted to a time-limited duration  
• Business justification always required  
• Risk-based access removal (optional)  

### ⭐ Additional Security Controls:
• Block guest requests without sponsor  
• Apply Conditional Access to resources  
• Monitor activity logs for unusual access  
• Enforce time-bound admin access (if admin resources included)  

---

# 6. Provisioning & Deprovisioning Logic

### Provisioning Steps:
1. User requests access  
2. Approval workflow runs  
3. User assigned to resource groups  
4. Apps provision access  
5. Access logs updated  
6. User notified  

### Deprovisioning Steps:
1. Assignment expires or is denied  
2. User removed from groups  
3. App access revoked  
4. Licences removed (if tied)  
5. Activity logged  
6. Reviewer notified  

---

# 7. Access Review Requirements

Specify how access to this package will be checked over time.

### Review Frequency:
• Monthly  
• Quarterly  
• Semi-annually  

### Reviewer Type:
• Manager  
• Access Package Owner  
• Application Owner  

### Criteria:
• Role relevance  
• Last sign-in  
• Project involvement  
• Guest justification  

---

# 8. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|---------|-------------|
| Guest over-permission | Data leakage | Time-bound access + reviews |
| Incorrect approvals | Privilege creep | Multi-stage approval |
| Orphaned access | Compliance issue | Expiration policies |
| Admin access misuse | Security risk | PIM + logs |

---

# 9. Change Management

Define how changes to this access package are managed.

### Changes require:
• Request via ITSM ticket  
• Approval from owner  
• Documentation update  
• Testing (if app or group changes)  

### Examples of changes:
• Adding a new resource  
• Updating approval workflows  
• Changing duration settings  
• Removing a deprecated resource  

---

# 10. Attachments & Evidence

Attach or reference:
• Resource documentation  
• App owner lists  
• Group membership exports  
• Access logs  
• Review summaries  
• Workflow diagrams  

---

# ✔ Summary

This Access Package Template standardises how enterprise access is bundled, governed and assigned using Microsoft Entra ID.  

It improves security, compliance, and operational efficiency by ensuring requests, approvals, and lifecycle management follow structured governance controls.

