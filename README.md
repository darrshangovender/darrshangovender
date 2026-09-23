<a href="https://agulhascode.co.za">
  <img src="https://raw.githubusercontent.com/darrshangovender/darrshangovender/main/banner.svg" alt="Darrshan Govender — AI engineer. LLM systems: cheaper, faster, safer." width="100%"/>
</a>

### AI engineer. I make LLM systems cheaper, faster, and safer.

I build production LLM infrastructure — inference routing, context compression, evaluation harnesses, and safety gateways — and I publish the tooling as open source with reproducible benchmarks.

Independent, remote, available for contract and fractional work (10–30 hrs/week).
**Durban, South Africa · UTC+2** — full overlap with EU/UK, four hours with US Eastern.

---

### Selected work

Every number below is reproduced by a script in its repo. Clone it and run `python benchmarks/run.py` — offline, no API keys.

| Project | The problem it solves | Result |
|---|---|---|
| **[cascade](https://github.com/darrshangovender/cascade)** | You pay frontier prices for every query, but most queries are easy. | Verifier-gated model cascade: **94% of the strongest model's accuracy at 34% lower cost**, 1.69 model calls/query. |
| **[thinking-loop](https://github.com/darrshangovender/thinking-loop)** | A single LLM call is the entire reasoning surface most apps use, even on hard questions. | Five published test-time strategies + critic adjudicator: **92.5% vs a 67.5% single-call baseline** on a 40-question set. |
| **[context-compress](https://github.com/darrshangovender/context-compress)** | Retrieved RAG context is mostly padding, and truncation silently destroys the answer. | **48% fewer tokens at 100% fact recall** — measured, because truncation scores 57% savings at 21.7% recall. |
| **[guardrail](https://github.com/darrshangovender/guardrail)** | Most LLM features validate neither the prompt going in nor the answer coming out. | Injection detection, PII redaction, groundedness checks: **100% detection at 0% false positives** on the bundled corpus. |

Those four compose into one thesis about inference economics: **route to the cheapest model that will get it right, spend more compute only when the question is hard, shrink the input to every call, and validate both ends.**

---

### Also open source

- [**agent-runtime**](https://github.com/darrshangovender/agent-runtime) — checkpointed state-machine executor for agents: resume after a crash, break identical-call loops, fall back across models
- [**mcp-gateway**](https://github.com/darrshangovender/mcp-gateway) — MCP server with API-key auth, tenant isolation, per-tool guardrails, rate limits and an audit log
- [**whatsapp-agent-kit**](https://github.com/darrshangovender/whatsapp-agent-kit) — WhatsApp Cloud API agents: webhook dedup, the 24-hour window, human handoff, POPIA redaction
- [**multi-agent-orchestrator**](https://github.com/darrshangovender/multi-agent-orchestrator) — typed Pydantic handoffs between agents, workspace memory, full trace observability
- [**rag-graph**](https://github.com/darrshangovender/rag-graph) — knowledge-graph-augmented retrieval; hybrid vector kNN + graph BFS for multi-hop questions
- [**rag-eval-harness**](https://github.com/darrshangovender/rag-eval-harness) — faithfulness, recall@k, latency and cost, wired into CI so a prompt change can't merge on a regression
- [**sql-guardrails**](https://github.com/darrshangovender/sql-guardrails) — sqlglot AST allowlisting so LLM-written SQL can't drop a table
- [**semantic-cache**](https://github.com/darrshangovender/semantic-cache) · [**llm-cost-tracker**](https://github.com/darrshangovender/llm-cost-tracker) · [**prompt-versioner**](https://github.com/darrshangovender/prompt-versioner) — the cost and reliability plumbing

Domain work for [LeasEase](https://leasease.co.za), the rental-trust startup I founded — South African law, built to run offline:

- [**lease-abstract**](https://github.com/darrshangovender/lease-abstract) — lease clause extraction with per-field citations, compliance checks against the Rental Housing Act and CPA, plain-English summaries for both parties
- [**affordability-scorer**](https://github.com/darrshangovender/affordability-scorer) — explainable tenant affordability scoring with tamper detection, calibration and a fairness audit; no LLM in the scoring path (POPIA)

---

### How I work

Structured outputs at every model boundary. Evals in CI that block a merge on regression. Guardrails by default — citation enforcement, AST allowlists, human-review queues. Cost and latency attributed per call.

Frameworks turn over every six months; that discipline doesn't. It's also why every repo here ships a benchmark you can re-run rather than a number you have to take on faith.

Through [**Agulhas Code**](https://agulhascode.co.za) I've shipped this into production: ~94% accuracy on a natural-language-to-SQL layer over a live warehouse with zero destructive incidents, a RAG assistant at >0.95 faithfulness, and report queries cut from minutes to sub-second on multi-million-row Postgres.

---

### Working together

**Architecture review** — a week with your team, mapping the AI surface. You get a written report and a 30-day plan.
**Contract build** — scoped LLM features, RAG systems, evals. Discovery through shipped and monitored.
**Fractional AI lead** — 10–30 hrs/week, embedded. I own the roadmap, the prompt discipline, and the eval gates.

📧 **darrshangovender@gmail.com** · 🌐 **[agulhascode.co.za](https://agulhascode.co.za)**
