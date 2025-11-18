# Service Account Governance Framework  
A governance model for managing non human identities and service accounts in Microsoft Entra ID and related systems.

---

## 1. Purpose

This framework defines how service accounts are created, managed, used and monitored.

It aims to

• Protect critical infrastructure and applications  
• Enforce least privilege access for non human identities  
• Reduce misuse or abuse of unattended accounts  
• Provide full auditing and accountability  
• Support compliance and security best practice  

---

## 2. Scope

This governance applies to

• Service accounts in Microsoft Entra ID  
• On premises service accounts synchronised into Entra ID  
• Managed identities in Azure  
• Application registration identities and service principals  
• Accounts used by scripts, automation and integration tools  

---

## 3. Service Account Definitions

• Service account  
  An account used by applications, scripts or services rather than a human user.  

• Managed identity  
  A special identity in Azure created and managed by the platform for an application or service.  

• Service principal  
  Identity created for application registrations or enterprise applications in Entra ID.  

---

## 4. Service Account Categories

Service accounts should be classified into clear categories

• Application service account  
  Used by an app or API to access resources.  

• Integration service account  
  Used for data transfer or system integration between platforms.  

• Automation service account  
  Used by scripts, scheduled tasks or orchestration tools.  

• Infrastructure service account  
  Used by infrastructure services such as backup, monitoring or deployment tools.  

For each category, define

• Typical permissions  
• Allowed authentication methods  
• Required monitoring level  

---

## 5. Ownership and Accountability

Every service account must have

• A named technical owner  
• A business owner  
• A documented purpose  
• A defined system or application it supports  

Ownership requirements

• Owner must be an internal staff member  
• Owner is responsible for justification, review and removal  
• Changes to the account must be linked to a ticket or change request  

No service account is allowed to exist without a clearly recorded owner.

---

## 6. Creation and Approval Process

Creation steps

1. Request raised through IT service management tool  
2. Justification documented  
3. Account category chosen  
4. Required permissions documented  
5. Security review for least privilege  
6. Manager and security approval  

After approval

• Service account is created in Entra ID or Azure  
• Assigned only the required roles or group memberships  
• Documented in a central register  

---

## 7. Authentication and Secrets

Preferred methods

• Managed identities in Azure wherever possible  
• Certificates for application authentication  
• Secret values stored in secure vaults only  

Rules

• No shared human credentials used as service accounts  
• No interactive sign in for service accounts  
• No use of basic authentication where modern auth is available  
• All secrets must be rotated regularly and recorded  

Secrets storage

• Azure Key Vault or equivalent enterprise grade vault  
• Access to vault controlled with least privilege  
• Access logs must be enabled  

---

## 8. Permissions and Least Privilege

Principles

• Grant only the minimal role or permission needed  
• Use role based access control features  
• Avoid global administrator permission for any service account  
• Avoid broad directory wide permissions where a narrower scope is possible  

Checks

• Review app and service permissions before granting  
• Use built in least privilege roles where possible  
• Map every permission to a specific business need  

---

## 9. Lifecycle and Expiry

Every service account must have

• A creation date  
• A review date  
• An expiry or recertification date  

Lifecycle stages

• Creation  
• Active and monitored  
• Periodic review  
• Decommission and clean up  

Decommission process

1. Confirm the service is no longer required  
2. Disable the account  
3. Remove roles and group memberships  
4. Rotate or delete secrets  
5. Archive logs and configuration details  

---

## 10. Monitoring and Logging

All service accounts must be monitored for

• Interactive sign in attempts  
• Sign in from unexpected locations or devices  
• Unusual behaviour or high risk events  
• Use outside of documented hours if relevant  

Logs to enable

• Entra ID sign in logs  
• Entra ID audit logs  
• Application logs where available  
• SIEM integration for alerting  

Suspicious activity must trigger

• Alert to security or IAM team  
• Investigation using logs  
• Temporary disabling of access if necessary  

---

## 11. Periodic Reviews

Service accounts must be reviewed at regular intervals

Review includes

• Does the account still support an active service  
• Do the current permissions still match the requirement  
• Has the owner changed role or left the company  
• Are secrets and certificates within rotation policy  
• Is the account showing unexpected behaviour in logs  

Outcomes

• Keep and document  
• Reduce permissions  
• Migrate to managed identity  
• Decommission  

---

## 12. Policy Violations

Examples of violations

• Service account with no recorded owner  
• Service account with global administrator role  
• Service account using interactive sign in by human users  
• Secrets stored in plain text or unapproved locations  
• No activity for a long period with no explanation  

Actions

• Immediate investigation  
• Potential disablement of the account  
• Reporting to security leadership  
• Corrective actions agreed and tracked  

---

## 13. Compliance and Standards

This governance framework supports

• Least privilege and zero standing privilege principles  
• ISO and SOC style controls for identity  
• Strong audit requirements for regulated environments  

---

## ✔ Summary

This Service Account Governance Framework ensures that non human identities are controlled, monitored, and secured with the same care as human identities, while respecting least privilege and reducing the risk of misuse or compromise.
