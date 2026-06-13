🏛️ College Admission Agent (RAG-Based)
📌 Project Overview

This project implements an AI-powered College Admission Agent using a decoupled Retrieval-Augmented Generation (RAG) architecture. The system is engineered to automate the parsing, retrieval, and contextual summarization of admission guidelines, eligibility metrics, and institutional databases through natural language interaction. It transforms static data into conversational intelligence, ensuring context-aware and zero-hallucination responses for prospective students.

The project was developed as part of the IBM SkillsBuild AICTE Internship 2026 program, utilizing IBM Cloud Lite services, Langflow orchestration, and IBM Granite AI infrastructure.

🎯 Problem Statement

Develop an automated, high-fidelity College Admission Agent that streamlines the student onboarding process by retrieving and summarizing:

Admission policies
Eligibility criteria
Course availability
Fee structures
Deadlines
Institutional FAQs

The system must eliminate hallucinations and ensure accurate, data-grounded responses using IBM Granite and RAG.

🛠️ Technologies Used
Orchestration Layer: Langflow Core UI Engine
Cognitive Infrastructure: IBM watsonx.ai Platform
Foundation LLM Engine: IBM Granite Series (Enterprise Chat & Instruct Models)
Vector Database: FAISS (Facebook AI Similarity Search) Local Indexer
Integration Workspace: IBM watsonx Orchestrate Integration Gateway
Core Implementation: Python 3.10+ & REST API Integration
✨ Key Features
Natural Language Admission Support: Handles complex multi-turn student queries
Intelligent Course Guidance: Maps student profiles to eligible academic programs (Pharmacy, Diploma, B.Sc, etc.)
Factual Grounding: Zero-overlap chunking strategy (Chunk Size: 1000, Overlap: 0) to avoid data contamination
Vectorized Processing: Fast semantic search using FAISS nearest-neighbor indexing
Enterprise Deployment: Integrated with IBM watsonx Orchestrate cloud environment
🏗️ System Architecture & Workflow

The system separates data ingestion from runtime orchestration to ensure low latency (~1.5–2.8 seconds):

[Raw Dataset: 20k Records]
        │
        ▼
[Langflow Text Splitter (\n, Overlap: 0)]
        │
        ▼
[FAISS Vector Index]
        │
        ▼
[User Natural Query]
        │
        ▼
[watsonx Orchestrate API Gateway]
        │
        ▼
[Custom JSON Parser Block]
        │
        ▼
[IBM watsonx.ai (Granite Model)]
        │
        ▼
[Grounded Response]
🔄 Workflow Steps
Query Submission: User sends an admission-related query via frontend
Vector Conversion: Query is converted into embeddings
Similarity Search: FAISS retrieves nearest matching records
Context Extraction: Relevant chunks are isolated
Model Grounding: Data is injected into IBM Granite via strict prompt structure
Response Generation: Final grounded response is returned to user
💻 Project Implementations
1. Langflow-Based RAG Pipeline
CSV ingestion (e.g., Attendance_Prediction.csv)
Context-preserving text splitting
Embedding generation
FAISS indexing
JSON parser orchestration
2. IBM watsonx Orchestrate Agent
Custom tool configuration for agent workflows
Metadata-driven routing system
Live cloud deployment for conversational AI
Flow status tracking via API integration
📂 Repository Structure
College-Admission-Agent-RAG/
│
├── README.md
├── PPT/
│   └── Project_Presentation.pptx
│
├── Langflow/
│   ├── flow.json
│   └── screenshots/
│
├── Watsonx-Orchestrate/
│   └── screenshots/
│
├── Knowledge-Base/
│   └── documents/
│
└── Images/
    └── architecture.png
📊 Performance Metrics & Results
⚡ High efficiency semantic search over thousands of records in milliseconds
🎯 Strict constraint adherence with zero hallucination output behavior
📉 Automatic fallback to “Data not found” when inputs are outside dataset scope
🚀 Scalable architecture suitable for enterprise-level admission systems
🔮 Future Scope
🎙️ Voice-based admission counseling (Speech-to-Text integration)
☁️ Migration to scalable vector DBs (IBM watsonx.data)
🌍 Multilingual support for regional accessibility
🤖 Enhanced AI agent autonomy with tool-augmented reasoning
✍️ Author

Saurabh Kumar Maurya
B.Tech – Electrical Engineering
Rajkiya Engineering College, Ambedkar Nagar

🎓 Internship Recognition
Program: IBM SkillsBuild AICTE Internship 2026
Track: Artificial Intelligence & Enterprise Automation Cloud Pipelines
