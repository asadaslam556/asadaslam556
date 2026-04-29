# Hi, I'm Asad Aslam 👋

**Data & AI Engineer** based in Nürnberg, Germany. Over the past 3+ years at Siemens I have built production ETL/ELT pipelines in Python, managed Snowflake data warehouse operations, and deployed Gen AI solutions on Azure. My work sits at the intersection of data engineering, analytics, and applied AI — turning messy supply-chain data into tools that people actually use every day.

I completed my MSc in Data Science at Friedrich-Alexander University Erlangen-Nürnberg in 2025 and am currently looking for full-time Data Engineer, AI Engineer, or Analytics Engineer roles across Germany.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Asad%20Aslam-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/asadaslam556/)
[![Email](https://img.shields.io/badge/Email-asadaslam556%40gmail.com-D14836?style=flat&logo=gmail)](mailto:asadaslam556@gmail.com)
[![Location](https://img.shields.io/badge/Location-Nürnberg%2C%20Germany-lightgrey?style=flat)](https://www.linkedin.com/in/asadaslam556/)

---

## 🚀 What I Build

- **Gen AI systems** that convert natural language into Neo4j Cypher queries using Azure OpenAI and LangChain, deployed as Azure ML Managed Online Endpoints
- **ETL/ELT pipelines** in Python running on GitLab CI/CD with ML-based supplier name matching using Sentence Transformers (SBERT)
- **Streamlit applications** deployed on Azure for reviewing and managing 10,000+ supplier name and location records
- **Snowflake data warehouse** operations and ELT workflow optimization at enterprise scale for supply-chain analytics
- **Power BI dashboards** with advanced DAX models eliminating 10–15 hours of manual reporting work per week
- **Low-code applications** in Mendix covering multi-dimensional supplier risk assessment across 210+ active suppliers

---

## 🔧 Tech Stack

**Languages & Databases**
`Python` `SQL` `Snowflake` `dbt` `Neo4j` `R` `JSON`

**Cloud & DevOps**
`Microsoft Azure` `AWS` `Azure ML` `GitLab CI/CD` `Docker` `Kubernetes`

**AI & ML**
`LangChain` `Azure OpenAI` `Sentence Transformers (SBERT)` `NLP` `LLMs` `Prompt Engineering` `PyTorch` `Pandas` `NumPy`

**Analytics & BI**
`Power BI` `DAX` `Power Query` `Streamlit` `NeoDash` `Graph Analytics` `Statistical Analysis`

**Other**
`REST APIs` `Mendix` `Plotly` `Nominatim API` `Prewave API`

---

## 💼 Work Experience

### Data Engineer (Working Student) — Siemens AG, Munich
**Jul 2024 – Present**

Part of the TIERN (Tier-N supply chain visibility) team at Siemens AG, building internal data engineering and Gen AI tools for supplier mapping and supply chain analytics.

- Build Python ETL pipelines with GitLab CI/CD, using a Sentence Transformers (SBERT) model to automatically match supplier names from multiple source systems, reducing manual mapping by **50%**
- Develop and deploy a Streamlit application on Azure for reviewing and managing over 10,000 supplier name and location mappings, reducing manual correction effort by roughly **30–40%**
- Manage Snowflake data warehouse operations, optimizing ELT workflows using SQL to improve pipeline efficiency for enterprise-scale supply-chain analytics
- Integrate REST APIs to automatically enrich supply-chain supplier and location data, reducing manual lookup effort across 10,000+ records
- Develop and optimize Neo4j Cypher queries for supply-chain data retrieval, forming the graph database layer behind a Gen AI chatbot
- Build and deploy a Gen AI chatbot in Python that converts supply-chain questions in natural language into Neo4j Cypher queries, using Azure OpenAI and LangChain, deployed as an Azure ML API endpoint

---

### Data Analyst (Working Student) — Siemens Mobility, Erlangen
**Jun 2022 – Jun 2024**

Supporting the BI and analytics function at Siemens Mobility, delivering reporting tools and data workflows for operational teams.

- Designed interactive Power BI dashboards for real-time KPI tracking, used across 3 operational teams
- Developed ETL workflows with Power Query to consolidate data from 6 diverse sources including Snowflake and Excel, ensuring consistent data quality
- Developed advanced DAX analytical models, reducing manual reporting time by roughly **40–45%**
- Automated KPI reporting processes, eliminating roughly **10–15 hours** of manual work per week
- Built a supplier risk assessment application in Mendix covering 8 risk dimensions per supplier, with automated risk classification, a Risk Share dashboard, and an Excel importer for bulk data upload, deployed to Mendix Cloud

---

### Web Developer (Full-time) — AIMS IT Solutions and Trainings, Lahore
**Jul 2019 – Jan 2021**

- Implemented a responsive, mobile-first approach that increased mobile user engagement
- Led the end-to-end development of multiple websites, a mobile app, and several landing pages
- Deployed web applications on AWS EC2, achieving high uptime and reducing maintenance costs

---

## 📂 Featured Projects

### [TinaGPT — Gen AI Supply Chain Chatbot](https://github.com/asadaslam556/tinagpt)
**Mar 2026 – Present | Associated with Siemens AG**

A domain-specific question-answering system for Siemens supply-chain analysts. Users ask questions in plain English and get answers drawn directly from a Neo4j graph database covering suppliers, parts, tier-n relationships, and product change notifications.

- Two-tier query engine: rule-based intent router with pre-built Cypher templates + Azure OpenAI/LangChain fallback for everything else
- Safety layer blocks all write operations (DELETE, CREATE, MERGE) before any query executes
- Tested against **109 representative questions** before production deployment (75 auto-scored, 100% pass rate)
- Deployed as an **Azure ML Managed Online Endpoint** inside a Docker container

`Python` `Neo4j` `Azure OpenAI` `LangChain` `Docker` `Azure ML` `Cypher` `Prompt Engineering`

---

### [TIERN MappingHub — Supplier and Location Data Platform](https://github.com/asadaslam556/tiern-mappinghub)
**Jan 2025 – Mar 2026 | Associated with Siemens AG**

A two-workspace Streamlit application deployed on Azure via GitLab CI/CD for the TIERN supply chain visibility program at Siemens.

**Supplier Mapping Workspace:**
- SBERT model with custom text normalizer stripping legal suffixes across 20+ jurisdictions before matching
- 95% confidence threshold for auto-locking; human review queue for lower-confidence matches
- Reduced manual mapping by **50%**

**Location Mapping Workspace:**
- Nominatim OpenStreetMap API with rate limiting and retry logic
- High-confidence matches auto-locked, rest queued for human review

**Infrastructure:** Snowflake backend, Plotly dashboards, live Prewave API integration. Managing 10,000+ records, reducing correction effort by **30–40%**

`Python` `Streamlit` `Snowflake` `SBERT` `GitLab CI/CD` `Azure` `Nominatim` `REST APIs` `Plotly`

---

### TCP Risk Management — Supplier Risk Assessment Tool
**Jun 2022 – Jun 2024 | Associated with Siemens Mobility**

A Mendix application deployed to Mendix Cloud for the procurement team at Siemens Mobility Erlangen, replacing a fully manual Excel-based process.

- Tracks **8 risk dimensions** per supplier: financial stability, environmental and social risk, production risk, quality, geopolitical risk, delivery, solvency, and image and compliance
- Features: multi-dimensional risk scoring forms, automated risk classification, Risk Share dashboard, Risk/Cost Matrix, Excel importer, currency converter, role-based user management
- **210+ active supplier records** in daily operational use
- Wrote the complete user manual and handed over to procurement stakeholders

`Mendix` `Mendix Cloud` `Low-Code Development` `Business Process Automation`

---

### KPI Reporting Dashboard
**Jun 2022 – Jun 2024 | Associated with Siemens Mobility**

An interactive Power BI reporting platform replacing manual Excel-based KPI tracking for three operational teams at Siemens Mobility Erlangen.

- Consolidated data from 6 sources using Power Query ETL workflows (Snowflake, Excel, manual tracking sheets)
- Built 4 dashboard pages: Executive KPI Overview, Operations, Quality, and Logistics
- Advanced DAX measures covering production achievement, on-time delivery, first pass yield, fail rate, budget variance, and average delay days
- Eliminated **10–15 hours** of manual reporting per week, reducing reporting time by **40–45%**

`Power BI` `DAX` `Power Query` `Snowflake` `ETL/ELT` `Data Visualization`

---

## 🎓 Education

### MSc Data Science
**Friedrich-Alexander University Erlangen-Nürnberg | Oct 2021 – May 2025 | Grade: 2.8**

Focus on machine learning, deep learning, natural language processing, statistical modeling, and data engineering.

Thesis: *Investigating the Role of MicroRNAs and IsomiRs as Biomarkers in Psychiatric Disorders Using Advanced Machine Learning Methods*

---

### BSc Computer Science
**University of South Asia | Oct 2015 – Jun 2020 | CGPA: 3.41/4.0**

Coursework: algorithms, data structures, artificial intelligence, database management systems, software engineering, statistics and probability.

Thesis: *Paintex — Android application using Google ARCore augmented reality and machine learning to visualize paint colors on walls in real time before ordering*

---

## 📜 Certifications

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

## 📊 GitHub Stats

![Asad's GitHub Stats](https://github-readme-stats.vercel.app/api?username=asadaslam556&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=asadaslam556&layout=compact&theme=tokyonight&hide_border=true)

---

## 📫 Get in Touch

Open to **Data Engineer**, **AI Engineer**, and **Analytics Engineer** roles across Germany. Available from June 2026 with a one-month notice period, earlier by agreement.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/asadaslam556/)
[![Email](https://img.shields.io/badge/Email-asadaslam556%40gmail.com-D14836?style=for-the-badge&logo=gmail)](mailto:asadaslam556@gmail.com)
