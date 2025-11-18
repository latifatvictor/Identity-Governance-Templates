# Access Review Template  
A standardised template for planning, documenting and executing access reviews across Microsoft Entra ID Governance.

---

# 1. Review Overview

**Review Name:**  
Example: Quarterly Admin Role Access Review

**Review Type:**  
• User-to-Group  
• Role Assignment  
• Application Assignment  
• Guest User Access  
• Access Package Assignment  

**Review Owner:**  
• Name of IT Security Manager or IAM Lead  

**Review Frequency:**  
• Monthly  
• Quarterly  
• Bi-annually  
• Annually  

**Review Scope:**  
Describe what is being reviewed. Examples:  
• All users assigned to Global Administrator  
• All members of the Finance group  
• All external users with access to SharePoint site  
• All users assigned to critical business apps  

---

# 2. Review Objectives

Clearly define why the review is required:

• Maintain least privilege  
• Remove unnecessary access  
• Validate role-based access  
• Clean up dormant accounts  
• Reduce access creep  
• Validate guests still require access  
• Improve security posture and compliance  
• Support ISO 27001 / SOC2 requirements  

---

# 3. Review Configuration (Microsoft Entra ID)

**Review Method:**  
• Self-attestation  
• Manager review  
• Sponsor review (for guests)  
• Application owner review  

**Scope Filters:**  
• Exclude inactive accounts  
• Exclude service accounts  
• Include only enabled users  
• Include guests only  

**Decision Options Available:**  
• Approve (Access Required)  
• Deny (Remove Access)  
• Take No Action  
• Reassign to Manager  

**Auto-Apply Recommendations:**  
• Enabled / Disabled  
• Criteria: Last sign-in, role activity, group activity  

**Actions on Completion:**  
• Automatically remove denied users  
• Require justification  
• Require multi-factor approval  
• Send completion report  

---

# 4. Reviewer Guidance

Provide instructions to reviewers:

### Reviewers must:
• Validate if the user still requires access  
• Check role relevance to current job title  
• Confirm that external users still collaborate  
• Remove any dormant or unneeded accounts  
• Provide justification for approvals  
• Flag suspicious or high-risk access  

### Reviewers should check:
• Recent sign-in logs  
• Role usage activity  
• Employment status  
• Job changes  
• Project completion  

### Important Notes:
• Access should not be approved automatically  
• Access must be removed if unused for 90+ days  
• Guests should be strictly validated  

---

# 5. Access Review Decision Log

| User | Access Being Reviewed | Reviewer | Decision | Justification | Date |
|------|-----------------------|----------|----------|---------------|------|
| Example User A | Global Administrator | IT Security Manager | Deny | User no longer in admin team | 12 Jan 2025 |
| Example User B | Finance Group | Department Manager | Approve | Required for daily finance tasks | 12 Jan 2025 |

---

# 6. Completion Results

After the review, document:

**Total users reviewed:**  
**Access removed:**  
**Access retained:**  
**Users with no response:**  
**Escalations raised:**  
**High-risk access discovered:**  

---

# 7. Post-Review Governance Actions

List the follow-up actions:

• Remove approved “deny” users  
• Re-assign access based on role changes  
• Update dynamic group rules  
• Audit PIM assignments  
• Log all removals  
• Inform managers of significant changes  
• Produce compliance evidence  
• Update access policies if required  

---

# 8. Attachments & Evidence

Attach or reference:

• Export of review results  
• Screenshots from Entra ID  
• Reviewer justification logs  
• Sign-in logs  
• PIM activity logs  
• Risk detections  

---

# ✔ Summary

This template ensures all access reviews are structured, compliant, repeatable and aligned with identity governance best practice.  
It can be reused for user access, role assignments, group memberships, privileged roles and application access reviews.
