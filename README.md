# Projects - Lewis Muguna

This portfolio showcases my end-to-end expertise in Data Science, AI Engineering, and Data Infrastructure, featuring projects developed through professional engagements, academic research, and independent innovation. Each project highlights my ability to design scalable, cloud-native AI systems, perform data-driven analysis, and build intelligent automation solutions that solve real-world problems.

It serves as a living record of my achievements, technical growth, and certifications, and is regularly updated with new projects that reflect the latest advancements in Machine Learning, Generative AI, and MLOps.

📧 Email: lewiemuguna417@gmail.com

🔗 LinkedIn: www.linkedin.com/in/lewis-muguna-070080166

## Projects

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Muguna_Portfolio/blob/main/catalog-sentinel.png?raw=true"> **[Catalog Sentinel: Agentic Catalog Verification for Music Distribution](https://github.com/lewis-hue/catalog-sentinel.git)**

▶ **[Watch the demo walkthrough](https://github.com/lewis-hue/Lewis_Muguna_Portfolio/blob/main/catalog-sentinel-demo.mp4)** (a real catalog audit, from connect to drafted fix)

Catalog Sentinel is a production-grade agentic workflow that tells independent musicians where their music is actually live across roughly 28 stores, and turns every confirmed gap into a ready-to-send fix.

It is not a scraper. Catalog Sentinel is a full-stack, verification-first system that connects to an artist's own distributor account through an attended, read-only cloud browser, reads the entire catalog, confirms real store presence, verifies lyrics per store, quantifies catalog health, and drafts evidence-backed support tickets, all with a human in the loop at every consequential step.

Built end-to-end as a TypeScript monorepo, the system runs as cooperating cloud services: a Next.js Backend-for-Frontend with a React frontend, a Fastify API, BullMQ and Redis background workers, PostgreSQL with Prisma, a Steel cloud browser driven by Playwright over CDP, Keycloak OIDC identity with Google federation, and AWS KMS envelope encryption.

<br clear="left"/>

✨ **Core Features: The Catalog Integrity Engine**

🎧 **Real-Browser Catalog Extraction**

Catalog Sentinel reads ground truth from a live browser instead of trusting a "delivered" flag.

- Attended, read-only Steel cloud-browser session signed in by the artist, with no passwords or 2FA ever stored.
- Playwright-over-CDP DOM reader for catalogs that expose no JSON API.
- Durable, checkpointed pipeline: catalog-index, plan-chunks, release-chunk, retry-failed, reconcile, finalize.
- Resumes mid-scan after a crash instead of restarting.
- Field-level provenance that separates source absence from extraction failure.

🛡️ **Verification-First Store Presence**

Every release is checked across the stores with evidence, never a guess.

- Per-store DSP adapters for Spotify, Tidal, Deezer, Apple/iTunes, Audiomack, SoundCloud, and YouTube.
- Serper web-search confirmation for stores without a usable API.
- Identity matching that confirms a hit is really the artist's release, not a same-titled track by someone else.
- Every result classified live, missing, or unverifiable, so a rate-limited store never becomes a false "not live".

🎤 **Per-Store Lyrics Coverage and One-Click Fixer**

- Store-by-store lyric availability checks.
- A one-click fixer for closing lyric and metadata gaps.
- Uncertain items routed to a human-approved manual review queue.

🩺 **A Single Catalog Health Score**

- One weighted score across metadata completeness, store presence, artist identity, and lyric coverage.
- A transparent breakdown that quantifies exactly what is driving the number.

🎫 **Evidence-Backed Support Tickets**

- Auto-drafted, ready-to-send distributor support tickets for missing releases.
- Exact track titles and ISRCs included, with CSV evidence export for the full audit.
- Drafted, never sent, until the artist approves.

🔔 **Change Detection and Release Alerts**

- Diff-based comparison between audits, backed by a full audit history.
- Release alerts when something that was live goes missing, so a disappearance never stays invisible.

🔐 **Production Security and Identity**

- Keycloak OIDC with Authorization Code plus PKCE and a confidential BFF client.
- AWS KMS envelope encryption for session state, with jose-signed JWS gates.
- Append-only hash-chained audit records and S3 Object Lock anchors.
- Fail-closed configuration with no hardcoded secrets.

☁️ **Cloud-Native Architecture**

- Local Docker Compose stack, plus an AWS single-instance deploy behind Caddy auto-HTTPS.
- A two-AZ ECS, Aurora, and ElastiCache production reference under infra/aws.
- GitHub Actions CI/CD with typecheck, lint, and a 751-test suite gating every deploy.

🚀 **Engineering Scope**

Catalog Sentinel demonstrates end-to-end ownership across agentic workflow design, browser automation, backend architecture, verification and reliability engineering, security, and cloud operations. It connects a real problem faced by independent artists with a durable, human-in-the-loop system that produces evidence a user can act on, reducing a full day of manual store-by-store checking to about ten minutes.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/katibaai/blob/main/Landing%20page.png?raw=true"> **[KATIBA AI: AI-Powered Kenyan Constitution Assistant](https://github.com/lewis-hue/katibaai.git)**

Katiba AI is a production-grade Retrieval-Augmented Generation platform built to make the Constitution of Kenya easier to understand, search, and reason about through natural-language conversation.

It is not just a chatbot. Katiba AI is a full-stack civic intelligence system that combines constitutional document retrieval, AI-generated answers, article-level citations, streamed responses, workspace collaboration, subscription billing, identity management, usage analytics, and secure cloud deployment.

Built end-to-end, the system runs as a multi-service cloud architecture with a React/Vite frontend, FastAPI backend services, Gemini-powered embeddings and generation, Milvus vector search, MongoDB persistence, Redis pub/sub, Keycloak authentication, Lago metering, Stripe checkout, and M-Pesa STK Push payments.

<br clear="left"/>

✨ **Core Features: The Constitutional Intelligence Engine**

🏛️ **Retrieval-Augmented Constitutional Q&A**

Katiba AI grounds every answer in retrieved constitutional evidence instead of relying on generic model memory.

- Constitution of Kenya chunked by legal hierarchy: chapter, article, clause, and section.
- Gemini embeddings stored in Milvus for high-speed semantic retrieval.
- Top-K constitutional evidence retrieved before every answer.
- Article-aware citations generated from retrieved source material.
- Hallucination checks ensure cited articles appear in the retrieved evidence.
- Evidence panel shows the constitutional grounding behind the assistant’s answer.

⚡ **Real-Time Streamed AI Chat**

The platform delivers a polished conversational experience with token-by-token streaming.

- Server-Sent Events for live assistant responses.
- Markdown rendering with clean typography.
- Inline constitutional citations.
- Clickable article references.
- Chat history and URL-synced conversations.
- Read-aloud support, voice input, notes, feedback, branching, and public shared chats.

🏢 **Workspace Collaboration**

Katiba AI supports team-based usage for higher-tier users.

- Owner, admin, member, and viewer roles.
- Workspace-level tier inheritance.
- Shared chats and shared files.
- Invite links with expiring tokens.
- Per-member usage analytics.
- Owner/admin-only billing and usage controls.
- Backend-enforced role-based access control.

💳 **Subscription, Billing, and Payments**

The system includes a dedicated billing service for monetization and usage management.

- Stripe Checkout for card payments.
- Safaricom Daraja M-Pesa STK Push for mobile money payments.
- Lago for metered subscriptions and usage events.
- SendGrid for transactional billing emails.
- Canonical backend-owned plan definitions.
- Webhook handling for Stripe, Lago, and M-Pesa.
- Keycloak role synchronization after payment and cancellation.

🔐 **Production Security and Identity**

Katiba AI uses Keycloak as the identity provider and applies security controls across the stack.

- Email/password login and Google SSO.
- JWT verification with RS256 and JWKS.
- Public issuer validation for production OIDC correctness.
- CSRF protection for mutating requests.
- Redis-based rate limiting.
- Hashed public share tokens.
- CORS allow-listing.
- Audit logs for sensitive workspace, invite, share, and billing actions.
- Secrets managed through Google Secret Manager.

☁️ **Cloud-Native Architecture**

The system is deployed on Google Cloud with separate services for clean domain boundaries and safer operations.

- React frontend on Cloud Run.
- Core AI/chat API on Cloud Run.
- Billing API on Cloud Run.
- Keycloak auth proxy on Cloud Run.
- Stateful infrastructure on Compute Engine.
- MongoDB for users, chats, messages, workspaces, usage, and audit logs.
- Milvus for vector search.
- Redis for SSE pub/sub, rate limiting, session cache, and workspace context.
- Cloud Build CI/CD with Artifact Registry and revision-based rollback.

📊 **Analytics and Operational Readiness**

Katiba AI includes production-grade observability and analytics.

- Usage ledger for user and workspace consumption.
- Workspace analytics with member-level breakdowns.
- Structured JSON logs.
- Health endpoints for backend dependencies.
- Cloud Logging integration.
- Cloud Run revision rollback strategy.
- Clear scale path toward managed Redis, managed MongoDB, and dedicated vector infrastructure.

🚀 **Engineering Scope**

Katiba AI demonstrates end-to-end ownership across AI engineering, backend architecture, frontend product engineering, authentication, billing, security, DevOps, and cloud infrastructure.

The project reflects principal-level system design by connecting a real civic use case with a reliable RAG pipeline, production SaaS architecture, secure identity, monetization, collaboration, and scalable cloud operations.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Anagum-coder/blob/main/logo.png"> **[ANAGUM-CODER: The Blueprint-First Agentic Platform](https://github.com/lewis-hue/Anagum-coder.git)**

ANAGUM-CODER is not just another autocomplete tool. It is a revolutionary VS Code Integrated Development Environment (IDE) Layer that transforms coding from simple text generation into intelligent system architecture.

Designed for high-performance engineering teams, Anagum eliminates "AI Spaghetti Code" by enforcing Template-First Development. It combines advanced multi-agent orchestration, cost-optimized model routing (SLMs + LLMs), and a self-healing compilation loop to ensure that every line of code generated is production-grade, secure, and structurally sound. 

✨ Core Features: The Backend Brain
🏗️ Template-First RAG (The Blueprint Engine)
Most agents hallucinate folder structures. Anagum retrieves them from a curated Knowledge Base of Enterprise Blueprints.

Universal Blueprints: Access pre-validated architectural patterns:
Enterprise SaaS: RBAC, query boundaries, decoupled APIs.
Headless E-commerce: Cart logic, payment gateways (Stripe), ISR.
Data Agents: Task queues (Celery/BullMQ), SSE, Vector storage.
AST-Based Indexing: We index templates by Abstract Syntax Tree (structure), not just keywords, ensuring the AI understands how components fit together.
Blueprint Validation: Automatic checks to ensure new code adheres to the selected architecture (e.g., "No direct DB calls in Client Components").

🤖 Multi-Agent Orchestration ("The Tri-Core")

We decouple the workload into specialized agents to mimic a real engineering team, all orchestrated via **high-performance REST APIs** for seamless IDE integration:

@Architect: Analyzes the prompt, selects the Blueprint, drafts a TODO.md plan.
@Coder: Implements the logic file-by-file based on the Architect's specs.
@Linter (The Supervisor): The "Bad Cop." It runs your local compiler/linter. If the code fails type-checking, the Supervisor rejects it and forces the Coder to fix it before you see it.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Agentic-Viral-Video-Orchestrator/blob/main/AVVO%20System%20Overview.png"> **[Agentic Viral Video Orchestrator (AVVO)](https://github.com/lewis-hue/Agentic-Viral-Video-Orchestrator.git)**

**Agentic Viral Video Orchestrator (AVVO)** is a multi-agent **AI automation system** that autonomously discovers viral trends, generates short-form videos, and distributes them across multiple social media platforms.  
Built using **Python (FastAPI)** to deliver **production-ready REST APIs** for the backend and **React + TypeScript** for the frontend, AVVO integrates **LangChain**, **Gemini 2.5-Flash**, and **FAISS** for intelligent content generation and retrieval.  
The system leverages **Celery** and **Redis** for task scheduling and parallel processing, **Cloudinary** for media storage and public video URLs, **Zapier Webhooks** for seamless automation triggers, and **Buffer API** for automated publishing workflows.  
Additional integrations with **OpenAI**, **Vertex AI Veo**, and **Google TTS** enable generative video synthesis and narration.  
The solution runs on **Dockerized infrastructure**, backed by **PostgreSQL**, and deploys via **AWS/GCP** with **CI/CD pipelines** managed through **GitHub Actions**.  
AVVO’s architecture is designed for **scalability**, **continuous optimization**, and **real-time feedback loops**, making it a **robust API-driven AI system** for teams aiming to scale viral content creation through automation and machine learning.

#
**[AI Job Outreach Automation: Autonomous Executive-Assistant Job Sourcing](https://github.com/lewis-hue/AI-Job-Outreach-Automation.git)**

An enterprise-grade automation system that turns a full job-outreach pipeline into one autonomous workflow. It scrapes postings across multiple job boards, validates quality roles through multi-tier filtering and AI confidence scoring, generates personalized outreach messages with an LLM using several professional templates, and syncs everything to a Google Sheets dashboard for sales-team review and application tracking. Built on a Python FastAPI backend with APScheduler for daily and interval-based runs, async scraping with rate limiting, and a React and TypeScript dashboard for launching scrapes, reviewing jobs, generating messages, and exporting to CSV or JSON.

**Skills and tools:** Python, FastAPI, APScheduler, LLM message generation, Google Sheets API, async processing, React, TypeScript, Tailwind CSS.

#
**[Outreach Automation: LangGraph Multi-Step Outreach Pipeline](https://github.com/lewis-hue/outreach-automation.git)**

A LangGraph-based outreach pipeline that models scraping, validation, and LLM-driven message generation as a graph of composable, independently testable steps. It uses LangChain for model calls, Pydantic models for validated data structures at every stage, and LangSmith tracing for run-level observability, making the outreach workflow auditable and straightforward to extend.

**Skills and tools:** Python, LangGraph, LangChain, LangSmith, Pydantic, agentic pipeline design.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/REVIEWS-HQ/blob/main/flex.webp"> **[Reviews HQ - AI-Powered Property Management Analytics Platform](https://github.com/lewis-hue/REVIEWS-HQ.git)**

Reviews HQ is an AI analytics platform for property management, offering real-time sentiment analysis. It streamlines guest communication with AI response suggestions, live translation, and voice-to-text. The high-performance stack uses a **FastAPI-driven REST API backend** with Groq LLM, a React 18 frontend, and MongoDB Atlas, deployed scalably via Docker on Google Cloud Run.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/download%20(1).jpg"> **[Agentic Plan Workbench: LLM-Powered Red Teaming for Function Calls](https://github.com/lewis-hue/Agentic-Plan-Workbench.git)**

This production-grade, full-stack web application serves as an interactive development environment (IDE) for building and validating complex AI agent behaviors. At its core, the application employs a multi-agent "red teaming" architecture where a Critic agent, powered by a high-speed LLM like Groq LLaMA 3, performs an adversarial analysis of user-defined function-calling plans. This process identifies subtle logical flaws, semantic errors, and schema violations, culminating in the automated generation of an optimized "Golden Plan" and preventing unreliable agent actions. The developer experience is centered around an interactive workbench featuring the Monaco Editor, providing a familiar, code-centric workflow for rapid iteration.
Architecturally, the system is built on an **asynchronous Python backend** using **FastAPI**, ensuring high-performance handling of concurrent **LLM REST API calls**. Data integrity and strict schema validation are enforced at the **API boundary** using Pydantic models, a critical practice for building reliable AI services. The framework is strategically designed as a powerful synthetic data generation engine, creating structured (**plan, critique, golden_plan**) triplets ideal for fine-tuning smaller, more specialized models. The entire application is containerized with Docker and designed for serverless deployment on platforms like **Google Cloud Run**, demonstrating expertise across a modern tech stack including **Python, FastAPI, RESTful API design, Pydantic, JavaScript, the OpenAI SDK, and Docker for DevOps**. 

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/download%20(5).jpg"> **[Production-Grade Serverless RAG Application: A Full-Stack LLM System for Secure Document Analysis and Constitutional Compliance](https://github.com/lewis-hue/Qubiten-AI-Assistant.git)**

This production-grade, serverless web application is a proactive compliance advisor that translates complex constitutional law into actionable guidance for businesses, schools, and hospitals. At its core, the application uses a **Retrieval-Augmented Generation (RAG)** system powered by a **Groq LLaMA 3.1 LLM** and coordinated via **secure REST APIs** to deliver citation-backed answers, preventing AI hallucinations. The user experience is enhanced with **real-time streaming responses** and hands-free query input via **Google Cloud Speech-to-Text** for voice transcription. 

Architecturally, it ensures user privacy and scalability through a **stateless backend** with **secure client-side document processing** in the browser using **IndexedDB**. The entire system is containerized with **Docker** and deployed serverlessly on **Google Cloud Run** with an **automated CI/CD pipeline**, demonstrating expertise across a modern tech stack including **Python, Flask, REST APIs, JavaScript, LangChain, Vector Databases (FAISS), and the full suite of Google Cloud and Docker for DevOps**. 

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/AI-Powered-Web-Scraper-Data-Extraction-Platform/blob/main/download%20(4).jpg"> **[AI-Powered Web Scraper and Data Extraction Platform](https://github.com/lewis-hue/AI-Powered-Web-Scraper-Data-Extraction-Platform.git)**

This project is a scalable, cloud-based application designed for web scraping and data export management. It features **RESTful APIs** for initiating and monitoring scraping jobs, as well as exporting and downloading data. Built with a Flask backend, MongoDB for scalable data storage, and Docker containers for seamless deployment, the application is optimized for performance and horizontal scaling. Future enhancements include the potential integration of Celery for task queue management. 

**Skills and tools:** Flask, MongoDB, **RESTful APIs**, Docker, Cloud Hosting (AWS, GCP, Heroku), CI/CD, Scalable Architecture, Asynchronous Processing, Performance Optimization, Task Queue Management (Celery).

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/LLMs-and-RAG/blob/main/download%20(3).jpg"> **[Qubiten Compliance Chatbot: An LLM-Powered RAG System](https://github.com/lewis-hue/LLMs-and-RAG.git)**

Qubiten Compliance Chatbot is a Retrieval-Augmented Generation (RAG) system leveraging Google Vertex AI’s text-bison\@001 model and embeddings. Built with a Python Flask backend and HTML/CSS/JavaScript frontend, it ingests compliance documents, performs FAISS-based similarity search, and assembles prompts for the LLM via **modular REST APIs**. 

**Skills and tools:** RAG, LLM fine-tuning, Vertex AI, Flask, Python, FAISS/Pinecone, **RESTful APIs**, and UI development, ensuring accurate, scalable regulatory guidance using a fine-tuned knowledge base and chat interface.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/End-to-End-Data-Architecture-and-Analytics-Pipeline-on-AWS/blob/main/images.jpg"> **[End-to-End Data Architecture and Analytics Pipeline on AWS
](https://github.com/lewis-hue/End-to-End-Data-Architecture-and-Analytics-Pipeline-on-AWS.git)**

This project simulates the design of an end-to-end data engineering and analytics pipeline using AWS. It demonstrates the use of AWS services like Amazon EKS for container orchestration, Amazon S3 for data storage, AWS Glue for ETL processing, Amazon Athena for querying, Amazon SageMaker for machine learning, and Amazon QuickSight for data visualization. The pipeline integrates **internal REST APIs** to trigger data workflows and provide programmatic access to analytics. The pipeline simulates a scalable, secure architecture for ingesting, transforming, analyzing, and visualizing customer transactional data, providing business insights and predictive models in a telecommunications context.

**Skills & Tools:** Amazon Elastic Kubernetes Service (EKS), Amazon S3, AWS Glue, Amazon Athena, Amazon SageMaker, Amazon QuickSight, Apache Doris, **REST API integration**, data pipeline design and implementation, data ingestion, transformation, and feature engineering, scalable architecture creation, feature engineering, model development and training, predictive modeling for customer behavior analysis, secure and scalable cloud infrastructure design, end-to-end data pipeline integration and optimization, querying, reporting, business intelligence (BI) insights generation, and data-driven decision-making.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/Snowflake.jpg"> **[Fraud Detection and Financial Transaction Analysis Using Snowflake, Machine Learning, and Tableau](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-.git)**

This project showcases advanced SQL, Snowflake, and Tableau skills to analyze financial transactions for fraud detection and customer insights. Using Snowflake for data warehousing and SQL for data transformation, I built a robust ETL pipeline to process and stage transaction data. Key analyses include customer segmentation, fraud risk scoring, and transaction breakdowns. I developed interactive Tableau dashboards to visualize customer spending behavior and fraud risks. This project optimized fraud prevention, enhanced customer targeting, and improved financial operations through actionable insights, leveraging advanced analytics, data visualization, and cloud data infrastructure.

**Skills & Tools:** Snowflake, Advanced SQL, Data Modeling, Data Warehousing, ETL Pipelines, Tableau Dashboards, Data Visualization, Business Intelligence, Customer Segmentation, Fraud Analytics, KPI Monitoring, Data-Driven Decision Making, Cloud Analytics Infrastructure, Performance Optimization, Transaction Analysis, Risk Scoring Frameworks


#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Google_Ads_Analytics/blob/main/download.png"> **[Google Ads Campaign Optimization Using Amplitude Analytics](https://github.com/lewis-hue/Google_Ads_Analytics.git)**

This project utilizes Amplitude, a powerful product analytics tool, to optimize Google Ads campaigns through detailed analysis of user behavior and ad performance across platforms like Google, YouTube, and Google Display Network. By tracking key metrics such as clicks, conversions, cost, impressions, and interactions, we identify areas for improvement in targeting and engagement. The insights derived from Amplitude's marketing analytics enable better ad spend allocation, refined targeting strategies, and enhanced user journeys, ultimately improving conversion rates and maximizing customer lifetime value.

**Skills & Tools:** Product analytics, web analytics, Marketing analytics, Amplitude, and data visualisation.

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/Snowflake.jpg"> **[Fraud Detection and Financial Transaction Analysis Using Snowflake, Machine Learning, and Tableau](https://github.com/lewis-hue/Fraud-Detection-Financial-Transaction-Analysis-Snowflake-.git)**

This project showcases advanced SQL, Snowflake, and Tableau skills to analyze financial transactions for fraud detection and customer insights. Using Snowflake for data warehousing and SQL for data transformation, I built a robust ETL pipeline to process and stage transaction data. Key analyses include customer segmentation, fraud risk scoring, and transaction breakdowns. I developed interactive Tableau dashboards to visualize customer spending behavior and fraud risks. This project optimized fraud prevention, enhanced customer targeting, and improved financial operations through actionable insights, leveraging advanced analytics, data visualization, and cloud data infrastructure.

**Skills & Tools:** Snowflake, Advanced SQL, Data Modeling, Data Warehousing, ETL Pipelines, Tableau Dashboards, Data Visualization, Business Intelligence, Customer Segmentation, Fraud Analytics, KPI Monitoring, Data-Driven Decision Making, Cloud Analytics Infrastructure, Performance Optimization, Transaction Analysis, Risk Scoring Frameworks

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/Oracle.png"> **[Sales Forecasting and Marketing Optimization Using Python, Oracle, Machine Learning, and Power BI](https://github.com/lewis-hue/oracle-powerbi.git)**

This project showcases **data science** techniques and **business intelligence** strategies to optimize sales forecasting and marketing efforts using state-of-the-art tools and technologies. By leveraging **Python** for **Data Science**, **Machine Learning**, and **Oracle** for data storage and processing, the project develops an **end-to-end sales prediction pipeline**. The pipeline includes crucial steps such as **data preprocessing**, **feature engineering**, and **model training**, enabling market effectiveness.

**Skills & Tools:** Oracle Database, Python for Data Science, Pandas, NumPy, Scikit-learn, Machine Learning, Gradient Boosting, Predictive Modeling, Power BI, Data Visualization, ETL Pipelines, Advanced Analytics, Business Intelligence, Marketing ROI Optimization, Sales Forecasting, Hyperparameter Tuning, Regression Modeling.
##

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/lewis_page/blob/main/databricks.png"> **[Business Intelligence (BI): Sales Forecasting Dashboard (Databricks)](https://github.com/lewis-hue/BusinessIntelligence.git)**

This project demonstrates a comprehensive sales data analysis using **SQL** within **Databricks** on **Microsoft Azure**. The analysis covers product-level revenue, units sold, store performance, and geographic trends. A robust **ETL pipeline** was developed in Databricks to ingest and process transactional sales data across countries and stores. Key business insights were visualized via interactive dashboards to support strategic decision-making.

**Skills & Tools:** SQL, Databricks, Microsoft Azure, Business Intelligence, Data Visualization, Data Analysis, Sales Analytics, ETL Pipelines, Dashboarding, Retail Analytics

##

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/lewis_page/blob/main/Customer%20segmentation.png"> **[Data Analysis: Customer Segmentation and Behavior Analysis](https://github.com/lewis-hue/data_analysis.git)**

This project focuses on customer behavior analytics using **R** in **R Studio**, exploring the relationship between `TotalPurchase`, `Frequency`, and `Customer Lifetime Value (CLV)` through exploratory data analysis and correlation testing. Visualizations include bar graphs and scatterplots, supported by statistical metrics (correlation coefficients and p-values) to uncover actionable insights.


**Skills & Tools:** R, R Studio, Data Analysis, Correlation Analysis, Data Visualization, Customer Segmentation, CLV Modeling, Business Intelligence, Exploratory Data Analysis (EDA), Statistical Testing

##

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Data_Science_Profile/blob/main/BigQuery.jpg"> **[B2B SaaS Analysis Using Customer Data (BigQuery & Looker Studio)](https://github.com/lewis-hue/BigQuery.git)**

This project focuses on analyzing customer behavior, churn risk, and revenue generation for a B2B SaaS company using a variety of advanced data science techniques and tools. The objective is to uncover insights that can optimize customer acquisition, retention strategies, and revenue generation by leveraging the power of SQL, BigQuery, Looker Studio, and predictive modeling.

**Skills & Tools:** SQL, BigQuery, Looker Studio, Business Intelligence, Data Visualization, Data Analysis, Dashboarding
<br />

## Core Competencies


- **Methodologies**: Data Engineering, Data Analysis, Machine Learning, Deep Learning, Time Series Analysis, Natural Language Processing (NLP), ETL, ELT, Big Data Analytics, **REST API Architecture**
- **Languages**: Python (Pandas, Numpy, Scikit-Learn, Scipy, Keras, Matplotlib), R (Dplyr, Tidyr, Caret, Ggplot2), SQL (PostgreSQL, MySQL, BigQuery), Scala (Spark), C++
- **Tools**: Apache Spark, dbt, Docker, Kubernetes, Airflow, Tableau, Power BI, Looker Studio, Flask, FastAPI, PySpark, MS Excel, Google Sheets, AWS

## Certificates


- [IBM Data Engineering Specialization(IBM)](https://www.coursera.org/account/accomplishments/specialization/L2LPK72TSHIV)
- [AWS Cloud Solutions Architect(AWS)](https://www.coursera.org/account/accomplishments/professional-cert/certificate/YOI9L6540YBA)
- [Google Business Intelligence Specialization(Google)](https://www.coursera.org/account/accomplishments/specialization/2BO13KGKPD5V)
- [Python for Data Science, AI & Development (IBM)](https://www.coursera.org/account/accomplishments/verify/D433KOIGEMR5)
- [Machine Learning Models in Microsoft Azure (Microsoft)](https://www.coursera.org/account/accomplishments/verify/DM2KWMQBJ61M)
- [SQL and Relational Databases (IBM)](https://courses.cognitiveclass.ai/certificates/730619af9d6f4605abcf94d609d810d6)
- [Data Analysis with R Programming](https://www.coursera.org/account/accomplishments/verify/QBE3ZPA5Z7L0)
- [Scala (IBM)](https://courses.cognitiveclass.ai/certificates/7fa09c3eb5c94eaeaac9051512bc0870)
- [BigQuery for Data Analysts](https://www.coursera.org/account/accomplishments/verify/FXW8MAV2EWWJ)
- [Exploratory Data Analysis forMachine Learning (IBM)](https://www.coursera.org/account/accomplishments/verify/0M1V5IH0DPIM)
- [Data Analysis and Visualization with PowerBI](https://www.coursera.org/account/accomplishments/verify/1WJM24A7HZJ9)
- [Developing AI Applications withPython and Flask (IBM)](https://www.coursera.org/account/accomplishments/verify/E8KKQL3YJJIZ)
- [Modernizing DataLakes and Data Warehouses with Google Cloud](https://www.coursera.org/account/accomplishments/verify/IIR4VSGR470J)

