<div align="center">

# Darrshan Govender

### Senior AI Engineer · LLM / RAG · Full-Stack · Data &amp; SQL

[![Available](https://img.shields.io/badge/Available-Fractional%20%2F%20Contract%20%2810%E2%80%9330%20hrs%2Fwk%29-059669?style=for-the-badge)](mailto:darrshangovender@gmail.com)
[![Location](https://img.shields.io/badge/Durban%2C%20South%20Africa-GMT%2B2-1F3A8A?style=for-the-badge)](#)
[![Email](https://img.shields.io/badge/-darrshangovender%40gmail.com-555?style=for-the-badge&logo=gmail&logoColor=white)](mailto:darrshangovender@gmail.com)
[![Website](https://img.shields.io/badge/-agulhascode.co.za-555?style=for-the-badge&logo=safari&logoColor=white)](https://agulhascode.co.za)

</div>

---

I build **LLM-powered products** and **data-driven web platforms**. I run [**Agulhas Code**](https://agulhascode.co.za) — a Durban engineering studio shipping AI features, RAG systems, agentic pipelines, and data engineering for SMEs across South Africa.

Full EMEA timezone overlap. 4 hours of US Eastern overlap. Async-first.

---

### Selected results from production work

<table>
<tr>
<td valign="top" width="33%">

**~94%** &nbsp;benchmark accuracy<br/>
*InsightEngine · NL→SQL · 0 destructive incidents*

</td>
<td valign="top" width="33%">

**Faithfulness > 0.95**<br/>
*RAG Chatbot · Recall@5 > 0.85*

</td>
<td valign="top" width="33%">

**ROC-AUC 0.87**<br/>
*Churn classifier · top-decile precision 0.62*

</td>
</tr>
<tr>
<td valign="top">

**99.9%+ uptime**<br/>
*across live client systems*

</td>
<td valign="top">

**Sub-second queries**<br/>
*from minutes · multi-million-row Postgres*

</td>
<td valign="top">

**Recall@10 = 0.41**<br/>
*Recommender · 0.18 baseline*

</td>
</tr>
</table>

---

### What I'm shipping in production

| Project | What it does | Headline result |
|---|---|---|
| [**InsightEngine**](../../insightengine) | NL→SQL analytics over multi-table warehouses with sqlglot AST guardrails | **~94% accuracy** · **0 destructive incidents** |
| [**RAG Chatbot**](../../rag-chatbot) | Production support bot · hybrid retrieval (cosine + BM25) · citation-guarded | **Faithfulness > 0.95** · **Recall@5 > 0.85** |
| [**Churn &amp; MRR Forecasting**](../../churn-forecasting) | XGBoost churn classifier + Prophet MRR forecast for a SaaS client | **ROC-AUC 0.87** · **Top-decile precision 0.62** |
| [**Recommendation Engine**](../../recommendation-engine) | Hybrid content + collaborative recommender for an e-commerce client | **Recall@10 = 0.41** vs **0.18** baseline |
| [**Lead Scorer**](../../lead-scorer) | B2B lead-ranking with LR baseline + XGBoost ranker, scores pushed to CRM | **Top-decile precision ~0.6** |
| [**Document-Intelligence**](../../doc-intelligence) | OCR → LLM extraction → Pydantic schema validation → human-review queue | Replaces manual data entry |

### Open-source tooling

Reusable patterns extracted from production work, plus the things I wish existed when I started:

| Repo | What it does |
|---|---|
| [**multi-agent-orchestrator**](../../multi-agent-orchestrator) ⭐ | Production-grade multi-agent system · structured Pydantic handoffs · workspace memory · full trace observability |
| [**rag-graph**](../../rag-graph) ⭐ | Knowledge-graph-augmented RAG · LLM entity+relation extraction · hybrid vector + graph retrieval |
| [**rag-eval-harness**](../../rag-eval-harness) | Production evals for RAG · faithfulness, recall@k, latency, cost · runs in CI · gates merges |
| [**prompt-eval-toolkit**](../../prompt-eval-toolkit) | A/B test prompt versions with paired-bootstrap p-values · fail-the-build on regression |
| [**prompt-versioner**](../../prompt-versioner) | Git-style version control for prompts · hash-stable weighted A/B routing · CLI + library |
| [**llm-cost-tracker**](../../llm-cost-tracker) | Token / cost / latency observability per LLM call · SQLite store · CLI for stats |
| [**semantic-cache**](../../semantic-cache) | Production semantic cache for LLM responses · pgvector kNN · saves 30–80% on chatbot workloads |
| [**agent-tool-router**](../../agent-tool-router) | LLM tool-use router · two-stage embedding-then-LLM with explicit refusal fallback |
| [**sql-guardrails**](../../sql-guardrails) | Make LLM-generated SQL safe to execute · sqlglot AST + EXPLAIN cost limits |

---

### Stack

`Python` · `FastAPI` · `TypeScript` · `Next.js` · `PostgreSQL` · `pgvector` · `OpenAI` · `Anthropic` · `LangChain` · `XGBoost` · `scikit-learn` · `Prophet` · `Pydantic` · `AWS` · `Vercel` · `Docker` · `GitHub Actions`

---

### How I work

- **Ship end-to-end** — discovery, architecture, build, deploy, monitor
- **Async-first** — written specs, weekly status updates, comfortable owning ambiguous problems
- **Test what you ship** — every prompt change runs an eval suite before merge
- **Defensive by default** — guardrails, citations, exception queues, read-only roles
- **Treat prompts like code** — versioned, diffable, rollback-able, A/B routable
- **Structured > freeform** — Pydantic at every LLM boundary; fail fast on schema mismatch

---

### GitHub

<a href="https://github.com/darrshangovender">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=darrshangovender&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=false&hide=issues,prs" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=darrshangovender&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />
</a>

---

### Get in touch

📧 [darrshangovender@gmail.com](mailto:darrshangovender@gmail.com) &nbsp;·&nbsp; 🌐 [agulhascode.co.za](https://agulhascode.co.za) &nbsp;·&nbsp; 📍 Durban, South Africa (GMT+2)