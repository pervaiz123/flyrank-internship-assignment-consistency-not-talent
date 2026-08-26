# Agent Build Log: ML Research Scout

## 1. Initial Build Goal vs Final MVP

* **Initial Spec (FL-06):** Complex multi-tool pipeline querying arXiv API, scraping GitHub search endpoints, generating Pydantic schemas, and calling external LLMs via paid API keys.
* **Final MVP Executed:** Autonomous Python agent connecting directly to the live arXiv REST API, parsing feed XML, executing scoring heuristics, and auto-generating structured Markdown briefings locally.

---

## 2. Iteration Chronology

| Hour Window | Focus Area | What Happened & What Broke | Resolution / Decision |
| :--- | :--- | :--- | :--- |
| **Hours 1–2** | Environment & API Setup | `requests` library dependency issues when running in basic Python environments. | Switched to native `urllib.request` to ensure zero-dependency portability. |
| **Hours 3–4** | Live Tool Connection | arXiv API returned nested Atom XML feeds with complex namespace tags (`{http://www.w3.org/2005/Atom}`). | Implemented explicit namespace mapping dictionary in `xml.etree.ElementTree`. |
| **Hours 5–6** | GitHub API Integration | GitHub Search API hit strict unauthenticated rate limits (HTTP 403) during bulk title searches. | **Cut from Scope:** Scoped out direct GitHub code matching to avoid credential dependency; fallback to direct paper link tracking. |
| **Hours 7–8** | Triaging & Scoring Logic | Keyword matching initially flagged irrelevant theoretical math papers with a high score. | Refined signal dictionary to target deployment/optimization tokens (`quantization`, `llm`, `throughput`). |
| **Hours 9–10** | Execution & Output Formatting | File IO created relative path errors depending on where the CLI script was executed from. | Anchored file saving via `Path(__file__).parent` to guarantee consistent file writes to `docs/`. |

---

## 3. Deviations from FL-06 Specification

1. **GitHub Code Extraction:** Deferred to v2. Unauthenticated GitHub API calls caused unpredictable rate limits.
2. **LLM Dependency:** Replaced external API wrapper with a deterministic keyword heuristic and text slicing pipeline to ensure offline reliability and instantaneous execution.

---

## 4. Verification Check

* **Live Tool Connection:** Verified (Calls `export.arxiv.org` REST API).
* **Local Workspace Access:** Verified (Writes `docs/daily_paper_briefing.md`).
* **End-to-End Execution:** Runs cleanly from start to finish via `python work/agent/ml_scout.py`.
