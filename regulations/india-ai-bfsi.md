---
tags: [india, regulation, rbi, sebi, irdai, bfsi, ai, public-intelligence]
updated: 2026-09-10
---

# India AI + BFSI Regulatory Watch

[[index|← Home]] · [[bfsi/risk-compliance-ai]] · [[sources/source-catalog]]

This page records primary-source Indian regulatory and regulator-published AI material relevant to financial services. It does not treat TCS viewpoints as regulation and does not infer obligations beyond the cited regulatory source.

## Reserve Bank of India (RBI)

### Draft Guidance on Regulatory Principles for Model Risk Management — `regulatory / draft consultation`

**Published:** June 24, 2026  
**Press Release:** 2026-2027/528  
**Consultation closed:** July 24, 2026

RBI issued draft **Guidance on Regulatory Principles for Model Risk Management** covering all models used by regulated entities, explicitly including **third-party models** and models employing **AI / ML**.

The draft describes a model-risk governance perimeter covering:

- Board-approved Model Risk Management Frameworks
- risk-based model tiering and model inventories
- lifecycle governance from development/acquisition through validation, deployment, monitoring, change management, business continuity and decommissioning
- independent validation
- third-party model governance
- enhanced AI/ML controls

AI/ML-specific themes in the draft include bias/discriminatory-output risk, explainability, overfitting/generalisation, spurious correlations, stochastic/output variability, data-quality and drift risk, adversarial testing/red-teaming, stronger controls for dynamic or automatic model updates, and human oversight of automated decisions.

For customer-facing and generative systems, the draft introduces stronger transparency and cyber-control expectations, including safeguards against prompt-injection/adversarial inputs, disclosure that customers are interacting with AI and access to human assistance.

**Status discipline:** this remains a **draft**, not a final binding direction, unless RBI subsequently issues a final instrument.

Primary RBI domain / draft directions area:
- https://www.rbi.org.in/
- https://www.rbi.org.in/Scripts/BS_ViewREwiseDraftDirections.aspx

Deep study: [[research/rbi-model-risk-management-ai-ml-2026]]

### FREE-AI Committee Report — `regulatory`

**Published:** August 2025  
**Title:** *Framework for Responsible and Ethical Enablement of Artificial Intelligence (FREE-AI) Committee Report*

RBI's official reports/publications page lists the FREE-AI Committee report in August 2025, convened by Dr. Pushpak Bhattacharyya. The report is a primary RBI source on responsible and ethical AI enablement in the financial sector.

RBI reports page: https://m.rbi.org.in/scripts/bs_viewpublicationreport.aspx

Primary RBI domain: https://www.rbi.org.in/

The complete report should be consulted before quoting detailed principles or requirements; this note records the publication fact and scope at this level.

### MuleHunter.AI — mule-account detection — `regulator-published pilot`

RBI has publicly described **MuleHunter.AI**, an AI/ML model developed by the Reserve Bank Innovation Hub (RBIH) for detecting mule bank accounts used in financial fraud.

RBI's public material states that:

- MuleHunter.AI is an **AI/ML-based model** for identifying mule bank accounts
- it was being **piloted by RBIH**
- a pilot with **two large public-sector banks** had yielded encouraging results
- banks were encouraged to collaborate with RBIH to develop the initiative further

Primary RBI source: https://www.rbi.org.in/Scripts/BS_ViewBulletin.aspx?Id=23057

RBI Annual Report reference: https://www.rbi.org.in/scripts/AnnualReportPublications.aspx?Id=1436

This is a concrete regulator-led Indian banking AI initiative and is kept separate from regulatory-rule status.

### Global FinTech Fest 2026 — RBI Governor AI signal — `regulatory / official-speech`

**Published / delivered:** September 8, 2026

In the inaugural session of Global FinTech Fest 2026, the RBI Governor publicly cited **AI-driven analytics for fraud detection** and **real-time supervision** among the ways fintech is improving the efficiency and customer experience of India's financial infrastructure. The speech also reiterated RBI's policy posture of encouraging innovation while safeguarding trust, inclusion, fairness and system safety.

This is a current regulator-positioning signal, not a new AI rule.

Primary RBI speech: https://www.rbi.org.in/Scripts/BS_SpeechesView.aspx?Id=1576

### Global FinTech Fest 2026 — emerging-technology prudence and consequence-based AI governance — `regulatory / official-speech`

**Published / delivered:** September 9, 2026  
**Speaker:** Shri Rohit Jain, Deputy Governor, Reserve Bank of India  
**Title:** *Emerging Technologies in Finance: The Imperatives of Purpose, Prudence, and Policy*

The Deputy Governor described AI as increasingly augmenting **human judgment** in finance and identified three technology-amplified risk dimensions that matter as AI and other emerging technologies scale: **speed, concentration and opacity**.

The speech sharpens several governance/control expectations that are directly relevant to AI architecture in regulated financial institutions:

- **machine-speed resilience:** institutions should be able to detect problems early, contain effects and intervene before small errors amplify
- **concentration / common-dependency risk:** reliance on a small set of cloud, technology and model providers can transmit disruption or error across institutions
- **accountability despite outsourcing:** an institution may outsource computation, but responsibility for outcomes does not disappear when a model or technology is supplied by a third party
- **explainability / meaningful accountability:** higher model sophistication should not weaken the ability to explain consequential financial decisions
- **consequence-based proportionality:** low-consequence uses such as internal summarisation should not be treated like autonomous credit approval or transaction execution
- **stronger controls for higher-consequence AI:** governance, validation, oversight and intervention expectations should increase with the consequence of the use case
- **controlled experimentation:** regulatory sandboxes remain a mechanism for testing novel applications within defined safeguards before wider deployment
- **network-level fraud intelligence:** the speech cites the Digital Payments Intelligence Platform as recognition that fraud can cross institutional boundaries and may require near-real-time information sharing

This is **not a new binding AI rule**. It is an official RBI policy/supervisory signal that complements the June 2026 draft Model Risk Management Guidance and the earlier FREE-AI framework. It should be used to infer required control capabilities only at the architectural level; it does **not** constitute regulator endorsement of any TCS product or operating model.

Primary RBI speech: https://www.rbi.org.in/Scripts/BS_SpeechesView.aspx?Id=1577

## Securities and Exchange Board of India (SEBI)

### Responsible usage of AI/ML in Indian securities markets — `regulatory / consultation`

**Published:** 20 June 2025

SEBI published a consultation paper titled **“Consultation Paper on Guidelines for Responsible Usage of AI/ML in Indian Securities Markets.”**

Primary source: https://www.sebi.gov.in/reports-and-statistics/reports/jun-2025/consultation-paper-on-guidelines-for-responsible-usage-of-ai-ml-in-indian-securities-markets_94687.html

Status is recorded as a consultation paper; a consultation paper should not be presented as a final rule unless a later final regulation/circular is separately sourced.

### Advisory on advanced AI tools for vulnerability detection — `regulatory / advisory`

**Published:** 5 May 2026  
**Circular:** HO/13/19/12(1)2026-ITD-1_CIMGI/10873/2026

SEBI published an advisory titled **“Advisory on Emerging Advanced Artificial Intelligence (AI) Tools for Vulnerability Detection.”**

Primary source: https://www.sebi.gov.in/legal/circulars/may-2026/advisory-on-emerging-advanced-artificial-intelligence-ai-tools-for-vulnerability-detection_101270.html

### SEBI CyberSuraksha AI material — `regulator-published knowledge/cybersecurity`

SEBI's official CyberSuraksha portal publicly lists AI-related knowledge material including:

- **“AI-driven Emerging Cyber Security Threats and Defences for Securities market participants”** — 10 June 2026
- **“Frontier AI readiness: Defining the next era of enterprise resilience”** — 16 August 2026

Official portal: https://cybersuraksha-ai.sebi.gov.in/

These are regulator-published knowledge/tutorial items; they are not binding regulations.

#### Frontier AI readiness — machine-speed resilience and delegated-agent governance

**Published/listed:** August 16, 2026  
**Evidence class:** `regulator-published knowledge / thought-leadership`  
**Authoring organization:** Deloitte Touche Tohmatsu India LLP  
**Host:** SEBI CyberSuraksha

The 16-page regulator-hosted paper argues that frontier AI changes the **speed and scale** of cyber risk and therefore requires a higher-velocity operating model rather than a standalone AI policy. It organizes the response into six connected workstreams:

1. AI-speed vulnerability operations
2. exposure and attack-path reduction
3. identity resilience
4. AI-augmented security operations, deception and containment
5. crown-jewel recovery
6. secure AI governance

Its most relevant agentic-AI control statement is that **AI agents should be governed as delegated actors**, with risk determined by the combination of data, tools, permissions and autonomy available to them.

The paper recommends controls including:

- inventories of agents, copilots, models, plugins, connectors and tools
- documented owner, approved purpose, data access and action scope
- least privilege and read-only-by-default access where possible
- downstream authorization controls rather than relying on prompts/model behaviour for restraint
- logging of prompts, tool calls, data access, outputs and downstream actions
- ability to pause agents, revoke tokens and disable connectors
- adversarial re-testing when models, instructions, tools, connectors or permissions change
- separation of orchestration, logging, evaluation, tools and controls from the underlying model where practical
- governed reversible containment, rollback and audit trails
- identity governance for non-human identities including service accounts, bots, scripts and AI agents

The paper also says irreversible response actions should not be delegated to unproven automation, preserving an explicit human/control boundary as autonomy increases.

**Published visual:** the PDF includes **“Image 2: The six workstream programme for a resilient enterprise.”** The repository does not re-host the artwork.

**Status boundary:** this is a Deloitte perspective carried on SEBI's CyberSuraksha knowledge portal. It should not be presented as a SEBI regulation or mandatory control framework.

Regulator-hosted PDF: https://cybersuraksha-ai.sebi.gov.in/documents/48365173/0/Frontier_AI_Readiness_Enterprise_Resilience.pdf/bd92d325-a730-ec92-2e3e-feb634cd4ed0?t=1786867808004

Deep study: [[research/sebi-frontier-ai-readiness-enterprise-resilience-2026]]

## Insurance Regulatory and Development Authority of India (IRDAI)

Primary source monitored: https://irdai.gov.in/

This repository does not assert a dedicated IRDAI AI framework unless an exact IRDAI circular/guideline/report is captured and linked. General insurance cybersecurity, outsourcing, data and governance rules are not automatically labeled “AI regulation.”

## Regulatory-status discipline

The graph keeps these categories separate:

- **consultation** — proposal/discussion; not automatically final law/rule
- **report/framework** — authoritative publication, but legal effect depends on the document
- **circular/advisory** — regulator-issued material; applicability must be read from the source
- **regulator-published pilot** — regulator-backed technical initiative, not automatically a rule
- **regulator-published knowledge** — educational/technical material, not automatically binding
- **TCS thought leadership** — not regulation
- **product controls** — technical capability, not a legal requirement by itself

## Related TCS public material

TCS publicly discusses governance, auditability, guardrails, observability and human oversight in BFSI AI. Those TCS sources are cataloged separately in [[bfsi/risk-compliance-ai]] and [[ai/agentic-ai-bfsi-architecture]].

The RBI model-risk draft, September 2026 speeches and SEBI CyberSuraksha frontier-AI material should be compared against those TCS public controls only as an architecture/control mapping exercise; **RBI and SEBI do not endorse TCS products or architectures**.

## Related

[[bfsi/banking-ai]] · [[bfsi/insurance-ai]] · [[bfsi/capital-markets-ai]] · [[research/rbi-model-risk-management-ai-ml-2026]] · [[research/sebi-frontier-ai-readiness-enterprise-resilience-2026]] · [[sources/source-radar]]
