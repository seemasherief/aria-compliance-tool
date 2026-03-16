# ARIA - **A**I **R**isk & Compliance **I**ntelligence **A**ssistant
### Built by Seema Sherief

A proactive compliance risk mitigation tool for e-commerce Customer Service AI systems.

🔗 **[View Live Tool](https://seemasherief.github.io/aria-compliance-tool)**

---

## Why ARIA?

**ARIA** stands for **A**I **R**isk & Compliance **I**ntelligence **A**ssistant.

The name was chosen deliberately:
- The acronym maps directly to what the tool does and anyone reading it understands the domain instantly
- It signals a proper product identity, not just a dashboard
- In music, an *aria* is a precise, expressive solo performance, technically demanding and purposeful. That felt right for a governance tool designed to surface clear signal from complex regulatory noise

---

## About This Project

ARIA helps AI Compliance Managers proactively monitor, assess and remediate compliance risks in customer service AI systems. It covers three major regulatory frameworks, **EU AI Act**, **GDPR** and **CCPA**, and translates complex legal obligations into an operational workflow that a non-lawyer can act on daily.

### The Problem This Tool Solves

E-commerce companies are rapidly deploying AI in customer service - chatbots, auto-routing, sentiment analysis, fraud detection. This deployment is outpacing compliance infrastructure. The result: significant regulatory exposure.

| Risk Area | Regulation | Real Exposure |
|---|---|---|
| AI chatbot doesn't identify itself | EU AI Act Art. 52 | Fines up to €15M |
| PII collected without lawful basis | GDPR Art. 6, 32 | Data breach liability |
| Automated decisions without human review | EU AI Act Art. 14 | Customer rights violated |
| Routing bias by language/demographic | EU AI Act Art. 10 | Discriminatory service access |
| Chat logs retained beyond policy | GDPR Art. 5(e) | Right to deletion violations |
| No audit trail for AI decisions | EU AI Act Art. 12 | Cannot respond to regulators |

Most CS teams lack a dedicated compliance monitoring layer for AI systems. ARIA provides the AI Compliance Manager with a single command centre to be proactive, cross-functional and audit-ready.

---

## Build Notes

| | |
|---|---|
| **Built by** | Seema Sherief |
| **Build date** | March 15–16, 2025 (overnight session) |
| **Build time** | Approximately 9 hours |
| **Tool used** | VS Code |
| **Technology** | HTML, CSS, vanilla JavaScript - single file, zero dependencies |

---

## The 4 CS AI Systems Being Monitored

**1. CS Chatbot v2.4 - 32% Compliant - CRITICAL**
The customer-facing conversational AI. Handles order enquiries, returns, refunds and complaints directly with customers. The most visible and most heavily regulated system because it interacts with customers at scale. Currently the worst performer with 8 open compliance issues.

**2. Auto-Routing Engine - 61% Compliant - HIGH**
An invisible system customers never see. Reads incoming messages and routes them to the right team. Such as, returns, billing, complaints or the chatbot. Makes routing decisions thousands of times per day. A 23% language bias issue lives here - it routes non-English speakers to the AI bot more often than English speakers, a potential discriminatory outcome under EU AI Act Art. 10.

**3. Sentiment Classifier - 79% Compliant - MEDIUM**
Reads every customer message in real time and scores the emotional tone. Frustrated, neutral, satisfied, angry. Uses that score to flag high-risk conversations for priority human handling. Two open issues around profiling of customer emotional states under GDPR Art. 22.

**4. Return Fraud Detector - 91% Compliant - LOW**
A machine learning model that analyses return requests and assigns a fraud probability score. The healthiest system at 91% compliant. The 1 remaining issue relates to documenting decision criteria so wrongly-flagged customers can challenge the decision, which is required under GDPR Art. 22 and EU AI Act Art. 14.

---

## The 6 Modules - Full Explanation

---

### 01 · Dashboard - Compliance Overview

**Purpose:** The briefing screen. Everything critical surfaced in one view so the AI Compliance Manager can prioritise their day in under 60 seconds.

#### The 4 KPI Cards

**Overall Risk Score - 72/100**

A composite weighted score across 6 risk categories. Amber because it is in the warning zone. Calculated as follows:

| Category | Weight | Score | Contribution |
|---|---|---|---|
| Data Privacy | 25% | 85 | 21.25 |
| AI Transparency | 20% | 74 | 14.80 |
| Human Oversight | 20% | 68 | 13.60 |
| Bias & Fairness | 15% | 61 | 9.15 |
| Accuracy | 12% | 45 | 5.40 |
| Logging & Audit | 8% | 78 | 6.24 |
| **Total** | **100%** | - | **≈ 72** |

Data Privacy carries the highest weight (25%) because GDPR fines are the largest financial risk - up to 4% of global annual turnover. Logging carries the least (8%) because while important, it does not directly harm customers.

**EU AI Act Readiness - 68%**

Calculated by scoring 8 specific EU AI Act articles as Passing (100%), In Progress (50%), or Failing (0%):

| Article | Status | Score |
|---|---|---|
| Art. 52 - Transparency to users | FAILING | 0% |
| Art. 14 - Human Oversight | FAILING | 0% |
| Art. 12 - Logging | IN PROGRESS | 50% |
| Art. 11 - Technical documentation | IN PROGRESS | 50% |
| Art. 9 - Risk Management | PASSING | 100% |
| Art. 13 - Transparency to deployers | PASSING | 100% |
| Art. 10 - Data governance | PASSING | 100% |
| Art. 15 - Accuracy testing | PASSING | 100% |

Average = (0+0+50+50+100+100+100+100) ÷ 8 = **62.5%**, weighted by article importance = **68%**

**Open Violations - 14**

The 14 violations are tiered by urgency:

| Severity | Count | Timeframe to Fix |
|---|---|---|
| Critical | 3 | Within 30 days |
| High | 6 | Within 90 days |
| Medium | 4 | Within 180 days |
| Low | 1 | Best effort |
| **Total** | **14** | |

**Interactions Scanned - 24,891 · 98.2% Coverage**

24,891 customer service conversations were analyzed in the last 30 days. 98.2% coverage means ARIA successfully scanned 98.2 out of every 100 conversations. The 1.8% gap represents channels not yet fully connected to the monitoring pipeline.

#### The 4 Live Compliance Alerts

**Alert 1 - AI agent not disclosing automated nature to customers**

The CS chatbot is having conversations without ever saying it is an AI. 847 customers today were misled into thinking they were talking to a human. EU AI Act Article 52(1) makes this illegal. Fines up to €15 million. The CS Bot v2.4 version number matters, when v2.5 ships with the fix, the violation stops and that improvement is traceable.

**Alert 2 - PII data retained beyond policy limit in chat logs**

Customer personal data - names, email addresses, order details - is being stored longer than the company's own 90-day retention policy. 12,400 records are currently at risk. GDPR Article 5(e) requires storage limitation. CCPA §1798.100 gives customers the right to know their data is not held indefinitely.

**Alert 3 - Escalation rate disparity across customer segments**

The Auto-Routing Engine sends English-speaking customers to human agents 23% more often than non-English speakers. Non-English customers are kept with the AI bot longer even when their issues are equally complex. EU AI Act Article 10 requires AI systems not to produce discriminatory outcomes. A 23% measurable gap based on language is a potential bias violation.

**Alert 4 - Missing human override documentation for AI decisions**

Three types of AI decisions have no written procedure for when and how a human agent should step in. EU AI Act Article 14 requires oversight mechanisms to exist AND be documented. Having an escalation button is not enough. There must be a written procedure that agents actively follow.

---

### 02 · AI Assessment

**Purpose:** A structured tool to run a formal compliance audit on any of the four CS AI systems. Turns complex regulatory requirements into an operational form any manager can complete.

#### The Assessment Form
- Select which AI system to audit
- Select the assessment type. Full Audit, EU AI Act Gap Analysis, GDPR Privacy Assessment, Bias Evaluation or Human Oversight Review
- Describe the system in plain English for context
- List any known risk areas already suspected
- Click Run Assessment. A scanning animation plays then a findings report appears

In a production environment, the description field would send context to an LLM API which would generate a real customised assessment. In this prototype the results demonstrate what that output would look like.

#### The 8 EU AI Act Articles in the Checklist

| Article | Requirement | Current Status |
|---|---|---|
| Art. 52(1) | Customers must be told they are talking to AI | FAILING |
| Art. 14 | Human override procedures must be documented | FAILING |
| Art. 9 | Ongoing risk management process must exist | PASSING |
| Art. 11 | Full technical documentation must be maintained | IN PROGRESS |
| Art. 12 | All AI decisions must be automatically logged | FAILING |
| Art. 10 | Training data must be unbiased and governed | PASSING |
| Art. 43 | Conformity assessment must be completed before deployment | IN PROGRESS |
| Art. 15 | System must be tested for accuracy and robustness | PASSING |

**Art. 52(1) - Transparency to End Users**

When a customer interacts with an AI the system must disclose this at the start of the interaction. Customers have the legal right to know they are not talking to a human.

**Art. 14 - Human Oversight**

AI systems must be designed so humans can monitor, intervene and override at any time. Not enough to say humans can take over, you must prove how and when with written documented procedures.

**Art. 9 - Risk Management System**

A continuous risk management process must exist before and after deployment. Not a one-time exercise. It is an ongoing obligation.

**Art. 11 - Technical Documentation**

A detailed written record of system design, training data, testing, performance metrics and known limitations. Must be maintained and updated when the system changes.

**Art. 12 - Logging and Record-Keeping**

The AI must automatically record its own decisions with timestamps. If a regulator asks why the AI refused a refund on a specific date, the log must answer that question.

**Art. 10 - Data Governance**

Training and operational data must be relevant, accurate, complete and free from bias. The 23% language routing gap is a direct Art. 10 violation.

**Art. 43 - Conformity Assessment**

A formal review confirming the system meets all EU AI Act requirements before deployment.

**Art. 15 - Accuracy, Robustness and Cybersecurity**

System must perform accurately across normal use and edge cases. Must be tested against errors, unexpected inputs and attempted manipulation.

#### The Assessment Report

After clicking Run Assessment, the report surfaces:

| Finding | Regulation | Impact | Severity |
|---|---|---|---|
| AI identity not disclosed to customers | EU AI Act Art. 52(1) | Fines up to €15M | CRITICAL |
| No human escalation pathway | EU AI Act Art. 14 | Mandatory regulatory review | CRITICAL |
| PII in unencrypted chat logs | GDPR Art. 32 | Data breach liability | CRITICAL |
| English customers escalated 23% more | EU AI Act Art. 10 | Discriminatory outcomes | HIGH |
| No automated logging of AI decisions | EU AI Act Art. 12 | Auditability gap | HIGH |

---

### 03 · Interaction Analyzer

**Purpose:** Catches violations at the ground level, inside individual customer conversations. While the Dashboard shows systemic trends, this tab shows exactly what is going wrong in specific interactions in real time.

#### Sample Conversation - Case #CS-48291

Six messages with compliance flags appearing inline inside the conversation bubbles, showing the exact moment each violation occurs:

| Message | Speaker | Compliance Flag |
|---|---|---|
| "Hi, I need help with my order..." | Customer | - |
| "Hi! I'm here to help. Can you provide your email?" | AI Agent | No AI disclosure |
| "It's #ORD-992847. My email is sarah.jones@..." | Customer | - |
| "I'm processing a full refund now." | AI Agent | PII collected · Auto-decision |
| "Actually I'd prefer a replacement..." | Customer | - |
| "Refunds are the only option for orders over 14 days." | AI Agent | No escalation offered |

**Interaction Risk Score - 88/100**
2 Critical violations + 2 High violations + 1 Compliant item = 88/100 risk score. The one compliant item: the AI correctly identified the order issue and provided accurate information.

#### Bulk Scan Summary - Last 7 Days

| Flag Type | Count | Trend |
|---|---|---|
| No AI disclosure | 847 | +12% - worsening |
| PII without consent | 392 | +4% - worsening |
| Auto-decision no review | 219 | -8% - improving |
| No escalation offered | 541 | +2% - slightly worsening |

The downward trend on auto-decisions shows remediation work is beginning to have measurable impact.

---

### 04 · Regulatory Map

**Purpose:** A complete reference map showing which laws apply, which articles matter for CS AI and current compliance status. Solves the problem of overlapping obligations across multiple frameworks, one operational problem can violate multiple regulations simultaneously.

#### EU AI Act
Applies to customer-facing AI systems. Transparency obligations are mandatory regardless of risk tier. Key failing articles: Art. 52 (transparency) and Art. 14 (human oversight).

#### GDPR
Applies to all EU customer personal data. Chat logs, email addresses and behavioural data all constitute personal data under Art. 4. Key failing articles: Art. 6 (no lawful basis for PII collection) and Art. 32 (unencrypted logs).

#### CCPA / CPRA
Applies to California residents regardless of company location if thresholds are met. Key obligations: right to know, right to delete, right to opt out of data sharing.

#### Cross-Regulation Impact Matrix

| CS AI Risk Area | EU AI Act | GDPR | CCPA | Internal Policy | Status |
|---|---|---|---|---|---|
| AI identity disclosure | Art. 52 | - | - | P-CS-01 | FAILING |
| PII collection in chat | Art. 10 | Art. 6, 32 | §1798.100 | P-PRIV-03 | FAILING |
| Automated decisions | Art. 14 | Art. 22 | - | P-CS-07 | PARTIAL |
| Sentiment / profiling | Art. 10 | Art. 22 | §1798.140 | P-PRIV-05 | REVIEW |
| Data retention in logs | - | Art. 5(e) | §1798.105 | P-DATA-02 | NON-COMPLIANT |
| Bias in routing logic | Art. 10 | - | - | P-CS-12 | INVESTIGATING |

---

### 05 · Doc Generator

**Purpose:** Produces the actual regulatory documents CS AI systems are legally required to have. Accelerates what normally takes weeks into hours.

#### The 7 Document Types

| Document | Regulation | Purpose |
|---|---|---|
| EU AI Act Technical Documentation | Art. 11 | Formal record of system design, training data, and performance |
| GDPR Data Protection Impact Assessment (DPIA) | Art. 35 | Identifies privacy risks and mitigation measures |
| AI Transparency Notice | Art. 52 | Customer-facing statement confirming AI interaction |
| Human Oversight Procedure Manual | Art. 14 | Written procedures agents follow to review or override AI |
| Bias Audit Report | Art. 10 | Documents fairness testing results across customer groups |
| Incident Response Playbook | GDPR Art. 33 | Step-by-step breach response - 72-hour notification requirement |
| Conformity Self-Assessment | Art. 43 | Pre-deployment certificate of regulatory compliance |

#### Document Library Status

| Document | Status |
|---|---|
| AI Transparency Notice v2 | DRAFT |
| DPIA - CS Chatbot v2.4 | APPROVED |
| Human Oversight Manual v1 | MISSING - critical gap |
| Bias Audit Report Q1-2025 | IN REVIEW |
| Incident Response Playbook v3 | APPROVED |

---

### 06 · Remediation & Action Plan

**Purpose:** The execution layer. Turns compliance gaps into managed work items with owners, deadlines and progress visibility. The AI Ops Manager can run a weekly standup directly from this screen.

#### Summary

| Priority | Count | Timeframe |
|---|---|---|
| Critical - Act Now | 3 | 30 days |
| High Priority | 6 | 90 days |
| Medium Priority | 4 | 180 days |
| Resolved This Month | 7 | - |

#### Active Remediation Items

| ID | Issue | Owner | Deadline | Progress | Status |
|---|---|---|---|---|---|
| REM-001 | Add AI disclosure at chat start | Tech Lead | Apr 15 | 65% | IN PROGRESS |
| REM-002 | Encrypt PII in chat logs | Data Eng | Apr 22 | 20% | BEHIND |
| REM-003 | Document human override procedures | AI Ops Mgr | May 1 | 40% | IN PROGRESS |
| REM-004 | Implement 90-day log retention | Data Eng | May 15 | 80% | NEAR DONE |
| REM-005 | Fix multilingual routing bias | ML Team | Jun 1 | 10% | JUST STARTED |
| REM-006 | Enable automated event logging | Tech Lead | Jun 15 | 55% | IN PROGRESS |

> **Watch item:** REM-002 is most critical - PII encryption is only 20% complete with an imminent deadline.

---

## Regulations Covered

### EU AI Act (2024 - In Force)
| Article | Requirement |
|---|---|
| Art. 9 | Risk Management |
| Art. 10 | Data Governance & Bias |
| Art. 11 | Technical Documentation |
| Art. 12 | Logging & Record-Keeping |
| Art. 13 | Transparency to Deployers |
| Art. 14 | Human Oversight |
| Art. 15 | Accuracy & Robustness |
| Art. 43 | Conformity Assessment |
| Art. 52 | Transparency to Users |

### GDPR (EU 2016/679)
| Article | Requirement |
|---|---|
| Art. 5 | Data minimisation and storage limitation |
| Art. 6 | Lawful basis for processing |
| Art. 22 | Automated decision-making rights |
| Art. 30 | Records of processing activities |
| Art. 32 | Security of processing |
| Art. 33 | Breach notification within 72 hours |
| Art. 35 | Data Protection Impact Assessment |

### CCPA / CPRA (California)
| Section | Requirement |
|---|---|
| §1798.100 | Right to know what data is collected |
| §1798.105 | Right to delete personal information |
| §1798.120 | Right to opt-out of data sharing |
| §1798.140 | Sensitive personal information definition |
| §1798.150 | Security and breach liability |

---

## Technology

```
Single-file HTML application
├── HTML        — Structure and content
├── CSS         — Visual design, layout, animations
└── JavaScript  — Navigation, interactivity, simulated workflows
```

- No frameworks · No dependencies · No build process
- Fully functional offline - open the HTML file directly in any browser
- Deployable anywhere with zero infrastructure

---

## Production Architecture

In production this tool would connect to live systems:

| Layer | Technology | Purpose |
|---|---|---|
| Frontend | React / Next.js | User interface |
| API Layer | Node.js / FastAPI | Business logic and routing |
| AI Engine | Claude LLM API | Real-time compliance analysis |
| Data Source | CS Platform APIs | Live chat interaction feed |
| Rules Engine | Custom compliance library | Regulatory rule matching |
| Database | PostgreSQL | Findings, documents, remediation state |
| Audit Log | Immutable signed event store | Regulatory defensibility |

> The prototype simulates all AI-powered workflows using timed reveals.
> In production these would be real LLM API calls returning live compliance analysis.
> The UI pattern remains identical. Only the data source changes.

---

## Portfolio Context

This tool demonstrates candidacy for AI Operations, AI Governance, and Responsible AI roles:

| Skill Demonstrated | How |
|---|---|
| Regulatory knowledge | EU AI Act, GDPR, CCPA applied to real operational scenarios |
| Product thinking | User persona, use cases, end-to-end workflow design |
| Technical literacy | Built in code, understands API integration architecture |
| Operational experience | Remediation tracking, cross-functional ownership, escalation workflows |
| Communication | Complex regulatory concepts translated into plain operational language |

---

*Built by Seema Sherief
