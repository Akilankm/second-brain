---
tags: [sources, verification, tcs, bfsi, ai, media, visuals, public-intelligence]
updated: 2026-09-09
---

# Source Radar and Verification Rules

[[index|← Home]] · [[sources/source-catalog]] · [[news/timeline]] · [[media/watchlist]] · [[media/visual-reference-library]]

> Build a high-recall, high-precision public evidence graph: search broadly, verify narrowly, preserve provenance, and keep evidence status explicit.

## Trust hierarchy

### Tier 1A — Primary / authoritative factual sources

**TCS**
- Newsroom: https://www.tcs.com/who-we-are/newsroom
- Events: https://www.tcs.com/who-we-are/events
- Artificial Intelligence: https://www.tcs.com/what-we-do/services/artificial-intelligence
- Banking: https://www.tcs.com/what-we-do/industries/banking
- Insurance: https://www.tcs.com/what-we-do/industries/insurance
- Capital Markets: https://www.tcs.com/what-we-do/industries/capital-markets
- TCS BaNCS: https://www.tcs.com/what-we-do/products-platforms/tcs-bancs
- Quartz: https://www.tcs.com/what-we-do/products-platforms/quartz
- BFSI Platforms: https://www.tcs.com/what-we-do/products-platforms/tcs-bfsi-platforms
- Investor Relations: https://www.tcs.com/who-we-are/investor-relations
- Annual Report: https://www.ar.tcs.com/
- TCS-hosted PDFs, brochures, research journals and white papers under `tcs.com/content/dam/...`

**Indian regulators**
- RBI: https://www.rbi.org.in/
- SEBI: https://www.sebi.gov.in/
- SEBI CyberSuraksha AI: https://cybersuraksha-ai.sebi.gov.in/
- IRDAI: https://irdai.gov.in/

**Standards / global authorities**
- BIS / Basel Committee: https://www.bis.org/
- FSB: https://www.fsb.org/
- FATF: https://www.fatf-gafi.org/

### Tier 1B — Official TCS media / public communications

Use for public vocabulary, demos, speaker statements, event recaps, product videos and visual references:

- TCSGlobal YouTube videos
- public videos linked by official TCS pages/newsletters
- Tata Consultancy Services official LinkedIn posts
- official TCS regional LinkedIn entities when directly relevant
- TCS event “Watch” pages
- TCS BaNCS newsletters/research journals
- TCS-hosted brochures, solution PDFs and architecture figures

Store high-value media in [[media/watchlist]] and figures in [[media/visual-reference-library]].

### Tier 2 — Direct ecosystem partners / customers

AWS, Google Cloud, Microsoft, NVIDIA, Anthropic, Mistral AI, OpenAI, ServiceNow, FICO, named customers and market-infrastructure partners when they publish the same initiative independently.

### Tier 3 — Analyst / industry evidence

Gartner, Forrester, IDC, NelsonHall, Everest Group, Celent and Chartis. Use for market positioning, independent capability assessments and adoption research, not as automatic proof of a specific live deployment.

### Tier 4 — Reputable news / discovery

Use to discover leads. Verify important claims against Tier 1–3 sources before promotion into durable notes.

### Tier 5 — Community / unverified social discussion

May surface leads, but must not become factual repository content without independent verification. Anonymous posts, rumors and “insider” claims are excluded.

## Evidence labels

| Label | Meaning |
|---|---|
| `live` | Source explicitly describes an active service/platform/capability |
| `deployed` | Source explicitly states implementation/deployment is operating |
| `pilot` | Source explicitly says pilot/PoC/trial |
| `announced` | Public announcement exists; deployment status may not be known |
| `planned` | Future activity/event/investment is stated |
| `public-case-study` | TCS/customer has published implementation evidence |
| `product-capability` | Product page states the capability but does not establish a named production deployment |
| `public-demo` | Public event/experience-center/video demonstrates or describes a solution/use case |
| `public-article-example` | Official article states an example/implementation without a full case-study artifact |
| `thought-leadership` | White paper/POV/journal; not proof of deployment |
| `analyst-recognition` | Third-party analyst assessment |
| `regulatory` | Regulator consultation, framework, circular, report or rule |
| `official-post` | Official social post; facts remain scoped to what it establishes |
| `official-video` | Official/publicly linked video; claims remain scoped to the video/content |

## Intelligence scoring

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| TCS relevance | none | adjacent | direct |
| BFSI relevance | none | indirect | direct |
| AI relevance | none | adjacent | core |
| Source quality | weak | credible secondary | primary/authoritative |
| Specificity | vague claim | named capability | named capability + figures/status/use case |
| Novelty | duplicate | incremental | meaningful new fact |

**Promote to radar:** normally 9+/12.  
**Keep in timeline:** lower-scoring items may remain when they establish chronology/status.  
**Keep in media/visual library:** lower novelty is acceptable if the asset materially improves understanding.

## Mandatory capture fields — factual item

- event date
- publication date when available
- entity/program/product
- evidence label
- factual statement
- numerical claims attributed to source
- original source URL
- publisher/source type
- confidence
- related Foam links

## Media capture fields

- title
- publisher/account
- publication date when available
- official/non-official status
- direct URL
- subject/domain
- information-dense facts/demos
- related durable notes

## Figure / architecture capture fields

- figure/title as published
- page/PDF URL
- section/page locator when known
- layers/components explicitly shown
- related Mermaid reconstruction if useful
- explicit statement that reconstruction is editorial, not an internal TCS diagram

## Update rules

1. Do not add duplicate news because a source was re-indexed.
2. Prefer event/announcement date over crawl date.
3. Preserve original URLs.
4. Separate product capability from production deployment evidence.
5. Separate TCS viewpoints from regulatory requirements.
6. Separate event/demo positioning from customer implementation evidence.
7. Separate company-wide AI partnerships from BFSI-specific evidence.
8. Do not add personal recommendations, employment guidance or career advice.
9. Do not store role, grade, joining, compensation or other personal-employment context.
10. Never add internal TCS information, confidential client material, credentials, non-public project details or rumors.
11. If a client is unnamed publicly, keep it unnamed.
12. If a fact cannot be verified, do not promote it as fact.
13. Link durable notes to at least two related Foam notes.
14. For public people, record only titles/topics published by TCS; never infer private org structure.
15. Do not re-host copyrighted architecture images; link originals and use clearly labelled Mermaid study reconstructions.
16. YouTube thumbnail embeds may link to public videos while media stays externally hosted.

## Continuous-monitoring queries

### TCS primary web
- `site:tcs.com/who-we-are/newsroom AI BFSI banking insurance capital markets TCS`
- `site:tcs.com/who-we-are/events TCS BFSI AI banking insurance`
- `site:tcs.com/what-we-do/industries/banking agentic AI GenAI`
- `site:tcs.com/what-we-do/industries/insurance agentic AI GenAI`
- `site:tcs.com/what-we-do/industries/capital-markets AI agentic`
- `site:tcs.com TCS BaNCS AI Quartz AI`
- `site:tcs.com TCS BaNCS research journal AI`
- `site:tcs.com "context fabric" BFSI`
- `site:tcs.com "Cognitive Automation Platform" agentic`
- `site:tcs.com "AI WisdomNext" agentic`

### Official media / posts
- `site:youtube.com/watch TCSGlobal BFSI AI`
- `site:youtube.com/watch TCSGlobal "TCS BaNCS"`
- `site:youtube.com/watch TCSGlobal "agentic AI"`
- `site:linkedin.com/posts/tata-consultancy-services BFSI AI`
- `site:linkedin.com/posts/tata-consultancy-services banking agentic AI`
- `site:linkedin.com/posts/tata-consultancy-services insurance AI`

### Regulation
- `site:rbi.org.in artificial intelligence banking responsible AI`
- `site:rbi.org.in AI ML fraud mule accounts banking`
- `site:sebi.gov.in artificial intelligence machine learning circular consultation`
- `site:cybersuraksha-ai.sebi.gov.in AI cybersecurity financial markets`
- `site:irdai.gov.in artificial intelligence insurance`

### Ecosystem
- TCS + AWS financial services AI
- TCS + Google Cloud BFSI Gemini
- TCS + Anthropic financial services
- TCS + NVIDIA BFSI AI Spectrum
- TCS + Microsoft financial services AI
- TCS + FICO insurance AI

## Output destinations

- high-signal facts → [[dashboards/tcs-bfsi-ai-radar]]
- chronology → [[news/timeline]]
- dated snapshots → `news/YYYY-MM-DD.md`
- initiatives/status → [[tcs/public-ai-initiative-index]]
- architecture → [[atlas/architecture-atlas]]
- use-case mapping → [[bfsi/use-case-atlas]]
- videos/posts/journals → [[media/watchlist]]
- official figures/diagrams → [[media/visual-reference-library]]
- TCS terminology → [[tcs/public-language-glossary]]
- public authors/speakers → [[people/public-voices]]
- public event agendas/recordings → [[events/public-event-watch]]
- source inventory → [[sources/source-catalog]]
