---
tags: [sources, verification, tcs, bfsi, ai, public-intelligence]
updated: 2026-09-09
---

# Source Radar and Verification Rules

[[index|← Home]] · [[sources/source-catalog]] · [[news/timeline]]

## Trust hierarchy

### Tier 1 — Primary / authoritative

Use these first for factual claims.

**TCS**
- Newsroom: https://www.tcs.com/who-we-are/newsroom
- Events: https://www.tcs.com/who-we-are/events
- Banking: https://www.tcs.com/what-we-do/industries/banking
- Insurance: https://www.tcs.com/what-we-do/industries/insurance
- Capital Markets: https://www.tcs.com/what-we-do/industries/capital-markets
- BFSI Platforms: https://www.tcs.com/what-we-do/products-platforms/tcs-bfsi-platforms
- Investor Relations: https://www.tcs.com/who-we-are/investor-relations
- Annual Report: https://www.ar.tcs.com/

**Indian regulators**
- RBI: https://www.rbi.org.in/
- SEBI: https://www.sebi.gov.in/
- IRDAI: https://irdai.gov.in/

**Standards / global financial authorities**
- BIS / Basel Committee: https://www.bis.org/
- FSB: https://www.fsb.org/
- FATF: https://www.fatf-gafi.org/

### Tier 2 — Direct ecosystem partners / customers

AWS, Google Cloud, Microsoft, NVIDIA, Anthropic, Mistral AI, OpenAI, ServiceNow and named customers when they publish the same program independently.

### Tier 3 — Analyst / industry evidence

Gartner, Forrester, IDC, NelsonHall, Everest Group, Celent and Chartis. These are useful for externally assessed capabilities, not as a replacement for primary evidence about product status or deployments.

### Tier 4 — Reputable news / discovery

Use to discover leads. Verify important claims against Tier 1–3 sources before promotion into durable notes.

## Evidence labels

Every entry must use one of these labels where applicable:

| Label | Meaning |
|---|---|
| `live` | TCS/source explicitly describes an active service/platform/capability |
| `deployed` | Source explicitly states implementation/deployment is operating |
| `pilot` | Source explicitly says pilot/PoC/trial |
| `announced` | Public announcement exists; deployment status may not be known |
| `planned` | Future activity/event/investment is stated |
| `public-case-study` | TCS/customer has published implementation evidence |
| `thought-leadership` | White paper/POV; represents a public TCS view, not proof of deployment |
| `analyst-recognition` | Third-party analyst assessment |
| `regulatory` | Regulator consultation, framework, circular, report or rule |

## Intelligence scoring

Score candidate items from 0–2 on each dimension.

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| TCS relevance | none | adjacent | direct |
| BFSI relevance | none | indirect | direct |
| AI relevance | none | adjacent | core |
| Source quality | weak | credible secondary | primary/authoritative |
| Specificity | vague claim | named capability | named capability + figures/status/use case |
| Novelty | duplicate | incremental | meaningful new fact |

**Promote to the current radar:** normally 9+/12.  
**Keep in the timeline:** lower-scoring items may be retained if they establish chronology or status history.

## Mandatory capture fields

For every new factual item record:

- event date
- publication date when available
- entity / program / product
- evidence label
- factual statement
- exact numerical claims, if any, attributed to the source
- original source URL
- source publisher/type
- confidence
- related Foam links

## Update rules

1. Do not add duplicate news simply because the source was re-indexed.
2. Prefer the event/announcement date over crawl date.
3. Preserve original source URLs.
4. Separate product capability claims from proof of production deployment.
5. Separate TCS-authored viewpoints from regulatory requirements.
6. Do not convert public facts into personal recommendations or career advice.
7. Do not store role, grade, joining, compensation, personal-employment or other private context.
8. Never add internal TCS information, confidential client material, credentials, non-public project details or rumors.
9. If a client is unnamed in the public source, keep it unnamed.
10. If a fact cannot be verified, do not promote it as fact.
11. Link durable notes to at least two related Foam notes.

## Continuous-monitoring queries

- `site:tcs.com/who-we-are/newsroom AI BFSI banking insurance capital markets TCS`
- `site:tcs.com/who-we-are/events TCS BFSI AI banking insurance`
- `site:tcs.com/what-we-do/industries/banking agentic AI GenAI`
- `site:tcs.com/what-we-do/industries/insurance agentic AI GenAI`
- `site:tcs.com TCS BaNCS AI Quartz AI`
- `site:rbi.org.in artificial intelligence banking responsible AI`
- `site:sebi.gov.in artificial intelligence machine learning circular consultation`
- `site:irdai.gov.in artificial intelligence insurance`

## Output destinations

- current high-signal facts → [[dashboards/tcs-bfsi-ai-radar]]
- chronology → [[news/timeline]]
- dated research snapshot → `news/YYYY-MM-DD.md`
- durable product/initiative knowledge → `tcs/`, `bfsi/`, `ai/`, `regulations/`
- source inventory → [[sources/source-catalog]]
