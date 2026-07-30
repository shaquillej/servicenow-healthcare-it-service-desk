# SLA Matrix — Wasatch Family Health Clinic Service Desk

This project uses ServiceNow's out-of-the-box Priority-based SLA Definitions (`Incident` table) rather than rebuilding them from scratch, matching how most live ServiceNow implementations operate: admins typically tune the built-in SLA framework instead of reinventing it. All 12 tickets in this project were categorized and prioritized against this matrix.

| Priority | Response Target | Resolution Target | Example Ticket Type |
|---|---|---|---|
| 1 - Critical | 15 minutes | 1 hour | EHR down clinic-wide, network outage affecting patient care |
| 2 - High | 1 hour | 8 hours | Satellite clinic outage, e-Prescribing failure, MFA/sign-in blocking clinical work |
| 3 - Moderate | 4 hours | 1 day | Single-user hardware/software issue, non-blocking access request |
| 4 - Low | 8 hours | 2 days | New-hire provisioning ahead of a future start date, minor inquiry |

## How Priority Is Determined

ServiceNow calculates Priority automatically from the combination of Impact (how many people/systems are affected) and Urgency (how time-sensitive the issue is). This project used the following combinations to land tickets in the intended priority tier:

| Impact | Urgency | Resulting Priority |
|---|---|---|
| 1 - High | 1 - High | 1 - Critical |
| 2 - Medium | 1 - High | 2 - High |
| 1 - High or 2 - Medium | 2 - Medium | 3 - Moderate |
| 3 - Low | 3 - Low | 4 - Low |

## SLA Ownership by Assignment Group

| Assignment Group | Typical Priority Range Handled |
|---|---|
| Service Desk (Tier 1) | 3 - Moderate, 4 - Low (password resets, account lockouts) |
| Clinical Applications Support (Tier 2) | 1 - Critical, 2 - High, 3 - Moderate (EHR, e-Prescribing) |
| Network & Infrastructure | 2 - High, 3 - Moderate (VPN, WiFi, connectivity) |
| Desktop & Hardware Support | 3 - Moderate (printers, badge readers, workstations) |
| IAM & Account Support | 2 - High, 4 - Low (access provisioning, MFA, elevated access requests) |
