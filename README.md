# Hi, I'm Asad Aslam 👋

Data and AI Engineer with 3+ years at Siemens building production ETL/ELT pipelines, managing Snowflake data warehouse operations, and deploying Gen AI solutions on Azure. My work sits at the intersection of data engineering and applied AI – turning messy supply-chain data into tools that people actually use every day.

---

## 🚀 What I Build

- **Gen AI systems** that convert natural language into graph database queries (Neo4j + Azure OpenAI + LangChain)
- **ETL/ELT pipelines** in Python running on GitLab CI/CD with ML-based entity matching (SBERT)
- **Streamlit applications** deployed on Azure managing 10,000+ supplier records
- **Snowflake data warehouse** operations and ELT workflow optimization at enterprise scale
- **Power BI dashboards** with advanced DAX models for real-time KPI tracking

---

## 🔧 Tech Stack

**Languages & Databases**
`Python` `SQL` `Snowflake` `dbt` `Neo4j` `R`

**Cloud & DevOps**
`Azure` `AWS` `GitLab CI/CD` `Docker` `Kubernetes`

**AI & ML**
`LangChain` `Azure OpenAI` `Sentence Transformers (SBERT)` `NLP` `LLMs` `Prompt Engineering`

**Analytics & BI**
`Power BI` `DAX` `Power Query` `Streamlit` `NeoDash`

---

## 📂 Featured Projects

### [TinaGPT – Gen AI Supply Chain Chatbot](https://github.com/asadaslam556/tinagpt)
A domain-specific question-answering system for Siemens supply-chain analysts. Users ask questions in plain English and get answers drawn directly from a Neo4j graph database covering suppliers, parts, tier-n relationships, and product change notifications.

- Two-tier query engine: rule-based intent router with pre-built Cypher templates + Azure OpenAI/LangChain fallback
- Safety layer blocks all write operations before execution
- Tested against 109 representative questions before production deployment
- Deployed as an **Azure ML Managed Online Endpoint** inside a Docker container

`Python` `Neo4j` `Azure OpenAI` `LangChain` `Docker` `Azure ML`

---

### [TIERN MappingHub – Supplier and Location Data Platform](https://github.com/asadaslam556/tiern-mappinghub)
A two-workspace Streamlit application deployed on Azure via GitLab CI/CD, built for the TIERN supply chain visibility program at Siemens.

- **Supplier Mapping:** SBERT model with multi-jurisdiction legal suffix cleaner (20+ jurisdictions), 95% confidence threshold for auto-locking, human review queue for low-confidence matches – reduced manual mapping by **50%**
- **Location Mapping:** Nominatim OpenStreetMap API with rate limiting and retry logic
- Snowflake backend, Plotly dashboards, Prewave API integration
- Managing 10,000+ supplier name and location records, reducing manual correction effort by **30–40%**

`Python` `Streamlit` `Snowflake` `SBERT` `GitLab CI/CD` `Azure` `REST APIs`

---

## 📊 GitHub Stats

![Asad's GitHub Stats](https://github-readme-stats.vercel.app/api?username=asadaslam556&show_icons=true&theme=tokyonight&hide_border=true)

---

## 🎓 Education & Certifications

- **MSc Data Science** – Friedrich-Alexander University Erlangen-Nürnberg (2021–2025)
- **BSc Computer Science** – University of South Asia (2015–2020)
- Neo4j Certified Professional
- AWS Certified Cloud Practitioner
- Microsoft AI Agents Professional Certificate
- Microsoft GenAI for Data Analysis Professional Certificate
- Introduction to Generative AI – Google Cloud

---

## 📫 Get in Touch

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Asad%20Aslam-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/asadaslam556/)
[![Email](https://img.shields.io/badge/Email-asadaslam556%40gmail.com-D14836?style=flat&logo=gmail)](mailto:asadaslam556@gmail.com)

---

*Open to Data Engineer, AI Engineer, and Analytics Engineer roles across Germany. Available from June 2026.*
