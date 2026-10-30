<p><a href="https://darrshangovender.github.io">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/darrshangovender/darrshangovender/main/assets/banner-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/darrshangovender/darrshangovender/main/assets/banner-light.svg">
    <img src="https://raw.githubusercontent.com/darrshangovender/darrshangovender/main/assets/banner-light.svg" alt="Darrshan Govender, AI engineer. Industrial AI, built to be evaluated, audited and trusted. Predictive maintenance, knowledge assistants, supervised agents." width="100%">
  </picture>
</a></p>

I build AI systems that engineering and operations teams can defend. My current focus is heavy industry: predictive maintenance, knowledge assistants that answer only from controlled documents, and agents that draft work and stop for human approval before anything is acted on. I run [Agulhas Code](https://agulhascode.co.za), an AI engineering studio in Durban.

The featured repositories run offline by default with no API keys, state what their results were measured on, and list their limitations. Where the data is synthetic or the model is simulated, the README says so.

**[See it run → darrshangovender.github.io](https://darrshangovender.github.io)**: replay a pump failing in the asset-health fleet report, then try to push an unsafe work order past maintenance-agent's approval gate. Both are driven by the repositories' own output.

## Industrial AI

<p><picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/darrshangovender/darrshangovender/main/assets/pipeline-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/darrshangovender/darrshangovender/main/assets/pipeline-light.svg">
  <img src="https://raw.githubusercontent.com/darrshangovender/darrshangovender/main/assets/pipeline-light.svg" alt="Flow diagram. Sensor data feeds asset-health, which raises an alert with a remaining-useful-life interval. plant-copilot supplies the cited procedure with its safety clause quoted verbatim. maintenance-agent drafts a work order, a rule-based verifier checks it, and it is held at a human approval gate until a person approves. Reference flow: each repository runs on its own, on synthetic data." width="100%">
</picture></p>

A reference flow, not an integrated product: asset-health raises the alert, plant-copilot supplies the controlled procedure, and maintenance-agent drafts the work order and waits for a person. They share no code and have not been tested together. All data is synthetic and labelled as such, so the results describe the method, not a plant.

### [asset-health](https://github.com/darrshangovender/asset-health)

Predictive maintenance for mining and processing assets: regime-aware anomaly detection, remaining useful life with an uncertainty interval, cost-aware alerting and structured work-order recommendations. Runs on a seeded synthetic fleet.<br>
**Result:** On 80 held-out synthetic failures: 79 warned 3+ days ahead vs 70 for the better of two tuned fixed-limit baselines, at about two-thirds of that baseline's illustrative cost. Still ahead when failure signatures are scaled to 30%; behind at 15%, and the README shows that curve.

### [plant-copilot](https://github.com/darrshangovender/plant-copilot)

Bilingual Arabic and English assistant for SOPs and HSE procedures. Answers only from controlled documents, cites the exact clause and revision, applies access control before retrieval, and refuses when the answer is not there.<br>
**Result:** 0 access-control leaks in 4,603 probes; safety-critical clauses quoted verbatim in 64 of 64 answers against a simulated model; 68% correct on held-out questions it was never tuned on. Synthetic corpus.

### [maintenance-agent](https://github.com/darrshangovender/maintenance-agent)

Supervised maintenance-planning agent. Takes an asset-health alert, retrieves the relevant procedures with citations, drafts a work order, checks it with a rule-based safety verifier, and stops at a human approval gate. Every tool call is logged and replayable.<br>
**Result:** Blocked 99.5% of seeded unsafe drafts, with the six it misses listed; 0 of 55 correct drafts wrongly blocked; 15 of 15 approval-gate bypass attempts refused. Each number states what it cannot show.

<p><a href="https://github.com/darrshangovender/asset-health"><img src="https://raw.githubusercontent.com/darrshangovender/darrshangovender/main/assets/report-asset-health.png" alt="Top of the asset-health fleet report: a synthetic-data notice, a fleet status table with remaining-useful-life intervals, and the fused anomaly score for a cyclone feed pump rising through its alert threshold before an injected failure. Synthetic data." width="100%"></a></p>

<sub>Top of asset-health's self-contained fleet report on its seeded synthetic fleet. The full report also shows the work order it drafts.</sub>

## LLM infrastructure

Cost, safety and reliability controls that sit around a model.

| Repository | What it does | Key result |
|---|---|---|
| **[cascade](https://github.com/darrshangovender/cascade)** | Verifier-gated model cascade: answer with the cheapest model first, escalate only when verification fails, fit the thresholds offline. Benchmarked on a simulated model. | Counts every verifier call, priced from the list prices in the repo. On the simulated benchmark a 2-tier cascade is 5% cheaper at 99% of the strong model's accuracy; the 3-tier one costs more, and the README shows why. |
| **[context-compress](https://github.com/darrshangovender/context-compress)** | Prompt and RAG context compression with a fact-recall evaluator, so savings are reported next to what was lost. | On a synthetic RAG set: 48% fewer tokens with every fact kept, where naive truncation saves 57% but keeps 21.7%. |
| **[guardrail](https://github.com/darrshangovender/guardrail)** | Safety gateway for model inputs and outputs: prompt-injection detection, PII redaction, groundedness checks and structured-output repair behind one policy layer. | On the held-out test splits of two public datasets (whose training splits informed its patterns): 59.6% of 193 labelled attacks flagged, 0 false alarms on 178 benign prompts. Saudi National ID/Iqama, IBAN and mobile detection with checksums. |
| **[sql-guardrails](https://github.com/darrshangovender/sql-guardrails)** | Makes LLM-written SQL safe to execute: sqlglot AST allowlisting, read-only enforcement and optional EXPLAIN cost limits. Ships an adversarial corpus. | Executes only the guard's own normalised SQL, so a parser disagreement between guard and database cannot become a bypass. 22 functions blocked permanently, beyond the reach of config. |
| **[mcp-gateway](https://github.com/darrshangovender/mcp-gateway)** | MCP server wrapper with API-key auth, tenant isolation, per-tool guardrails, rate limits and an audit log. Serves the 2026-07-28 MCP revision and the 2025 revisions side by side. | STRIDE threat model; 253 tests |
| **[agent-runtime](https://github.com/darrshangovender/agent-runtime)** | Checkpointed state-machine executor for agents: resume after a crash, identical-call loop breaker, model fallback chain, schema self-correction. | Design reference; no headline number |
| **[thinking-loop](https://github.com/darrshangovender/thinking-loop)** | Published test-time reasoning strategies behind one interface, adjudicated by a critic, under hard token, time and cost budgets. | Benchmark harness; a real-model run needs your own key |
| **[rag-eval-harness](https://github.com/darrshangovender/rag-eval-harness)** | Faithfulness, answer relevance and recall@k for RAG pipelines, wired into CI so a regression fails the build. | A CI gate, not a benchmark |

## Domain work

- **[lease-abstract](https://github.com/darrshangovender/lease-abstract)**: South African residential lease abstraction with per-field clause citations and compliance checks against the Rental Housing Act and the Consumer Protection Act.
- **[affordability-scorer](https://github.com/darrshangovender/affordability-scorer)**: explainable tenant affordability scoring with tamper detection, calibration and structural fairness checks. No LLM in the scoring path.
- **[whatsapp-agent-kit](https://github.com/darrshangovender/whatsapp-agent-kit)**: WhatsApp Business agents with webhook dedup, the session window rule, human handoff and POPIA-aware redaction. Runs offline against a mock transport.

**Also:** [multi-agent-orchestrator](https://github.com/darrshangovender/multi-agent-orchestrator) · [rag-graph](https://github.com/darrshangovender/rag-graph) · [rag-chatbot](https://github.com/darrshangovender/rag-chatbot) · [doc-intelligence](https://github.com/darrshangovender/doc-intelligence) · [insightengine](https://github.com/darrshangovender/insightengine) · [agent-tool-router](https://github.com/darrshangovender/agent-tool-router) · [semantic-cache](https://github.com/darrshangovender/semantic-cache) · [llm-cost-tracker](https://github.com/darrshangovender/llm-cost-tracker) · [prompt-versioner](https://github.com/darrshangovender/prompt-versioner) · [prompt-eval-toolkit](https://github.com/darrshangovender/prompt-eval-toolkit) · [lead-scorer](https://github.com/darrshangovender/lead-scorer) · [churn-forecasting](https://github.com/darrshangovender/churn-forecasting) · [recommendation-engine](https://github.com/darrshangovender/recommendation-engine)

## How I work

- **Offline by default.** Tests, examples and benchmarks need no API keys and no network. Hosted-model paths are optional extras, so data can stay inside the client environment.
- **Every number has a script.** Results are regenerated by a script in the repository and say what they were measured on: synthetic data, a simulated model, or a bundled corpus.
- **Controls sit outside the model.** Rule-based verifiers, AST allowlists, access control before retrieval and human approval gates, not instructions in a prompt.
- **Limitations are written down.** Each README has a Limitations section that says what changes on real data.

## Contact

Available for contract and fractional work. I am in Durban (UTC+2), one hour behind Riyadh, so the working day overlaps almost entirely with Gulf hours.

[darrshangovender.github.io](https://darrshangovender.github.io) · [agulhascode.co.za](https://agulhascode.co.za) · darrshangovender@gmail.com
