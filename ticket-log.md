# Ticket Log — Wasatch Family Health Clinic Service Desk

Simulated in a ServiceNow Personal Developer Instance (PDI). All tickets below were created, categorized, prioritized, assigned, and worked through to resolution or an active state exactly as they would be in a live service desk queue.

| Number | Opened | Caller | Category | Priority | Assignment Group | State | Short Description |
|---|---|---|---|---|---|---|---|
| INC0010001 | 2026-07-29 | Abel Tuter | Software | 1 - Critical | Clinical Applications Support (Tier 2) | Resolved | EHR unavailable clinic-wide - providers unable to access patient charts |
| INC0010002 | 2026-07-29 | Abraham Lincoln | Software | 3 - Moderate | Clinical Applications Support (Tier 2) | In Progress | Provider unable to complete order entry in EHR - errors on submit |
| INC0010003 | 2026-07-29 | Adela Cervantsz | Inquiry / Help | 4 - Low | Service Desk (Tier 1) | Closed | Password reset needed - locked out of workstation login |
| INC0010004 | 2026-07-29 | Aileen Mottern | Inquiry / Help | 3 - Moderate | Service Desk (Tier 1) | Resolved | Account locked out after repeated failed login attempts |
| INC0010005 | 2026-07-29 | Alejandra Prenatt | Inquiry / Help | 4 - Low | IAM & Account Support | In Progress | New hire needs elevated EHR access provisioned before start date |
| INC0010006 | 2026-07-29 | Alejandro Mascall | Hardware | 3 - Moderate | Desktop & Hardware Support | New | Printer offline in Exam Room 3 - unable to print visit summaries |
| INC0010007 | 2026-07-29 | Alene Rabeck | Network | 3 - Moderate | Network & Infrastructure | Resolved | VPN not connecting for remote billing staff |
| INC0010008 | 2026-07-29 | Alfonso Griglen | Network | 2 - High | Network & Infrastructure | Closed | Satellite clinic WiFi outage - all staff at South Valley location offline |
| INC0010009 | 2026-07-29 | Allie Pumphrey | Hardware | 3 - Moderate | Desktop & Hardware Support | New | Badge reader malfunctioning at front desk - staff unable to clock in |
| INC0010010 | 2026-07-29 | Allyson Gillispie | Software | 2 - High | Clinical Applications Support (Tier 2) | In Progress | e-Prescribing errors for physician - prescriptions failing to transmit to pharmacy |
| INC0010011 | 2026-07-29 | Alva Pennigton | Hardware | 3 - Moderate | Desktop & Hardware Support | Resolved | Mobile COW (computer on wheels) won't boot on nursing floor |
| INC0010012 | 2026-07-29 | Alyssa Biasotti | Inquiry / Help | 2 - High | IAM & Account Support | Resolved | MFA push notification not working for physician logging into Okta |

## Resolution Summaries (Resolved / Closed tickets)

**INC0010001 - EHR unavailable clinic-wide (P1-Critical)**
Root cause traced to an EHR application server issue. Escalated to Clinical Applications Support (Tier 2) for immediate response per the P1 SLA. Downtime procedures were communicated to clinical staff while the issue was resolved. Service restored and confirmed with affected providers before closing.

**INC0010003 - Password reset needed**
Verified caller identity, reset the workstation login password through self-service reset flow (see the "How to Reset Your EHR Password" knowledge article), and confirmed the caller could log in successfully.

**INC0010004 - Account locked out after repeated failed login attempts**
Confirmed the lockout was caused by mistyped credentials, not a security event. Unlocked the account in Okta, reset the password, and advised the caller on password manager use to avoid repeat lockouts.

**INC0010007 - VPN not connecting for remote billing staff**
Walked the caller through the VPN troubleshooting steps in the knowledge base (client restart, workstation restart). Connection restored; confirmed EHR access from the remote location before closing.

**INC0010008 - Satellite clinic WiFi outage**
Network & Infrastructure identified a failed access point at the South Valley location. Replaced the hardware and confirmed connectivity was restored for all affected staff before closing the ticket.

**INC0010011 - Mobile COW won't boot**
Desktop & Hardware Support found a failed battery/power issue on the mobile workstation. Swapped in a spare unit for immediate use and scheduled the original for hardware repair.

**INC0010012 - MFA push notification not working**
Confirmed with the physician that Okta Verify notifications were disabled on their device after a recent phone update. Walked through re-enabling push notifications and verified successful MFA login. This ticket cross-references the tiered sign-in policy and EHR-Elevated group built in the companion IAM/RBAC project.
