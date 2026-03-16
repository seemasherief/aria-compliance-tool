# ARIA - **A**I **R**isk & Compliance **I**ntelligence **A**ssistant
### Built by Seema Sherief

A proactive compliance risk mitigation tool for e-commerce Customer Service AI systems.

🔗 **[View Live Tool](https://seemasherief.github.io/aria-compliance-tool)**

---

About This Project:
ARIA (AI Risk & Compliance Intelligence Assistant) helps AI Compliance Managers proactively monitor, assess and remediate compliance risks in customer service AI systems. It covers three major regulatory frameworks - the EU AI Act, GDPR and CCPA, and translates complex legal obligations into an operational workflow that a non-lawyer can act on daily.
The tool was built as a portfolio prototype to demonstrate:

Deep understanding of AI governance and data privacy regulations
Ability to translate regulatory complexity into operational tools
Product thinking: user personas, use cases, information architecture
Cross-functional awareness across Tech, Legal, Data and CS Operations


Build Notes

Built from scratch using VS Code, learning in real time
Every line of code typed manually
Total build time: approximately 9 hours
Tool: HTML, CSS, vanilla JavaScript - single file, zero dependencies


The Problem This Tool Solves
E-commerce companies are rapidly deploying AI in customer service - chatbots, auto-routing, sentiment analysis, fraud detection. This deployment is outpacing compliance infrastructure. The result: significant regulatory exposure.
Risk AreaRegulationReal ExposureAI chatbot doesn't identify itself as AIEU AI Act Art. 52Fines up to €15MPII collected in chat without lawful basisGDPR Art. 6, 32Data breach liabilityAutomated refund/resolution decisionsEU AI Act Art. 14Customer right to human review not metRouting bias by language/demographicEU AI Act Art. 10Discriminatory service accessChat logs retained beyond policyGDPR Art. 5(e)Right to deletion violationsNo audit trail for AI decisionsEU AI Act Art. 12Cannot respond to regulatory enquiry
Most CS teams lack a dedicated compliance monitoring layer for AI systems. ARIA provides the AI Ops Manager with a single command centre to be proactive, cross-functional, and audit-ready.

The 4 CS AI Systems Being Monitored
1. CS Chatbot v2.4 — 32% Compliant — CRITICAL
The customer-facing conversational AI. The one customers type to when they contact support. It handles order enquiries, returns, refunds, and complaints. The most visible and most heavily regulated system because it directly interacts with customers. Currently the worst performer with 8 open issues.
2. Auto-Routing Engine — 61% Compliant — HIGH
An invisible system customers never see. When a customer contacts support, this AI reads the message and routes it to the right team — returns, billing, complaints, or the chatbot. It makes routing decisions thousands of times a day. A 23% language bias issue lives here — it's routing non-English speakers to the AI bot more often than English speakers.
3. Sentiment Classifier — 79% Compliant — MEDIUM
Reads every customer message in real time and scores the emotional tone — frustrated, neutral, satisfied, angry. Uses that score to flag high-risk conversations for priority human handling. 2 open issues, likely around profiling of customer emotional states under GDPR Art. 22.
4. Return Fraud Detector — 91% Compliant — LOW
A machine learning model that analyses return requests and assigns a fraud probability score. Flags unusual patterns for human review. The healthiest system at 91%. The 1 remaining issue relates to documenting decision criteria so wrongly-flagged customers can challenge the decision — required under GDPR Art. 22 and EU AI Act Art. 14.

The 6 Modules — Detailed Explanation

01 · Dashboard — Compliance Overview
Purpose: The morning briefing screen. Everything critical surfaced in one view so the AI Ops Manager can prioritise their day in under 60 seconds.
The 4 KPI Cards:

Overall Risk Score — 72/100 — A composite weighted score across all risk categories. Amber because it is in the warning zone. Think of it like a credit score but for AI compliance. The higher the number, the more urgent the risk.
EU AI Act Readiness — 68% — Out of all applicable EU AI Act requirements, 68% are currently being met. Calculated by scoring 8 specific articles as compliant (100%), partial (50%), or non-compliant (0%) and averaging the results. Green because it is trending upward.
Open Violations — 14 — 14 active compliance problems right now, broken down as: 3 Critical, 6 High, 4 Medium, 1 Low. Red because the critical count demands immediate attention.
Interactions Scanned — 24,891 · 98.2% coverage — 24,891 customer service conversations were analyzed for compliance issues in the last 30 days. 98.2% coverage means that out of every 100 conversations, ARIA successfully scanned 98.2 of them. The 1.8% gap represents conversations on channels not yet fully connected to ARIA.

How the Risk Score (72) is calculated:
The composite score is a weighted average across 6 risk categories. Each category carries a different weight because some matter more legally and financially than others:
CategoryWeightScoreContributionData Privacy25%8521.25AI Transparency20%7414.80Human Oversight20%6813.60Bias & Fairness15%619.15Accuracy12%455.40Logging & Audit8%786.24Total100%—≈ 72
Data Privacy carries the highest weight (25%) because GDPR fines are the largest financial risk — up to 4% of global annual turnover. Logging carries the least weight (8%) because while important, it does not directly harm customers.
How EU AI Act Readiness (68%) is calculated:
8 specific EU AI Act articles were assessed. Each is scored as Passing (100%), In Progress (50%), or Failing (0%):
ArticleStatusScoreArt. 52 — TransparencyFAILING0%Art. 14 — Human OversightFAILING0%Art. 12 — LoggingIN PROGRESS50%Art. 9 — Risk ManagementPASSING100%Art. 13 — Transparency to deployersPASSING100%Art. 10 — Data governancePASSING100%Art. 11 — Technical docsIN PROGRESS50%Art. 15 — Accuracy testingPASSING100%
Average = (0+0+50+100+100+100+50+100) ÷ 8 = 62.5%, weighted by article importance = 68%
Why only 3 Critical and 6 High out of 14 violations?
The 14 violations are tiered by urgency:

3 Critical — Direct legal violations with immediate financial consequences. Must fix within 30 days.
6 High — Serious regulatory exposure but not immediately actionable by regulators. Fix within 90 days.
4 Medium — Bad practice but low immediate risk. Fix within 180 days.
1 Low — Minor non-conformance, negligible risk.

The 4 Live Compliance Alerts explained:
Alert 1 — AI agent not disclosing automated nature to customers
The CS chatbot is having conversations without ever saying it is an AI. 847 customers today were misled into thinking they were talking to a human. EU AI Act Article 52(1) makes this illegal. Fines up to €15 million. The version number CS Bot v2.4 matters because when v2.5 ships with the fix, the violation stops — and that is traceable.
Alert 2 — PII data retained beyond policy limit
Customer personal data — names, email addresses, order details — is being stored longer than the company's own 90-day retention policy. 12,400 records are currently at risk. GDPR Article 5(e) requires data minimisation and storage limitation. CCPA §1798.100 gives customers the right to know their data is not held indefinitely.
Alert 3 — Escalation rate disparity across customer segments
The Auto-Routing Engine is sending English-speaking customers to human agents 23% more often than non-English speakers. Non-English customers are kept with the AI bot longer even when their issues are equally complex. EU AI Act Article 10 requires AI systems not to produce discriminatory outcomes. A 23% measurable gap based on language is a potential bias violation.
Alert 4 — Missing human override documentation
Three types of AI decisions have no written procedure for when and how a human agent should step in. EU AI Act Article 14 requires that oversight mechanisms exist AND are documented. Having an escalation button is not enough — there must be a written procedure that agents follow.

02 · AI Assessment
Purpose: A structured tool to run a formal compliance audit on any of the four CS AI systems. Turns a complex regulatory checklist into an operational form any manager can complete.
The Assessment Form:

Select which AI system to audit
Select the type of assessment — Full Audit, EU AI Act Gap Analysis, GDPR Privacy Assessment, Bias Evaluation, or Human Oversight Review
Describe the system in plain English to provide context
List any known risk areas already suspected
Click Run Assessment — a scanning animation plays then a findings report appears

The 8 EU AI Act Articles in the Checklist — explained:
Art. 52(1) — Transparency to End Users
When a customer interacts with an AI — chatbot, voice assistant, automated email — the AI must tell them it is an AI before or at the start of the interaction. This is the most talked-about EU AI Act obligation. Customers have the legal right to know they are not talking to a human.
Art. 14 — Human Oversight
AI systems must be designed so humans can monitor, intervene, and override the AI at any time. This means documented procedures, trained staff, and functional override controls. It is not enough to say humans can take over — you must prove how and when with written evidence.
Art. 9 — Risk Management System
Before deploying any AI system, a continuous risk management process must exist. This means identifying risks before launch, testing for them, and continuing to monitor after deployment. It is an ongoing obligation — not a one-time exercise.
Art. 11 — Technical Documentation
A detailed written record of the AI system must exist covering: how it was designed, what data it was trained on, how it was tested, what its performance metrics are, and what its known limitations are. Must be maintained and updated when the system changes.
Art. 12 — Logging and Record-Keeping
The AI system must automatically record its own decisions and actions with timestamps. If a customer or regulator asks "why did the AI refuse my refund on March 15th at 10:16am?" — the log must answer that question. Without this, the company cannot defend its decisions.
Art. 10 — Data Governance
The data used to train and operate the AI must be relevant, accurate, complete, and unbiased. Companies must verify that training data does not contain historical biases causing the AI to treat different customer groups unfairly. This is the article behind the 23% language routing gap.
Art. 43 — Conformity Assessment
Before a high-risk AI system is deployed to the public, it must go through a formal conformity assessment — confirming it meets all EU AI Act requirements. Think of it like an MOT certificate for AI systems. Must be documented and renewed when the system changes significantly.
Art. 15 — Accuracy, Robustness and Cybersecurity
The AI must perform accurately and consistently across normal use and edge cases. Must be tested against errors, unexpected inputs, and attempted manipulation. For a CS chatbot this means testing what happens when a customer types something confusing, abusive, or designed to trick the system.
The Assessment Report — explained in full:
After clicking Run Assessment, the report contains three layers:
Layer 1 — Three Summary Boxes

3 Critical Gaps — must fix immediately, direct legal violations
5 High Gaps — serious but slightly less urgent
4 Compliant Items — what is already working correctly

Layer 2 — Findings Table
FindingWhy It MattersAI identity not disclosed — Art. 52(1) — CRITICAL847 violations daily. Fines up to €15M. Most urgent fix.No human escalation pathway — Art. 14 — CRITICALMandatory regulatory review required. Cannot be compliant without this.PII in unencrypted logs — GDPR Art. 32 — CRITICALData breach liability. Class action exposure. GDPR fines up to 4% of turnover.English customers escalated 23% more — Art. 10 — HIGHDiscriminatory service access. Measurable and documented — regulators treat this seriously.No automated logging of AI decisions — Art. 12 — HIGHAuditability gap. Cannot produce decision records if asked by regulator.
Layer 3 — Action Buttons

Generate Documentation → goes directly to Tab 5 to produce required documents
View Remediation Plan → goes directly to Tab 6 to track fixes


03 · Interaction Analyzer
Purpose: Catches violations at the ground level — inside individual customer conversations. While the Dashboard shows systemic trends, this tab shows exactly what is going wrong in specific interactions.
The Sample Conversation — Case #CS-48291:
Six messages with compliance flags appearing inline inside the conversation bubbles:

Customer asks about a missing order
AI responds without disclosing it is an AI ← No AI disclosure flag
Customer provides order number and email address
AI confirms the issue and processes a refund automatically ← PII collected flag + Auto-decision flag
Customer asks for replacement instead of refund
AI refuses and offers no human option ← No escalation offered flag

The flags appear directly inside the bubble where the violation happened so you can pinpoint the exact moment of non-compliance.
Interaction Risk Score — 88/100:
This single conversation scores 88 — very high risk. Badges show 2 Critical, 2 High, and 1 Compliant item. The one compliant item is that the AI correctly identified the order issue and provided accurate information — not everything was wrong.
Bulk Scan Summary — Last 7 Days:
Shows systemic violation volumes across all scanned conversations:
Flag TypeCountTrendNo AI disclosure847▲ +12% — worseningPII without consent392▲ +4% — worseningAuto-decision no review219▼ -8% — improvingNo escalation offered541▲ +2% — slightly worsening
The downward trend on auto-decisions shows remediation work is starting to have impact.

04 · Regulatory Map
Purpose: A complete reference map showing which laws apply, which specific articles matter for CS AI, and the current compliance status of each one. Solves the problem of overlapping obligations across multiple frameworks.
Three Regulation Cards:
EU AI Act
Applies as a customer-facing AI system. Transparency obligations are mandatory regardless of risk tier. Key failing articles: Art. 52 (transparency) and Art. 14 (human oversight).
GDPR
Applies to all EU customer personal data. Chat logs, email addresses, and behavioural data all constitute personal data under Art. 4. Key failing articles: Art. 6 (no clear lawful basis for PII collection) and Art. 32 (unencrypted logs).
CCPA / CPRA
Applies to California residents regardless of company location if revenue or data thresholds are met. Key areas: right to know, right to delete, right to opt out of data sharing.
Cross-Regulation Impact Matrix:
Shows that one operational problem often violates multiple regulations simultaneously. For example — PII collection in chat violates EU AI Act Art. 10, GDPR Art. 6 and 32, CCPA §1798.100, AND internal policy P-PRIV-03 all at the same time. This matrix helps prioritise fixes that deliver the most compliance coverage per remediation effort.

05 · Doc Generator
Purpose: Produces the actual regulatory documents that CS AI systems are legally required to have. Accelerates what normally takes weeks into hours.
The 7 Document Types:
1. EU AI Act Technical Documentation (Art. 11)
The formal technical record of how the AI system was built, what data it uses, and how it performs. Required before deployment and must be kept updated.
2. GDPR Data Protection Impact Assessment (DPIA)
Mandatory when processing personal data at scale. Identifies privacy risks and documents mitigation measures. Required under GDPR Art. 35 when AI processes sensitive customer data.
3. AI Transparency Notice
The customer-facing statement explaining they are talking to an AI and what their rights are. Required under EU AI Act Art. 52. Must appear at the start of every AI interaction.
4. Human Oversight Procedure Manual
The written procedure agents follow when reviewing or overriding an AI decision. Required under EU AI Act Art. 14. Cannot be compliant without this document existing and being actively used.
5. Bias Audit Report
Documents the results of testing the AI for unfair treatment of different customer groups. Required under EU AI Act Art. 10. The 23% language routing gap would be documented and remediated here.
6. Incident Response Playbook
Step-by-step procedures for data breaches or AI failures. GDPR Art. 33 requires notifying regulators within 72 hours of a breach. This playbook ensures the team knows exactly what to do when something goes wrong.
7. Conformity Self-Assessment (Art. 43)
A self-evaluation confirming the system meets EU AI Act requirements before deployment. Think of it as the AI system's certificate of roadworthiness.
Document Library:
Tracks all existing documents with status — Approved, Draft, In Review, or Missing. The Human Oversight Manual is flagged as Missing — a critical gap visible right on screen.

06 · Remediation & Action Plan
Purpose: The execution layer. After the Dashboard identifies problems and the Assessment details them, this tab tracks who is fixing what, by when, and how far along they are. Turns compliance gaps into managed work items.
The 4 Summary Cards:

Critical — Act Now — 3 items — resolve within 30 days
High Priority — 6 items — resolve within 90 days
Medium Priority — 4 items — resolve within 180 days
Resolved This Month — 7 items — up from 3 last month (positive trend)

The 6 Active Remediation Items:
IDIssueOwnerDeadlineProgressStatusREM-001Add AI disclosure at chat startTech LeadApr 1565%In ProgressREM-002Encrypt PII in chat logsData EngApr 2220%BEHIND — most urgentREM-003Document human override proceduresAI Ops MgrMay 140%In ProgressREM-004Implement 90-day log retentionData EngMay 1580%Nearly doneREM-005Fix multilingual routing biasML TeamJun 110%Just startedREM-006Enable automated event loggingTech LeadJun 1555%In Progress
REM-002 is the most critical item to watch — PII encryption is only 20% complete with a deadline in days.

Regulations Covered
EU AI Act (2024 — In Force)

Art. 9 — Risk Management
Art. 10 — Data Governance & Bias
Art. 11 — Technical Documentation
Art. 12 — Logging & Record-Keeping
Art. 13 — Transparency to Deployers
Art. 14 — Human Oversight
Art. 15 — Accuracy & Robustness
Art. 43 — Conformity Assessment
Art. 52 — Transparency to Users

GDPR (EU 2016/679)

Art. 5 — Data minimisation and storage limitation
Art. 6 — Lawful basis for processing
Art. 22 — Automated decision-making
Art. 30 — Records of processing
Art. 32 — Security of processing
Art. 33 — Breach notification (72 hours)
Art. 35 — Data Protection Impact Assessment

CCPA / CPRA (California)

§1798.100 — Right to know
§1798.105 — Right to delete
§1798.120 — Right to opt-out
§1798.140 — Sensitive personal information
§1798.150 — Security and breach liability


Technology

HTML — Structure and content
CSS — Visual design, layout, animations
JavaScript — Tab navigation, interactive assessment, doc generation
Single-file architecture — no frameworks, no dependencies, no build process
Deployable anywhere with zero infrastructure
Fully functional offline — open the HTML file directly in any browser


Production Architecture (If Built for Real)
In a production environment this would connect to:
Frontend (React/Next.js)
    ↓
API Layer (Node.js / FastAPI)
    ↓
[LLM API — Claude]  [CS Platform APIs]  [Compliance Rules Engine]
    ↓                      ↓                      ↓
Assessment             Live Chat              Regulatory
Generation             Stream                 Rule Library
    ↓
[Database] ← Findings, documents, remediation state
    ↓
[Immutable Audit Log] ← Cryptographically signed compliance events
The prototype simulates all AI-powered workflows using timed reveals. In production these would be real API calls to an LLM returning live compliance analysis.

Portfolio Context
This tool was built to demonstrate candidacy for AI Operations, AI Governance, and Responsible AI roles. It shows:

Regulatory knowledge — EU AI Act, GDPR, CCPA applied to real operational scenarios
Product thinking — user persona, use cases, end-to-end workflow design
Technical literacy — built in code, understands architecture and API integration
Operational experience — remediation tracking, cross-functional ownership, escalation workflows
Communication — complex regulatory concepts translated into plain operational language


Built by Seema Sherief 
