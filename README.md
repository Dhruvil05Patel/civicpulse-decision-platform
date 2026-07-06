# CivicPulse AI 🏙️

### *An Agentic Decision Intelligence & Multimodal Automation Engine for Smarter Communities*

CivicPulse AI is an intelligent, serverless command center designed for municipal stakeholders, utility operators, and community leaders. By bridging the gap between raw, unstructured citizen data (photos, voice logs, text) and automated real-world operations, CivicPulse turns community feedback into decisive, real-time municipal action.

---

## 🚀 The Core Challenge & Solution

**The Problem:** Modern urban centers generate immense amounts of data, yet infrastructure management remains slow and reactive. Critical issues like water main breaks, hazardous road damage, or utility failures are buried under manual triage queues, stalling emergency response times and wasting vital public resources.

**The Solution:** CivicPulse acts as an autonomous triage and response layer. It ingests multimodal citizen reports, uses Generative AI to understand context and gauge severity instantly, maps the data for city coordinators, and autonomously triggers backend workflows (like dispatching crews or alerting emergency networks) via agentic function calling.

---

## 🛠️ Tech Stack & Google Cloud Architecture

CivicPulse is built completely within the Google Cloud ecosystem for maximum scalability, security, and performance:

* **Frontend Interface:** Next.js / React — A sleek, map-centric decision dashboard featuring a natural language conversational analytics sidebar for city coordinators.
* **AI Engine & Orchestration:** **Vertex AI (Gemini 1.5 Flash)** — Leveraged for ultra-fast multimodal classification (image + text) and intelligent tool/function calling.
* **Database & RAG Layer:** **AlloyDB / Cloud SQL** — Built-in geospatial indexing handles rapid coordinate mapping alongside vector embeddings of municipal Standard Operating Procedures (SOPs).
* **Serverless Compute & Automation:** **Cloud Run** & **Cloud Functions** — Handles decoupled event processing, API endpoints, and triggers intelligent outbound webhooks to maintenance management systems.

---

## 🏗️ System Workflow

1. **Ingestion:** A citizen uploads an image and short text describing a infrastructure hazard via the frontend app.
2. **Analysis:** The payload is processed by `gemini-1.5-flash` inside Vertex AI, extracting structured insights: Category, Severity, and Text Summary.
3. **Agentic Execution:** If a critical threshold is crossed, the Gemini agent autonomously executes a native function tool, triggering a Google Cloud Function.
4. **Action:** The Cloud Function dispatches an automated webhook notification to localized field teams, instantly updating the city coordinator's map dashboard in real-time.

---

## 💻 Setup & Installation (Local Development)

### Prerequisites
* Node.js (v18+)
* Google Cloud CLI installed and authenticated
* Vertex AI API enabled on your GCP project

### 1. Clone the Repository
```bash
git clone [https://github.com/YOUR_USERNAME/civic-pulse-ai.git](https://github.com/YOUR_USERNAME/civic-pulse-ai.git)
cd civic-pulse-ai
