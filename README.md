<!-- ============================================================ -->
<!-- HERO SECTION -->
<!-- Purpose: 3-second read. Name, role, one-sentence value prop. -->
<!-- No "Hi I'm" opener, no emoji spam, no buzzwords. -->
<!-- ============================================================ -->

<h1 align="center">Sai Cheranjeeve S</h1>
<h3 align="center">Backend Engineer · AI/ML Systems · Final-Year CS Undergraduate, CUSAT '27</h3>

<p align="center">
I design backend systems that stay correct under real constraints — resource limits, concurrency, and scale — not just in a notebook.
</p>

<!-- ============================================================ -->
<!-- TYPING BANNER -->
<!-- Purpose: rotates real, verifiable facts instead of clichés. -->
<!-- Replace nothing here — every line is already true. -->
<!-- ============================================================ -->

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=20&duration=3000&pause=1200&color=2563EB&center=true&vCenter=true&width=600&lines=Building+fault-tolerant+retrieval+systems;Engineering+concurrency-safe+distributed+backends;Final-year+CS+%40+CUSAT%2C+graduating+2027;Open+to+Software+Engineering+internships" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://linkedin.com/in/sai-cheranjeeve-s-30081129b"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:saicheranjeeves@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

---

<!-- ============================================================ -->
<!-- ABOUT ME -->
<!-- Purpose: what I build, what problems I solve, current focus. -->
<!-- Kept to 4 short lines, no life story. -->
<!-- ============================================================ -->

### About

I build backend systems and applied ML pipelines that hold up under real constraints — a RAG platform tuned to run inside a 512MB, single-core deployment; a resume-evaluation pipeline that processes candidates in parallel batches without blocking; a multi-agent system with a human-in-the-loop review layer instead of full autonomy.

Currently completing my final year of a B.Tech in Computer Science at CUSAT (graduating 2027), and looking for full-time Software Engineering / AI-ML Engineering roles.

---

<!-- ============================================================ -->
<!-- EXPERTISE -->
<!-- Purpose: skills grouped by category, pulled only from resume. -->
<!-- ============================================================ -->

### Expertise

**Languages**
`Python` `Java` `C++` `SQL`

**Backend & Distributed Systems**
`FastAPI` `Django` `Django REST Framework` `Async REST APIs` `Celery` `Redis` `Event-Driven Architecture`

**AI / ML & RAG**
`TensorFlow` `PyTorch` `FAISS` `BM25` `Sentence Transformers` `Cross-Encoder Reranking` `Groq LLM` `Google Gemini API` `ONNX Runtime` `Prompt Engineering`

**Agentic AI**
`LangChain` `Google ADK` `Multi-Agent Orchestration` `HITL / RLHF Pipelines`

**Databases**
`PostgreSQL` `MySQL` `MongoDB` `SQL Server` `ChromaDB`

**Cloud & DevOps**
`AWS (Foundational)` `GCP` `Docker` `Git` `Linux` `Vercel` `Render` `CI/CD`

**Testing**
`Pytest` `Unit Testing` `Integration Testing` `API Contract Testing`

---

<!-- ============================================================ -->
<!-- FEATURED PROJECTS -->
<!-- Purpose: strongest, most defensible work only. -->
<!-- [[REPO LINK]] placeholders — fill in your actual repo URLs. -->
<!-- ============================================================ -->

### Featured Projects

#### Atlan AI — AI Customer Support Copilot
**Problem:** Support teams need fast, accurate answers grounded in real documentation, not hallucinated ones — while keeping infrastructure cost near zero.
**Approach:** Hybrid retrieval combining a FAISS vector index with BM25 lexical search, merged via Reciprocal Rank Fusion and refined with cross-encoder reranking. Deployed on Render's free tier (512MB RAM, single-core CPU), using a SHA-256 query cache for sub-1ms repeat responses.
**Result:** ~20% accuracy improvement over a dense-only baseline (to 90–95%), serving 10–15 concurrent sessions with 700 ingested docs indexed into 2,142 semantic chunks.
**Stack:** `FastAPI` `React 19` `PostgreSQL` `FAISS` `BM25` `Pytest` `Vercel` `Render`
**Repo:** [github.com/Sai-developer-6699/support-copilot-rag](https://github.com/Sai-developer-6699/support-copilot-rag)

#### AegisHire AI — Intelligent Applicant Tracking System
**Problem:** Manual resume screening doesn't scale, and naive automation introduces race conditions when multiple evaluations run in parallel.
**Approach:** Django REST Framework backend with an async Celery/Redis pipeline batching up to 50 candidates per run, and database-level row locking to prevent concurrent-evaluation collisions.
**Result:** Architected to scale to 10,000+ candidate profiles across 4 role-based access tiers; throughput analysis projects a 90%+ cut in active screening time per hiring cycle.
**Stack:** `Django 5` `DRF` `MySQL` `Redis` `Celery` `Google Gemini API`
**Repo:** [github.com/Sai-developer-6699/AegisHire](https://github.com/Sai-developer-6699/AegisHire)

#### NeuroTutor — AI-Powered Adaptive Learning Platform
**Problem:** Fixed-pace flashcard drilling doesn't adapt to what a learner actually needs to review.
**Approach:** Bloom's Taxonomy-based question selection paired with SM-2 spaced repetition, served through async Django (ADRF) APIs with Groq-backed LLM streaming and a ChromaDB RAG layer grounding answers in course material.
**Result:** Currently in active trial with 10 students and 2 teachers via the college placement office; backend load-tested at 20 concurrent interview sessions with automated GPU failover.
**Stack:** `Django 5` `ADRF` `React 19` `ChromaDB` `PostgreSQL` `Redis` `Groq (Llama 3.3 70B)`
**Repo:** [github.com/Sai-developer-6699/Neurobots](https://github.com/Sai-developer-6699/Neurotutor)

#### RetentionX — Autonomous Customer Lifecycle Agent Mesh
**Problem:** Fully autonomous agents making customer-facing decisions is risky without a human checkpoint.
**Approach:** A mesh of 5 specialized subagents (orchestrator, adoption analyst, dynamic pricing, outreach copywriter, compliance auditor) built on Google ADK principles, with a Streamlit human-in-the-loop review queue feeding an RLHF training loop, plus a cross-tenant registry for cold-start learning.
**Result:** Reached the finals among ~30 teams in a live hackathon showcase.
**Stack:** `Python` `React 19` `LangChain` `Google ADK` `OpenAI GPT-4o-mini` `Gemini 1.5 Flash`
**Repo:** [github.com/Sai-developer-6699/RetentionX](https://github.com/Sai-developer-6699/RetentionX)

#### SentinAI — Context-Aware Notification Manager (Android)
**Problem:** Notification overload, without sending anything to a server (privacy-sensitive by nature).
**Approach:** A 7-stage on-device filtering pipeline combining heuristic rules, a quantized DistilBERT model via ONNX Runtime, and foreground-app context.
**Result:** ~65% reduction in notification volume during testing, at 45–60ms on-device inference latency, 100% local — no data ever leaves the device.
**Stack:** `Kotlin` `Jetpack Compose` `ONNX Runtime` `Room DB`
**Repo:** [github.com/Sai-developer-6699/AI-notification-manager](https://github.com/Sai-developer-6699/AI-notification-manager)

---

<!-- ============================================================ -->
<!-- ENGINEERING PHILOSOPHY -->
<!-- Purpose: shows how I think, derived from actual decisions -->
<!-- made across the projects above — not a motivational quote. -->
<!-- ============================================================ -->

### Engineering Philosophy

Constraints are a design input, not an afterthought — Atlan AI's architecture came from deploying inside a 512MB free tier, not from adding limits after the fact. Systems that act autonomously need a way to be stopped or corrected before they act, not just audited after — that shaped RetentionX's human-in-the-loop queue as a core component, not a bolt-on. And a system that fails should fail safe: the drift-detection layer at Mirrorfolio was built specifically so an uncertain model defers to a rule-based safety net rather than guessing.

---

<!-- ============================================================ -->
<!-- CURRENT FOCUS -->
<!-- Purpose: what's active right now — keeps profile from feeling stale. -->
<!-- ============================================================ -->

### Current Focus

- Finishing final year of B.Tech Computer Science at CUSAT (graduating 2027)
- Running an active trial of NeuroTutor with real students and teachers
- Interviewing for full-time Software Engineering and AI/ML Engineering roles

---

<!-- ============================================================ -->
<!-- TIMELINE -->
<!-- Purpose: career progression at a glance, factual only. -->
<!-- ============================================================ -->

### Timeline

| Year | Milestone |
|---|---|
| 2022 | School topper, Amrita Vidyalayam (96%) |
| 2023 | Started B.Tech Computer Science, CUSAT |
| 2024 | Software Development Intern, Softronics |
| 2025 | ML Intern, EBTS · Software Development Intern, Safe Integrated Solutions · Research Intern, ACARR (CUSAT) |
| 2026 | ML Intern, Mirrorfolio (current) · Built Atlan AI, AegisHire AI, NeuroTutor, RetentionX, SentinAI |
| 2027 | Graduating — seeking full-time SDE / AI-ML Engineer roles |

---

<!-- ============================================================ -->
<!-- GITHUB ANALYTICS -->
<!-- Purpose: standard, trusted widgets. No fake metrics. -->
<!-- ============================================================ -->

### GitHub Analytics

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Sai-developer-6699&show_icons=true&theme=default&hide_border=true" alt="GitHub Stats" width="48%" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sai-developer-6699&layout=compact&theme=default&hide_border=true" alt="Top Languages" width="48%" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Sai-developer-6699&theme=default&hide_border=true" alt="GitHub Streak" width="96%" />
</p>

---

<!-- ============================================================ -->
<!-- OPEN SOURCE -->
<!-- Purpose: honest placeholder — no fabricated contributions. -->
<!-- ============================================================ -->

### Open Source

No public contributions listed yet. Interested in retrieval-augmented generation tooling and agent-orchestration frameworks, given hands-on experience building both from scratch.

---

<!-- ============================================================ -->
<!-- CERTIFICATIONS -->
<!-- Purpose: real credentials only. -->
<!-- ============================================================ -->

### Certifications

- Distributed Systems — NPTEL, IIT
- Large Language Models — NPTEL, IIT
- Information Retrieval — NPTEL, IIT
- AWS Skill Builder — Foundational Badges
- Google Cloud Skills Boost — Multiple Badges

---

<!-- ============================================================ -->
<!-- ACHIEVEMENTS -->
<!-- ============================================================ -->

### Achievements

- 1st Place — Vismayam Ideathon
- Finalist — CodeSprint, Neurobots, HackNight 2.0
- Excellent Student Award (Leadership & Academics)
- School Topper, Class of 2022

---

<!-- ============================================================ -->
<!-- CONTACT -->
<!-- Purpose: only real, confirmed profiles. -->
<!-- ============================================================ -->

### Contact

📧 [saicheranjeeves@gmail.com](mailto:saicheranjeeves@gmail.com)
💼 [LinkedIn](https://linkedin.com/in/sai-cheranjeeve-s-30081129b)
💻 [GitHub](https://github.com/Sai-developer-6699)
