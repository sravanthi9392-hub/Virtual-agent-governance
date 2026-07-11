# Virtual Agent–Driven SLA Breach Awareness & Justification System

A zero-code, admin-level governance and compliance solution built natively on the **ServiceNow** platform. It transforms SLA management from a passive countdown into an active accountability loop — combining automated tracking, real-time conversational AI (Virtual Agent), UI enforcement policies, and role-based access controls to guarantee a permanent, audit-ready compliance trail for high-risk service delays.

## Overview

| | |
|---|---|
| **Platform** | ServiceNow (ITSM Architecture) |
| **Trigger Threshold** | Incident Resolution SLA reaches 80% elapsed time |
| **Target Persona** | ITIL Service Desk Agents / Assigned Support Engineers |
| **Type** | Zero-code (Flow Designer, Virtual Agent, UI Policies, ACLs) |

## The Problem

ITIL agents lack proactive tracking and automated warnings when incident SLAs near an 80% breach threshold, resulting in unlogged delays, missing audit readiness, and unsecure historical justification entries.

## Core Features (5 Pillars)

1. **SLA Monitoring & Backend Status Updates**
   Background engine tracks `task_sla` percentages. At 80%+, it flags the parent Incident as **SLA At Risk** via a custom checkbox (`u_sla_at_risk`).

2. **Flow Designer Automation & Proactive Alerts**
   Automated workflow detects threshold changes, emails the assignee, and includes a direct link into the portal chat.

3. **Conversational Layer (Virtual Agent Designer)**
   Guided chatbot topic identifies at-risk tickets, walks the agent through risk acknowledgement, captures structured breach categories, and appends the transcript to the record's Work Notes.

4. **UI Governance Enforcement (UI Policies)**
   When `SLA At Risk = True`, dynamic form policies make **SLA Breach Reason** (choice list) and **SLA Breach Justification** (journal) Visible and Mandatory.

5. **Data Security & Role-Based Integrity (ACLs)**
   ACL condition scripts (`current.assigned_to == gs.getUserID()`) restrict Write access to the active assignee; all others get Read-Only.

6. **Analytics & Accountability Dashboards**
   Aggregated dashboards track justification compliance rates and common bottlenecks (e.g., Waiting on Vendor, Technical Complexity).

## Tech Stack

- ServiceNow Flow Designer
- Virtual Agent Designer
- UI Policies
- Access Control Lists (ACLs)
- Performance Analytics / Dashboards

## Project Documentation

Phase-wise documentation (Ideation, Design, Development, Testing, Deployment, etc.) is maintained in `/docs`, following the project's standard phase template — each sub-phase documented as its own file.

## Status

✅ Implemented as part of ServiceNow System Administartor Internship from SmartBridge
