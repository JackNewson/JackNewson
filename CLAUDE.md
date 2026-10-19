# Core memory

Standing instructions from Jack. Apply these in every session on this repo.
Recorded 2026-10-19.

## 1. Sol 6.1 routing: hand over to Oliver

"Sol 6.1" is OpenAI's GPT-6.1 Sol (ChatGPT/API, launched at DevDay 2026-09-29).

Rule: for every area where Sol 6.1 is more economical or performs better than
Claude (Sonnet 5.5 / Opus 5.5), hand that work to **Oliver** through the **den
chat (AgentxAgent)** instead of doing it here.

Areas that currently qualify:

| Area | Evidence | Confidence |
|---|---|---|
| Cost-sensitive work run at medium/high reasoning effort | Artificial Analysis index at medium effort: Sol 48 vs Sonnet 5.5 41; Sol also ahead of Sonnet at high effort | Medium |
| Automation-style agentic tasks at medium effort | AutomationBench medium: Sol 31.7% at $0.19/task vs 29.5% at $0.65/task (compared against Opus 5.5) | Medium |
| Questions over complex PDFs | GDP.pdf: Sol 31.0% vs 25.8% | Low (single benchmark) |
| Cost per task vs Opus 5.5 where the quality gap is acceptable | Terminal-Bench Science: Sol 57.0% at $5.47/task vs Opus 63.3% at $23.21/task | Medium |
| Cached-input-heavy workloads | One aggregator lists Sol cache reads at $0.10/1M vs $0.20 for Claude | Low (unverified) |

Keep on Claude, do not hand over:
- Max-effort quality (index: Opus 5.5 58, Sonnet 5.5 56, Sol 52)
- Terminal and agentic coding (Terminal-Bench 4.0 favors Claude in most independent runs)
- Knowledge-work tasks such as GDPval-AA (Sonnet 1840 vs Sol 1575)

Caveats to pass along with every handoff:
- Figures come from secondary sources (aggregators and blogs); the primary
  OpenAI and Artificial Analysis pages could not be opened.
- Vendor-reported and independent benchmark runs disagree.
- No data found on latency, multimodal/vision, writing quality, or tool-use
  reliability. Do not assume Sol wins there.
- Re-check this table when new benchmarks land or pricing changes.

## 2. Extra checks and tests: run in parallel

Whenever checks or tests are run here, also run the matching additional
checks and tests in parallel on the Sol 6.1 side (via Oliver), so results can
be compared on cost and quality. Do not block on them; report both sets
together.

## 3. Open tasks

Every open task carries rule 1 and rule 2 above. When creating or updating a
task, add them to the description.

## Status (2026-10-19)

- Handoff to Oliver NOT yet delivered: no reachable agent named Oliver and no
  den chat / AgentxAgent channel was found from this environment. See the open
  task for what is needed.
