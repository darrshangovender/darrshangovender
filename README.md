# Hi — I'm Darrshan 👋

**AI Engineer · LLM / RAG · Full-Stack · Data & SQL · Durban, South Africa (GMT+2)**

I build LLM-powered products and data-driven web platforms. I run [Agulhas Code](https://agulhascode.co.za), a Durban-based engineering studio, and I'm the technical lead on [LeasEase](#leasease), an AI-driven property-tech platform.

> **Available** for fractional / contract AI engagements (10–30 hrs/week). Full EMEA timezone overlap, 4-hour US ET overlap.

---

## Production projects

| Project | What it is |
|---|---|
| **[InsightEngine](insightengine)** | Natural-language SQL analytics over a multi-table warehouse. ~94% accuracy on benchmark business questions, 0 destructive incidents. |
| **[RAG Chatbot](rag-chatbot)** | Production support chatbot. Hybrid retrieval (cosine + BM25), citation-guarded responses, faithfulness eval. |
| **[Churn & MRR Forecasting](churn-forecasting)** | XGBoost churn classifier + Prophet MRR forecast for a SaaS client. ROC-AUC 0.87, top-decile precision 0.62. |
| **[Recommendation Engine](recommendation-engine)** | Hybrid content + collaborative recommender for an e-commerce client. Recall@10 = 0.41 vs 0.18 baseline. |
| **[Lead Scorer](lead-scorer)** | B2B lead-ranking. XGBoost + LR baseline for trust. Top-decile precision held at ~0.6 in production. |
| **[Document-Intelligence Pipeline](doc-intelligence)** | OCR → LLM extraction → schema validation → Postgres for invoices and statements. Exception queue + human-in-the-loop few-shot store. |

## Open-source tooling

The reusable patterns from the production work, extracted as standalone libraries:

| Repo | What it does |
|---|---|
| **[rag-eval-harness](rag-eval-harness)** | Production-grade evals for RAG systems. Faithfulness, answer relevance, retrieval recall@k, latency, cost. Runs in CI, gates merges. |
| **[prompt-eval-toolkit](prompt-eval-toolkit)** | A/B test prompt versions on a dataset. Bootstrap p-values, single-number verdict, fail-the-build on regression. |
| **[agent-tool-router](agent-tool-router)** | Small, well-evaluated tool-use router. Two-stage embedding-then-LLM routing with explicit refusal. |
| **[sql-guardrails](sql-guardrails)** | Make LLM-generated SQL safe to execute. sqlglot AST parsing, EXPLAIN cost limits, deny-by-default allowlists. |

## Stack I reach for first

- **AI / LLM** — OpenAI, Anthropic, LangChain, RAG, embeddings, pgvector, evals
- **ML** — scikit-learn, XGBoost, pandas/NumPy, Prophet
- **Backend** — Python (FastAPI), Node.js, PostgreSQL, MySQL, Redis
- **Frontend** — Next.js, React, TypeScript, Tailwind
- **Cloud / Ops** — AWS (EC2, S3, Lambda, RDS), Vercel, Docker, GitHub Actions

## How I work

- Ship end-to-end — discovery, architecture, build, deploy, monitor.
- Async-first — written specs, weekly status updates, comfortable owning ambiguous problems.
- Test what you ship — every prompt change runs an eval suite before merge.
- Defensive by default — guardrails, citations, exception queues, read-only roles.

## Get in touch

- 📧 darrshangovender@gmail.com
- 🌐 [agulhascode.co.za](https://agulhascode.co.za)
- 📍 Durban, South Africa (GMT+2)
