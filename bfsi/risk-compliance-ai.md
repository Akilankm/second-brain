---
tags: [bfsi, risk, compliance, ai, aml, kyc, governance]
---

# BFSI Risk, Compliance & AI

[[index|← Home]] · [[bfsi/domain-map]] · [[ai/agentic-ai-bfsi-architecture]]

## Why this area matters

Risk and compliance is one of the best places to build differentiated AI expertise because value and control must coexist. A fast AI system that cannot explain, evidence or bound its decisions is often unusable in regulated workflows.

## Core use-case map

| Process | AI role | Primary risk |
|---|---|---|
| KYC/CDD | document extraction, entity resolution, risk summarization | identity error, privacy, stale evidence |
| AML monitoring | alert prioritization, investigation support | missed suspicious activity, false positives |
| Sanctions | entity matching, adverse evidence | false negatives, explainability |
| Fraud | anomaly detection, investigation orchestration | latency, adversarial behavior |
| Credit | scoring support, memo generation | bias, policy violation, model risk |
| Regulatory change | obligation extraction, impact mapping | hallucinated/omitted obligations |
| Compliance QA | evidence review, control testing | incomplete audit trail |
| Conduct surveillance | communications/event analysis | privacy, false accusation |

## Architecture principle

Use LLMs where language/context/reasoning help, but retain deterministic systems where policy, thresholds and calculations must be exact.

A strong pattern is:

`Predictive model / rules → evidence retrieval → agent reasoning → policy check → human approval where required → action → immutable audit trace`

## Control families for GenAI / agentic AI

### Input controls
- data classification
- PII handling
- prompt injection defenses
- source authorization

### Model controls
- approved model registry
- versioning
- validation and benchmark thresholds
- fallback model behavior

### Retrieval/context controls
- source lineage
- effective-date filtering
- jurisdiction filtering
- entitlements
- freshness checks

### Agent/tool controls
- allow-listed tools
- least privilege
- transaction limits
- idempotency
- maker-checker approval
- reversible actions where possible

### Output controls
- structured output validation
- citations/evidence
- prohibited-content checks
- deterministic policy validation

### Runtime controls
- traces
- latency/cost monitoring
- drift
- task success rate
- hallucination/groundedness measures
- anomaly detection

### Governance controls
- model/agent inventory
- owner
- intended use
- risk tier
- approval history
- incident process
- periodic review

## Indian regulatory radar

### SEBI

SEBI has explicitly addressed responsibility around AI/ML usage by regulated entities and has also issued guidance/advisories related to responsible usage and advanced AI tools. Track new circulars continuously.

Useful public starting points:

- https://www.sebi.gov.in/legal/circulars/may-2026/advisory-on-emerging-advanced-artificial-intelligence-ai-tools-for-vulnerability-detection_101270.html
- https://www.sebi.gov.in/sebi_data/attachdocs/jun-2025/1750415065695.pdf

### RBI

Track RBI material touching digital lending, model risk, cybersecurity, fraud, data governance, responsible AI and supervisory technology.

Source root: https://www.rbi.org.in/

### IRDAI

Track insurance cyber, governance, outsourcing, digital distribution, claims and AI-related developments.

Source root: https://irdai.gov.in/

## High-value demo ideas

1. **AML investigation agent** — alert + transactions + KYC + policy → evidence-backed investigation brief.
2. **Regulatory change impact agent** — circular → obligations → impacted processes/controls → owner/action list.
3. **Credit memo copilot** — structured financial metrics + policy rules + sourced narrative.
4. **Control evidence reviewer** — tests whether required evidence exists before a case is closed.

## Design review questions

- What happens when retrieval returns conflicting regulations?
- Can the system prove which version of a rule was used?
- Which actions require maker-checker approval?
- How are false negatives measured?
- How is privileged/customer data isolated?
- Can an investigator reconstruct the complete agent decision path months later?
