# Projects - Lewis Muguna

Senior AI Engineer building production-grade agentic AI systems, LLM and RAG applications,
and the full-stack and cloud infrastructure that runs them. This is a focused selection of
my strongest work, each with a clear problem, a real architecture, and honest limitations.

Email: lewiemuguna417@gmail.com  ·  LinkedIn: www.linkedin.com/in/lewis-muguna-070080166

## Projects

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Muguna_Portfolio/blob/main/thumb-storeproof.png?raw=true"> **[StoreProof: Per-Store Catalog Verification for Musicians](https://github.com/lewis-hue/storeproof)**

Built for the micro1 Frontier Engineering Challenge 2026. Independent artists distribute through services like DistroKid, which deliver a release to 30+ stores, but "delivered" is not "live": songs silently fail to appear on some stores, and no dashboard reports which song is missing where. StoreProof checks each song against each store and classifies it live (with a link as proof), missing, or unverified, then auto-drafts an itemized re-distribution request to support.

The engineering discipline is the point: a store it cannot confirm is reported as unverified, never as a false missing (precision over recall). The search backend is pluggable so the core is testable without the network, it starts with one Docker command, and the README states its limitations and discloses that AI coding agents were used. A fuller, private version (Catalog Sentinel) extends this with attended real-browser catalog extraction.

**Stack:** TypeScript, Next.js, BullMQ, Redis, Docker, GitHub Actions CI.

<br clear="left"/>

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Muguna_Portfolio/blob/main/thumb-katiba.png?raw=true"> **[Katiba AI: AI-Powered Kenyan Constitution Assistant](https://github.com/lewis-hue/katibaai)**

A production RAG SaaS that makes the Constitution of Kenya searchable and conversational, with article-level citations grounded in retrieved evidence. It runs as a multi-service system: a FastAPI backend with Celery workers, Milvus vector search, MongoDB persistence, Redis for pub/sub and rate limiting, Keycloak identity, and a full Lago billing stack with Stripe and M-Pesa, deployed on Google Cloud with Cloud Build CI/CD. The backend is extensively tested.

This repository is a case study (product screenshots and an architecture overview); the full source is private and available to walk through on request.

**Stack:** FastAPI, Celery, Milvus, MongoDB, Redis, Keycloak, Lago, Stripe, M-Pesa, GCP.

<br clear="left"/>

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Muguna_Portfolio/blob/main/thumb-avvo.png?raw=true"> **[AVVO: Agentic Viral Video Orchestrator](https://github.com/lewis-hue/Agentic-Viral-Video-Orchestrator)**

A multi-agent system that discovers viral trends, generates short-form videos, and distributes them across social platforms. Specialized agents own each stage (trend discovery, story ideation, video generation, brand safety, publishing, optimization) behind a FastAPI backend, with a React and Vite frontend and Docker plus Kubernetes deployment manifests.

**Stack:** Python, FastAPI, LangChain, Gemini, FAISS, Celery, Redis, Cloudinary, React, Docker, Kubernetes.

<br clear="left"/>

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Muguna_Portfolio/blob/main/thumb-flexliving.png?raw=true"> **[Flex Living: AI Property-Management Analytics](https://github.com/lewis-hue/Flex-Living)**

Helps property managers understand their portfolio from guest reviews. It runs LLM-based sentiment and topic analysis on each review with a Groq-hosted model, pushes updates to the UI in real time through MongoDB change streams and WebSocket, and renders per-property analytics in a React dashboard. Deployed on Google Cloud Run with Cloud Build.

**Stack:** FastAPI, MongoDB, Groq LLM, WebSocket, React, TypeScript, Vite, Recharts, Docker, Nginx, GCP.

<br clear="left"/>

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Muguna_Portfolio/blob/main/thumb-paxform.png?raw=true"> **[PAXFORM: Appointment Booking System](https://github.com/lewis-hue/PAXFORM)**

A full-stack appointment booking system with a public booking interface and an admin dashboard. Bookings sync to Google Calendar; admins get JWT-authenticated CRUD, real-time WebSocket notifications, and SendGrid email confirmations. Containerized and deployed on Google Cloud Platform.

**Stack:** NestJS, PostgreSQL, TypeORM, React, Vite, Tailwind, shadcn/ui, Google Calendar API, SendGrid, Docker, GCP.

<br clear="left"/>

#
<img align="left" width="250" height="150" src="https://github.com/lewis-hue/Lewis_Muguna_Portfolio/blob/main/thumb-outreach.png?raw=true"> **[Outreach Automation: LangGraph Pipeline](https://github.com/lewis-hue/outreach-automation)**

A LangGraph-based outreach pipeline that models scraping, validation, and LLM-driven message generation as a graph of composable, independently testable steps, with LangSmith tracing and Pydantic-validated stages. A work in progress, and labeled as such.

**Stack:** Python, LangGraph, LangChain, LangSmith, Pydantic.

<br clear="left"/>

## Core Competencies

- **AI Engineering:** Agentic and multi-agent systems, RAG pipelines, retrieval and evaluation, LLM integration (OpenAI, Anthropic, Groq, Gemini), function-call validation, AI safety and governance.
- **Backend & Full-Stack:** Python (FastAPI, Flask), TypeScript (Next.js, React, NestJS, Fastify), PostgreSQL, MongoDB, Redis, background workers (BullMQ, Celery).
- **MLOps, DevOps & Cloud:** Docker, Kubernetes, GitHub Actions, Terraform, AWS and GCP (Cloud Run, Cloud Build), Keycloak, OAuth2/JWT, AWS KMS.

## Certifications (selected)

- IBM Generative AI Engineering with LLMs (Specialization)
- AWS Cloud Solutions Architect
- IBM Data Engineering (Specialization)
- micro1 Senior AI Engineer Certification
