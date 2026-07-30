# Healthcare IT Service Desk Simulation

Built on a ServiceNow Personal Developer Instance for the same fictional healthcare organization used in the companion IAM project, Wasatch Family Health Clinic.

## Overview

This project simulates a Healthcare IT service desk end to end: designing the support structure, standing it up in a live ServiceNow instance, and working a realistic ticket queue through intake, triage, resolution, and knowledge capture.

## What Was Built

Five assignment groups modeling a tiered healthcare IT support structure: Service Desk (Tier 1), Clinical Applications Support (Tier 2), Network & Infrastructure, IAM & Account Support, and Desktop & Hardware Support.

Twelve incident tickets spanning the full priority range (Critical through Low), categorized across Software, Hardware, Network, and Inquiry/Help, and worked through New, In Progress, Resolved, and Closed states with realistic resolution notes.

SLA targets mapped to ServiceNow's built-in Priority-based SLA Definitions, covering response and resolution windows for all four priority tiers.

Six knowledge base articles covering the most common ticket types (password resets, printer troubleshooting, VPN setup, badge reader issues, elevated access requests, and EHR downtime procedures), each written to deflect Tier 1 volume and support self-service.

## Design Approach

Ticket categorization and assignment group routing follow how a real healthcare IT service desk is structured: Tier 1 handles high-volume, low-complexity issues (password resets, account lockouts); specialized groups own domain-specific issues (clinical software, network, hardware, identity). Priority is driven by Impact x Urgency, matching ServiceNow's out-of-the-box calculation, rather than being set manually per ticket. Two tickets in this project (account lockout and MFA push failure) directly reference the group structure and sign-in policy built in the companion Okta IAM project, so the two projects tell one consistent story rather than existing in isolation.

## Tools and Skills Demonstrated

ServiceNow administration (Incident Management, Assignment Groups, Knowledge Management, SLA Definitions), ITIL-aligned incident lifecycle management, priority/impact/urgency triage, knowledge base authoring for self-service deflection, and healthcare IT support operations.

## Repo Contents

- `ticket-log.md` — full log of all 12 incidents with resolution summaries
- `sla-matrix.md` — the Priority/Impact/Urgency SLA framework used to triage tickets
- `knowledge-base-summary.md` — summary of the six published knowledge base articles

## About

Built by Shaquille Jackson as part of a self-directed transition from healthcare operations into Healthcare IT and IAM. Portfolio: https://shaquillejackson.com
