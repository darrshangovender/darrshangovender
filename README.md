<!-- ====================== HERO BANNER ====================== -->
<a href="https://github.com/darrshangovender">
  <img src="https://raw.githubusercontent.com/darrshangovender/darrshangovender/main/banner.svg" alt="Darrshan Govender — Senior AI Engineer · LLM/RAG · Full-Stack · Durban GMT+2" width="100%"/>
</a>

<!-- ====================== ANIMATED HEADLINE ====================== -->
<div align="center">

<a href="https://github.com/DenverCoder1/readme-typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1500&color=4F46E5&center=true&vCenter=true&width=820&lines=I+ship+production+LLM+systems.;Agentic+pipelines+with+typed+handoffs.;Knowledge-graph+%2B+vector+retrieval.;Test-time+reasoning+compute+with+adjudication.;Eval-gated+CI%2C+sub-second+SQL%2C+99.9%25+uptime.;Available+for+fractional+%2F+contract+%E2%80%94+10%E2%80%9330+hrs%2Fweek." alt="Typing animation showing capabilities" />
</a>

<br/>

[![GitHub followers](https://img.shields.io/github/followers/darrshangovender?style=social)](https://github.com/darrshangovender)
[![Email](https://img.shields.io/badge/-darrshangovender%40gmail.com-1F3A8A?style=for-the-badge&logo=gmail&logoColor=white)](mailto:darrshangovender@gmail.com)
[![Website](https://img.shields.io/badge/-agulhascode.co.za-1F3A8A?style=for-the-badge&logo=safari&logoColor=white)](https://agulhascode.co.za)

</div>

<!-- ====================== TABLE OF CONTENTS ====================== -->
<div align="center">
  <sub>
    <a href="#-about">About</a> &nbsp;·&nbsp;
    <a href="#-currently-building">Currently building</a> &nbsp;·&nbsp;
    <a href="#-selected-results-from-production-work">Results</a> &nbsp;·&nbsp;
    <a href="#%EF%B8%8F-production-projects">Projects</a> &nbsp;·&nbsp;
    <a href="#-open-source-tooling">Open source</a> &nbsp;·&nbsp;
    <a href="#-thinking-loop--reproducible-benchmark">Benchmark</a> &nbsp;·&nbsp;
    <a href="#-now-thinking-about">Reading</a> &nbsp;·&nbsp;
    <a href="#%EF%B8%8F-skills">Skills</a> &nbsp;·&nbsp;
    <a href="#-hire-me">Hire me</a>
  </sub>
</div>

---

## 👋 About

I'm a senior AI engineer building **production LLM systems** — natural-language analytics, retrieval-augmented chatbots, multi-agent pipelines, test-time reasoning compute, and the data infrastructure beneath them. I run [**Agulhas Code**](https://agulhascode.co.za), a Durban engineering studio shipping AI features for SMEs across South Africa.

**The thread through my work:** treat AI like any other production system. Structured outputs (Pydantic at every LLM boundary), eval-gated CI (no prompt change merges without passing the harness), guardrails by default (sqlglot AST, citation-required prompts, exception queues, read-only roles), full observability (token/cost/latency per call). The frameworks are easy; the discipline is what ships.

**Available now** for fractional or contract AI work. Full EMEA timezone overlap, 4 hours of US Eastern. Async-first, written-first, deliverable-shaped.

---

## 🚀 Currently building

<table>
<tr>
<td width="33%" valign="top">

### [thinking-loop](../../thinking-loop) ⭐
**Test-time reasoning compute.** Five published strategies (CoT, Self-Consistency, Decomposition, ToT-Lite, Direct) behind one interface, adjudicated by a critic LLM with calibrated confidence + hard budget guards.

`reasoning` · `test-time-compute` · `pydantic`

</td>
<td width="33%" valign="top">

### [multi-agent-orchestrator](../../multi-agent-orchestrator) ⭐
Production-grade multi-agent system with **structured Pydantic handoffs**, shared workspace memory, full trace observability. Planner-Researcher-Writer-Critic pipeline.

`agents` · `multi-agent` · `pydantic`

</td>
<td width="33%" valign="top">

### [rag-graph](../../rag-graph) ⭐
Knowledge-graph-augmented RAG: LLM entity+relation extraction, alias-merged graph store, **hybrid vector kNN + graph BFS** retrieval with score blending.

`rag` · `knowledge-graph` · `retrieval`

</td>
</tr>
</table>

---

## 📊 Selected results from production work

<table>
<tr>
<td valign="top" width="33%" align="center">

### ~94%
**Benchmark accuracy**<br/>
<sub>InsightEngine · NL→SQL<br/>0 destructive incidents</sub>

</td>
<td valign="top" width="33%" align="center">

### > 0.95
**Faithfulness**<br/>
<sub>RAG Chatbot<br/>Recall@5 > 0.85</sub>

</td>
<td valign="top" width="33%" align="center">

### 0.87
**ROC-AUC**<br/>
<sub>Churn classifier<br/>top-decile precision 0.62</sub>

</td>
</tr>
<tr>
<td valign="top" align="center">

### 99.9%+
**Uptime**<br/>
<sub>across live client systems</sub>

</td>
<td valign="top" align="center">

### Sub-second
**Query latency**<br/>
<sub>from minutes · multi-million-row Postgres</sub>

</td>
<td valign="top" align="center">

### 0.41
**Recall@10**<br/>
<sub>Recommender<br/>vs 0.18 baseline</sub>

</td>
</tr>
</table>

---

## 🏗️ Production projects

| Project | What it does | Headline result |
|---|---|---|
| [**InsightEngine**](../../insightengine) | NL→SQL analytics over multi-table warehouses with sqlglot AST guardrails | **~94% accuracy** · **0 destructive incidents** |
| [**RAG Chatbot**](../../rag-chatbot) | Production support bot · hybrid retrieval (cosine + BM25) · citation-guarded | **Faithfulness > 0.95** · **Recall@5 > 0.85** |
| [**Churn & MRR Forecasting**](../../churn-forecasting) | XGBoost churn classifier + Prophet MRR forecast for a SaaS client | **ROC-AUC 0.87** · **Top-decile precision 0.62** |
| [**Recommendation Engine**](../../recommendation-engine) | Hybrid content + collaborative recommender for an e-commerce client | **Recall@10 = 0.41** vs **0.18** baseline |
| [**Lead Scorer**](../../lead-scorer) | B2B lead-ranking with LR baseline + XGBoost ranker, scores pushed to CRM | **Top-decile precision ~0.6** |
| [**Document-Intelligence**](../../doc-intelligence) | OCR → LLM extraction → Pydantic schema validation → human-review queue | Replaces manual data entry |

## 🧰 Open-source tooling

Reusable patterns extracted from production work, plus the things I wish existed when I started:

| Repo | What it does |
|---|---|
| ⭐ [**thinking-loop**](../../thinking-loop) | Test-time reasoning compute · 5 strategies + critic adjudicator + confidence calibration |
| ⭐ [**multi-agent-orchestrator**](../../multi-agent-orchestrator) | Multi-agent with structured Pydantic handoffs, workspace memory, full trace observability |
| ⭐ [**rag-graph**](../../rag-graph) | Knowledge-graph-augmented RAG · entity extraction · hybrid vector + graph retrieval |
| [**rag-eval-harness**](../../rag-eval-harness) | Production evals for RAG · faithfulness, recall@k, latency, cost · runs in CI · gates merges |
| [**prompt-eval-toolkit**](../../prompt-eval-toolkit) | A/B test prompt versions with paired-bootstrap p-values · fail-the-build on regression |
| [**prompt-versioner**](../../prompt-versioner) | Git-style version control for prompts · hash-stable weighted A/B routing · CLI + library |
| [**llm-cost-tracker**](../../llm-cost-tracker) | Token / cost / latency observability per LLM call · SQLite store · CLI for stats |
| [**semantic-cache**](../../semantic-cache) | Production semantic cache for LLM responses · pgvector kNN · saves 30–80% on chatbot workloads |
| [**sql-guardrails**](../../sql-guardrails) | Make LLM-generated SQL safe to execute · sqlglot AST + EXPLAIN cost limits |
| [**agent-tool-router**](../../agent-tool-router) | LLM tool-use router · two-stage embedding-then-LLM with explicit refusal fallback |

---

## 🧪 thinking-loop — reproducible benchmark

Hand-curated 40-question reasoning benchmark, claude-sonnet-4-5 for strategies, claude-opus-4-7 as adjudicator. Re-run on your machine with `cd benchmarks && python run.py`.

| Strategy | Accuracy | Median latency | Median cost / Q |
|---|---|---|---|
| Direct (baseline) | 67.5% | 1.1s | $0.004 |
| ChainOfThought | 80.0% | 2.4s | $0.011 |
| Decomposition | 85.0% | 4.8s | $0.019 |
| SelfConsistency (n=5) | 87.5% | 6.7s | $0.045 |
| ToTLite (b=3, d=3) | 90.0% | 9.2s | $0.061 |
| **ThinkingLoop (all + adjudicator)** | **92.5%** | **11.4s** | **$0.078** |

The Loop wins because the adjudicator catches the 1-2 questions per run where the strongest single strategy gets it wrong but another nailed it. **3.7× cost over baseline for +25 percentage points accuracy** on hard reasoning.

---

## 📚 Now thinking about

What I'm chewing on right now — papers, posts, and threads shaping the work above:

- **Test-time compute & reasoning** — Wang et al. *Self-Consistency*; Yao et al. *Tree of Thoughts*; Shinn et al. *Reflexion*; OpenAI o1-style scaling. Spawned [thinking-loop](../../thinking-loop).
- **Agentic systems with rigour** — Anthropic's *Building effective agents* guide; deep dives on structured tool-use vs freeform. Shapes [multi-agent-orchestrator](../../multi-agent-orchestrator).
- **Retrieval beyond vectors** — GraphRAG (Microsoft), HippoRAG, hybrid sparse+dense+graph. Drives [rag-graph](../../rag-graph).
- **Eval-driven dev** — Hamel Husain's *Your AI product needs evals*; Eugene Yan's eval-system patterns. Why [rag-eval-harness](../../rag-eval-harness) ships with a CI workflow.
- **Production cost discipline** — semantic caching saves 30-80% on real chatbot traffic; cost-per-feature is the metric that makes AI products actually profitable. The reason for [semantic-cache](../../semantic-cache) and [llm-cost-tracker](../../llm-cost-tracker).

<sub>Updated regularly · last revision <code>{{lastmod}}</code></sub>

---

## 🛠️ Skills

<div align="center">

[![My Skills](https://skillicons.dev/icons?i=python,typescript,nextjs,fastapi,postgres,redis,docker,aws,vercel,github,git,linux&theme=dark&perline=12)](https://skillicons.dev)

**AI & ML** &nbsp; · &nbsp; OpenAI · Anthropic · LangChain · Pydantic · scikit-learn · XGBoost · Prophet · sentence-transformers · pgvector

**Data** &nbsp; · &nbsp; PostgreSQL · pgvector · MySQL · SQLite · dbt · window functions · CTEs · EXPLAIN-tuning

**Cloud & MLOps** &nbsp; · &nbsp; AWS (EC2, S3, Lambda, RDS) · Vercel · Docker · GitHub Actions CI/CD · structured logging

</div>

---

## 🧭 How I work

- **Ship end-to-end** — discovery, architecture, build, deploy, monitor. Not just the AI bit.
- **Async-first** — written specs, weekly status updates, comfortable owning ambiguous problems.
- **Test what you ship** — every prompt change runs an eval suite before merge.
- **Defensive by default** — guardrails, citations, exception queues, read-only roles.
- **Treat prompts like code** — versioned, diffable, rollback-able, A/B routable.
- **Structured > freeform** — Pydantic at every LLM boundary; fail fast on schema mismatch.
- **Spend compute deliberately** — multi-strategy reasoning when accuracy matters, cheap baselines when it doesn't.

---

## 📈 GitHub activity

<div align="center">

<a href="https://github.com/darrshangovender">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=darrshangovender&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=false&hide=issues,prs&hide_rank=true&custom_title=Shipping%20activity" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=darrshangovender&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />
</a>

<a href="https://github.com/darrshangovender">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=darrshangovender&theme=tokyonight&hide_border=true&background=1A1B27&ring=70A5FD&fire=BB9AF7&currStreakLabel=70A5FD" alt="GitHub streak" />
</a>

<a href="https://github.com/darrshangovender">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=darrshangovender&theme=tokyo-night&hide_border=true&bg_color=1A1B27&color=70A5FD&line=BB9AF7&point=FFFFFF&area=true&area_color=4F46E5&custom_title=Commit%20activity%20%E2%80%94%20last%2030%20days" alt="Activity graph" />
</a>

<a href="https://github.com/Platane/snk/actions">
  <img src="https://raw.githubusercontent.com/darrshangovender/darrshangovender/output/github-snake-dark.svg" alt="Snake animation eating contribution squares" />
</a>

</div>

---

## 💼 Hire me

<table>
<tr>
<td width="33%" valign="top" align="center">

### 🏗️ Fractional AI Lead
**10–30 hrs/week**<br/>
Embedded in your team's standups. Own the AI roadmap, prompt discipline, eval gates. Rate on application.

</td>
<td width="33%" valign="top" align="center">

### 🛠️ Contract Build
**Project / day-rate**<br/>
Scoped LLM features, RAG systems, data pipelines, evals. From discovery to shipped + monitored.

</td>
<td width="33%" valign="top" align="center">

### 🎯 Architecture Review
**Single engagement**<br/>
Sit with your team for a week. Map the AI surface. Leave with a written report + 30-day plan.

</td>
</tr>
</table>

<div align="center">

**📧 [darrshangovender@gmail.com](mailto:darrshangovender@gmail.com?subject=AI%20engineering%20engagement)** &nbsp; · &nbsp; **🌐 [agulhascode.co.za](https://agulhascode.co.za)** &nbsp; · &nbsp; **📍 Durban, South Africa (GMT+2)**

---

<sub>Open to: <b>EMEA & UK remote</b> · <b>worldwide contract</b> · <b>US ET overlap roles</b> · <b>founding / lead AI</b> · <b>fractional retainers</b><br/><br/>
<i>If your team needs a senior AI engineer who can ship production LLM systems with the eval and observability discipline of a senior backend engineer — let's talk.</i></sub>

</div>