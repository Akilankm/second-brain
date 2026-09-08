---
tags: [projects, backlog, bfsi, ai]
---

# BFSI AI Build Backlog

[[index|← Home]] · [[career/recognition-operating-system]] · [[ai/agentic-ai-bfsi-architecture]]

Prioritize projects that prove **domain understanding + production AI engineering + governance**.

## P0 — Regulatory Change Impact Agent

**Why:** public data, directly relevant to BFSI compliance, demonstrates context engineering and evidence.

### Input
- RBI / SEBI / IRDAI public circular or consultation paper

### Output
- obligations
- impacted business process
- impacted systems/controls
- owner/action proposal
- source evidence
- confidence
- human review queue

### Engineering capabilities
- ingestion
- chunking + metadata
- effective-date-aware retrieval
- structured extraction
- evidence grounding
- policy mapping
- eval dataset
- trace/observability

### Definition of done
- [ ] reproducible repo
- [ ] 20+ evaluation documents/examples
- [ ] precision/recall for obligation extraction
- [ ] grounded citation checks
- [ ] failure analysis
- [ ] architecture diagram
- [ ] cost/latency benchmark

---

## P1 — AML Investigation Agent

**Goal:** turn a synthetic transaction alert into an evidence-backed investigation summary.

Use synthetic/public data only.

Key evaluation:
- suspicious-pattern recall
- evidence completeness
- false unsupported claims
- tool-call correctness
- escalation accuracy

---

## P1 — Agentic AI Evaluation Harness

Reusable evaluator for:

- task completion
- groundedness
- tool selection
- tool arguments
- policy compliance
- human escalation
- latency
- cost

This can become a generic accelerator across multiple BFSI use cases.

---

## P2 — Credit Memo Copilot

Combine deterministic financial calculations and credit-policy rules with GenAI narrative generation.

Core lesson: **LLM reasoning must not replace deterministic credit calculations/policy controls.**

---

## P2 — BFSI Context Fabric Prototype

Build a small semantic/context layer connecting:

- business process
- regulations
- controls
- products
- entities
- documents
- effective dates

Expose it to an agent through well-bounded retrieval/tools.

---

## Selection rule

A project moves up the backlog when it scores highly on:

1. BFSI business relevance
2. TCS public-strategy relevance
3. reusable engineering value
4. production-readiness learning
5. demonstrability using non-confidential data
