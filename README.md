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
Natural Language Admission Support for multi-turn queries
Intelligent Course Guidance (Pharmacy, Diploma, B.Sc, etc.)
Factual Grounding using zero-overlap chunking (Chunk Size: 1000, Overlap: 0)
Fast semantic search using FAISS vector indexing
Enterprise-grade deployment using IBM watsonx Orchestrate
🏗️ System Architecture & Workflow
[Raw Dataset: 20,000 Records]
        │
        ▼
[Langflow Text Splitter (\n, Overlap: 0)]
        │
        ▼
[FAISS Vector Index]
        │
        ▼
[User Natural Language Query]
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
User submits admission-related query via frontend
Query is converted into embeddings
FAISS performs similarity search on dataset
Relevant context chunks are retrieved
Data is passed to IBM Granite model
Final grounded response is generated and returned
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
Live cloud conversational deployment
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
⚡ High-speed semantic retrieval (milliseconds response time)
🎯 Zero-hallucination output behavior with strict grounding
📉 Automatic fallback: “Data not found” for invalid queries
🚀 Scalable architecture for enterprise admission systems
🔮 Future Scope
🎙️ Voice-based admission counseling (Speech-to-Text integration)
☁️ Migration to cloud vector databases (IBM watsonx.data)
🌍 Multilingual support for regional accessibility
🤖 Enhanced autonomous AI agent capabilities
✍️ Author

Saurabh Kumar Maurya
B.Tech – Electrical Engineering
Rajkiya Engineering College, Ambedkar Nagar

🎓 Internship Recognition
Program: IBM SkillsBuild AICTE Internship 2026
Track: Artificial Intelligence & Enterprise Automation Cloud Pipelines
