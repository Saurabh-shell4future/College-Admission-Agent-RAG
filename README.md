Markdown
# 🏛️ College Admission Agent (RAG-Based)

### 📌 Project Overview
This project implements an AI-powered **College Admission Agent** using a decoupled **Retrieval-Augmented Generation (RAG)** architecture. The system is engineered to automate the parsing, retrieval, and contextual summarization of admission guidelines, eligibility metrics, and institutional databases through natural language interaction. It effectively transforms static data into conversational intelligence, ensuring context-aware and zero-hallucination responses for prospective students.

The project was developed as part of the **IBM SkillsBuild AICTE Internship 2026** program, utilizing **IBM Cloud Lite** services, **Langflow orchestration**, and enterprise-grade **IBM Granite** AI infrastructure.

---

## 🎯 Problem Statement
Develop an automated, high-fidelity **College Admission Agent** that streamlines the student onboarding process by retrieving and summarizing admission policies, eligibility criteria, course availability, fee structures, deadlines, and institutional FAQs. The system must eliminate parametric hallucinations and ensure accurate, data-grounded responses using IBM Granite and Retrieval-Augmented Generation (RAG).

---

## 🛠️ Technologies Used
* **Orchestration Layer:** Langflow Core UI Engine
* **Cognitive Infrastructure:** IBM watsonx.ai Platform
* **Foundation LLM Engine:** IBM Granite Series (Enterprise Chat & Instruct Models)
* **Vector Database:** FAISS (Facebook AI Similarity Search) Local Indexer
* **Integration Workspace:** IBM watsonx Orchestrate Integration Gateway
* **Core Implementation:** Python 3.10+ & REST API Integration

---

## ✨ Key Features
* **Natural Language Admission Support:** Seamless handling of complex, multi-turn student queries.
* **Intelligent Course Guidance:** Automatically maps student profiles to eligible branches (Pharmacy, Technical Diploma, and B.Sc streams).
* **Factual Grounding:** Employs a strict zero-overlap data isolation strategy (`Chunk Size: 1000`, `Overlap: 0`) over a comprehensive dataset of **20,000 multi-variate records** to prevent data cross-contamination.
* **Vectorized Processing:** Lightning-fast semantic nearest-neighbor lookups using an in-memory FAISS vector space.
* **Enterprise Cloud Deployment:** Live integration hooks connecting the local backend pipeline directly with the cloud-hosted IBM watsonx Orchestrate client panel.

---

## 🏗️ System Architecture & Workflow

The system completely isolates data ingestion from runtime orchestration to guarantee low-latency processing (~1.5 to 2.8 seconds):

```text
[Raw Dataset: 20k Records] ──► [Langflow Text Splitter (\n, Overlap: 0)] ──► [FAISS Vector Index]
                                                                                    │
[User Natural Query] ──► [watsonx Orchestrate API Gateway Interface] ◄──────────────┘
         │
         ▼
[Custom JSON Parser Block] ──► [IBM watsonx.ai (IBM Granite Model)] ──► [Grounded Response]
Query Submission: User submits an admission or eligibility query through the frontend gateway.

Vector Conversion: The input string is transformed into a dense vector embedding in real time.

Similarity Match: FAISS performs an optimized matrix operation to locate the closest text nodes.

Context Extraction: Relevant data chunks are isolated and fed into a custom structural parser component.

Model Grounding: The compiled payload is packed into a strict system prompt boundary ({text}) and sent to the foundational IBM Granite model on IBM Cloud.

Execution Output: The model generates a completely grounded response and streams it back to the user interface.

💻 Project Implementations
1. Langflow-Based RAG Pipeline
Automated file ingestion parsing tabular multi-variate metrics (Attendance_Prediction.csv).

Context-preserving newline (\n) text splitting parameters.

Embedding generation and local FAISS vector indexing.

Custom JSON array parser node orchestration.

2. IBM watsonx Orchestrate Agent
Custom tool configuration (Agentic workflow & Get flow status background tracker API).

Standardized metadata-driven tool descriptions ensuring accurate model routing choices.

Live enterprise cloud workspace conversational deployment.

📂 Repository Structure
Plaintext
College-Admission-Agent-RAG/
│
├── README.md                  # Comprehensive Project Documentation
├── PPT/
│   └── Project_Presentation.pptx  # Core Technical Presentation Slides
├── Langflow/
│   ├── flow.json              # Exported Langflow Orchestration Graph
│   └── screenshots/           # Backend Pipeline Execution State Visuals
├── Watsonx-Orchestrate/
│   └── screenshots/           # Chat Widget & Live Cloud Tooling Visuals
├── Knowledge-Base/
│   └── documents/             # Sample Structured Data Sheets / FAQs
└── Images/
    └── architecture.png       # Core High-Level System Architecture Diagram
📊 Performance Metrics & Results
High Efficiency: Successfully executes dense semantic lookups over thousands of composite profile records within milliseconds.

Strict Constraint Adherence: Zero hallucination instances observed; outputs deterministic "Data not found" flags when inputs violate boundary values.

Scalability Ready: Drastically reduces manual administrative workload and query response queue times.

🔮 Future Scope
Voice-Driven Interfaces: Integrating automated speech-to-text pipelines for real-time telephonic counseling.

Managed Vector Infrastructure: Transitioning local FAISS indexes into highly scalable cloud vector databases like IBM watsonx.data.

Global Accessibility: Implementing multilingual processing arrays for regional language assistance.

✍️ Author
Saurabh Kumar Maurya Bachelor of Technology (B.Tech) — Electrical Engineering Rajkiya Engineering College, Ambedkar Nagar

🎓 Internship Recognition
Program: IBM SkillsBuild AICTE Internship 2026

Track: Artificial Intelligence & Enterprise Automation Cloud Pipelines
