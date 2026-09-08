---
tags: [sources, research, tcs, bfsi, ai]
---

# Source Radar

[[index|← Home]] · [[dashboards/tcs-bfsi-ai-radar]] · [[templates/intelligence-note]]

## Trust hierarchy

### Tier 1 — Primary / authoritative

Use these first for facts, regulations and company direction.

#### TCS
- Newsroom: https://www.tcs.com/who-we-are/newsroom
- Banking: https://www.tcs.com/what-we-do/industries/banking
- BFSI platforms: https://www.tcs.com/what-we-do/products-platforms/tcs-bfsi-platforms
- Investor relations: https://www.tcs.com/who-we-are/investor-relations

#### Indian regulators
- RBI: https://www.rbi.org.in/
- SEBI: https://www.sebi.gov.in/
- IRDAI: https://irdai.gov.in/

#### Global financial / standards bodies
- BIS: https://www.bis.org/
- Basel Committee: https://www.bis.org/bcbs/
- Financial Stability Board: https://www.fsb.org/
- FATF: https://www.fatf-gafi.org/

### Tier 2 — Strong ecosystem sources

- AWS financial services
- Microsoft financial services / Azure AI
- Google Cloud financial services
- NVIDIA financial services
- Anthropic / OpenAI / major model-vendor technical releases
- major cloud security and AI governance documentation

### Tier 3 — Analyst / industry intelligence

Use for market interpretation, then verify important claims against primary sources when possible.

- Gartner
- Forrester
- IDC
- NelsonHall
- Everest Group
- Celent
- Chartis Research

### Tier 4 — News / community

Useful for discovery, not as the sole basis for a high-confidence claim.

## Topics to continuously monitor

### TCS
- AI strategy
- AI revenue / deals
- BFSI wins
- banking / insurance / capital-markets offerings
- agentic AI platforms
- GenAI / composite AI
- Google/AWS/Azure/NVIDIA partnerships
- innovation labs / experience centers

### BFSI business
- retail banking
- lending
- payments
- fraud
- AML/KYC
- capital markets
- insurance
- wealth
- service operations

### AI engineering
- agent orchestration
- RAG / context engineering
- knowledge graphs
- evaluation
- observability
- model routing
- MCP/tool protocols
- identity/authorization
- prompt injection
- inference economics

### Regulation / governance
- AI responsibility/accountability
- data privacy
- model risk
- cybersecurity
- digital lending
- financial crime
- outsourcing / third-party risk
- operational resilience

## Intelligence scoring

Score each discovered item before promoting it to the radar.

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| TCS relevance | none | adjacent | direct |
| BFSI relevance | none | indirect | direct |
| AI relevance | none | adjacent | core |
| Actionability | trivia | useful context | changes learning/design/action |
| Source quality | weak | credible secondary | primary/authoritative |
| Novelty | duplicate | incremental | meaningful new signal |

**Promote to dashboard:** normally 9+/12.

## Update rules

1. Never add duplicate news just to create activity.
2. Prefer event date over crawl/index date.
3. Record source URL and publication date.
4. Separate fact from interpretation.
5. Add a BFSI implication.
6. Add a career/engineering action only when justified.
7. Link the note to at least two relevant Foam notes.
8. If information is uncertain, label confidence explicitly.

## Search patterns

- `site:tcs.com BFSI agentic AI banking insurance`
- `site:tcs.com newsroom AI banking TCS`
- `site:rbi.org.in AI banking model risk cybersecurity`
- `site:sebi.gov.in AI ML circular securities`
- `site:irdai.gov.in AI insurance cybersecurity`
- `agentic AI financial services production governance`
- `banking GenAI evaluation observability regulation`

## Output destination

- breaking/high-value signal → `news/YYYY-MM-DD.md`
- durable knowledge → relevant `tcs/`, `bfsi/`, or `ai/` note
- executive implications → [[dashboards/tcs-bfsi-ai-radar]]
- personal action → [[dashboards/career-visibility]]
