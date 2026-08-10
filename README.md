# Asad Aslam

**Data and AI Engineer** based in Nürnberg, Germany.

I have spent the last four years at Siemens working on the supply chain side of things: Python ETL pipelines, Snowflake, supplier name matching with sentence transformers, Power BI reporting, and a Neo4j backed chatbot that lets analysts ask questions in plain English instead of writing Cypher by hand. I finished my MSc in Data Science at FAU Erlangen-Nürnberg in May 2025.

What I publish here is what I build on my own time, mostly agentic LLM systems. I tend to spend my effort on the parts that get skipped: validating generated code before it runs, writing tests that pass without a live model, evaluating honestly instead of eyeballing a few outputs, and making the system admit when it does not know. Everything here is open source and runs locally by default.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-asadaslam556-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/asadaslam556/)
[![Portfolio](https://img.shields.io/badge/Portfolio-asadaslam.tech-4F46E5?style=flat&logo=vercel)](https://asadaslam.tech)
[![Email](https://img.shields.io/badge/Email-asadaslam556%40gmail.com-D14836?style=flat&logo=gmail)](mailto:asadaslam556@gmail.com)

---

## Featured projects

### [prism-data-agent](https://github.com/asadaslam556/prism-data-agent)

An AI data analyst you can ask questions in plain English. It plans an approach, writes the SQL, runs pandas over the results, charts what comes back, then checks its own answer before handing it to you.

- LangGraph handles the multi-agent orchestration, FastAPI serves the backend, React renders the console, and the live reasoning trace streams over SSE so you can watch it think
- Generated SQL is parsed and restricted to a single SELECT or WITH statement before it touches a database
- Generated Python is AST inspected and executed in a sandboxed namespace against a restricted builtins allow-list
- 168 tests with the LLM fully mocked, so CI runs without a model
- Local-first through Ollama, with OpenAI and Anthropic available as drop-in providers
- Docker Compose and GitHub Actions included

`Python` `LangGraph` `FastAPI` `React` `Ollama` `pandas` `SSE` `Docker` `pytest`

### [portfolio](https://github.com/asadaslam556/portfolio) · [asadaslam.tech](https://asadaslam.tech)

My personal site, built as a 3D scene rather than a static page because I wanted to learn React Three Fiber properly. Deployed on Vercel.

`React 18` `Vite` `React Three Fiber` `Tailwind CSS` `Framer Motion` `Vercel`

---

## Work at Siemens

The code below is internal and not public, so there are no repository links. Happy to walk through the architecture and the tradeoffs in a conversation.

### Data Engineer (Working Student) · Siemens AG, Munich
**Jul 2024 – Present**

Building internal data engineering and Gen AI tooling for a tier-n supply chain visibility program.

**Gen AI supply chain chatbot.** A question answering system for supply chain analysts, backed by a Neo4j graph of suppliers, parts, tier-n relationships, and product change notifications. Two-tier query engine: a rule-based intent router with pre-built Cypher templates handles the common questions deterministically, and an Azure OpenAI and LangChain path covers everything else. A read-only safety layer blocks writes before any query reaches the database. Deployed as an Azure ML Managed Online Endpoint inside a Docker container. Correctness is tracked with a regression suite of 150 representative business questions run against the live endpoint, most recently 147 pass, 3 flagged for review, zero failures.

**Supplier and location mapping platform.** A two-workspace Streamlit application on Azure, shipped through GitLab CI/CD. The supplier workspace runs an SBERT model behind a text normalizer that strips legal suffixes across 20+ jurisdictions before matching, auto-locks anything above a 95% confidence threshold, and queues the rest for human review. The location workspace uses the Nominatim OpenStreetMap API with rate limiting and retry logic. Snowflake backend, Plotly dashboards, live Prewave API integration. It manages more than 10,000 supplier name and location records and cut manual mapping by 50% and correction effort by 30–40%.

Alongside those, I run Snowflake warehouse operations and optimize ELT workflows in SQL, write and tune the Cypher behind the graph layer, and integrate REST APIs to enrich supplier and location data automatically.

### Data Analyst (Working Student) · Siemens Mobility, Erlangen
**Jun 2022 – Jun 2024**

Reporting and analytics for operational teams.

**KPI reporting dashboard.** An interactive Power BI platform replacing a manual Excel process for three operational teams. Power Query ETL consolidating six sources including Snowflake and Excel, four dashboard pages covering executive overview, operations, quality, and logistics, and DAX measures for production achievement, on-time delivery, first pass yield, fail rate, budget variance, and average delay days. Cut reporting time by 40–45% and removed roughly 10–15 hours of manual work per week.

**Supplier risk assessment tool.** A Mendix application on Mendix Cloud for the procurement team, replacing a spreadsheet process. Scores 8 risk dimensions per supplier covering financial stability, environmental and social risk, production risk, quality, geopolitical risk, delivery, solvency, and image and compliance. Automated risk classification, a risk share dashboard, a risk/cost matrix, an Excel bulk importer, a currency converter, and role-based user management. 210+ active supplier records in daily use. I wrote the user manual and handed it over to the procurement stakeholders.

### Web Developer · AIMS IT Solutions and Trainings, Lahore
**Jul 2019 – Jan 2021**

Built and shipped several websites, a mobile app, and a set of landing pages. Moved the front end to a mobile-first responsive approach, which raised mobile engagement. Deployed on AWS EC2.

---

## Research and awards

**Data attribution for satellite imagery classification** (University of Bonn)

Which training images actually shaped the model, and can you find the mislabeled ones without looking at every sample? I implemented three attribution methods from scratch on EuroSAT with a ResNet-18 backbone: EL2N, TracIn, and influence functions. Experiments ran on the Bender HPC cluster. All three separated corrupted from clean samples well, with AUROC between 0.967 and 0.997 depending on the method and the corruption rate.

`PyTorch` `ResNet-18` `EuroSAT` `Influence Functions` `TracIn` `EL2N` `HPC`

**Second place, Neo4j Graphathon**

---

## Tech stack

**Languages and data**
`Python` `SQL` `R` `Snowflake` `dbt` `Neo4j` `Cypher` `pandas` `NumPy` `PyTorch` `JSON`

**AI and ML**
`LangChain` `LangGraph` `Azure OpenAI` `Anthropic Claude API` `Ollama` `RAG` `Agentic RAG` `Hybrid retrieval (BM25 + vector)` `Reciprocal rank fusion` `Vector search` `Embeddings` `Sentence Transformers (SBERT)` `LoRA` `PEFT` `Transformers` `GGUF` `LLM-as-judge evaluation` `Prompt engineering` `NLP` `Graph RAG` `Text-to-Cypher`

**Backend and frontend**
`FastAPI` `React` `Vite` `Streamlit` `REST APIs` `SSE streaming` `PWA` `pytest`

**Cloud and DevOps**
`Azure` `Azure ML` `AWS` `Docker` `Docker Compose` `Kubernetes` `GitLab CI/CD` `GitHub Actions`

**Analytics and BI**
`Power BI` `DAX` `Power Query` `Plotly` `NeoDash` `Graph analytics` `Statistical analysis`

**Other**
`Mendix` `Nominatim API` `Prewave API` `Git`

---

## Education

### MSc Data Science
**Friedrich-Alexander University Erlangen-Nürnberg · Oct 2021 – May 2025**

Machine learning, deep learning, NLP, statistical modeling, and data engineering.

Thesis: *Investigating the Role of MicroRNAs and IsomiRs as Biomarkers in Psychiatric Disorders Using Advanced Machine Learning Methods*

### BSc Computer Science
**University of South Asia · Oct 2015 – Jun 2020**

Algorithms, data structures, artificial intelligence, database systems, software engineering, statistics and probability.

Thesis: *Paintex*, an Android app using Google ARCore and machine learning to preview paint colors on real walls before ordering.

---

## Certifications

| Certification | Issuer |
|---|---|
| Neo4j Certified Professional | Neo4j |
| Building Neo4j Applications with Python | Neo4j |
| Microsoft AI Agents: From Foundations to Applications Professional Certificate | Microsoft |
| Microsoft Generative AI for Data Analysis Professional Certificate | Microsoft |
| AWS Certified Cloud Practitioner | AWS |
| Introduction to Generative AI | Google Cloud |
| Rapid Developer Certification | Mendix |
| Python for Data Science, AI & Development | IBM |
| Databases and SQL for Data Science with Python | IBM |

---

## Get in touch

I am looking for **Data Engineer**, **AI Engineer**, and **Analytics Engineer** roles across Germany, and I am open to relocating. Available from September 2026 with a one-month notice period, earlier by agreement.

If something here overlaps with what your team is building, I would be glad to talk about it.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/asadaslam556/)
[![Email](https://img.shields.io/badge/Email-Say%20hello-D14836?style=for-the-badge&logo=gmail)](mailto:asadaslam556@gmail.com)

<!--
==========================================================================
DROP-IN BLOCKS FOR REPOS NOT YET PUSHED.
These are invisible on the rendered profile. When a repo goes public,
cut the block out of this comment and paste it into "Featured projects".
Check the repo name in the link matches what you actually pushed.
==========================================================================

### [agentic-rag-assistant](https://github.com/asadaslam556/agentic-rag-assistant)

A chat assistant that decides which tool to reach for, then proves what it
tells you. It plans across hybrid BM25 and vector search, web search, a
structured catalog lookup, and a calculator, fuses the evidence with
reciprocal rank fusion, streams a cited answer token by token over SSE, and
verifies every individual claim against its sources before the turn counts as
finished. When the evidence is not there, it says so instead of guessing.

- Plan-and-act loop written by hand on a strict JSON protocol, no agent
  framework, which is also what makes a fully deterministic offline mock
  possible for tests and CI
- 66 tests, 58 of which run offline with no model
- Golden-set eval plus an LLM-as-judge mode scoring faithfulness and relevance
- React and Vite console shipped as a PWA, Bearer token auth on the API
- Runs against Ollama, OpenAI, Azure OpenAI, or Anthropic

`Python` `RAG` `BM25` `Vector search` `RRF` `FastAPI` `React` `PWA` `SSE` `Docker`

### [llm-finetune-lab](https://github.com/asadaslam556/llm-finetune-lab)

A runnable LoRA fine-tuning pipeline, end to end. Ingest a support ticket
dataset, dedupe and format it, pull a small base model (Qwen2.5-0.5B-Instruct),
profile the available compute, fine-tune with LoRA through transformers and
peft, evaluate on token-overlap F1 and keyword hit rate, then export to GGUF
and deploy to Ollama.

- Dry-run mode walks all seven stages with no GPU and no downloads, so you can
  iterate on the pipeline itself in seconds
- Real-run mode does the actual training and deployment
- FastAPI backend with a React ops console, 88 tests

`Python` `LoRA` `PEFT` `transformers` `Qwen2.5` `GGUF` `Ollama` `FastAPI` `React`

### [job-apply-pipeline](https://github.com/asadaslam556/job-apply-pipeline)

Job search automation for the German market. A two-step collect then verify
flow that pulls from six ATS providers and the Bundesagentur API, scores each
posting against a profile, reads Gmail for application status, and tracks
everything as an event-sourced log rather than a mutable spreadsheet.

- Corporate sibling guard that stops cross-entity false matches between
  companies with similar names
- Deduplication on a normalized company key
- 116 tests

`Python` `Gmail API` `ATS integrations` `Event sourcing` `pytest`

-->
