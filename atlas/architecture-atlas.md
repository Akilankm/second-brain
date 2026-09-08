---
tags: [atlas, architecture, tcs, bfsi, ai, agentic-ai, public-intelligence]
updated: 2026-09-09
---

# TCS BFSI AI — Public Architecture Atlas

[[index|← Home]] · [[tcs/public-ai-initiative-index]] · [[ai/agentic-ai-bfsi-architecture]] · [[bfsi/use-case-atlas]] · [[media/visual-reference-library]]

> This page reconstructs **only architecture concepts TCS has described publicly**. Mermaid diagrams are editorial reconstructions for study; they are **not internal TCS architecture diagrams** and should not be represented as such.

## 1. The public TCS BFSI AI stack — one-page system map

The recurring pattern across TCS' public BFSI AI material is: enterprise/core systems → governed data/context → models and agents → orchestration/guardrails → AI-augmented business work.

```mermaid
flowchart TB
  subgraph UX[AI-augmented work systems]
    U1[Banking operations]
    U2[Insurance operations]
    U3[Risk & compliance]
    U4[Advisory / wealth]
    U5[Customer service]
    U6[Capital markets]
  end

  subgraph ORCH[Agentic orchestration and control]
    A1[Specialist / doer agents]
    A2[Critique / compliance agents]
    A3[Agent orchestration]
    A4[Human review / override]
    A5[Observability & evaluation]
    A6[Policy / guardrails]
  end

  subgraph CTX[Context & knowledge fabric]
    C1[Process / task context]
    C2[Regulatory obligations]
    C3[Enterprise policies]
    C4[Semantic / ontology layer]
    C5[Knowledge / RAG]
    C6[Tool & API context]
  end

  subgraph MODELS[AI / analytics layer]
    M1[Foundation models / LLMs]
    M2[Enterprise / domain models]
    M3[ML / deep learning]
    M4[Embeddings]
    M5[Computer vision / NLP]
  end

  subgraph DATA[Data and governance platform]
    D1[Data products]
    D2[Data lakes / warehouses]
    D3[Catalog / metadata / lineage]
    D4[Access / privacy / audit]
    D5[External data]
  end

  subgraph CORE[Enterprise and financial systems]
    E1[Core banking / BaNCS]
    E2[Insurance platforms]
    E3[Payments]
    E4[CRM / ERP / DMS]
    E5[Market infrastructure]
    E6[Legacy systems]
  end

  CORE --> DATA --> MODELS --> CTX --> ORCH --> UX
  A4 --> ORCH
  A5 --> ORCH
  A6 --> ORCH
  D4 -. governance .-> CTX
  D4 -. governance .-> ORCH
```

**Public basis**

- [Context Fabric – The Backbone of Agentic AI in BFSI](https://www.tcs.com/what-we-do/industries/banking/white-paper/context-fabric-backbone-agentic-ai-bfsi)
- [Generative AI in Finance: Opening up a Sea of Possibilities](https://www.tcs.com/what-we-do/industries/banking/white-paper/generative-ai-finance-insurance-industry)
- [TCS Cognitive Automation Platform](https://www.tcs.com/what-we-do/industries/insurance/solution/cognitive-automation-platform-transform-banking)
- [TCS GenAI for BFSI](https://www.tcs.com/what-we-do/industries/banking/genai-insurance-banking-financial-services)

---

## 2. Context Fabric — architecture reconstructed from TCS Figure 1

TCS publicly describes a three-layer pattern: **agentic automation**, **context fabric**, and **data/governance platform**, with governance spanning the stack.

```mermaid
flowchart TB
  H[Human oversight / override]

  subgraph AGENT[Agentic automation layer]
    Q[User / workflow objective]
    D[Doer / specialist agent]
    K[Critique / compliance agent]
    ACT[Approved action / recommendation]
    Q --> D
    D --> K
    K -->|validated| ACT
    K -->|feedback| D
  end

  subgraph FABRIC[Enterprise context fabric]
    SEM[Semantic layer / business ontology]
    PROC[Process & task context]
    REG[Regulatory obligations]
    POL[Enterprise policy]
    TOOLS[Tools / API specifications]
    HIST[Precedents / historical examples]
    PROC --> SEM
    REG --> SEM
    POL --> SEM
    TOOLS --> SEM
    HIST --> SEM
  end

  subgraph DP[Data & governance platform]
    CAT[Data catalogues]
    LAKE[Data lakes]
    WH[Data warehouses]
    PROD[Data products]
    SEC[Entitlements / privacy / classification / audit]
  end

  D <--> SEM
  K <--> SEM
  SEM <--> CAT
  SEM <--> LAKE
  SEM <--> WH
  SEM <--> PROD
  H --> D
  H --> K
  SEC -. governance .-> FABRIC
  SEC -. runtime governance .-> AGENT
```

TCS' public terminology for operationalising this layer is:

| Pillar | Public description |
|---|---|
| **Externalise** | Curate business-specific functional context plus underlying data/analytics context into an accessible layer |
| **Harness** | Inject dynamic context into AI agents through the runtime harness |
| **Manage** | Keep context current using human-controlled feedback and enterprise knowledge |

Source: [Context Fabric – The Backbone of Agentic AI in BFSI](https://www.tcs.com/what-we-do/industries/banking/white-paper/context-fabric-backbone-agentic-ai-bfsi)

---

## 3. TCS Cognitive Automation Platform — public capability topology

TCS describes CAP as an agentic AI orchestration platform combining existing automation with agentic systems, knowledge, governance, observability, multi-modal inputs and integrations.

```mermaid
flowchart LR
  EVT[Events / emails / docs / alerts / workflow updates]

  subgraph CAP[TCS Cognitive Automation Platform]
    CMD[Command center]
    MESH[Agentic mesh]
    MARKET[Agent marketplace\n200+ pre-built agents]
    STUDIO[Agent studio / builder]
    KB[Knowledge fabric / RAG]
    GOV[Guardrails / policy / PII / hallucination controls]
    OBS[Observability / evaluation]
    TRANS[Transform.ai]
    MULTI[Multimodal ingestion]

    CMD --> MESH
    MARKET --> MESH
    STUDIO --> MESH
    KB --> MESH
    GOV --> MESH
    OBS --> MESH
    TRANS --> CMD
    MULTI --> KB
  end

  EVT --> CMD
  MESH --> LEG[Legacy applications]
  MESH --> MOD[Modern applications]
  MESH --> BP[Business operations]
  MESH --> IT[IT operations]
  MESH --> CX[Contact center / CX]
```

Publicly stated CAP features include:

- agentic mesh and agent marketplace
- **200+ pre-built reusable domain-trained AI agents**
- agent studio and future-ready agent builder
- event-driven agent triggers
- multi-step goal-driven workflows
- knowledge fabric and RAG
- responsible-agentic-AI guardrails
- multi-modal inputs
- deep process observability
- on-premises or hyperscaler deployment options

Source: [TCS Cognitive Automation Platform](https://www.tcs.com/what-we-do/industries/insurance/solution/cognitive-automation-platform-transform-banking)

See also: [[media/watchlist#tcs-unified-workbench--cognitive-automation-platform]]

---

## 4. TCS AI Spectrum for BFSI — NVIDIA-backed composite AI path

TCS describes AI Spectrum as an end-to-end BFSI AI framework for operationalising **Composite AI** — predictive AI plus generative AI — using NVIDIA's stack.

```mermaid
flowchart LR
  RAW[Financial documents / operational data / enterprise knowledge]
  CURATE[NeMo Curator\ndata preparation & curation]
  EMBED[NVIDIA embedding model\nlanguage understanding]
  CUSTOM[NeMo Customizer\nBFSI / enterprise customization]
  MODELS[Domain / enterprise AI models]
  GUARD[NeMo Guardrails\nsafety & topical controls]
  INFER[TensorRT / NIM\noptimized inference]
  USERS[Advisors / fund managers / investors / regulators / operations]

  RAW --> CURATE --> EMBED --> CUSTOM --> MODELS --> GUARD --> INFER --> USERS
```

Source: [TCS AI Spectrum for BFSI](https://www.tcs.com/what-we-do/industries/banking/solution/tcs-ai-spectrum-for-bfsi)

Official visual reference: [[media/visual-reference-library#tcs-ai-spectrum-for-bfsi-framework]]

---

## 5. TCS AI WisdomNext — public enterprise orchestration topology

TCS describes WisdomNext as a layer above models and agentic platforms that orchestrates **models, agents, data and workflows** while centralising governance, observability and cost visibility.

```mermaid
flowchart TB
  USE[Business / technology use case]

  subgraph WN[TCS AI WisdomNext]
    FLOW[Visual flow design]
    AO[Task & agent orchestration]
    DISC[Agent / tool discovery]
    EVAL[Evaluator bots / model comparison]
    GOV[Central guardrails & policies]
    OBS[End-to-end observability]
    FIN[Cost / FinOps visibility]
    PIPE[Enterprise data pipeline]
    LIB[Industry-tested agents & workflow templates]
  end

  subgraph ECOS[Model / platform ecosystem]
    C1[Cloud LLMs]
    C2[Open-source LLMs]
    C3[Internal models]
    C4[Agentic platforms]
  end

  subgraph ENT[Enterprise systems]
    E1[ERP]
    E2[SaaS]
    E3[Document platforms]
    E4[JIRA / Confluence]
    E5[APIs / databases]
  end

  USE --> FLOW --> AO
  LIB --> AO
  ECOS --> AO
  ENT --> PIPE --> AO
  EVAL --> AO
  GOV --> AO
  OBS --> AO
  FIN --> AO
```

Sources:

- [Accelerate Enterprise Generative AI Adoption with TCS AI WisdomNext](https://www.tcs.com/what-we-do/services/artificial-intelligence/solution/enterprise-generative-ai-adoption-wisdomnext)
- [TCS Launches WisdomNext](https://www.tcs.com/who-we-are/newsroom/press-release/tcs-launches-wisdomnext-an-industry-first-genai-aggregation-platform)
- [TCS AI WisdomNext — official TCSGlobal video](https://www.youtube.com/watch?v=FhQSMJT0vwc)

---

## 6. TCS BaNCS AI Compass — public AI core model

TCS announced AI Compass in December 2025 as an AI core for BaNCS combining ML/deep learning, GenAI and pre-built intelligent agents, with emphasis on responsible, explainable and traceable AI.

```mermaid
flowchart TB
  CORE[TCS BaNCS banking / securities core]
  DATA[Core transaction & operational context]
  ML[ML / deep learning]
  GEN[Generative AI]
  AG[Pre-built intelligent agents]
  XAI[Explainability / traceability]
  DEC[Actionable insights / workflow augmentation]
  RISK[Risk management]
  OPS[Operational excellence]

  CORE --> DATA
  DATA --> ML
  DATA --> GEN
  ML --> AG
  GEN --> AG
  AG --> XAI --> DEC
  DEC --> RISK
  DEC --> OPS
```

Source: [TCS BaNCS Gets AI Upgrade: AI Compass](https://www.tcs.com/who-we-are/newsroom/press-release/tcs-bancs-ai-upgrade-new-core-tool-supercharge-innovation)

---

## 7. ABOS — public fully agentic banking-operating-platform concept

The TCS BaNCS Research Journal describes ABOS as a **fully agentic AI-driven bank operating platform**. This is public TCS BaNCS thought leadership; the source should not be treated as proof of a named production deployment unless TCS publishes such evidence separately.

```mermaid
flowchart TB
  REQ[Natural-language business model / requirement]

  subgraph G[Genesis layer]
    NL[Natural-language bank modelling]
    GEN[Generate microservices / APIs / compliance rules]
  end

  subgraph H[Hyper-composability layer]
    AG[Agent-based orchestration]
    WF[Dynamic workflow composition]
    RT[Real-time adaptation]
  end

  subgraph P[Autonomous product layer]
    PI[Product ideation]
    PR[Risk / market / customer analysis]
    DEP[Rapid product creation / deployment]
  end

  subgraph W[Autonomous watchdog layer]
    COMP[Continuous compliance]
    FRAUD[Fraud / AML oversight]
    REG[Regulatory change response]
  end

  ADAPT[Adaptive AI engine]

  REQ --> NL --> GEN --> AG --> WF --> PI --> DEP
  PR --> PI
  COMP --> WF
  FRAUD --> WF
  REG --> WF
  ADAPT --> G
  ADAPT --> H
  ADAPT --> P
  ADAPT --> W
```

Sources:

- [Redefining Banking Intelligence with ABOS](https://www.tcs.com/what-we-do/products-platforms/tcs-bancs/articles/redefining-banking-intelligence-abos)
- [TCS BaNCS Research Journal Issue 16](https://www.tcs.com/what-we-do/products-platforms/tcs-bancs/research-journal/tcs-bancs-research-journal-16-future-finance)
- [Research Journal PDF — Redefining Banking Intelligence](https://www.tcs.com/content/dam/global-tcs/en/pdfs/what-we-do/platforms/TCS-BaNCS/research-journal/tcs-bancs-research-journal-16-redefining-banking-intelligence.pdf)

---

## 8. GenAI-for-BFSI operating model — public TCS framing

TCS' GenAI for BFSI page summarises its approach as:

```mermaid
flowchart LR
  A[ASSIST\nAI supports existing work]
  B[AUGMENT\nAI expands human capability]
  C[TRANSFORM\nAI reshapes end-to-end value streams]

  D[Data & integration-intensive\npolyglot architecture]
  H[Machine-first,\nhuman-in-the-loop]
  G[Enterprise-wide\nguardrails & ethics]

  A --> B --> C
  D --> A
  D --> B
  D --> C
  H --> B
  H --> C
  G --> A
  G --> B
  G --> C
```

Source: [TCS GenAI for BFSI](https://www.tcs.com/what-we-do/industries/banking/genai-insurance-banking-financial-services)

---

## 9. Quartz — coexistence of traditional systems, DLT and AI

Quartz publicly uses the idea of **co-existence**: keep conventional systems where appropriate while using on-chain/off-chain DLT and AI/ML where they add value.

```mermaid
flowchart LR
  LEG[Existing enterprise / market systems]
  GW[Quartz Gateway]
  OFF[Off-chain services / databases]
  ON[On-chain services / smart contracts]
  AI[AI / ML / NLP]
  CMD[Quartz Command Center]
  ECO[Participants / banks / exchanges / custodians / regulators]

  LEG <--> GW
  GW <--> OFF
  GW <--> ON
  AI --> OFF
  AI --> ON
  CMD --> OFF
  CMD --> ON
  ON <--> ECO
```

Sources:

- [Quartz — The Smart Ledgers](https://www.tcs.com/what-we-do/products-platforms/quartz)
- [Quartz Smart Solutions](https://www.tcs.com/what-we-do/products-platforms/quartz/solution/quartz-smart-solutions-dlt-friendly-ready-to-use)
- [Quartz for Interbank Ledger](https://www.tcs.com/what-we-do/products-platforms/quartz/solution/quartz-interbank-ledger)
- [Quartz for Surveillance](https://www.tcs.com/what-we-do/products-platforms/quartz/solution/quartz-surveillance)

---

## 10. Cross-map: which public TCS asset sits where?

| Public asset / concept | Primary public role | BFSI relevance | Evidence type |
|---|---|---|---|
| **TCS Cognitive Automation Platform** | Agentic orchestration + business/IT automation | Direct | Product/solution page |
| **TCS AI Spectrum for BFSI** | Composite AI framework | Direct | BFSI solution page |
| **Context Fabric** | Semantic/context layer for regulated agents | Direct | BFSI white paper |
| **TCS AI WisdomNext** | Model/agent/data orchestration and governance | Cross-industry, usable in BFSI | Product page + video |
| **TCS BaNCS AI Compass** | AI core for banking/securities platform | Direct | Product announcement |
| **ABOS** | Fully agentic banking-operating-platform concept | Direct | BaNCS thought leadership |
| **Quartz** | DLT + AI for trusted financial ecosystems | Direct in several solutions | Product pages/case evidence |
| **GenAI for BFSI** | AI-led assist/augment/transform operating model | Direct | BFSI capability page |

## Related Foam notes

- [[tcs/tcs-bfsi-ai-offerings]]
- [[tcs/public-language-glossary]]
- [[bfsi/use-case-atlas]]
- [[bfsi/public-implementations]]
- [[media/watchlist]]
- [[media/visual-reference-library]]
- [[people/public-voices]]
